# AutoSDV Containerization: Complete Guide

**Version:** 2025.11-containerization  
**Last Updated:** November 19, 2025  
**Architecture:** ARM64 (Jetson AGX Orin)  
**Build Platform:** x86_64 with cross-compilation

---

## Table of Contents

1. [Overview](#overview)
2. [Host Side Operations](#host-side-operations)
   - [Cross-Platform Build Setup](#cross-platform-build-setup)
   - [Docker Image Build Issues](#docker-image-build-issues)
   - [Repository Management](#repository-management)
3. [Container Side Operations](#container-side-operations)
   - [Dependency Installation](#dependency-installation)
   - [Build System Issues](#build-system-issues)
   - [Runtime Errors](#runtime-errors)
4. [Launch Configuration](#launch-configuration)
5. [Hardware Checklist](#hardware-checklist)
6. [Quick Reference](#quick-reference)

---

## Overview

This document comprehensively tracks all issues, solutions, and configurations for the AutoSDV containerization project, organized by where operations occur: **host machine** or **Docker container**.

**Key Achievements:**
- ✅ Cross-platform ARM64 Docker image builds on x86_64 hosts
- ✅ Automated deployment workflow with jetson_setup.sh
- ✅ Dual launch modes: simulation (no hardware) and hardware (full sensors)
- ✅ RViz enabled with automatic X11 configuration
- ✅ All 42 ROS packages building successfully

---

# Host Side Operations

## Cross-Platform Build Setup

### Issue H1.1: Cannot Build ARM64 Image on x86 Host
**Date:** November 13-18, 2025  
**Location:** Development machine (x86_64)  
**Error:** `docker build` cannot create ARM64 images on x86_64 architecture  

**Root Cause:** Standard Docker build doesn't support cross-architecture compilation

**Solution:**
```bash
# 1. Install QEMU for ARM64 emulation
sudo apt-get install qemu binfmt-support qemu-user-static
docker run --privileged --rm tonistiigi/binfmt --install all

# 2. Enable Docker buildx
docker buildx create --name autosdv-builder --use

# 3. Verify platform support
docker buildx inspect --bootstrap
```

**Files Modified:**
- `docker/Makefile`: Added `buildx` support and `--platform linux/arm64` flag

**Verification:**
```bash
cd docker/
make bootstrap  # One-time setup
make build      # Should build for ARM64
```

---

### Issue H1.2: Git Submodule Repository Mismatch
**Location:** Host during Docker build  
**Error:** 
```
fatal: reference is not a tree: 798e7c415a310a85576d1c21e62ed37ca0a0bcd5
```

**Root Cause:** Dockerfile cloned from upstream `NEWSLabNTU/AutoSDV` but tried to checkout commits from fork `misuhsieh001/AutoSDV-containerization`

**Solution:**
```bash
# Makefile now auto-detects repository URL from git config
REPO_URL = $(shell cd .. && git config --get remote.misuhsieh.url || git config --get remote.origin.url)

# Dockerfile uses dynamic repository
ARG REPO_URL=https://github.com/misuhsieh001/AutoSDV-containerization.git
RUN git clone --recursive ${REPO_URL} /AutoSDV
```

**Files Modified:**
- `docker/Dockerfile`: Added `ARG REPO_URL` parameter
- `docker/Makefile`: Auto-detect and pass `REPO_URL` as build arg

---

### Issue H1.3: Nested Git Submodules Not Initialized
**Location:** Host during Docker build  
**Error:** 
```
fatal: destination path 'zed-ros2-interfaces' already exists
```

**Root Cause:** `git clone --recursive` only initializes one level of submodules

**Solution:**
```dockerfile
# In Dockerfile, after cloning
RUN cd /AutoSDV && \
    git submodule update --init --recursive
```

**Files Modified:**
- `docker/Dockerfile`: Added explicit nested submodule initialization

---

### Issue H1.4: X11 Authorization for RViz
**Location:** Host machine (Jetson or x86 with display)  
**Error:** 
```
Authorization required, but no authorization protocol specified
Error: Can't open display: :1
```

**Root Cause:** Docker container lacks permission to access X11 display server

**Solution (Automated):**
```makefile
# docker/Makefile automatically runs before container start
run:
	@if command -v xhost >/dev/null 2>&1; then \
		echo "Enabling X11 access for Docker containers..."; \
		xhost +local:docker >/dev/null 2>&1 || true; \
	fi
```

**Manual Solution:**
```bash
# On host, before running container
xhost +local:docker
```

**Files Modified:**
- `docker/Makefile`: Added automatic `xhost +local:docker` in `run` target

---

### Issue H1.5: Docker Image Detection for Fresh Deployments
**Location:** Fresh Jetson deployment  
**Error:** 
```
ERROR: No Docker image found!
```

**Root Cause:** Makefile checked local images before DockerHub, fresh Jetson has no local build

**Solution:**
```makefile
# Prioritize DockerHub image over local build
DOCKERHUB_IMAGE = misuhsieh001/autosdv:2025.11-latest
IMAGE_TO_USE = $(shell \
	if docker inspect $(DOCKERHUB_IMAGE) >/dev/null 2>&1; then \
		echo $(DOCKERHUB_IMAGE); \
	elif docker inspect $(IMAGE_NAME):$(SHORT_HASH) >/dev/null 2>&1; then \
		echo $(IMAGE_NAME):$(SHORT_HASH); \
	fi)
```

**Files Modified:**
- `docker/Makefile`: Reordered image detection to check DockerHub first

---

### Issue H1.6: Automated Jetson Setup Script
**Location:** Fresh Jetson AGX Orin deployment  
**Problem:** Manual setup too complex, prone to errors

**Solution:** Created comprehensive `jetson_setup.sh`:
```bash
#!/bin/bash
# Automates: Docker install, NVIDIA toolkit, repo clone, container launch

# Key features:
- Detects existing installations
- Handles git submodules with --recursive
- Uses $HOME/AutoSDV-containerization for workspace
- Pulls DockerHub image automatically
- Launches container when done
```

**Files Created:**
- `jetson_setup.sh`: Complete automation script
- `DEPLOYMENT_ON_NEW_ARM64.md`: Deployment guide

**Usage:**
```bash
wget https://raw.githubusercontent.com/misuhsieh001/AutoSDV-containerization/2025.11-containerization/jetson_setup.sh
chmod +x jetson_setup.sh
./jetson_setup.sh
```

---

# Container Side Operations

## Dependency Installation

### Issue C2.1: ROS 2 Packages Not Found During Build
**Location:** Inside Docker build process  
**Error:** 
```
E: Unable to locate package ros-humble-cv-bridge
```

**Root Cause:** ROS 2 packages installed before ROS repository was configured by `setup-dev-env.sh`

**Solution:**
```dockerfile
# Step 1: Install non-ROS packages first
RUN apt-get install -y opencv-contrib-python i2c-tools wget

# Step 2: Run setup script to configure ROS repos
RUN cd /AutoSDV && ./setup-dev-env.sh

# Step 3: Source ROS and install ROS packages
RUN /bin/bash -c "source /opt/ros/humble/setup.bash && \
    apt-get install -y ros-humble-cv-bridge ros-humble-vision-opencv"
```

**Files Modified:**
- `docker/Dockerfile`: Split package installation into pre-ROS and post-ROS steps

---

### Issue C2.2: ZED SDK Installation for JetPack 6.0
**Location:** Docker container during build  
**Requirement:** ZED SDK for L4T 36.3 (JetPack 6.0)

**Solution:**
```dockerfile
# Install ZED SDK 4.0 for JetPack 6.0 (L4T 36.3)
RUN apt-get update && apt-get install -y wget lsb-release zstd
RUN wget -q -O ZED_SDK_Linux.run \
    https://download.stereolabs.com/zedsdk/4.0/l4t36.3/jetsons && \
    chmod +x ZED_SDK_Linux.run && \
    ./ZED_SDK_Linux.run -- silent skip_tools skip_cuda && \
    rm ZED_SDK_Linux.run
```

**Files Modified:**
- `docker/Dockerfile`: Added ZED SDK installation

---

### Issue C2.3: Seyond LiDAR SDK Architecture Mismatch
**Location:** Container during colcon build  
**Error:**
```
/usr/bin/ld: libinnolidarsdkclient.a: error adding symbols: file in wrong format
Relocations in generic ELF (EM: 62)
```

**Root Cause:** Precompiled x86-64 static libraries (`.a` files) in seyond SDK cannot link to ARM64 build

**Why It Works on ARM Host:** SDK compiled from source for ARM64 on real Jetson

**Solution:**
```dockerfile
# Force rebuild SDK from source for ARM64
RUN cd /AutoSDV/src/drivers/seyond/robin_ros2/inno-lidar-sdk && \
    rm -f lib/*.a && \
    cd build && \
    bash build_unix.sh
```

**Files Modified:**
- `docker/Dockerfile`: Added seyond SDK compilation step

---

## Build System Issues

### Issue C3.1: ZED SDK Not Found During CMake Configuration
**Location:** Container during `colcon build`  
**Error:**
```
CMake Error: Could not find a package configuration file provided by "ZED"
```

**Root Cause:** ZED SDK installed but `CMAKE_PREFIX_PATH` not set

**Solution:**
```makefile
# In top-level Makefile
build:
	colcon build --symlink-install \
		--cmake-args -DCMAKE_PREFIX_PATH="/usr/local/zed"
```

**Files Modified:**
- `Makefile`: Added ZED SDK path to CMake arguments

---

### Issue C3.2: Only 4 Packages Building (Submodule Issue)
**Location:** Container after `make build`  
**Problem:** Only 4 packages built instead of 42

**Root Cause:** Git submodules not initialized in cloned repository

**Solution:**
```bash
# In jetson_setup.sh
git clone --recursive https://github.com/misuhsieh001/AutoSDV-containerization.git
cd AutoSDV-containerization
git submodule update --init --recursive
```

**Files Modified:**
- `jetson_setup.sh`: Added `--recursive` flag and explicit submodule update

---

## Runtime Errors

### Issue C4.1: Missing Perception Model File (BLOCKING)
**Location:** Container during launch  
**Error:**
```
[ERROR] [launch]: Caught exception in launch (see debug for traceback): 
[Errno 2] No such file or directory: 
'data/lidar_centerpoint/centerpoint_tiny_ml_package.param.yaml'
```

**Status:** 🔴 **BLOCKING** - Prevents system startup in hardware mode

**Solution:**
```bash
# Option 1: Use simulation mode (no perception)
make launch-sim

# Option 2: Download perception models (if available)
cd /AutoSDV/data
# Download centerpoint models here
```

---

### Issue C4.2: Actuator Node - PCA9685 I2C PWM Driver
**Location:** Container during hardware launch  
**Error:**
```
OSError: [Errno 121] Remote I/O error
File "Adafruit_PCA9685/PCA9685.py", line 75, in __init__
```

**Cause:** PCA9685 PWM chip not connected on I2C bus  
**Status:** ✅ **EXPECTED** without hardware

**Solution:**
```bash
# Use simulation mode
make launch-sim  # Sets launch_vehicle:=false
```

---

### Issue C4.3: Velocity Report - Jetson.GPIO Module
**Location:** Container during hardware launch  
**Error:**
```
ModuleNotFoundError: No module named 'Jetson'
```

**Cause:** Jetson.GPIO Python module not installed in container  
**Status:** ✅ **EXPECTED** in Docker (GPIO not accessible)

**Solution:**
```dockerfile
# Add to Dockerfile (optional, GPIO won't work in Docker anyway)
RUN pip install Jetson.GPIO
```

**Or use simulation:**
```bash
make launch-sim
```

---

### Issue C4.4: GPS Serial Port Missing
**Location:** Container during hardware launch  
**Error:**
```
serial.serialutil.SerialException: [Errno 2] could not open port /dev/ttyUSB0
```

**Cause:** No GPS device connected  
**Status:** ✅ **EXPECTED** without GPS hardware

**Solution:**
```bash
make launch-sim  # Sets use_gnss:=false
```

---

### Issue C4.5: NumPy 2.0 Compatibility with transforms3d
**Location:** Container during GPS processing  
**Error:**
```
AttributeError: `np.maximum_sctype` was removed in the NumPy 2.0 release.
File "transforms3d/quaternions.py", line 26
```

**Status:** 🟡 **SOFTWARE BUG**

**Solution:**
```dockerfile
# Add to Dockerfile
RUN pip install "numpy<2.0" "transforms3d>=0.4.0"
```

---

### Issue C4.6: MPU9250 IMU I2C Communication
**Location:** Container during hardware launch  
**Error:**
```
Error waking sensor
OSError: Remote I/O error
```

**Cause:** MPU9250 IMU not connected on I2C  
**Status:** ✅ **EXPECTED** without hardware

**Solution:**
```bash
make launch-sim  # Sets launch_sensing_driver:=false
```

---

### Issue C4.7: Seyond LiDAR Network Connection
**Location:** Container during hardware launch  
**Error:**
```
get_connection timeout for 5.00000s
Error opening HTTP connection (172.168.1.10:8010)
```

**Cause:** Seyond LiDAR not connected at IP 172.168.1.10  
**Status:** ✅ **EXPECTED** without LiDAR

**Solution:**
```bash
make launch-sim  # Sets launch_sensing_driver:=false
```

---

### Issue C4.8: ROS 2 DDS Communication Failure - Topics Not Discovered
**Date:** November 20, 2025  
**Location:** ARM64 Docker container  
**Error:** 
```
# After launching AutoSDV with make launch-sim:
ros2 topic list
# Output: Only /parameter_events and /rosout (should show 400+ topics)

ros2 node list
# Output: No nodes listed (should show 40+ nodes)

# However, system processes are running:
ps aux | grep ros2  # Shows 33 processes running
```

**Root Cause #1: Conflicting CYCLONEDDS_URI Environment Variable**

The ARM64 L4T Docker base image (nvcr.io/nvidia/l4t-tensorrt:r8.6.2-devel) sets a default environment variable:
```bash
CYCLONEDDS_URI=file:///opt/autoware/cyclonedds.xml
```

This causes **two critical problems**:

1. **Forces CycloneDDS even when Fast-RTPS is specified:**
   - Even though Makefile sets `export RMW_IMPLEMENTATION=rmw_fastrtps_cpp`
   - ROS 2 detects CYCLONEDDS_URI and switches to CycloneDDS middleware
   - The config file `/opt/autoware/cyclonedds.xml` doesn't exist or has wrong settings

2. **Middleware mismatch between launch and CLI tools:**
   - Launch system uses CycloneDDS (due to CYCLONEDDS_URI)
   - CLI tools (`ros2 topic list`) default to Fast-RTPS
   - **Different DDS implementations cannot discover each other's nodes/topics**

**Root Cause #2: Missing ROS_LOCALHOST_ONLY Setting**

Fast-RTPS by default uses UDP multicast for node discovery, which fails in Docker because:
- Docker bridge networks don't support multicast properly
- Container network isolation prevents multicast packets from propagating
- Result: Nodes can't discover each other even though they're running

**Symptoms:**
- ✅ Nodes are running (confirmed by process count)
- ✅ Launch completes without errors (log shows all nodes starting)
- ❌ `ros2 topic list` shows only 2 topics
- ❌ `ros2 node list` shows nothing
- ❌ Nodes are invisible to each other (DDS discovery failure)

**Diagnosis Steps Taken:**

1. **Verified node processes running:**
   ```bash
   ps aux | grep ros2 | wc -l  # Shows 33 processes
   ```

2. **Checked DDS daemon:**
   ```bash
   ros2 daemon status  # Shows "The daemon is running"
   ros2 daemon stop && ros2 daemon start  # No improvement
   ```

3. **Discovered conflicting environment variable:**
   ```bash
   echo $CYCLONEDDS_URI
   # Output: file:///opt/autoware/cyclonedds.xml
   ```

**Solution:**

Modified `Makefile` to properly configure DDS environment:

```makefile
# Before (BROKEN):
launch-sim:
	@/bin/bash -c ' \
		set -e; \
		source install/setup.bash; \
		export RMW_IMPLEMENTATION=rmw_fastrtps_cpp; \
		ros2 launch autosdv_launch autosdv.launch.yaml \
			launch_rviz:=true \
			launch_vehicle:=false \
			launch_sensing_driver:=false \
			launch_perception:=false \
			use_gnss:=false \
	'

# After (WORKING):
launch-sim:
	@/bin/bash -c ' \
		set -e; \
		source install/setup.bash; \
		unset CYCLONEDDS_URI; \
		export ROS_LOCALHOST_ONLY=1; \
		export ROS_DOMAIN_ID=0; \
		export RMW_IMPLEMENTATION=rmw_fastrtps_cpp; \
		ros2 launch autosdv_launch autosdv.launch.yaml \
			launch_rviz:=true \
			launch_vehicle:=false \
			launch_sensing_driver:=false \
			launch_perception:=false \
			use_gnss:=false \
	'
```

**Key Changes:**

1. **`unset CYCLONEDDS_URI`** - Removes conflicting environment variable
2. **`export ROS_LOCALHOST_ONLY=1`** - Forces all DDS communication through localhost (127.0.0.1)
   - Bypasses multicast issues in Docker
   - Ensures all nodes can discover each other via loopback interface
3. **`export ROS_DOMAIN_ID=0`** - Explicitly sets ROS domain (default is 0)
4. **`export RMW_IMPLEMENTATION=rmw_fastrtps_cpp`** - Uses Fast-RTPS (now actually works)

**Files Modified:**
- `Makefile`: Updated both `launch-sim` and `launch-hw` targets with DDS environment fixes

**Verification:**

After applying the fix:
```bash
# Terminal 1: Launch system
cd /AutoSDV
make launch-sim

# Terminal 2: Check topics (must use same environment!)
unset CYCLONEDDS_URI
export ROS_LOCALHOST_ONLY=1
export ROS_DOMAIN_ID=0
export RMW_IMPLEMENTATION=rmw_fastrtps_cpp

ros2 topic list | wc -l
# Output: 400+ topics ✅

ros2 node list | wc -l  
# Output: 40+ nodes ✅
```

**Important Notes:**

1. **CLI tools must use same DDS configuration:**
   - When running `ros2` commands in another terminal, you MUST set the same environment variables
   - Otherwise CLI tools won't see the nodes (DDS mismatch)

2. **ROS_LOCALHOST_ONLY is critical for Docker:**
   - This is the key setting for container environments
   - Forces unicast communication via localhost instead of multicast
   - Works reliably in all Docker networking modes

3. **Alternative: Use CycloneDDS properly:**
   ```makefile
   # If you prefer CycloneDDS instead of Fast-RTPS:
   export RMW_IMPLEMENTATION=rmw_cyclonedds_cpp
   export CYCLONEDDS_URI=file:///AutoSDV/cyclonedds.xml
   # Make sure cyclonedds.xml exists and is configured for Docker
   ```

**Background: What is RMW_IMPLEMENTATION?**

RMW (ROS MiddleWare) is the abstraction layer that lets ROS 2 use different DDS implementations:

- **`rmw_fastrtps_cpp`** - Fast-RTPS/Fast-DDS (default, from eProsima)
  - Pros: Well-tested, feature-rich, default choice
  - Cons: Multicast issues in Docker without ROS_LOCALHOST_ONLY

- **`rmw_cyclonedds_cpp`** - CycloneDDS (from Eclipse Foundation)
  - Pros: Better Docker support, lower latency
  - Cons: Requires separate installation, needs proper config file

**Why This Matters:**

Different DDS implementations are **completely incompatible**:
- Fast-RTPS nodes cannot talk to CycloneDDS nodes
- If launch uses CycloneDDS but CLI tools use Fast-RTPS, you see nothing
- Must ensure ALL processes use the same RMW_IMPLEMENTATION

**Status:** ✅ **RESOLVED**  
**Impact:** Critical - System appeared broken but was just a DDS discovery issue  
**Lesson Learned:** Always check for conflicting environment variables in Docker base images

---

### Issue C4.9: DDS Multicast Failures (Legacy Issue)
**Location:** Container during ROS node communication  
**Error:**
```
IP_MULTICAST_IF failed: No such device
```

**Root Cause:** Docker container network doesn't support multicast properly

**Solution (Old Method - Now superseded by ROS_LOCALHOST_ONLY):**
```xml
<!-- cyclonedds.xml -->
<CycloneDDS>
  <Domain>
    <General>
      <AllowMulticast>false</AllowMulticast>
      <NetworkInterfaceAddress>lo</NetworkInterfaceAddress>
    </General>
  </Domain>
</CycloneDDS>
```

**Modern Solution:**
Use `ROS_LOCALHOST_ONLY=1` environment variable (works with any DDS implementation)

**Files Modified:**
- `cyclonedds.xml`: Disabled multicast, use loopback interface (if using CycloneDDS)
- `Makefile`: Added ROS_LOCALHOST_ONLY=1 (recommended approach)

---

# Launch Configuration

## Launch Modes

### Simulation Mode (No Hardware Required)
```bash
make launch-sim
```

**Configuration:**
- `launch_rviz: true` (GUI enabled - requires X11)
- `launch_vehicle: false` (no GPIO/I2C)
- `launch_sensing_driver: false` (no sensors)
- `launch_perception: false` (no TensorRT)
- `use_gnss: false` (no GPS)

**Use Cases:**
- Testing in Docker container
- Development on x86 PC
- Clean Jetson without sensors

---

### Hardware Mode (Full Sensor Suite)
```bash
make launch-hw
```

**Configuration:**
- `launch_rviz: true` (GUI enabled)
- `launch_vehicle: true` (GPIO for motors)
- `launch_sensing_driver: true` (LiDAR, camera, IMU)
- `launch_perception: true` (TensorRT models)
- `use_gnss: true` (GPS)

**Requirements:**
- Real Jetson AGX Orin
- All sensors connected (see checklist below)
- Perception models downloaded
- Running on bare metal (not Docker)

---

### Auto-Detection Mode
```bash
make launch
```

**Behavior:**
- Detects Docker environment → uses `launch-sim`
- Detects Jetson + `/etc/nv_tegra_release` → uses `launch-hw`

---

## Module Control Parameters

| Module | Parameter | Sim Mode | HW Mode | Required Hardware |
|--------|-----------|----------|---------|-------------------|
| RViz/GUI | `launch_rviz` | ✅ true | ✅ true | Display/X11 |
| Vehicle Interface | `launch_vehicle` | ❌ false | ✅ true | Jetson.GPIO, PCA9685 |
| Sensor Drivers | `launch_sensing_driver` | ❌ false | ✅ true | LiDAR, Camera, IMU |
| Perception | `launch_perception` | ❌ false | ✅ true | GPU, TensorRT, Models |
| GNSS (GPS) | `use_gnss` | ❌ false | ✅ true | GPS at /dev/ttyUSB0 |

---

# Hardware Checklist

When deploying on **real Jetson with full sensor suite**, verify:

## Network Devices
- [ ] **Seyond LiDAR**: Ping 172.168.1.10 successful
- [ ] **LiDAR HTTP API**: `curl http://172.168.1.10:8010/cgi/network`

## USB Devices
- [ ] **ZED Camera**: `/dev/video*` exists, `v4l2-ctl --list-devices` shows ZED
- [ ] **GPS**: `/dev/ttyUSB0` exists, `ls -l /dev/ttyUSB*`

## I2C Devices
```bash
# Check I2C bus (should show addresses)
sudo i2cdetect -y 1

# Expected devices:
# - MPU9250 IMU at 0x68
# - PCA9685 PWM at 0x40 or 0x70
```

- [ ] **MPU9250 IMU**: Shows at address 0x68
- [ ] **PCA9685 PWM**: Shows at address 0x40 or 0x70

## Perception Models
- [ ] **Centerpoint Model**: `data/lidar_centerpoint/centerpoint_tiny_ml_package.param.yaml` exists

## Display
- [ ] **X11 Server**: `echo $DISPLAY` shows `:0` or `:1`
- [ ] **X11 Auth**: `xhost +local:docker` executed on host
- [ ] **Test GUI**: `glxgears` or `xclock` works in container

---

# Quick Reference

## Host Side Commands (Outside Container)

### Initial Setup (One-Time)
```bash
# On x86 development machine
cd docker/
make bootstrap          # Install buildx, QEMU

# On Jetson (automated)
wget https://raw.githubusercontent.com/misuhsieh001/AutoSDV-containerization/2025.11-containerization/jetson_setup.sh
chmod +x jetson_setup.sh
./jetson_setup.sh
```

### Build Docker Image
```bash
cd docker/
make build              # Build ARM64 image (20-30 min)
make build-force        # Force rebuild without cache
```

### Run Container
```bash
cd docker/
make run                # Create/start/attach container
                       # Automatically runs xhost +local:docker
```

### Update Repository
```bash
cd ~/AutoSDV-containerization
git pull origin 2025.11-containerization
```

---

## Container Side Commands (Inside Container)

### First-Time Setup
```bash
make setup              # Install dependencies (first time only)
```

### Build Workspace
```bash
make build              # Build all 42 ROS packages (~15-20 min)
```

### Launch System
```bash
# Simulation mode (no hardware)
make launch-sim

# Hardware mode (all sensors)
make launch-hw

# Auto-detect mode
make launch
```

### Development
```bash
# Rebuild after code changes
colcon build --symlink-install --packages-select <package_name>

# Source workspace
source install/setup.bash

# List ROS nodes/topics
ros2 node list
ros2 topic list
```

---

## Summary of Modified Files

### Host Side
1. **`docker/Dockerfile`**:
   - ZED SDK 4.0 for JetPack 6.0
   - Seyond SDK ARM64 compilation
   - Split ROS package installation
   - Nested submodule initialization

2. **`docker/Makefile`**:
   - Docker buildx with `--platform linux/arm64`
   - Auto-detect repository URL and branch
   - Automatic `xhost +local:docker`
   - Prioritize DockerHub image detection

3. **`jetson_setup.sh`**:
   - Automated Jetson deployment
   - Docker + NVIDIA toolkit installation
   - Git clone with recursive submodules
   - Container launch

### Container Side
4. **`Makefile` (top-level)**:
   - ZED SDK CMake path
   - Launch mode targets (sim/hw/auto)
   - RViz enabled in simulation mode

5. **`cyclonedds.xml`**:
   - Disabled multicast
   - Loopback interface

6. **`src/launch/autosdv_launch/launch/autosdv.launch.yaml`**:
   - Added hardware control parameters
   - Config directory paths

---

## Error Severity Summary

| Severity | Count | Examples |
|----------|-------|----------|
| 🔴 **BLOCKING** | 1 | Missing perception model |
| 🟡 **SOFTWARE BUG** | 1 | NumPy 2.0 compatibility |
| ⚠️ **WARNING** | 4 | System monitors, cleanup errors |
| ✅ **EXPECTED** | 5 | Hardware not connected (normal) |
| ℹ️ **INFO** | 13+ | Topic state monitors (normal) |

---

## Current Status

✅ **Completed:**
- Cross-platform ARM64 build on x86 working
- All 42 packages building successfully
- Docker image on DockerHub: `misuhsieh001/autosdv:2025.11-latest` (19GB)
- GitHub repository: `misuhsieh001/AutoSDV-containerization:2025.11-containerization`
- Automated deployment with `jetson_setup.sh`
- Simulation mode tested and working
- RViz enabled with automatic X11 setup
- **DDS communication fixed with ROS_LOCALHOST_ONLY** ✅

⏳ **Pending:**
- Download perception models for hardware mode
- Fix NumPy 2.0 compatibility
- Test on real Jetson with full sensor suite

---

**Document Last Updated:** November 20, 2025  
**Status:** Production ready for simulation, hardware deployment requires sensors and perception models

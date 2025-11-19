root@ubuntu:/AutoSDV# make launch-sim
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🐳 Launching in SIMULATION mode (no hardware required)
   launch_rviz:=true (GUI enabled)
   launch_vehicle:=false (no GPIO hardware)
   launch_sensing_driver:=false (no sensors)
   launch_perception:=false (no GPU/TensorRT)
   use_gnss:=false (no GPS hardware)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[INFO] [launch]: All log files can be found below /root/.ros/log/2025-11-19-16-16-00-606160-ubuntu-7931
[INFO] [launch]: Default logging verbosity is set to INFO
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/system/system_monitor/cpu_monitor' in container '/system/system_monitor/system_monitor/system_monitor_container'
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/system/component_state_monitor/component' in container '/system/component_state_monitor/container'
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/sensing/lidar/passthrough_as_concatenate' in container 'pointcloud_container'
[INFO] [component_container_mt-1]: process started with pid [7966]
[INFO] [component_container_mt-2]: process started with pid [7968]
[INFO] [duplicated_node_checker_node-3]: process started with pid [7970]
[INFO] [processing_time_checker_node-4]: process started with pid [7972]
[INFO] [service_log_checker_node-5]: process started with pid [7974]
[INFO] [component_container-6]: process started with pid [7976]
[INFO] [topic_state_monitor_node-7]: process started with pid [7978]
[INFO] [topic_state_monitor_node-8]: process started with pid [7980]
[INFO] [topic_state_monitor_node-9]: process started with pid [7982]
[INFO] [topic_state_monitor_node-10]: process started with pid [7984]
[INFO] [topic_state_monitor_node-11]: process started with pid [7986]
[INFO] [topic_state_monitor_node-12]: process started with pid [8030]
[INFO] [topic_state_monitor_node-13]: process started with pid [8108]
[INFO] [topic_state_monitor_node-14]: process started with pid [8110]
[INFO] [topic_state_monitor_node-15]: process started with pid [8120]
[INFO] [topic_state_monitor_node-16]: process started with pid [8124]
[INFO] [topic_state_monitor_node-17]: process started with pid [8142]
[INFO] [topic_state_monitor_node-18]: process started with pid [8160]
[INFO] [topic_state_monitor_node-19]: process started with pid [8166]
[INFO] [topic_state_monitor_node-20]: process started with pid [8178]
[INFO] [topic_state_monitor_node-21]: process started with pid [8185]
[INFO] [component_container-22]: process started with pid [8188]
[INFO] [component_container-23]: process started with pid [8190]
[INFO] [aggregator_node-24]: process started with pid [8192]
[INFO] [component_state_diagnostics-25]: process started with pid [8196]
[INFO] [converter-26]: process started with pid [8198]
[INFO] [mrm_handler_node-27]: process started with pid [8207]
[INFO] [component_container_mt-28]: process started with pid [8221]
[INFO] [map_hash_generator-29]: process started with pid [8223]
[INFO] [autoware_map_projection_loader_node-30]: process started with pid [8226]
[INFO] [imu_corrector_node-31]: process started with pid [8240]
[INFO] [gyro_bias_estimator_node-32]: process started with pid [8248]
[INFO] [autoware_vehicle_velocity_converter_node-33]: process started with pid [8264]
[INFO] [autoware_ndt_scan_matcher_node-34]: process started with pid [8305]
[INFO] [autoware_gyro_odometer_node-35]: process started with pid [8315]
[INFO] [autoware_pose_initializer_node-36]: process started with pid [8328]
[INFO] [automatic_pose_initializer_node-37]: process started with pid [8331]
[INFO] [autoware_ekf_localizer_node-38]: process started with pid [8373]
[INFO] [autoware_stop_filter_node-39]: process started with pid [8406]
[INFO] [autoware_twist2accel_node-40]: process started with pid [8427]
[INFO] [autoware_pose_instability_detector_node-41]: process started with pid [8432]
[INFO] [autoware_localization_error_monitor_node-42]: process started with pid [8436]
[INFO] [component_container_mt-43]: process started with pid [8456]
[INFO] [component_container_mt-44]: process started with pid [8466]
[INFO] [control_evaluator-45]: process started with pid [8476]
[INFO] [component_container_mt-46]: process started with pid [8479]
[INFO] [web_server.py-47]: process started with pid [8504]
[INFO] [initial_pose_adaptor_node-48]: process started with pid [8507]
[INFO] [routing_adaptor_node-49]: process started with pid [8515]
[INFO] [component_container_mt-50]: process started with pid [8545]
[INFO] [rviz2-51]: process started with pid [8548]
[INFO] [rqt_runtime_monitor-52]: process started with pid [8558]
[INFO] [static_transform_publisher-53]: process started with pid [8592]
[autoware_map_projection_loader_node-30] Load ./data/COSS-map-planning/map_projector_info.yaml
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/system/mrm_emergency_stop_operator' in container '/system/mrm_emergency_stop_operator/mrm_emergency_stop_operator_container'
[component_container_mt-1] [INFO] [1763568981.180488884] [pointcloud_container]: Load Library: /opt/ros/humble/lib/libpointcloud_preprocessor_filter.so
[component_container_mt-1] [INFO] [1763568981.635114526] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::ApproximateDownsampleFilterComponent>
[component_container_mt-1] [INFO] [1763568981.635196669] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::BlockageDiagComponent>
[component_container_mt-1] [INFO] [1763568981.635207069] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::CropBoxFilterComponent>
[component_container_mt-1] [INFO] [1763568981.635213373] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::DistortionCorrectorComponent>
[component_container_mt-1] [INFO] [1763568981.635219293] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::DualReturnOutlierFilterComponent>
[component_container_mt-1] [INFO] [1763568981.635225405] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::Lanelet2MapFilterComponent>
[component_container_mt-1] [INFO] [1763568981.635239421] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::PassThroughFilterComponent>
[component_container_mt-1] [INFO] [1763568981.635246077] [pointcloud_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::PassThroughFilterComponent>
[component_container_mt-1] [INFO] [1763568982.216085024] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::ApproximateDownsampleFilterComponent>
[component_container_mt-1] [INFO] [1763568982.216152415] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::BlockageDiagComponent>
[component_container_mt-1] [INFO] [1763568982.216163071] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::CropBoxFilterComponent>
[component_container_mt-1] [INFO] [1763568982.216170975] [pointcloud_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::CropBoxFilterComponent>
[component_container_mt-2] [INFO] [1763568981.314764679] [system.system_monitor.system_monitor.system_monitor_container]: Load Library: /opt/ros/humble/lib/libcpu_monitor_lib.so
[component_container_mt-2] [INFO] [1763568981.316346176] [system.system_monitor.system_monitor.system_monitor_container]: Found class: rclcpp_components::NodeFactoryTemplate<CPUMonitor>
[component_container_mt-2] [INFO] [1763568981.316403071] [system.system_monitor.system_monitor.system_monitor_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<CPUMonitor>
[component_container-6] [INFO] [1763568981.379597691] [system.component_state_monitor.container]: Load Library: /opt/ros/humble/lib/libcomponent_state_monitor.so
[component_container-6] [INFO] [1763568981.382753164] [system.component_state_monitor.container]: Found class: rclcpp_components::NodeFactoryTemplate<component_state_monitor::StateMonitor>
[component_container-6] [INFO] [1763568981.382826636] [system.component_state_monitor.container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<component_state_monitor::StateMonitor>
[topic_state_monitor_node-7] [INFO] [1763568981.303404827] [system.topic_state_monitor_vector_map]: /map/vector_map has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-8] [INFO] [1763568981.282841370] [system.topic_state_monitor_pointcloud_map]: /map/pointcloud_map has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-9] [INFO] [1763568981.303511867] [system.topic_state_monitor_initialpose3d]: /initialpose3d has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-10] [INFO] [1763568981.324546810] [system.topic_state_monitor_pose_twist_fusion_filter_pose]: /localization/pose_twist_fusion_filter/pose has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-11] [INFO] [1763568981.283113241] [system.topic_state_monitor_obstacle_segmentation_pointcloud]: /perception/obstacle_segmentation/pointcloud has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-12] [INFO] [1763568981.321312105] [system.topic_state_monitor_object_recognition_objects]: /perception/object_recognition/objects has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-13] [INFO] [1763568981.520705679] [system.topic_state_monitor_traffic_light_recognition_traffic_signals]: /perception/traffic_light_recognition/traffic_signals has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-14] [INFO] [1763568981.328279080] [system.topic_state_monitor_mission_planning_route]: /planning/mission_planning/route has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-15] [INFO] [1763568981.407816825] [system.topic_state_monitor_scenario_planning_trajectory]: /planning/scenario_planning/trajectory has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-16] [INFO] [1763568981.346476660] [system.topic_state_monitor_trajectory_follower_control_cmd]: /control/trajectory_follower/control_cmd has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-17] [INFO] [1763568981.508288328] [system.topic_state_monitor_control_command_control_cmd]: /control/command/control_cmd has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-18] [INFO] [1763568981.372197309] [system.topic_state_monitor_vehicle_status_velocity_status]: /vehicle/status/velocity_status has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-19] [INFO] [1763568981.659065967] [system.topic_state_monitor_vehicle_status_steering_status]: /vehicle/status/steering_status has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-20] [INFO] [1763568982.088095727] [system.topic_state_monitor_system_emergency_control_cmd]: /system/emergency/control_cmd has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-21] [INFO] [1763568981.887432399] [system.topic_state_monitor_transform_map_to_base_link]: /tf has not received. Set ERROR in diagnostics.
[component_container-23] [INFO] [1763568982.365385165] [system.mrm_emergency_stop_operator.mrm_emergency_stop_operator_container]: Load Library: /opt/ros/humble/lib/libmrm_emergency_stop_operator_component.so
[component_container-23] [INFO] [1763568982.366786439] [system.mrm_emergency_stop_operator.mrm_emergency_stop_operator_container]: Found class: rclcpp_components::NodeFactoryTemplate<mrm_emergency_stop_operator::MrmEmergencyStopOperator>
[component_container-23] [INFO] [1763568982.366853767] [system.mrm_emergency_stop_operator.mrm_emergency_stop_operator_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<mrm_emergency_stop_operator::MrmEmergencyStopOperator>
[mrm_handler_node-27] [INFO] [1763568981.878999638] [system.mrm_handler]: waiting for operation_mode_availability msg...
[rviz2-51] QStandardPaths: XDG_RUNTIME_DIR not set, defaulting to '/tmp/runtime-root'
[component_container_mt-28] [INFO] [1763568982.615639208] [map.map_container]: Load Library: /opt/ros/humble/lib/libpointcloud_map_loader_node.so
[static_transform_publisher-53] [WARN] [1763568982.716046616] []: Old-style arguments are deprecated; see --help for new-style arguments
[autoware_ekf_localizer_node-38] [WARN] [1763568982.786148820] [localization.pose_twist_fusion_filter.ekf_localizer]: The node is not activated. Provide initial pose to pose_initializer
[component_container_mt-2] [INFO] [1763568982.875853173] [system.system_monitor.system_monitor.system_monitor_container]: Load Library: /opt/ros/humble/lib/libmem_monitor_lib.so
[component_container_mt-2] [INFO] [1763568982.876525266] [system.system_monitor.system_monitor.system_monitor_container]: Found class: rclcpp_components::NodeFactoryTemplate<MemMonitor>
[component_container_mt-2] [INFO] [1763568982.876576946] [system.system_monitor.system_monitor.system_monitor_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<MemMonitor>
[static_transform_publisher-53] [INFO] [1763568983.427178176] [map_to_base_link_static_tf]: Spinning until stopped - publishing transform
[static_transform_publisher-53] translation: ('0.000000', '0.000000', '0.000000')
[static_transform_publisher-53] rotation: ('0.000000', '0.000000', '0.000000', '1.000000')
[static_transform_publisher-53] from 'map' to 'base_link'
[component_container_mt-43] [INFO] [1763568983.521956906] [control.control_container]: Load Library: /opt/ros/humble/lib/libautoware_glog_component.so
[component_container_mt-43] [INFO] [1763568983.523250436] [control.control_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::glog_component::GlogComponent>
[component_container_mt-43] [INFO] [1763568983.523304036] [control.control_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<autoware::glog_component::GlogComponent>
[mrm_handler_node-27] [INFO] [1763568983.578952099] [system.mrm_handler]: waiting for mrm emergency stop to become available...
[component_container_mt-1] [INFO] [1763568983.608080412] [localization.util.crop_box_filter_measurement_range]: Input and output frames are the same. Overriding has_static_tf_only to true.
[component_container_mt-28] [INFO] [1763568983.648201282] [map.map_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::map_loader::PointCloudMapLoaderNode>
[component_container_mt-28] [INFO] [1763568983.649286589] [map.map_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<autoware::map_loader::PointCloudMapLoaderNode>
[component_container_mt-43] [WARN] [1763568983.764187210] [control.control_container.rclcpp]: failed to send response to /control/control_container/_container/load_node (timeout): client will not receive response, at ./src/rmw_response.cpp:154, at ./src/rcl/service.c:314
[component_container_mt-43] [INFO] [1763568983.764868999] [control.control_container]: Load Library: /opt/ros/humble/lib/libautoware_external_cmd_selector_node.so
[component_container_mt-43] [INFO] [1763568983.768278647] [control.control_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::external_cmd_selector::ExternalCmdSelector>
[component_container_mt-43] [INFO] [1763568983.768371223] [control.control_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<autoware::external_cmd_selector::ExternalCmdSelector>
[component_container_mt-1] [INFO] [1763568983.796281654] [pointcloud_container]: Load Library: /opt/ros/humble/lib/libautoware_glog_component.so
[component_container_mt-1] [INFO] [1763568983.797799375] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::glog_component::GlogComponent>
[component_container_mt-1] [INFO] [1763568983.797866319] [pointcloud_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<autoware::glog_component::GlogComponent>
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/localization/util/crop_box_filter_measurement_range' in container '/pointcloud_container'
[topic_state_monitor_node-8] [INFO] [1763568984.382788542] [system.topic_state_monitor_pointcloud_map]: /map/pointcloud_map has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-11] [INFO] [1763568984.383078589] [system.topic_state_monitor_obstacle_segmentation_pointcloud]: /perception/obstacle_segmentation/pointcloud has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-9] [INFO] [1763568984.403562014] [system.topic_state_monitor_initialpose3d]: /initialpose3d has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-7] [INFO] [1763568984.403574302] [system.topic_state_monitor_vector_map]: /map/vector_map has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-12] [INFO] [1763568984.421266924] [system.topic_state_monitor_object_recognition_objects]: /perception/object_recognition/objects has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-10] [INFO] [1763568984.424481629] [system.topic_state_monitor_pose_twist_fusion_filter_pose]: /localization/pose_twist_fusion_filter/pose has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-14] [INFO] [1763568984.428225004] [system.topic_state_monitor_mission_planning_route]: /planning/mission_planning/route has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-16] [INFO] [1763568984.437247042] [system.topic_state_monitor_trajectory_follower_control_cmd]: /control/trajectory_follower/control_cmd has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-18] [INFO] [1763568984.472145025] [system.topic_state_monitor_vehicle_status_velocity_status]: /vehicle/status/velocity_status has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-15] [INFO] [1763568984.507803484] [system.topic_state_monitor_scenario_planning_trajectory]: /planning/scenario_planning/trajectory has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-17] [INFO] [1763568984.508349850] [system.topic_state_monitor_control_command_control_cmd]: /control/command/control_cmd has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-13] [INFO] [1763568984.520829152] [system.topic_state_monitor_traffic_light_recognition_traffic_signals]: /perception/traffic_light_recognition/traffic_signals has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-19] [INFO] [1763568984.758862835] [system.topic_state_monitor_vehicle_status_steering_status]: /vehicle/status/steering_status has not received. Set ERROR in diagnostics.
[autoware_ekf_localizer_node-38] [WARN] [1763568984.800587347] [localization.pose_twist_fusion_filter.ekf_localizer]: The node is not activated. Provide initial pose to pose_initializer
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/control/external_cmd_selector' in container '/control/control_container'
[component_container_mt-43] [INFO] [1763568984.940717131] [control.control_container]: Load Library: /opt/ros/humble/lib/libautoware_external_cmd_converter.so
[topic_state_monitor_node-21] [INFO] [1763568984.942074500] [system.topic_state_monitor_transform_map_to_base_link]: /tf has not received. Set ERROR in diagnostics.
[component_container_mt-43] [INFO] [1763568984.949453058] [control.control_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::external_cmd_converter::ExternalCmdConverterNode>
[component_container_mt-43] [INFO] [1763568984.949553570] [control.control_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<autoware::external_cmd_converter::ExternalCmdConverterNode>
[component_container_mt-44] [INFO] [1763568985.036475280] [control.control_check_container]: Load Library: /opt/ros/humble/lib/libautoware_glog_component.so
[component_container_mt-44] [INFO] [1763568985.040038112] [control.control_check_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::glog_component::GlogComponent>
[component_container_mt-44] [INFO] [1763568985.040133951] [control.control_check_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<autoware::glog_component::GlogComponent>
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/map/pointcloud_map_loader' in container '/map/map_container'
[component_container-22] [INFO] [1763568985.168018896] [system.mrm_comfortable_stop_operator.mrm_comfortable_stop_operator_container]: Load Library: /opt/ros/humble/lib/libmrm_comfortable_stop_operator_component.so
[component_container-22] [INFO] [1763568985.169013899] [system.mrm_comfortable_stop_operator.mrm_comfortable_stop_operator_container]: Found class: rclcpp_components::NodeFactoryTemplate<mrm_comfortable_stop_operator::MrmComfortableStopOperator>
[component_container-22] [INFO] [1763568985.169071819] [system.mrm_comfortable_stop_operator.mrm_comfortable_stop_operator_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<mrm_comfortable_stop_operator::MrmComfortableStopOperator>
[component_container_mt-28] [INFO] [1763568985.178344768] [map.map_container]: Load Library: /opt/ros/humble/lib/liblanelet2_map_loader_node.so
[component_container_mt-28] [INFO] [1763568985.186625082] [map.map_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::map_loader::Lanelet2MapLoaderNode>
[component_container_mt-28] [INFO] [1763568985.188760112] [map.map_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<autoware::map_loader::Lanelet2MapLoaderNode>
[component_container_mt-44] [INFO] [1763568985.447357188] [control.control_check_container]: Load Library: /opt/ros/humble/lib/libautoware_collision_detector.so
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/control/glog_control_check_container_component' in container '/control/control_check_container'
[component_container_mt-44] [INFO] [1763568985.453639623] [control.control_check_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::collision_detector::CollisionDetectorNode>
[component_container_mt-44] [INFO] [1763568985.455393375] [control.control_check_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<autoware::collision_detector::CollisionDetectorNode>
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/system/system_monitor/mem_monitor' in container '/system/system_monitor/system_monitor/system_monitor_container'
[component_container_mt-2] [INFO] [1763568985.637971155] [system.system_monitor.system_monitor.system_monitor_container]: Load Library: /opt/ros/humble/lib/libnet_monitor_lib.so
[component_container_mt-2] [INFO] [1763568985.639593260] [system.system_monitor.system_monitor.system_monitor_container]: Found class: rclcpp_components::NodeFactoryTemplate<NetMonitor>
[component_container_mt-2] [INFO] [1763568985.639669323] [system.system_monitor.system_monitor.system_monitor_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<NetMonitor>
[web_server.py-47]  * Running on http://localhost:8888/ (Press CTRL+C to quit)
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/pointcloud_container/glog_component' in container '/pointcloud_container'
[component_container_mt-1] [INFO] [1763568986.228541865] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::ApproximateDownsampleFilterComponent>
[component_container_mt-1] [INFO] [1763568986.228637864] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::BlockageDiagComponent>
[component_container_mt-1] [INFO] [1763568986.228653000] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::CropBoxFilterComponent>
[component_container_mt-1] [INFO] [1763568986.228660488] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::DistortionCorrectorComponent>
[component_container_mt-1] [INFO] [1763568986.228667208] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::DualReturnOutlierFilterComponent>
[component_container_mt-1] [INFO] [1763568986.228673000] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::Lanelet2MapFilterComponent>
[component_container_mt-1] [INFO] [1763568986.228678824] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::PassThroughFilterComponent>
[component_container_mt-1] [INFO] [1763568986.228684392] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::PassThroughFilterUInt16Component>
[component_container_mt-1] [INFO] [1763568986.228779944] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::PickupBasedVoxelGridDownsampleFilterComponent>
[component_container_mt-1] [INFO] [1763568986.228791847] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::PointCloudConcatenateDataSynchronizerComponent>
[component_container_mt-1] [INFO] [1763568986.228799399] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::PointCloudConcatenationComponent>
[component_container_mt-1] [INFO] [1763568986.228806151] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::PointCloudDataSynchronizerComponent>
[component_container_mt-1] [INFO] [1763568986.228812615] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::PointcloudAccumulatorComponent>
[component_container_mt-1] [INFO] [1763568986.228818183] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::PolygonRemoverComponent>
[component_container_mt-1] [INFO] [1763568986.228823655] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::RadiusSearch2DOutlierFilterComponent>
[component_container_mt-1] [INFO] [1763568986.228829287] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::RandomDownsampleFilterComponent>
[component_container_mt-1] [INFO] [1763568986.228835079] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::RingOutlierFilterComponent>
[component_container_mt-1] [INFO] [1763568986.228840775] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::VectorMapInsideAreaFilterComponent>
[component_container_mt-1] [INFO] [1763568986.228847175] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::VoxelGridDownsampleFilterComponent>
[component_container_mt-1] [INFO] [1763568986.228853159] [pointcloud_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::VoxelGridDownsampleFilterComponent>
[rqt_runtime_monitor-52] QStandardPaths: XDG_RUNTIME_DIR not set, defaulting to '/tmp/runtime-root'
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/map/lanelet2_map_loader' in container '/map/map_container'
[component_container_mt-28] [INFO] [1763568986.370892662] [map.map_container]: Load Library: /opt/ros/humble/lib/liblanelet2_map_visualization_node.so
[component_container_mt-28] [INFO] [1763568986.372203824] [map.map_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::lanelet2_map_visualizer::Lanelet2MapVisualizationNode>
[component_container_mt-28] [INFO] [1763568986.372261072] [map.map_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<autoware::lanelet2_map_visualizer::Lanelet2MapVisualizationNode>
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/system/mrm_comfortable_stop_operator' in container '/system/mrm_comfortable_stop_operator/mrm_comfortable_stop_operator_container'
[component_container_mt-44] [INFO] [1763568986.579507346] [control.control_check_container]: Load Library: /opt/ros/humble/lib/libautoware_autonomous_emergency_braking_node.so
[component_container_mt-28] [WARN] [1763568986.592990612] [map.lanelet2_map_loader]: ./data/COSS-map-planning/lanelet2_map.osm has no format_version(null) or non semver-style format_version(null) information
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/control/collision_detector' in container '/control/control_check_container'
[component_container_mt-28] [INFO] [1763568986.604423647] [map.lanelet2_map_loader]: Loaded map format_version: null
[component_container_mt-44] [INFO] [1763568986.678701415] [control.collision_detector]: waiting for current odometry...
[autoware_ekf_localizer_node-38] [WARN] [1763568986.800624212] [localization.pose_twist_fusion_filter.ekf_localizer]: The node is not activated. Provide initial pose to pose_initializer
[component_container_mt-44] [INFO] [1763568986.908705344] [control.control_check_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::motion::control::autonomous_emergency_braking::AEB>
[component_container_mt-44] [INFO] [1763568986.909253949] [control.control_check_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<autoware::motion::control::autonomous_emergency_braking::AEB>
[component_container_mt-28] [INFO] [1763568986.999618364] [map.lanelet2_map_loader]: Succeeded to load lanelet2_map. Map is published.
[component_container_mt-2] [ERROR] [1763568987.053422019] [system.system_monitor.net_monitor]: Failed to connect socket. No such file or directory
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/system/system_monitor/net_monitor' in container '/system/system_monitor/system_monitor/system_monitor_container'
[component_container_mt-2] [INFO] [1763568987.068631613] [system.system_monitor.system_monitor.system_monitor_container]: Load Library: /opt/ros/humble/lib/libntp_monitor_lib.so
[component_container_mt-2] [INFO] [1763568987.069546552] [system.system_monitor.system_monitor.system_monitor_container]: Found class: rclcpp_components::NodeFactoryTemplate<NTPMonitor>
[component_container_mt-2] [INFO] [1763568987.069607928] [system.system_monitor.system_monitor.system_monitor_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<NTPMonitor>
[component_container_mt-1] [INFO] [1763568987.263265273] [localization.util.voxel_grid_downsample_filter]: Input and output frames are the same. Overriding has_static_tf_only to true.
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/map/lanelet2_map_visualization' in container '/map/map_container'
[component_container_mt-28] [INFO] [1763568987.313568432] [map.lanelet2_map_visualization]: Map is loaded
[component_container_mt-28]
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/localization/util/voxel_grid_downsample_filter' in container '/pointcloud_container'
[component_container_mt-1] [INFO] [1763568987.323669377] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::ApproximateDownsampleFilterComponent>
[component_container_mt-1] [INFO] [1763568987.323769249] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::BlockageDiagComponent>
[component_container_mt-1] [INFO] [1763568987.323784353] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::CropBoxFilterComponent>
[component_container_mt-1] [INFO] [1763568987.323791361] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::DistortionCorrectorComponent>
[component_container_mt-1] [INFO] [1763568987.323797825] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::DualReturnOutlierFilterComponent>
[component_container_mt-1] [INFO] [1763568987.323803617] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::Lanelet2MapFilterComponent>
[component_container_mt-1] [INFO] [1763568987.323810209] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::PassThroughFilterComponent>
[component_container_mt-1] [INFO] [1763568987.323815841] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::PassThroughFilterUInt16Component>
[component_container_mt-1] [INFO] [1763568987.323821633] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::PickupBasedVoxelGridDownsampleFilterComponent>
[component_container_mt-1] [INFO] [1763568987.323828321] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::PointCloudConcatenateDataSynchronizerComponent>
[component_container_mt-1] [INFO] [1763568987.323834305] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::PointCloudConcatenationComponent>
[component_container_mt-1] [INFO] [1763568987.323905376] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::PointCloudDataSynchronizerComponent>
[component_container_mt-1] [INFO] [1763568987.323916160] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::PointcloudAccumulatorComponent>
[component_container_mt-1] [INFO] [1763568987.323922176] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::PolygonRemoverComponent>
[component_container_mt-1] [INFO] [1763568987.323928448] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::RadiusSearch2DOutlierFilterComponent>
[component_container_mt-1] [INFO] [1763568987.323934112] [pointcloud_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::RandomDownsampleFilterComponent>
[component_container_mt-1] [INFO] [1763568987.323940256] [pointcloud_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<autoware::pointcloud_preprocessor::RandomDownsampleFilterComponent>
[component_container_mt-28] [INFO] [1763568987.325350234] [map.map_container]: Load Library: /opt/ros/humble/lib/libvector_map_tf_generator_node.so
[component_container_mt-28] [INFO] [1763568987.332235642] [map.map_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::map_tf_generator::VectorMapTFGeneratorNode>
[component_container_mt-28] [INFO] [1763568987.332321401] [map.map_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<autoware::map_tf_generator::VectorMapTFGeneratorNode>
[topic_state_monitor_node-11] [INFO] [1763568987.383122543] [system.topic_state_monitor_obstacle_segmentation_pointcloud]: /perception/obstacle_segmentation/pointcloud has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-12] [INFO] [1763568987.421285054] [system.topic_state_monitor_object_recognition_objects]: /perception/object_recognition/objects has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-14] [INFO] [1763568987.428225214] [system.topic_state_monitor_mission_planning_route]: /planning/mission_planning/route has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-16] [INFO] [1763568987.437257780] [system.topic_state_monitor_trajectory_follower_control_cmd]: /control/trajectory_follower/control_cmd has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-18] [INFO] [1763568987.487167150] [system.topic_state_monitor_vehicle_status_velocity_status]: /vehicle/status/velocity_status has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-9] [INFO] [1763568987.503510402] [system.topic_state_monitor_initialpose3d]: /initialpose3d has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-15] [INFO] [1763568987.507875278] [system.topic_state_monitor_scenario_planning_trajectory]: /planning/scenario_planning/trajectory has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-17] [INFO] [1763568987.510504866] [system.topic_state_monitor_control_command_control_cmd]: /control/command/control_cmd has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-10] [INFO] [1763568987.524423009] [system.topic_state_monitor_pose_twist_fusion_filter_pose]: /localization/pose_twist_fusion_filter/pose has not received. Set ERROR in diagnostics.
[web_server.py-47] [INFO] [1763568987.535040656] [adapi.web_server]: service not available, waiting again... (/api/interface/version
[topic_state_monitor_node-13] [INFO] [1763568987.620597413] [system.topic_state_monitor_traffic_light_recognition_traffic_signals]: /perception/traffic_light_recognition/traffic_signals has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-19] [INFO] [1763568987.758869157] [system.topic_state_monitor_vehicle_status_steering_status]: /vehicle/status/steering_status has not received. Set ERROR in diagnostics.
[rviz2-51] [INFO] [1763568987.816206748] [rviz2]: Stereo is NOT SUPPORTED
[rviz2-51] [INFO] [1763568987.816553947] [rviz2]: OpenGl version: 4.6 (GLSL 4.6)
[rviz2-51] [INFO] [1763568988.028680422] [rviz2]: Stereo is NOT SUPPORTED
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/control/external_cmd_converter' in container '/control/control_container'
[component_container_mt-43] [INFO] [1763568988.030984699] [control.control_container]: Load Library: /opt/ros/humble/lib/libcontroller_node.so
[topic_state_monitor_node-21] [INFO] [1763568988.042058312] [system.topic_state_monitor_transform_map_to_base_link]: /tf has not received. Set ERROR in diagnostics.
[component_container_mt-43] [INFO] [1763568988.044778427] [control.control_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::motion::control::trajectory_follower_node::Controller>
[component_container_mt-43] [INFO] [1763568988.045951446] [control.control_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<autoware::motion::control::trajectory_follower_node::Controller>
[component_container_mt-2] [ERROR] [1763568988.048762249] [system.system_monitor.net_monitor]: Failed to connect socket. No such file or directory
[control_evaluator-45] [WARN] [1763568988.103634411] [route_handler]: setMap() for invalid version map:
[component_container_mt-1] [INFO] [1763568988.371560149] [localization.util.random_downsample_filter]: Input and output frames are the same. Overriding has_static_tf_only to true.
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/localization/util/random_downsample_filter' in container '/pointcloud_container'
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/system/system_monitor/ntp_monitor' in container '/system/system_monitor/system_monitor/system_monitor_container'
[component_container_mt-2] [INFO] [1763568988.494474108] [system.system_monitor.system_monitor.system_monitor_container]: Load Library: /opt/ros/humble/lib/libprocess_monitor_lib.so
[component_container_mt-2] [INFO] [1763568988.495914902] [system.system_monitor.system_monitor.system_monitor_container]: Found class: rclcpp_components::NodeFactoryTemplate<ProcessMonitor>
[component_container_mt-2] [INFO] [1763568988.495989781] [system.system_monitor.system_monitor.system_monitor_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<ProcessMonitor>
[web_server.py-47] [INFO] [1763568988.538157970] [adapi.web_server]: service not available, waiting again... (/api/interface/version
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/map/vector_map_tf_generator' in container '/map/map_container'
[component_container_mt-28] [INFO] [1763568988.664453098] [map.vector_map_tf_generator]: broadcast static tf. map_frame:map, viewer_frame:viewer, x:4.14566, y:18.7981, z:8.97937
[autoware_ekf_localizer_node-38] [WARN] [1763568988.820602745] [localization.pose_twist_fusion_filter.ekf_localizer]: The node is not activated. Provide initial pose to pose_initializer
[component_container_mt-2] [ERROR] [1763568989.048565467] [system.system_monitor.net_monitor]: Failed to connect socket. No such file or directory
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/system/system_monitor/process_monitor' in container '/system/system_monitor/system_monitor/system_monitor_container'
[component_container_mt-2] [INFO] [1763568989.160326870] [system.system_monitor.system_monitor.system_monitor_container]: Load Library: /opt/ros/humble/lib/libhdd_monitor_lib.so
[component_container_mt-2] [INFO] [1763568989.161362673] [system.system_monitor.system_monitor.system_monitor_container]: Found class: rclcpp_components::NodeFactoryTemplate<HddMonitor>
[component_container_mt-2] [INFO] [1763568989.161424625] [system.system_monitor.system_monitor.system_monitor_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<HddMonitor>
[component_container_mt-44] [INFO] [1763568989.273496011] [control.control_check_container]: Load Library: /opt/ros/humble/lib/libautoware_lane_departure_checker.so
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/control/autonomous_emergency_braking' in container '/control/control_check_container'
[component_container_mt-44] [INFO] [1763568989.286174000] [control.control_check_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::lane_departure_checker::LaneDepartureCheckerNode>
[component_container_mt-44] [INFO] [1763568989.286267280] [control.control_check_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<autoware::lane_departure_checker::LaneDepartureCheckerNode>
[component_container_mt-1] [WARN] [1763568989.427326147] [sensing.lidar.passthrough_as_concatenate]: New subscription discovered on topic '/sensing/lidar/concatenated/pointcloud', requesting incompatible QoS. No messages will be sent to it. Last incompatible policy: RELIABILITY_QOS_POLICY
[web_server.py-47] [INFO] [1763568989.541386164] [adapi.web_server]: service not available, waiting again... (/api/interface/version
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/adapi/node/autoware_state' in container '/adapi/container'
[component_container_mt-2] [ERROR] [1763568989.787712321] [system.system_monitor.hdd_monitor]: socket connect error. Connection refused
[component_container_mt-2] [ERROR] [1763568989.787862081] [system.system_monitor.hdd_monitor]: Failed to unmount device : overlay
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/system/system_monitor/hdd_monitor' in container '/system/system_monitor/system_monitor/system_monitor_container'
[component_container_mt-2] [INFO] [1763568989.812610254] [system.system_monitor.system_monitor.system_monitor_container]: Load Library: /opt/ros/humble/lib/libgpu_monitor_lib.so
[component_container_mt-2] [INFO] [1763568989.813237195] [system.system_monitor.system_monitor.system_monitor_container]: Found class: rclcpp_components::NodeFactoryTemplate<GPUMonitor>
[component_container_mt-2] [INFO] [1763568989.813283403] [system.system_monitor.system_monitor.system_monitor_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<GPUMonitor>
[component_container_mt-2] [ERROR] [1763568990.048724490] [system.system_monitor.net_monitor]: Failed to connect socket. No such file or directory
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/autoware_api/external/rtc_controller/node' in container '/autoware_api/external/rtc_controller/container'
[topic_state_monitor_node-14] [INFO] [1763568990.432388989] [system.topic_state_monitor_mission_planning_route]: /planning/mission_planning/route has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-16] [INFO] [1763568990.437294246] [system.topic_state_monitor_trajectory_follower_control_cmd]: /control/trajectory_follower/control_cmd has not received. Set ERROR in diagnostics.
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/control/trajectory_follower/controller_node_exe' in container '/control/control_container'
[topic_state_monitor_node-11] [INFO] [1763568990.483086066] [system.topic_state_monitor_obstacle_segmentation_pointcloud]: /perception/obstacle_segmentation/pointcloud has not received. Set ERROR in diagnostics.
[component_container_mt-43] [INFO] [1763568990.489847731] [control.trajectory_follower.controller_node_exe]: Waiting for acceleration data
[component_container_mt-43] [INFO] [1763568990.489961970] [control.trajectory_follower.controller_node_exe]: Control is skipped since input data is not ready.
[topic_state_monitor_node-9] [INFO] [1763568990.503578228] [system.topic_state_monitor_initialpose3d]: /initialpose3d has not received. Set ERROR in diagnostics.
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/adapi/node/diagnostics' in container '/adapi/container'
[topic_state_monitor_node-12] [INFO] [1763568990.521264322] [system.topic_state_monitor_object_recognition_objects]: /perception/object_recognition/objects has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-10] [INFO] [1763568990.524706514] [system.topic_state_monitor_pose_twist_fusion_filter_pose]: /localization/pose_twist_fusion_filter/pose has not received. Set ERROR in diagnostics.
[web_server.py-47] [INFO] [1763568990.549604479] [adapi.web_server]: service not available, waiting again... (/api/interface/version
[topic_state_monitor_node-18] [INFO] [1763568990.572085079] [system.topic_state_monitor_vehicle_status_velocity_status]: /vehicle/status/velocity_status has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-15] [INFO] [1763568990.607811186] [system.topic_state_monitor_scenario_planning_trajectory]: /planning/scenario_planning/trajectory has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-17] [INFO] [1763568990.608287919] [system.topic_state_monitor_control_command_control_cmd]: /control/command/control_cmd has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-13] [INFO] [1763568990.720600200] [system.topic_state_monitor_traffic_light_recognition_traffic_signals]: /perception/traffic_light_recognition/traffic_signals has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-19] [INFO] [1763568990.758876215] [system.topic_state_monitor_vehicle_status_steering_status]: /vehicle/status/steering_status has not received. Set ERROR in diagnostics.
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/system/system_monitor/gpu_monitor' in container '/system/system_monitor/system_monitor/system_monitor_container'
[component_container_mt-2] [INFO] [1763568990.793627127] [system.system_monitor.system_monitor.system_monitor_container]: Load Library: /opt/ros/humble/lib/libvoltage_monitor_lib.so
[component_container_mt-2] [INFO] [1763568990.794674834] [system.system_monitor.system_monitor.system_monitor_container]: Found class: rclcpp_components::NodeFactoryTemplate<VoltageMonitor>
[component_container_mt-2] [INFO] [1763568990.794743217] [system.system_monitor.system_monitor.system_monitor_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<VoltageMonitor>
[autoware_ekf_localizer_node-38] [WARN] [1763568990.820604154] [localization.pose_twist_fusion_filter.ekf_localizer]: The node is not activated. Provide initial pose to pose_initializer
[topic_state_monitor_node-21] [INFO] [1763568991.042444312] [system.topic_state_monitor_transform_map_to_base_link]: /tf has not received. Set ERROR in diagnostics.
[component_container_mt-2] [ERROR] [1763568991.048618428] [system.system_monitor.net_monitor]: Failed to connect socket. No such file or directory
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/control/trajectory_follower/lane_departure_checker_node' in container '/control/control_check_container'
[component_container_mt-44] [INFO] [1763568991.063151928] [control.control_check_container]: Load Library: /opt/ros/humble/lib/libautoware_control_validator_component.so
[component_container_mt-44] [INFO] [1763568991.065193647] [control.control_check_container]: Found class: rclcpp_components::NodeFactoryTemplate<autoware::control_validator::ControlValidator>
[component_container_mt-44] [INFO] [1763568991.065266063] [control.control_check_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<autoware::control_validator::ControlValidator>
[component_container_mt-2] [ERROR] [1763568991.088897249] [system.system_monitor.hdd_monitor]: socket connect error. Connection refused
[component_container_mt-2] [ERROR] [1763568991.089043233] [system.system_monitor.hdd_monitor]: Failed to unmount device : overlay
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/system/system_monitor/voltage_monitor' in container '/system/system_monitor/system_monitor/system_monitor_container'
[component_container_mt-44] [INFO] [1763568991.389679187] [control.trajectory_follower.lane_departure_checker_node]: waiting for current_twist msg...
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/adapi/node/fail_safe' in container '/adapi/container'
[web_server.py-47] [INFO] [1763568991.554815735] [adapi.web_server]: service not available, waiting again... (/api/interface/version
[component_container_mt-2] [INFO] [1763568991.636684669] [system.system_monitor.gpu_monitor]: GPUMonitorBase::checkTemp not implemented.
[component_container_mt-2] [INFO] [1763568991.636807996] [system.system_monitor.gpu_monitor]: GPUMonitorBase::checkUsage not implemented.
[component_container_mt-2] [INFO] [1763568991.636826044] [system.system_monitor.gpu_monitor]: GPUMonitorBase::checkMemoryUsage not implemented.
[component_container_mt-2] [INFO] [1763568991.636839004] [system.system_monitor.gpu_monitor]: GPUMonitorBase::checkThrottling not implemented.
[component_container_mt-2] [INFO] [1763568991.636859836] [system.system_monitor.gpu_monitor]: GPUMonitorBase::checkFrequency not implemented.
[component_container_mt-44] [INFO] [1763568991.678832762] [control.collision_detector]: waiting for current odometry...
[component_container_mt-2] [ERROR] [1763568991.835272391] [system.system_monitor.hdd_monitor]: socket connect error. Connection refused
[component_container_mt-2] [ERROR] [1763568991.835418310] [system.system_monitor.hdd_monitor]: Failed to unmount device : overlay
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/control/control_validator' in container '/control/control_check_container'
[component_container_mt-2] [ERROR] [1763568992.048721132] [system.system_monitor.net_monitor]: Failed to connect socket. No such file or directory
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/adapi/node/heartbeat' in container '/adapi/container'
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/adapi/node/interface' in container '/adapi/container'
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/adapi/node/localization' in container '/adapi/container'
[rviz2-51] [INFO] [1763568992.590557027] [rviz2]: Stereo is NOT SUPPORTED
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/adapi/node/motion' in container '/adapi/container'
[component_container_mt-2] [ERROR] [1763568992.801404244] [system.system_monitor.hdd_monitor]: socket connect error. Connection refused
[component_container_mt-2] [ERROR] [1763568992.801584851] [system.system_monitor.hdd_monitor]: Failed to unmount device : overlay
[autoware_ekf_localizer_node-38] [WARN] [1763568992.820708411] [localization.pose_twist_fusion_filter.ekf_localizer]: The node is not activated. Provide initial pose to pose_initializer
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/adapi/node/operation_mode' in container '/adapi/container'
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/adapi/node/perception' in container '/adapi/container'
[component_container_mt-2] [ERROR] [1763568993.048780988] [system.system_monitor.net_monitor]: Failed to connect socket. No such file or directory
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/adapi/node/planning' in container '/adapi/container'
[service_log_checker_node-5] [ERROR] [1763568993.272054324] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/pose_initializer)
[service_log_checker_node-5] [ERROR] [1763568993.275947490] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763568993.276144321] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763568993.279302642] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/default_ad_api/helpers/automatic_pose_initializer)
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/adapi/node/routing' in container '/adapi/container'
[topic_state_monitor_node-11] [INFO] [1763568993.483122212] [system.topic_state_monitor_obstacle_segmentation_pointcloud]: /perception/obstacle_segmentation/pointcloud has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-9] [INFO] [1763568993.503867108] [system.topic_state_monitor_initialpose3d]: /initialpose3d has not received. Set ERROR in diagnostics.
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/adapi/node/vehicle' in container '/adapi/container'
[topic_state_monitor_node-12] [INFO] [1763568993.521275444] [system.topic_state_monitor_object_recognition_objects]: /perception/object_recognition/objects has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-14] [INFO] [1763568993.528245331] [system.topic_state_monitor_mission_planning_route]: /planning/mission_planning/route has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-16] [INFO] [1763568993.537233354] [system.topic_state_monitor_trajectory_follower_control_cmd]: /control/trajectory_follower/control_cmd has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-18] [INFO] [1763568993.572140840] [system.topic_state_monitor_vehicle_status_velocity_status]: /vehicle/status/velocity_status has not received. Set ERROR in diagnostics.
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/adapi/node/vehicle_info' in container '/adapi/container'
[topic_state_monitor_node-15] [INFO] [1763568993.607938787] [system.topic_state_monitor_scenario_planning_trajectory]: /planning/scenario_planning/trajectory has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-17] [INFO] [1763568993.608520928] [system.topic_state_monitor_control_command_control_cmd]: /control/command/control_cmd has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-10] [INFO] [1763568993.624442263] [system.topic_state_monitor_pose_twist_fusion_filter_pose]: /localization/pose_twist_fusion_filter/pose has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-13] [INFO] [1763568993.720630682] [system.topic_state_monitor_traffic_light_recognition_traffic_signals]: /perception/traffic_light_recognition/traffic_signals has not received. Set ERROR in diagnostics.
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/adapi/node/vehicle_door' in container '/adapi/container'
[component_container_mt-2] [ERROR] [1763568993.800979398] [system.system_monitor.hdd_monitor]: socket connect error. Connection refused
[component_container_mt-2] [ERROR] [1763568993.801105606] [system.system_monitor.hdd_monitor]: Failed to unmount device : overlay
[topic_state_monitor_node-19] [INFO] [1763568993.858897499] [system.topic_state_monitor_vehicle_status_steering_status]: /vehicle/status/steering_status has not received. Set ERROR in diagnostics.
[component_container_mt-2] [ERROR] [1763568994.048776973] [system.system_monitor.net_monitor]: Failed to connect socket. No such file or directory
[topic_state_monitor_node-21] [INFO] [1763568994.142079901] [system.topic_state_monitor_transform_map_to_base_link]: /tf has not received. Set ERROR in diagnostics.
[service_log_checker_node-5] [ERROR] [1763568994.283638383] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/pose_initializer)
[service_log_checker_node-5] [ERROR] [1763568994.287151231] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763568994.287322974] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763568994.287401725] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/default_ad_api/helpers/automatic_pose_initializer)
[component_container_mt-44] [INFO] [1763568994.367997385] [control.autonomous_emergency_braking]: [AEB] waiting for ego velocity
[component_container_mt-2] [ERROR] [1763568994.804144968] [system.system_monitor.hdd_monitor]: socket connect error. Connection refused
[component_container_mt-2] [ERROR] [1763568994.804260616] [system.system_monitor.hdd_monitor]: Failed to unmount device : overlay
[autoware_ekf_localizer_node-38] [WARN] [1763568994.840617664] [localization.pose_twist_fusion_filter.ekf_localizer]: The node is not activated. Provide initial pose to pose_initializer
[component_container_mt-2] [ERROR] [1763568995.049102012] [system.system_monitor.net_monitor]: Failed to connect socket. No such file or directory
[service_log_checker_node-5] [ERROR] [1763568995.290712223] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/pose_initializer)
[service_log_checker_node-5] [ERROR] [1763568995.291018909] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763568995.291145053] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763568995.291966745] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/default_ad_api/helpers/automatic_pose_initializer)
[component_container_mt-43] [INFO] [1763568995.499653817] [control.trajectory_follower.controller_node_exe]: Waiting for acceleration data
[component_container_mt-43] [INFO] [1763568995.499810456] [control.trajectory_follower.controller_node_exe]: Control is skipped since input data is not ready.
[component_container_mt-2] [ERROR] [1763568995.804995445] [system.system_monitor.hdd_monitor]: socket connect error. Connection refused
[component_container_mt-2] [ERROR] [1763568995.805144116] [system.system_monitor.hdd_monitor]: Failed to unmount device : overlay
[component_container_mt-2] [ERROR] [1763568996.048850670] [system.system_monitor.net_monitor]: Failed to connect socket. No such file or directory
[service_log_checker_node-5] [ERROR] [1763568996.294602141] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/pose_initializer)
[service_log_checker_node-5] [ERROR] [1763568996.295861336] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763568996.296039607] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763568996.296916979] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/default_ad_api/helpers/automatic_pose_initializer)
[component_container_mt-44] [INFO] [1763568996.448567286] [control.trajectory_follower.lane_departure_checker_node]: waiting for current_twist msg...
[topic_state_monitor_node-12] [INFO] [1763568996.521289477] [system.topic_state_monitor_object_recognition_objects]: /perception/object_recognition/objects has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-14] [INFO] [1763568996.528269957] [system.topic_state_monitor_mission_planning_route]: /planning/mission_planning/route has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-16] [INFO] [1763568996.537245756] [system.topic_state_monitor_trajectory_follower_control_cmd]: /control/trajectory_follower/control_cmd has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-18] [INFO] [1763568996.572158330] [system.topic_state_monitor_vehicle_status_velocity_status]: /vehicle/status/velocity_status has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-11] [INFO] [1763568996.583083560] [system.topic_state_monitor_obstacle_segmentation_pointcloud]: /perception/obstacle_segmentation/pointcloud has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-9] [INFO] [1763568996.603539785] [system.topic_state_monitor_initialpose3d]: /initialpose3d has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-10] [INFO] [1763568996.624467528] [system.topic_state_monitor_pose_twist_fusion_filter_pose]: /localization/pose_twist_fusion_filter/pose has not received. Set ERROR in diagnostics.
[component_container_mt-44] [INFO] [1763568996.678890957] [control.collision_detector]: waiting for current odometry...
[topic_state_monitor_node-15] [INFO] [1763568996.707794695] [system.topic_state_monitor_scenario_planning_trajectory]: /planning/scenario_planning/trajectory has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-17] [INFO] [1763568996.708322533] [system.topic_state_monitor_control_command_control_cmd]: /control/command/control_cmd has not received. Set ERROR in diagnostics.
[component_container_mt-2] [ERROR] [1763568996.801172407] [system.system_monitor.hdd_monitor]: socket connect error. Connection refused
[component_container_mt-2] [ERROR] [1763568996.801338679] [system.system_monitor.hdd_monitor]: Failed to unmount device : overlay
[topic_state_monitor_node-13] [INFO] [1763568996.820981148] [system.topic_state_monitor_traffic_light_recognition_traffic_signals]: /perception/traffic_light_recognition/traffic_signals has not received. Set ERROR in diagnostics.
[autoware_ekf_localizer_node-38] [WARN] [1763568996.861053379] [localization.pose_twist_fusion_filter.ekf_localizer]: The node is not activated. Provide initial pose to pose_initializer
[topic_state_monitor_node-19] [INFO] [1763568996.958885790] [system.topic_state_monitor_vehicle_status_steering_status]: /vehicle/status/steering_status has not received. Set ERROR in diagnostics.
[component_container_mt-2] [ERROR] [1763568997.049697466] [system.system_monitor.net_monitor]: Failed to connect socket. No such file or directory
[topic_state_monitor_node-21] [INFO] [1763568997.142104623] [system.topic_state_monitor_transform_map_to_base_link]: /tf has not received. Set ERROR in diagnostics.
[service_log_checker_node-5] [ERROR] [1763568997.301812941] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/pose_initializer)
[service_log_checker_node-5] [ERROR] [1763568997.302151755] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763568997.302369354] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763568997.302568329] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/default_ad_api/helpers/automatic_pose_initializer)
[component_container_mt-2] [ERROR] [1763568997.802978752] [system.system_monitor.hdd_monitor]: socket connect error. Connection refused
[component_container_mt-2] [ERROR] [1763568997.803116287] [system.system_monitor.hdd_monitor]: Failed to unmount device : overlay
[component_container_mt-2] [ERROR] [1763568998.049073422] [system.system_monitor.net_monitor]: Failed to connect socket. No such file or directory
[service_log_checker_node-5] [ERROR] [1763568998.305251181] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/pose_initializer)
[service_log_checker_node-5] [ERROR] [1763568998.305520716] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763568998.305631212] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763568998.306493896] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/default_ad_api/helpers/automatic_pose_initializer)
[component_container_mt-2] [ERROR] [1763568998.804557321] [system.system_monitor.hdd_monitor]: socket connect error. Connection refused
[component_container_mt-2] [ERROR] [1763568998.804706696] [system.system_monitor.hdd_monitor]: Failed to unmount device : overlay
[autoware_ekf_localizer_node-38] [WARN] [1763568998.880667017] [localization.pose_twist_fusion_filter.ekf_localizer]: The node is not activated. Provide initial pose to pose_initializer
[component_container_mt-2] [ERROR] [1763568999.049345981] [system.system_monitor.net_monitor]: Failed to connect socket. No such file or directory
[service_log_checker_node-5] [ERROR] [1763568999.309020717] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/pose_initializer)
[service_log_checker_node-5] [ERROR] [1763568999.309333227] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763568999.309464587] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763568999.309696106] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/default_ad_api/helpers/automatic_pose_initializer)
[component_container_mt-44] [INFO] [1763568999.467359889] [control.autonomous_emergency_braking]: [AEB] waiting for ego velocity
[topic_state_monitor_node-12] [INFO] [1763568999.521315383] [system.topic_state_monitor_object_recognition_objects]: /perception/object_recognition/objects has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-14] [INFO] [1763568999.528362903] [system.topic_state_monitor_mission_planning_route]: /planning/mission_planning/route has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-16] [INFO] [1763568999.537262285] [system.topic_state_monitor_trajectory_follower_control_cmd]: /control/trajectory_follower/control_cmd has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-18] [INFO] [1763568999.572172716] [system.topic_state_monitor_vehicle_status_velocity_status]: /vehicle/status/velocity_status has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-11] [INFO] [1763568999.583164281] [system.topic_state_monitor_obstacle_segmentation_pointcloud]: /perception/obstacle_segmentation/pointcloud has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-10] [INFO] [1763568999.624489978] [system.topic_state_monitor_pose_twist_fusion_filter_pose]: /localization/pose_twist_fusion_filter/pose has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-9] [INFO] [1763568999.703514765] [system.topic_state_monitor_initialpose3d]: /initialpose3d has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-15] [INFO] [1763568999.707828313] [system.topic_state_monitor_scenario_planning_trajectory]: /planning/scenario_planning/trajectory has not received. Set ERROR in diagnostics.
[component_container_mt-2] [ERROR] [1763568999.802664482] [system.system_monitor.hdd_monitor]: socket connect error. Connection refused
[component_container_mt-2] [ERROR] [1763568999.802804482] [system.system_monitor.hdd_monitor]: Failed to unmount device : overlay
[topic_state_monitor_node-17] [INFO] [1763568999.808409512] [system.topic_state_monitor_control_command_control_cmd]: /control/command/control_cmd has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-13] [INFO] [1763568999.920573441] [system.topic_state_monitor_traffic_light_recognition_traffic_signals]: /perception/traffic_light_recognition/traffic_signals has not received. Set ERROR in diagnostics.
[component_container_mt-2] [ERROR] [1763569000.048998255] [system.system_monitor.net_monitor]: Failed to connect socket. No such file or directory
[topic_state_monitor_node-19] [INFO] [1763569000.058866082] [system.topic_state_monitor_vehicle_status_steering_status]: /vehicle/status/steering_status has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-21] [INFO] [1763569000.242077203] [system.topic_state_monitor_transform_map_to_base_link]: /tf has not received. Set ERROR in diagnostics.
[service_log_checker_node-5] [ERROR] [1763569000.313851239] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/pose_initializer)
[service_log_checker_node-5] [ERROR] [1763569000.315078209] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763569000.325396274] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763569000.325955375] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/default_ad_api/helpers/automatic_pose_initializer)
[component_container_mt-43] [INFO] [1763569000.509598142] [control.trajectory_follower.controller_node_exe]: Waiting for acceleration data
[component_container_mt-43] [INFO] [1763569000.509710493] [control.trajectory_follower.controller_node_exe]: Control is skipped since input data is not ready.
[component_container_mt-2] [ERROR] [1763569000.801287961] [system.system_monitor.hdd_monitor]: socket connect error. Connection refused
[component_container_mt-2] [ERROR] [1763569000.801433945] [system.system_monitor.hdd_monitor]: Failed to unmount device : overlay
[autoware_ekf_localizer_node-38] [WARN] [1763569000.900660110] [localization.pose_twist_fusion_filter.ekf_localizer]: The node is not activated. Provide initial pose to pose_initializer
[component_container_mt-2] [ERROR] [1763569001.049289951] [system.system_monitor.net_monitor]: Failed to connect socket. No such file or directory
[service_log_checker_node-5] [ERROR] [1763569001.329322512] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/pose_initializer)
[service_log_checker_node-5] [ERROR] [1763569001.329725838] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763569001.329875054] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763569001.330269996] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/default_ad_api/helpers/automatic_pose_initializer)
[component_container_mt-44] [INFO] [1763569001.548578042] [control.trajectory_follower.lane_departure_checker_node]: waiting for current_twist msg...
[component_container_mt-44] [INFO] [1763569001.678990911] [control.collision_detector]: waiting for current odometry...
[component_container_mt-2] [ERROR] [1763569001.803659647] [system.system_monitor.hdd_monitor]: socket connect error. Connection refused
[component_container_mt-2] [ERROR] [1763569001.803867838] [system.system_monitor.hdd_monitor]: Failed to unmount device : overlay
[component_container_mt-2] [ERROR] [1763569002.049060496] [system.system_monitor.net_monitor]: Failed to connect socket. No such file or directory
[service_log_checker_node-5] [ERROR] [1763569002.333240943] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/pose_initializer)
[service_log_checker_node-5] [ERROR] [1763569002.333706924] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763569002.333836876] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763569002.334667592] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/default_ad_api/helpers/automatic_pose_initializer)
[topic_state_monitor_node-14] [INFO] [1763569002.528453160] [system.topic_state_monitor_mission_planning_route]: /planning/mission_planning/route has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-12] [INFO] [1763569002.621270235] [system.topic_state_monitor_object_recognition_objects]: /perception/object_recognition/objects has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-16] [INFO] [1763569002.637263313] [system.topic_state_monitor_trajectory_follower_control_cmd]: /control/trajectory_follower/control_cmd has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-18] [INFO] [1763569002.672289999] [system.topic_state_monitor_vehicle_status_velocity_status]: /vehicle/status/velocity_status has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-11] [INFO] [1763569002.683133469] [system.topic_state_monitor_obstacle_segmentation_pointcloud]: /perception/obstacle_segmentation/pointcloud has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-9] [INFO] [1763569002.703571742] [system.topic_state_monitor_initialpose3d]: /initialpose3d has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-10] [INFO] [1763569002.724473246] [system.topic_state_monitor_pose_twist_fusion_filter_pose]: /localization/pose_twist_fusion_filter/pose has not received. Set ERROR in diagnostics.
[component_container_mt-2] [ERROR] [1763569002.802492405] [system.system_monitor.hdd_monitor]: socket connect error. Connection refused
[component_container_mt-2] [ERROR] [1763569002.802667572] [system.system_monitor.hdd_monitor]: Failed to unmount device : overlay
[topic_state_monitor_node-15] [INFO] [1763569002.807809980] [system.topic_state_monitor_scenario_planning_trajectory]: /planning/scenario_planning/trajectory has not received. Set ERROR in diagnostics.
[autoware_ekf_localizer_node-38] [WARN] [1763569002.900719983] [localization.pose_twist_fusion_filter.ekf_localizer]: The node is not activated. Provide initial pose to pose_initializer
[topic_state_monitor_node-17] [INFO] [1763569002.908309900] [system.topic_state_monitor_control_command_control_cmd]: /control/command/control_cmd has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-13] [INFO] [1763569002.921313808] [system.topic_state_monitor_traffic_light_recognition_traffic_signals]: /perception/traffic_light_recognition/traffic_signals has not received. Set ERROR in diagnostics.
[component_container_mt-2] [ERROR] [1763569003.049090337] [system.system_monitor.net_monitor]: Failed to connect socket. No such file or directory
[topic_state_monitor_node-19] [INFO] [1763569003.058893588] [system.topic_state_monitor_vehicle_status_steering_status]: /vehicle/status/steering_status has not received. Set ERROR in diagnostics.
[service_log_checker_node-5] [ERROR] [1763569003.337930730] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/pose_initializer)
[service_log_checker_node-5] [ERROR] [1763569003.338287208] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763569003.338519527] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763569003.338712806] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/default_ad_api/helpers/automatic_pose_initializer)
[topic_state_monitor_node-21] [INFO] [1763569003.342072118] [system.topic_state_monitor_transform_map_to_base_link]: /tf has not received. Set ERROR in diagnostics.
[component_container_mt-2] [ERROR] [1763569003.803948479] [system.system_monitor.hdd_monitor]: socket connect error. Connection refused
[component_container_mt-2] [ERROR] [1763569003.804280253] [system.system_monitor.hdd_monitor]: Failed to unmount device : overlay
[component_container_mt-2] [ERROR] [1763569004.048823283] [system.system_monitor.net_monitor]: Failed to connect socket. No such file or directory
[service_log_checker_node-5] [ERROR] [1763569004.342015911] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/pose_initializer)
[service_log_checker_node-5] [ERROR] [1763569004.344047358] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763569004.344389820] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763569004.344572731] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/default_ad_api/helpers/automatic_pose_initializer)
[component_container_mt-44] [INFO] [1763569004.467411460] [control.autonomous_emergency_braking]: [AEB] waiting for ego velocity
[component_container_mt-2] [ERROR] [1763569004.802849077] [system.system_monitor.hdd_monitor]: socket connect error. Connection refused
[component_container_mt-2] [ERROR] [1763569004.803044788] [system.system_monitor.hdd_monitor]: Failed to unmount device : overlay
[autoware_ekf_localizer_node-38] [WARN] [1763569004.920654228] [localization.pose_twist_fusion_filter.ekf_localizer]: The node is not activated. Provide initial pose to pose_initializer
[component_container_mt-2] [ERROR] [1763569005.048826755] [system.system_monitor.net_monitor]: Failed to connect socket. No such file or directory
[service_log_checker_node-5] [ERROR] [1763569005.347743197] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/pose_initializer)
[service_log_checker_node-5] [ERROR] [1763569005.348520826] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763569005.349550165] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763569005.350423473] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/default_ad_api/helpers/automatic_pose_initializer)
[component_container_mt-43] [INFO] [1763569005.519581219] [control.trajectory_follower.controller_node_exe]: Waiting for acceleration data
[component_container_mt-43] [INFO] [1763569005.519690722] [control.trajectory_follower.controller_node_exe]: Control is skipped since input data is not ready.
[topic_state_monitor_node-14] [INFO] [1763569005.628229421] [system.topic_state_monitor_mission_planning_route]: /planning/mission_planning/route has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-16] [INFO] [1763569005.637314211] [system.topic_state_monitor_trajectory_follower_control_cmd]: /control/trajectory_follower/control_cmd has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-18] [INFO] [1763569005.672976446] [system.topic_state_monitor_vehicle_status_velocity_status]: /vehicle/status/velocity_status has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-12] [INFO] [1763569005.721300926] [system.topic_state_monitor_object_recognition_objects]: /perception/object_recognition/objects has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-10] [INFO] [1763569005.724478288] [system.topic_state_monitor_pose_twist_fusion_filter_pose]: /localization/pose_twist_fusion_filter/pose has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-11] [INFO] [1763569005.783069921] [system.topic_state_monitor_obstacle_segmentation_pointcloud]: /perception/obstacle_segmentation/pointcloud has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-9] [INFO] [1763569005.803509922] [system.topic_state_monitor_initialpose3d]: /initialpose3d has not received. Set ERROR in diagnostics.
[component_container_mt-2] [ERROR] [1763569005.803595330] [system.system_monitor.hdd_monitor]: socket connect error. Connection refused
[component_container_mt-2] [ERROR] [1763569005.803711105] [system.system_monitor.hdd_monitor]: Failed to unmount device : overlay
[topic_state_monitor_node-15] [INFO] [1763569005.907850592] [system.topic_state_monitor_scenario_planning_trajectory]: /planning/scenario_planning/trajectory has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-17] [INFO] [1763569006.008295311] [system.topic_state_monitor_control_command_control_cmd]: /control/command/control_cmd has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-13] [INFO] [1763569006.020572375] [system.topic_state_monitor_traffic_light_recognition_traffic_signals]: /perception/traffic_light_recognition/traffic_signals has not received. Set ERROR in diagnostics.
[component_container_mt-2] [ERROR] [1763569006.049116659] [system.system_monitor.net_monitor]: Failed to connect socket. No such file or directory
[topic_state_monitor_node-19] [INFO] [1763569006.158874519] [system.topic_state_monitor_vehicle_status_steering_status]: /vehicle/status/steering_status has not received. Set ERROR in diagnostics.
[topic_state_monitor_node-21] [INFO] [1763569006.342355687] [system.topic_state_monitor_transform_map_to_base_link]: /tf has not received. Set ERROR in diagnostics.
[service_log_checker_node-5] [ERROR] [1763569006.355272939] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/pose_initializer)
[service_log_checker_node-5] [ERROR] [1763569006.355803945] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763569006.355914440] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763569006.357878591] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/default_ad_api/helpers/automatic_pose_initializer)
[component_container_mt-44] [INFO] [1763569006.648767934] [control.trajectory_follower.lane_departure_checker_node]: waiting for current_twist msg...
[component_container_mt-44] [INFO] [1763569006.778887621] [control.collision_detector]: waiting for current odometry...
[component_container_mt-2] [ERROR] [1763569006.804993260] [system.system_monitor.hdd_monitor]: socket connect error. Connection refused
[component_container_mt-2] [ERROR] [1763569006.805118411] [system.system_monitor.hdd_monitor]: Failed to unmount device : overlay
[autoware_ekf_localizer_node-38] [WARN] [1763569006.940617913] [localization.pose_twist_fusion_filter.ekf_localizer]: The node is not activated. Provide initial pose to pose_initializer
[component_container_mt-2] [ERROR] [1763569007.048787493] [system.system_monitor.net_monitor]: Failed to connect socket. No such file or directory
[service_log_checker_node-5] [ERROR] [1763569007.359674503] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/pose_initializer)
[service_log_checker_node-5] [ERROR] [1763569007.361464639] [system.service_log_checker]: /localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763569007.361686622] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/adapi/node/localization)
[service_log_checker_node-5] [ERROR] [1763569007.361832094] [system.service_log_checker]: /api/localization/initialize: status code 1 'The vehicle is not stopped.' (/localization/util/default_ad_api/helpers/automatic_pose_initializer)
[component_container_mt-2] [ERROR] [1763569007.804241056] [system.system_monitor.hdd_monitor]: socket connect error. Connection refused
[component_container_mt-2] [ERROR] [1763569007.804367136] [system.system_monitor.hdd_monitor]: Failed to unmount device : overlay
[component_container_mt-2] [ERROR] [1763569008.048900245] [system.system_monitor.net_monitor]: Failed to connect socket. No such file or directory
^C[WARNING] [launch]: user interrupted with ctrl-c (SIGINT)
[WARNING] [launch_ros.actions.load_composable_nodes]: Abandoning wait for the '/control/control_container/_container/load_node' service response, due to shutdown.
[static_transform_publisher-53] [INFO] [1763569008.113923496] [rclcpp]: signal_handler(signum=2)
[INFO] [topic_state_monitor_node-11]: process has finished cleanly [pid 7986]
[INFO] [autoware_vehicle_velocity_converter_node-33]: process has finished cleanly [pid 8264]
[INFO] [topic_state_monitor_node-18]: process has finished cleanly [pid 8160]
[INFO] [duplicated_node_checker_node-3]: process has finished cleanly [pid 7970]
[INFO] [service_log_checker_node-5]: process has finished cleanly [pid 7974]
[INFO] [static_transform_publisher-53]: process has finished cleanly [pid 8592]
[INFO] [topic_state_monitor_node-17]: process has finished cleanly [pid 8142]
[INFO] [topic_state_monitor_node-16]: process has finished cleanly [pid 8124]
[INFO] [topic_state_monitor_node-21]: process has finished cleanly [pid 8185]
[INFO] [routing_adaptor_node-49]: process has finished cleanly [pid 8515]
[INFO] [autoware_twist2accel_node-40]: process has finished cleanly [pid 8427]
[INFO] [topic_state_monitor_node-9]: process has finished cleanly [pid 7982]
[INFO] [component_container-23]: process has finished cleanly [pid 8190]
[INFO] [topic_state_monitor_node-14]: process has finished cleanly [pid 8110]
[INFO] [initial_pose_adaptor_node-48]: process has finished cleanly [pid 8507]
[INFO] [topic_state_monitor_node-8]: process has finished cleanly [pid 7980]
[INFO] [topic_state_monitor_node-10]: process has finished cleanly [pid 7984]
[INFO] [mrm_handler_node-27]: process has finished cleanly [pid 8207]
[INFO] [control_evaluator-45]: process has finished cleanly [pid 8476]
[INFO] [gyro_bias_estimator_node-32]: process has finished cleanly [pid 8248]
[INFO] [autoware_gyro_odometer_node-35]: process has finished cleanly [pid 8315]
[INFO] [component_state_diagnostics-25]: process has finished cleanly [pid 8196]
[INFO] [web_server.py-47]: process has finished cleanly [pid 8504]
[INFO] [autoware_pose_initializer_node-36]: process has finished cleanly [pid 8328]
[INFO] [autoware_localization_error_monitor_node-42]: process has finished cleanly [pid 8436]
[INFO] [autoware_map_projection_loader_node-30]: process has finished cleanly [pid 8226]
[INFO] [autoware_ndt_scan_matcher_node-34]: process has finished cleanly [pid 8305]
[INFO] [autoware_pose_instability_detector_node-41]: process has finished cleanly [pid 8432]
[INFO] [topic_state_monitor_node-7]: process has finished cleanly [pid 7978]
[INFO] [component_container-22]: process has finished cleanly [pid 8188]
[INFO] [map_hash_generator-29]: process has finished cleanly [pid 8223]
[component_container_mt-50] [INFO] [1763569008.113925000] [rclcpp]: signal_handler(signum=2)
[INFO] [autoware_ekf_localizer_node-38]: process has finished cleanly [pid 8373]
[autoware_stop_filter_node-39] [INFO] [1763569008.113948648] [rclcpp]: signal_handler(signum=2)
[INFO] [topic_state_monitor_node-15]: process has finished cleanly [pid 8120]
[component_container_mt-44] [INFO] [1763569008.113962216] [rclcpp]: signal_handler(signum=2)
[component_container_mt-43] [INFO] [1763569008.113964040] [rclcpp]: signal_handler(signum=2)
[rqt_runtime_monitor-52] [INFO] [1763569008.113943816] [rclcpp]: signal_handler(signum=2)
[autoware_localization_error_monitor_node-42] [INFO] [1763569008.113978312] [rclcpp]: signal_handler(signum=2)
[autoware_twist2accel_node-40] [INFO] [1763569008.113997032] [rclcpp]: signal_handler(signum=2)
[initial_pose_adaptor_node-48] [INFO] [1763569008.114061992] [rclcpp]: signal_handler(signum=2)
[autoware_pose_initializer_node-36] [INFO] [1763569008.114068136] [rclcpp]: signal_handler(signum=2)
[topic_state_monitor_node-17] [INFO] [1763569008.114099304] [rclcpp]: signal_handler(signum=2)
[topic_state_monitor_node-14] [INFO] [1763569008.114136071] [rclcpp]: signal_handler(signum=2)
[routing_adaptor_node-49] [INFO] [1763569008.114143271] [rclcpp]: signal_handler(signum=2)
[component_container_mt-28] [INFO] [1763569008.114187783] [rclcpp]: signal_handler(signum=2)
[component_container-6] [INFO] [1763569008.114179079] [rclcpp]: signal_handler(signum=2)
[imu_corrector_node-31] [INFO] [1763569008.114166631] [rclcpp]: signal_handler(signum=2)
[service_log_checker_node-5] [INFO] [1763569008.114183559] [rclcpp]: signal_handler(signum=2)
[control_evaluator-45] [INFO] [1763569008.114211911] [rclcpp]: signal_handler(signum=2)
[topic_state_monitor_node-12] [INFO] [1763569008.114216231] [rclcpp]: signal_handler(signum=2)
[topic_state_monitor_node-13] [INFO] [1763569008.114223463] [rclcpp]: signal_handler(signum=2)
[topic_state_monitor_node-11] [INFO] [1763569008.114271239] [rclcpp]: signal_handler(signum=2)
[mrm_handler_node-27] [INFO] [1763569008.114273991] [rclcpp]: signal_handler(signum=2)
[topic_state_monitor_node-8] [INFO] [1763569008.114301191] [rclcpp]: signal_handler(signum=2)
[component_container-23] [INFO] [1763569008.114300743] [rclcpp]: signal_handler(signum=2)
[topic_state_monitor_node-16] [INFO] [1763569008.114344646] [rclcpp]: signal_handler(signum=2)
[topic_state_monitor_node-19] [INFO] [1763569008.114354502] [rclcpp]: signal_handler(signum=2)
[processing_time_checker_node-4] [INFO] [1763569008.114391942] [rclcpp]: signal_handler(signum=2)
[topic_state_monitor_node-18] [INFO] [1763569008.114416166] [rclcpp]: signal_handler(signum=2)
[topic_state_monitor_node-9] [INFO] [1763569008.114428550] [rclcpp]: signal_handler(signum=2)
[INFO] [topic_state_monitor_node-19]: process has finished cleanly [pid 8166]
[topic_state_monitor_node-10] [INFO] [1763569008.114435750] [rclcpp]: signal_handler(signum=2)
[topic_state_monitor_node-21] [INFO] [1763569008.114429094] [rclcpp]: signal_handler(signum=2)
[autoware_ndt_scan_matcher_node-34] [INFO] [1763569008.114502054] [rclcpp]: signal_handler(signum=2)
[topic_state_monitor_node-7] [INFO] [1763569008.114531558] [rclcpp]: signal_handler(signum=2)
[autoware_gyro_odometer_node-35] [INFO] [1763569008.114574629] [rclcpp]: signal_handler(signum=2)
[component_container_mt-2] [INFO] [1763569008.114581125] [rclcpp]: signal_handler(signum=2)
[converter-26] [INFO] [1763569008.114651045] [rclcpp]: signal_handler(signum=2)
[autoware_pose_instability_detector_node-41] [INFO] [1763569008.114752644] [rclcpp]: signal_handler(signum=2)
[component_container-22] [INFO] [1763569008.115258402] [rclcpp]: signal_handler(signum=2)
[autoware_vehicle_velocity_converter_node-33] [INFO] [1763569008.118149685] [rclcpp]: signal_handler(signum=2)
[duplicated_node_checker_node-3] [INFO] [1763569008.118675250] [rclcpp]: signal_handler(signum=2)
[component_container_mt-46] [INFO] [1763569008.119228848] [rclcpp]: signal_handler(signum=2)
[topic_state_monitor_node-15] [INFO] [1763569008.122785343] [rclcpp]: signal_handler(signum=2)
[autoware_map_projection_loader_node-30] [INFO] [1763569008.116032639] [rclcpp]: signal_handler(signum=2)
[autoware_ekf_localizer_node-38] [INFO] [1763569008.126932364] [rclcpp]: signal_handler(signum=2)
[component_container_mt-1] [INFO] [1763569008.119222416] [rclcpp]: signal_handler(signum=2)
[automatic_pose_initializer_node-37] [INFO] [1763569008.114185767] [rclcpp]: signal_handler(signum=2)
[gyro_bias_estimator_node-32] [INFO] [1763569008.115902367] [rclcpp]: signal_handler(signum=2)
[topic_state_monitor_node-20] [INFO] [1763569008.129504064] [rclcpp]: signal_handler(signum=2)
[aggregator_node-24] [INFO] [1763569008.197395942] [rclcpp]: signal_handler(signum=2)
[rviz2-51] [INFO] [1763569008.113924136] [rclcpp]: signal_handler(signum=2)
[INFO] [autoware_stop_filter_node-39]: process has finished cleanly [pid 8406]
[INFO] [automatic_pose_initializer_node-37]: process has finished cleanly [pid 8331]
[INFO] [converter-26]: process has finished cleanly [pid 8198]
[INFO] [component_container_mt-1]: process has finished cleanly [pid 7966]
[INFO] [topic_state_monitor_node-13]: process has finished cleanly [pid 8108]
[ERROR] [launch]: Caught exception in launch (see debug for traceback): cannot use Destroyable because destruction was requested
[INFO] [topic_state_monitor_node-20]: process has finished cleanly [pid 8178]
[INFO] [imu_corrector_node-31]: process has finished cleanly [pid 8240]
[INFO] [processing_time_checker_node-4]: process has finished cleanly [pid 7972]
[INFO] [aggregator_node-24]: process has finished cleanly [pid 8192]
[INFO] [rqt_runtime_monitor-52]: process has finished cleanly [pid 8558]
[INFO] [component_container_mt-50]: process has finished cleanly [pid 8545]
[INFO] [component_container_mt-28]: process has finished cleanly [pid 8221]
[INFO] [component_container_mt-43]: process has finished cleanly [pid 8456]
[INFO] [component_container_mt-44]: process has finished cleanly [pid 8466]
[INFO] [component_container_mt-2]: process has finished cleanly [pid 7968]
[INFO] [component_container_mt-46]: process has finished cleanly [pid 8479]



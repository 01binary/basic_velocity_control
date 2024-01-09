cmake_minimum_required(VERSION 3.0.2)
project(basic_velocity_control)

find_package(
  catkin
  REQUIRED COMPONENTS
    actionlib
    angles
    control_msgs
    control_toolbox
    controller_interface
    controller_manager
    hardware_interface
    pluginlib
    realtime_tools
    roscpp
    trajectory_msgs
    urdf
)

catkin_package(
  CATKIN_DEPENDS
    actionlib
    angles
    control_msgs
    control_toolbox
    controller_interface
    controller_manager
    hardware_interface
    realtime_tools
    roscpp
    trajectory_msgs
    urdf
  INCLUDE_DIRS
    src
  LIBRARIES
    ${PROJECT_NAME}
)

include_directories(
  src
  ${catkin_INCLUDE_DIRS}
)

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
    hardware_interface
    realtime_tools
    roscpp
    trajectory_msgs
    urdf
  INCLUDE_DIRS
    include
  LIBRARIES
    ${PROJECT_NAME}
)

include_directories(
  include ${catkin_INCLUDE_DIRS}
)

add_executable(
  rrbot
    src/rrbot.cpp
)

add_dependencies(
  rrbot
    ${${PROJECT_NAME}_EXPORTED_TARGETS}
    ${catkin_EXPORTED_TARGETS}
)

target_link_libraries(
  rrbot
    ${catkin_LIBRARIES}
)

install(
  TARGETS
    rrbot
  RUNTIME DESTINATION
    ${CATKIN_PACKAGE_BIN_DESTINATION}
)

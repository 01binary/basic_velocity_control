cmake_minimum_required(VERSION 3.1.3)
project(basic_velocity_control)

find_package(catkin REQUIRED)

catkin_package()

install(DIRECTORY description DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
install(DIRECTORY config DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})

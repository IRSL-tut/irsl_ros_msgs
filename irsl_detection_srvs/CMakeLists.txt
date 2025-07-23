cmake_minimum_required(VERSION 3.0.2)
project(irsl_detection_srvs)

## Compile as C++11, supported in ROS Kinetic and newer
add_compile_options(-std=c++11)

find_package(catkin REQUIRED COMPONENTS
  std_msgs
  sensor_msgs
  irsl_detection_msgs
  message_generation
)

## Generate messages in the 'msg' folder
# add_message_files(
#  FILES
# )

## Generate services in the 'srv' folder
add_service_files(
  FILES
  GetInstanceSegmentation.srv
)

## Generate actions in the 'action' folder
# add_action_files(
#   FILES
#   Action1.action
#   Action2.action
# )

## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs
  sensor_msgs
  irsl_detection_msgs
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES irsl_ros_msgs 
#  CATKIN_DEPENDS std_msgs
#  DEPENDS system_lib
CATKIN_DEPENDS message_runtime
)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)
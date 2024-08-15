cmake_minimum_required(VERSION 3.0.2)
project(pycram_msgs)

find_package(catkin REQUIRED COMPONENTS
  std_msgs
  message_generation
  rospy
  roscpp
)

add_message_files(
  FILES
  ObjectIdentifier.msg
  ObjectIdentifierArray.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs
)

catkin_package(
  CATKIN_DEPENDS message_runtime std_msgs rospy roscpp
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)


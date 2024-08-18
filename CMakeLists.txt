cmake_minimum_required(VERSION 2.8.3)
project(hdmap_msgs)

find_package(catkin REQUIRED COMPONENTS
  geometry_msgs
  std_msgs
  message_generation
  nav_msgs
)


add_message_files(
  FILES
  HDMap.msg
  Vector.msg
)


generate_messages(
  DEPENDENCIES
  std_msgs
  geometry_msgs
  nav_msgs
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)

catkin_package()
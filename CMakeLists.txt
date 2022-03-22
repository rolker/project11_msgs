cmake_minimum_required(VERSION 2.8.3)
project(project11_msgs)
find_package(catkin REQUIRED roscpp std_msgs message_generation geographic_msgs)

add_message_files(
  FILES
  NavSource.msg
  PIDDebug.msg
  PIDParameters.msg
  Platform.msg
  PlatformList.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs
  geographic_msgs
)

catkin_package(CATKIN_DEPENDS message_runtime geographic_msgs)

cmake_minimum_required(VERSION 2.8.3)
project(project11_msgs)
find_package(catkin REQUIRED roscpp std_msgs message_generation geographic_msgs marine_acoustic_msgs)

add_message_files(
  FILES
  AcousticLayer.msg
  AcousticSlice.msg
  BehaviorInformation.msg
  Contact.msg
  CourseMadeGood.msg
  CourseMadeGoodStamped.msg
  CTD.msg
  CTDStamped.msg
  Detect.msg
  DifferentialDrive.msg
  GeoPoseNavEuler.msg
  GeoPoseNavEulerStamped.msg
  GeoPoseNavEulerWithCovariance.msg
  GeoPoseNavEulerWithCovarianceStamped.msg
  Heartbeat.msg
  Helm.msg
  KeyValue.msg
  NavEuler.msg
  NavEulerStamped.msg
  NavSource.msg
  PIDDebug.msg
  PIDParameters.msg
  Platform.msg
  PlatformList.msg
  RangeBearing.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs
  geographic_msgs
  marine_acoustic_msgs
)

catkin_package(CATKIN_DEPENDS message_runtime geographic_msgs marine_acoustic_msgs)

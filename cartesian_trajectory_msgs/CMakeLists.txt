cmake_minimum_required(VERSION 2.8.6)

project(cartesian_trajectory_msgs)

find_package(catkin REQUIRED 
  COMPONENTS std_msgs geometry_msgs message_generation)

add_message_files(FILES
  CartesianTrajectory.msg
  CartesianTrajectoryPoint.msg
  CartTrajectory.msg
  CartTrajectoryPoint.msg
  PoseTwist.msg
  PoseTwistStamped.msg
  )

generate_messages(
  DEPENDENCIES
  std_msgs
  geometry_msgs
  )


catkin_package(
  CATKIN_DEPENDS std_msgs geometry_msgs message_runtime)



cmake_minimum_required(VERSION 2.8.3)
project(simRobot_msgs)

find_package(catkin REQUIRED COMPONENTS geometry_msgs message_generation std_msgs )

add_message_files(
  DIRECTORY msg
  FILES
  transformation.msg
	sim_singleArm.msg
	sim_bimanArm.msg
	sim_singleArmTransport.msg
	sim_robot.msg
)

add_service_files(
  DIRECTORY srv
  FILES
  simulateRobotSRV.srv)

generate_messages(DEPENDENCIES geometry_msgs std_msgs )

catkin_package(CATKIN_DEPENDS geometry_msgs message_runtime std_msgs  )

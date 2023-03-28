cmake_minimum_required(VERSION 3.16)



find_package(catkin REQUIRED COMPONENTS
   rospy
   sensor_msgs
   
   
)
project( sparkfun_VR_IMU )
catkin_package(
  CATKIN_DEPENDS rospy sensor_msgs
)

catkin_install_python(PROGRAMS scripts/serial_uart_rvc_ros.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
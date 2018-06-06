cmake_minimum_required(VERSION 2.8)
PROJECT(RDC2018)

find_package(catkin REQUIRED)

include_directories(${catkin_INCLUDE_DIRS})

catkin_package(
#   INCLUDE_DIRS include
#   LIBRARIES CartesianInterface
#  CATKIN_DEPENDS other_catkin_pkg
#  DEPENDS system_lib
)

message(${CATKIN_PACKAGE_SHARE_DESTINATION})

## Mark other files for installation (e.g. launch and bag files, etc.)
install(DIRECTORY launch/
#   # myfile2
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/launch
  FILES_MATCHING PATTERN "*.launch"
)

install(DIRECTORY robot_urdf/
#   # myfile2
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/robot_urdf
  FILES_MATCHING PATTERN "*.urdf"
)

install(DIRECTORY robot_srdf/
#   # myfile2
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/robot_srdf
  FILES_MATCHING PATTERN "*.srdf"
)

install(DIRECTORY joint_map/
#   # myfile2
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/joint_map
  FILES_MATCHING PATTERN "*.yaml"
)

install(DIRECTORY stacks/
#   # myfile2
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/stacks
  FILES_MATCHING PATTERN "*.yaml"
)

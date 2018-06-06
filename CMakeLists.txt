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
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
  FILES_MATCHING PATTERN "*.launch"
)

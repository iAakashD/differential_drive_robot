cmake_minimum_required(VERSION 3.0.2)
project(diffdrive_description)

find_package(catkin REQUIRED COMPONENTS
  rviz
)

catkin_package(
)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)

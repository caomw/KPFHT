cmake_minimum_required(VERSION 2.6 FATAL_ERROR)
project(face_tracker)

# The version number.
set (face_tracker_VERSION_MAJOR 0)
set (face_tracker_VERSION_MINOR 1)

# pcl
find_package(PCL 1.3 REQUIRED)
include_directories(${PCL_INCLUDE_DIRS})
#message(STATUS ${PCL_INCLUDE_DIRS})
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})

add_executable(	face_tracker face_tracker.cpp )

target_link_libraries( face_tracker ${PCL_LIBRARIES})

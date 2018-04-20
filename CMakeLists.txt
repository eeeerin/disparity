cmake_minimum_required(VERSION 3.9)
project(distort)

set(CMAKE_CXX_STANDARD 11)

set( CMAKE_BUILD_TYPE "RELEASE" )

find_package( OpenCV REQUIRED )
include_directories( ${OpenCV_INCLUDE_DIRS} )

find_package( Pangolin REQUIRED )
include_directories( ${Pangolin_INCLUDE_DIRS} )

include_directories( "/usr/include/eigen3" )



add_executable(distort disparity.cpp)
target_link_libraries( distort ${OpenCV_LIBS} ${Pangolin_LIBRARIES} )

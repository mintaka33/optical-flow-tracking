cmake_minimum_required(VERSION 2.8)

project( lkdemo )

find_package( OpenCV REQUIRED )
include_directories( ${OpenCV_INCLUDE_DIRS} )

# need use C++11 to invoke OpenCV
set (CMAKE_CXX_STANDARD 11)

# set debug build option
set (CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -g")

add_executable( lkdemo lkdemo.cpp )

target_link_libraries( lkdemo ${OpenCV_LIBS} )
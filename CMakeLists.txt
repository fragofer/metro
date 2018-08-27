PROJECT(metro)
cmake_minimum_required(VERSION 2.8)

#add_definitions(-D_CRT_SECURE_NO_WARNINGS)

set(CMAKE_CXX_STANDARD 11)

IF(CMAKE_BUILD_TYPE MATCHES Release)
    message("Release mode")
#    set (CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -O3")
#    set (CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Ofast -fopenmp")
     set (CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Ofast")
ENDIF()

IF(CMAKE_BUILD_TYPE MATCHES Debug)
    message("Debug mode")
    set (CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -O0 -Wall")
ENDIF()


add_subdirectory(src)


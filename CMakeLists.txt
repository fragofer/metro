PROJECT(metro)
cmake_minimum_required(VERSION 2.8)

#add_definitions(-D_CRT_SECURE_NO_WARNINGS)

set(CMAKE_CXX_STANDARD 14)

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

set(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} -pthread")

add_subdirectory(src)


set(SOURCE_FILES
        plylib.cpp
        sampling.h)

#add_executable(metro ${SOURCE_FILES})

#install(TARGETS compression DESTINATION ${CMAKE_INSTALL_PREFIX}/bin)
#####################################################

#find_package(Qt5Widgets)
#
#include_directories(/Users/pachi/software/vcglib)
#
#add_executable(metro ${SOURCE_FILES})
#
#target_link_libraries(metro Qt5::Widgets)

#############
# Instruct CMake to run moc automatically when needed.
set(CMAKE_AUTOMOC ON)

# set to the proper directory in your machine
set(Qt5_cmake_DIR /Users/pachi/software/Qt560/5.6/clang_64/lib/cmake)

# This is needded for CMake to find the Qt libraries
set(CMAKE_PREFIX_PATH
        ${Qt5_cmake_DIR}
        CACHE PATH "Qt5 cmake directory" FORCE)

# you can comment the following line
#message ("CMAKE_PREFIX_PATH = ${CMAKE_PREFIX_PATH}")

# alternative way to make CMake find the Qt libraries
# set(Qt5core_DIR    ${Qt5_cmake_DIR}/Qt5core)
#set(Qt5Widgets_DIR ${Qt5_cmake_DIR}/Qt5Widgets)
# set(Qt5Svg_DIR     ${Qt5_cmake_DIR}/Qt5Svg)

# Find the QtWidgets library
#find_package(Qt5core)
find_package(Qt5Widgets)
#find_package(Qt5Svg)


include_directories(/Users/pachi/software/vcglib)

add_executable(metro ${SOURCE_FILES} metro.cpp)

target_link_libraries(metro Qt5::Widgets)

##################################################

#set(CMAKE_AUTOMOC ON)
#
##find_package(Qt4 4.4.3 REQUIRED QtGui QtXml)
#find_package(Qt4 REQUIRED)
#
#add_definitions(-DQT_NO_DEBUG -fPIC)
#
##include_directories(/home/frago/software/vcglib)
#include_directories(/User/pachi/software/vcglib)
#
#add_executable(metro ${SOURCE_FILES})
#
#target_link_libraries(metro Qt4::QtGui)
cmake_minimum_required(VERSION 3.13)
project(git-action-sandbox)
set(CMAKE_CXX_STANDARD 23)

include(CTest)

find_package(PkgConfig REQUIRED)
find_library(SENSORS_LIB sensors)
if (NOT SENSORS_LIB)
    message(FATAL_ERROR "libsensors not found. Please run: sudo apt install libsensors-dev")
endif()

add_subdirectory(deps/gtest)
add_subdirectory(test)
add_executable(cmake_git_actions main.cpp)

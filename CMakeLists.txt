cmake_minimum_required(VERSION 3.13)
project(git-action-sandbox)
set(CMAKE_CXX_STANDARD 23)

include(CTest)

add_subdirectory(deps/gtest)
add_subdirectory(test)
add_executable(cmake_git_actions main.cpp)

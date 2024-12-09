# This configuration file tells CMake to:
#    + Set the C++ standard to C++20.
#    + Include the ImGUI source files from `src` directory.


cmake_minimum_required(VERSION 3.10)
project(imgui)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(imgui imgui.cpp imgui.h)

target_include_directories(imgui PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
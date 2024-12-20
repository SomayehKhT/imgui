# This configuration file tells CMake to:
#    + Set the C++ standard to C++20.
#    + Include the ImGUI source files from `src` directory.
#    + Link against the ImGUI implementation (e.g., `imgui_impl_glfw`) from the `backends` directory.


cmake_minimum_required(VERSION 3.10)
project(imgui)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(imgui 
imgui.cpp 
imgui.h
backends/imgui_impl_sdl3.cpp
backends/imgui_impl_sdl3.h
backends/imgui_impl_dx12.cpp
backends/imgui_impl_dx12.h
imgui_demo.cpp
imgui_draw.cpp
imgui_internal.h
imgui_tables.cpp
imgui_widgets.cpp)

target_link_libraries(imgui PRIVATE SDL3::SDL3)

target_include_directories(imgui PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

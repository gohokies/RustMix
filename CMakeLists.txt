cmake_minimum_required(VERSION 3.18)

project(CMakeRustExternal
        VERSION "0.1.0"
        DESCRIPTION "A demo CMake project with components written in Rust.")

set(CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/cmake" ${CMAKE_MODULE_PATH})

set(CMAKE_POSITION_INDEPENDENT_CODE ON)

find_package(Rust REQUIRED)

add_subdirectory(rust)
add_subdirectory(cpp)
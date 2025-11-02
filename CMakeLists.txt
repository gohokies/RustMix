cmake_minimum_required(VERSION 3.28)

project(CMakeRustExternal
        VERSION "0.1.0"
        DESCRIPTION "A demo CMake project with components written in Rust.")

set(CMAKE_POSITION_INDEPENDENT_CODE ON)

add_subdirectory(rust)
add_subdirectory(cpp)
add_executable(CppDemo main.cpp)

add_dependencies(CppDemo build_rust_libs)
find_library(RustAlgorithmsLib NAMES algorithms PATHS ${CMAKE_BINARY_DIR}/rust/target/$<IF:$<CONFIG:DEBUG>,debug,release> OUTPUT_VARIABLE RUST_LIB_FOUND)
if (NOT RustAlgorithmsLib)
    message(FATAL_ERROR "Could not find Rust algorithms library")
endif()
target_link_libraries(CppDemo PRIVATE ${RustAlgorithmsLib})
cmake_minimum_required(VERSION 3.10)

project(Program VERSION 1.0)

add_subdirectory(source)

add_executable(static_block program.c)

target_link_libraries(static_block PUBLIC Block)

target_include_directories(static_block PUBLIC
                          "${PROJECT_BINARY_DIR}"
                          "${PROJECT_SOURCE_DIR}/headers"
                          )

add_executable(dynamic_block program.c)

target_link_libraries(dynamic_block PUBLIC Block_shared)

target_include_directories(dynamic_block PUBLIC
                          "${PROJECT_BINARY_DIR}"
                          "${PROJECT_SOURCE_DIR}/headers"
                          )

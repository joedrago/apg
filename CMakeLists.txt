cmake_minimum_required(VERSION 3.10)
project(apg)

add_subdirectory(ext)

include_directories(
    include
    "${CMAKE_CURRENT_SOURCE_DIR}/ext/aom"
    "${AOM_BINARY_DIR}"
)
add_library(apg STATIC
    include/apg.h
    src/apg.c
)
target_link_libraries(apg aom)

option(APG_BUILD_EXAMPLES "Build APG Examples." OFF)

if(APG_BUILD_EXAMPLES)
    add_executable(apg_example1 examples/apg_example1.c)
    target_link_libraries(apg_example1 apg)
endif()

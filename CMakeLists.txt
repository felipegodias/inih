cmake_minimum_required(VERSION 3.6)

project(inih)

option(INIH_BUILD_TESTS "Build tests" OFF)
option(INIH_BUILD_EXAMPLES "Build examples" OFF)

add_library(inih STATIC src/ini.c src/INIReader.cpp)

target_include_directories(inih PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
)

IF(INIH_BUILD_TESTS)
    add_subdirectory(tests)
endif(INIH_BUILD_TESTS)

if(INIH_BUILD_EXAMPLES)
    add_subdirectory(examples)
endif(INIH_BUILD_EXAMPLES)

unset(INIH_BUILD_TESTS CACHE)
unset(INIH_BUILD_EXAMPLES CACHE)
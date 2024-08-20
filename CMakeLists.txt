cmake_minimum_required (VERSION 3.20)
project (testsum)

#version number
set (testsum_VERSION_MAJOR 1)
set (testsum_VERSION_MINOR 0)

#include the subdirectory containing our libs
add_subdirectory(module)
include_directories(module)

#indicate the entry point for the executable
add_executable (testsum module test.cpp)

# Indicate which libraries to include during the link process.
target_link_libraries (testsum module)


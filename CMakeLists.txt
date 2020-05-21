cmake_minimum_required(VERSION 3.1.0)

set(CPP_STANDARD "14" CACHE STRING "Flag to upgrade the C++ standard used. The default is 14.")

project(hello CXX)

# Doxygen
include(cmake/Doxygen.cmake)
enable_doxygen()

# Allow for static analysis options
include(cmake/StaticAnalyzers.cmake)

add_subdirectory(src)

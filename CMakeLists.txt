cmake_minimum_required(VERSION 3.1.0)

project(hello CXX)

# Doxygen
include(cmake/Doxygen.cmake)
enable_doxygen()

# Allow for static analysis options
include(cmake/StaticAnalyzers.cmake)

add_subdirectory(src)

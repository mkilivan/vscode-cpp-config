cmake_minimum_required(VERSION 3.1.0)

project(hello CXX)

# Allow for static analysis options
include(cmake/StaticAnalyzers.cmake)

add_subdirectory(src)
add_subdirectory(docs)

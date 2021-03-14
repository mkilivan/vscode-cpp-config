cmake_minimum_required(VERSION 3.9)

project(hello CXX)

# Allow for static analysis options
include(cmake/StaticAnalyzers.cmake)

add_subdirectory(src)
add_subdirectory(docs)

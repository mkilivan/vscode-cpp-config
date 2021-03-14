set(CPP_STANDARD "14" CACHE STRING "Flag to upgrade the C++ standard used. The default is 14.")

include_directories("${PROJECT_SOURCE_DIR}")

add_executable(hello main.cpp)
set_property(TARGET hello PROPERTY CXX_STANDARD ${CPP_STANDARD})

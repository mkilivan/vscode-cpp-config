include_directories("${PROJECT_SOURCE_DIR}")

add_executable(hello main.cpp)
set_property(TARGET hello PROPERTY CXX_STANDARD ${CPP_STANDARD})

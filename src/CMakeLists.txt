include_directories("${PROJECT_SOURCE_DIR}")

file(GLOB sources "*.cpp")

add_executable(hello ${sources})
set_property(TARGET hello PROPERTY CXX_STANDARD ${CPP_STANDARD})
target_compile_options(hello PRIVATE -Werror -Wall -Wextra)

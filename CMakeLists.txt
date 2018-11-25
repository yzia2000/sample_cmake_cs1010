cmake_minimum_required( VERSION 3.0 )

project(sample)

add_compile_options( -g -Wall -Wextra -Wpedantic -Wdocumentation )

set( CMAKE_RUNTIME_OUTPUT_DIRECTORY ~/sample/bin)

set( CMAKE_EXPORT_COMPILE_COMMANDS ON )

include_directories( ~/libcs1010/include )

link_directories( ~/libcs1010/lib )

add_executable(
  test
  src/test.c
)



target_link_libraries( test m cs1010 )

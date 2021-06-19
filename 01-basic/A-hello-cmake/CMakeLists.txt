# Set the minimum version of CMake that can be used
# To find the cmake version run
# $ cmake --version
cmake_minimum_required(VERSION 3.5)

# Set the project name
project (hello_cmake)

# cmake --help-command message | less
message(TRACE "TRACE Found CFLAGS $ENV{CFLAGS}")
message(DEBUG "DEBUG Found CFLAGS $ENV{CFLAGS}")
# Not shown in "cmake ."
# cmake --log-level=DEBUG . or cmake --log-level=TRACE .
message(VERBOSE "VERBOSE Found CFLAGS $ENV{CFLAGS}")
message(NOTICE "NOTICE Found CFLAGS $ENV{CFLAGS}")
message("Found CFLAGS $ENV{CFLAGS}") # NOTICE is same to (none)
message(DEPRECATION "DEPRECATION Found CFLAGS $ENV{CFLAGS}")
message(AUTHOR_WARNING "AUTHOR_WARNINGFound CFLAGS $ENV{CFLAGS}")
message(WARNING "WARNING Found CFLAGS $ENV{CFLAGS}")
message(SEND_ERROR "SEND_ERROR Found CFLAGS $ENV{CFLAGS}") # CMake Error, continue processing, but skip generation.
message(FATAL_ERROR "FATAL_ERROR Found CFLAGS $ENV{CFLAGS}") # CMake Error, stop processing and generation.

#[[
To see cmake internal execution, like 'set -x' in shell
cmake --debug-output .
cmake --trace . | less
#]]

# Add an executable
add_executable(hello_cmake main.cpp)

cmake_minimum_required(VERSION 3.0)
cmake_policy(SET CMP0048 NEW)
project(Hello 
        LANGUAGES C
        VERSION 0.1.0)

set(CMAKE_C_FLAGS "-Wall -Wextra -pedantic -std=c99")
set(CMAKE_C_FLAGS_DEBUG "-Werror -g -O0")
set(CMAKE_C_FLAGS_RELEASE "-DNDEBUG -O2")

if(NOT CMAKE_BUILD_TYPE)
  message("No build type specified - defaulting to Debug.")
endif()

add_executable(HelloWorld "${CMAKE_SOURCE_DIR}/src/hello.c")


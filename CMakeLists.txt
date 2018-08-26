cmake_minimum_required(VERSION 2.6)
project(riscv_asm)

set (CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/libs/)
set (CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/bin/)

include_directories(${CMAKE_CURRENT_SOURCE_DIR})
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/src)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FALGS} -Wall -O3 -std=c++17")
add_library(riscv_asm src/instruction_set.cpp src/helper.cpp src/assembler.cpp)

add_executable(demo main.cpp)
target_link_libraries(demo riscv_asm)

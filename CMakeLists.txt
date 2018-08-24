cmake_minimum_required(VERSION 2.6)
project(riscv_asm)

add_executable(riscv_asm main.cpp)

install(TARGETS riscv_asm RUNTIME DESTINATION bin)

cmake_minimum_required(VERSION 3.13)

include(pico_sdk_import.cmake)

project(test_project C CXX ASM)
set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)
pico_sdk_init()

add_executable(main
  main.c
)

pico_add_extra_outputs(main)

target_link_libraries(main pico_stdlib hardware_pwm)

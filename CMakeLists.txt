cmake_minimum_required(VERSION 3.12)

include(pico_sdk_import.cmake)

project(IMU-test)

pico_sdk_init()

add_executable(IMU
    IMU.c
)

target_link_libraries(IMU 
    pico_stdlib
    hardware_i2c
    
    )

pico_enable_stdio_usb(IMU 1) # from video
pico_enable_stdio_uart(IMU 0)

pico_add_extra_outputs(IMU)
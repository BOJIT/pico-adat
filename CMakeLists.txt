cmake_minimum_required(VERSION 3.13)

include(/home/pico-sdk/pico_sdk_init.cmake)

project(main)
set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)

# Initialise Pico-SDK
pico_sdk_init()

# Include CMake libraries here

include_directories(src)

# Add source files
add_executable(main
    # src/main.cpp
    src/main-hatach.c
    src/usb_descriptors.c
)

# Link in libraries/pico-sdk
target_link_libraries(main
    pico_stdlib
    tinyusb_device
    tinyusb_board
)

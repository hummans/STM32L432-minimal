# STM32L432-minimal

Minimal environment for STM32L432 (Nucleo-32 STML432) for Linux and gcc-arm-none-eabi.

Download/clone git content in to your working directory (i.e. ./MyWork)

## Install compiler

    apt-get install git cmake unzip
    apt-get install build-essential
    apt-get install gcc-arm-none-eabi gdb-arm-none-eabi
    apt-get install openocd
  
## Build programmer 

    git clone https://github.com/texane/stlink.git
    cd stlink
    make release
    cd build/Release
    make install
    
Check programmer, connect board to computer and run

    st-info --probe
  
## Download library

Fro www STM [STM32Cube MCU & MPU Packages](https://www.st.com/en/embedded-software/stm32cube-mcu-mpu-packages.html) download and unpack (after login) library for L4 family

    STM32Cube_FW_L4_V1.14.0.zip
    
Copy directories from library directory ./Drivers

    BSP
    CMSIS
    STM32L4xx_HAL_Driver
    
to ./MyWork/Drivers

## Compile library

In ./MyWork/Drivers run

    make
    
this create *libll.a*

## Compile project

Create project files (in ./src), edit *Makefile*  and add your files to variable SRCS

    SRCS = system_stm32l4xx.c main.c 
    
and  in ./MyWork run

    make
    
## Flash MCU

    make flash
    




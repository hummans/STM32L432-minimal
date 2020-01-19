# STM32L432-minimal

Minimal environment for STM32L432 for Linux and gcc-arm-none-eabi

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
  
## Download library

Fro www STM [STM32Cube MCU & MPU Packages](https://www.st.com/en/embedded-software/stm32cube-mcu-mpu-packages.html) download and unpack (after login) library for L4 family

    STM32Cube_FW_L4_V1.14.0.zip
    

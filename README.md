# OpenX05R-C-stm32-drivers
Drivers for OpenX05R-C + Core205R (STM32F205R) for GCC toolchain.

![](https://www.waveshare.com/w/thumb.php?f=Open205R-C-Standard_l.jpg&width=450)

Following drivers are implemeted:
* PLL Clocks (runs board 120MHz using 25MHz crystal)
* LED (GPIOB)
* printf via serial UART
* watchdog

TODO:
* ADC
* DAC

# Hardware

* WaveShare [Open205R-C](https://www.waveshare.com/wiki/Open205R-C) with [Core205R](https://www.waveshare.com/wiki/Core205R), which carries STM32F205R.
* ST-LINK V2 debugger/programmer ([example](https://www.amazon.de/ARCELI-ST-LINK-CN-Version-MCU-Mikrocontroller-Circuit-Debugger-Programmierer-Emulator/dp/B07RKVM7H8))
* Any USB-to-TTL (CP2102) to allow serial communication ([example](https://www.amazon.de/SODIAL-USB-TTL-Konverter-Modul-eingebautem-CP2102/dp/B008RF73CS)).

# Software

GCC ARM toolchain
```
sudo apt-get install gcc-arm-none-eabi
```

Install `stlink-tools` as described [here](https://github.com/stlink-org/stlink#installation). Ubuntu 16.04 and 18.04 users have to compile from source. Check if debugger is visible.
```
st-info --probe
```

# Build

Compile
```
make
```

Flash
```
make flash
```

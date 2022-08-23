# ESP32

## Device info
- AliExpress procuct page: [USB C ESP32-DevKitC](https://www.aliexpress.com/item/1005004268911484.html)
- [Photo win win](https://ae01.alicdn.com/kf/Sbe50b314ac8c40f3ae04073a03299fb4S/ESP32-Development-Board-TYPE-C-USB-CH340C-WiFi-Bluetooth-Ultra-Low-Power-Dual-Core-ESP32-DevKitC.jpg_Q90.jpg_.webp)
- [Photo other](https://ae01.alicdn.com/kf/S4771d935337141938995bc6d53fac7b0z.jpg).
- [Alternate buy](https://www.aliexpress.com/item/1005004491534008.html)  
- [Pinout & recommended pins](https://www.studiopieters.nl/esp32-pinout/)
### Product description:
```
Development board model: ESP32-DevKitC-32
Module model: ESP32-WROOM-32
Main control chip: ESP32-D0WDQ6-V3 dual-core 32bit MCU integrated WiFi, Bluetooth
```

## Getting started with Thonny
1) Install Thonny (flatpak version)
```
flatpak install flathub org.thonny.Thonny
```

2) Download [MicroPython firmware for ESP32](https://micropython.org/download/esp32/).  

3) Flash the image on the board:
- connect the board to the computer
- open Thonny. Go to `Tools` > `Options` > `Interpreter`
- select the interpreter (`MicroPython(ESP32)`) and the port and click `Install or update firmware`
- on the screen that opens select the port (same as previous screen), click `Browse` to select the .bin downloaded file, for `Flash mode` select `From image file (keep)`, select `Erase flash before installing`, click `Install`

Get port
```
dmesg | grep ttyUSB
```

Query port
```
esptool.py --port /dev/ttyUSB0 flash_id
```

Erase flash
```
esptool.py --port /dev/ttyUSB0 erase_flash
```

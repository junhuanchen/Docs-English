# product description

![](https://img.shields.io/badge/open%20source-bananpi-brightgreen.svg)
![](https://img.shields.io/badge/support-webduino-blue.svg)

![](https://webduino.com.cn/site/img/tutorials/en_us/detail-03.gif)

This product is designed with ESP-WROOM-32 (ESP32) module as the core, with 40nm process, using Tensilica LX6 dual-core 32-bit processor, frequency up to 240 MHz, with 32 I/O pins, supporting 2.4G Wi -Fi, Bluetooth 4.0 and above, with 448KB ROM and 520 KB SRAM memory capacity, processing speed of 600 DMIPS, with ultra-low power consumption of 40nm process, is the highest performance, most stable and most versatile on the market. One of the products.

It is also known as Webduino Bit, which is the latest development board of Webduino. In addition to the original functions (Wi-Fi control, multi-device parallel, work together, etc.), it also has many interesting components and sensors built in.

At the same time, the bpi:bit open source community will continue to be compatible with most of the micro:bit accessories and usage.

## Appearance introduction

![](readme/Interface_CN.jpg)

The Webduino Bit development board is 5 cm wide and 5 cm wide and weighs about 10 to 12 grams. In addition to the 20-pin "golden finger interface" below, it also has a matrix of 25 full-color LED lights, two photoresistors and two push button switches. , a temperature sensing resistor, a buzzer and a nine-axis sensor (three-axis acceleration, three-axis gyroscope and three-axis magnetic compass), the pin configuration is as follows:

- Full Color LED Matrix: A10 (GPIO 4)
- Photosensitive sensor: upper left A0 ( GPIO 36 ), upper right A3 ( GPIO 39 )
- Push button switch: Button A P5 ( GPIO 35 ), button B P11 ( GPIO 27 )
- Temperature sensor: A6 ( GPIO 34 )
- Buzzer: P0 ( GPIO 25 )
- Nine-axis sensor MPU-9250: P20 (GPIO 21), P19 (GPIO 22)

## Extension pin

![](readme/goldfinger.jpg)

![](readme/pin-define.jpg)

### LED number

The board is soldered with 25 (numbered 0 ~ 24) 16 million color full-color LEDs (WS2812) in a 5 * 5 arrangement. All LED controls can be controlled using only one pin (GPIO 4).

![](readme/product.jpg)

The front panel LEDs are arranged in the following order (5 * 5)

![](readme/table.png)

(Put the front of the board toward you, and combine the gold finger of the chassis to know its position)

## Version difference

The board is divided into multiple versions, such as version 1.2 and version 1.4. The version number is marked on the lower right corner of the back of the board.

![](readme/version.jpg)

## Product Support

### [Install Driver] (driver.md)

### Webduino

- [Webduino Basic Teaching] (https://webduino.com.cn/site/zh_cn/tutorials.html)
- [Webduino Player Guide] (https://github.com/BPI-STEAM/BPI-BIT-WebDuino)
- [Webduino Chinese Community] (https://forum.banana-pi.org.cn/c/bpi-bit/webduino)

### MicroPython

- [MicroPython Player Guide] (https://github.com/BPI-STEAM/BPI-BIT-MicroPython)
- [MicroPython sample code] (https://github.com/BPI-STEAM/BPI-BIT-Samples)
- [MicroPython Chinese Community] (https://forum.banana-pi.org.cn/c/bpi-bit/micropython)

### Arduino

- [Arduino Player Guide] (https://github.com/BPI-STEAM/BPI-BIT-Arduino)

## hardware design

### Pin occupation

![](readme/extern.png)

### Appearance data

![](readme/bot.png)

![](readme/top.png)

### Hardware Information

- [BPI-WEBDUINO-BIT-V1_2] (https://github.com/BPI-STEAM/BPI-BIT-Hardware/tree/master/docs/BPI-WEBDUINO-BIT-V1_2.pdf)

- [BPI-WEBDUINO-BIT-V1_4] (https://github.com/BPI-STEAM/BPI-BIT-Hardware/tree/master/docs/BPI-WEBDUINO-BIT-V1_4.pdf)

- [Buzzer-SS-S050020Z-120] (https://github.com/BPI-STEAM/BPI-BIT-Hardware/tree/master/docs/Buzzer-SS-S050020Z-120.pdf)

- [CH340DS1-ch] (https://github.com/BPI-STEAM/BPI-BIT-Hardware/tree/master/docs/CH340DS1-ch.pdf)

- [CH340DS1-en] (https://github.com/BPI-STEAM/BPI-BIT-Hardware/tree/master/docs/CH340DS1-en.pdf)

- [esp32_hardware_design_guidelines_en](https://github.com/BPI-STEAM/BPI-BIT-Hardware/tree/master/docs/esp32_hardware_design_guidelines_en.pdf)

- [ESP32-datesheet_english](https://github.com/BPI-STEAM/BPI-BIT-Hardware/tree/master/docs/ESP32-datesheet_english.pdf)

- [esp-wroom-32_datasheet_cn](https://github.com/BPI-STEAM/BPI-BIT-Hardware/tree/master/docs/esp-wroom-32_datasheet_en.pdf)

- [LightSensor-PTSMD021-0805] (https://github.com/BPI-STEAM/BPI-BIT-Hardware/tree/master/docs/LightSensor-PTSMD021-0805.pdf)

- [LM1117] (https://github.com/BPI-STEAM/BPI-BIT-Hardware/tree/master/docs/LM1117.pdf)

- [MPU-9250 Datasheet-v1.1-ch] (https://github.com/BPI-STEAM/BPI-BIT-Hardware/tree/master/docs/MPU-9250%20Datasheet-v1.1-ch. Pdf)

- [MPU-9250 Datasheet-v1.1-en] (https://github.com/BPI-STEAM/BPI-BIT-Hardware/tree/master/docs/MPU-9250%20Datasheet-v1.1-en. Pdf)

- [MPU-9250 Register Map-v1.6] (https://github.com/BPI-STEAM/BPI-BIT-Hardware/tree/master/docs/MPU-9250%20Register%20Map-v1.6.pdf )

- [NTC-0805-103F-3950F] (https://github.com/BPI-STEAM/BPI-BIT-Hardware/tree/master/docs/NTC-0805-103F-3950F.pdf)

- [SY7208] (https://github.com/BPI-STEAM/BPI-BIT-Hardware/tree/master/docs/SY7208.pdf)

- [WS2812B] (https://github.com/BPI-STEAM/BPI-BIT-Hardware/tree/master/docs/WS2812B.pdf)

- [DS-000189-ICM-20948-v1.3] (https://github.com/BPI-STEAM/BPI-BIT-Hardware/tree/master/docs/DS-000189-ICM-20948-v1.3 .pdf)

## Related Websites

- [Official Chinese Community] (https://forum.banana-pi.org.cn/c/bpi-bit)
- [Official English Community] (http://forum.banana-pi.org/c/bpi-bit)
- [Webduino Domestic Edition] (https://webduino.com.cn/site/)
- [Webduino International Edition] (https://webduino.io/)
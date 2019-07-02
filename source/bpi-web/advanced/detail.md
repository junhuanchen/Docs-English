# Webduino Bit Detailed Specifications

Webduino Bit is the latest development board of Webduino. In addition to the original functions (Wi-Fi control, multi-device serial connection, collaborative operation, etc.), many new components and sensors are built in. Webduino Bit adopts ESP32 module. Built-in 2.4G Wi-Fi and Bluetooth, with 448KB ROM and 520 KB SRAM memory capacity, processing speed of 600 DMIPS, with ultra-low power consumption of 40nm process, is the highest performance, most stable and most versatile on the market. One of the products.

> To control the Webduino Bit, be sure to read [Webduino Bit] (setting.html#_top) for related network settings.

![](img/tutorials/zh_cn/detail-03.gif)

## Default component pin introduction

The Webduino Bit development board is 5 cm wide and 5 cm wide and weighs about 10~12 grams. In addition to the 20-pin "Golden Finger Interface" below, it has a built-in matrix of 25 full-color LED lights, two photoresistors and two buttons. Switch, a temperature sensing resistor, a buzzer and a nine-axis sensor (three-axis acceleration, three-axis gyroscope and three-axis magnetic compass), the pin configuration is as follows:

- * Full Color LED Matrix*: A10 ( GPIO 4 )
- * Photosensitive sensor*: upper left A0 ( GPIO 36 ), upper right A3 ( GPIO 39 )
- * Push button switch *: Button A P5 ( GPIO 35 ), button B P11 ( GPIO 27 )
- * Temperature sensor *: A6 ( GPIO 34 )
- *Buzzer*: P0 ( GPIO 25 )
- *Nine-axis sensor MPU-9250*: P20 (GPIO 21), P19 (GPIO 22)

![](img/tutorials/zh_cn/detail-05.jpg)

![](img/tutorials/zh_cn/detail-04.jpg)

## Appearance introduction

![](img/tutorials/zh_cn/detail-01.jpg)
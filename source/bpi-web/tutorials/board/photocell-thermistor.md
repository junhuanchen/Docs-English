#检测光与温度

The development board has two built-in photoresistors and a temperature-sensitive resistor. The photoresistor can detect the lumen value of the ambient light. The temperature-sensitive resistor can detect the temperature change of two decimal places, and the light and temperature are detected. It is easy to make field monitoring related environment applications.

## Building block list

The detection light can detect the brightness changes in the upper left and upper right respectively. The unit of detection is lumens, the value range is an integer from 0 to 1000, the unit of temperature detection is degree C, and the value can be two decimal places.

![Detect Light & Temperature](../images/zh-tw/docs/webbit/board/photocell-thermistor-01.jpg)

> * Detecting light and temperature building blocks must be matched with "development board" building blocks*, select the simulator, after execution, you can use the mouse to drag the light bulb or flame of the simulator, select USB, and then control the physical development board through USB connection. , select Wi-Fi to specify Device ID control via Wi-Fi.
> - USB control mode is limited to "Installation Editor", please refer to [Editor] (../index.html#software)
> - Wi-Fi mode requires a development board to connect to Wi-Fi, please refer to [Hardware Development Board (Initial Settings)] (../info/setup.html)

![Detect Light & Temperature](../images/zh-tw/docs/webbit/board/photocell-thermistor-08.jpg)


## Detecting light

The "Detect Light" building block will only be detected once, and it can be continuously detected with repeated loops.

![Detect Light & Temperature](../images/zh-tw/docs/webbit/board/photocell-thermistor-02.jpg)

After the execution, if the simulator is used, the “one light bulb” pattern* will appear in the screen, and the light bulb can be simulated by pulling the light bulb close to the screen. If the physical development board is used, the light can be used to observe the photosensitive resistor. Light changes.

![Detect Light & Temperature](../images/zh-tw/docs/webbit/board/photocell-thermistor-03.gif)

After understanding the principle of light detection, if you use simple logic judgment, you can make the effect of the night light. In the example of the following figure, as long as any one of the left or right photoresistors detects brightness greater than or equal to 600 lumens, Turn off the light, otherwise the left and right sides will light up as long as the value detected at the same time is less than 600 lumens.

![Detect Light & Temperature](../images/zh-tw/docs/webbit/board/photocell-thermistor-04.gif)

## Detecting temperature

The "Detected Temperature" building block will only be detected once, and it can be continuously detected with repeated loops.

![Detect Light & Temperature](../images/zh-tw/docs/webbit/board/photocell-thermistor-05.jpg)

After the execution, if the simulator is used, the “one flame” pattern* will appear in the screen, and the temperature change can be simulated by pulling the bulb close to the thermistor in the screen. If the physical development board is used, the thermal can be pressed with a finger. The temperature change can be observed by resistance or by blowing the nozzle against the thermistor.

![Detect Light & Temperature](../images/zh-tw/docs/webbit/board/photocell-thermistor-06.gif)

After understanding the principle of temperature detection, if you use simple logic judgment, you can make the effect of reflecting the temperature with color. When the temperature is greater than or equal to 50 degrees, it will be red, and if it is less than 40 degrees, it will be blue.

![Detect Light & Temperature](../images/zh-tw/docs/webbit/board/photocell-thermistor-07.gif)
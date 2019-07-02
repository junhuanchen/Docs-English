#检测温度

The Webduino Bit has a built-in temperature-sensitive resistor. The temperature-sensitive resistor is similar to the principle of a photoresistor. The analog signal is used to feedback the temperature value and detect the temperature change in real time, which further enables the application of intelligent home monitoring.

## Basic operation (display temperature value)

Open [Webduino Blockly Bit Experience Edition] (https://webduino.com.cn/link.html?lang=zh-hans&type=blockly), put * development board building blocks* in the editing area, and use "* emulation by default. "*", connect to the "*Virtual Bit Development Board*" on the screen, and the default Device ID is "*1234*".

> Development board related building blocks, under the "* development board*" directory.

![](img/tutorials/zh_cn/rgbmatrix-01.jpg)

If you are using "*Ent Bit Development Board*", select "*Wi-Fi*" from the drop-down menu and fill in the Device ID of the development board in the back field.

![](img/tutorials/zh_cn/rgbmatrix-02.jpg)

Put the "* set thermistor as the thermistor*" in the development board.

> Thermistor related building blocks are in the "* Thermistor*" catalog.

![](img/tutorials/zh_cn/temperature-01.jpg)

Click the menu at the top right to open the interactive area of ​​the web page. Select the "*Display Text*" from the drop-down menu. The corresponding building block function will also appear on the left menu.

![](img/tutorials/zh_cn/temperature-02.jpg)

Put the blocks that thermistor starts to detect, and display the detected temperature in the interactive area of ​​the webpage while detecting.

![](img/tutorials/zh_cn/temperature-03.jpg)

Click on the red button at the top right to execute. You will see a light bulb and a flame pattern appearing below the virtual Bit development board. Just drag the "flame pattern" near the thermistor with your mouse and you will see the temperature appear on the web page. Using the physical Bit development board, you can use your finger to press the thermistor or blow it with your mouth to observe changes in temperature values.

> Example link: [Webduino Bit Detection Temperature] (https://webduino.com.cn/link.html?lang=zh-hans&type=example&blockly=temperature01)

![](img/tutorials/zh_cn/temperature-04.gif)

Because the thermistor is an analog signal, the values ​​presented will have many digits below the decimal point. We can display the value of two decimal places by rounding the bricks.

> The blocks that are rounded to the decimal point are in the "*Advanced Functions > Numerical Conversion*" directory.

![](img/tutorials/zh_cn/temperature-05.jpg)

## Component Interaction (Full color dot matrix color display temperature)

In the [5x5 Full Color LED Dot Matrix] (rgbmatrix.html) tutorial, there is a description of the usage of the full-color dot matrix. Next, we will show how to change the temperature through different colors. The higher the temperature, the more red the color. The lower the temperature, the more blue the color. At the beginning, in addition to the temperature-sensitive resistors, the blocks with the matrix set to the full-color dot matrix are placed.

![](img/tutorials/zh_cn/temperature-06.jpg)

Because you want to change the color, you will use the "red, green, blue" color blocks in the color catalog. Since the maximum value of the mixed color is 100 in the Blockly setting, the minimum value is 0, and the temperature will be set. The values ​​are limited to this range.

![](img/tutorials/zh_cn/temperature-07.jpg)

First, a variable t is used to indicate the detected temperature, and then it is logically judged: "* If t is greater than 100, then t is equal to 100. If t is less than 0, t is equal to 0*", and t can be limited to 0. Between 100, after completion, the value of t can also be displayed through the interactive area of ​​the webpage.

> The building blocks of the variables are in the "* variable *" directory, the logical building blocks are in the "*Basic Functions > Logic*" directory, and the digital building blocks are in the "*Basic Functions > Mathematical*" directory.

![](img/tutorials/zh_cn/temperature-08.jpg)

Put the building block of "Set the first color of the matrix", set the red to t, and the blue to 100-t, so that the higher the temperature, the more red, and the lower the temperature, the more blue.

> Mathematical addition and subtraction blocks are in the "*Basic Functions > Mathematical*" directory.

![](img/tutorials/zh_cn/temperature-09.jpg)

Click the red button at the top right to execute. To drag the "flame pattern" to the farther or away from the thermistor, you will see the first light of the full-color dot matrix, showing a red-blue change. If you are using a physical Bit development board. , you can use your finger to press the thermistor, or use your mouth to blow to observe the color change.

> Example link: [Webduino Bit full color dot matrix color display temperature 1] (https://webduino.com.cn/link.html?lang=zh-hans&type=example&blockly=temperature02)

![](img/tutorials/zh_cn/temperature-10.gif)

If you want to light up the 25 lights of the full-color dot matrix at a time, you can make the 25 lights together produce a red-blue color change depending on the temperature.

> Example link: [Webduino Bit full color dot matrix color display temperature 2] (https://webduino.com.cn/link.html?lang=zh-hans&type=example&blockly=temperature03)

![](img/tutorials/zh_cn/temperature-11.jpg)

![](img/tutorials/zh_cn/temperature-12.gif)
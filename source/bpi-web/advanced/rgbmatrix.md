# 5x5 Full Color LED Dot Matrix

The center of the Webduino Bit is embedded with a 5x5 dot matrix of 25 full-color LEDs. Each of the lights can be mixed with the three primary colors of red, green and blue. It can be displayed through various positions of lights and colors. Different pattern shapes.

## Basic operation

Open [Webduino Blockly Bit Experience Edition] (https://webduino.com.cn/link.html?lang=zh-hant&type=blockly), put * development board building blocks* in the editing area, and use "* emulation by default. "*", connect to the "*Virtual Bit Development Board*" on the screen, and the default Device ID is "*1234*".

> Development board related building blocks, under the "* development board*" directory.

![](img/tutorials/zh_cn/rgbmatrix-01.jpg)

If you are using "*Ent Bit Development Board*", select "*Wi-Fi*" from the drop-down menu and fill in the Device ID of the development board in the back field.

![](img/tutorials/zh_cn/rgbmatrix-02.jpg)

In the development board, the building block "* sets the matrix to be a full-color dot matrix*" is placed, and the blocks of "*set matrix color*" are placed below it.

> Full color dot matrix related building blocks in the "* Full color dot matrix*" directory.

![](img/tutorials/zh_cn/rgbmatrix-03.jpg)

First select the color with the mouse, click on the space below to fill in the color and draw the pattern, if you choose black, the light will not shine.

![](img/tutorials/zh_cn/rgbmatrix-04.jpg)

Click the red button on the top right to execute, you can see the virtual development board of the emulator, or your own physical development board to display the corresponding color and pattern.

> Example Answer: [Webduino Bit Full Color Dot Matrix Display Color] (https://webduino.com.cn/link.html?lang=zh-hans&type=example&blockly=rgbmatrix01)

![](img/tutorials/zh_cn/rgbmatrix-05.jpg)

## Web button interaction

Now that you have learned the basic application of the full-color dot matrix, you need to use the "Web button" of the "Webpage Interactive Area" to control the light number display, click the webpage interactive area button of the above menu, select the "* button behavior*" from the drop-down menu, and select After that, five buttons will appear on the screen, and the corresponding building block menu will appear on the left side.

![](img/tutorials/zh_cn/rgbmatrix-06.jpg)

Put the blocks of "*click button to execute*" on the screen, and set different buttons when setting click button 1 and click button 2 respectively. Clicking button 3 will close the full color point matrix.

![](img/tutorials/zh_cn/rgbmatrix-07.jpg)

Click the red button on the top right to execute, you can use the buttons in the interactive area of ​​the web page to control the virtual development board of the emulator, or display the corresponding color and pattern on your own physical development board.

> Example Answer: [Web Button Switch Webduino Bit Full Color Dot Matrix Pattern] (https://webduino.com.cn/link.html?lang=zh-hans&type=example&blockly=rgbmatrix02)

![](img/tutorials/zh_cn/rgbmatrix-08.gif)
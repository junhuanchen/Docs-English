#检测光

The Webduino Bit has a number of built-in sensors, one of which is a photoresistor. With the default two photoresistors, you can detect the intensity of light, even with the application of smart appliances or auto-detection.

## Basic operation (displaying light values)

Open [Webduino Blockly Bit Experience Edition] (https://webduino.com.cn/link.html?lang=zh-hans&type=blockly), put * development board building blocks* in the editing area, and use "* emulation by default. "*", connect to the "*Virtual Bit Development Board*" on the screen, and the default Device ID is "*1234*".

> Development board related building blocks, under the "* development board*" directory.

![](img/tutorials/zh_cn/rgbmatrix-01.jpg)

If you are using "*Ent Bit Development Board*", select "*Wi-Fi*" from the drop-down menu and fill in the Device ID of the development board in the back field.

![](img/tutorials/zh_cn/rgbmatrix-02.jpg)

Put two "* set photocell for the photoresistor*" in the development board. From the pull-down menu of the rear photoresistor, you can select the upper left or upper right. After the selection is complete, click the drop-down menu for setting the block in front. Use "*new variable*" to name the variables left and right respectively.

> Photosensitive resistor related building blocks in the "*Photosensitive Resistor*" catalog.

![](img/tutorials/zh_cn/photocell-01.jpg)

Click the menu at the top right to open the interactive area of ​​the web page. Select the "*Display Text*" from the drop-down menu. The corresponding building block function will also appear on the left menu.

![](img/tutorials/zh_cn/photocell-02.jpg)

Because there are two photoresistors, if you want to detect them at the same time, you need to put the blocks detected by left and right respectively.

![](img/tutorials/zh_cn/photocell-03.jpg)

In order to display the values ​​of the two photoresistors at the same time, you must use the building blocks of the "variable" to load the ray value. Here, the L variable is loaded with the value detected by left, and the R variable is loaded with the value detected by right.

> Variable related building blocks are in the "* variable*" directory.

![](img/tutorials/zh_cn/photocell-04.jpg)

Use the "display" block that displays the text, and the block with "*Create string*", display the values ​​of the R and L variables in the interactive area of ​​the webpage, and click "*Blue pinion*" to create the string building block. You can add a combination of gaps, you can put a comma as a separator.

> Create string related blocks in the "*Basic Functions > Text*" directory.

![](img/tutorials/zh_cn/photocell-05.jpg)

Click on the red button at the top right to execute. You will see a light bulb and a flame pattern appearing below the virtual Bit development board. At this time, just drag the light bulb near the photoresistor with the mouse, you will see different values, if you are using the physical Bit development board. , you can use the light to illuminate the photoresistor, or block the photoresistor by hand to observe the change in the value of the light.

> Example link: [Webduino Bit Photosensitive Resistor Detecting Light] (https://webduino.com.cn/link.html?lang=zh-hans&type=example&blockly=photocell01)

![](img/tutorials/zh_cn/photocell-06.gif)

## Logic interaction (lighting page bulb)

After you have been able to obtain the ray value from the photoresistor, you can then use a logical judgment to implement a virtual night light function. Because the night light usually only needs one photoresistor, first use the upper left photoresistor, name setting. For left.

![](img/tutorials/zh_cn/photocell-07.jpg)

Open the webpage interactive area, select “*click bulb*” from the drop-down menu, and the corresponding building block menu will appear on the left side.

![](img/tutorials/zh_cn/photocell-08.jpg)

Put the building block of "*Logic Judgment*" and judge that the light value is less than 0.7, it will light the bulb in the interactive area. If the light is greater than 0.7, let the light bulb go out. If you want to add logic judgment, you can click on the logic block. *Blue pinion*" added.

> Logic-related building blocks in the "*Basic Functions > Logic*" directory, and the number-related building blocks are in the "*Basic Functions > Mathematical*" directory.

![](img/tutorials/zh_cn/photocell-09.jpg)

Click the red button on the upper right side to execute. A light bulb and a flame pattern appear below the virtual Bit development board. Use the mouse to drag the light bulb near the upper left of the light bulb. You will see the light bulb in the interactive area go out, and the light bulb will light up if you leave. If you use the physical Bit development board, you can use the light to illuminate the photoresistor, or block the photoresistor by hand to observe the virtual light bulb changes.

> Example link: [Webduino Bit detects light to light the webpage bulb] (https://webduino.com.cn/link.html?lang=zh-hans&type=example&blockly=photocell02)

![](img/tutorials/zh_cn/photocell-10.gif)
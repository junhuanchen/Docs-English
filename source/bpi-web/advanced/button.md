# power switch button

The switch is commonly used in daily life. On the left and right sides of the front of the Webduino Bit development board, two button switches are defaulted. Through the control of the switch, we can more effectively realize the situation of crop networking, and even create a real game remote control or smart home appliance. Applications.

## Basic operation

Open [Webduino Blockly Bit Experience Edition] (https://webduino.com.cn/link.html?lang=zh-hans&type=blockly), put * development board building blocks* in the editing area, and use "* emulation by default. "*", connect to the "*Virtual Bit Development Board*" on the screen, and the default Device ID is "*1234*".

> Development board related building blocks, under the "* development board*" directory.

![](img/tutorials/zh_cn/rgbmatrix-01.jpg)

If you are using "*Ent Bit Development Board*", select "*Wi-Fi*" from the drop-down menu and fill in the Device ID of the development board in the back field.

![](img/tutorials/zh_cn/rgbmatrix-02.jpg)

Put two "* set button as button switch*" blocks in the development board. From the pull-down menu of the rear button switch, you can select button A or button B. After the selection is complete, click to set the pull-down of the building block in front. Menu, use "* new variable *" to name the variables btnA and btnB respectively.

> The button switch related blocks are in the "* button switch*" directory.

![](img/tutorials/zh_cn/button-01.jpg)

Click the menu at the top right to open the interactive area of ​​the web page. Select the "*Display Text*" from the drop-down menu. The corresponding building block function will also appear on the left menu.

![](img/tutorials/zh_cn/button-02.jpg)

Put the "When the button is pressed" block, select the corresponding btnA or btnB through the drop-down menu, and set the "press A" in the interactive area of ​​the webpage when btnA is pressed. When btnB is pressed, “Press B” is displayed.

> Display blocks are displayed in the "*Display Text*" directory, and the text blocks are in the "*Basic Functions > Text*" directory.

![](img/tutorials/zh_cn/button-03.jpg)

Click the red button on the top right to execute, use the mouse to click the button switch of the virtual development board, or press the button switch of the physical development board, you will see different text in the interactive area of ​​the webpage.

> Example Answer: [Click the Webduino Bit button switch to display different text] (https://webduino.com.cn/link.html?lang=zh-hans&type=example&blockly=button01)

![](img/tutorials/zh_cn/button-04.gif)

## Button Switch Controls Full Color Dot Matrix

In addition to interacting with webpage elements, the button switch can also directly manipulate other components on the Bit development board. Then we let the button switch interact with the full-color dot matrix, and when we click different buttons, we will present different patterns because we want to The dot matrix interacts, so put a block of a full color dot matrix in the development board, the * name is set to matrix*, and the blocks of the two button switches are placed, and the * names are set to btnA and btnB*, respectively.

![](img/tutorials/zh_cn/button-05.jpg)

Put in the blocks that are pressed when the button is pressed, and when btnA and btnB are pressed respectively, the full-color dot matrix will display different patterns.

![](img/tutorials/zh_cn/button-06.jpg)

Click the red button on the top right to execute, use the mouse to click the button switch of the virtual development board, or press the button switch of your own physical development board, you will see a different pattern of the full color dot matrix.

> Example Answer: [Webduino Bit Button Switch Controls Full Color Dot Matrix] (https://webduino.com.cn/link.html?lang=zh-hans&type=example&blockly=button02)

![](img/tutorials/zh_cn/button-07.gif)
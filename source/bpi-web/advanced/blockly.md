# Meet Webduino Blockly Bit

Webduino Blockly Bit Experience Edition is an image editing tool developed by Webduino. It is designed by Google Blockly. It provides virtual and real integration, program building blocks and remote control environment. It can experience the use situation and operation experience of the Internet of Things. A variety of ideas.

Open: [Webduino Blockly Bit Experience Edition] (https://webduino.com.cn/link.html?lang=zh-hans&type=blockly)

> For more Webduino Blockly functions please refer to: [Webduino Blockly Basic Operations] (https://tutorials.webduino.io/zh-tw/docs/basic/blockly/blockly-tutorial-01.html), [Webduino Blockly Special Features ](https://tutorials.webduino.io/zh-tw/docs/basic/blockly/blockly-tutorial-02.html), [Link multiple development boards] (https://tutorials.webduino.io/ Zh-tw/docs/basic/blockly/multi-board.html).

## Tool Interface Description

Webduino Blockly's interface is mainly divided into three parts. The first part is the menu bar on the left and the top left. There are two tabs that switch between "program block" and "JavaScript". The top right is "Generate QRCode". , "View Device Status", "Web Interactive Test", "Webduino Bit Emulator", "Delete All Building Blocks", "Save and Generate Links" and "Execute".

![](img/tutorials/zh_cn/blockly-01.jpg)

## Control Webduino Bit Development Board

Ebduino Blockly Bit can now be controlled by Wi-Fi and WebSocket. If there is no physical development board, it can also be controlled by "emulator".

![](img/tutorials/zh_cn/blockly-02.jpg)

Note that to use WebSocket, the **URL must be http and the port number must be 8080**.

![](img/tutorials/zh_cn/blockly-08.jpg)

## Storage file

After we have finished editing, you can click the "Link" icon at the top right of Webduino Blockly, which will generate a set of link URLs. This set of link URLs represents the current picture. Just write this set of URLs to the browser's "My Most In the "love" or "bookmark", the next time you open it, the same picture will appear.

![](img/tutorials/zh_cn/blockly-07.jpg)

## Online Webduino Bit Emulator

After opening the Webduino Blockly Bit experience version, the emulator will be automatically opened on the screen. The emulator contains a virtual Bit development board. After the program is executed, the Webduino logo on the development board will turn green, and the light bulb and flame will appear below. Element, if you use "photoresist", you can interact through the bulb element. If you use "temperature sensitive resistor", you can interact through the flame element.

![](img/tutorials/zh_cn/blockly-03.jpg)

## Web interaction area

Webduino Blockly embeds webpage templates, clicks the webpage interactive test button, you can select these webpage templates from the drop-down menu, and manipulate the IoT devices through these webpages. The webpage templates include: display text, click bulb, control image, color adjustment , button behavior, slave operation, Youtube, image tracking, remote control, drawing charts.

![](img/tutorials/zh_cn/blockly-04.jpg)

## Perfect support for mobile phones

Webduino Blockly has built-in QRCode button. Clicking this button will generate QRCode. By scanning with mobile device, the current "Webpage Interactive Area" web page can be displayed in the mobile phone's browser.

![](img/tutorials/zh_cn/blockly-05.jpg)

![](img/tutorials/zh_cn/blockly-06.jpg)
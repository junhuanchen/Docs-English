#编辑器(Operation interface)

The editor is Webduino's latest program editing & learning software. In addition to the Webduino Blockly-based operation mode, it also greatly simplifies the step-by-step process of the operation. Even the virtual development board and the small monster interactive stage are added, whether it is a big friend or a child. Quick and easy to get started with Web: Bit.

> - Web version: [https://webbit.webduino.io](https://webbit.webduino.io#_blank)
> - Installation version download: [WebBitSetup.zip] (http://webduinoio.github.io/samples/content/bit-download/WebBitSetup.zip#_blank)

## Operation interface list

The editor's interface is divided into the following blocks:

- ** Main Function Menu**: Contains file storage and opening, example and teaching, delete all building blocks, more functions and execute buttons.
- **Building block/code switching**: Convert the written program to standard Javascript to make the learning program easier.
- **List of building blocks**: Contains basic functions, small monster interaction, development board control and IoT expansion...
- **Building block editing area**: Perform a logical combination of building blocks to produce a variety of different contextual applications.
- **Development Board Simulator**: Contains a virtual development board that simulates the condition and application of the actual development board.
- **Little Monster Interactive Stage**: A small monster with four different styling colors that can be used to set related movements and interactive situations.
- **Zoom button**: Fast enough to zoom in and out of the wood or remove blocks.
- **Screen folding button**: Quickly fold the development board simulator and the small monster interaction area to enlarge or reduce the building block editing area.

![editor (operation interface)](../images/zh-tw/docs/webbit/info/interface-01.jpg)

## What is the program building block?

For those who are in contact with the first time, it is not clear about the origin of the "program block". The "building block" is an English word translated from "block". Its operation is similar to the concept of "assembled building blocks" or "puzzles". By stacking and combining with each other, it is possible to judge different logics or implement corresponding actions according to a specified arrangement order.

![editor (operation interface)](../images/zh-tw/docs/webbit/info/interface-02.gif)

The editor is an editing tool developed by Google's graphical program editing tool Blockly. Each building block has its own functions and uses. If you want to know how to use the building block, you can use the mouse in the specified building block. Press the right button *" to open the function list of the building block. Click "Teaching" to read the teaching file of the building block. If the building block has "Gadget", you can click the gadget to open more advanced functions.

![editor (operation interface)](../images/zh-tw/docs/webbit/info/interface-03.jpg)

## Cloud deployment

The cloud deployment function can help us to deploy the edited program blocks to the Webduino cloud server, so that we can continue to execute the corresponding program actions when the computer is off* (* still need to keep the development board normal) Internet connection*), as long as the program board contains a Wi-Fi connection development board**, you can use the cloud deployment features.

> Note that after the cloud deployment is successful, it will stop under the following two conditions:
> - * First, the development board network is disconnected for more than 20 minutes. *
> - * Second, re-cloud deployment, or click the editor's "Execute" button. *

![editor (operation interface)](../images/zh-tw/docs/webbit/info/interface-06.jpg)

## Web version, installed version of the main function menu differences

The main function menu at the top right contains the main functions of the editor, but the menus for the "Web Edition" and "Installed" editors are slightly different. In the web version, you can use "File > Share Link" and the installation version will not work. Share the link. It can help us quickly archive and generate a "URL". You can open the file the next time you open the URL, because the installation version can't open the URL, so you can't use this option.

![editor (operation interface)](../images/zh-tw/docs/webbit/info/interface-04.jpg)

In the "More" section of the main menu of the webpage, the option of "Download and install" is also included. After clicking, the compressed version of the installation version will be downloaded, and the installation version can be used after decompressing the installation. (The current installation editor only supports Windows)

![editor (operation interface)](../images/zh-tw/docs/webbit/info/interface-05.jpg)

## Program Building Tips

### Tips 1, multi-line and single-line input

If the program building block is too long, we can use the mouse to right click on the building block. If the building block supports multiple lines of input, you can click "*Multiple Line Input*" to change the building block from a single line to multiple lines, which is more convenient for reading and editing.

![editor (operation interface)](../images/zh-tw/docs/webbit/info/interface-07.gif)

### Tips 2, organize the blocks

When implementing the program building blocks, you will often encounter the situation that the building blocks are scattered on the screen. In this case, right click on the editing area and select “*Finished Building Blocks*” to arrange the blocks neatly.

![editor (operation interface)](../images/zh-tw/docs/webbit/info/interface-08.gif)
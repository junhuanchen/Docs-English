# Development board

Three ways to control the development board are provided, namely "emulator", "USB" and "Wi-Fi". The simulator can learn without hardware. USB can be transmitted without network. USB connection control, and Wi-Fi can be wireless remote control, through three different control modes, regardless of the situation can be controlled as desired.

![Development Board](../images/zh-tw/docs/webbit/board/board-01.jpg)

## How to use

Select the "simulator" from the drop-down menu to indicate that * use the "virtual development board"* on the right side. All the components in the development board will point to the virtual development board on the right side. For example, draw a pattern. After execution, the virtual development board will Display graphics.

![Development Board](../images/zh-tw/docs/webbit/board/board-02.jpg)

Select "USB" from the drop-down menu to indicate that * "USB cable" is used to connect to the "hardware development board"*, ** must use the "installation editor" operation**, for example, draw a pattern, after execution, development via USB connection The board will display the graph.

> Installer Editor please refer to: [Editor (Installation Toolbar)] (../info/toolbar.html)

![Development Board](../images/zh-tw/docs/webbit/board/board-03.jpg)

Select "Wi-Fi" from the drop-down menu to indicate that * "Wi-Fi" is used to connect to the "hardware development board"*, that is, by controlling the Device ID of each development board**, as long as the Device ID is known, regardless of development Where the board is located, it can be controlled remotely. (With the mobile power supply, there will be more "distance control" or "wireless control" feeling)

> Development Board Device ID Please refer to: [Hardware Development Board (Initialization Settings)] (../info/setup.html)

![Development Board](../images/zh-tw/docs/webbit/board/board-04.jpg)


## Control multiple development boards

The editor can * control multiple development boards at the same time*, only need to put the development board in the editing screen, specify the control mode of the development board, and after execution, you will see all the development boards change at the same time. The example below is the same. In an editing screen, let a simulator development board and two Wi-Fi development boards simultaneously present a flower pattern.

> Multiple development boards* include up to one "simulator" development board and one "USB" development board. There is no limit to the number of "Wi-Fi" development boards*.

![Development Board](../images/zh-tw/docs/webbit/board/board-05.jpg)


In the case of controlling multiple development boards, ** does not support the use of function control**, pay special attention!

![Development Board](../images/zh-tw/docs/webbit/board/board-06.jpg)

![Development Board](../images/zh-tw/docs/webbit/board/board-07.jpg)
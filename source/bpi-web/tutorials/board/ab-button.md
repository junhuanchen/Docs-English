# power switch button

On the left and right sides of the front of the development board, two button switches are preset. Through the control of the switch, the situation of crop networking can be realized, and even the real game remote control or smart home appliance application can be created.

## Button switch block description

The push button switch block can specify three kinds of switch behaviors: “press, release, long press”. The three behaviors can be applied to A, B or A and B respectively. (Long press is defined as continuous press for one second)

![Button Switch](../images/zh-tw/docs/webbit/board/ab-button-01.jpg)

> * Use the button switch block to match the "development board" building block*, select the simulator, after execution, you can use the mouse to click the simulator, select USB, after execution, the physical development board will be controlled via USB connection, and Wi-Fi will be selected. Device ID control can be specified via Wi-Fi.
> - USB control mode is limited to "Installation Editor", please refer to [Editor] (../index.html#software)
> - Wi-Fi mode requires a development board to connect to Wi-Fi, please refer to [Hardware Development Board (Initial Settings)] (../info/setup.html)

![Button Switch](../images/zh-tw/docs/webbit/board/ab-button-04.jpg)

## Press the switch to change the LED matrix pattern

Put the A, B, and A+B blocks on the editing screen, and then place the LED matrix display blocks in the respective blocks. After the execution, if you use the simulator, you can use Click the A, B or A+B button to see the effect of the change. If you are using the physical development board, you can press the switch directly with your finger.

> The A+B button switch in the simulator will only appear if there are blocks on the editing screen with the A+B button switch.

![Button Switch](../images/zh-tw/docs/webbit/board/ab-button-02.gif)

## Press, release, and long press

Through the three actions of pressing, releasing and long-pressing the switch, you can make an example of "there is a pattern when pressed, the pattern will change after the long press, and the light will be turned off when the switch is turned off". If it is executed, if it is Using the simulator, you can click the A button to see the change effect. If you are using the physical development board, you can press the switch directly with your finger.

![Button Switch](../images/zh-tw/docs/webbit/board/ab-button-03.gif)
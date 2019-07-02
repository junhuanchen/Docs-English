# Matrix LED

In the center of the development board, a matrix of 25 full-color LEDs is embedded in the center. Each LED can be mixed in red, green and blue colors to produce different colors, which can be displayed through different positions of lights and colors. Can present a variety of patterns.

## Matrix LED Building Blocks List

The matrix LED block list contains display colors, turn off lights, draw patterns, preset patterns, specify the colors of the lights, marquees, and brightness.

![Matrix LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-01.jpg)

> * Use matrix LED building blocks must be matched with "development board" building blocks*, select the simulator, after execution, it will control the right simulator light number, select USB, after execution, it will control the physical development board through USB connection mode, select Wi-Fi Device ID control can be specified via Wi-Fi.
> - USB control mode is limited to "Installation Editor", please refer to [Editor] (../index.html#software)
> - Wi-Fi mode requires a development board to connect to Wi-Fi, please refer to [Hardware Development Board (Initial Settings)] (../info/setup.html)

![Matrix LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-02.jpg)

## Display color

The "Display Color" block allows 25 lights to illuminate the specified color at the same time. (If black is selected, the effect is equivalent to no light)

![Matrix LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-04.jpg)

The development board selects the simulator, and the color building blocks are selected in red. After execution, the 25 pieces of the virtual development board turn red. (If you have a development board at hand, you can use USB or Wi-Fi connection control)

![Matrix LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-03.jpg)

## Draw a pattern

The "Draw Pattern" bricks can customize the different colors of each light and draw a 5x5 pattern.

![Matrix LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-05.jpg)

Click on the color block above the building block to select different colors. If it is the same color, you can revert to black after repeated clicks (the same effect is used directly with black).

![Matrix LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-07.gif)

For example, draw a flower, let the petals be red, the peduncle and the leaves are green. After execution, the virtual development board will present a colored flower.

![Matrix LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-06.jpg)

## Preset pattern

The "Preset Pattern" building blocks provide 56 preset patterns and a random pattern option (60 patterns randomly take one).

![Matrix LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-08.gif)

After selecting the pattern and color, the corresponding development pattern and color will appear on the virtual development board.

![Matrix LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-09.jpg)


## Display a word

The "Show a word" building block can display *one single * uppercase and lowercase English letters, numbers or punctuation marks, and specify the color of the display. (Chinese characters are not supported)

![Matrix LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-10.jpg)

Enter letters or numbers in the text block and specify the color. When executed, you will see the letters or numbers of the specified color appear.

![Matrix LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-11.jpg)

## Marquee

The "Marquee" building blocks can display a string of characters in a specified color by means of a marquee. The marquee can be played only once or indefinitely and can set the speed at which the text moves. (Chinese characters are not supported)

![Matrix LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-12.jpg)

If the number of marquees is set to "once", the blocks of the marquee will be of the type "* will continue to execute the program after execution*" (click on the small question mark in the front) and the other will not be executed after the marquee is over. Program*, if set to "unlimited", * the program will continue to execute, but the behavior related to the LED matrix will be replaced by the marquee *, pay special attention to the use.

![Matrix LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-13.jpg)

In the example below, after the execution, the red Hello text will appear first, followed by a green smile.

![Matrix LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-14.gif)

## Array control light

The "array control light" building blocks can be used to control the operation of the matrix LEDs in an array.

![Matrix LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-15.jpg)

The order of the arrays corresponds to the order of the lights on the development board. The order of the development board numbers 1~25 is from left to right and top to bottom.

![Matrix LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-16.jpg)

For example, if the three values ​​of the array are set to red, green, and blue, the first to third lights of the board will display the corresponding colors.

![Matrix LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-17.jpg)

If it is a multi-dimensional array, it will be displayed in the order of the array elements. If the element content is left blank, the LED will be off.

![Matrix LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-18.jpg)

## The first few lights

The "number of lights" blocks can specify the color of the first few lights.

![Matrix LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-19.jpg)

The order of the first lights corresponds to the order of the lights on the development board. The order of the development lights 1~25 is from left to right and top to bottom.

![Matrix LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-16.jpg)

Specify the color of the light in different positions. After execution, you will see the light of the specified position light up.

![Matrix LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-20.jpg)

## X, Y coordinate control light

The "X, Y coordinate control light" building blocks can be displayed in the color of the light with the coordinate values ​​of X and Y.

![Matrix LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-21.jpg)

The X and Y coordinates of the development board are (1, 1) in the upper left corner, X plus 1 in the right, Y plus 1, and so on.

![Matrix LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-22.jpg)

Specify the color of the different X and Y lights separately. After execution, you will see the light of the specified position light up.

![Matrix LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-23.jpg)

## Brightness

The "Brightness" brick can control the brightness of "*All LEDs*". The bricks cannot specify the brightness of a single lamp. The darkest to brightest value is 0~20, the default value is 10.

![Matrix LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-24.jpg)

## Turn off the lights

The "lights off" block can turn off "*all LEDs*", which is equivalent to setting the color of 25 lights to black at the same time.

![Matrix LED](../images/zh-tw/docs/webbit/board/rgbled-matrix-25.jpg)
# colour

By changing the color of the elements in the web page, or by specifying the color of the actual color of the full-color LED matrix of the development board, many colorful effects can be achieved by the colorful taste changes.

## Color Building Blocks List

Array blocks include four common color blocks, including specified colors, random colors, RGB three primary colors, mixed colors, and so on.

![color](../images/zh-tw/docs/webbit/basic/color-01.jpg)

## Specify the color

The "Specify Color" building block allows us to select the corresponding color through the color selection panel.

![color](../images/zh-tw/docs/webbit/basic/color-02.jpg)

If we specify that the background of the little monster interaction stage is red, the stage background will turn red after the page is executed.

![color](../images/zh-tw/docs/webbit/basic/color-03.jpg)

## random color

Random Color takes a random color display from each color as each page is executed.

![color](../images/zh-tw/docs/webbit/basic/color-04.jpg)

If you repeat the loop, after the web page is executed, you can see that the color of the little monster stage background changes randomly.

![color](../images/zh-tw/docs/webbit/basic/color-05.gif)

## RGB three primary colors

The "RGB Primary Colors" building block can specify the values ​​of the three primary colors in the web page, and directly present the different colors by numerical values.

> The three primary colors indicate *R red, G green, B blue*, and the three colors have 256 shades from dark to light. By mixing the three colors, more than 16 million colors can be produced. (But the human eye can't distinguish such a variety of colors)

![color](../images/zh-tw/docs/webbit/basic/color-06.jpg)

Because there are 256 colors, the corresponding value is 0 ~ 255, 0 is the darkest, 255 is the brightest, and the corresponding value can be input to produce the corresponding color. For example, red 255 with green 255 will be yellow.

> The three primary colors of the web page are "*Color*", *Red+Green=Yellow*, *Green+Blue=Cyan*, *Red+Blue=Purple*.

![color](../images/zh-tw/docs/webbit/basic/color-07.jpg)

With a repeating loop, you can make a red to yellow color conversion effect.

![color](../images/zh-tw/docs/webbit/basic/color-08.gif)


## Mixed color

The "mixed color" building block means that the two color blocks are mixed in proportion to produce a new color. The ratio is a value between 0 and 1. The smaller the number, the closer the color is to the color. The larger the number, the closer the color is to the color 2.

![color](../images/zh-tw/docs/webbit/basic/color-09.jpg)

If Color 1 is set to red, Color 2 is set to blue, and the mixed color of 0.2 is reddish purple.

![color](../images/zh-tw/docs/webbit/basic/color-10.jpg)

With a repeating loop, you can make a color transition from red to blue

![color](../images/zh-tw/docs/webbit/basic/color-11.gif)
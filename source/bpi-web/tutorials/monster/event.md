#小怪兽互动&stage

In addition to setting the position or size of the little monster, the editor allows us to interact with the little monsters, such as clicking the little monster with the mouse, colliding with the little monsters, colliding with the edge of the stage, etc. Achieve more ideas and ideas.

## Little monster building blocks list ( interaction & stage )

The interactive & stage blocks have mouse clicks on small monsters, mouse touches on small monsters, small monsters colliding with each other, small monsters colliding with the screen, bumping at the edge of the screen, changing the stage background and setting the full screen.

![Little Monster Interactive & Stage] (../images/zh-tw/docs/webbit/monster/event-01.jpg)

## Mouse click

The "click" block allows you to do something when the specified mouse clicks on the little monster.

> The mouse clicks on the building block "* does not need to be placed in the repeating loop*" to repeat the detection.

![Little Monster Interactive & Stage] (../images/zh-tw/docs/webbit/monster/event-02.jpg)

In the example below, when you click on the green monster, you will talk, click on the red monster to zoom in, click on the yellow monster to rotate, and click on the blue monster to change your mood.

![Little Monster Interactive & Stage] (../images/zh-tw/docs/webbit/monster/event-03.gif)

## Mouse touch

The "snake touch" building block contains two behavioral actions, namely what the mouse touches the little monster, and what the mouse does to leave the little monster.

> Note that the behavior of leaving will be repeated after the touch, the mouse touches the building block "* does not need to be placed in the repeating loop *" to repeat the detection.

![Little Monster Interactive & Stage] (../images/zh-tw/docs/webbit/monster/event-04.jpg)

In the example below, when the mouse touches the green monster, the little monster's mood will be happy, and the little monster will return to normal mood after the mouse leaves.

![Little Monster Interactive & Stage] (../images/zh-tw/docs/webbit/monster/event-05.gif)

## Touching each other

"Touching each other" blocks can detect if the little monsters touch each other.

> Touching each other's blocks "* will only detect once*", you must *match the repeating loop* to repeat the detection.

![Little Monster Interactive & Stage] (../images/zh-tw/docs/webbit/monster/event-06.jpg)

The following picture is an example. With repeated loops, you can continuously detect whether the little monsters touch each other and use the mouse to pull the little monster. When the two encounter each other, the little monster becomes a surprised mood, and then returns to normal after separation. .

![Little Monster Interactive & Stage] (../images/zh-tw/docs/webbit/monster/event-07.gif)

## Touching the stage screen

The "collision stage screen" building block can detect whether the small monster touches the four sides of the interactive stage, or individually detects the behavior of the four sides of the upper, lower, left and right sides.

> Collision stage painting area wood "* will only detect once *", must be * with repeated loops *, in order to repeat the detection.

![Little Monster Interactive & Stage] (../images/zh-tw/docs/webbit/monster/event-08.jpg)

The following picture is an example. With the repeated loops, you can make the little monsters become happy when you touch the upper edge or the lower edge of the stage screen. When you touch the left or right side, you will get angry emotions. If you don’t touch it, it will be normal emotions. .

![Little Monster Interactive & Stage] (../images/zh-tw/docs/webbit/monster/event-09.gif)

## Touching the stage screen will rebound

"Bounces on the stage screen." The building block is a simplified version of the "touch the stage picture" building block. The behavior after the touch is singularized as "bounce". The bounce indicates the opposite position. * If you hit the left and right sides of the stage, The X-direction of the little monster moves in the opposite direction. If you hit the top and bottom of the stage, the Y-direction of the little monster moves in the opposite direction*.

> When you touch the stage screen, you will rebound the building block "* will only detect once*", you must *match the repeating loop* to repeat the detection.

![Little Monster Interactive & Stage] (../images/zh-tw/docs/webbit/monster/event-10.jpg)

The following picture is an example. With a repeating loop, you can make the little monster touch the stage screen and bounce when it hits the edge of the stage.

![Little Monster Interactive & Stage] (../images/zh-tw/docs/webbit/monster/event-11.gif)

## Replace the stage background color or picture

"Replace the stage background color" and "Replace the stage background image", you can change the monster stage background to the specified color or picture. The picture will be filled in the image URL and will be replaced after execution. (Image support jpg, jpeg, png, and gif)

![Little Monster Interactive & Stage] (../images/zh-tw/docs/webbit/monster/event-12.jpg)

For example, find the image URL of [Qingming Shanghe Map] (https://theme.npm.edu.tw/opendata/att/collectionPic/04015934/17024347.jpg#_blank) and paste the URL on the background image. In the text building block, after the web page is executed, you will see the stage background become a clear upper shell.

![Little Monster Interactive & Stage] (../images/zh-tw/docs/webbit/monster/event-13.jpg)

## Set the stage to full screen

The "Set Stage as Full Screen" building block does not affect any operation. It only turns the monster interactive stage into full screen size when "Web page execution".

![Little Monster Interactive & Stage] (../images/zh-tw/docs/webbit/monster/event-14.jpg)

If you don't want to use this function, you can also manually operate it. You can also switch the full screen by clicking the small button at the top right of the monster interaction stage.

![Little Monster Interactive & Stage] (../images/zh-tw/docs/webbit/monster/event-15.jpg)

## Get the stage size

The "Get Stage Size" building block can get the width or height of the current monster interactive stage.

![Little Monster Interactive & Stage] (../images/zh-tw/docs/webbit/monster/event-16.jpg)

The example below will show the stage width when the web page is executed, and the red monster tells the stage height.

![Little Monster Interactive & Stage] (../images/zh-tw/docs/webbit/monster/event-17.jpg)
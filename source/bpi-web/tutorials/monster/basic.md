#小怪兽操作

The editor has designed four cute little monsters, which can control the speech, sound, interaction and behavior of each little monster through the logical sequence of program blocks, and even further interact with the actual development board. More fun and interesting apps.

## Little monster building blocks list (basic operation)

Basically, the little monster's building blocks have speech, display pictures, emotions, change position, change angle, change size, display hiding and class, etc., and these blocks can control the external performance of the little monster.

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-01.jpg)

## Speech & No Speech

The "speech" and "no speech" blocks allow the little monster to speak the specified text, or don't speak the text. You can also choose which little monster to speak through the drop-down menu, or all the little monsters to talk together.

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-02.jpg)

As long as the specified text is connected behind the building blocks, the little monster will say the specified text after the web page is executed.

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-03.jpg)

Just leave the text blank or use a brick that doesn't talk, so that the little monster can't talk.

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-04.jpg)

## Show pictures

The "show image" building block allows the mob to display a "web image".

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-05.jpg)

For example, search for [Mona Lisa] from Wikipedia (https://en.wikipedia.org/wiki/%E8%92%99%E5%A8%9C%E4%B8%BD%E8%8E %8E#_blank), you can get the "[URL] of this image (https://upload.wikimedia.org/wikipedia/commons/thumb/e/ec/Mona_Lisa%2C_by_Leonardo_da_Vinci%2C_from_C2RMF_retouched.jpg/460px-Mona_Lisa%2C_by_Leonardo_da_Vinci %2C_from_C2RMF_retouched.jpg#_blank)", copy the image URL and paste it into the text space of the small monster display image. After the webpage is executed, you will see the little monster display this image.

> The current image format only supports jpg, jpeg, png, gif

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-06.jpg)

## Emotions

"Emotional" blocks can change the mood of little monsters, including happy, surprised, angry, sad and random.

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-07.jpg)

Select the corresponding little monster (you can also have four at the same time), select the corresponding emotions, and you will see the emotional changes of the little monsters after the webpage is executed.

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-08.jpg)

## Change location

The "change position" block can specify that the little monster changes *the current position*, and the options are up, down, left, right, random or toward the mouse.

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-09.jpg)

With the blocks that are repeated ten times and waiting for 0.1 seconds, you can move the little monsters to the upper right.

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-10.gif)

If you use wireless repeating blocks, with the setting "Move to the mouse position", you can let the little monsters chase the mouse to move.

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-11.gif)

## Positioning

The "positioning" bricks can place the little monsters at the specified coordinate positions.

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-12.jpg)

The monster's coordinate system uses the *Cartesian coordinate system* (right-angle coordinate system), with y being positive and x being positive to the right, and (0,0) * origin being at the lower left corner of the monster interactive stage*, specifying The little monster xy coordinates, the small monster will appear in the specified position after the web page is executed.

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-13.jpg)

## Rotation angle

"Rotation Angle" can specify that the little monster changes *the current angle*, and the options are left or right.

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-14.jpg)

With the infinite number of blocks, you can make the little monsters rotate 10 degrees every 0.1 seconds.

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-15.gif)


## Facing the direction

The "facing direction" angle specifies the angle at which the little monster rotates, clockwise positive and counterclockwise negative.

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-16.jpg)

Because the "facing direction" is an angle specified, if you want to achieve the same effect as the previous building "rotation angle", you can use variables with infinitely repeating blocks, and modify the variable values ​​at each execution.

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-17.gif)

## Auto face-to-mouse direction

The "Automatic Face-to-Mouse" building block allows the little monster to go in the direction of the mouse. There are two options, Auto and Stop. The preset does not face the mouse.

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-18.jpg)

Because the "automatic face-to-mouse direction" will only be executed once, if you want the little monster to face the mouse constantly, you must match the infinitely repeating blocks. As shown below, the small monster will automatically rotate toward the mouse after the webpage is executed.

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-19.gif)

## Get coordinates and angles

The "Get coordinates and angles" bricks can read the current X coordinates, Y coordinates, and rotation angle of the little monster.

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-20.jpg)

In the example below, you can let the little monsters speak their own X coordinates, Y coordinates, and rotation angles.

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-21.jpg)

## Size zoom in and out

The "size enlargement" building block can specify that the little monster changes *the current size*, and the options are enlarged or reduced.

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-22.jpg)

With the blocks that are repeated ten times and waiting for 0.1 seconds, after the web page is executed, the monsters can be gradually enlarged.

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-23.gif)

## size percentage

The "% of size" block allows you to specify the percentage of small monsters to zoom in and out.

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-24.jpg)

Since 100% means the size of the original monster, 200% will be doubled, and 50% will be reduced to 1/2 size. The following figure shows the size of the four monsters in different sizes.

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-25.jpg)

## Display / Do not display

The "Show/Do Not Show" building block allows you to specify whether the little monster is displayed in the interactive stage area.

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-26.jpg)

## hierarchy

The "hierarchy" building blocks can specify the hierarchy of small monsters, with the top layer at the top and the bottom layer at the bottom.

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-28.jpg)

By repeating the loop and waiting for the blocks, the little monsters can be displayed in the front.

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-29.gif)

## Back to original state

The "back to original state" building block allows the little monster to return to its original state. The initial state includes non-speaking, preset coordinates, preset rotation angle, and preset size.

![Little monster basic operation] (../images/zh-tw/docs/webbit/monster/basic-27.jpg)
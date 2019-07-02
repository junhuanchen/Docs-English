#音乐&声

The development board has a built-in miniature buzzer that can emit a single sound of three octaves. With a combination of different note codes, or with built-in example music, the board can make a variety of beautiful melodies.

## Music & Sound Building Blocks List

The building blocks of music & sound include building blocks such as playing a certain scale, rest, preset music, and stopping playing.

![Music & Sound](../images/zh-tw/docs/webbit/board/buzzer-01.jpg)

> *Music & sound building blocks must be matched with "development board" building blocks*, select the simulator, after execution, you can hear the sound of the computer speaker, select USB, and then control the physical development board through USB connection, so that the development board beeps The sound is emitted, and Wi-Fi is selected to specify the Device ID control via Wi-Fi.
> - USB control mode is limited to "Installation Editor", please refer to [Editor] (../index.html#software)
> - Wi-Fi mode requires a development board to connect to Wi-Fi, please refer to [Hardware Development Board (Initial Settings)] (../info/setup.html)

## Playing scales

The “Performance Scale” building block can play three octaves, and you can also specify the tempo for each scale. The beats are divided into 1/16, 1/8, 1/4, 1/2, 1 and 2 beats.

![Music & Sound](../images/zh-tw/docs/webbit/board/buzzer-02.jpg)

Clicking on the scale option will bring up a virtual piano keyboard, use the mouse to move to the key, and the computer's speaker will make a corresponding sound.

![Music & Sound](../images/zh-tw/docs/webbit/board/buzzer-03.gif)

In the gap of the scale, you can put the scale and rest blocks separately, and the continuous gap can only be placed in the beat block.

![Music & Sound](../images/zh-tw/docs/webbit/board/buzzer-08.jpg)

Put in several scales and you can hear one scale and then one scale after execution.

![Music & Sound](../images/zh-tw/docs/webbit/board/buzzer-04.gif)

Since the playing scale building block will be of the type "* will continue to execute the rear program* after the performance is completed", if the program is placed after the scale, the rear program will be executed after all the scales have been played.

![Music & Sound](../images/zh-tw/docs/webbit/board/buzzer-05.gif)

Playing scales can also be combined with repeated loops to repeat the effect of repeating a melody.

![Music & Sound](../images/zh-tw/docs/webbit/board/buzzer-06.gif)

The use of scale building blocks supports the ability to edit music and reuse it by array arrangement. The following example shows the scale and beat separately into two arrays.

> In the case of arrays, if the number of scales is less than the beat, the extra beats will be played in the last scale. If the number of beats is less than the scale, the extra scale will be played with the last beat.

![Music & Sound](../images/zh-tw/docs/webbit/board/buzzer-09.jpg)


## Playing a break

The "playing rest" block indicates that the beat has no sound, which is equivalent to using the scale building blocks with the rest blocks.

![Music & Sound](../images/zh-tw/docs/webbit/board/buzzer-07.jpg)

![Music & Sound](../images/zh-tw/docs/webbit/board/buzzer-10.gif)

## Playing music

The "Music Music" building blocks include Super Malang, Super Malang and Chord, True and Good, Big Brother Dad, and Five Musics. They can be used independently or in combination with scale blocks.

![Music & Sound](../images/zh-tw/docs/webbit/board/buzzer-11.jpg)

Since the performance of the music building block will be the type of "* will continue to execute the rear program* after the performance is completed", if the scale or other program is placed after the music is played, the rear program will be executed after the music performance is completed.

![Music & Sound](../images/zh-tw/docs/webbit/board/buzzer-12.gif)


## Stop/Pause/Continue to play

The "stop/pause/continue to play" blocks control the behavior of the music.

![Music & Sound](../images/zh-tw/docs/webbit/board/buzzer-13.jpg)

The example in the figure below controls the music playback through the button switch of the development board. When A and B are pressed at the same time, playback starts. When the playback is in progress, pressing A will pause, and pressing B will continue playback.

![Music & Sound](../images/zh-tw/docs/webbit/board/buzzer-14.gif)

If you want to mix the music and scales, you can stop the existing music and switch it by adding the blocks of "stop playing" before switching music.

![Music & Sound](../images/zh-tw/docs/webbit/board/buzzer-15.jpg)
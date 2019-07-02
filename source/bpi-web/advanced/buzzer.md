# buzzer

The buzzer is a device that can generate a sound signal. It is powered by DC power. After the source of the communication signal, the audio signal current passes through the electromagnetic coil, causing the electromagnetic coil to generate a magnetic field, causing the diaphragm to vibrate periodically. The Webduino Bit is built-in. The buzzer can play seven octaves of sound, and the specified sound can be played by filling in the note code on the web page.

## Basic operation

Open [Webduino Blockly Bit Experience Edition] (https://webduino.com.cn/link.html?lang=zh-hans&type=blockly), put * development board building blocks* in the editing area, and use "* emulation by default. "*", connect to the "*Virtual Bit Development Board*" on the screen, and the default Device ID is "*1234*".

> Development board related building blocks, under the "* development board*" directory.

![](img/tutorials/zh_cn/rgbmatrix-01.jpg)

If you are using "*Ent Bit Development Board*", select "*Wi-Fi*" from the drop-down menu and fill in the Device ID of the development board in the back field.

![](img/tutorials/zh_cn/rgbmatrix-02.jpg)

Put the building blocks of "*Set buzzer as buzzer*" in the development board.

> Buzzer related blocks, under the "* buzzer*" directory.

![](img/tutorials/zh_cn/buzzer-01.jpg)

Put the blocks in "Play with Buzzer", the notes and rhythm are placed first, and the first drop-down menu of "Notes" has "* silent, C, CS, D, DS, E, F, FS, G, GS, A , AS, B*", can be imagined as the black and white keys of the piano, the black key with S, the second pull-down menu is a few octaves, here you can set seven octaves (1~ 7), * The higher the number, the higher the sound*, and the "rhythm" is *a fraction of a second*, at least 1/10 seconds.

> You can put several note rhythms in succession, and play them in the order they are placed.

![](img/tutorials/zh_cn/buzzer-02.jpg)

If you feel that the rhythm of the notes is cumbersome, you can also use the blocks that fill in the rhythm of the notes.

> If the number of rhythms is less than the note, the extra notes will be played using the last rhythm number.

![](img/tutorials/zh_cn/buzzer-03.jpg)

If you don't edit music at all, you can even use the "music" blocks directly. There are five different tune melody in the default.

![](img/tutorials/zh_cn/buzzer-04.jpg)

Finally, you can mix the above three modes of playing music, play the single tone first, then play the music and play the one-time note rhythm.

![](img/tutorials/zh_cn/buzzer-05.jpg)

Click the red button on the top right to execute. If it is a virtual development board, it will hear the sound from the speaker or earphone. If it is a physical development board, you will hear the buzzer on the top.

> Example Answer: [Webduino Bit Buzzer Play Music] (https://webduino.com.cn/link.html?lang=zh-hans&type=example&blockly=buzzer01)

## Web Button Control Buzzer

Open the web interactive test area, select the "button behavior" from the drop-down menu, and several web buttons will appear in the screen. At this time, the corresponding building block function will also appear in the lower right corner.

![](img/tutorials/zh_cn/buzzer-06.jpg)

Put the "*click button...execute*" building block, put the sound to be played by the corresponding buzzer, or put in the block that sets the buzzer playing state (pause, stop, continue), such a When the button is clicked, the buzzer will play the sound or pause the play.

> It is often forgotten to put in the "* Use buzzer to play" blocks, pay special attention to *.

![](img/tutorials/zh_cn/buzzer-07.jpg)

> Example Answer: [Web Button Control Webduino Bit Buzzer] (https://webduino.com.cn/link.html?lang=zh-hans&type=example&blockly=buzzer02)
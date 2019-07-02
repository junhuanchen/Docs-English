# Voice reading

Voice reading is through the computer's speech synthesizer, and we can pronounce the language we specify. The educational version of the speech reading can easily make creative applications such as voice time, voice notification, voice dialogue, etc., and can adjust the speed of the voice and The tone changes a lot of interesting patterns.

## Description of building blocks

The speech reading block contains three languages ​​(Chinese, English or Japanese), five tones and five speeds.

> Note that * In the "Installed" editor, Chinese and Japanese* may not be read normally. If you are unable to pronounce it, please use the "Web Edition" version of the editor. (Refer to [editor](../index.html#software) )

![Voice reading] (../images/zh-tw/docs/webbit/sound/speak-aloud-01.jpg)

The voice reading block is of the type "* will continue to execute the program after execution *" (click on the small question mark in the front), when the program uses the voice reading block, * will continue to execute other programs after the end of the reading *, Pay special attention to the use.

[[Voice reading] (../images/zh-tw/docs/webbit/sound/speak-aloud-02.jpg)

## Reading text

To read the text aloud, you only need to enter the corresponding text in the rear text block. After the web page is executed, you can hear the voice from the computer speaker.

![Voice reading](../images/zh-tw/docs/webbit/sound/speak-aloud-03.jpg)

## Read the text of different paragraphs

If you want to read the text of different paragraphs, the first method can use the building block to match the variable building blocks, and the voice will be heard from the computer speaker after the web page is executed.

![Voice reading] (../images/zh-tw/docs/webbit/sound/speak-aloud-04.jpg)

The second method can read the characteristics of the building blocks by voice, and sequentially connect the texts of different paragraphs to the rear. After the webpage is executed, the first paragraph is read aloud, and then the second paragraph is read.

![Voice reading] (../images/zh-tw/docs/webbit/sound/speak-aloud-05.jpg)

## Read the input text

Since the "Enter text in the dialog box" and the voice reading block have the same characteristics, with the repeated loops, you can read through the voice and read the input text.

![Voice reading] (../images/zh-tw/docs/webbit/sound/speak-aloud-06.jpg)
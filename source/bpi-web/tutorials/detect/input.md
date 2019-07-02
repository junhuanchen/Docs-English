# Dialog input text

If you use the "Dialog Input Text" building block in the editor, after the web page is executed, at the bottom of the screen of the monster interaction Wutai, a dialog box for entering text will appear, which can be further developed with the development board or the little monster by inputting the text. interactive.

## Building block list

There are two types of building blocks for entering text in the dialog box. The first one is "Enter text in dialog box". After execution, a dialog box for inputting text will appear. The second type is "Entered text". After execution, the input will be obtained. Text.

![Dialog input text] (../images/zh-tw/docs/webbit/detect/input-01.jpg)

## Dialog input text

The "Dialog Input Text" building block belongs to the type of "* Execution will continue to execute the following program*" (click on the small question mark in the front) will be prompted. When there is this brick in the editing screen, * when the program encounters this Block bricks will pause until the text is entered before continuing *.

![Dialog input text] (../images/zh-tw/docs/webbit/detect/input-02.jpg)

For example, the little monster in the program below will not speak after the web page is executed, and will not speak until the text is entered.

![Dialog input text] (../images/zh-tw/docs/webbit/detect/input-03.gif)

## Get the entered text

The "input text" building blocks* are always placed after the "dialog input text" building block*, and the input text will be obtained. If the above example is slightly modified, the little monster can be told to input the input text.

![Dialog input text] (../images/zh-tw/docs/webbit/detect/input-04.gif)

## Repeat input text

With the infinitely repeated loops, you can modify the above example to change the version of "Continuously Enter Text".

![Dialog input text] (../images/zh-tw/docs/webbit/detect/input-05.gif)

##一问一答

By inputting text, you can easily achieve the effect of "one question and one answer". Before entering the text block, place the small monster to ask for the name of the text. After the web page is executed, it will stay at the stage of inputting the text. After inputting the text, create the string. Building blocks, let the little monsters say "XXX hello" text combination.

![Dialog input text] (../images/zh-tw/docs/webbit/detect/input-06.gif)
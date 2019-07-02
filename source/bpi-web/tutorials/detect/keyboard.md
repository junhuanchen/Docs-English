# Keyboard behavior

The mouse and keyboard are two indispensable input devices for the computer. When you are familiar with the way you control the behavior of the keyboard, you can simply convert the keyboard into interesting interactive components. It is easy to make a piano keyboard or game controller. It can also be used with text input to make many unexpected interaction effects.

## Detecting keyboard behavior

The "Detect Keyboard Behavior" building block can detect most of the keys on the computer keyboard. The detection methods include pressing and releasing.

> Detecting keyboard behavior building blocks* is in a state of detecting * at any time, * does not need to be matched with an infinite repeating loop*.

![Keyboard Behavior](../images/zh-tw/docs/webbit/detect/keyboard-01.jpg)

By pressing and releasing the two behaviors, you can let the little monster say the corresponding button name while pressing the keyboard, and then do not speak after releasing the keyboard.

![Keyboard Behavior](../images/zh-tw/docs/webbit/detect/keyboard-02.gif)

The behavior of pressing the keyboard will be "*Continuous execution of the command*". Similar to the typing, if a button is pressed, a series of characters of the button will appear on the screen, for example, the following figure, set to press the keyboard A. The little monster will rotate to the left. After the web page is executed, keep pressing the A monster and it will continue to rotate. When the A monster is released, it will stop, and there is no need to set the release command.

![Keyboard Behavior] (../images/zh-tw/docs/webbit/detect/keyboard-03.gif)

## Keyboard Controls Little Monsters Move

Building blocks can *detect multiple keyboard button behaviors* at the same time. It is very easy to make "press the up, down, left and right buttons through the keyboard behavior, and the little monsters will move up and down and left and right."

![Keyboard Behavior](../images/zh-tw/docs/webbit/detect/keyboard-04.gif)
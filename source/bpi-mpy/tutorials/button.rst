Detection panel button
==============================================================

Ok, at least I have created some code to let the board do something.
So, let's deal with the input of the device, such as the key input.
First, we need to know two concepts, the Output output is the output from the device to the periphery, Input
Input is some information received during the processing of the device

Then the most obvious input on the board is two buttons, two A and B left and right on the board.
Button, if we can know if the board button is pressed, or if it is pressed, or if it is pressed a few times, how to do it?

In fact, this is not difficult, it is better to say that it is easy to do.

.. code:: python

    From microbit import *

    Sleep(2000)

    Display.scroll(str(button_a.get_presses()))

This code will pause for two seconds before running, then you will start to press the button, which will scroll to show you press A.
The number of times. It's that simple, although the code is not very useful, it still provides some new ideas, so you can imagine more ways to control the hardware.

This sleep
    The function can pause the board for a certain amount of time. The pause time is the number of milliseconds. If you want to pause at some time in your program, write it as above.
    The sleep function will do.
2. The button_a object allows you to get the number of times pressed in a time via the get_presses method.

Then once get_presses gets the value, pass it to display.sroll
In this method, only the character type can be accepted, so we need to convert the integer to a string through the str function.
So for the python principle we made a hypothesis for a deeper understanding if you are at 10
Pressed 10 times in seconds, then how to execute the third line of the above code? Thanks to python
The code is executed from the innermost layer. and so:

``display.scroll(str(button_a.get_presses()))``

Of course, this will show the number of times you press the button (you can specify it for a while).

``display.scroll(str(10))``

Now Python already knows how much has been pressed, so the next one will become a string, and the note must be the innermost priority, ie execute first.
Str("10").

``display.scroll(str("10"))``

Loop processing event
----------------------------------------

If you want the board to respond to a button press event, then you need to use if
It is judged whether the button is pressed, and this judgment method is suggested to be placed in an infinite loop. E.g:

.. code:: python

    While True:
         # Do stuff

So we can build a very simple code

.. code:: python

    From microbit import *

    While True:
         If button_a.is_pressed():
              Display.show(Image.HAPPY)
              Display.clear()

At this point, you can press the button A to display the Image we have learned before. This is what the so-called learning is.
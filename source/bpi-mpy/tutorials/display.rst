Hello, World!
==============================================================

The traditional way to start programming in a new language is to have the computer print "Hello, World!".

.. image:: images/scroll-hello.gif

This is easy for MicroPython ::

  From microbit import *
  Display.scroll("Hello, World!")

Each line of the above code has its effect.

::

  From microbit import *

Tell MicroPython to get all the information it needs for BPI-BIT. All of this is placed in the microbit module (a module is a pre-existing code base). When you enter a message, you are telling MicroPython that you want to use that information. Also, * is the way Python represents all the information. So, from microbit import * means that I need to use everything in the microbit codebase.

::

  Display.scroll("Hello, World!")

Tells MicroPython to use the display command to scroll through the string's "helloworld" character number, which is a module in the microbit that represents the physical display of the device, and the content displayed in quotes (').

Copy the relevant code for "Hello, World!" into the editor and have the device display these characters. You can try to change what is displayed.

Why not try it yourself?

.. image:: images/scroll.gif

.. Attention::

 The code you write may go wrong.

 But MicroPython will help. When an error occurs, the REPL scrolls through some error messages, and if it does, it will display the line number of the error.

 Python requires that you enter the exact information. For example, for Python, Bpibit, bpibit, and bpiBit are all different things. If MicroPython displays an error comment for NameError, it may be because the information entered is not accurate. Like “Nicholas” and “Nicolas”, although the names are similar, they represent two different people.

 If MicroPython prompts SyntaxError , this is because you entered code that MicroPython does not recognize. Check if you forgot to type something like " or : a class of characters. It's like entering a period in the middle of a sentence, the meaning of the sentence becomes incomprehensible.

 The board may stop responding: the new code does not work for it, there is no way to enter a new command into REPL. If this happens, try rebooting. Unplug the USB cable. If the power cord is connected, you need to unplug the power cord and plug it in again. You may also need to quit and restart the code editor.

Modify character color
---------------------------

Compared to microbit, bpibit's led panel uses a programmable RGB light (ws2812b).

.. image:: images/ws2812.png

This RGB lamp can theoretically display 255 * 255 * 255 colors, which is 16 million colors. Is it a little unbelievable? Let's start our color show.

It is very simple to change the color of the font. There are 8 colors preset in the firmware.

.. code:: python

  Black = [0, 0, 0]
  Red = [2, 0, 0]
  Orange = [2, 1, 0]
  Yellow = [2, 2, 0]
  Green = [0, 2, 0]
  Blue = [0, 0, 2]
  Indigo = [0, 2, 2]
  Purple = [2, 0, 2]

They are black (lights are off), red, orange, yellow, green, blue, enamel, purple. With these basic colors, you can modify our font colors.

.. code:: python

  From display import*
  Display = Display()
  Display.scroll("Hello, World!", Yellow)

.. image:: images/yellow.gif

The color displayed by the board by default is red. You can modify the color of the displayed characters by adding other colors after the string (that is, "Hello, World!" above). From the picture above you can see that the color of our characters has turned yellow. Some students who are here may have questions?

So how do you make the colors of each character displayed different? Let's take a look at the following operations.

.. code:: python

  From display import*
  Display = Display()
  Color = [Red, Orange, Yellow, Green, Blue, Indigo, Purple]
  Display.scroll("ROYGBIP", color)

.. image:: images/color.gif

We created a new list color, which stores the colors needed for each character in order, and then adds the color after the scroll function, so that the color of each character is different.

Custom color
---------------------------

The smart classmates here have to ask questions, not to say that there are more than 16 million colors. How come these kinds? Well, no hurry, let us slowly come.

Having said RGB for so long, what is RGB? RGB color is commonly referred to as the three primary colors, R for Red (red), G for Green (green), and B for Blue (blue). Any color that can be seen by the naked eye in nature can be superimposed by these three colors. In a computer, the so-called "how much" of RGB refers to brightness and is represented by an integer. Normally, RGB has 256 levels of brightness, which are represented by numbers from 0, 1, 2... up to 255. Note that although the number is up to 255, 0 is also one of the values, so a total of 256 levels. According to the calculation, 256 levels of RGB colors can be combined to form about 16.78 million colors, that is, 256 × 256 × 256 = 16777216. It is also often referred to as 16 million colors or tens of millions of colors. Also known as 24-bit color (2 to the 24th power). In the LED field, a three-in-one full-color technology is used, that is, a full-color pixel is composed of RGB three-color chips in one light-emitting unit. As this technology continues to mature, led display technology will bring people more rich and true color experience.

Back to the topic, how do we control our board to display the color we want? In front of us, we use the list to save the color information.

.. code:: python

  Red = [2, 0, 0]

Here we can also define our colors in this way.

So why is Red [2, 0, 0], in fact, the three numbers in the list correspond to the brightness of our R (red) G (green) B (blue), which is mentioned in the previous color. There are 256 levels of brightness. It is obvious that [2, 0, 0] means that the brightness of red is 2, the brightness of green is 0, and the brightness of blue is 0. This will give you the meaning of other color lists.

Let's define a mycolor = [1 , 2 , 3] to see the effect of the display

.. code:: python

  From display import *
  Display = Display()
  Mycolor = [3,3,3]
  Display.scroll("hello",mycolor)

.. image:: images/mycolor.gif

Is it very interesting, I believe that you will have a lot of interesting ideas at this time, then hurry and try it.

.. Attention::

  The brightness of each color has 0-255. A total of 256 values ​​can be selected, so the minimum is [0, 0, 0], and the maximum is [255, 255, 255]
  Do not adjust the brightness too high, too bright and easily hurt your eyes.
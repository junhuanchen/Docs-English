Panel display image
==============================================================

Before I start the project, you can know that MicroPython has a lot of built-in images. If you want to display a smiley face, then you only need to run the following code.

.. code:: python

    From microbit import *
    Display.show(Image.HAPPY)

The effect is as follows

.. Image:: images/emoj.jpg

.. Note::

    Through the previous chapter, we think you should know the purpose of the first line, then the second line refers to the display module to display the built-in Image image, the smile pattern we show is actually only part of the Image, and its name Called Happy, and we want to show it by using show and placing it in brackets, so write it as ``display.show(Image.HAPPY)`` and try it out.

Built-in image list
---------------------------

.. code:: python

- Image.HEART
- Image.HEART_SMALL
- Image.HAPPY
- Image.SMILE
- Image.SAD
- Image.CONFUSED
- Image.ANGRY
- Image.ASLEEP
- Image.SURPRISED
- Image.SILLY
- Image.FABULOUS
- Image.MEH
- Image.YES
- Image.NO
- Image.CLOCK12, Image.CLOCK11, Image.CLOCK10, Image.CLOCK9, Image.CLOCK8, Image.CLOCK7, Image.CLOCK6, Image.CLOCK5, Image.CLOCK4, Image.CLOCK3, Image.CLOCK2, Image.CLOCK1
- Image.ARROW_N, Image.ARROW_NE, Image.ARROW_E, Image.ARROW_SE, Image.ARROW_S, Image.ARROW_SW, Image.ARROW_W, Image.ARROW_NW
- Image.TRIANGLE
- Image.TRIANGLE_LEFT
- Image.CHESSBOARD
- Image.DIAMOND
- Image.DIAMOND_SMALL
- Image.SQUARE
- Image.SQUARE_SMALL
- Image.RABBIT
- Image.COW
- Image.MUSIC_CROTCHET
- Image.MUSIC_QUAVER
- Image.MUSIC_QUAVERS
- Image.PITCHFORK
- Image.XMAS
- Image.PACMAN
- Image.TARGET
- Image.TSHIRT
- Image.ROLLERSKATE
- Image.DUCK
- Image.HOUSE
- Image.TORTOISE
- Image.BUTTERFLY
- Image.STICKFIGURE
- Image.GHOST
- Image.SWORD
- Image.GIRAFFE
- Image.SKULL
- Image.UMBRELLA
- Image.SNAKE

There are so many visible numbers. When you see this, we think you can try other pictures and have fun.

Try DIY pictures
---------------------------

Of course, you certainly won’t stop there, so how can you go further? For example, create your own picture?

So Easy!!!

Each LED can be set to a value on the physical display, similar to high and low levels. For example, if a pixel is set to 0, its brightness is 0. However, if it is set to 9, then it means The brightness of the lamp is 9. So remember this sentence, from 0 to 9, the brightness is increasing in order! Based on this, we can easily create a new picture we want.

.. code:: python

    From microbit import *

    Boat = Image("05050:"
                    "05050:"
                    "05050:"
                    "99999:"
                    "09990")

    Display.show(boat)

.. image:: images/emoj2.jpg

.. Note::

    At runtime, you should be able to see one such picture! !

Now that you know how to draw, you should notice that there is one at the end of each line: then both sides are enclosed with double quotation marks, which are just the brightness of the numerical representation, so creating an image is as simple as that.

    But in fact, you don't need to write multiple lines. If you can guarantee that each line doesn't go wrong, you can write it like this.

.. code:: python

    Boat = Image("05050:05050:05050:99999:09990")

Make simple animations
---------------------------

Static images are fun, but more fun is to make them move. This is exciting but easy to do in Python, just use a list of images~!

If there are some shopping lists here:

[Eggs, Bacon, Tomatoes]

Then you need to represent these gadgets in Python in a way.

.. code:: python

    Shopping = ["Eggs", "Bacon", "Tomatoes" ]

This method is called list, which is a list. We simply create a list called shopping, and then it contains 3 elements. Python knows it is a list because it has a pair of parentheses [], and the elements in the list are Separated by commas, then in this example, items contains three strings, "Eggs", "Bacon", and "Tomatoes". We need to know that they are all string objects because they are split with "".

You can use the list to store anything in python. The following example will teach you how to create numbers with lists.

Then you need to represent these things in Python in one way.

.. code:: python

    Shopping = [2, 3, 5,11 ]

The list also holds many different types of variables:

.. code:: python

    Mixed_up_list = ["hello!", 1.234, Image.HAPPY]

Notice that the last element doesn't, it's an Image object, so we can tell Python to store an Image list, but in the built-in method, there are two objects that have already been made. They are called Image.ALL_CLOCKS and Image.ALL_ARROWS.

.. code:: python

    From microbit import *
    Display.show(Image.ALL_CLOCKS, loop=True, delay=100)

Like a single image, we use display.show to display it on the device. However, we tell Python to use the Image.ALL_CLOCKS list and then it will understand and display all the elements of the list in order. We can also tell Python to keep the loop state. By *loop=True*\ , in addition, we can also set the time for this animation to switch pictures. Pass the following code. \ ``delay=100``\.

Now you know how to create an animation, and how do you know how to avoid looping all the time? How to change the speed of animation playback? If you understand it, just give it a try! ~

Let's create a list of our own animations. In this case, we'll make an animation where the boat sinks to the bottom.

.. code:: python

    From microbit import *

    Boat1 = Image("05050:"
                     "05050:"
                     "05050:"
                     "99999:"
                     "09990")

    Boat2 = Image("00000:"
                     "05050:"
                     "05050:"
                     "05050:"
                     "99999")

    Boat3 = Image("00000:"
                     "00000:"
                     "05050:"
                     "05050:"
                     "05050")

    Boat4 = Image("00000:"
                     "00000:"
                     "00000:"
                     "05050:"
                     "05050")

    Boat5 = Image("00000:"
                     "00000:"
                     "00000:"
                     "00000:"
                     "05050")

    Boat6 = Image("00000:"
                     "00000:"
                     "00000:"
                     "00000:"
                     "00000")

    All_boats = [boat1, boat2, boat3, boat4, boat5, boat6]
    Display.show(all_boats, delay=500, loop=True)


.. Note::

    running result:

    .. image:: images/running.gif

Modify the color of the image
---------------------------

We modified the color of the displayed characters in the previous chapters. How do I change the display color of the image? Let us then look down.

.. code:: python

    From microbit import *
    From display import *
    Display.show(Image.ALL_CLOCKS, color=Blue, loop=True, delay=100)

We are still using the above example to change its color by simple modification. We can see that the biggest difference from the previous code example is the addition of color=Blue to the show() function. This code is added to the end of the Image, which is the location of the second argument to show() . The color displayed at this time has been modified by us.

.. image:: images/blue.gif

As we mentioned in the previous chapters, if we want to use the built-in color, we need to import the display module. We use the built-in color Blue here, so we import the display module from the beginning by using display import \*.

Of course, what if the built-in colors do not meet the requirements? You can also refer to what we said in the previous chapter, we can customize a color.

.. code:: python

    From microbit import *
    Mycolor = [3, 1, 1]
    Display.show(Image.ALL_CLOCKS, color=mycolor, loop=True, delay=500)

.. image:: images/mycolor.gif

.. Note::

    Then let's explain how the code works.

    - The first code is to create an image of 6 ships.
    - Then store them with a list.
    - Then use display to display these images and set the delay to 500 milliseconds
    - Finally, loop=True is set, so this ship will sink again and again.
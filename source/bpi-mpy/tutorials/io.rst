Control gold finger IO
==============================================================

IO refers to Input/Output in the computer, that is, input and output, referred to as IO port.

.. image::image/io.png

The various IO interfaces are different. Some special interfaces are larger. In general, labels are also printed near the user for easy understanding. For example, the bottom of the board is 0/1/2/3V. The order of /GND is distributed on the golden finger (mostly the computer is calculated from 0).

If you attach the gold finger to the base, then the pins of other smaller blue and white lines can be used. This is especially pointed out in the hardware introduction in the first chapter. You can check the product introduction on the left.

In this microbit module, the interface of the board is defined as a pinN object, where N represents the value of the interface, so the interface number 0 is also called the pin0 object. If you feel that this is not easy to use later, you can use the pin of the import machine. Redefine to the pin name you like.

"shy" board
---------------------------

The following case to write is very interesting.

I want to touch the board's pin and let it react accordingly. It looks like this board is like a shy girl.

The prepared code is as follows:

.. code:: python

   From microbit import *
   While True:
       If pin1.is_touched():
           Display.show(Image.HAPPY)
       Else:
           Display.show(Image.SAD)

At this time, you need a hand to touch the pin of the No. 1 tag, you can see the board turned from sad to happy.
If you loosen it, it will change your expression again. Is it angry? XD

The program is explained as follows: 1. Run ``pin1.is_touched()` repeatedly.
To determine if this pin has been touched. (The principle is ADC sampling) 2. Returned to True after running.
It is displayed as a smiley face at this time, otherwise it will always show bitter face, so when you don't touch it, it will feel sad. (Wait! What kind of shy is this!!!!)

The effect is as follows:

.. image:: images/touched_io.gif

It should be noted that because our body (hand) has static electricity, it may be electrically connected to it, causing its expression to sometimes be very convulsive.

Light on and off
---------------------------

When we first started, we have already learned how to control the changes of the LED lights on the board, but that is what others have done for us, so today we will try it out automatically, how others do it, and become a regular after others. Say someone else’s child.

To this end, we have prepared the following common Led lamps, you will find that they are different in length, in order to distinguish between their positive and negative poles, where the positive pole is the long end, so the negative pole is the short end.

Tip: The intention of distinguishing between positive and negative poles is that when you are wiring, the positive pole of the component (LED) is connected to the positive pole (+) of the power supply, and the negative pole of the component (LED) is connected to the negative pole of the power supply (-).

.. image:: images/leds.jpg

Let's start with the first step. First light the lamp, that is, directly connect it (LED) to the power supply, then connect the big guy directly to the board.
3V and GND, 3V refers to the positive power supply (3V), GND refers to the negative power supply, also known as ground.

.. image:: images/led.gif

This will light up a light (note the positive and negative), but the light that is lit can not be controlled, it will only be bright, not extinguished.

I wanted to take another light to connect to compare, but we found a problem, the other lights are too short, so we exchanged the following, with our headlights to control, you can see that the lights are connected at this time. It won't light up.

.. image:: images/led_off.jpg

Then we use the following code to control its lighting and extinction, we can see that we use pin2 pin to control.

.. code:: python

   From microbit import *
   Pin2.write_digital(1)

You can see that it is lit up, which means that we can control its brightness. Is this consistent with the initial tutorial?

.. image:: images/led_on.jpg

Then we will add a Blink effect this time, using the following code.

.. code:: python

   From microbit import *

   While True:
       Pin2.write_digital(1)
       Sleep(200)
       Pin2.write_digital(0)
       Sleep(1000)

The effect is as follows:

.. image:: images/blink.gif

.. Note::

   1. Use the pin2 pin to output 1 , which will make the LED become high. It is simply assumed that there is voltage on this pin, and the effect is equivalent to directly connecting the positive terminal of the power supply. (In principle, it should be understood that a potential difference is formed between the two pins).
   
   2. First light it up, which is `pin2.write_digital(1)`, then use `sleep(200) ` to let the board rest for 200 milliseconds.

   3. Then turn it off, which is `pin2.write_digital(0)`, then rest for 1000 milliseconds, which is 1 second.

   4. Repeat the process above.
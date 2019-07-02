Lighting the LED light again
==============================================================

If Hello World is a religious programming start for software programmers, then for those who are hardware programmers, Blink Led, too, all hardware programming starts with lighting a light. . Therefore, we pay attention to the gradual progress, first a light, then a row of lights.

.. figure:: leds/ready.png

Light up the LED light on the GPIO
------------------------------------------------------

Enter repl mode
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. figure:: leds/into_repl.png

Manual input (you can also select the text to copy, right-click in the black box)

.. code:: python

      From machine import Pin

re-enter

.. code:: python

      Pin(18, Pin.OUT).value(1)

.. figure:: leds/light_up.png

Press the Enter key (Enter) to see that the light on the panel is lit.

.. figure:: leds/light_result.png

To further confirm that it is the light we control, enter

.. code:: python

      Pin(18, Pin.OUT).value(0)

.. figure:: leds/light_down.png

Then you can see that it is gone.

.. figure:: leds/light_restore.png

Use the mian.py file
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Prepare the following code into the main.py file. The difference from the previous one is that the effect is continuous. It will make the light be on, wait for a second and then go out. Since the effect is continuous, there is no way to pass the graph. Show the situation, so try it yourself.

.. code:: python

      From machine import Pin
      Import time
      Led = Pin(18, Pin.OUT) # get a led on gpio 18.
      Print('turn on')
      Led.value(1) # turn on
      Print('sleep 1s')
      Time.sleep(1) # sleep 1s
      Print('turn off')
      Led.value(0) # turn off

.. figure:: leds/mian_light.png

If the effect is not obvious, you can write an infinite loop to see the effect, pay attention to use \ ``Ctrl + C``\ to stop, otherwise you can not continue.

.. code:: python

      From machine import Pin
      Import time
      Led = Pin(18, Pin.OUT) # get a led on gpio 18.
      While True:
            Print('turn on')
            Led.value(1) # turn on
            Print('sleep 1s')
            Time.sleep(1) # sleep 1s
            Print('turn off')
            Led.value(0) # turn off
            Print('sleep 1s')
            Time.sleep(1) # sleep 1s

.. figure:: leds/blink_led.png

LED panel light that illuminates the panel (NeoPixel)
------------------------------------------------------

Prepare the following code into main.py

.. code:: python

      From pixel import Pixel
      View = Pixel()
      RGB = (10, 10, 10)
      View.LoadXY(2, 2, RGB)
      View.Show()

Use ``runfile main.py`` to execute.
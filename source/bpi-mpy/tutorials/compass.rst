Make a compass
==============================================================

Note: There is no magnetometer function on the 1.2 version.

This module gives you access to the built-in electronic compass (ie AK8963). The compass should be calibrated before using the compass, otherwise the reading may be wrong.

Calibrating the compass will cause the program to pause until the calibration is complete. The calibration consists of a small game that is calibrated by rotating the board in the air.

Function about compass
--------------------

.. function:: compass.calibrate()

Execute this function to start the calibration process, you will receive a guiding message, then I need to rotate the board and draw an inverted '8' or a circle in the air. (This action can refer to your mobile phone, the compass function of the phone. There will be a calibration step before use. This calibration process takes about 1 minute. You cannot execute other programs during calibration.
Prompt message

.. figure:: compass/prompt.png

.. function:: compass.is_calibrated ()

Returns True if the compass is successfully calibrated, otherwise returns False.

.. function:: compass.get_x ()

Returns the reading of the magnetic field strength on the x-axis, which is a positive or negative integer, depending on the direction of the magnetic field.

.. function:: compass.get_y ()

Returns the reading of the magnetic field strength on the y-axis, which is a positive or negative integer, depending on the direction of the magnetic field.

.. function:: compass.get_z ()

Returns the reading of the z-axis magnetic field strength, which is a positive or negative integer, depending on the direction of the magnetic field.

.. function:: compass.heading()

Give the compass heading calculated from the above readings as an integer in the range 0 to 360, indicating the angle in the clockwise direction, 0 in the 12 o'clock direction

.. function:: compass.get_field_strength()

Returns the size of the magnetic field around the device, which is an integer.

Experience the compass
--------------------

.. code:: python

   """
       Compass.py
       Creates a compass.
       The user will need to calibrate the compass first. The compass uses the
       Built-in clock images to display the position of the needle.

   """
   From microbit import *

   # Start calibrating
   Compass.calibrate()
   # Try to keep the needle pointed in (roughly) the correct direction
   While True:
       Sleep(100)
       Needle = ((15 - compass.heading()) // 30) % 12
       Display.show(Image.ALL_CLOCKS[needle])

In this example, the first step is to calibrate the electronic compass (mpu). After the calibration is complete, we can see that there is a compass on our led panel. It always points to the south no matter how we turn the board.
|compass|

.. |compass| image:: compass/compass.gif
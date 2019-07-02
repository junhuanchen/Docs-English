Get ambient temperature
==============================================================

The thermistor underneath this LED panel allows you to get the ambient temperature around you. Before using it, it is recommended to place the board under cooling and collect it again. Otherwise, the reading temperature will deviate from the surrounding temperature. Because the board will heat up, the heat source that has the most influence around it is the temperature of the board itself, so the environment The temperature will change to the temperature of the board.

Therefore, before the board has begun to heat up, the initial acquisition must be the ambient temperature, and then gradually become the board temperature.

Come and try it now.
---------------------------

.. code:: python

    From microbit import *

    While True:
         Temp = temperature() # get temperature °C
         Print(temp)
         Display.scroll(str(temp))
         Sleep(10000)

Measured contrast effect
---------------------------

LED panel display

.. figure:: temperature/tem.gif

REPL printed data

.. figure:: temperature/tem2.png

Temperature gun measured temperature

.. figure:: temperature/tem1.jpg
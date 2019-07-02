The easiest start
==============================================================

.. Hint::

    If a worker wants to do something good, he must first sharpen his tools.

    Make sure you have BPI-BIT ready and have :ref:`flash_mpy`.

    And get the simplest MicroPython editor from here: download:`mpy-editor <https://github.com/BPI-STEAM/mpy-editor>`.

Connect devices under Windows
---------------------------

When you plug in the device, you will be prompted to select the serial port of the device after opening the software. Click on COM4 as shown in the figure. If you disconnect the device, you can continue to click the Connect icon to reconnect.

.. image:: simple_use/ready.png

Run the code after confirming the connection
---------------------------

Copy and paste into the edit box, click Run, you can let the board display a smile::

    From microbit import *
    Display.show(Image.HAPPY)

As you can see, the board shows a smiley face and I have successfully run the MicroPython code.

.. image:: simple_use/display.png

.. Hint::

    The firmware is already compatible with microbit's Python code, so you can call most of the microbit functions directly.

This article shows you how to program with tools, but it's just the beginning, there are many basics to learn, such as learning to use more cases, or improving the programming tools used.
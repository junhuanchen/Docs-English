.. _flash_mpy:

Brush in MicroPython firmware
=========================================================== ===

For the first time, please burn the MicroPython firmware first. If you don't burn it, there is no MicroPython programming environment.

.. Hint::

    Please confirm that the driver has been installed and you have already know the name of your hardware serial port, for example: COM5, ttyUSB0.

.. toctree::
   :maxdepth: 2

   ../bpi-steam/driver

Under Windows
---------------------------

- Get a link to the programming tool from `BPI-BIT-MicroPython/release <https://github.com/BPI-STEAM/BPI-BIT-MicroPython/releases/tag/FlashTool>`_ with a domestic micro cloud The network disk is diverted.

- After downloading, open the `FlashMicroPython-*.zip` package and run the Flashtool.exe tool inside.

.. image:: flash_mpy/flash_mpy.png

- Please open the software after inserting the hardware first. This software will automatically run the programming. You can also directly click the Flash button to burn.

- You can also choose the serial port to burn. To upgrade the firmware, just replace the firmware.bin in the compressed package and re-burn it.

Under other systems
---------------------------

Please refer to other web tutorials. If you have special needs, you can submit a question or open an issue to the community.

.. Attention::

    If you have any questions, please go to the Chinese community <https://forum.banana-pi.org.cn/c/bpi-bit>`_ feedback.
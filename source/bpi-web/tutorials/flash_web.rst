Brush in the Webduino firmware
==============================================================

For the first time, please burn the Webduino firmware first. If you don't burn it, there is no Webduino hardware running environment.

.. Hint::

    Please confirm that the driver has been installed and you have already know the name of your hardware serial port, for example: COM5, ttyUSB0.

.. toctree::
   :maxdepth: 2

   ../bpi-steam/driver

Under Windows
---------------------------

- Get a link to the programming tool from `BPI-BIT-Webduino/release <https://github.com/BPI-STEAM/BPI-BIT-Webduino/releases/tag/FlashTool>`_ with a domestic micro cloud The network disk is diverted.

- After downloading, open the `FlashWebduino-*.zip` archive and run the Flashtool.exe tool inside.

.. image:: flash_web/flash_web.png

- Please open the software after inserting the hardware first, and the software will automatically run the programming.

- You can also choose the serial port to burn. To upgrade the firmware, just replace the firmware.bin in the compressed package and re-burn it.

Under other systems
---------------------------

Please refer to other web tutorials. If you have special needs, you can submit a question or open an issue to the community.

.. Hint::

    For the problem of displaying x after burning, please see this `Skip production test X <https://github.com/BPI-STEAM/BPI-BIT-WebDuino/issues/3>`_, more questions can be found in `中文Community <https://forum.banana-pi.org.cn/c/bpi-bit>`_ Feedback.
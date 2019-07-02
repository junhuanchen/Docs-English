Programming with Pycharm IDE
=========================================================== ===

It's time to switch to a top-level Python professional IDE. What do you think? This article will teach you how to write MicroPython and run it in Pycharm.

Get the intellij-MicroPython plugin
-------------------------------------------------- ----

Download here: download:`intellij-micropython <https://github.com/BPI-STEAM/BPI-BIT-MicroPython/releases/tag/pycharm>`.

You can view it here, `project home page <https://github.com/junhuanchen/intellij-micropython>`_.

Install pycharm community edition
---------------------------

Get `pycharm`_ using windows system `Click here to download 2019.1 version`_ (community version is free to use)

Once the installation is complete, you can open the following interface by default.

|image0|

Create a new project
---------------------------

Click Create New Project to bring up the following interface.

|image1|

If Python is not installed, it is the following interface.

|image2|

Finally, you can see that the project has been completed.

|image3|

Install the intellij-MicroPython plugin
---------------------------

|image4|

|image5|

|image6|

Hint: This version has been modified to the bottom of the mpfshell, and is not fully integrated into the official, so it still has the same name as the plugin of the main warehouse, so when the IDE prompts the plugin to be upgraded or other repairs, it will be replaced back to the original version. In the case of the situation, it is good to ignore it.

|image7|

Run a file
---------------------------

Once the plugin is installed, launch it in your project.

|image8|

You can find the above page by searching for ``MicroPython`` in the settings.

|image9|

Now start it, click on the setting, Enable MicroPython support.

|image10|

Select ESP8266 (ESP32) to configure the device type, and then click Detect to automatically determine the path (or name) of the board you are connected to. At this time, Detect will fail because the key dependencies have not been installed.

|image11|

When the automatic identification of the serial port fails, you need to fill in the serial port name (including the path) of your board, or other connection parameters, such as: ws: 192.168.1.1, 1234, which is the same as the opening of ``mpfshell``. of.

|image12|

At this point, the connection parameters of the board have been set. You can now create a new one at untitled.
For python files, the first time you use it, be sure to create a file to trigger the installation dependencies. After the installation is complete, you can use the auto-recognition serial port and other tools (Tools in the menu item).

|image13|

Write a ` `print(helloworld!)``\ in the code edit box on the right.

|image14|

When you use it for the first time, you will be prompted to install the dependencies, so you can download and install it automatically in the background by clicking the Install requirement of the message.

|image15|

Wait patiently for a while.

|image16|

The installation will be prompted.

|image17|

Now we can run the main.py file, right-click anywhere in the edit box and select Run ‘Flash main.py’ to automatically generate the run file configuration and run it on the board.

.. Attention::

    If the serial port connection does not appear on the Linux system, check whether the serial port has permission for the general user. If you are not sure, please check this command \ ``usermod -a -G dialout Username && sudo reboot``\ , Username refers to your Username, not Username.

|image18|

Can see the results of the operation as follows

|image19|

Use Mpfshell directly
---------------------------

The shortcuts for REPL and Mpfshell are available in MicroPython -> Run Mpfshell Tools.

|image20|

.. _pycharm: https://www.jetbrains.com/pycharm/
.. _Click here to download version 2019.1: https://download-cf.jetbrains.com/python/pycharm-community-2019.1.exe

.. |image0| image:: pycharm/03.png
.. |image1| image:: pycharm/05.png
.. |image2| image:: pycharm/04.png
.. |image3| image:: pycharm/06.png
.. |image4| image:: pycharm/07.png
.. |image5| image:: pycharm/08.png
.. |image6| image:: pycharm/29.jpg
.. |image7| image:: pycharm/09.png
.. |image8| image:: pycharm/10.png
.. |image9| image:: pycharm/11.png
.. |image10| image:: pycharm/12.png
.. |image11| image:: pycharm/13.png
.. |image12| image:: pycharm/14.png
.. |image13| image:: pycharm/15.png
.. |image14| image:: pycharm/16.png
.. |image15| image:: pycharm/17.png
.. |image16| image:: pycharm/18.png
.. |image17| image:: pycharm/19.png
.. |image18| image:: pycharm/20.png
.. |image19| image:: pycharm/21.png
.. |image20| image:: pycharm/22.png
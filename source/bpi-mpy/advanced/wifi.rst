Let the board connect to the Internet
==============================================================

.. Attention::

     After the 20190528 official firmware has been turned off the debug information, so you need to disable the following code, you can modify it in the boot.py content.
     
     .. code:: python

          Import esp
          Esp.osdebug(None)

Connect to a WIFI hotspot
---------------------------

After the firmware is powered on, after the panel LED is scrolled, the network will try to connect by default. You can notice that if the tool or artificial Ctrl + C stops, it will not be connected. You need to use the following code.

.. code:: python

    Import wifi # booy.py default enable
    Wifi.try_connect()

The effect is as shown below. The default boot.py will be called by default.
``import wifi``\ , so you can also call directly in REPL
``wifi.try_connect()``\.

.. image:: wifi/try_connect.png

In the default networking mode, if the network has never been configured, the board will automatically connect to the WIFI name initially.
``webduino.io`` Password ``webduino`` WIFI hotspot.

If there is no such hotspot nearby, \ ``no AP found``\ will be output, and this hotspot is prepared in advance in my environment, so I will get an IP address \ ``192.168.10.185``\ (pictured). Otherwise, the connection will be repeatedly outputted (this will not affect your input and output). If you do not want it to continue to connect to the network, you can manually enter \ ``wifi.close()``\
WIFI connection.

.. image:: wifi/got_ip.png

SmartConfig distribution network
---------------------------

Of course, your WIFI hotspot is not necessarily this, so you can now press the **A button** and release it during the LED scrolling process, it will automatically enter the distribution mode, and re-connect the board to other WIFI, help The board is connected to the specified WIFI, enter the distribution mode of \ ``SmartConfig``, the LED (18) will light up, the LED light shown in the legend.

.. image:: wifi/start_config.png

After reset, the LED of the board is lit.

You can confirm that you have entered the distribution mode. If necessary, you can also view the output corresponding information at the serial port at this time.

.. Attention::

     In this mode, the ``Mpfshell`` open will not work properly, but it can be accessed using other serial tools. This is because the board has been unable to respond to the REPL operation, and the REPL will continue to run when the distribution network is completed.

.. image:: wifi/smartconfig.png

If the tool software fails during the run, you can also use other serial tools to view the output information.

After confirming that you have entered the distribution mode, you need to use an Android phone to install the distribution software of `EspTouch`_. You can also search for the SmartConfig related software in the mobile application market.

.. Attention::

     Now the software is developing very fast. The software UI interface in the figure below has changed, but the function is unchanged. Please download EspTouch.APK to view and support reading the WIFI name after Android 9+.
     
     If you can't get it, go to the community and search for it.

.. image:: wifi/view_apk.png

Take ``Android-SmartConfig.apk`` as an example, first connect the phone to WIFI, then connect the board to the same WIFI, and then enter the password of the connected WIFI in the software, this will inform the board, how to connect To the WIFI.

.. image:: wifi/open_apk.png

Click the only button to start the distribution network, you can see that REPL has corresponding information output, and the board's LED
The lights will also change.

.. _EspTouch: https://github.com/EspressifApp/EspRelease/raw/master/EspTouch/esptouch.apk


Wait for a while, if the card is not successful in the distribution mode, it will automatically restart within two minutes. And when the distribution network is successful, the LED
The light will turn into **light **\ , at which point REPL will output the IP of the board connected to WIFI
The address is as follows: \ ``192.168.10.185``\, and it is worth noting that 3de1
Corresponding to the name of the board, this name will be used later.

.. image:: wifi/smc_apk.png

And on the phone, you will also see the IP address of the board, at this time the board has completed the network configuration.

.. image:: wifi/smc_finish.png

.. image:: wifi/apk_finish.png

Tip: If the distribution network fails, please follow the process below to solve the problem.

- Confirmed to enter the distribution network mode (SmartConfig)
- Confirm that the WIIFI hotspot password is correct
- Enter wifi.isconnected() to return True
- Confirm that the WIFI RF is 2.4Ghz (Important)

Modify the networking profile
---------------------------

When you fail to find the above distribution network, and can't find any solution, you can directly modify the network configuration file, that is, manually create or modify the WIFI name and password configuration file ``wifi_cfg, py``.

(The firmware will now automatically generate ``wifi_cfg,py``\ after calling wifi.start())

Prepare a ``wifi_cfg, py`` with the contents:

.. code:: python

    WIFI_SSID = 'Your WIFI hotspot name'
    WIFI_PSWD = 'Your WIFI Hotspot Password'
    HOST_NAME = 'Your board's network name' #Optional

(Now you can first ``get wifi_cfg.py`` to retrieve the configuration) and ``mpfshell``
Use ``put wifi_cfg.py`` in the same directory and replace it with the current WIFI connection configuration.

You can also manually enter the ‘wifi.smartcoinfig()’ in ``repl`` to manually start the distribution mode instead of using the button trigger at power-on.

Wireless use REPL
---------------------------

Note that before using, make sure that the application is allowed to pass through the network firewall, and the computer and the board are connected under the same network (under the same WIFI).

Before entering the ``repl`` input\ ``import webrepl_setup``\, start the network configuration process.

According to the steps, (e, 1234, y)

Start network service configuration (start input e, stop input d)
Set the network connection password (not less than 4 digits, you need to enter it twice, it is up to you, I just want to save trouble)
Is it necessary to restart the board (reset input y, otherwise enter n)

.. image:: wifi/webrepl.png

I already knew that the IP of the board is ``192.168.10.185``\. If you don't know, you can power it back, then use \ ``mpfshell`` and enter \ ``ws:192.168.10.185,1234`` \ , where \ ``,1234``\ is the connection password I have previously set (previous chapter), you can also not enter now, but will also prompt you to enter the password. (Note that the comma of the English input method)

.. image:: wifi/into_webrepl.png

You can see that the connection has been successful. At this time, the board can also be operated by wireless. You can also restart the reset and try again.

There are two tips for connecting failures:

The remote connection is not responding, prompt \ ``WebREPL Remote IP Does not respond``\. The analysis is that one may be a network different from the board, and the other may be blocked by various software or hardware firewalls.
The connection password is incorrect, prompt \ ``WebREPL Password Error``\, re-enter the password, maybe you are connected to someone else's board.
In the case of a problem, if you can't connect, use the cable to press Ctrl + D to reset the connection after soft reset, and then exit to change to a wireless connection.

.. image:: wifi/error_webrepl.png
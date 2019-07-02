Network foundation
==============

.. _network_base:

The MicroPython :mod:`network` module is used to configure the WiFi connection. There are two WiFi interfaces, STA mode is workstation mode (ESP32 is connected to the router),
AP mode provides access services (other devices connect to ESP32). For a discussion of MicroPython's network connection methods, check out the :mod:`network` module.

STA mode
-------

The board is packaged in a network-based module :ref:`MicroPython.wifi()<MicroPython.wifi>` Simplified wifi connection settings::

     From MicroPython import * #import MicroPython module

     Mywifi=wifi() #instantiate wifi class
     mywifi.connectWiFi("ssid","password") #WiFi connection, set ssid and password

.. Note::

     After instantiating wifi(), two objects ``sta`` and ``ap`` are built. The ``sta`` object is in workstation mode and is connected to the network via a router. ``ap`` is AP mode, providing wifi access.

After the connection is successful, the Repl serial port prints as follows:

     Connecting to network...
     Connecting to network...
     WiFi Connection Successful, Network Config:('192.168.0.2', '255.255.255.0', '192.168.0.1', '192.168.0.1')


Disconnect WiFi connection::

     mywifi.disconnectWiFi()

Check if the wifi connection has been established::

     Mywifi.sta.isconnected()

.. Note:: If a connection has been established, return ``True``, otherwise ``False``.

You can view the network settings in the following ways:

     Mywifi.sta.ifconfig()

.. Note:: Return value 4 tuples: (IP address, netmask, gateway, DNS)
     
When ``ifconfig()`` takes parameters, configure a static IP. E.g:

     Mywifi.sta.ifconfig(('192.168.0.4', '255.255.255.0', '192.168.0.1', '192.168.0.1'))

AP mode
-------

In addition to the STA mode to connect to the router wifi, the board can also use the AP mode to provide wifi access services.

::

     From MicroPython import wifi # Import the wifi class of the MicroPython module

     Mywifi=wifi() # instance wifi
     mywifi.enable_APWiFi("MicroPython-wifi", 13) # Configure and enable AP mode, the first parameter: wifi name, use channel

``wifi.enable_APWiFi(essid, channel=10)`` is used to configure and enable the AP mode function. The ``essid`` parameter is the wifi name, and the ``channel`` parameter is the wifi channel. After the AP mode is enabled, other boards or network devices can connect to the network for network communication.

.. Attention:: AP mode is not a hotspot feature similar to mobile phones, devices can connect to the Internet through hotspots. This needs attention.

----------------------------

Once WiFi is set up, the way to access the network is to use sockets.
A socket represents an endpoint on a network device that can continue to communicate when two sockets are connected together.
Internet protocols are built on top of sockets such as email (SMTP), Web (HTTP), telnet, ssh, and more.
Each of these protocols is assigned a specific port, which is just an integer. Given the IP address and port number, you can connect to the remote device and start communicating with it.

The next part of this tutorial will discuss how to use sockets to perform some common and useful network tasks.
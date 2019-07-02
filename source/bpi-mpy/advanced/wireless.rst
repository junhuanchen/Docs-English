Understanding wireless programming
==============================================================

Wired connection to the board has been a feature of the last century, so in the future development process, we support and try to go in the direction of wireless control, because various simple IoT devices will not leave a special one. The wired interface gives you connection to the computer control, for example: a smart-controlled light.

So at this time, wireless is used. It can be seen that when the board is connected to the Internet, we can directly help the board to access the Internet without inserting a computer, so this is the basis of wireless programming, to pass a simple The way to get the board into your network, you can control it.

Remote connection board
------------------------------------------------------

MicroPython's interactive interface uses Python
REPL, which is itself a re-operable system operating environment, is different from previous Linux. It is simple and easy to use. We are not enjoying the beauty brought by technology itself. If programming is only let Tools become difficult to use, so why continue programming?

REPL is a common interactive interface when wired, but on the wireless, it is launched.
`WebREPL`_\, as its name suggests, is the REPL in the cloud, as shown below:

.. figure:: wireless/webrepl.png

It can be seen that it can directly operate the board. Like the wired connection in the past, the response speed is very fast, and the difference in wired experience is not much different.

But this is obviously not enough, because this editor can only be used, but it is not easy to use, so I am also specializing in
Mpfshell is adapted to webrepl, that is, mpfshell based pycharm
Plug-ins, also support wireless programming, then all the features that feel good to use are used, as shown below.

.. figure:: wireless/pycharm.png

The running program is normal, but you need to be aware that the path settings of the two are not the same.

1. The webrepl standard path is ``ws://192.168.30.116:8266``\.

2. The path to mpfshell is
   ``ws:192.168.30.116,1234``\, the difference is that the latter allows the pass-through password, thus eliminating the connection authentication.

At this point, you can use it like wired in the past. If there is any problem during the period, you only need to restart the board. It will automatically connect to the network and open it.
Webrepl's support services.

In the future, you will use the battery-powered way to get out of the computer, so you can completely control it from the cable. Pay attention to the need to downgrade to the necessary time.
80Mhz, or there will be no electricity soon.

.. _WebREPL: http://micropython.org/webrepl

Remote management board
------------------------------------------------------

Although REPL can be used to program the board, we also need some additional network support services to make our board more enjoyable.

Here I will briefly introduce them.

FTP standard file system operation service
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Use the following code to start the FTP service

.. code:: python

   Import ftptiny
   ftptiny.FtpTiny().start()

.. figure:: wireless/ftp.png

WebDAV HTTP file system service (firmware temporarily removed after 20190312)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ ^^^^^^

Use the following code to start

.. code:: python

   Import webdav
   Webdav.start()

.. figure:: wireless/webdav.png

It is not the same as FTP, it uses port 80, access is used http, not ftp.

.. figure:: wireless/webdav_index.png

Hostname local domain name service
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This requires specific routing service support, for example: openwrt(linux).

It allows you to access the board instead of IP using hostname.lan (or direct hostname).

So you don't need to remember the IP address, but you define your own board name.

The hostname is saved in the wifi_cfg.py file below.

.. figure:: wireless/wifi_cfg.png

As shown in the figure of bit3D6D, the access method and test method are as follows.

.. figure:: wireless/hostname.png

And how to use it?

.. figure:: wireless/hostname_demo.png

And after you go to other places to change the network, you do not need to change the IP, just need to replace the connected WIFI
Configuration is fine.

MDns Reverse Domain Name Resolution Service
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you can't use the hostname to replace the IP memory, in addition to requesting the cloud service provider to register the DNS.
In addition to domain name resolution, there is still a way to reverse registration DNS, DNS
This is a server-specific management service, the underlying client can not be changed, so we use the domain name resolution of the initiative to obtain their own specific domain name.

To put it bluntly, the IP is turned into a custom network path, for example: hostname.local.

As shown in the following example, this also requires newer router support. As long as it is not a router of the last century, it basically supports this service, but does not deny it.
Routers that were produced 10 years ago may not necessarily have this MDns
Services, including computers, are not necessarily supported, and Windows requires additional installation of Bonjour Print Services
Features can be downloaded at \`here`_\.

Now I use the following code to configure the board to have the registration function of Mdns (all operations are based on networking conditions).

.. code:: python

   Try:
       Import network
       Mdns = network.mDNS()
       Mdns.start("bpibit", "MicroPython with mDNS")
       _ = mdns.addService('_ftp', '_tcp', 21, "MicroPython",
                           {"board": "ESP32", "service": "bpibit FTP File transfer", "passive": "True"})
       _ = mdns.addService('_telnet', '_tcp', 23, "MicroPython", {"board": "ESP32", "service": "bpibit Telnet REPL"})
       _ = mdns.addService('_http', '_tcp', 80, "MicroPython", {"board": "ESP32", "service": "bpibit Web server"})
       Print("mDNS started")
   Except Exception as e:
       Print("mDNS not started")

You can use ``bpibit.local`` instead of IP on your computer.
Address access it, as shown below, you can also take the name you want, change the code
``mdns.start("bpibit", "MicroPython with mDNS")``.

.. _Download here: https://support.apple.com/kb/DL999

.. figure:: wireless/mdns.png

But in fact, not only that, but also know what services it provides, etc. I used other software to view, the following is the result of viewing in the phone, you can see
MicroPython corresponds to the parameters of mdns.addService.

.. figure:: wireless/mdns_server.png

Look at the picture to see the information we provided when we registered, such as FTP and HTTP services.

Python dynamically builds web services
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Webdav implements a static, pure website that is not suitable for background Python
Website service for computing.

So `microwebsrv`_ is provided in the firmware to build a Python dynamic website.

After that, I will give a simple application example to illustrate, it will be similar to PHP.
Create a website service like a language.

.. _microwebsrv: https://microwebsrv.hc2.fr/
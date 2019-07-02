Try the MQTT app
==============================================================

What is MQTT?
---------------------------

MQTT is now an important part of the Internet of Things. Its service outer layer has complex security functions, and the architecture design is a data forwarding server. For example, an MQTT server can solve data of two types of systems of different types. Exchange, through the interface design of subscription and sending and receiving, so that it is only responsible for the exchange of data at both ends.

The transfer mode of the MQTT server can be thought of as entering a public chat room through their internal conventions. If you want to communicate with others, you can create a chat room (push), or you can join someone else's chat room ( Subscribe), the server, no matter how you communicate with each other, it will only help you to set up this chat room, you can exchange information freely, and thus complete the transmission.

for example:

Xiao Ming wants to send a message to Xiao Hong, then Xiao Ming can create a topic chat room to send (publish), then Xiaohong to subscribe to the topic (topic) chat room, so she can receive Xiao Ming The information, the old version of MQTT's chat room is open, you can join other people's topics, that is, other people can also receive Xiao Ming's message, but now the MQTT server allows you to define permissions in private (config) Let Xiao Ming's topic only Xiaohong can join.

.. image:: mqtt/process.png

.. Hint::

    Under such a framework, the code between us is the client code, so there is no need to write the receiving program of the server. As long as the two parties agree on the data protocol of the interface, the communication between them is too transparent. Therefore, its current security is also too dependent on surface authentication, and this authority and communication control will be improved in the future.

Prepare the MQTT server
---------------------------

Use a public MQTT server. If you don't have a server, click here to enter the `Communication Cat MQTT Server`_. Note that the ports of the WS and TCP servers are inconsistent, so you have to change the server port when you connect.

You can also test the MQTT service directly online, subscribe to your own topic information and send your own topic information.

.. image:: mqtt/online_demo.png

If you don't want to use the network's MQTT server, you can use the local `mosquitto Windows`_ server environment package and unzip directly to run mosquitto.exe, where the configuration file is mosquitto.conf.

.. image:: mqtt/config.png

After running normally, it will not display any data, otherwise it will report a flashback, so don't worry if it is working. If you need to confirm that it is working properly, you can try the following tutorial.

- `windows environment mosquitto environment to build and mqtt test `_

- `Windows installation mosquitto`_

- `MQTT teaching (2): Install MQTT server Mosquitto, Windows system articles `_

Start the MQTT client
---------------------------

Please confirm the network before you can start the MQTT service.

Now prepare the following code

.. code:: python

   Import wifi
   Wifi.start()

   Server_ip = "mq.tongxinmao.com" # Online public MQTT server
   Client_id = "umqtt_client" # Client ID, optionally defined, to identify the data that it sends.

   Import time

   From umqtt.robust import MQTTClient

   Try:
       # see https://github.com/micropython/micropython-lib/blob/master/umqtt.simple/umqtt/simple.py
       c = MQTTClient(client_id, server_ip, 18830) # Configure the connection. This is the server configuration of the communication cat. The port is 18830. The default is 1883.

       c.DEBUG = True # Output Debug information

       Def sub_cb(topic, msg):
           Print((topic, msg))
           C.publish(topic, msg) # No matter what subscription information is received, it is returned with the same subject and data.

       C.set_callback(sub_cb) # Receive callback processing for data that is subscribed to the remote.

       If not c.connect(clean_session=False):
           C.subscribe(b"foo_topic") # Subscribe to a topic of foo_topic (topic)

       C.publish(b"foo_topic", b"hello") # Send a hello string to the topic of foo_topic.

       While 1:
           # Let the chip run a little slower and easy to observe.
           Time.sleep(1)

           # Waiting to process data for MQTT
           If c.check_msg() is not None:
               C.wait_msg()

           # No other things can be done when the data can be processed.
           Else:
               Print('other operator')

   Finally:
       C.disconnect() # Debug the program to reopen the service, remember to close the line, otherwise the board will restart before you can continue.

.. _ communication cat MQTT server: http://www.tongxinmao.com/txm/webmqtt.php
.. _mosquitto Windows: https://github.com/BPI-STEAM/BPI-BIT-MicroPython/releases/tag/windows-mosquitto
.. _windows environment mosquitto environment to build and mqtt test: https://blog.csdn.net/pgpanda/article/details/51800865
.. _Windows install mosquitto: https://www.cnblogs.com/xhxljh/p/7307100.html
.. _MQTT teaching (2): Install MQTT server Mosquitto, Windows system articles: http://swf.com.tw/?p=1005

The above is a concrete example of MQTT, which should have the following effects.

1. The board will send a ``hello`` to the subscribed foo_topic theme.
   Data, users who subscribe to the topic on the web page at this time should get the data and display it.

2. The board subscribes to the foo_topic theme, so it will receive 1 `hello` previously sent by itself.
   Data, and then according to the code, it will send this received data back, so this time the board will be
   Receive and send data cyclically on the foo_topic theme.

3. If we are on the web side of the section to foo_topic
   If the subject sends data, the board will receive the data and display the corresponding data, as seen in the figure.
   ``11 22 3311`` data, pay attention to this time, your new data will also participate 2
   The loop mentioned in the output data.

.. image:: mqtt/online_test.png

If it is a web page, it will display the data you have sent in the board definition.

.. image:: mqtt/running.png
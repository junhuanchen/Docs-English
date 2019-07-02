.. _umqtt.simple:
:mod:`umqtt.simple`

Umqtt.simple module
==================================================

MQTT is a publish-subscribe "lightweight" messaging protocol for use over TCP/IP.
Provides a subscription/release mode that is simpler, lighter, and easier to use. For limited environments (low bandwidth, high network latency, and unstable network communication), it can be easily summarized for the Internet of Things.

.. Hint::

    This module is derived from ``MicroPython-lib`` : https://github.com/micropython/micropython-lib/tree/master/umqtt.simple

Build object
-------------

.. class:: MQTTClient(client_id, server, port=0, user=None, password=None, keepalive=0,ssl=False, ssl_params={})

    - ``client_id``
    - ``server``
    - ``port``
    - ``user``
    - ``password``
    - ``keepalive``
    - ``ssl``
    - ``ssl_params``

method
----------------

.. method:: MQTTClient.set_callback(f)

    - ``f`` - f(topic, msg) is the callback function, the first parameter is the subject received by ``topic``, and the second parameter is ``msg`` for the topic message.



Set a callback for incoming subscription messages

.. method:: MQTTClient.set_last_will(topic, msg, retain=False, qos=0)

Set the MQTT "last will" message. Should be called before connect().

.. method:: MQTTClient.connect( clean_session=True )

Connect to the server. Returns True if this connection uses a persistent session stored on the server (or False (default) if the clean_session = True parameter is used).

.. method:: MQTTClient.disconnect()

Disconnect from the server and release resources.

.. method:: MQTTClient.ping()

Ping server (response automatically by wait_msg())

.. method:: MQTTClient.publish(topic, msg, retain=False, qos=0)

make an announcement

.. method:: MQTTClient.subscribe(topic, qos=0)

Subscribe to topics

.. method:: MQTTClient.wait_msg()

Waiting for a server message. The subscription message will be passed to the callback set via set_callback() and any other messages will be processed internally.

.. method:: MQTTClient.check_msg()

Check if the server has pending messages. If yes, it is handled in the same way as wait_msg(), and if not, it returns immediately.


.. Attention::

    * wait_msg() and check_msg() are "main loop iteration" methods, blocking and non-blocking versions. Wait_msg() If you don't have any other foreground tasks to execute (ie your app only responds to subscribed MQTT messages), check_msg() If you also handle other foreground tasks, you should periodically call them in a loop.
    * Note that if you only post messages, you don't need to call wait_msg()/check_msg() or subscribe to the message.
    * QoS 0 and 1 are supported for both publish and subscribe. QoS2 is not supported to maintain a small code size. In addition to the ClientID, only the "clean session" parameter is currently supported for connection.
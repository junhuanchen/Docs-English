Socket-UDP
================

Introduction to UDP Protocol
---------

UDP (User Datagram Protocol) is a connectionless, unreliable, datagram-based transport layer communication protocol.

The UDP communication process is simpler than TCP. It does not require a copy of the three-way handshake and four wave hands, which means no connection.
Therefore, UDP transmission speed is faster than TCP, but it is easy to lose packets, the order of data arrival is not guaranteed, the lack of congestion control, and the principle of delivering the best effort, which is unreliable.

The following figure shows the interaction process between the server and the client UDP communication connection:

.. figure:: ../../images/tutorials/udpprincipal.png
    :scale: 100 %
    :align: center

    Socket UDP communication process

-----------------

UDP programming
--------

Usually, when I talk about network programming, it refers to TCP programming by default, which is the TCP method I mentioned in the previous section.
When the socket function creates a socket object, no parameters are given. The default is SOCK_STREAM, which is socket (socket.AF_INET, socket.SOCK_STREAM), which means creating a socket for streaming network communication.

``SOCK_STREAM`` is connection-oriented, that is, each connection must be created by ``connect`` before sending and receiving data. It is also bidirectional, that is, either party can send and receive data. The protocol itself provides some guarantee mechanisms to ensure that it is reliable. Ordered, that is, each packet arrives at the receiver in the order in which it was sent.

``SOCK_DGRAM`` is the network communication of the User Datagram Protocol. It is connectionless and unreliable because the communication parties do not know whether the other party has received the data after sending the data, and whether the data is received normally.
Any party can use the ``sendto`` to send data later, or use ``recvfrom`` to receive data. I don't care if the other party exists or not. It is characterized by faster communication speed. Everyone knows that TCP is going through three handshakes, but UDP is not.


UDP client
~~~~~~~~

The general steps of the UDP programming client are:

1. Create a UDP socket with the function socket (socket.AF_INET, socket.SOCK_DGRAM)
2. Set the socket property, using the function ``setsockopt()`` *optional*
3. Bind the IP address, port and other information to the socket, using the function ``bind()`` *optional*
4. Set the properties such as the IP address and port of the other party.
5. Send the data using the function ``sendto()``
6. Turn off the network connection

Example of a UDP client:

.. code-block:: python
    :linenos:

    From MicroPython import *
    Import socket
    
    Mywifi=wifi() # Create wifi object
    mywifi.connectWiFi("ssid","password") # Connect to the network
    Dst = ("192.168.0.3", 6000) # destination ip address and port number

    # caught exception, stop closing the socket if it is unexpectedly interrupted in the "try" code block
    Try:
        s = socket.socket(socket.AF_INET, socket.SOCK_DGRAM) # Create UDP sockets
        S.setsockopt(socket.SOL_SOCKET, socket.SO_REUSEADDR, 1) # Set socket properties

        While True:
            S.sendto(b'hello message from MicroPython\r\n',dst) # Send data to destination ip
            Sleep(2)

    # When catching an exception, close the socket, network
    Except:
        If (s):
            S.close()
        mywifi.disconnectWiFi()

.. image:: ../../images/tutorials/udpclient.gif
    :align: center

UDP server
~~~~~~~~

The general steps on the server side of UDP programming are:

1. Create a UDP socket with the function socket (socket.AF_INET, socket.SOCK_DGRAM)
2. Set the socket property, using the function ``setsockopt()`` *optional*
3. Bind the IP address, port, and other information to the socket, using the function ``bind()``.
4. Loop through the data, using the function ``recvfrom()``
5. Close the connection

Example of a UDP server:

.. code-block:: python
    :linenos:

    From MicroPython import *
    Import socket
    
    Mywifi=wifi() # Create wifi object
    mywifi.connectWiFi("ssid","password") # Connect to the network

    # caught exception, stop closing the socket if it is unexpectedly interrupted in the "try" code block
    Try:
        s = socket.socket(socket.AF_INET, socket.SOCK_DGRAM) # Create UDP sockets
        S.setsockopt(socket.SOL_SOCKET, socket.SO_REUSEADDR, 1) # Set socket properties
        Ip=mywifi.sta.ifconfig()[0] # Get the local ip address
        S.bind((ip,6000)) # bind ip and port number
        Print('waiting...')
        oled.DispChar("%s:6000" %ip,0,0)
        Oled.show()
        While True:
            Data,addr=s.recvfrom(1024) # Receive the data sent by the other party, the read byte is set to 1024 bytes, and the (data, addr) binary group is returned.
            Print('received:',data,'from',addr) #Print received data
            Oled.fill(0) #清屏
            oled.DispChar("%s" %data.decode(),0,15) # oledDisplay receiving content
            oled.DispChar("from%s" %addr[0],0,31)
            Oled.show()
            

    # When catching an exception, close the socket, network
    Except:
        If (s):
            S.close()
        mywifi.disconnectWiFi()

.. Note::

    The return value of the ``recvfrom()`` function is a tuple (bytes, address), where bytes is the received byte data, and address is the sender's IP address at the port number.
    Expressed in a binary group (host, port). Note that the return value of the recv() function is only bytes data. UDP, each time you send ``sendto()`` and receive data ``recvfrom``, you need to specify the address information in TCP programming. You do not need to call ``listen()`` and ``accept()``. .

.. Attention:: In the above example, use ``connectWiFi()`` to connect to the same router wifi. You can also use the ``enable_APWiFi()`` to enable the AP mode and build a wifi network to allow other devices to access it. This eliminates the need to rely on other router wifi networks.
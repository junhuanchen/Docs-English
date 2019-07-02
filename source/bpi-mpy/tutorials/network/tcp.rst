Socket-TCP
================


What is a socket?
-----

``Socket`` is an abstract concept of network programming. Usually I use a Socket to mean "open a network link", and open a Socket needs to know the IP address and port number of the target computer, and then specify the protocol type.

Introduction to TCP protocol
-----

The TCP protocol, Transmission Control Protocol (TCP) is a connection-oriented, reliable, byte stream-based transport layer communication protocol defined by IETF's RFC 793.

TCP communication requires three steps: creating a connection, transferring data, and terminating a connection. In the TCP communication model, before the communication starts, it is necessary to create a related connection before sending data, similar to "calling" in life.

When working, the socket divides the two sides of the connection into server and client, that is, C/S mode. The principle of TCP communication is as follows:

.. figure:: ../../images/tutorials/tcpprincipal.png
     :scale: 90 %
     :align: center

     Socket TCP communication process


---------------------------------

TCP programming
-----


This part of the tutorial will show you how to use TCP sockets as a client or server. For a more comprehensive use of the socket module, please refer to the :mod:`usocket` module.
The following tutorials require the use of TCP network debugging tools. The following is the IOS Network Test Utility**, which can be searched and installed in the APP Store. Please click the download for the Android system. :download:`Network Test Utility.apk </../docs/tools/com.jca.udpsendreceive.2.apk>`

Disclaimer: The TCP client (tcpClient) here is your computer or mobile phone, and the TCP server (tcpServer) is the MicroPython board.

TCP client
~~~~~~~~


The general steps of the TCP programming client are:

1. Create a socket with the function socket()
2. Set the socket property, use the functions setsockopt(), *optional*
3. Bind the IP address, port, and other information to the socket, using the function bind(), *optional*
4. Set the properties such as the IP address and port of the other party to connect to.
5. Connect to the server, use the function connect()
6. Send and receive data, using the functions send() and recv(), or read() and write()
7. Turn off the network connection


tcpClient example:

.. code-block:: python
     :linenos:

     Import socket
     From MicroPython import *

     Host = "172.25.1.63" #TCP server IP address
     Port = 5001 # TCP server port
     s=None

     Mywifi=wifi() # Create wifi class


     # caught exception, stop closing the socket if it is unexpectedly interrupted in the "try" code block
     Try:
          mywifi.connectWiFi("ssid","password") #WiFi connection, set ssid and password
          # mywifi.enable_APWiFi("wifi_name",13) # You can also enable AP mode and build your own wifi network.
          Ip=mywifi.sta.ifconfig()[0] # Get the local IP address
          s = socket.socket(socket.AF_INET, socket.SOCK_STREAM) # Create a TCP socket, or you can give no parameters. The default is TCP communication mode
          S.setsockopt(socket.SOL_SOCKET, socket.SO_REUSEADDR, 1) # Set the socket property
          S.connect((host,port)) # Set the IP and port of the server to be connected and connect
          S.send("hello MicroPython, I am TCP Client") # Send data to the server

          While True:
                Data = s.recv(1024) # Read 1024 bytes of data from the server-side socket
                If(len(data) == 0): # If the received data is 0 bytes, close the socket
                     Print("close socket")
                     S.close()
                     Break
                Print(data)
                Data=data.decode('utf-8') # decode the string in UTF-8 encoding
                Oled.fill(0) #清屏
                oled.DispChar(data,0,0) # oledDisplay socket receiving data
                Oled.show() # show
                S.send(data) # Send the received data to the server

     # When catching an exception, close the socket, network
     Except:
          If (s):
                S.close()
          mywifi.disconnectWiFi()

.. Attention::

     Since it is transmitted in bytes in the network, it is necessary to pay attention to data encoding and decoding.

.. Attention:: In the above example, use ``connectWiFi()`` to connect to the same router wifi. You can also use the ``enable_APWiFi()`` to enable the AP mode and build a wifi network to allow other devices to access it.

First, the board and mobile phone must be connected to the same LAN. Open Network Test Utility and go to the TCP Server interface.
TCP Server IP selects the IP address of the mobile phone in the network. The port number can be set from 0 to 65535. Then, click on Listen and start listening to the port.
In the program, set the TCP server IP address ``host`` and port number ``port`` selected above to restart the running program.

When the connection to the server is successful, the TCP Server will receive the text ``hello MicroPython, I am TCP Client`` sent by the client. At this point, you send text to the client in TCP Server, the board will
Receive the text and display the text on the oled screen.


.. image:: ../../images/tutorials/socket_1.gif
    

TCP server
~~~~~~~~


The general steps of the TCP programming server are:

1. Create a socket with the function socket()
2. Set the socket property, use the functions setsockopt(), *optional*
3. Bind the IP address, port, and other information to the socket, using the function bind()
4. Turn on the listener and set the maximum number of listeners, use the function listen()
5. Wait for the client to request a connection with the function accept()
6. Send and receive data, using the functions send() and recv(), or read() and write()
7. Turn off the network connection



tcpServer example:

.. code-block:: python
     :linenos:

     Import socket
     From MicroPython import *

     Port=5001 #TCP server port, range0~65535
     listenSocket=None

     Mywifi=wifi() # Create wifi class

     # caught exception, stop closing the socket if it is unexpectedly interrupted in the "try" code block
     Try:
          mywifi.connectWiFi("ssid","password") #WiFi connection, set ssid and password
          # mywifi.enable_APWiFi("wifi_name",13) # You can also enable AP mode and build your own wifi network.
          Ip= mywifi.sta.ifconfig()[0] # Get the local IP address
          listenSocket = socket.socket(socket.AF_INET, socket.SOCK_STREAM) # Create a socket, the default parameter is TCP communication mode.
          listenSocket.setsockopt(socket.SOL_SOCKET, socket.SO_REUSEADDR, 1) # Set socket property parameters
          listenSocket.bind((ip,port)) # bind ip and port
          listenSocket.listen(3) # Start listening and set the maximum number of connections
          Print ('tcp waiting...')
          oled.DispChar("%s:%s" %(ip,port),0,0) # oled screen shows the local server ip and port
          oled.DispChar('accepting.....',0,16)
          Oled.show()

          While True:
                Print("accepting.....")
                Conn, addr = listenSocket.accept() # Block, wait for the client's request to connect, if there is a new client to connect to the server, then a new socket will be returned to serve this client specifically
                Print(addr,"connected")
          
                While True:
                     Data = conn.recv(1024) # Receive the data sent by the other party, the read byte is set to 1024 bytes.
                     If(len(data) == 0):
                          Print("close socket")
                          Conn.close() # Close the socket if the received data is 0 bytes
                          Break
                     Data_utf=data.decode() # Received byte stream to decode the string in utf8 encoding
                     Print(data_utf)
                     oled.DispChar(data_utf,0,48) # will display the received text oled
                     Oled.show()
                     Oled.fill_rect(0,48,128,16,0) # Partial clear screen
                     Conn.send(data) # return data to the client

     # When catching an exception, close the socket, network
     Except:
          If(listenSocket):
                listenSocket.close()
          mywifi.disconnectWiFi()

.. Attention:: In the above example, use ``connectWiFi()`` to connect to the same router wifi. You can also use the ``enable_APWiFi()`` to enable the AP mode and build a wifi network to allow other devices to access it.

First, the board and mobile phone must be connected to the same LAN. The board restarts the running program, and the TCP server waits for the client connection request. Open Network Test Utility, enter the "TCP Client" interface, fill in the Remote host and port, ie ``socket.blind(ip,port)``
IP address and port. After the Connect connection is successful, the text is sent, and the board receives the text display to the oled screen and returns to the TCP Client. You can see the text from Client->Server, Server->Client on the phone receiving interface.


.. image:: ../../images/tutorials/socket_2.gif
     :scale: 60 %
     :align: center
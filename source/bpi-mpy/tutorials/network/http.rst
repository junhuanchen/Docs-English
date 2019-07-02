HTTP
=======

HTTP is a client/server (C/S) based architectural model that exchanges information over a reliable link and is a stateless request/response protocol.

An HTTP "client" is an application (web browser or any other client) that achieves the purpose of sending one or more HTTP requests to the server by connecting to the server.

HTTP GET request
----------------




The following example shows how to download a web page. HTTP uses port 80, you first need to send a "GET" request to download anything. As part of the request, you need to specify which page to retrieve.

Let me define a function that can download and print URLs:

    Import socket

    Def http_get(url):
        _, _, host, path = url.split('/', 3)
        Addr = socket.getaddrinfo(host, 80)[0][-1]
        s = socket.socket()
        S.connect(addr)
        S.send(bytes('GET /%s HTTP/1.0\r\nHost: %s\r\n\r\n' % (path, host), 'utf8'))
        While True:
            Data = s.recv(100)
            If data:
                Print(str(data, 'utf8'), end='')
            Else:
                Break
        S.close()

.. Hint::

    When using the socket module, please connect to wifi first and make sure you can access the internet. For information on how to connect to wifi, please see the previous section :ref:`config wifi<network_base>`.

Then you can try:

    >>> http_get('http://micropython.org/ks/test.html')


At this point, the html page is received and printed to the terminal.



HTTP Server
----------------

In the following example, the board acts as an HTTP server and can access the onboard light sensor using a browser:

    Import socket
    Import network,time
    From MicroPython import *

    Mywifi=wifi() #instantiate wifi class

    mywifi.connectWiFi("ssid","password") #WiFi connection, set ssid and password

    CONTENT = b"""\
    HTTP/1.0 200 OK

    <meta charset="utf-8">
    Welcome to MicroPython! Your light sensor value is: %d
    """

    Def main():
        s = socket.socket()
        Ai = socket.getaddrinfo(mywifi.sta.ifconfig()[0], 80)
        Print("Bind address info:", ai)
        Addr = ai[0][-1]
        S.setsockopt(socket.SOL_SOCKET, socket.SO_REUSEADDR, 1)
        S.bind(addr)
        S.listen(5)
        Print("Listening, connect your browser to http://%s:80/" %addr[0])
        oled.DispChar('Connect your browser',0,0,) #oledDisplay board ip address
        oled.DispChar('http://%s' %addr[0],0,16)
        Oled.show()
        While True:
            Res = s.accept()
            Client_s = res[0]
            Client_addr = res[1]
            Print("Client address:", client_addr)
            Print("Client socket:", client_s)
            Req = client_s.recv(4096)
            Print("Request:")
            Print(req)
            Client_s.send(CONTENT % light.read())
            Client_s.close()




Run main: in the REPL:

    >>> main()

.. image:: ../../images/tutorials/http_1.png


Connect your mobile phone or laptop to the same wifi so that it is on the same LAN. Press the print prompt or oled screen to display ip, use the browser to access the board sub-host IP address.

.. image:: ../../images/tutorials/http_2.png
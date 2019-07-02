JSON analysis
=======

JSON (JavaScript Object Notation) is a lightweight data exchange format. The use of text format completely independent of the programming language to store and represent data, easy to read and write, and easy to machine parsing and generation, so it is widely used in the Internet.

In Python, json and dict are very similar, both in the form of key-value, and json and dict can be easily transferred through the :mod:`json` module.

* json: is a data format, is a pure string, the essence is a file organization, such as txt, csv, doc, docx, xls, xlsx files, etc. that you are familiar with.

* dict: is a data structure, such as list list, collection set, string str, array array.

Network acquisition JSON analysis
---------------

The http protocol uses the request/response model, the browser or client makes the request, and the server gives the response.

For example, if I want to get information such as IP address from the open interface of http://ip-api.com/json/, I will enter the address directly into the browser and you can see:

.. image:: ../../images/tutorials/httpjson.png
    :align: center
    :scale: 100 %

This is a json array containing information such as the IP address. By accessing this url, we get the information and return the string text. We can use the ujson.loads(str) string to generate the dict dictionary type, so we can directly read the key (key) to get the corresponding value (value).

Example: Display some information on the website on the OLED display
::
    From MicroPython import*
    Import json
    Import urequests # urequests module is a module for network access

    Mywifi=wifi()
    mywifi.connectWiFi('yourESSID', 'yourpassword') #Connect to WiFi network

    Url_ip ="http://ip-api.com/json/" #Add request address

    Rsp=urequests.get(url_ip) #send get request

    ipJson=rsp.text

    ipDict=json.loads(ipJson)

    oled.DispChar('Country: %s' % ipDict['country'],0,5) #Show country information on OLED display
    Oled.show()

    oled.DispChar('City: %s' % ipDict['city'],0,25) #Show city information to OLED display
    Oled.show()

    oled.DispChar('IP:%s' % ipDict['query'],0,45) #Display IP address information on the OLED display
    Oled.show()

.. image:: ../../images/tutorials/json.jpg
    :align: center
    :scale: 70 %


We analyze it step by step in the interactive programming environment of the REPL to see the results more intuitively.

Import MicroPython, json, urequests modules before use:

    >>> from MicroPython import*
    >>> import json
    >>> import urequests

To connect to your WiFi network, you need to set your WiFi name and password:

    >>> mywifi=wifi()
    >>> mywifi.connectWiFi('yourESSID', 'yourpassword')
    Connecting to network...
    Connecting to network...
    Connecting to network...
    WiFi Connection Successful, Network Config:('','','','')

Add the request address, send a get request, and get the data returned by the third-party interface of the webpage:

    >>> url_ip ="http://ip-api.com/json/"
    >>> rsp=urequests.get(url_ip)

The obtained data is returned as json data text format, printout, we can see the returned data::

    >>> ipJson=rsp.text
    >>> print(jpJson)
    {"as":"AS56040 China Mobile Communications Corporation","city":"Guangzhou","country":"China","countryCode":"CN","isp":"China Mobile communications corporation","lat ":23.1292,"lon":113.264,"org":"China Mobile","query":"120.234.223.173","region":"GD","regionName":"Guangdong","status":" Success","timezone":"Asia/Shanghai","zip":""}

.. Note::

    Rsp.text returns the format of the json data text.

Convert the acquired data to the dict dictionary type, print out the output, we can see the returned data::

    >>> ipDict=json.loads(ipJson)
    >>> print(ipDict)
    {'countryCode': 'CN', 'lon': 113.264, 'regionName': 'Guangdong', 'query': '120.234.223.173', 'city': 'Guangzhou', 'status': 'success', ' Org': 'China Mobile', 'timezone': 'Asia/Shanghai', 'region': 'GD', 'lat': 23.1292, 'isp': 'China Mobile communications corporation', 'as': 'AS56040 China Mobile Communications Corporation', 'zip': '', 'country': 'China'}

.. Note::

    Json.loads(str) parses the JSON string and returns the object.

We can type the keyword (key) in the dict dictionary to get the corresponding information value (such as city, IP address::

    >>> ipDict['city']
    'Guangzhou'
    >>> ipDict['query']
    '120.234.223.173'
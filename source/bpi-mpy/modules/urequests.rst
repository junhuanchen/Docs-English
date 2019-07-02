.. _urequests:
:mod:`urequests`

Urequests module
=================================

I used the socket library before. This is a good tool for getting started. It is helpful to understand the basic concepts of crawlers and master the process of crawler crawling.
After getting started, we need to learn some more advanced content and tools to facilitate our crawling.
Then this section will briefly introduce the basic usage of the urequests library.

Response class
---------

.. class:: Response(s)

The object of the Response class, which contains the server's response to the HTTP request.

    - ``s``-ussl object

method
---------

.. method:: close()

Close the socket.

.. decorator:: content

Returns the content of the response, in bytes.

.. decorator:: text

The content of the response is returned as text, encoded as unicode.

.. method:: json()

Returns the response's json encoded content and converts to the dict type.

method
---------

.. method:: request(method, url, data=None, json=None, headers={},params=None)

Send an HTTP request to the server.

    - ``method`` - the HTTP method to use
    - ``url`` - the URL to send
    - ``data`` - to be attached to the body of the request. If a dictionary or tuple list is provided, the form will be encoded.
    - ``json`` - json is used to attach to the body of the request.
    - ``headers`` - the header dictionary to be sent.
    - ``params`` - the URL parameter attached to the URL. If a dictionary or tuple list is provided, the form will be encoded.

.. method:: head(url, **kw)

Send a HEAD request and return the Response object.

    - ``url`` - the URL of the Request object
    - ``**kw`` - the parameters of the request method.

.. method:: get(url, **kw)

Send a GET request and return the Response object.

    - ``url`` - the URL of the Request object
    - ``**kw`` - the parameters of the request method.

.. method:: post(url, **kw)

Send a POST request and return a Response object.

    - ``url`` - the URL of the Request object
    - ``**kw`` - the parameters of the request method.
    

.. method:: put(url, **kw)

Send a PUT request and return a Response object.

    - ``url`` - the URL of the Request object
    - ``**kw`` - the parameters of the request method.
    
.. method:: patch(url, **kw)

Send a PATCH request and return a Response object.

    - ``url`` - the URL of the Request object
    - ``**kw`` - the parameters of the request method.


    
.. method:: delete(url, **kw)

Send a DELETE request. , return the Response object.

    - ``url`` - the URL of the Request object
    - ``**kw`` - the parameters of the request method.
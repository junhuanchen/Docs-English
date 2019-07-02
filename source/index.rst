.. Introduction to BPI-STEAM documentation master file, created by
    Sphinx-quickstart on Sun May 26 22:43:43 2019.
    You can adapt this file completely to your liking, but it should at least
    Contain the root `toctree` directive.

Welcome to BPI-STEAM documentation!
==============================================================

.. Hint::

    Welcome to the user documentation for BPI-STEAM, which is hosted on the `Github BPI-STEAM <https://github.com/BPI-STEAM>`_ open source organization.

.. Attention::

    Due to the rapid development of open source, the English reference document can be searched in the document, which is helpful for developers to learn and consult the API in the future, and cannot fully Chinese content. Please understand.

I will introduce you to the basic information of BPI-BIT.

.. image:: _static/facade.gif

BPI-BIT is an open source STEAM education product based on ESP32 high performance chip and compatible with micro:bit design.

.. toctree::
    :maxdepth: 2
    :caption: BPI-BIT
    
    bpi-steam/readme
    bpi-steam/driver

Programming with Webduino
---------------------------

By programming the Webduino firmware, users can use Webduino Blockly for online programming.

.. toctree::
    :maxdepth: 2
    :caption: Webduino
    
    bpi-web/release
    bpi-web/tutorials/index
    bpi-web/advanced/index
    bpi-web/modules/index

Just look at the cloud and host your code at any time with the browser, and with the fun plug-in system and multi-language environment on Github, enjoy the world's popular building blocks programming!

Programming with MicroPython
---------------------------

By programming MicroPython firmware, users can program in the world's most popular Python language.

With the support of professional IDE (such as: VsCode, PyCharm), you can easily transfer the code from the computer to the board to experience the fun of program creation!

.. toctree::
    :maxdepth: 2
    :caption: MicroPython

    bpi-mpy/release
    bpi-mpy/tutorials/index
    bpi-mpy/advanced/index
    bpi-mpy/samples/index
    bpi-mpy/modules/index
    micropython/docs/index

Programming with Arduino
---------------------------

.. Hint::

    Arduino will not elaborate on too much basic content, please have your own language development foundation for C/C++.

BPI-BIT provides the software tools and best practices for getting started with Arduino, which will be your minimum barrier to entry into embedded professional development.

.. toctree::
    :maxdepth: 2
    :caption: Arduino
    
    bpi-adu/tutorials/index
    bpi-adu/advanced/index
    bpi-adu/modules/index

Expansion board support
---------------------------

BPI-BIT is designed to be compatible with microbit-compatible base hardware. You can view the following supported Microbit expansion boards or expand applications based on the expansion board design.

.. toctree::
    :maxdepth: 2
    :caption: expansion board

.. image:: _static/footer.png

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
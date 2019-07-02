.. _digital_io:

Digital IO
===============

This section describes how to use the digital I/O pins of the board's I/O pins. A pin is the way a board communicates with external devices connected to it. The board can be extended and connected to control or read other components or modules through the expansion board.

.. Attention::

     Except for P2 (digital input only) P3, P4, P10, other pins can use digital input and output modes. For a more detailed explanation, please see the :ref:`board subinterface pin description <MicroPythonPindesc>`.


Digital input
------------------

First, start by how to read the digital input of the pin. The following uses the built-in button a of the board as the key input:

     From MicroPython import * # Import MicroPython module

     P5=MicroPythonPin(5,PinMode.IN) # Instantiate MicroPythonPin, set button a pin (P5) to "PinMode.IN" mode

     While True:
          Value=p5.read_digital() # Read the digital input of the P5 pin
          oled.DispChar("Button_a:%d" %value,30,20) # Display the read value to oled
          Oled.show() # Refresh
          Oled.fill(0) #清屏

.. Note::

     At this point, you can press the button a button to see the "press" and "not pressed" readings. Since the button a circuit is pulled up, the output is high when "not pressed" and low when "pressed".
     
::

     From MicroPython import *
     P5=MicroPythonPin(5,PinMode.IN)
     

Before using, be sure to import the MicroPython module before using it.

Instantiate the pin object and set the mode. The ``MicroPythonPin(pin, mode=PinMode.IN, pull=None)`` class is used here.
``pin`` is the pin you want to access. If mode is not specified, the default is ``PinMode.IN``. If pull is not specified, the default is ``None``.

::

     P5.read_digital()

.. Note:: Use read_digital() to return the level value of the pin. High level (1), low level (0).


Digital output
------------------

The following is a simple drive to drive external LED lights::

     From MicroPython import * # Import MicroPython module

     P0=MicroPythonPin(0,PinMode.OUT) # Instantiate MicroPythonPin, set P0 to "PinMode.OUT" mode

     While True:
          P0.write_digital(1) # P0 write high
          Sleep(1) #时间
          P0.write_digital(0) # P0 write high
          Sleep(1) #时间


.. admonition:: Material, connection method

     A breadboard, an LED light, a MicroPython expansion board, and a DuPont line are required. The positive pole of the LED light is connected to the P0 pin of the board, and the negative pole of the LED is connected to the GND of the board.

.. image:: ../../images/tutorials/blink.gif

::

     P0=MicroPythonPin(0,PinMode.OUT)


.. Note::

     ``MicroPythonPin`` is instantiated. ``mode`` is set to ``PinMode.OUT`` digital output mode.

Write high and low level to P0 pin::

     P0.write_digital(1)
     P0.write_digital(0)

.. Note::

     Write a high or low level to the pin using the ``write_digital(value)`` method. Where ``value`` is the level value, "1" represents the high level, and "0" represents the low level.


External Interrupt
---------

.. admonition:: What is an interrupt?

     During the running of the program, the system has a situation that must be processed immediately by the CPU. At this time, the process in which the CPU temporarily suspends the execution of the program and processes the new situation is called an interrupt.
     When it is needed, the CPU must pause the current thing, handle other things, and go back to the execution of the pause.

The hardware interrupt is triggered when the input pin changes level, and the trigger executes the interrupt handler. You can define a callback function to do some of the work of breaking the response. The pin interrupt is used in the same way as the board's a, b button interrupts.

The following uses the built-in button a (P5 pin) as an input interrupt. When the button A is pressed, the buzzer sounds::

     From MicroPython import * # Import MicroPython module
     Import music # import music module
     P5=MicroPythonPin(5,PinMode.IN) # Instantiate MicroPythonPin and set P5 to "PinMode.IN" mode

     Def BuzzOn(_): # Define the callback function for the interrupt
          Music.play(music.BA_DING, wait=False)

     P5.irq(trigger=Pin.IRQ_FALLING,handler=BuzzOn) # Set the callback function for P5 pin interrupt

.. Hint::

     The effect is the same as when the ``button_a.irq()`` button is interrupted. The button_a interrupt is also used to ``Pin.irq``.


I first instantiate MicroPythonPin and configure the P5 pin as ``PinMode.IN`` ::

     P5=MicroPythonPin(5,PinMode.IN)

Define callback function:

     Def BuzzOn(_):
          Music.play(music.BA_DING, wait=False)

.. Note::

    The callback function, ** must contain a parameter **, otherwise it can not be used, the above ``BuzzOn()`` defines the callback function, the parameter is ``_``, you can define this parameter arbitrarily.


Finally we need to tell the pin when to fire, and the function that is called when the event is detected::

     P5.irq(trigger=Pin.IRQ_FALLING,handler=BuzzOn)

.. Note::

     We set P5 to trigger ``Pin.IRQ_FALLING`` only on the falling edge (when it goes from high to low). Set callback function
     Handler="You define the callback function for interrupt handling". For a more detailed triggering method, please see :ref:`MicroPythonPin.irq <MicroPythonPin.irq>` .
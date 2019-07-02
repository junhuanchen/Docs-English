Analog IO
===============

This section describes how to use the analog input and output of the board pins. A pin is how your board communicates with external devices connected to it. The board can be extended and connected to control or read other components or modules through the expansion board.

.. Attention::

    You can refer to the :ref:`board subinterface pin description <MicroPythonPindesc>` for the available analog pins.


.. _analog_in:

Analog input
--------

The analog input pins available for the board are **P0**, **P1**, **P2**, **P3**, P4, P10, where P4 and P10 are respectively used by the board's light and microphone sensors. use.


.. admonition:: What is an analog input?

    The analog input is the conversion of an analog signal to a digital signal, referred to as the ADC.



The following is to read the analog input using the P0 pin:

    From MicroPython import * # Import MicroPython module

    P0=MicroPythonPin(0,PinMode.ANALOG) # Instantiate MicroPythonPin and set P0 to "PinMode.ANALOG" mode
    While True:
         Value=p0.read_analog() # Read P0 pin analog
         oled.DispChar("analog:%d" %value,30,20)
         Oled.show()
         Oled.fill(0)


::
    
    From MicroPython import *
    P0=MicroPythonPin(0,PinMode.ANALOG)

.. Note::

    ``MicroPythonPin`` is instantiated. ``mode`` is set to ``PinMode.ANALOG`` analog input mode.



Read analog input::

    P0.read_analog()

.. Note::

    Because the adc sample data width is 12bit, the full scale is 4095.


EXT alligator clip
+++++++++

Next, you can connect resistive components (such as light-sensitive, thermistor) to the board's ``EXT`` and ``GND`` pads through the crocodile clip line to measure the sensor's input value change...


The EXT connection is the P3 pin of the board::

    From MicroPython import * # Import MicroPython module

         P3=MicroPythonPin(3,PinMode.ANALOG) # Instantiate MicroPythonPin and set P3 to "PinMode.ANALOG" mode
         While True:
                Value=p3.read_analog() # Read EXT(P3) pin analog
                oled.DispChar("analog:%d" %value,30,20)
                Oled.show()
                Oled.fill(0)

.. image:: ../../images/tutorials/ext.png
    :width: 180
    :align: center


Analog output
--------

.. admonition:: What is an analog output?

    The board's pins cannot output analog signals like an audio amplifier - by modulating the voltage on the pins. These pins can only enable a full 3.3V output or pull it down to 0V.
    However, it is still possible to control the brightness of the LED or the speed of the motor by turning the voltage on and off very quickly, and to control its turn-on time and turn-off time.
    This technique is called Pulse Width Modulation (PWM), which is the method of ``write_analog``.


Output a PWM signal of a voltage::

    From MicroPython import * # Import MicroPython module

    P0=MicroPythonPin(0,PinMode.PWM) # Instantiate MicroPythonPin, set P0 to "PinMode.PWM" mode

    Voltage=2.0 # voltage 2V
    P0.write_analog(int(voltage/3.3*1023)) #calculate the duty cycle of the corresponding voltage PWM

.. Note::

    * ``value`` in ``write_analog(value)`` is the duty cycle of the PWM signal.
    * Since the IO pin voltage is 3.3V, I need an output voltage of 2V. Therefore, the mapped value is 2/3*1023.
    * Since the calculated floating point number, we also need to use ``int()`` to convert to integer.

.. image:: ../../images/tutorials/pwm.png

You can see a graph of three different PWM signals on it. They all have the same period (and therefore frequency), but they have different duty cycles.

* The first one produced is ``write_analog(511)`` because it has exactly 50% duty cycle - power is in half the time, and in half the time. The result is that the total energy of the signal is the same as if it were 1.65V instead of 3.3V.

* The second signal has a 25% duty cycle and can be ``write_analog(255)``. It has a similar effect, as if it were outputting 0.825V on this pin.

* The third signal has a 75% duty cycle and can generate ``write_analog(767)``. Its energy is three times that of the second signal, which is equivalent to 2.475V on the second pin.
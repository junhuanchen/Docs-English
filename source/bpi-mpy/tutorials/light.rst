Photosensitive and gesture detection
==============================================================

Understanding photosensitive sensors
---------------------------

Careful classmates may have discovered that there are two small things on the bpibit board. Yes, these two small things are photosensitive sensors. It is a light-sensitive sensor that converts the intensity of light into a voltage through a sampling circuit.

.. image:: light/bpi.png

Its model number is PTSMD021.

.. image:: light/ptsmd021.png

Get ambient light intensity
---------------------------

There is a light built-in module in the firmware. I can easily get the intensity of the light by calling the function in this module.

.. code:: python

    Import light
    From time import sleep_ms
    R = light.Intensity(39)
    L = light.Intensity(36)

    While True:
        Print('R=',R.read())
        Print('L=',L.read())
        Sleep_ms(1000)

We want to use the light module, we must first import this module, you can use import light
To import.

Similarly, we need a delay function so we need to import the sleep_ms() function.

So what does light.Intensity(39) and light.Intensity(36) mean? Actually, what is done here is to initialize the photosensor. But why is it 36 ​​and 39? This question is left in the API documentation of the built-in module.

After the initialization is complete, we can call the read() function to get the intensity of the light. The read() function returns a value of 0 1000, which indicates the current approximate light intensity.

We can print the data from the serial port REPL at this time. The REPL tool used in the figure is ( `mpfshell-lite <https://github.com/BPI-STEAM/mpfshell-lite>`_ ).

.. image:: light/message.png

Sensitive recognition gesture
---------------------------

From the above we already know that there are two light sensors on our board, then we use these two light sensors to do some interesting things, such as simple gesture recognition.

Preset Gesture() in our light module, which allows us to implement simple gesture recognition, so let's try it.

.. code:: python

    Import light
    From display import*
    Ts = light.Gesture()
    Display = Display()
    t = 0
    While True:
        Res = ts.get_gesture()
        If res != None:
             t = t+1
             Print(res, t)
             If res == 'right':
                    Display.show(Image.ARROW_E)
             Else:
                    Display.show(Image.ARROW_W)

First import our light module, then instantiate the Gesture() class, ts = light.Gesture() to complete the initialization of the detected gestures with this code.

Calling the get_gesture() method to detect our actions, this detection function takes about 25ms to execute, and while True is because we want it to detect our gestures all the time. If you don't want to run for a long time, we can use A for statement determines the number of loops. For example, if we want it to detect gestures within 10 seconds, we can get get_gesture() to loop 400 times for for i in range(10 * 1000 / 25).

After calling the get_gesture() method, ‘right’ is returned if a left-hand action is detected, and ‘left’ is returned if it is a left-hand action.

We swept the two photosensors by hand and it detected the motion and returned the result. The result of the execution of the brush we swept back and forth over the board as shown below

.. figure:: light/message1.png

The measured results are as follows

.. figure:: light/light.gif

.. Attention::

    There are several places to note when using get_gesture()

    To use in an environment with moderate light intensity, do not use it in an environment where the light is too strong or too weak. Under the indoor fluorescent lamp, the accuracy of recognition is the best.

    It is important to ensure that the photosensor is facing the light source when using it, and then emphasize the need to point the board toward the light source.

After we understand how to use the photosensor, we can use it to do some interesting things, such as using gestures to light the led, detecting the light intensity to control the switch, etc., and also combining the previous display to start your brain. Hole and try to do some interesting little things.

.. Hint::

    If you want to know why is light.Intensity(39) and light.Intensity(36)?

    Let's take a look at the circuit diagram at a glance (`View the schematic of bpibit`_)

    .. figure:: light/sensor.png

    The photo sensor on the left is connected to pin pin36, and the photo sensor on the right is connected to pin pin39.

    .. _View the schematic of bpibit: https://github.com/BPI-STEAM/BPI-BIT/blob/master/doc/BPI-WEBDUINO-BIT-V1_4.pdf
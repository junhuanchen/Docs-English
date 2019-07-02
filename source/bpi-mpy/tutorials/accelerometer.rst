Board attitude detection
==============================================================

This module allows you to obtain the current nine-axis attitude of the board, which is the direction state values ​​of acceleration, gravity, and magnetic induction (X, Y).

The most basic function is to obtain the current X, Y, Z three-axis values ​​to determine the motion state of the board at this time. For example, the acceleration Z value increases from small, indicating that there is movement in the Z-axis direction (with acceleration) ), so it can be judged that the board is moving, and the direction of movement is above the Z axis.

Try it first
---------------------------

After a brief introduction, I can design a simple judgment, such as obtaining the balance of the board. Take the accelerometer acceleration module as an example, and get the value of its X-axis to get a basic value. If the value is greater than 20, it means It is biased to the right. If it is less than 20, it is biased to the left. If it is between the two, it is balanced, so there is the following code, showing L for the left and R for the board. Right, try it!

.. code:: python

   From microbit import *

   While True:
       Reading = accelerometer.get_x()
       If reading > 20:
           Display.show("R")
       Elif reading < -20:
           Display.show("L")
       Else:
           Display.show("-")

The effect is as follows:

.. image:: images/base.gif

Feedback board gesture
---------------------------

Attitude detection, such as up, down, left, right, left and right, forward and backward, shaking and landing, etc., the following code is, when the board is facing up, the smile is displayed, and the face down is the expression of angry.

.. code:: python

   From microbit import *

   While True:
       Gesture = accelerometer.current_gesture()
       If gesture == "face up":
           Display.show(Image.HAPPY)
       Else:
           Display.show(Image.ANGRY)

Experience balance ball game
---------------------------

.. Hint::
    
    The code is too complicated to paste the running experience directly.

Based on the previous basic application, we can make a fun balance ball game.

.. code:: python

   Import utime
   From random import randint
   From machine import I2C, Pin
   From mpu9250 import MPU9250

   I2c = I2C (scl=Pin(22), sda=Pin(21), freq=200000)
   Sensor = MPU9250(i2c)
   Print("MPU9250 id: " + hex(sensor.whoami))
   From display import Pixel, PixelPower

   PixelPower(True)
   View = Pixel()
   X, Y, Color, Flag = 2, 2, 2, 0
   While True:
       # print('acceleration:', sensor.acceleration)
       # print('gyro:', sensor.gyro)
       # print('magnetic:', sensor.magnetic)
       A = sensor.acceleration # -1 and -2 Software correction
       View.LoadXY(X, Y, (0, 0, 0), False)
       If (A[1] > -1 and A[1] > X and X < View.Max - 1):
           X = X + 1
       Elif (A[1] < -1 and A[1] < X and X > View.Min):
           X = X - 1
       If (A[0] > -2 and A[0] > Y and Y > View.Min):
           Y = Y - 1
       Elif (A[0] < -2 and A[0] < Y and Y < View.Max - 1):
           Y = Y + 1

       Color = Color + Flag
       If (Color == 10):
           Flag = -2
       Elif (Color == 2):
           Flag = +2

       View.LoadXY(X, Y, (0, Color, Color), False)
       View.Show()
       Utime.sleep_ms(100)

.. image:: images/balance_ball.gif
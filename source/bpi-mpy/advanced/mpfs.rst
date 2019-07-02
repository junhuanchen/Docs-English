Talk again about REPL
==============================

.. Attention::

    Make sure you have the Python3 and pip tools installed in your programming environment, otherwise you won't be able to get started.

We already know that REPL can do some simple code interaction and feedback, and now we have to revisit REPL.

Install the mpfshell tool
----------------------------------------

Please get the `mpfshell-lite <https://github.com/BPI-STEAM/mpfshell-lite>`_ tool from here, the installation and use methods are mentioned here.

REPL in mpfshell
----------------------------------------

Install it, you can use the following functions in repl, of course, you can also implement in other serial terminals such as Xshell and MobaXterm.

.. image:: mpfs.png

Enter history
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

REPL will remember a certain number of the first few lines of text you entered (up to 8 lines on ESP32).
To call the previous line, use the up and down arrow keys.

Use the Tab key
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The Tab key allows you to view a list of all members in the module. This is useful for finding out which functions and methods a module or object has.
Suppose you import import machine in the example below and type ``.`` and then press Tab to see a list of all members of the machine module::

    >>> import machine
    >>> machine.
    __class__ __name__ ADC DAC
    DEEPSLEEP DEEPSLEEP_RESET EXT0_WAKE
    EXT1_WAKE HARD_RESET I2C PIN_WAKE
    PWM PWRON_RESET Pin RTC
    SLEEP SOFT_RESET SPI Signal
    TIMER_WAKE TOUCHPAD_WAKE Timer TouchPad
    UART ULP_WAKE WDT WDT_RESET
    Deepsleep disable_irq enable_irq freq
    Idle mem16 mem32 mem8
    Reset reset_cause sleep time_pulse_us
    Unique_id wake_reason
    >>> machine.


Line continuation and automatic indentation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Some of the content you type will need to "go", that is, more line text is needed to generate the correct Python statement. under these circumstances,
The prompt will change to ``...`` and the cursor will automatically be indented to the correct amount so that you can start typing the next line immediately.
Try this by defining the following function:


    >>> def toggle(p):
    ... p.value(not p.value())
    ...
    ...
    ...
    >>>

Above, you need to press Enter three times in a row to complete the compound statement (ie, only three points on the three lines). Another way to complete a compound statement is to press the backspace key to reach the beginning of the line and press Enter. (If you make a mistake and want to quit, press ctrl-C and all lines will be ignored.)

You just defined the function function to flip the pin level. The pin object you created earlier should still exist
(If you don't have one, you need to recreate it), you can flip the LED with the following command:

    >>> toggle(pin)

Now let's flip the LED in a loop (if you don't have an LED, you can print some text instead of calling the switch to see the effect):

    >>> import time
    >>> while True:
    ... toggle(pin) # print('test')
    ... time.sleep_ms(500)
    ...
    ...
    ...
    >>>

This will flip the LED at 1 Hz (half second on, half second off). To stop switching by ``ctrl-C``, this will cause a keyboard interrupt exception and exit the loop.


Paste mode
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Press ``ctrl-E`` to enter the special paste mode, you can copy and paste a large piece of text into the REPL. If you press ctrl-E, you will see the paste mode prompt::

    Paste mode; Ctrl-C to cancel, Ctrl-D to finish
    ===

You can then paste (or type) your text. Please note that there are no special keys or commands to work in paste mode (eg tab or backspace)
They are only accepted as they are. Press ``ctrl-D`` to finish entering the text and execute it.

Other control commands
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

There are four other control commands:

- Ctrl-A on the blank line will enter the original REPL mode. This is similar to the permanent paste mode except that characters are not echoed.

- Ctrl-B in the blank to go to the normal REPL mode.

- ``Ctrl-C`` Cancel any input or interrupt the currently running code.

- ``Ctrl-D`` on the blank line will perform a soft restart.

Manage files on the board
----------------------------------------

Mpfs provides true file management capabilities, similar to most linux terminal file management tools.

MicroPython internally provides a FAT16 partition file system based on oofats, which can store some file contents, such as code files, resource files, music files, and so on.

In detail, you need to look at the mpfshell readme documentation. Here I will explain a few important features.

.. Note::

    Mpfs is short for mpfshell.

Run python files lexecfile and execfile
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Execfile refers to the code file that exists on the running board. After adding l, the local code file can be transferred to the board and run into repl.

View all files on the board ls
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This will list the names of all the directories and files on the board.

.. code:: shell

    Mpfs [/]> ls

    Remote files in '/':

        Boot.py
        Wifi_cfg.py

Quickly view the contents of the file cat
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To view the boot.py file shown above, type cat boot.py .


.. code:: shell

    Mpfs [/]> cat boot.py
    # This file is executed on every boot (including wake-boot from deepsleep)
    #import esp
    #esp.osdebug(None)
    #import webrepl
    #webrepl.start()
    Import wifi
    Wifi.ready()

    Mpfs [/]>

Delete the specified file rm
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you want to delete the boot.py file shown above, enter rm boot.py, which is irreversible.

File push put and get get
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The two brothers can help you download or upload the file, save it in the lpwd directory, and modify it with lcd.

There are more features you need to try in person or find answers in the tool's documentation.
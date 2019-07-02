First knowledge REPL
===============

One of the main advantages of using MicroPython is that the interactive REPL, REPL (read-evaluate-print loop) represents a read-evaluate-output loop.
REPL is a great help for learning a new programming language because it responds immediately to programs written by beginners, which means you can execute the code and see the results right away without having to compile and upload. Troublesome steps.

Connect the serial port first
--------------------

To access via USB-serial, you need to use the serial terminal software. On Windows such as MobaXterm, xshell are good choices. With the serial port baud rate set to 115200, you can start playing MicroPython.

Once the connection is established through the serial port, you can test if it works by pressing the Enter key a few times. If it works, you can go to the Python REPL prompt and say ``>>>``.

Use REPL
--------------------

Once prompted, you can start experimenting! After pressing Enter, you can type anything at the prompt.
MicroPython will run the code you entered and print the result (if any); if the text you entered is wrong, an error message will be printed.

Try entering the following at the prompt:

     >>> print('hello MicroPython')
     Hello MicroPython

Note that you don't need to type the ``>>>`` arrows, which means you should type text at this prompt, and the next line is the content of the response.

.. Hint::

     In fact, the black box under mpy-editor is actually the repl area where you can interact.

     .. image:: images/editor_repl.png

If you already know some python, you can try some basic commands now. E.g::

     >>> 1+2
     3
     >>> 1/2
     0.5
     >>> 12*34
     408

Try it out?

.. image::image/test_repl.png

Input line editing
---------------------------

You can use the left and right arrow keys to move the cursor to edit the currently entered line;

Press the Home key or ctrl-A to move the cursor to the beginning of the line and press End or ctrl-E to move to the end of the line;

The Delete key or the backspace key is used to delete.
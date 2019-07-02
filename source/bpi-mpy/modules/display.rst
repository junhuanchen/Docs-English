.. _display.py:

.. module:: display

Display module
==============

To use the display module, you need to:

    Import display
    Display= display.Display()


or::
     
    From microbit import display

function
+++++++

.. function:: display.scroll(val, color=Red, delay=150)

    - ``val`` The characters to be displayed are such as 'hello world!' or numbers such as 12345.

    - The colors of ``color`` internal presets are:
            * ``black`` - [0, 0, 0]
            * ``Red`` - [2, 0, 0]
            * ``Orange`` - [2, 1, 0]
            * ``Yellow`` - [2, 2, 0]
            * ``Green`` - [0, 2, 0]
            * ``Blue`` - [0, 0, 2]
            * ``Indigo`` - [0, 2, 2]
            * ``Purple`` - [2, 0, 2]
            
        Users can also use custom colors such as color=[7,8,9]. The values ​​in the list correspond to the red, green, and blue color values, all in the range 0-255.
        At the same time color can also contain multiple colors such as [[0,1,5],[2,2,8],[3,2,1],[4,5,6]], the color of each character will be Displayed according to the color of the color.
    - The speed of the ``delay`` character scrolling.
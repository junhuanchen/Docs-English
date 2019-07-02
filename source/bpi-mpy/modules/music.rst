.. _music.py:

.. module:: music

Music module
==============

The music module is used in the same way as the microbit's music.

To use the music module, you need to:

    Import music

Note
++++

The following is the note format:

    NOTE[octave][:duration]


For example, ``A1:4`` refers to the note "A" in the octave, which lasts for four beats (the beat can be set by the ``set_tempo`` function - see below).
If the note ``R`` is used, it is considered a break (mute).

In the tone symbol, "#" means that the basic pitch is raised by a semitone; "b" means that the basic pitch is lowered by a semitone; for example, Ab is an A-liter semitone and C# is a C-halftone.

The default state of octave is equal to 4, which is the middle scale; the default state of duration is 4 beats;


Beginning of Beethoven's Fifth Symphony::

    ['r4:2', 'g', 'g', 'g', 'eb:8', 'r:2', 'f', 'f', 'f', 'd:8']

The definition and scope of the octave corresponds to the table on the scientific pitch representation listed on this page `on this
Page about scientific pitch notation`_. For example, middle "C" is ``c4`` and concert "A" (440) is ``a4``. The octave begins with the note "C".

.. _on this page about scientific pitch notation: https://en.wikipedia.org/wiki/Scientific_pitch_notation#Table_of_note_frequencies


function
++++++++

.. function:: set_tempo(ticks=4, bpm=120)

    Set the play beat

    A certain number of ticks (integer) constitute a single beat. Each beat is played at a specific frequency per minute (beats per minute - also an integer).

    You can play the beat with reference to the following settings:

    * ``music.set_tempo()`` - Restores the beat settings to ticks = 4, bpm = 120
    * ``music.set_tempo(ticks=8)`` - only change the single beat speed
    * ``music.set_tempo(bpm=180)`` - only change the beat frequency

    Calculating the length of the ticks (in milliseconds) is a very simple arithmetic: ``60000/bpm/ticks_per_beat``.
    For those that are the default values ​​or. ``60000/120/4 = 125 milliseconds`` or ``1 beat = 500 milliseconds``.

.. function:: get_tempo()

    Get the current speed as an integer tuple: ``(ticks, bpm)``.

.. function:: play(music, pin=6, wait=True, loop=False)

    - ``music``

        - Play ``music`` contains the music DSL defined above.

        - If ``music`` is a string, it should be a single note, such as ``'c1:4'``.

        - If ``music`` is specified as a list of notes (as defined in the music DSL section above), they are played one after the other to perform the melody.

    - ``pin`` defaults to the board's P6 pin

    - ``wait`` Blocking: If ``wait`` is set to ``True``, it is blocked, otherwise it is not.

    - ``loop`` : If ``loop`` is set to ``True``, repeat the adjustment until stop is called (see below) or the blocking call is interrupted.
   

.. function:: pitch(frequency, duration=-1, pin=Pin.P6, wait=True)

    - ``frequency``, ``duration``: Plays the frequency at an integer frequency given the specified number of milliseconds. For example, if the frequency is set to 440 and the length is set to 1000, then I will hear standard A for one second.

        If ``duration`` is negative, the frequency is played continuously until blocked or interrupted, or in the case of a background call, the new frequency stop is set or called (see below).

    - ``pin`` pin=Pin.P6, the default is the P6 pin of the board. Other pins can be redefined.

        Please note that you can only play frequencies on one pin at a time.

    - ``wait`` Blocking: If ``wait`` is set to ``True``, it is blocked, otherwise it is not.


.. function:: stop()
    
   Stop all music playback on a given pin.


.. function:: reset()

    Reset the status of the following properties in the following manner

        * ``ticks = 4``
        * ``bpm = 120``
        * ``duration = 4``
        * ``octave = 4``

Built-in melody
++++++++

For educational and entertainment purposes, this module contains several sample tunes represented by a Python list. They can be used like this:

    >>> import music
    >>> music.play(music.NYAN)

All music is not protected by copyright, written by Nicholas H. Tollervey and published in the public domain or has an unknown composer and is protected by fair (education) terms of use.

They are:

    * ``DADADADUM`` - Beethoven's Fifth Symphony C minor opening ceremony.
    * ``ENTERTAINER`` - the opening episode of Scott Joplin's Ragtime classic "The Entertainer".
    * ``PRELUDE`` - JSBach's 48 preludes and fugues' opening of the first C major prelude.
    * ``ODE`` - Beethoven's seventh symphony in the D minor "Ode to Joy" theme.
    * ``NYAN`` - Nyan Cat Theme (http://www.nyan.cat/). The composer is unknown.
    * ``RINGTONE`` - something that sounds like a ringtone. Used to indicate incoming messages.
    * ``FUNK`` - a stylish bass series for secret agents and criminal masterminds.
    * ``BLUES`` - A boogie-woogie 12-bar blues walking bass.
    * ``BIRTHDAY`` - "Happy Birthday" Copyright status can be found at: http://www.bbc.co.uk/news/world-us-canada-34332853
    * ``WEDDING`` - a bride chorus from the Wagner opera "Lohengrin". .
    * ``FUNERAL`` - "Funeral March", also known as Frédéric Chopin's Piano Sonata No. 2 B-minor, Op 35.
    * ``PUNCHLINE`` - An interesting clip indicates that a joke has been created.
    * ``PYTHON`` - John Philip Sousa's parade "Liberty Bell" aka "Monty Python's Flying Circus" theme (later named after the Python programming language).
    * ``BADDY`` - A bad guy at the entrance to the silent movie era.
    * ``CHASE`` - the chase scene of the silent movie era.
    * ``BA_DING`` - indicates a short signal that something has happened
    * ``WAWAWAWAA`` - A very sad trombone.
    * ``JUMP_UP`` - for games, means moving up.
    * ``JUMP_DOWN`` - for games, indicating moving down.
    * ``POWER_UP`` - A show that indicates that an achievement has been released.
    * ``POWER_DOWN`` - A sadness that indicates that an achievement has been lost.

Example:

    """
        Music.py
        ~~~~~~~~

        Plays a simple tune using the Micropython music module.
        This example requires a speaker/buzzer/headphones connected to P0 and GND.
    """
    From microbit import *
    Import music

    # play Prelude in C.
    Notes = [
        'c4:1', 'e', ​​'g', 'c5', 'e5', 'g4', 'c5', 'e5', 'c4', 'e', ​​'g', 'c5', 'e5', 'g4', 'c5', 'e5',
        'c4', 'd', 'a', 'd5', 'f5', 'a4', 'd5', 'f5', 'c4', 'd', 'a', 'd5', 'f5 ', 'a4', 'd5', 'f5',
        'b3', 'd4', 'g', 'd5', 'f5', 'g4', 'd5', 'f5', 'b3', 'd4', 'g', 'd5', 'f5 ', 'g4', 'd5', 'f5',
        'c4', 'e', ​​'g', 'c5', 'e5', 'g4', 'c5', 'e5', 'c4', 'e', ​​'g', 'c5', 'e5 ', 'g4', 'c5', 'e5',
        'c4', 'e', ​​'a', 'e5', 'a5', 'a4', 'e5', 'a5', 'c4', 'e', ​​'a', 'e5', 'a5 ', 'a4', 'e5', 'a5',
        'c4', 'd', 'f#', 'a', 'd5', 'f#4', 'a', 'd5', 'c4', 'd', 'f#', 'a', 'd5', 'f#4', 'a', 'd5',
        'b3', 'd4', 'g', 'd5', 'g5', 'g4', 'd5', 'g5', 'b3', 'd4', 'g', 'd5', 'g5 ', 'g4', 'd5', 'g5',
        'b3', 'c4', 'e', ​​'g', 'c5', 'e4', 'g', 'c5', 'b3', 'c4', 'e', ​​'g', 'c5 ', 'e4', 'g', 'c5',
        'a3', 'c4', 'e', ​​'g', 'c5', 'e4', 'g', 'c5', 'a3', 'c4', 'e', ​​'g', 'c5 ', 'e4', 'g', 'c5',
        'd3', 'a', 'd4', 'f#', 'c5', 'd4', 'f#', 'c5', 'd3', 'a', 'd4', 'f#', 'c5 ', 'd4', 'f#', 'c5',
        'g3', 'b', 'd4', 'g', 'b', 'd', 'g', 'b', 'g3', 'b3', 'd4', 'g', 'b ', 'd', 'g', 'b'
    ]

    Music.play(notes)
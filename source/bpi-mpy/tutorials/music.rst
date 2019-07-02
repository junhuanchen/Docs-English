Play simple music
==============================================================

I have provided a MIDI playback function module that can perform PWM output on the specified buzzer to play music, although you may not need to know this.

Cough, not much nonsense, come to the music, a built-in buzzer has been pre-wired on the board, its pin position is 25, if you have some hands-on ability, you can learn how to pick one yourself later. A buzzer to play music.

.. Attention::

          Do not install a piezoelectric buzzer, it can only play a single tone.

Use the code as follows (interface can refer to Microbit documentation)

.. code:: python

    Import music
    Music.play(music.NYAN)

You can see the following list, which is our built-in music.

.. code:: python

          music.DADADADUM
          music.ENTERTAINER
          music.PRELUDE
          music.ODE
          music.NYAN
          music.RINGTONE
          music.FUNK
          music.BLUES
          music.BIRTHDAY
          music.WEDDING
          music.FUNERAL
          music.PUNCHLINE
          music.PYTHON
          music.BADDY
          music.CHASE
          music.BA_DING
          music.WAWAWAWAA
          music.JUMP_UP
          music.JUMP_DOWN
          music.POWER_UP
          music.POWER_DOWN

Pick some out and listen, there should be something you like.

Create a song
----------------------------------------

Write down a list of Python
``["C4:4", "D4", "C", "E:8"]``\ represents a piece of music.

How to understand this?

Each element can be thought of as a note, and its format satisfies the following:

.. code:: python

    NOTE[octave][:duration]

First of all, there must be a little bit of basic understanding of music theory.

NOTE refers to the scale of this node. In general, C D E F G A B in music is a scale, such as ``"C"`` refers to do, so C D E F G A B is do re mi fa so la xi.

Octave refers to the octave of this node. The octave refers to the interval relationship. Simply put, you sing 1 2 3 4 5 6 7 1 (note: 1234567 corresponds to the CDEFGAB), the first one is the last A low octave of 1 and the last 1 is the high octave of the first 1, the bass to the treble, and the smaller the bass, the lower the bass.

Duration refers to the number of beats of this node, which is simply understood as the duration of the note playback of the node.

for example:

``"C4:4"`` is equivalent to the note of C(Do) in 4 (middle part), then: 4 means four beats, the default beat duration is 125 ms, that is, the duration is 0.5. s.

If you name the node NOTE R, then the speaker will not play any sound for the specified length of time.

To explain this well, let's look at the case in the next chapter.

.. Hint::

          The default beat position of the music module is ticks=4, bmp=120, ticks
          Refers to the default value of the beat type of a note, such as ‘C4’ and ticks=4, which is equivalent to
          ‘C4:4’ means the length of time this node plays under the bpm benchmark, and bpm
          Refers to the unit of beats per minute, which is dependent on BPM in electronic music.
          The value of the value describes the rate of different music.

          According to the formula, the tempo of the benchmark can be calculated. beats = 60(s) \* 000 / 120 / ticks
          If it is the default value, the duration of the beat unit is 60000/120/4 = 125 milliseconds.

Try playing music
----------------------------------------

Try this code yourself.

.. code:: python

    Import music
    Music.play([ "C4", "D4", "E4", "F4", "G4", "A4", "B4", "C5"])
    Music.play([ "D1", "D2", "D3", "D4", "D5", "D6", "D7", "D8"])

Play two tigers
----------------------------------------

In order to be able to play this classic two tigers on the board, we prepared the following code.

.. code:: python

    Import music

    Tune = ["C4:4", "D4:4", "E4:4", "C4:4", "C4:4", "D4:4", "E4:4", "C4:4" ,
              "E4:4", "F4:4", "G4:8", "E4:4", "F4:4", "G4:8"]
    Music.play(tune)

And the magic is not only that, it can further simplify the composition process, for example, the current node
‘C4:4’ will affect the subsequent octave configuration until there is a new replacement. So you can write like this:

.. code:: python

    Import music

    Tune = ["C4:4", "D", "E", "C", "C", "D", "E", "C", "E", "F", "G:8" ,
              "E:4", "F", "G:8"]
    Music.play(tune)

Did it produce the same effect?

Special sound effects
----------------------------------------

Music lets you make non-note sounds, like here we create a siren

.. code:: python

    From microbit import *
    Import music
    While True:
         Music.pitch(range(880, 1760, 16), 15)
         Sleep(50)
         Music.pitch(range(1760, 880, -16), 15)
         Sleep(50)

Slightly note that the music.pitch method is an example of using it, it requires a frequency, and the frequency of 440 is equivalent to the frequency of a concert a used for tuning.

Also, in this case, the range function is used to generate a numeric value that defines the pitch of the pitch, which is divided into a start value, an end value, and a gradient value. So the meaning of the first range here is. Create a frequency value starting at 880, increasing from 16 to 1760, and the second range is to create a 1760 with a span of 16 to decrement to 880. This allows us to make a sound like a siren.

Finally, we also used while Ture: it will make this siren sound continuous, is it very interesting?

Connect your sounds
----------------------------------------

Did you find that the sound was a bit small when playing music on the board? Here we will show you how to connect the board to the sound and play the music with the sound, as shown below.

.. image:: music/music.jpg

P0 port is connected to the left channel or right channel of the audio cable, and GND is connected to the GND of the audio cable.

.. image:: music/5.png

Get music scores from the web
----------------------------------------

The first time you come into contact with the music format, the students who don’t understand the music may be a bit embarrassed. Is there a way to get the score quickly? Some netizens have specially created a conversion tool that can automatically generate data in audio format. Let us try to use this tool to generate music data that the board can play.

This tool is made by `fizban99`_. Https://github.com/fizban99/microbit_rttl

The conversion work is implemented by an excel file. We first download the excel file, \ `click to download `_

We have the conversion tool, then we need to download the music source file, click the link below to download
`Zip file of Mixed Tunes 1 (450 tunes)`_ `Zip file of Mixed Tunes 2 (375
Tunes)`_ `Zip file of Mixed Tunes 3 (10,000 tunes)`_ `Zip file of TV
Theme Tunes (50 tunes)`_ `Zip file of Christmas Tunes (70 tunes)`_

Unzip the downloaded music source files. After all the preparations are done, open the excel file we downloaded earlier and you will see an interface like the one below.

.. image:: music/1.png

Click Open RTTTL tune file, it will automatically pop up the file manager, find one of the files we just extracted, select the music file to be converted, click to open

.. image:: music/3.png

After completing the above steps, we have completed the conversion work. Click play to play the music file. Note: The Copy code here is not readable by copying the code, so we can copy the contents of the red box directly.

.. image:: music/4.png

Copy the converted code and let the board play the music.

.. code:: python

    Import music
    Music.set_tempo(ticks=16, bpm=45)
    Tune = ['D#6', 'D#', 'D#:2', 'F', 'G', 'G#', 'G#', 'G', 'F', 'F:6',
              'D:2', 'D', 'D', 'D', 'D#', 'F', 'G', 'G', 'F', 'D#', 'D#:6',
              'D#:2', 'D#', 'D#', 'D#', 'F', 'G', 'G#', 'G#', 'G', 'F', 'F:4']
    Music.play(tune)

.. _fizban99: https://github.com/fizban99

.. _Click to download: https://github.com/fizban99/microbit_rttl/raw/master/rtttl2microbit.xlsm

.. _Zip file of Mixed Tunes 1 (450 tunes): http://www.picaxe.com/downloads/rtttl.zip

.. _Zip file of Mixed Tunes 2 (375 tunes): http://www.picaxe.com/downloads/rtttl2.zip

.. _Zip file of Mixed Tunes 3 (10,000 tunes): http://www.picaxe.com/downloads/rtttl3.zip

.. _Zip file of TV Theme Tunes (50 tunes): http://www.picaxe.com/downloads/rtttl_tv.zip

.. _Zip file of Christmas Tunes (70 tunes): http://www.picaxe.com/downloads/rtttl_xmas.zip
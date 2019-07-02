How to use scratch3 for bpi:bit
=========================================================== ===

Online `Scratch3 Codelab`_ website, see here more in detail ` `codelab`_ and `scratch open source documentation `_\ .

First choose the version of the system that suits you, get `adapter`_, no need to install, open it.

Then refer to the `usb_microbit user manual `_\, and similarly, as shown below, check the mpfshell option.

.. figure:: codelab/used.png

How to use them?
-------------------------------------------------- ----

Make sure the adapter software and the scratch3 website are open. On the scratch3 website, click on it (the expansion button in the lower left corner)

.. figure:: codelab/external.png

And scroll to the bottom, find the bpi:bit plugin to select it, click OK to return to the main interface.

.. figure:: codelab/select.png

Check isconnected to connect

.. figure:: codelab/isconnected.png

At this point, insert the hardware, click on the connection, you can see that it will be connected soon. (If you are not sure, check it out with the usual mpfshell method)

.. figure:: codelab/result.png

At this time, the standard building blocks that it can use are as follows.

.. figure:: codelab/function.png

Since then you are free to use the built-in blocks, but if you are not satisfied with the building blocks, you can use them directly.
Mpfshell, directly control the hardware, directly complete the interface call and test, if you want some combination debugging interface, become a separate building block, you can submit it to me, merge directly, but because scratch3 does not have dynamic building block loading, so There is no way to completely open the docking.

.. figure:: codelab/demo.png

How to use Scratch3 for Mpfshell?
-------------------------------------------------- ----

How to use mpfshell, in fact, only need to look at a few examples to know their origin and control relationship.

.. figure:: codelab/example.png

If you know how mpfshell is used, then the same is true. The so-called control hardware is actually equivalent to calling mpfshell exec every time.

But the point to note is that eim/mpfshell/exec/bpibit is a typical theme, meaning that this is an instance access interface. If you have multiple hardware, it will present different interfaces, such as default
The mpfshell plugin theme is eim/mpfshell/exec/default, and the extension of bpibit is eim/mpfshell/exec/bpibit, so you can distinguish the control of multiple instances according to this, and when you need it, you will find it necessary. Sex.

Talk about how it was designed
-------------------------------------------------- ----

This time we have a second-editable interface, but if you really want to know how to do it, you can understand both projects.

- `scratch3-eim-mpfshell`_

- `webduino-module-eim`_

And the scratch3 plugin will eventually expect to sync to Webduino blockly, because on our blockly platform, allowing you to define your own building blocks without building a server, means you can focus on implementing your own building blocks instead of modifying each time. To merge into the server to rebuild. The building blocks and expansion plug-ins developed in this way are completely their own, and they can also eat most of the front-end platforms of building blocks, and the freedom is not limited, perfect!

.. _Scratch3 Codelab: https://scratch3.codelab.club/
.. _codelab: https://www.codelab.club
.. _scratch open source documentation: https://blog.just4fun.site/tag/scratch.html
.. _adapter: https://adapter.codelab.club/user_guide/install/
.. _usb_microbit User Manual: https://adapter.codelab.club/user_guide/usage/#3-microbit
.. _scratch3-eim-mpfshell: https://github.com/junhuanchen/scratch3-eim-mpfshell
.. _webduino-module-eim: https://github.com/junhuanchen/webduino-module-eim
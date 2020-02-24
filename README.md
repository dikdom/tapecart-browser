tapecart-browser large directory mod
=========================

This is a modified tapecart-browser that is capable of handling 8MB and 255 entries in the menu (coming from one single TCRT file). 

If you compile a TCRT file less than 2MB, then the original tapecart hardware will be able to handle it.
Otherwise you need to 
- replace the flash chip with a larger one (4, 8 or 16MB) which can store your TCRT content
- recompile the firmware of the tapecart (check out my tapecart repo clone), and flash the MCU you have. How to do that? It is beyond the scope of this doc.
Writing an 8MB TCRT file from C64 takes around 6 hours. 
If you have a DIY board and know what you are doing then you can re-flash the chips within 6 minutes with an EEPROM burner (the TCRT content must be written to the flash from the tcrt file address of $D8, the browser's entry point is changed to $3000 from $2800 and the length of the browser is changed to $3E5F - You need to fix these last two values in the EEPROM area of the MCU).
Have fun! 



Original README:

tapecart-browser
================

This is a browser for the tapecart.

The file system used is described in the doc folder.

Also included is a small program for bundeling files
and the browser together in a TCRT image.


Usage
-----

Run the following to create the binary:

    stack build
    stack exec tapecart-browser


Binaries
--------

Compiled binaries are available in the [Releases](https://github.com/alexkazik/tapecart-browser/releases/latest) section.

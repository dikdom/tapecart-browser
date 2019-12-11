taprecart-browser 8MB mod
=========================

This is a spinoff,  modified tapecart-browser that will be capable of
handling more than 126 entries in the menu (coming from one single
TCRT file). Currently investigation is ongoing for feasibility check
if it is reasonably possible...
This haskell environment is insane (almost 1GB needs to be downloaded to install), but I don't have time to refactor..



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

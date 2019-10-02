# Gameshark

*Note: Gameshark support has been deprecated. It is still provided, but without
guarantees.*

*Note: These instructions only cover Windows users.*

You will need:

-   An N64 with a supported game cartridge, and an Expansion Pak.
-   A Gameshark with a functional parallel port (note that some 3.3s only have
    dummy ports).
-   A Parallel to USB adapter cable with bidirectional communication support.
    The included Gameshark utility is designed to function with a Moschip
    MCS7705 cable, and has only been tested with a version 3.3 Gameshark.
-   [Zadig](http://zadig.akeo.ie/), a usb driver tool.

Follow these steps;

1.  Boot the Gameshark with your game cartridge. If your game requires a
    special keycode to boot, you'll first need to boot the Gameshark with a
    game that works with the default keycode, select the the required keycode
    in the Key Codes menu, and then reboot with the game you wish to use with
    The Practice ROM.
2.  In the Select Cheat Codes menu, select your game and make sure the `(M)`
    code is active, if one exists.
3.  In the Start Game submenu, enable the Code Generator option, and select
    Start Game With Selected Codes.
4.  Connect the Gameshark to your computer with your Parallel to USB adapter
    cable.
5.  Start Zadig and select the Gameshark in the device the list (probably named
    USB Device or something similar).
6.  Select libusbK in the driver list and click Replace Driver.
7.  Navigate to the directory that corresponds to your game and run the
    `upload.bat` script. This will instruct the Gameshark utility to upload The Practice ROM
    to the game's memory, and then disconnect the Gameshark. The operation will
    take a while.
8.  When the upload is completed, you can disconnect the USB cable and start
    playing.

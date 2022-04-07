# Macro

This menu provies tools for producing tool-assisted gameplay recordings. Press
**pause** to freeze/unfreeze the game, and **frame advance** to advance the
game one frame at a time, allowing for precise input control. Start recording
your inputs by pressing **record macro**, and play back your recorded inputs by
pressing **play macro**. The **macro frame** control shows the number of the
current frame which your inputs are being recorded to / played back from. You
can edit this value to seek to a specific frame of input, or press
**rewind macro** to seek to frame 0. The total number of input frames recorded
in the current macro is displayed on the right. Press **trim macro** to delete
all recorded inputs after the current macro frame, should you feel that you've
recorded too far.

Use the arrows to select a savestate slot, and save the current state of the
game to that slot by pressing **save state**. You can then return to that state
by pressing **load state**. If you are in macro recording/playback when saving
a state, the frame number will be saved within the state, and the macro will
seek to that frame when loading the state. This allows you to record over
previously recorded inputs, to correct mistakes for example. If there's no
macro frame stored in the state, your macro will not be affected.
**clear state** deletes the state in the current state slot. Some information
about the state saved in the current slot is displayed; the scene in which it
was saved, the size of the state, and the macro frame (if any) on which it was
saved.

**Quick record movie** is a convenience option to start recording a macro, save
a state to slot 0 for playing back the macro from the start, and then switch to
slot 1 to use for rerecording. **quick play movie** will start macro playback
from the start and load the state in slot 0.

Macros and savestates can be saved to and loaded from an SD card using **export
macro** / **import macro** and **export state** / **import state**. Pressing
any of these buttons will open the file browser. When importing, pressing the
name of a file in the file browser will load it and return to the macro menu.
When exporting, the filename can be changed by pressing the name field. The
default name for savestates is a number followed by the name of the scene where
the state was saved. The numbering starts at zero and increments if there is
already a file with that number in the current directory. Pressing **clear**
will set the name field to be empty. When the name field is empty, the default
filename is `untitled`. Pressing the name of a file will copy that name to the
name field. Pressing accept will save the file to the current folder in the
file browser with the specified file name. If the file exists, you will be
prompted to overwrite it. New directories can be created by pressing the folder
icon to the left of the name field, inputting a name for the new directory with
the on-screen keyboard, and then pressing the name to confirm. To cancel, use
the return command.

_Note:_ Macros override all controller input by default, but this can be
changed with the **macro input** setting in the settings menu.

_Note:_ States can not be used in the file select menu or on the n64 logo.

_See also:_ [Issues with Savestates](../../savestates/index.html).

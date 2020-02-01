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
macro** / **import macro** and **export state** / **import state**.

_Note:_ Macros override all controller input by default, but this can be
changed with the **macro input** setting in the settings menu.

_Note:_ States can not be used in the file select menu or on the n64 logo.

_See also:_ [Issues with Savestates](./issueswithsavestates.html).

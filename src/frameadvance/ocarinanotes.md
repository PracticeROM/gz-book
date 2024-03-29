# Ocarina Notes

When an ocarina song plays on a staff, the notes appearing on the staff are
synced to the audio. The purpose of this is to compensate for potential
differences in lag or framerate, so that the note always appears when you hear
the sound. This poses a problem when frame advancing, because as far as the
game is concerned, frame advancing is essentially lag. The note sync mechanic
is not robust against severe lag, and such lag can cause the staff to simply
stop playing notes, or break in other strange ways.

The Practice ROM circumvents these issues by disabling the audio sync when frame advancing or
recording/playing a macro. Instead, the game is assumed to run at a constant
framerate with no lag, so that no timing adjustment needs to be done.
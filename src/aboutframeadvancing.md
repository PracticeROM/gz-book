# About Frame Advancing And Recording

## Room Loading

Room loading normally happens asynchronously. That means the game continues
playing while the room loads, and the room appears whenever it's finished
loading. This usually takes 1 frame, but can take longer, depending on the cpu
and cartridge load. Emulators typically don't emulate cartridge bandwidth
limitations, so the delay is usually 0 frames.

When recording or playing back a macro, room loading behavior is changed to
always load synchronously. Thus the game stops until the room has finished
loading, such that load delay variations can not cause macros to desync.

## Ocarina Notes

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

## Ocarina Input

The game's input manager polls the controller at a rate of ~60Hz. Ocarina input
is handled separately from the common game input, and circumstances can cause
it to be delayed into a different controller input window. When this happens,
the input seen by the ocarina on a given frame may be different from that seen
by the rest of the game.

This is a source of potential desyncs in macros, so when playing or recording a
macro, The Practice ROM ensures that the ocarina input is the same as the common game input
for any given frame.

## RNG Seeds

The game's Random Number Generator (RNG) is used to decide the outcomes of
random events. The RNG is deterministic, which means that given the same
initial conditions, it will produce the same results. For example, by starting
from a savestate in the graveyard and playing a macro to have Dampé dig a
grave, your reward should be the same every time, as long as the same savestate
and macro is used.

The value of the RNG is predictable given a known starting state. However, the
starting state of the RNG itself (the _seed_), is generally not predictable
(read _pretty damn random_). The RNG is reseeded on every scene load, and from
that point, the future state of the RNG is equally unpredictable.

In order for macros to stay synchronized across scenes, all RNG reseeds are
recorded in the macro file. When an RNG reseed is detected during macro
playback, the stored seed will be used instead of a random value if the
following conditions hold;

-   The state of the RNG is the same as when the seed was recorded (i.e. the
    RNG is synced up until this point).
-   The reseed happens on the same macro frame that it was recorded.

If either of these would fail, the RNG is reseeded as normal with an
unpredictable value.

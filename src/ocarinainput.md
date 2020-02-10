# Ocarina Input

The game's input manager polls the controller at a rate of ~60Hz. Ocarina input
is handled separately from the common game input, and circumstances can cause
it to be delayed into a different controller input window. When this happens,
the input seen by the ocarina on a given frame may be different from that seen
by the rest of the game.


This is a source of potential desyncs in macros, so when playing or recording a
macro, The Practice ROM ensures that the ocarina input is the same as the common game input
for any given frame.

# RNG Seeds

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

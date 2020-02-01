# Issues with savestates

## Dangling Pointers

This mainly concerns what's known as the _cutscene pointer_. When executing a
wrong warp, the cutscene pointer will often be a _dangling pointer_, meaning
that it points to memory which is no longer in use, or is now used by something
else. This affects the behavior of wrong warps, because the cutscene data will
now have been replaced by _garbage_.

The Practice ROM does not save unused memory in states, and this can have some unexpected
side effects when loading a state that had a dangling pointer. The pointer
itself will have the same value, and be exactly the same. However, the memory
that the pointer points to _may not necessarily_ be exactly the same.
Specifically, if the cutscene pointer pointed to garbage, the only guarantee is
that it will still point to garbage, not the exact same garbage. Because of
this, the behavior of wrong warps is not guaranteed.

## Corruptions

Some assumptions are made about the state of the game when it is saved. For
example, the scene file is assumed to be largely the same as it appears on the
rom. As such, only a few details actually need to be saved. There are
situations where these assumptions break down; if the scene file had become
corrupted for some reason (e.g. double loading), those corruptions would not
be restored when the scene is loaded again.

## Graphics

Graphical dependencies (i.e. object files) take up a lot of space, and saving
them in states would not be practical. Fortunately, they mostly contain static
data that never changes, and can plainly be loaded from the rom when needed.
But there are some graphical effects that modify these files, and The Practice ROM does not
account for this. Specifically, some dissolving effects are known to modify
textures, which can cause them to look odd after a state load. These issues are
purely aesthetic.

## Audio

The state of the audio is well separated from the state of the game, so
restoring the audio state is not necessary for the game to behave correctly
after a state load. The audio state is also quite complex and take up much
space. For these reasons, savestates only save minimal information about the
state of the audio. This has been known to sometimes cause audio bugs, such as
music failing to start playing, or sound effects not playing as they should.

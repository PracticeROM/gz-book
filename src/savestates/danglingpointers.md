# Dangling Pointers

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

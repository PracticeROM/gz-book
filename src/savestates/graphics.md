# Graphics

Graphical dependencies (i.e. object files) take up a lot of space, and saving
them in states would not be practical. Fortunately, they mostly contain static
data that never changes, and can plainly be loaded from the rom when needed.
But there are some graphical effects that modify these files, and The Practice ROM does not
account for this. Specifically, some dissolving effects are known to modify
textures, which can cause them to look odd after a state load. These issues are
purely aesthetic.

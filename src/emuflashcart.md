# Nintendo 64 Console / Emulator

**Nintendo 64 Console:** Requires a flash cart.

**Windows:** Drag and drop a compatible rom onto the `patch.bat` script.

**GNU/Linux:** Run `./patch <rom-file>`.

A patched rom will be created. It can be played with an emulator or transferred
to a flash cart. For emulator usage, you will need to enable Expansion Pak
emulation. On some emulators, you may need to change CPU Core Style to
Interpreter. For use with a flash cart, your N64 will need an Expansion Pak.

### Enabling line features on N64
**Windows:** Select both your patched rom and a microcode rom, then drag and
drop them onto the `inject_ucode.bat` script.

**GNU/Linux:** Run `./inject_ucode <patched-rom> <ucode-rom>`.

The currently known and supported microcode roms are `Hey You, Pikachu! (U)`
and `Hey You, Pikachu! (J)`.
# Watch Import Syntax

A watch file is a normal text (*.txt) file containing names, types, and
addresses of watches. Like this document, which happens to be a valid watch
file. Each line in the file can have one watch entry. The ' character starts a
line comment (like this one). Comments are just plain text that gets ignored
when importing watches from a watch file.

Watches look like this:

```
"this is a watch" u16 0x80001234
```

The name of the watch goes first, contained in double quotes. After it comes
the data type. valid data types are:

```
u8,  s8,  x8  : one-byte value (signed format, unsigned format, hex format)
u16, s16, x16 : two-byte value (ditto)
u32, s32, x32 : four-byte value (ditto)
f32           : four-byte value, 32-bit ieee 754 single-precision floating-point format
```

Finally comes the address. In the example above, the address is just a simple
hexadecimal number. Numbers can start with '0x' for hexadeciaml, '0b' for
binary, '0' for octal, or any digit other than zero for decimal, but,
the address can also be a more complex expression, with arithmetic and
indirection.

The available arithmetic operators are:

```
*, /, % : multiplication, division, and remainder
+, - : addition and subtraction
```

Here's an example address with arithmetic operations:

```
"complex address with arithmetic" f32 5 * (3 + 4)
```

The address in this example becomes the result of the arithmetic expression,
which is equal to:

```
5 * (3 + 4) = 5 * (7) = 35
```

Obviously this isn't very useful, since you could have just written '35' as the
address (and also 35 isn't even a valid address). That's where indirection
comes in.

Indirection is the act of replacing part of an expression with the value at the
address given by that expression. This is done by enclosing the sub-expression
in [square brackets]. If we do this with the address in the first example we get:

```
"this is also a watch" u16 [0x80001234]
```

This expression no longer means "the address I want is 0x80001234", but instead
means "the address I want is the value located at 0x80001234 in memory". So
whatever 32-bit value happens to be at 0x80001234 when this watch is imported,
that's going to be the address of the new watch. This is useful for computing
the address of dynamically loaded things, such as most actors. The value given
by the indirection doesn't need to be an actual address though. It can be a
smaller part that is needed to compute the address of a bigger expression. The
result of an indirection can be used in arithmetic just like any number. There
can also be nested indirection:

```
[[0x80001234 + 0x20] + [0x80003210] * 0x31]
```

The expression above means: "add 0x20 to 0x80001234, then get the value at the
resulting address. Multiply the value at 0x80003210 by 0x31. Take these two
values and add them together. Then, since the whole thing is enclosed in square
brackets, get the value at the address resulting from the last summation and
use that as the new watch address."

In all of the above uses of indirection, the type of the value to get is
implicitly a 32-bit integer. But, other types can be used as well by explicitly
preceding the square brackets with a mode indicator.

The following modes are available:

```
b.[0x80001234]  : one-byte value, sign-extended to 32 bits.
bz.[0x80001234] : ditto, zero-extended to 32 bits.
h.[0x80001234]  : two-byte (16-bit halfword) value, sign-extended to 32 bits.
hz.[0x80001234] : ditto, zero-extended to 32 bits.
w.[0x80001234]  : four-byte value (32-bit word, the default mode when no mode is explicitly specified)
```

Finally, there are a few builtin symbols that can be used in address
expressions. Whenever one of these are encountered, they are replaced by the
address represented by that symbol.

```
"Link x" f32 link + 0x24
```

The above expression results in whatever address the Link actor is loaded at,
plus 0x24. This happens to be the address of Link's x-coordinate.

These symbols exist:

```
link  : gets replaced by the starting address of the Link actor
ctxt  : gets replaced by the address of the global context
file  : gets replaced by the address of the current zelda file data
```

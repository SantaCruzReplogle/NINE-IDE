
                         August 1, 2026

The "Nine" Integrated Development
Environment is a text editor, compiler
and virtual machine in a single program.
It was originally designed for embedded
industrial control systems and field
instruments using the Intel 80C196
microcontroller running at 12 MHz with
external SRAM, serial EEPROM, and a
detachable 40 column LCD display.  It
was written in assembly language, then
ported to mostly C in 2021 for MS-DOS
version 2.0 or higher and the 8086 CPU
with 64 kilobytes of free RAM.

To run, type "nine" (without quotations)
at the DOS prompt.  Almost immediately
you'll enter the text editor where
programs are entered and run.  The IDE
does not accept plain text files.
Instead the included utility CONVERT.COM
translates a text file into a compressed
format, then writes to file NINE.PRG.

C:\NINE>convert cube.txt
Writing file NINE.PRG

C:\NINE>nine

Nine works with just two source files,
NINE.PRG and NINE.OLD.  NINE.PRG is the
main work file that is loaded on startup
if present.  NINE.OLD is a backup file,
a copy of a previously saved file.  The
text editor treats NINE.OLD as
read-only, that is, it can only be read
into the editor.

Nine outputs another file, NINE.ROM.
This file contains nonvolatile data the
programmer can modify.

Included is MANUAL.TXT, the complete
text editor and programming language
reference manual.  The file is too large
to convert and read in Nine.  It will
need to be broken down in order to fit.

Nine's one command line option, -r or
/r, runs NINE.PRG automatically, then
exits.

C:\NINE>nine -r

A note should be made regarding the Ctrl
+ Break keys.  Ctrl + Break is arguably
one of the most important feature in the
IDE.  It is used to interrupt a
compiling, running, uploading or
downloading program.  The original IBM
Model M 101-key keyboard mapped Ctrl +
Break to Ctrl + Scroll Lock.  Modern
keyboards rarely have a dedicated
"break" key anymore.  Modern laptop
manufactures "map" the older and rarely
used keys behind the Fn (function) key
to save space.  On HP laptops for
example, triggering Ctrl + Break is done
by first holding keys Ctrl, then Fn, and
then the pause key.  On Lenovo, Dell and
most ASUS laptops, pressing Ctrl + Fn +
B activates the break.  On some laptops
like the ultra-slim Dell Latitude, no
Ctrl + Break scan code is generated.
Emulators like DOSBox or even MS-DOS
compatible operating systems like
FreeDOS or Real DOS do provide simple
remapping tools that change how the
physical buttons on a keyboard behave.

For DOSBox users, serial communications
via null modem should set "transparent"
to 1.

  serial1 = nullmodem ... transparent:1

Bugs, comments or questions?
Contact:

Todd J. Replogle
Email: santacruzreplogle@yahoo.com


Files included:

NINE.COM            The IDE

MANUAL.TXT          Reference manual

CONVERT.COM         Utility that
                    converts a text
                    file to NINE.PRG

LICENSE.TXT         Licensing
                    information

README.TXT          This file

CUBE.TXT            Rotating 3D cube

HELLO.TXT           "Hello World!"

HELLO2.TXT          "Hello World!" #2

MBROT.TXT           Mandelbrot Set

TEMPLATE.TXT        Useful template

TERM.TXT            Simple terminal
                    emulator

NINE.PRG            Converted HELLO.TXT


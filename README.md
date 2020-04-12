# secoli-libvrb

This repository contains the library `libvrb-0.5.1` by Philip D. Howard, 
which is needed to build and use [secoli-SCEd](https://github.com/reale/secoli-SCEd).

## Description

The VRB library implements a ring buffer, also known as a character
FIFO or circular buffer, with a special property that any data present
in the buffer, as well as any empty space, are always seen as a single
contiguous extent by the calling program.  This is implemented with
virtual memory mapping by creating a mirror image of the buffer contents
at the memory location in the virtual address space immediately after
the main buffer location.  This allows the mirror image to always be
seen without doing any copying of data.

VRB is written in C and is intended for C programmers.  It can be used
in C++ but C++ programmers will find that their usual ways of coding for
objects does not apply.  And this is because it is intended just for C.

## Installation

The installation instructions are in file "INSTALL".  But if you are in
a hurry, you can just do:

    ./configure --prefix=/usr/local
    make clean
    make install

You will probably have to configure your operating system to properly use
the new library.

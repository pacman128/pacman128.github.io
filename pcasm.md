---
layout: pcasm
title: PC Assembly Book
menu: main
permalink: /pcasm/
---

I taught Computer Science at the [University of Central Oklahoma](http://www.ucok.edu) for 10 years. During this time I taught an introductory course in PC
Assembly Language programming. I grew frustrated at teaching 16-bit
real mode programming and decided to change to 32-bit protected mode.
However, I soon ran into a problem. I could not find a textbook that
covered 32-bit protected mode assembly programming! So, I decided to
write my own.

I also did not want students to have to go out and buy expensive
software for the course. I decided to base the course on the free
_NASM_ (Netwide Assembler) and the free GNU _gcc_
compiler (however, any 32-bit C compiler would work). Another
advantage of these choices was that students could use
_Windows_, _Linux_ or _FreeBSD_ to develop
on. (In fact, I use Linux for my main development platform.)

Over one summer I wrote the bulk of this textbook and developed
the examples using _LaTeX_. I made a feeble attempt to get the
book published and then decided to publish it myself online for free.
Why? To return something back to the developer community. I have used
many _open source_ products and wanted to make a modest
contribution of my own.

The book has extensive coverage of interfacing assembly and C code
and so might be of interest to C programmers who want to learn about
how C works under the hood. All the examples use the free NASM
(Netwide) assembler. The tutorial only covers programming under 32-bit
protected mode and requires a 32-bit protected mode compiler. It
is possible to use the book and examples on a 64-bit OS; however, the
programs will be running in 32-bit mode and cannot use any 64-bit
functionality.

I have example code files for: DJGPP, Borland, Microsoft, Open
Watcom and Linux C compilers. The examples in the text of the tutorial
are for DJGPP only, but how to interface with the other compilers is
discussed as well. The example files also include macros that allow
easy input/output and debugging (register dumps, memory dumps,
coprocessor dumps and stack dumps). If you plan on running the
examples in the tutorial, you _must_ download the appropriate
example code file below. It contains support files
used by the examples in the tutorial (such as _asm_io.inc_).

### Table of Contents
1. Introduction
1. Basic Assembly Language
1. Bit Operations
1. Subprograms
1. Arrays
1. Floating Point
1. Structures and C++

Feedback is welcome. Below are links to the files:

## Example code:

* [Linux examples](/static/linux-ex.zip)
* [DJGPP examples](/static/djgpp-ex.zip)
* [cygwin examples]({{site-url}}/static/cgywin-ex.zip)
* [MS C examples](/static/ms-ex.zip)
* [Borland examples](/static/borland-ex.zip)
* [Open Watcom examples](/static/watcom-ex.zip)

## Book

* [English PDF File](/static/pcasm-book.pdf)
* [Physical book in English from Lulu](http://www.lulu.com/content/paperback-book/pc-assembly-language/7341484)

* [French PDF file](/static/pcasm-book-french.pdf) 
(Translated by Sébastien Le Ray)
* [German PDF file](/static/pcasm-book-german.pdf)
(Translated by Ulrich Bicheler)
* [Spanish PDF file](/static/pcasm-book-spanish.pdf)
(Translated by Leonardo Rodríguez Mújica)
* [Italian PDF file](/static/pcasm-book-italian.pdf)
(Translated by Giacomo Bruschi)
* [Korean PDF file](/static/pcasm-book-korean.pdf)
(Translated by Jae Beom Lee)
* [Simplified Chinese PDF file](/static/pcasm-book-simplified-chinese.pdf)
(Translated by Wu Xing)
* [Traditional Chinese PDF file](/static/pcasm-book-traditional-chinese.pdf)
(Translated by Wu Xing)





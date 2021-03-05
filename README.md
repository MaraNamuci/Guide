# Guide

## Resources

Sites with coding exercises
https://www.codewars.com/
https://exercism.io/

Quick Reference material
https://www.tutorialspoint.com/c_standard_library


## OOP is worthless

Java is the epitome of object oriented programming.
It's ridiculously verbose and unnecessarily convoluted.
Ultimately, you should focus on making the code simple 
and easy to maintain.
Only encapsulate things you actually plan to tweak.

## File system organisation
Tiny programs, keep all the code in main.c
Keep all the constants, includes and trash in main.h

As the project gets larger you will need to think
carefully about the easiest way to organise your files

https://www.microforum.cc/blogs/entry/46-modular-code-and-how-to-structure-an-embedded-c-project/

## Standard Libraries

The C programming language base is made up of a number
of keywords and constructs that on their own could build
a functioning operating system.

However, most of this work has already been done and
thoroughly optimised in the form of standard libraries.

* <stdio.h>
* <stdlib.h>
* <stddef.h>
* <string.h>
* <math.h>
* <assert.h>

To name a few useful and common libraries.

Each library contains dozens of functions, structures,
and type declarations that will help us build a program.
When we include these in a file, it is like pasting
all the definitions at the top of our code.



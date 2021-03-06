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
Tiny programs keep all the code in main.c and
keep all the constants, includes and trash in main.h

As the project gets larger you will need to think
carefully about the easiestĺ way to organise your files

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

## Testing and Debugging

The compiler will probably provide enough information
to fix most syntax errors that might come along.

However, sometimes it will compile and run seamlessly but
still give the wrong output.

### Simple Approach

A common and simple approach with a tiny program is
to print the state of variables at each step of the
algorithm.

As you can imagine, this does not scale well.

However, if the program is fairly modular, we can
use this to confirm that each individual component 
is working as intended.
Then we can mute the output when we are finished.

Next we trace the progress of our algorithm by printing
the name of each function and the state of its arguments
as it is called.
Giving us a clear picture of where something is going awry.

Function calls inside a loop might be an issue though.

### Asserts

This is not so much a debugging aid as a preventative measure.
The assert macro exits the program if a specific condition
is not met.
For instance, assert(num != 0) will output an error
if num is 0.

Read this for more information:
https://ptolemy.berkeley.edu/~johnr/tutorials/assertions.html

The macro can be found in the assert.h library.
But there are many things that assert does not do
and so it can feel better to create your own functions.

### Testing suite

This is an approach favoured by test driven development
proponents.
https://en.m.wikipedia.org/wiki/Test-driven_development

In essence, you construct two programs.
The program that does the job, and a program that exists
only to test that the job is done correctly.

You create a list of the requirements of the program,
and then write test cases that would identify flaws.

It is then possible to link all the test cases for 
the individual components together into a comprehensive
test suite.

Then you can run this suite against any changes made to the
program. Pairing this with version control systems makes managing
a big project much easier.

### Assembly Debugging

This is often only necessary when the error is not in
your program, but with the compiler, the operating system
or a binary library that you've included in the project.

To do this you should learn assembly, x86 architectural 
design, linking, executable file formats and a
bunch of other stuff.

Otherwise it'll be hard to find the problem, and
even harder to fix it.

# Lesson 1 : C99 Standard

## 1. Overview

We have already discussed some concepts of the C programming language (beginner class) that were included in the C99 standard:<br>
- bool data type - stdbool.h (added true/false keywords)
- variable length arrays
- single line comments

However, we have mainly focused on the C89 standard in the beginner class<br>
I want it to be clear that some concepts in this class will include functionality from the C99 standard

## 2. History

C99 is a revised standard for the C programming language
- refines and expands the capabilities of Standard C

C99 has not been widely adopted
- not all popular C compilers support it
- of the compilers that do offer C99 support, most support only a subset of the language
so, we do not focus on many of the additions added for C99
- this is why the focus is mainly on C89.
C89 is almost universally supported.

# 3. New features added that we will use

macros with a variable number of arguments

C99 allows the use of sophisticated numbers (complex.h)
- _Complex: used to declare complex floating type variables to store mathematical complex numbers
- _Imaginaray: declare imaginary floating type variable store mathematical imaginary numbers

designated initializes
- allow you to initialize the elements of an array, union, or struct explicitly by subscipt or name

restricted pointers
- a type qualifier that can be used only for pointers

new comment techniques
- C99 allows to put comment using a double front slash

inline functions
- supplies a hint for the compiler to perform optimizations

variable length arrays
- array dimension has to be declared in C89
- C99 permits declaration of array dimensions using integer variables or any valid integer expressions

flexiable array members
- allows us to declare an array of unspecified length as the last member of a struct

declaration of variables
- it is now legal to declare variables it at any point of the program within the curly braces of main() function
- very obvious in loops

required in C89 (all variables be declared at the start of a block)<br>
int i;<br>
for (i = 0; i < 10, i++)

new in C99 (variable can be declared anywhere)<br>
for(int i = 0; i < 10; i++)









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

## 3. New features added that we will use

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

# Lesson 2 : C11 Standard

## 1. Overview

We have not really focused on any C11 concepts up to this point

Features added to C11 were for more advanced concepts
- multithreading support
- safer standard libraries
- better compliance with other industry standards

the standard also attempts to fix some issues presented in C99
- some mandatory features are optional (variable lenth arrays and complex types)

also focuses on better compatibility with C++ as much as possible

I want it to be clear that we may touch on some concepts from C11 in this class, but, it will be minial

## 2. Overview (cont'd)

C11 standardizes many features that have already been available in common contemporary implementations

defines a memory model that better suits multithreading

fixes problems with the C99 standard
- some of its mandatory features proved difficult to implement in some platforms
- politics also played a role : cooperation between the C and C++ standards committees in the late 1990s was lacking
- design mistakes of C99 were avoided in C11

focuses on security (such as the string manipulation functions and input/output)
- a new set of safer standard functions that aim to replace the traditional unsafe functions: bounds checking functions : that begin or end with _s (strcat_s, strcpy_s, etc)
- removal of the gets function
- optional to the standard (will not focus on due to most compilers not supporting)

## 3. Topics we will address in this class

suport for anonymous structs and unions
- has neither a tag name nor a typedef name
- useful when unions and structures are nested

static assertions
- evaluated during translations at a later phase than #if and #error
- let you catch errors that are impossible to detect during the preprocessing phase

no-return functions
- declares a function that does not return
- suppresses compiler warnings on a function that doesn't return
- enables certain optimizations that are allowed only on functions that don't return

## 4. Multithreading

the biggest change in C11 is its standardized multithreading support

C has supported multithreading for decades
- however, all of the popular C threading libraries have thus far been non-standard extensions, and hence non-portable

the new C11 header file <threads.h>
- declares functions for creating and managing threads, mutexes, condition variables

however, it is widely not supported on windows and thus we will be learning aboud <pthread.h> instead (posix compliant)

# Lesson 3 : Installing the C Compiler

## 1. Windows

Download cygwin to: https://cygwin.com/install.html<br>
Checked bin in packages: gcc-core, gdb, make<br>
Create PATH: Copy path: C:\cygwin64\bin to ThisPC->Properties->Advanced system settings->Advanced->Environment Variables...->System variables->Path->Edit->New->Paste(C:\cygwin64\bin)->OK<br>
Installing CodeLite

## 2. Mac

Go to AppStore->Develop->XCode->GET<br>
Utilites->Terminal then input "which gcc" -> input "gcc --version" -> install -> input "vi test.c" -> input "gcc test.c" -> input "./a.out"

## 3. Ubuntu Linux













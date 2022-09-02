# C - Preprocessor, Structures, typedef

## preprocessor

### **Learning Objectives**

### What are macros and how to use them
- An object-like macro is a simple identifier which will be replaced by a code fragment
- You create macros with the `#define` directive. Example: `#define BUFFER_SIZE 1024`
- There is no restriction on what can go in a macro body provided it decomposes into valid preprocessing tokens.
- Function-like macros can take arguments: Example: `#define min(X, Y)  ((X) < (Y) ? (X) : (Y))`

### What are the most common predefined macros
- `__DATE__`	current date as a character `MMM DD YYYY`
- `__TIME__`	current time defined as `HH:MM:SS`
- `__FILE__`	current filename as a string literal
- `__LINE__`	this contains the current line number
- `__STDC__`	defined as 1 when the compiler compiles with `ANSI` standar

### How to include guard your header files
- an **`#include guard`,** sometimes called a **macro guard, header guard** or **file guard,** is a particular construct used to avoid the problem of double inclusion when dealing with the include directive.
- Another construct to combat double inclusion is _`#pragma once`_
- We include them using **`#ifndef FILE_H #define FILE_H #endif`**


## Structures, typedef

### **Learning Objectives**

### What are structures, when, why and how to use them
- A structure is a user-defined data type that allows to combine data items of different types/kinds
- Structures can be defined in the global scope of the program (i.e., outside functions)
	- Example: `struct User {char * name; int age}`
	- Elements are accessed using . Example `User.name = “John”`
- To access elements of a pointer to a structure, we have to **dereference the pointer and then access data using .**
	- A simpler way: **`use ->.`** Example **`User->name = “John”`**

### How to use typedef
- Typedef is used to provide a data type with a new name. Example **`typedef unsigned char byte`**
- Typedef can also be used with structures

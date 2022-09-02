# C - Functions, Nested Loops, Debugging

## Functions, nested loops

### **Learning Objectives**

### What are nested loops and how to use them
- Nested loops are combinations of loops inside other loops.

### What is a function and how do you use functions
- A function is a group of statements that together perform a specific task. A function is defined by **function declaration** and **function definition**

### What is the difference between a declaration and a definition of a function
- Function declarations include the return type of the function, its name and the list of parameters it takes. A function definition is the part of the function where the implementation is provided

### What is a prototype
- Inclusions of functions without proper implementation inside the code, i.e., the forward declaration of a function
	- It tells the return type, number of arguments, order and data types of arguments

### Scope of variables
- Local variables can be used only inside their scope (e.g., function)
- Global variables can be used everywhere in the program
- Static variables allow the value to **persist between calls**

### What are the `gcc flags -Wall -Werror -pedantic -Wextra -std=gnu89`

### What are header files and how to to use them with #include 
- A header file is a file with extension `.h` which contains C function declarations and macro definitions to be shared between several source files
By using `#include<header_file>` we are notifying the compiler about their usage. `#include “header_file”` is used if `header_file` is defined by ourselves

## Debugging

### **Learning Objectives**

### What is debugging
- Debugging is the process of finding and fixing errors in software that prevents it from running correctly.

### What are some methods of debugging manually
- We can start by reading the errors carefully; then aiming to explain as simply as possible every single line of code (in the function causing the error) to avoid mistakes. (check: rubber duck debugging)

### How to read the error messages
- Refer to the specific line of code in a specific function and then aim to understand from there by trying to walk through the work-flow/execution of the program

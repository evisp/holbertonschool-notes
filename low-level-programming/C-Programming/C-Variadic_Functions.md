# C - Variadic functions

## Function pointers

### **Learning Objectives**

### What are variadic functions
- Variadic functions allow functions to accept an indefinite number of arguments. They are declared with an ellipsis **`(...)`** as the last parameter
- `va_start:` start iterating arguments with a `va_list`
- `va_arg:` retrieve an argument
- `va_end:` free a `va_list`
- `va_copy:` copy contents of one `va_list` to another

### How to use **`va_start,`** **`va_arg`** and **`va_end macros`**
- The type `va_list` is used for argument pointer variables.
- `va_start` initializes the argument pointer variable ap to point to the first of the optional arguments of the current function;
- `va_arg` returns the value of the next optional argument, and modifies the value of ap to point to the subsequent argument
- `va_end:` returns the value of the next optional argument, and modifies the value of ap to point to the subsequent argument

### Why and how to use the const type qualifier

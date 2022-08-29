# C - Variadic functions

## Function pointers

### **Learning Objectives**

### What are variadic functions
- Variadic functions allow functions to accept an indefinite number of arguments. They are declared with an ellipsis (...) as the last parameter
- va`_`start: start iterating arguments with a va`_`list
- va`_`arg: retrieve an argument
- va`_`end: free a va`_`list
- va`_`copy: copy contents of one va`_`list to another

### How to use va`_`start, va`_`arg and va`_`end macros
- The type va`_`list is used for argument pointer variables.
- va`_`start initializes the argument pointer variable ap to point to the first of the optional arguments of the current function;
- va`_`arg returns the value of the next optional argument, and modifies the value of ap to point to the subsequent argument
- va`_`end: returns the value of the next optional argument, and modifies the value of ap to point to the subsequent argument

### Why and how to use the const type qualifier

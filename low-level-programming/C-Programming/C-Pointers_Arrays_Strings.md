# Pointers, Arrays and Strings

### **Learning Objectives**

### What are pointers and how to use them
- A pointer is simply **the address of a piece of data in memory**. A pointer variable is a variable that stores the address of that piece of data
- Pointers are declared as: `var_type` `*var`; Variable var is a `pointer (*)` that points to a `var_type`. The value of var is a memory address holding a value of type `var_type`
- To get the address where a pointer is stored we use the `& operator.`
- A pointer can only point to a variable of the type it is supposed to point to
### - **`Dereferencing`**
 - The real power of pointers is that they can manipulate values stored at the memory address they point to. 
 - To do this, you can use the dereference `operator *.`
 - has a different meaning depending on the context
  - At declaration, it is used to declare a variable of type pointer, e.g., `int *n`
  - When used inside the code, it dereferenced pointers, e.g., `*n =88`
### - **`Pointers Arithmetic`**
 - Another way to access different elements of an array, is to use this other notation: `*(var + x)`, where var is the name of an array, and `x` is the `(x+1)th` element
 - E.g.: `i[5]` will be the same as `*(i + 5)`

### What are arrays and how to use them
- Arrays in C are contiguous memory areas that hold a number of values of the same type.
- To declare an array we use this syntax: type `var_name[number_of_elements];`
- We refer to an element as `a[0], a[1], ..,` if a is the array name. Indexes are stored from 0 to n-1 where n is the length of the array

### What are the differences between pointers and arrays
- an array is NOT a pointer, the variables we declare as arrays do not hold a memory address.

### How to use strings and how to manipulate them
- Strings are a list of characters

### Scope of variables

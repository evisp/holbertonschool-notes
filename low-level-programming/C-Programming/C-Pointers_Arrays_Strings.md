# Pointers, Arrays and Strings

## 🔑 Key Concepts

### **Learning Objectives**

### What are Pointers and How to Use Them

- A **pointer** is the memory address of a data element. It's a variable that stores this memory address.

- Pointers are declared as follows: `var_type *var;` Here, `var` is a variable of type `pointer (*)` that points to a `var_type`. The value of `var` is a memory address holding a value of type `var_type`.

- To obtain the address where a pointer is stored, we use the `&` operator.

- Crucially, a pointer can only point to a variable of the same data type it is supposed to point to.


### **Dereferencing**

- Pointers offer the remarkable ability to manipulate values stored at the memory address they point to.

- This manipulation is achieved by using the dereference `*` operator.

- The meaning of `*` varies depending on the context:
  - During declaration, it is used to declare a variable of pointer type, as in `int *n`.
  - When applied within the code, it dereferences pointers, allowing you to modify the value they point to, such as `*n = 88`.



### **Pointers Arithmetic**
- Another way to access different elements of an array, is to use this other notation: `*(var + x)`, where var is the name of an array, and `x` is the `(x+1)th` element
- E.g.: `i[5]` will be the same as `*(i + 5)`

## 🌐 Applications

## 🌐 Applications

Pointers play a crucial role in programming by enabling:

- **Dynamic Memory Management:** Pointers allow efficient allocation and deallocation of memory, which is essential for data structures like linked lists and dynamic arrays.

- **Efficient Data Structures:** Pointers are fundamental in building complex data structures like trees, graphs, and hash tables, optimizing data manipulation.

- **Direct Hardware Access:** In systems programming and embedded systems, pointers provide direct access to hardware components, facilitating device control.

- **Array Manipulation:** Pointers allow for efficient traversal and manipulation of arrays, leading to optimized algorithms for tasks like sorting and searching.

- **String Handling:** Pointers simplify string operations by providing direct access to characters, reducing memory overhead and enhancing performance.


## 🚀 Bringing Concepts to Life

### Setting the value of a pointer

- Write a function that takes a pointer to an int as parameter and updates the value it points to to `98`.

```c
#include "main.h"
/**
 * reset_to_98 - updates the value it points to 98
 * @n: value it points
 */
void reset_to_98(int *n)
{
	*n = 98;
}
```


## 📚 Further information

### What are arrays and how to use them
- Arrays in C are contiguous memory areas that hold a number of values of the same type.
- To declare an array we use this syntax: type `var_name[number_of_elements];`
- We refer to an element as `a[0], a[1], ..,` if a is the array name. Indexes are stored from 0 to n-1 where n is the length of the array

### What are the differences between pointers and arrays
- an array is NOT a pointer, the variables we declare as arrays do not hold a memory address.

### How to use strings and how to manipulate them
- Strings are a list of characters

### Scope of variables



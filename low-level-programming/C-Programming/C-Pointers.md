# Pointers

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

### Finding the length of a string

- Write a function that returns the length of a string

```c
#include "main.h"

/**
 * _strlen - Returns the length of a string
 * @s: String to be measured
 *
 * Return: Length of the string
 */
int _strlen(char *s)
{
    int length = 0;

    while (*s)
    {
        length++;
        s++;
    }

    return length;
}

```

### Reverse a string

- Write a function that reverses a string

```c
#include "main.h"

/**
 * rev_string - Reverses a string
 * @s: String to be reversed
 */
void rev_string(char *s)
{
    int length = 0;
    int start = 0;
    int end;
	char temp;

    while (s[length] != '\0')
        length++;

    end = length - 1;

    while (start < end)
    {
        temp = s[start];
        s[start] = s[end];
        s[end] = temp;
        start++;
        end--;
    }
}
```

### Print half of a string

- Write a function that prints the second half of a string, followed by a new line

```c
#include "main.h"

/**
 * puts_half - Prints the second half of a string
 * @str: String to be printed
 */
void puts_half(char *str)
{
    int length = 0;
    int n;

    while (str[length] != '\0')
        length++;

    n = (length + 1) / 2;

    while (str[n] != '\0')
    {
        _putchar(str[n]);
        n++;
    }

    _putchar('\n');
}

```

## Challenge

Write a function that convert a string to an integer.

- Prototype: `int _atoi(char *s)`;
- The number in the string can be preceded by an infinite number of characters
- You need to take into account all the `-` and `+` signs before the number
- If there are no numbers in the string, the function must return `0`

Can you write `C` code for the following pseudocode

```
Function _atoi(s)
    Initialize result as 0
    Initialize sign as 1
    Initialize i as 0
    
    # Ignore leading white spaces
    While s[i] is a white space
        Increment i by 1
        
    # Check for a sign
    If s[i] is '-'
        Set sign to -1
        Increment i by 1
    Else If s[i] is '+'
        Increment i by 1
    
    # Read the digits and convert to an integer
    While s[i] is a digit
        Multiply result by 10
        Add (s[i] - '0') to result
        Increment i by 1
        
    # Return the result with the appropriate sign
    Return result * sign
End Function

```
## 📚 Further information

- [Pointers in C by C-Programming](https://www.cprogramming.com/tutorial/c/lesson6.html)

- [Geeks for Geeks Pointers](https://www.geeksforgeeks.org/c-pointers/)

#### ✨ Remember

You don't need to be a great programmer. Just a good programmer with great habits. 


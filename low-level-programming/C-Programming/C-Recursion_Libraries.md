# C - Recursion

## Recursion

### **Learning Objectives**

### What is recursion
- Recursion is a method where the solution to a problem depends on solutions to smaller instances of the same problem. 
- A recursive function is a function that calls itself

### How to implement recursion
- Since a recursive function is a function that calls itself, one must always consider 
 - **Base criteria (Base Case):** There must be at least one base criteria or condition, such that, when this condition is met the function stops calling itself recursively.
 - **Recursive Step:** the recursive calls should progress in such a way that each time a recursive call is made it comes closer to the base criteria.

### In what situations you should implement recursion
- Recursion is made for solving problems that can be broken down into smaller, repetitive problems

### In what situations you shouldn’t implement recursion
- Generally, it is advisable to avoid recursion in situations where memory overflow and stack space used grow progressively fast.

# C -Static Libraries, argc, argv

## Static libraries

### **Learning Objectives**

### How to use arguments passed to your program
- We can enhance the declaration of our main function into **int main(int argc, char *argv[]).** 
- **argc** stands for arguments count, while **argv** is an array of pointers to the strings which are those arguments
- When running our programs, we can pass a series of arguments. The first argument (count = 1, value = argv[0]) is always the name of the program.

### What are two prototypes of main that you know of, and in which case do you use one or the other
- **int main (void)** does not take any arguments
- **int main(int argc, char *argv[]) /**  **int main(int argc, char **argv)** allows to take multiple arguments

### How to use `__`attribute`__`((unused)) or (void) to compile functions with unused variables or parameters
- The compiler can warn if a variable is declared but is never referenced. The __attribute__((unused)) attribute informs the compiler to expect an unused variable, and tells it not to issue a warning.

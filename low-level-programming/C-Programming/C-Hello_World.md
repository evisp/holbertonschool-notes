# C - Hello World

## Learning Objectives

### Why C Programming is awesome

- Almost all programming languages are based upon C
- Mars Rover software is written in C: how awesome is that?
- Language of choice for kernel development
- It has been around long enough and won't go anywhere

### Who invented C?

- Deniss Ritchie

### Who are Dennis Ritchie, Brian Kernighan and Linus Torvalds

- Dennis Ritchie: inventor of C
- Brian Kernighan: contributed to development of Unix, co-authored the first book on the C programming language
- Linus Torvalds: main developer of Linux kernel

### What happens when you type `gcc main.c`

- `gcc` is a compiler for the `C` language. It compiles the code written in file main. Key processes: **preprocessing, compilation, assembly** and **linking**

### What is `main`?

- Main is the entry point for c programs. It is the *root* function that calls all other functions and makes possible the workflow of the program

### How to print text using `printf`, `puts` and `putchar`

- `printf`: displays formatted output to stdout (`scanf` is the reverse)
- `puts`: writes the string a tailing new line to the console
- `putchar`: writes the character `c` to standard output and returns the character that was written (`getchar` is the reverse)

### How to get the size of a specific type using the unary operator `sizeof` 

- Can be used to determine the amount of size any intrinsic type, union or struct takes in bytes

### How to compile using `gcc`

- `gcc filename` compiles the program and creates an executable file, which we can then run on our terminal

### What is the default program name when compiling with `gcc` 

- `a.out`

### What is the official C coding style and how to check your code with betty-style 

- Linux-kernel like coding style. We can install betty style and run our code against it

### How does the `main` function influence the return value of the program

- The return type of the function determines the return value of the program

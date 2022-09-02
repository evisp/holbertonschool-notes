# Python - Hello World

## General

### Why Python programming is awesome

- Python is an easy to learn, powerful programming language. It has efficient high-level data structures and a simple but effective approach to object-oriented programming. Python’s elegant syntax and dynamic typing, together with its interpreted nature, make it an ideal language for scripting and rapid application development in many areas on most platforms.
- Python allows you to split your program into modules that can be reused in other Python programs. It comes with a large collection of standard modules that you can use as the basis of your programs 


### Who created Python

- Guido van Rossum

### Where does the name ‘`Python`’ come from

- The language is named after the BBC show “Monty Python’s Flying Circus” and has nothing to do with reptiles

### What is the Zen of Python

- The Zen of Python is a collection of 19 "guiding principles" for writing computer programs that influence the design of the Python programming language.

### How to use the Python interpreter

- Python is an interpreted language; no compilation and linking is necessary.

### How to print text and variables using `print`

- One can call the `print` method. Formatting can be done using `printf` style or string formatting through `f-string`

### How to use strings

- Strings are denoted in single, double or triple quotes. Special characters can be escaped using \ or simply by enclosing them within quotes. 
- Strings can be concatenated using `+`, or multiplied using `*`
- Strings can be used as arrays, i.e., indexing them starting at position `0`
- Python strings cannot be changed, they are immutable


### What are indexing and slicing in Python

- A string can be indexed from `0` to `len - 1` where `len` is the length of the strings. E.g `word = “Python”`; `word[0] = ‘P’`; `word[5] = ‘n’`
- Negative indexing can also be used. E.g `word[-1] = ‘n’`

### What is the official Python coding style and how to check your code with `pycodestyle` 

- `pycodestyle` is a tool to check your Python code against some of the style conventions

## Using the Python Interpreter

- The Python interpreter is usually installed as `/usr/local/bin/python3.X`
- When known to the interpreter, the script name and additional arguments thereafter
are turned into a list of strings and assigned to the `argv` variable in the sys module.
    - You can access this list by executing `import sys`

## Using Python as a Calculator

### Numbers

- The interpreter acts as a simple calculator: you can type an expression at it and it will write the value.
- the operators `+`, `-`, `*` and `/` work just like in most other languages
- The integer numbers have type `int`, the ones with a fractional part have type `float`
  - To do floor division and get an integer result you can use the `//` operator;
  to calculate the remainder you can use `%`

### Strings

- They can be enclosed in single quotes (`'...'`) or double quotes (`"..."`) with the same result
- If you don’t want characters prefaced by `\` to be interpreted as special characters,
you can use raw strings by adding an `r` before the first quote
- Strings can be indexed (subscripted), with the first character having index 0
  - negative indices start from -1.
- slicing is also supported. it allows you to get a portion of a string. For example: `word[:2]` or `word[4:]` or `word[-2:]`
- **String formatting**
  - `f-strings` make formatting easier

```Python
name = "Eric"
age = 74
f"Hello, {name}. You are {age}."
```

### Lists

- A list can be written as a list of comma-separated values (items) between square brackets.
- Lists might contain items of different types, but usually the items all have the same type
- Lists can be indexed and sliced
- Lists also support operations like concatenation
- Unlike strings, which are immutable, lists are a mutable type, i.e. it is possible to change their content

### First steps toward programming

- we can use Python for more complicated tasks. For instance, we can write an initial sub-sequence of the Fibonacci series as follows

```Python
a, b = 0, 1
while a < 10:
      print(a)
      a, b = b, a+b
```
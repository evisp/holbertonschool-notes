# Python - if/else, loops, functions

# General

## Why indentation is so important in Python

- Indentation refers to the spaces at the beginning of a code line.
- Where in other programming languages the indentation in code is for readability only, the indentation in Python is very important.
- Python uses indentation to indicate a block of code.

```Python
if 5 > 2:
   print("Five is greater than two!") 
if 5 > 2:
   print("Five is greater than two!")
```

## How to use the `if`, `if ... else` statements

- Perhaps the most well-known statement type is the `if` statement
- There can be zero or more `elif` parts, and the `else` part is optional

```Python
if x < 0:
   x = 0
   print('Negative changed to zero')
elif x == 0:
   print('Zero')
elif x == 1:
   print('Single')
else:
   print('More')
```

## How to use comments

- To add or mark a line as a comment, start with a hash sign (`#`) and a space:
  - `# this is a comment`
- Block comments are longer-form comments that consist of multiple lines in a row.
  - `# this is a block of comments\n`
  `# that runs on several lines`
- Multi line comments, known as **docstrings** are wrapped inside triple-quote marks (`"""`)
  - `""" This is a docstring documenting the declaration of a function """`

## How to affect values to variables

- The assignment operator, denoted by the “`=`” symbol, is the operator that is used to assign values to variables in Python.

## How to use the while and for loops

### The `for` loop

- The `for` statement in Python differs a bit from what you may be used to in `C`
-  Rather than always iterating over an arithmetic progression of numbers, or giving the user the ability to define both the iteration step and halting condition, **Python’s `for` statement iterates over the items of any sequence
in the order that they appear**. 
```Python
words = ['cat', 'window', 'defenestrate']
for w in words:
    print(w, len(w))
``` 

### The `range` function

- If you do need to iterate over a sequence of numbers, the built-in function `range()` comes in handy. It generates arithmetic progressions: Example `for i in range(5):` or `list(range(5, 10))`

### How to use the `break` and `continues` statements

- The `break` statement, like in `C`, breaks out of the innermost enclosing `for` or `while` loop.

### How to use `else` clauses on loops

- Loop statements may have an `else` clause; it is executed when the loop terminates through exhaustion of the iterable (with `for`) or when the condition becomes `false` (with `while`), but not when the loop is terminated by a `break` statement.

```Python
for n in range(2, 10):
    for x in range(2, n):
    	if n % x == 0:
	   print(n, 'equals', x, '*', n//x)
	   break
    else:
	print(n, 'is a prime number')	    
```

### What does the `pass` statement do, and when to use it

- The `pass` statement does nothing. It can be used when a statement is required syntactically but the program requires no action. For example:

## What is a function and how do you use functions

- A function is a block of code which only runs when it is called.
- You can pass data, known as parameters, into a function.
- A function can return data as a result.
- In Python a function is defined using the def keyword:

```Python
def my_function():
    print("Hello from a function")
```

- To call a function, use the function name followed by parenthesis: `my_function()`

### What does return a function that does not use any return statement

- If a function doesn't specify a return value, it returns `None`

## Scope of variables

- **Local Scope**
  - Local scope variables can only be accessed within its block.
- **Global Scope**
  - The variables that are declared in the global scope can be accessed from anywhere in the program. 
  - Global variables can be used inside any functions
- **Enclosing Scope**
  - A scope that isn’t local or global comes under enclosing scope
- **Built-in Scope**
  - This is the widest scope in Python. All the reserved names in Python built-in modules have a built-in scope.

## What’s a traceback

- A traceback is a report containing the function calls made in your code at a specific point. 
- Tracebacks are known by many names, including stack trace, stack traceback, backtrace, and maybe others. 
- In Python, the term used is traceback.
- When your program results in an exception, Python will print the current traceback to help you know what went wrong.

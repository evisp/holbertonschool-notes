# Import and Modules

- Python has a way to put definitions in a file and use them in a script or in an interactive instance of the interpreter.
- Such a file is called a **module**; definitions from a module can be imported into other modules or into the main module
- A module is a file containing Python definitions and statements. The file name is the module name with the suffix `.py` appended
- A module can contain executable statements as well as function definitions.
- These statements are intended to initialize the module. They are executed only the first time the module name is encountered in an import statement
- Modules can import other modules
- Example: `from fibo import fib, fib2`
- If the module name is followed by `as`, then the name following `as` is bound directly to the imported module.
  - `import fibo as fib`
- 

## How to import functions from another file and how to use them

- Approach:
  - Create a Python file containing the required functions.
  - Create another Python file and import the previous Python file into it.
  - Call the functions defined in the imported file.

```Python

# test.py
 
def display_text():
    print( "Python is cool!")

# in another file
from test import display_text
 
# calling functions
displayText()
```

## How to create a module

- To create a module just save the code you want in a file with the file extension `.py`
- Now we can use the module we just created, by using the `import` statement

## How to use the built-in function `dir()`

- The built-in function `dir()` is used to find out which names a module defines. It returns a sorted list of strings:

## How to prevent code in your script from being executed when imported

## How to use command line arguments with your Python programs

- These arguments are stored in the `sys` module’s `argv` attribute as a list
  - `print(sys.argv)`
- The `sys` module also has attributes for `stdin`, `stdout`, and `stderr`. The latter is useful for emitting warnings and error messages to make them visible even when stdout has been redirected:
  - `sys.stderr.write('Warning, log file not found starting a new one\n')`
  
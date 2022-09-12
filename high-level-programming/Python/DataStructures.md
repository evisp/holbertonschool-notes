# Data Structures

Python knows a number of compound data types, used to group together other values

## Lists

- A list can be written as a list of comma-separated values (items) between square brackets, `squares = [1, 4, 9, 16, 25]`
- Lists might contain items of different types, but usually the items all have the same type
- Lists can be indexed and sliced `squares[-3:]`
- Lists also support operations like concatenation `squares + [36, 49, 64, 81, 100]`
- lists are a mutable type, i.e. it is possible to change their content `squares[2] = 18`
- You can also add new items at the end of the list, by using the `append()` method
- The built-in function `len()` also applies to lists: `len(squares)`
- It is possible to nest lists (create lists containing other lists), for example: `my_list = [[1, 2], [3, 4, 5]]`
- Other methods include:
  - `list.append(x)` Add an item to the end of the list
  - `list.extend(iterable)` Extend the list by appending all the items from the iterable
  - `list.insert(i, x)` inserts an item at a given position
  - `list.remove(x)` Remove the first item from the list whose value is equal to x
  - `list.pop([i])` Remove the item at the given position in the list, and return it.
  - `list.clear()` removes all items from the list
  - `list.count(x), list.sort(), list.reverse(), list.copy()`
- To use a list as a stack, use methods `append()` and `pop()`

### List comprehension

- List comprehensions provide a concise way to create lists. Common applications are to make new lists where each element is the result of some operations applied to each member of another sequence or iterable
- Example: `squares = list(map(lambda x: x**2, range(10)))` or, equivalently, `squares = [x**2 for x in range(10)]`
- A list comprehension consists of brackets containing an expression followed by a for clause, then zero or more for or if clauses
  - Example: `[(x, y) for x in [1,2,3] for y in [3,1,4] if x != y]`
- Nested list comprehensions can also be created, as in: `[[row[i] for row in matrix] for i in range(4)]`

## Tuples and Sequences

- A tuple consists of a number of values separated by commas, for instance: `t = 12345, 54321, 'hello!'`
- Tuples may be nested as in `(u = t, (1, 2, 3, 4, 5))`
- Tuples are immutable
- Tuples are immutable, and usually contain a heterogeneous sequence of elements that are accessed via unpacking or indexing
- A special problem is the construction of tuples containing 0 or 1 items
  - Empty tuples are constructed by an empty pair of parentheses, `()`
  - a tuple with one item is constructed by following a value with a comma, `('hello',)`


## Sets

- A set is an unordered collection with no duplicate elements.
- Basic uses include membership testing and eliminating duplicate entries.
- Set objects also support mathematical operations like union, intersection, difference, and symmetric difference
- Curly braces or the `set()` function can be used to create sets. Note: to create an empty set you have to use `set()`, not `{}`
- Example: `basket = {'apple', 'orange', 'apple', 'pear', 'orange', 'banana'}`
- Similarly to list comprehensions, set comprehensions are also supported: `a = {x for x in 'abracadabra' if x not in 'abc'}`

## Dictionaries

- Dictionaries are sometimes found in other languages as “associative memories” or “associative arrays”
- Unlike sequences, which are indexed by a range of numbers, dictionaries are indexed by keys, which can be any immutable type
- Tuples can be used as keys if they contain only strings, numbers, or tuples; if a tuple contains any mutable object either directly or indirectly, it cannot be used as a key.
- **Think of a dictionary as a set of key: value pairs, with the requirement that the keys are unique**
- It is also possible to delete a key:value pair with `del`
- If you store using a key that is already in use, the old value associated with that key is forgotten.
- Performing `list(d)` on a dictionary returns a list of all the keys used in the dictionary, in insertion order


## Looping and comparison techniques

- When looping through dictionaries, the key and corresponding value can be retrieved at the same time using the `items()` method: `for k, v in my_dict.items():`
- When looping through a sequence, the position index and corresponding value can be retrieved at the same time using the `enumerate()` function: `for i, v in enumerate(['tic', 'tac', 'toe']):`
- To loop over two or more sequences at the same time, the entries can be paired with the `zip()` function:
```Python
questions = ['name', 'quest', 'favorite color']
answers = ['lancelot', 'the holy grail', 'blue']
for q, a in zip(questions, answers):
    print('What is your {q}?  It is {a}.')
```
- To loop over a sequence in reverse, first specify the sequence in a forward direction and then call the `reversed()` function `for i in reversed(range(1, 10, 2))`

### Conditions

- The comparison operators `in` and `not in` are membership tests that determine whether a value is in a container or not
- Comparisons can be chained as in `a < b == c`
- Comparisons may be combined using the Boolean operators `and` and `or`

### Comparing Sequences and Other Types

- Sequence objects typically may be compared to other objects with the same sequence type. The comparison uses lexicographical ordering
- Note that comparing objects of different types with `<` or `>` is legal provided that the objects have appropriate comparison methods

## Anonymous Functions. Lambda Expressions

### The `lambda` operator

- The `lambda` operator or lambda function is a way to create small anonymous functions, i.e. functions without a name
- Lambda functions are mainly used in combination with the functions `filter()`, `map()` and `reduce()`
  - Example: `sum = lambda x, y : x + y`
  
### The `map()` Function
- `map()` is a function which takes two arguments: `r = map(func, seq)`
- The first argument func is the name of a function and the second a sequence (e.g. a list) `seq`. `map()` applies the function func to all the elements of the sequence `seq`.

```Python
def fahrenheit(T):
    return ((float(9)/5)*T + 32)
def celsius(T):
    return (float(5)/9)*(T-32)
temperatures = (36.5, 37, 37.5, 38, 39)
F = map(fahrenheit, temperatures)
C = map(celsius, F)
temperatures_in_Fahrenheit = list(map(fahrenheit, temperatures))
temperatures_in_Celsius = list(map(celsius, temperatures_in_Fahrenheit))
```

### Filtering

- The function `filter(function, sequence)` offers an elegant way to filter out all the elements of a sequence "`sequence`", for which the function function returns `True`

```Python
fibonacci = [0,1,1,2,3,5,8,13,21,34,55]
odd_numbers = list(filter(lambda x: x % 2, fibonacci))
print(odd_numbers)
```

### Reducing

- `reduce()` had been dropped from the core of Python when migrating to Python 3
- The function `reduce(func, seq)` continually applies the function `func()` to the sequence `seq`. It returns a single value.

```Python
import functools
functools.reduce(lambda x,y: x+y, [47,11,42,13])
```
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
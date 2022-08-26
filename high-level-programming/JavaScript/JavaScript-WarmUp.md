# JavaScript - Warm Up

## Variables

### Declare:

- `let variableName`
- `var variableName`		old-fashioned and error-prone
- `const variableName`	for constants

## Data Types

### Primitive:
- `Numbers, Strings, Booleans, BigInt` 

### Special:

- `Null`, `Undefined`, `Symbol` (unique and immutable)

### Object

- value, writable, enumerable, configurable

### Indexed collections

- Arrays

### Keyed collections

- `Maps, Sets, WeakMaps, WeakSets` 
- Difference between `Map` and `WeakMaps`: the former allows for enumeration

### Structured data
- `JSON`

## Operators

- Arithmetic: `+`, `-,` `/`, `*`
- Assignment: `=`
- Strict equality: `===` checks if two values are equal; return true/false
- Not / does not: `!`, `!==`

## Program Flow

### Conditionals: 

- `if…else if…else` and
- `switch (expression)...case label_1: … default`

### Loops: 

- `while (condition) statements`…
- `for (initialization; condition; step)`
- `for…await of` creates a loop iterating over async iterable objects
- `for…in` iterates over all enumerable properties of an object that are keyed by strings. Example: `for (const variable in object)`
- `for…of` iterates over iterable objects. Example `for (variable of iterable)`

## Functions

Functions are reusable pieces of code that focus on doing only one task. Functions that are part of objects are called methods.

- **Declare**: `function myFunction()` {...}
- **Parameters**: functions can have optional and/or default parameters. 
- **Anonymous functions and arrow functions**: a function that has no name, as in `function() {....}` is known as an anonymous function. Anonymous functions are typically used when a function expects to receive another function as an argument. 
- **Arrow functions** are an alternative way of writing anonymous functions. Instead of writing `function(event)` we write `(event) =>`:

## Objects
Most things in JavasScript are objects. Objects are the most fundamental element of the Object Oriented Programming paradigm. 


### Objects basics:
- An object is a collection of related data and functionalities
- Declaration example: `const person = {}`

```javascript
const person = {
	name: [‘Bob’, ‘Smith’],
	age: 32;
	bio: function() {console.log(`${this.name[0]}` …)}
}
```

- Accessing properties: we can use the “**dot notation**” as in `person.name` or the “**bracket notation**” as in `person[name]`
- Setting properties: we can set values using both dot and bracket notation
- `this` keyword: refers to the current object the code is being written inside
- Constructors: allow to create and initialize objects

```javascript
function User() {
    this.name = 'Bob';
}
var user = new User();
```

- Constructors, by convention, start with a capital letter and are named for the type of 
object they create.

### Objects prototype:
- Prototypes are the mechanism by which JavaScript objects inherit features from one another
Every object in JavaScript has a built-in property, which is called its prototype. The prototype is itself an object, so the prototype will have its own prototype, making what's called a prototype chain

### Setting a prototype: 

- `create`:	the `Object.create()` method creates a new object and allows you to specify an object that will be used as the new object's prototype. 
- `constructor`: 	all functions have a property named `prototype`. When you call a function as a constructor, this property is set as the prototype of the newly constructed object
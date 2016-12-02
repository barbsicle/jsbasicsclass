# Chapter 1 - Types and Bulit-in Functions

## Overview

1. Storing Todos
2. Displaying Todos
3. Adding Todos
4. Changing Todos
5. Deleting Todos
6. Checking off Todos (optional for now)

------

## Part 1 - Storing Todos

### Commenting in code

* Use `//` in JS, and `<!-- -->` in HTML
* Comment often so you don't get lost

### Using `var`

* Use `var` to declare variables for persistent storage
* The primitive types:
    * `string`
    * `number` (Float)
    * `NaN` and `Infinity`
    * `boolean`
    * `undefined` & `null`
* The "other" types:
    * `Object`
    * `Array` (also talk about zero-indexing)
* Doing arithmetic:
    * `+`, `-`, `*`, `/`
    * `++` and `--`
    * `%` for remainder
    * `Math` object

* Conclusion: We can use arrays of objects to store todos
* Extra conclusion: We shall use strings first to simplify things
* Note: Use `;` after each line

------

## Part 2 - Displaying Todos

### The first basic function

* `console.log()`

### Exercise: Hello World!

### Exercise (from part 1): Adding two variables together

------

## Part 3 - Adding Todos/Changing Todos/Deleting Todos

### Array functions

* Calling a specific item with `[]`
* `push()` - add a new item
* `splice()` - remove an item at defined position

### Exercise: Pushing to array and splicing it

------

## Part 4 - Logic (Intermission)

### Understanding Boolean and "truthiness"

* `true` and `false`
* Truthiness of...
    * booleans
    * strings
    * numbers
    * undefined/null?

### Basic logical operators

* `if`
* Equality: `==` and `===`
* NOT: `!` (equality: `!==`)
* AND: `&&`
* OR: `||`
* [Extra] Short-circuiting
* [Extra] Ternary operator

* Exercise: Using booleans, perform a `true` and `false` return of each operator (can be combined and permutated)
* Exercise: Write a function that prints something if true, and something else if false.

### Example: Loops

* `for`
* `for x in object`
* `while` and `do/while`

```
for (var i = 0; i < 10; i++) {
    console.log("This is a looped line" + i);
}
````

* Exercise: FizzBuzz (Fizz on x3, Buzz on x5)

------

## [Next: Functions](chapter2.md)

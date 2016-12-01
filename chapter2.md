# Chapter 2 - Functions

## Overview

1. Displaying Todos
2. Adding Todos
3. Changing Todos
4. Deleting Todos

------

## Part 1 - Displaying Todos

### Example: Creating a function

* Naming the function
* The role of parantheses `()`
* Double curly brackets `{}`

```
myFunction() {
    console.log("hi!");
}
```

### Exercise: Write your first function

* Create a `displayTodos()` function
* Basically just `console.log()` the TodoList

------

## Part 2 - Adding Todos

### Example: Functions of functions

* Functions can run other functions
* Functions can run themselves (recursion, advanced topic)
* Exercise: Add the `displayTodos()` function after `push()`

```
myFunction() {
    console.log("hello");
}

myOtherFunction() {
    myFunction();
}
```

------

## Part 3 - Changing Todos/Deleting Todos

### Example: Function arguments

* We need the target index (`[]`) of the Todo to replace
* Then we need the new string to replace it with
* Therefore, the function needs two arguments

```
repeat(text) {
    console.log("Repeating text:", text);
}

...

repeat("I love Javascript.");
```

### Crafting the function

* The change function will need 2 defined "vars" in the parantheses; delete function will require 1
* Write the function relative to the arguments
* You can write a usecase first and then change it to the general variable
* Exercise: Write the function!

### Executing the function

* Input the two desired values to get the correct output

### Extra: The `return` statement

* Used to make the function evaluate to a values
* That value can be called without storing in a var
* Will also end the function execution

```
myFunction() {
    return "hello";
}

myOtherFunction() {
    console.log(myFunction() + "from the other side");
}
```

------

## [Next: Objects](chapter3.md)

# Chapter 4 - Manipulating Logic

## Overview

1. Refactoring Todos as Objects
2. Methods
    * Adding Todos
    * Changing Todos
    * Deleting Todos
    * Displaying Todos
3. New Methods
    * Toggling Todos

------

## Refactoring to Objects

### Generating the Object

* Up till now, we have been using strings
* Change each string to an Object with properties `name` (string) and `checked` (boolean)
* Furthermore, use a constructor to generate the objects

```
function Todo(name, checked) {
    this.name = name;
    this.checked = checked;
}

var sampleTodo = new Todo("do something", false);
```

### Refactoring the Methods

* Since the type of the todos has changed, the methods that act on them should be reviewed
* The `add` method needs to be refactored - it should create a new Todo object instead of a string
* The `change` method needs to be refactored - it should manipulate the `name` property of the todos
* The `delete` method does not need to be refactored

### Special Case: Displaying Todos

* Technically this does not need to be refactored, but say we just want the name of each todos
* We will need to **loop** through each of the items in `todoList.todos` and print its name
* We can also add functionality to print a "list is empty" message **if** there are no todos

Remember your loops:
```
for (var i = 0; i > 10; i++) {
    // do something
}
```

And your conditionals:
```
if (x) {
    // do someting
}
else if (y) {
    // do something else
}
else {
    // do something else else
}
```


### More special cases: guarding against exceptions

* Display: special message if the array is empty (done above)
* Add: do not allow adding of empty Todos
* Change: do not allow changing of Todo that does not exist
* Delete: do not allow deleting of Todo that does not exist

------

## Toggling Todos

### Creating the toggle method

* Write a function to toggle a specific todo (needs to find an index)
* The function will be a method in the TodoList object
* It will reach the specific todo and change `todo.checked` to true or false, depending

```
var x = true;
x = !x;  // x is now false
x = !x;  // x is now true
```

```
var myArray = ['item1', 'item2', 'item3'];
console.log(myArray[0]);  // 'item1'
console.log(myArray[1]);  // 'item2'
console.log(myArray[2]);  // 'item3'
```

### Modifying the display method (again)

* Now that we have incorporated the `checked` property, we should display whether a todo is checked or not
* Add to the `console.log` a bracket: `( )` when unchecked, and a bracketed x: `(x)` when checked

### Creating the `toggleAll()` method (anonymous functions and arrow functions)

* Similar to toggle, but now with a **loop** to toggle through everything
* Here would be a good point to teach `.forEach()` to manipulate arrays
* Point out that functions can take functions as their argument (higher order functions vs callback functions)
* The function in this argument is usually defined on the spot and anonymous
* An arrow function `list.forEach(item => { doSomething(); });` can be used in place of the longer syntax

### Example of `forEach()`

```
var myArray = [1, 2, 3];
myArray.forEach(entry => {entry = entry + 1});
```
* Extra: Is there any way we can shorten the code further?

------

## Complexity Increasing

* As complexity of functions increases, use the debugger to perform a step-by-step breakdown
* The `debugger;` keyword
* Highlighting breakpoints
* The `try`, `catch`, and `break` statements

------

## [Next: HTML Primer](chapter5.md)
# Chapter 6 - The DOM

## Overview

1. Functioning buttons
2. Attaching the function straight to the button
3. Retrieving information from elements

------

## Part 1 - Attaching functions to buttons

### Retrieving the button

* We have a button in HTML that we want to link to a JS function
* We need a way to identify this button with the `id` attribute
* Once that's done, we can use `document.getElementById()` to retrieve the button in JS
* You can `console.log` this new var to check if its correct
* Note: Remember to have the script tag right at the bottom

HTML:
```
<p id="example">Example Paragraph</p>
```

JS:
```
var myParagraph = document.getElementById("example");
```

### Attaching the listener

* A button (and any other HTML element) is just another JS object, and it has methods
* A method we can call is `addEventListener()` which takes 2 arguments
    * A string argument corresponding to the event (search online for detailed list)
    * A callback function, or the function to run when the event is triggered (a method from `todoList`)
* Once the `displayTodos()` function is attached, we can try clicking the button to see what happens
* Note that the output is still in the console.

HTML:
```
<button id="example">Example Button</button>
```

JS:
```
var myButton = document.getElementById("example");
myButton.addEventListener("click", () => {
    // perform your function here
})
```


### Repeating the process

* Attach the `toggleAll()` function to the respective button, using the steps above

------

## Part 2 - A `handlers` object

### Shifting all the callback functions

* This is a bit roundabout, but we can start with a `handlers` object
* Under this object, we list down a few functions copied from the event listeners
* Technically we do not need a `handlers` object, but this helps organise things

### Attaching the function directly to the buttons
* Using the `onclick` attribute, we link the buttons straight to the respective method in `handlers`
* This is so we no longer need to do the `addEventListener()` when it comes to clicking buttons
* `addEventListener()` is still very useful for other events

HTML
```
<button onclick="myFunction()">Example Button</button
```

------

## Part 3 - Retrieving information

### Adding Todos

* We attach an `id` to the text input field
* In the function, we retrieve this text input field as a string with `document.getElementById()`
* We can now manipulate the `value` of this variable
* Pass the variable to the `addTodos()` function
* Check the result!
* Lastly, you should do some cleanup by clearing the field (manipulate the `value` property)

HTML:
```
<input id="myInput" type="text" placeholder="Type a todo..."></input>
```

JS:
```
var myInput = document.getElementById("myInput");
var text = myInput.value;
```


### Changing Todos

* Similar to the add button, we need 2 inputs now (1 for position, 1 for new text)
* Position should be an `input` of `type=number`, text should be an `input` of `type=text`
* When retrieving values, the position should be `.valueAsNumber` instead of `.value`
* The rest is straightforward and the same as adding todos

### Deleting Todos

* This should be an easy repeated exercise which only requires 1 number input
* Follow the steps above

### Toggle Todos (not for now)

* Again this is similar to the above examples
* We may not want to touch this if we actually want a proper toggle (i.e. by clicking the element)
* The above is only possible once we render our TodoList in the DOM properly
* Which will be in the next chapter

------

## [Next: The DOM Part II](chapter7.md)

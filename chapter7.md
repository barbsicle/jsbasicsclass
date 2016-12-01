# Chapter 7 - The DOM Part II

## Overview

1. Creating elements in JS
2. Manipulating the created elements
3. More advanced element creation and manipulation
4. Updating the DOM

------

## Creating the list of Todos

### Example: Adding children to an element

* We should have already created an empty list `<li>` in the HTML
* We now need to add `<li>` elements to that list
* Create an element with `document.createElement`
* You can manipualte that element's value etc. as usual
* Target the list with either `document.querySelector('ul')` or `document.getElementById()`
* Use the `appendChild()` method to add a child to the `<ul>`

### Exercise: Supplementing the `displayTodos()` function

* Now, back in our js file, we should factor the above into our `displayTodos()` method
* Create a new object called `view`
* Create a `displayTodos()` method in `view`:
    * Should generate as many `<li>` elements as there are Todos (hint: use a loop)
    * Should clear the `<ul>` before generating again (using `.innerHTML` property)
    * Each `<li>` element needs to have the `name` of the respective Todo as its `.textContent` property
    * Each `<li>` element needs to represent the `checked` property of its respective Todo either as `(x)` or with `style.textDecoration=line-through`

------

## Making each Todo clickable

### Creating a button element

* Create a new function for `createDeleteButton()`
* The function will return a button
* Attach this button to the `<li>` with the `displayTodos()` method

### Adding an identifier to each Todo

* In the `displayTodos()` method, add an id which corresponds to the index of the todo to each `<li>`

### Attaching a function to each button

* We need to read the id of the `<li>` whenever we click the delete button
* One way to do this is by adding a click event listener to the whole list and grabbing `event.target.parent`
* Another way could just be to add the click event listener when you create the delete button
* Using the information from above, we can modify `createDeleteButton()` to take an argument which will be the id
* In the `createDeleteButton()` function, add a click event listener that fires the `deleteTodo()` function
* Lastly, remember to refresh the view with `view.displayTodos()` once the target todo is deleted

### Exercise: Check off Todos

* Similarly, we can add a function to each li to check its respective todo
* We can try that after adding delete buttons

------

## We're Done! [Endnotes](chapter8.md)

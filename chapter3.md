# Chapter 3 - Objects

## Overview

1. TodoList on Object
2. Methods
    * Displaying Todos
    * Adding Todos
    * Changing Todos
    * Deleting Todos

------

## Introduction to Objects

### The Object

* A very abstract concept...think of it like what you would define an "object" or "thing" in the real world
* Type that takes the form of `{ }`
* Has properties and keys in a `property:key` format
* Each property can be a different type
* Each property can be manipulated (mutable)
* Can have varying complexities (Array, Function)
* A function in an object is known as a method
* `new` keyword
* `this` keyword

### Example: Creating a car object
Without constructor:
```
var myCar = {
    color: "red",
    brand: "honda",
    wheels: 4,
    horn: function() {
        console.log("Beep beep!");
    }
}
```

With constructor:
```
function Car(color, brand, wheels) {
    this.color = color;
    this.brand = brand;
    this.wheels = wheels;
    function horn() {
        console.log("Beep beep beep!);
    };
}

var myCar = new Car("silver", "toyota", 4);
```

### Exercise: Migrating the TodoList to an Object

* Create a property for the Todos Array
* Create a property to display the Todos
* Create a property to add the Todos
* Create a property to change the Todos
* Create a property to delete the Todos

* Note: Each method can be adapted from the previous chapter's functions

------

## [Next: Manipulating Logic](chapter4.md)

## React - Conditional Rendering
In React, you can create distinct components that encapsulate behavior you need. Then, you can render only some of them, depending on the state of your application.
Conditional rendering in React works the same way conditions work in JavaScript. Use JavaScript operators like if or the conditional operator to create elements representing the current state, and let React update the UI to match them.
Element Variables
You can use variables to store elements. This can help you conditionally render a part of the component while the rest of the output doesn’t change.
While declaring a variable and using an if statement is a fine way to conditionally render a component, sometimes you might want to use a shorter syntax
Inline If with Logical && Operator
You may embed expressions in JSX by wrapping them in curly braces. This includes the JavaScript logical && operator
It works because in JavaScript, true && expression always evaluates to expression, and false && expression always evaluates to false.
Inline If-Else with Conditional Operator
Another method for conditionally rendering elements inline is to use the JavaScript conditional operator condition ? true : false.
Preventing Component from Rendering
component to hide itself even though it was rendered by another component. To do this return null instead of its render output.

## Lists and Keys
Given the code below, we use the map() function to take an array of numbers and double their values.
We assign the new array returned by map() to the variable doubled and log it.

## Basic List Component
Usually you would render lists inside a component.
We can refactor the previous example into a component that accepts an array of numbers and outputs a list of elements.
When you run this code, you’ll be given a warning that a key should be provided for list items.
A “key” is a special string attribute you need to include when creating lists of elements.

## Keys
Keys help React identify which items have changed, are added, or are removed.
Keys should be given to the elements inside the array to give the elements a stable identity.
The best way to pick a key is to use a string that uniquely identifies a list item among its siblings.
When you don’t have stable IDs for rendered items, you may use the item index as a key as a last resort.

## Forms:
HTML form elements work a bit differently from other DOM elements in React, because form elements naturally keep some internal state.
In React, mutable state is typically kept in the state property of components, and only updated with setState().
The textarea Tag
In HTML, a < textarea > element defines its text by its children
The select Tag:
In HTML, < select > creates a drop-down list
The file input Tag
In HTML, an  lets the user choose one or more files from their device storage to be uploaded to a server or manipulated by JavaScript via the File API.
Controlled Input Null Value
Specifying the value prop on a controlled component prevents the user from changing the input unless you desire so. If you’ve specified a value but the input is still editable, you may have accidentally set value to undefined or null.

## Composition vs Inheritance
Inheritance
Object Oriented Programming are well aware of Inheritance and use it on a regular basis. When a child class derives properties from it’s parent class,
Composition
is also a familiar concept in Object Oriented Programming. Instead of inheriting properties from a base class, it describes a class that can reference one or more objects of another class as instances

# ES6 Syntax and Feature Overview

### Legend
I'm not a fan of foo bar baz. Here is a key of most identifier names used throughout this reference.

Variable: x
Object: obj
Array: arr
Function: func
Parameter, method: a, b, c
String: str

### Table of contents
Variable declaration
Constant declaration
Arrow function syntax
Template literals
Implicit returns
Key/property shorthand
Method definition shorthand
Destructuring (object matching)
Array iteration (looping)
Default parameters
Spread syntax
Classes/constructor functions
Inheritance
Modules - export/import
Promises/callbacks

### Variables and constant feature comparison
I explain the concepts of scope and the differences between let, var,
and const in the Understanding Variables, Scope, and Hoisting in JavaScript resource on DigitalOcean. This table provides a brief overview.

### Variable declaration
ES6 introduced the let keyword, which allows for block-scoped variables which cannot be hoisted or redeclared.

### Constant declaration
ES6 introduced the const keyword, which cannot be redeclared or reassigned, but is not immutable.

### Arrow functions
The arrow function expression syntax is a shorter way of creating a function expression. Arrow functions do not have their own this, do not have prototypes, cannot be used for constructors, and should not be used as object methods.

### Template literals
Concatenation/string interpolation
Expressions can be embedded in template literal strings.

### Multi-line strings
Using template literal syntax, a JavaScript string can span multiple lines without the need for concatenation.

### mplicit returns
The return keyword is implied and can be omitted if using arrow functions without a block body.

### Key/property shorthand
ES6 introduces a shorter notation for assigning properties to variables of the same name.

### Promises/Callbacks
Promises represent the completion of an asynchronous function. They can be used as an alternative to chaining functions.

# React

### React - Hello World
```
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);

```
#### How to Read This Guide
In this guide, we will examine the building blocks of React apps: elements and components. Once you master them, you can create complex apps from small reusable pieces.

### React - JSX
```
const element = <h1>Hello, world!</h1>;
```
This funny tag syntax is neither a string nor HTML.
It is called JSX, and it is a syntax extension to JavaScript. We recommend using it with React to describe what the UI should look like. JSX may remind you of a template language, but it comes with the full power of JavaScript.
JSX produces React “elements”. We will explore rendering them to the DOM in the next section. Below, you can find the basics of JSX necessary to get you started.

#### Why JSX?
React embraces the fact that rendering logic is inherently coupled with other UI logic: how events are handled, how the state changes over time, and how the data is prepared for display.
Instead of artificially separating technologies by putting markup and logic in separate files, React separates concerns with loosely coupled units called “components” that contain both. We will come back to components in a further section, but if you’re not yet comfortable putting markup in JS, this talk might convince you otherwise.

#### Embedding Expressions in JSX
In the example below, we declare a variable called name and then use it inside JSX by wrapping it in curly braces:
```
const name = 'Josh Perez';
const element = <h1>Hello, {name}</h1>;

ReactDOM.render(
  element,
  document.getElementById('root')
);
```
### React - Rendering Elements
Rendering an Element into the DOM
Let’s say there is a <div> somewhere in your HTML file:
  
```
<div id="root"></div> 
```
We call this a “root” DOM node because everything inside it will be managed by React DOM.
Applications built with just React usually have a single root DOM node. If you are integrating React into an existing app, you may have as many isolated root DOM nodes as you like.

#### Updating the Rendered Element
React elements are immutable. Once you create an element, you can’t change its children or attributes. An element is like a single frame in a movie: it represents the UI at a certain point in time.
With our knowledge so far, the only way to update the UI is to create a new element, and pass it to ReactDOM.render().
  
#### React Only Updates What’s Necessary
React DOM compares the element and its children to the previous one, and only applies the DOM updates necessary to bring the DOM to the desired state.
 
### React - Components & Props
#### Components and Props
Components let you split the UI into independent, reusable pieces, and think about each piece in isolation. This page provides an introduction to the idea of components. You can find a detailed component API reference here.
Conceptually, components are like JavaScript functions. They accept arbitrary inputs (called “props”) and return React elements describing what should appear on the screen.
 
#### Composing Components
Components can refer to other components in their output. This lets us use the same component abstraction for any level of detail. A button, a form, a dialog, a screen: in React apps, all those are commonly expressed as components.

#### Extracting Components
Don’t be afraid to split components into smaller components.
It accepts author (an object), text (a string), and date (a date) as props, and describes a comment on a social media website.
This component can be tricky to change because of all the nesting, and it is also hard to reuse individual parts of it. Let’s extract a few components from it. 
  
#### Props are Read-Only
Whether you declare a component as a function or a class, it must never modify its own props.
  
### React - State & Lifecycle
This page introduces the concept of state and lifecycle in a React component. You can find a detailed component API reference here.
Consider the ticking clock example from one of the previous sections. In Rendering Elements, we have only learned one way to update the UI. We call ReactDOM.render() to change the rendered output: 

### React - Handling Events 
Handling events with React elements is very similar to handling events on DOM elements. There are some syntax differences:
React events are named using camelCase, rather than lowercase.
With JSX you pass a function as the event handler, rather than a string.  
  
Passing Arguments to Event Handlers
Inside a loop, it is common to want to pass an extra parameter to an event handler. For example, if id is the row ID, either of the following would work:
  
```
  <button onClick={(e) => this.deleteRow(id, e)}>Delete Row</button>
  <button onClick={this.deleteRow.bind(this, id)}>Delete Row</button>
```
The above two lines are equivalent, and use arrow functions and Function.prototype.bind respectively.
  
  
# Utility-first CSS
Alternatively, you can use an unopinionated approach, such as utility-first CSS, which removes the problems caused by using bespoke CSS or frameworks.

Utility-first CSS frameworks give a constrained set of primitive classes, called utilities, that are not named semantically and usually apply a single style, such as margin-bottom. Using a utility-first CSS framework, such as Tailwind CSS, lets you customise and access pre-existing utility classes and apply them directly to your HTML.

In fact, most CSS frameworks already have some utility classes in their systems. Bootstrap has a large list of utility classes to let you add styles alongside components, including:

Borders: weight, colour, and radius
Colours: text, backgrounds, and gradients
Display: inline, block, flex, and hidden
Position: static, relative, absolute, fixed, and sticky
Spacing: margin and padding
Text: alignment, wrapping, font weight, decoration, and transform
…etc.
 
# Next.js
## Next.js: The React Framework
Enter Next.js, the React Framework. Next.js provides a solution to all of the above problems. But more importantly, it puts you and your team in the pit of success when building React applications.
Next.js aims to have best-in-class developer experience and many built-in features, such as:

An intuitive page-based routing system (with support for dynamic routes)
Pre-rendering, both static generation (SSG) and server-side rendering (SSR) are supported on a per-page basis
Automatic code splitting for faster page loads
Client-side routing with optimized prefetching
Built-in CSS and Sass support, and support for any CSS-in-JS library
Development environment with Fast Refresh support
API routes to build API endpoints with Serverless Functions
Fully extendable
Next.js is used in tens of thousands of production-facing websites and web applications, including many of the world's largest brands.

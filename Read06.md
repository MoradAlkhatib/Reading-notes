# Functions [JavaScript Function](https://www.w3schools.com/js/js_functions.asp)

Functions are one of the fundamental building blocks in JavaScript. A function in JavaScript is similar to a procedure—a set of statements that performs a task or calculates a value, but for a procedure to qualify as a function, it should take some input and return an output where there is some obvious relationship between the input and the output. To use a function, you must define it somewhere in the scope from which you wish to call it.

## Defining functions
### Function declarations
A function definition (also called a function declaration, or function statement) consists of the function keyword, followed by:

The name of the function.
A list of parameters to the function, enclosed in parentheses and separated by commas.
The JavaScript statements that define the function, enclosed in curly brackets, {...}.
For example, the following code defines a simple function named square:

### function square(number) {
   return number * number;
### }


## Calling functions
Defining a function does not execute it. Defining it names the function and specifies what to do when the function is called.

Calling the function actually performs the specified actions with the indicated parameters. For example, if you define the function square, you could call it as follows:

### square(5);

## Function parameters [ parameters Of JavaScript](https://www.w3schools.com/js/js_function_parameters.asp)
Starting with ECMAScript 2015, there are two new kinds of parameters: default parameters and rest parameters.

Default parameters
In JavaScript, parameters of functions default to undefined. However, in some situations it might be useful to set a different default value. This is exactly what default parameters do.

Without default parameters (pre-ECMAScript 2015)
In the past, the general strategy for setting defaults was to test parameter values in the body of the function and assign a value if they are undefined.

In the following example, if no value is provided for b, its value would be undefined when evaluating a*b, and a call to multiply would normally have returned NaN. However, this is prevented by the second line in this example:

### function multiply(a, b) {
  b = typeof b !== 'undefined' ?  b : 1;

  return a * b;
### }

### multiply(5); // 5

# More Examples [Function Examples](https://www.programiz.com/javascript/function)

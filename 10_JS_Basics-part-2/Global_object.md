# Global Object in JavaScript

## Introduction

In JavaScript, the Global Object is a special object that serves as the root of the scope chain. It provides access to built-in properties, functions, and other objects that are available throughout your entire JavaScript program. Understanding the Global Object is important for accessing global variables, using global functions, and working with standard built-in objects. 
In this tutorial, we'll explore the Global Object in JavaScript and provide sample code snippets with comments to help you understand its usage.

## The Global Object in Browsers and Node.js

In web browsers, the Global Object is referred to as the `window` object. It represents the global scope and provides access to the global environment, including the global variables and functions.

In Node.js (server-side JavaScript), the Global Object is referred to as the `global` object. It works similarly to the `window` object in browsers but in a server environment.

## Sample Code with Comments

```javascript
// Global variable
var globalVar = "I am a global variable";

function exampleFunction() {
  // Local variable
  var localVar = "I am a local variable";
  console.log(localVar); // Output: I am a local variable

  // Accessing the global variable
  console.log(globalVar); // Output: I am a global variable
  console.log(window.globalVar); // Output: I am a global variable (in a browser environment)

  // Global function
  function globalFunction() {
    console.log("I am a global function");
  }

  // Accessing the global function
  globalFunction(); // Output: I am a global function
  window.globalFunction(); // Output: I am a global function (in a browser environment)
}

exampleFunction();

// Accessing the global variable outside the function
console.log(globalVar); // Output: I am a global variable

// Accessing the global function outside the function
globalFunction(); // Output: I am a global function (if globalFunction is defined in the global scope)
window.globalFunction(); // Output: I am a global function (in a browser environment, if globalFunction is defined in the global scope)
```

## Built-in Global Properties and Functions

The Global Object provides access to several built-in global properties and functions, such as:

### Global Properties

- `Infinity`: Represents positive infinity value.
- `NaN`: Represents "Not-a-Number" value.
- `undefined`: Represents undefined value.
- `null`: Represents null value.

### Global Functions

- `parseInt()`: Parses a string and returns an integer.
- `parseFloat()`: Parses a string and returns a floating-point number.
- `isNaN()`: Checks if a value is NaN.
- `isFinite()`: Checks if a value is a finite number.
- `eval()`: Evaluates a JavaScript expression or statement.
- `decodeURI()`: Decodes a Uniform Resource Identifier (URI).
- `encodeURI()`: Encodes a Uniform Resource Identifier (URI).
- `decodeURIComponent()`: Decodes a component of a URI.
- `encodeURIComponent()`: Encodes a component of a URI.
- `setTimeout()`: Executes a function after a specified delay.

## Conclusion

In this tutorial, we learned about the Global Object in JavaScript, which is the root of the scope chain and provides access to global variables, functions, and built-in properties. In a browser environment, the Global Object is referred to as `window`, while in Node.js, it is referred to as `global`. Understanding the Global Object is important for accessing and working with global variables and functions throughout your JavaScript program. 
Knowing the built-in global properties and functions provided by the Global Object can also be beneficial for various tasks in your code. Happy coding!
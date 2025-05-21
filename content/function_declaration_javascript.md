+++
date = '2025-01-14T18:55:24+03:00'
title = 'Function Declaration in JavaScript'
categories = [ "javascript" ]
+++

Function Declaration is one of the ways to create functions in JavaScript.

### Syntax of Function Declaration

```js
function functionName(parameters) {
  // function body
}
```

- `function` — keyword used to declare a function.
- `functionName` — name of the function, used to call it.
- `parameters` — arguments passed to the function (optional).
- `function body` — code that is executed when the function is called.

### Example

```js
function sayHello() {
  console.log('Hello!');
}

sayHello(); 
// Output: Hello!
```

### Features of Function Declaration

- Functions declared this way are hoisted, meaning they can be called before they are defined in the code.
- It's the most common and readable way to define a function.

### Summary

Function Declarations are a basic building block of JavaScript and are essential for organizing and reusing code.
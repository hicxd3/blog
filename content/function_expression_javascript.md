+++
date = '2025-01-14T19:55:24+03:00'
title = 'Function Expression in JavaScript'
categories = [ "javascript" ]
+++

A **Function Expression** is a way to define a function in JavaScript as part of an expression (for example, by assigning it to a variable). Unlike a Function Declaration, a Function Expression is **not hoisted** and can be either anonymous or named.

### Syntax of Function Expression
```js
const variableName = function(parameters) {
  // function body
};
```

- `function` — the keyword used to create the function.
- `variableName` — the variable that stores the function.
- `parameters` — arguments passed to the function (optional).
- `function body` — the code executed when the function is called.

### Example of a Function Expression
```js
const greet = function(name) {
  console.log(`Hello, ${name}!`);
};

greet("Elle"); 
// Hello, Elle!
```

### No Hoisting

Function Expressions are **not hoisted** to the top of their scope. This means they can only be called after their definition:

```js
greet("Elle"); 
// Error: greet is not defined

const greet = function(name) {
  console.log(`Hello, ${name}!`);
};
```

### Anonymous Function Expression

Function Expressions can be anonymous (without a name):

```js
const sum = function(a, b) {
  return a + b;
};
console.log(sum(2, 3)); 
// 5
```

A Function Expression is created only when the execution reaches it.

### When to Use Function Expressions

- For creating **closures**, where a function keeps access to variables from an outer scope.
- When you want a function to be created **conditionally** during runtime.
- For passing a function as an **argument** (e.g., in callbacks).

---

Function Expressions are a flexible way to define functions in JavaScript. They allow for anonymous or named functions that can be used in callbacks, object methods, closures, and more.

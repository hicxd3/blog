+++
date = '2025-01-15T18:53:24+03:00'
title = 'Arguments in JavaScript Functions'
categories = [ "javascript" ]
+++

In JavaScript, arguments are the values passed into a function when it is called. They allow functions to receive and work with data. Arguments can be of any type: numbers, strings, objects, arrays, functions, and so on.

There is a distinction between *parameters* and arguments in JavaScript:

Function parameters are the variables listed in the function definition. They are placeholders used to receive the arguments passed during a function call.

```js
function greet(name) { // name — parameter
  console.log(`Hello, ${name}!`);
}
```

Function arguments are the actual values provided when the function is called.

```js 
greet("Elle"); // "Elle" — argument
```

Arguments Are Passed by Value - Primitive types (numbers, strings, booleans) are passed by value. This means the function gets a copy, and any changes do not affect the original variable. Objects and arrays are passed by reference. The function works with the original object, so any changes will affect it outside the function.

```js
function changeValue(a, b) {
  a = 10;
  b.value = 20;
}

let num = 5;
let obj = { value: 15 };

changeValue(num, obj);
console.log(num);       // 5 (unchanged)
console.log(obj.value); // 20 (modified)
```

Functions Can Accept Any Number of Arguments - If more arguments are passed than parameters, the extra ones are ignored. If fewer arguments are passed, the missing parameters are set to undefined.

```js
function sum(a, b) {
  return a + b;
}

console.log(sum(1, 2, 3)); // 3 (third argument ignored)
console.log(sum(1));       // NaN (b = undefined → 1 + undefined = NaN)
```

Examples of Argument Usage

Simple function with arguments:

```js
function add(a, b) {
  return a + b;
}

console.log(add(2, 3)); // 5
```

Function with default parameters:

```js
function greet(name = "Guest") {
  console.log(`Hello, ${name}!`);
}

greet();        // Hello, Guest!
greet("Elle");  // Hello, Elle!
```

Summary: 

Arguments are the values passed to a function.

Parameters are the variables used to handle those values.

JavaScript functions can accept any number of arguments — use them wisely.
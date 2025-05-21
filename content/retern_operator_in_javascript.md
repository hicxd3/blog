+++
date = '2025-01-15T19:53:24+03:00'
title = 'The return operator in Javascript'
categories = [ "javascript" ]
+++

The `return` operator in JavaScript is used to return a value from a function. When the interpreter encounters a `return`, the function execution stops, and control returns to where the function was called. If a value is specified after `return`, it is returned as the result of the function.

`return` can return any value: a number, string, object, array, other function, and even `null` or `undefined`.

As soon as the `return` is executed, the function immediately completes its work. The code that is after the `return' is not executed.

If `return` is used without a value, the function returns `undefined`.

```js
function functionName() {
// Function code
  return value; 
  // Return the value and end the function
}
```

Returning a number:

```js
function sum(a, b) {
  return a + b; // Returns the sum of a and b
}

const result = sum(2, 3); // result = 5
console.log(result); // Outputs: 5
```

String Return:

```js
function greet(name) {
  return "Hello, " + name +"!";
}

const message = greet("Elle"); // message = "Hello, Elle!"
console.log(message); // Outputs: "Hello, Elle!"
```

Object return:
```js
function createUser(name, age) {
  return { name: name, age: age }; // Returns an object
}

const user = createUser("Mia", 25);
console.log(user); // Outputs: { name: "Mia", age: 25 }
```

Return without value:
```js
function doSomething() {
console.log("Doing something...");
  return; // The function terminates, returns undefined
  console.log("This code will not execute");
}

const result = doSomething(); // result = undefined
console.log(result); // Outputs: undefined
```

`return` can be used to terminate a function early if no further code execution is required.

```js
function checkAge(age) {
  if (age < 18) {
return "Access denied"; // The function ends if age < 18
}
return "Access allowed"; // Executed if age >= 18
}

console.log(checkOut(15)); // Outputs: "Access denied"
console.log(checkOut(20)); // Outputs: "Access is allowed"
```

Using return makes functions more flexible and powerful, allowing them to interact with the rest of the code.
+++
date = '2025-05-02T00:00:24+03:00'
title = 'Constructor Functions and new Function in JavaScript'
categories = [ "javascript" ]
+++


A constructor function is a regular function used to create multiple objects with the same structure. By convention, the function name starts with a capital letter, and we use this inside the function to assign properties.

Example — creating a constructor function:

```javascript
function User(name, age) {
  this.name = name;
  this.age = age;
}

const user1 = new User('Mia', 27);
console.log(user1.name); // Mia
```

We create a new object by using the new keyword with the constructor function.

Another way to create a function is using the Function constructor:

```javascript
const sum = new Function('a', 'b', 'return a + b');
console.log(sum(2, 3)); // 5
```

The Function constructor takes strings for the argument names and the function body.

Note: Using new Function is rare and generally discouraged in modern code because it creates functions from strings, similar to eval, and may have security risks. It is better to use regular function declarations or expressions.

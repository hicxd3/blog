+++
date = '2025-01-08T19:53:24+03:00'
title = 'Interpolation in JavaScript'
categories = [ "javascript" ]
+++

Interpolation in JavaScript is a way to insert variable values or expressions directly into a string. 
JavaScript uses **template literals** for this purpose, which are enclosed in backticks (`) instead of regular single or double quotes.

Backticks are also known as grave accents.

To insert a variable or expression into a string, the following syntax is used: `${}`

```js
const name = "Cxd3"
const age = 35;

const message = `Hi, my name is ${name}, and I am ${age} years old.`;
console.log(message);
// Output:
// Hi, my name is Cxd3, and I am 35 years old.
```

To use interpolation, you **must** use backticks.
Using single or double quotes will not work.

```js
const categories = 'toys';
console.log(`https://someurl.com/${categories}`);
// Output:
// https://someurl.com/toys
```

Another example for reinforcement:

```js
const admin = "Cxd3";
alert(`Hello, ${admin}`);
```

This will show a modal window with your name.
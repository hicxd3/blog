+++
date = '2025-02-07T12:00:24+03:00'
title = 'Spread operator in JavaScript'
categories = [ "javascript" ]
+++

The Spread operator, which looks like this `(...)` is a JavaScript tool that allows you to "expand" array elements or object properties.

The spread operator is indicated by three dots `(...)`. Its main task is to "expand" the array elements or object properties so that they can be used in other contexts. For example, it makes it easy to copy arrays, merge objects, pass array elements to a function, and more.

The Spread Operator is very often used with arrays.
Let's look at an example of cloning an array. This feature
is very useful when you need to avoid changing
the source array.

```js
const arr = [1, 2, 3];
const arr2 = [...arr];

console.log(arr2); // [1, 2, 3]
```

You can also combine two arrays into one

```js
const arr1 = [1, 2];
const arr2 = [3, 4];
const arr3 = [...arr1, ...arr2];

console.log(arr3); // [1, 2, 3, 4]
```

You can add data to an existing array.

```js
const arr1 = [1, 2];
const arr2 = [...arr1, 3, 4];

console.log(arr2); // [1, 2, 3, 4]
```

The spread operator is used no less often
when working with objects. Let's look at some simple examples.

As with arrays, objects can be cloned
using the spread orator.

```js
const obj1 = { a: 1, b: 2 };
const obj2 = { ...obj1 };

console.log(obj2); // { a: 1, b: 2 }
```

We can also combine several objects into one 

```js
const obj1 = { a: 1, b: 2 };
const obj2 = { b: 3, c: 4 };
const mergedObject = { ...obj1, ...obj2 };

console.log(mergedObject); // { a: 1, b: 3, c: 4 }
```

The Spread operator allows you to add properties
to an existing object.

```js
const obj1 = { a: 1, b: 2 };
const newObject = { ...obj1, c: 3 };

console.log(newObject); // { a: 1, b: 2, c: 3 }
```

It can be used when working with strings, a small example

```js
const str = "Elle";
const chars = [...str];

console.log(chars); // ['E', 'l', 'l', 'e']
```
<p class="gray">
It is important to remember that the spread operator
only works with strings, objects, and arrays.
If you try to use it
when working with numbers, it will cause an error.
</p>
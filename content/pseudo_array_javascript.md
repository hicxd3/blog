+++
date = '2024-10-03T18:53:24+03:00'
title = 'Arrays and Pseudo-Arrays in JavaScript'
categories = [ "javascript" ]
+++

Today's lecture will cover arrays and pseudo-arrays, as well as the main methods for working with them.

Arrays and pseudo-arrays are two different but similar data structures in JavaScript.

Arrays are a built-in type in JavaScript designed to store ordered collections of elements. They come with many useful methods for manipulating data.

### Example of a simple array

```js
let array = ['apple', 'banana', 'orange'];
console.log(array[0]); // 'apple'
```

### Array features:

> Array elements are indexed (starting from 0)  
> Arrays are dynamic: their length can change  
> Support methods for working with collections: `push`, `pop`, `map`, `filter`, `reduce`, etc.

---

#### Pseudo-arrays

Pseudo-arrays are objects that look like arrays but are not true arrays. They have numeric indexes and a `length` property but do not support array methods.

For example:

```js
function showArguments() {
  console.log(arguments); // pseudo-array
}
```

### Pseudo-array features:

> Have numeric indices (e.g., 0, 1, 2)  
> Have a `length` property that indicates the number of elements  
> Do not support array methods (`push`, `pop`, `map`, etc.)

+++
date = '2025-01-30T18:55:24+03:00'
title = 'Array Methods in JavaScript'
categories = [ "javascript" ]
+++

All methods and properties available to arrays can be found in the documentation.

Alternatively, you can print all available methods to the console using the `console.dir` command.

Today, we'll explore the most commonly used array methods.

Let's start by creating a simple array to experiment with. At first, it will just be a list of numbers:

```js
let array = [1, 2, 3, 4, 5];
```

When working with arrays, we often need to modify them—either by adding or removing items.

There are methods for manipulating the beginning or end of an array.

Let's begin with a method that edits the last element: it's called `pop()`.

This method removes the last value from our array.

```js
let array = [1, 2, 3, 4, 5];
array.pop();
// Returns
// 1 2 3 4 
```

There is also the opposite method that adds an element to the end of the array, called `push()`.

```js
let array = [1, 2, 3, 4, 5];
array.push(6);
// Returns
// 1 2 3 4 5 6 
```

To work with the beginning of an array, there are two methods: `shift()` and `unshift()`. They add or remove items at the beginning of the array.

However, they have a major drawback, which is why they are rarely used.

The issue is that when you add data at the beginning, all the subsequent indexes shift.

You can also loop through arrays using a standard `for()` loop.

The `length` property allows you to iterate through all elements of the array.

```js
let array = [1, 2, 3, 4, 5];
for (let i = 0; i < array.length; i++) {
    console.log(array[i]);
}
```

You can also loop through an array using `for of()`, which can also be used for strings, pseudo-arrays, and collections like `Map` and `Set`.

`for of()` only works with array-like structures; it won’t work with plain objects.

```js
for(let value of array) {
    console.log(value);
}
```

Now let's talk about one of the most commonly used methods: `forEach()`.

This method works similarly to `for of()` and `for()` loops, but with some differences.

`forEach()` takes a callback function and includes three arguments.

Syntax:

```js
let array = [1, 2, 3, 4, 5];
array.forEach(function(item, i, array) {
    console.log(`${i}: ${item} inside array ${array}`)
});
```

The `forEach()` method makes it easy to manipulate elements on the page.

#### Method split()

The `split()` method in JavaScript is used to split a string into an array of substrings based on a given delimiter.

```js
let str = "apple,banana,orange";
let fruits = str.split(",");
console.log(fruits); 
// ["apple", "banana", "orange"]
```

#### Method sort()

The `sort()` method in JavaScript is used to sort the elements of an array.

Example: alphabetical sorting:

```js
let fruits = ["banana", "apple", "orange", "grape"];
fruits.sort();
console.log(fruits); 
// ["apple", "banana", "grape", "orange"]
```

This method sorts elements as strings, i.e., alphabetically.

But if the array contains numbers, the sorting behavior changes.

We can write a function to sort a numeric array correctly:

```js
let num = [4, 2, 1, 6];
num.sort(compareNum);
console.log(num);

function compareNum(a, b) {
    return a - b;
}

// Output:
// 1 2 4 6
```
+++
date = '2024-11-17T18:53:24+03:00'
title = 'Arrays in JavaScript'
categories = [ "javascript" ]
+++

A small Task from RS School about arrays in JavaScript.

To store ordered sets of data, we use a special structure called an **Array**.

### Creating an array

To create an empty array, you can use two syntax options:

```js
let arr = new Array();
let arr = [];
```

Usually, the second option is preferred.
You can also immediately define initial values inside the square brackets:

```js
let girls = ["Elle", "Mia", "Eve"];
```

Array indexing starts from zero.

To access an element, use its index inside square brackets:

```js
let girls = ["Eve", "Mia", "Elle"];  

console.log(girls[0]); // Eve
console.log(girls[1]); // Mia
console.log(girls[2]); // Elle
```

You can replace an array element like this:

```js
girls[2] = 'Anna'; 
// the array is now:
girls = ["Eve", "Mia", "Anna"]
```

And you can add a new item into an existing array:

```js
girls[3] = 'Elle'; 
// now the array looks like:
girls = ["Eve", "Mia", "Anna", "Elle"]
```

To get the number of items in the array, use the `.length` property:

```js
let girls = ["Eve", "Mia", "Elle"];   
console.log(girls.length); // 3
```

To print the entire array, just use `console.log`:

```js
let girls = ["Eve", "Mia", "Elle"];
console.log(girls); // Eve, Mia, Elle
```

Arrays can hold values of different types.
Example:

```js
// mixed types
let arr = ['Elle', { name: 'Mia' }, true, function() { alert('I miss you'); }];   
    
// get the object at index 1 and log its property
console.log(arr[1].name); // Mia
    
// get the function at index 3 and call it
arr[3](); // I miss you
```


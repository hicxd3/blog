
+++
date = '2025-01-25T12:55:24+03:00'
title = 'Destructuring Objects in JavaScript'
categories = [ "javascript" ]
+++

Object destructuring is a convenient way to extract data from objects in JavaScript. It allows you to “break down” an object into individual variables, making the code more readable and concise.

Objects in JavaScript are associative arrays and are similar to objects in other languages such as PHP.

Here's a small example for experimenting with objects:

```js
let obj = {
    name: 'Elle',
    age: 22,
    hobbies: {
        film: 'Crank',
        music: 'DVRST',
    }
};

console.log(obj.name); // 'Elle'
```

To delete a property from an object, use the `delete` operator:

```js
let obj = {
    name: 'Elle',
    age: 22,
    hobbies: {
        film: 'Crank',
        music: 'DVRST',
    }
};

delete obj.age;

console.log(obj); 
// returns object without the age property
```

#### Looping through objects with for...in

Using the same object:

```js
let obj = {
    name: 'Elle',
    age: 22,
    hobbies: {
        film: 'Crank',
        music: 'DVRST',
    }
};

for(let key in obj) {
    console.log(`Property ${key} has value ${obj[key]}`)
}
```

Note the `hobbies` property — when the interpreter encounters a nested object, it outputs `[object Object]` because it converts everything to a string.

To access nested object properties, use a `for...in` loop inside another `for...in` loop:

```js
let obj = {
    name: 'Elle',
    age: 22,
    hobbies: {
        film: 'Crank',
        music: 'DVRST',
    }
};

for(let key in obj) {
    if(typeof(obj[key]) === 'object') {
        for(let i in obj[key]) {
            console.log(`Property ${i} has value ${obj[key][i]}`)
        }
    } else {
        console.log(`Property ${key} has value ${obj[key]}`)
    }
}
```

Note: Objects don't have a `length` property, so you can't directly count the key-value pairs.

Here’s how to count them:

```js
let obj = {
    name: 'Elle',
    age: 22,
    hobbies: {
        film: 'Crank',
        music: 'DVRST',
    }
};

let counter = 0;

for(let key in obj) {
    counter++;
}
console.log(counter);
```

#### The Object.keys() method

`Object.keys()` returns an array of the object’s own enumerable property names:

```js
let obj = {
    name: 'Elle',
    age: 22,
    hobbies: {
        film: 'Crank',
        music: 'DVRST',
    }
};
console.log(Object.keys(obj).length);
```

### Summary:

Objects are structures that can store any type of data as key-value pairs. Keys and values can be nested (objects in objects, arrays in objects, etc.).

Use `for...in` to iterate over keys and access their values. You can reference properties using dot notation or bracket notation.

Objects may have built-in methods and properties, and defining functions inside an object creates object methods.

### Object Destructuring

Let’s destructure an object:

```js
let obj = {
    name: 'Elle',
    age: 22,
    hobbies: {
        film: 'Crank',
        music: 'DVRST',
    }
};

const {film, music} = obj.hobbies;
console.log(film); 
// outputs Crank
```

1. Object destructuring allows you to extract properties into separate variables.

2. You can rename variables, set default values, and destructure nested objects.

3. Destructuring is often used in function parameters or to extract remaining properties.

This approach helps keep the code cleaner and easier to work with.

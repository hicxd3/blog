+++
date = '2025-03-22T12:00:24+03:00'
title = 'The querySelector() Method in JavaScript'
categories = [ "javascript" ]
+++

The `querySelector` method is one of the most popular and powerful tools for selecting elements in the DOM (Document Object Model) in JavaScript. It allows you to find the first element on the page that matches a given CSS selector. This method greatly simplifies working with the DOM compared to older element selection methods such as `getElementById`, `getElementsByClassName`, and others.

```js
document.querySelector(selector);
```

Here, `selector` is a string representing a CSS selector, for example `#id`, `.class`, or `div`.

The `querySelector` method returns the first element that matches the passed selector. If no such element is found, it returns null. It's important to remember that `querySelector` only finds the first matching element. If there are multiple elements matching the selector on the page, it will select only the first one.

Example of selecting an element by `id`:

```js
let element = document.querySelector('#myElement');
console.log(element); 
// Returns the element with id="myElement"
```

Example of selecting an element by class:

```js
let element = document.querySelector('.myClass');
console.log(element); 
// Returns the first element with the class 'myClass'
```

Selecting an element by tag:

```js
let element = document.querySelector('div');
console.log(element); 
// Returns the first <div> on the page
```

The `querySelector` method makes it easy and fast to find elements for further manipulation, such as changing styles, adding event listeners, or performing other actions.

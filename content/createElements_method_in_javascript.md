+++
date = '2025-03-29T10:00:24+03:00'
title = 'The createElement() Method in JavaScript'
categories = [ "javascript" ]
+++

The `document.createElement()` method allows you to create new HTML elements directly in JavaScript. It is the main way to dynamically add content to the page.

### Method Syntax

```js
let element = document.createElement(tagName);
```

When calling the method, you should specify the tag name, such as `div`, `p`, `h1`, and so on.

### Example: Creating a `div` and appending it to the end of the `body`

```js
let newDiv = document.createElement('div'); 
newDiv.textContent = 'Cxd3 was here =)';
document.body.appendChild(newDiv); 
// Adds the div to the end of the body
```

### Example: Adding CSS styles and classes

```js
let button = document.createElement('button');
button.textContent = 'I am a button';
button.classList.add('btn');
button.style.background = 'black';
document.body.appendChild(button);
```

### Inserting an element at a specific position using `insertBefore()`

```js
let list = document.getElementById('myList'); 
let newItem = document.createElement('li');
newItem.textContent = 'New item';
list.insertBefore(newItem, list.firstChild); 
// Inserts the new item at the beginning of the list
```

`document.createElement()` is a fundamental tool that allows you to build dynamic interfaces without constantly redrawing the entire page. This is especially useful when working with interactive lists, dynamic content, and reactive UI components like `React`, which I dream of mastering =)
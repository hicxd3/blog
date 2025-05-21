+++
date = '2025-03-30T7:00:24+03:00'
title = 'append() and prepend() Methods in JavaScript'
categories = [ "javascript" ]
+++

The `append()` and `prepend()` methods allow you to insert elements or text  
at the **end** or the **beginning** of another element.  
They provide a cleaner and more convenient alternative to `appendChild()`.

### `element.append()` — Add to the End

The `append()` method inserts content at the **end** of an element.  
It can accept both DOM elements and text strings:

```js
let container = document.getElementById('box');
let newDiv = document.createElement('div');
newDiv.textContent = 'New element';
container.append(newDiv, ' And this is just text');
```

### `element.prepend()` — Add to the Beginning

The prepend() method inserts content at the beginning of an element:

```js
let list = document.getElementById('myList');
let newItem = document.createElement('li');
newItem.textContent = 'New first item';
list.prepend(newItem);
```

`append()` and `prepend()` are clean and modern methods for inserting content into the DOM.
They replace the older `appendChild()` approach, offer shorter syntax,
and allow you to insert multiple nodes or text at once.
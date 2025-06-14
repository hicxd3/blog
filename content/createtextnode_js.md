+++
date = '2025-03-30T8:00:24+03:00'
title = 'Creating Text Nodes with createTextNode in JavaScript'
categories = [ "javascript" ]
+++

The `document.createTextNode()` method creates a text node without wrapping it in an `HTML` tag. It's useful when you want to add plain text to an element without altering its structure.

```js
let textNode = document.createTextNode('Dxrkd3v was here');
```

Example of inserting text into a paragraph using pure `JS` without modifying the `HTML`:

```js
let p = document.createElement('p');  
let t = document.createTextNode('Hello, Cxd3!');  

p.appendChild(t);  
document.body.appendChild(p); 
```

This method also lets you change text on the fly:

```js
let div = document.getElementById('h1');  
div.appendChild(document.createTextNode('New h1!'));  
```

`createTextNode()` is a cool way to add text without touching the document's structure. It gives you precise control over content while preserving the existing `HTML`.

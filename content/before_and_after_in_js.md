+++
date = '2025-03-30T8:03:24+03:00'
title = 'The before() and after() Methods in JavaScript'
categories = [ "javascript" ]
+++

The `before()` and `after()` methods allow you to insert new elements or text before or after an existing element. Unlike `append()` and `prepend()`, these work outside the target element.

### element.before() — insert before an element

The `before()` method inserts new content before the specified element.

```js
let heading = document.getElementById('title'); 
let newText = document.createElement('p'); 
newText.textContent = 'Dxrkd3v was here =)'; 
heading.before(newText); 
// Now <p> will appear before <title>
```

### element.after() — insert after an element

The `after()` method inserts content after the specified element.

```js
let button = document.getElementById('submitBtn'); 
let note = document.createElement('span'); 
note.textContent = ' (This is important!)'; 
button.after(note); 
// Now <span> will appear right after the button
```

The `before()` and `after()` methods make it easy to insert elements around others without needing to manipulate parent containers. They help keep your code clean and straightforward, especially when dynamically modifying the interface.

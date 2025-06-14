+++
date = '2025-03-09T00:53:24+03:00'
title = 'The remove() method in Javascript'
categories = [ "javascript" ]
+++

The 'remove()` method allows you to remove an element from the page without having to access its parent. This is the most convenient way to delete elements in modern JavaScript.

```js
element.remove();
```

Deleting an item from a page by id

```js
let element = document.getElementById('box');
element.remove();
// Completely removing the element with the id "box"
```

Deleting an element by class

```js
document.querySelector('.item').remove();
```

Deleting all list items, using a combination with `forEach()`

```js
document.querySelectorAll('.list-item').forEach(item => item.remove());
```

Removing elements from a page after events, such as when a wedge is placed on something

```js
document.getElementById('deleteBtn').addEventListener('click', function() {
this.remove();
// The button will delete itself
});
```

The remove() method helps with removing elements from the DOM. It gets rid of unnecessary code and makes working with dynamic interfaces more convenient.
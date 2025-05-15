+++
date = '2025-03-30T14:43:24+03:00'
title = 'The addEventListener() Method in JavaScript'
categories = [ "javascript" ]
+++

The `addEventListener()` method is the standard way to assign event handlers in `JavaScript`.  
It allows you to attach functions that run when a specific event occurs, offering more flexibility than old-school inline HTML event attributes.

This method takes **three arguments**:

- The **event type** (like `click`, `keydown`, `mouseover`).

- The **handler function** (what should happen when the event triggers).

- An optional **options object** (such as whether the event is captured during bubbling or capturing phase).

### Example:

```js
document.getElementById('myButton').addEventListener('click', function() {
  alert('Button was clicked!');
});

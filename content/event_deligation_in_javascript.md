+++
date = '2025-04-29T01:00:00+03:00'
title = 'Event Delegation in JavaScript'
categories = [ "javascript" ]
+++

Event delegation is a pattern where we add a single event listener to a parent element instead of adding listeners to each child element individually.

We use querySelectorAll to select elements, but instead of attaching listeners to each one, we attach a single listener to their common parent, often called a wrapper.

Example:

```javascript
const wrapper = document.querySelector('.wrapper');

wrapper.addEventListener('click', (event) => {
  console.log(event.target);
});
```

Here, event.target gives us the actual element that was clicked inside the wrapper.

We can use an if-statement to check exactly which element was clicked:

```javascript
wrapper.addEventListener('click', (event) => {
  if (event.target.classList.contains('button')) {
    console.log('Button inside wrapper clicked!');
  }
});
```

This way, we react only when specific elements are clicked, not just any click inside the wrapper.

Event delegation helps us manage events more efficiently, especially when dealing with dynamically created elements.
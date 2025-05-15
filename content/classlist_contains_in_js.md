+++
date = '2025-04-28T09:00:24+03:00'
title = 'ClassList.contains() in JavaScript'
categories = [ "javascript" ]
+++

When we need to check if an element has a specific class, we use the contains method from classList.

Since contains is a method and performs an action, we must always use parentheses () when calling it.

It returns true if the class is present and false if it is not.

Example of using contains:

```javascript
const button = document.querySelector('.my-button');
console.log(button.classList.contains('active')); // true or false
```

This allows us to dynamically control the page by checking the state of elements and applying logic accordingly.

Here is a simple example of a menu toggle using contains:

```javascript
const menu = document.querySelector('.nav-menu');
const toggleButton = document.querySelector('.toggle-button');

toggleButton.addEventListener('click', () => {
  if (menu.classList.contains('open')) {
    menu.classList.remove('open');
  } else {
    menu.classList.add('open');
  }
});
```

We check if the menu already has the "open" class. If it does, we remove it. If it doesn't, we add it.

This approach helps us create dynamic and responsive interfaces easily.

### Notes

contains is a method, so we always use parentheses.
It helps us check if a class is present on an element.
Dynamic checks with contains make our pages more interactive and state-aware.
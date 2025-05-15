+++
date = '2025-04-28T08:50:24+03:00'
title = 'ClassList.toggle() in JavaScript'
categories = [ "javascript" ]
+++

When we want to add or remove a class based on its current presence, we use the toggle method from classList.

Since toggle is a method and performs an action, we must always use parentheses () when calling it.

If the class is present, toggle will remove it. If the class is absent, toggle will add it.

Example of toggling a single class:

```javascript
const menu = document.querySelector('.nav-menu');
menu.classList.toggle('open');
```

Each time this code runs, the "open" class will be added or removed depending on whether it is already there.

This method is perfect for building dynamic elements like opening and closing menus, modals, or dropdowns.

### Notes

Toggle is a method, so we always use parentheses.

It helps us add or remove a class automatically based on its current state.

Perfect for dynamic interface elements that change on user actions.

And that's it.

Simple, smart, and extremely useful for creating interactive pages.

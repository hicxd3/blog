+++
date = '2025-04-28T08:20:24+03:00'
title = 'ClassList.add() in JavaScript'
categories = [ "javascript" ]
+++


When we want to add new classes to an element dynamically, we use the add method from classList.

Since add is a method and performs an action, we must always use parentheses () when calling it.

We can add a single class:

```javascript
const button = document.querySelector('.my-button');
button.classList.add('active');
```

Or we can add multiple classes at once by passing several arguments:

```javascript
const card = document.querySelector('.profile-card');
card.classList.add('highlighted', 'featured');
```

This method allows us to dynamically manipulate the page, changing the appearance of elements based on user actions or script logic.

### Notes

add is a method, so we always use parentheses.
It helps us add one or more classes to an element easily.
Dynamic class manipulation makes our pages more interactive and responsive.

And that's it.
Simple, powerful, and very useful for building dynamic websites.

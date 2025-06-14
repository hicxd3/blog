+++
date = '2025-04-28T08:40:24+03:00'
title = 'ClassList.remove() in JavaScript'
categories = [ "javascript" ]
+++


When we want to remove classes from an element dynamically, we use the remove method from classList.

Since remove is a method and performs an action, we must always use parentheses () when calling it.

We can remove a single class:

```javascript
const button = document.querySelector('.my-button');
button.classList.remove('active');
```

Or we can remove multiple classes at once by passing several arguments:

```javascript
const card = document.querySelector('.profile-card');
card.classList.remove('highlighted', 'featured');
```

This method allows us to dynamically update the page, making elements change appearance based on user actions or script logic.

### Notes

remove is a method, so we always use parentheses.
It helps us remove one or more classes from an element easily.
Dynamic class removal makes our pages more flexible and responsive.

And that's it.
Simple, effective, and essential for managing interactive websites.

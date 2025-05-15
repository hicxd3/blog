+++
date = '2025-04-29T05:53:24+03:00'
title = 'ScrollTop in JavaScript'
categories = [ "javascript" ]
+++

The scrollTop property returns the number of pixels that an element's content is scrolled vertically.

We use it to check how far a user has scrolled, or to programmatically scroll an element.

Example — reading scroll position:

```javascript
const box = document.querySelector('.box');
console.log(box.scrollTop); // number of pixels scrolled vertically
```

Example — reacting to scroll:

```javascript
window.addEventListener('scroll', () => {
  if (document.documentElement.scrollTop > 100) {
    console.log('Scrolled more than 100px');
  }
});
```

Example — setting scroll position:

```javascript
document.documentElement.scrollTop = 0; // scroll to top
```

scrollTop is commonly used in real-world development to create sticky headers, scroll-based animations, and back-to-top buttons.

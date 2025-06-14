+++
date = '2025-05-01T03:53:24+03:00'
title = 'Opening a Modal at the Bottom of the Page in JavaScript'
categories = [ "javascript" ]
+++

We can show a modal window when the user scrolls to the bottom of the page by checking scroll position inside a scroll event listener.

Example — opening the modal at the bottom:

```javascript
const modal = document.querySelector('.modal');
const body = document.body;

window.addEventListener('scroll', () => {
  if (window.pageYOffset + document.documentElement.clientHeight >= document.documentElement.scrollHeight) {
    modal.classList.add('active');
    body.classList.add('modal-open');
  }
});
```

This code checks if the sum of vertical scroll and viewport height reaches or exceeds the total scrollable height of the page.

By adding the active class to the modal and modal-open to the body, we display the modal and prevent page scrolling.
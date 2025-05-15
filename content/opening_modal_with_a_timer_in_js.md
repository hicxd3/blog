+++
date = '2025-05-01T02:53:24+03:00'
title = 'Opening a Modal Window with a Timer in JavaScript'
categories = [ "javascript" ]
+++

We can make a modal window open automatically after a delay using setTimeout.
We can also add logic to cancel the timer if the user opens the modal manually before the timer finishes.

Example — opening the modal after 5 seconds:

```javascript
const modal = document.querySelector('.modal');
const openButton = document.querySelector('.modal-open');
const body = document.body;

const timerId = setTimeout(() => {
  modal.classList.add('active');
  body.classList.add('modal-open');
}, 5000);

openButton.addEventListener('click', () => {
  clearTimeout(timerId); // cancel auto-open if user opened manually
  modal.classList.add('active');
  body.classList.add('modal-open');
});
```

Example — closing the modal:

```javascript
const closeButton = document.querySelector('.modal-close');

closeButton.addEventListener('click', () => {
  modal.classList.remove('active');
  body.classList.remove('modal-open');
});
```

This approach improves user experience by preventing the modal from showing again if it was already opened manually.
+++
date = '2025-05-01T01:53:24+03:00'
title = 'Working with Modal Window Behavior in JavaScript'
categories = [ "javascript" ]
+++

To create a better user experience with modal windows, we can add logic for closing the modal when clicking outside of it (on the overlay), and prevent page scrolling while the modal is open.

Example — opening the modal and disabling scroll:

```javascript
const openButton = document.querySelector('.modal-open');
const modal = document.querySelector('.modal');
const body = document.body;

openButton.addEventListener('click', () => {
  modal.classList.add('active');
  body.classList.add('modal-open'); // disable page scroll
});
```

In CSS:

```css
.modal-open {
  overflow: hidden;
}
```

Example — closing the modal when clicking the close button:

```javascript
const closeButton = document.querySelector('.modal-close');

closeButton.addEventListener('click', () => {
  modal.classList.remove('active');
  body.classList.remove('modal-open');
});
```

Example — closing the modal when clicking on the overlay:

```javascript
const overlay = document.querySelector('.modal-overlay');

overlay.addEventListener('click', (event) => {
  if (event.target === event.currentTarget) {
    modal.classList.remove('active');
    body.classList.remove('modal-open');
  }
});
```

By combining these techniques, we ensure the modal closes both via button and overlay, and the page remains static while the modal is open.

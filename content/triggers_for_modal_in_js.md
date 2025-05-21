+++
date = '2025-05-01T00:53:24+03:00'
title = 'Classes for Modal Triggers in JavaScript'
categories = [ "javascript" ]
+++

In web development, we often use classes like modal-open and modal-close to control the display of modal windows.

We add event listeners to elements with these classes to open or close the modal.

Example — opening a modal:

```javascript
const openButton = document.querySelector('.modal-open');
const modal = document.querySelector('.modal');

openButton.addEventListener('click', () => {
  modal.classList.add('active');
});
```

Example — closing a modal:

```javascript
const closeButton = document.querySelector('.modal-close');

closeButton.addEventListener('click', () => {
  modal.classList.remove('active');
});
```

By toggling a class like active on the modal element, we can show or hide the modal using CSS.

This pattern keeps JavaScript simple and leaves the styling to CSS.

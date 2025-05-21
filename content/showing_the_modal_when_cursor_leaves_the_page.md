+++
date = '2025-05-01T04:53:24+03:00'
title = 'Showing a Modal When the Cursor Leaves the Page in JavaScript'
categories = [ "javascript" ]
+++

We can show a modal window when the user's cursor leaves the page (for example, moving the mouse toward the browser's close button) by listening for the mouseout event.

Example — opening the modal when the cursor leaves at the top:

```javascript
const modal = document.querySelector('.modal');
const body = document.body;
let modalShown = false;

document.addEventListener('mouseout', (event) => {
  if (event.clientY <= 0 && !modalShown) {
    modal.classList.add('active');
    body.classList.add('modal-open');
    modalShown = true; // show only once
  }
});
```

This checks if the mouse leaves the top of the viewport and shows the modal only once.

Adding modal-open to the body disables page scrolling while the modal is open.
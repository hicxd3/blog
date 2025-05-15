+++
date = '2025-04-15T12:00:24+03:00'
title = 'stopPropagation() method in JavaScript'
categories = [ "javascript" ]
+++

Sometimes we want an event to happen only on the element it was triggered on, and nowhere else.

We don't want it to bubble up to parent elements. That's when we can use `stopPropagation()` - it tells the browser 
<br />
- "Stop right here. Don't go any further."

### What does stopPropagation do?

In JavaScript most events bubble up through the DOM tree. 

When we use `event.stopPropagation()` we tell the event:
<br />
- "Handle it here - and don't pass it to anyone else"

Example with button inside a container

html:

```html
<div id="container">
    <button id="anna">
        Click Me
    </button>
</div>
```

JS:

```js
const container = document.getElementById('container');
const anna = document.getElementById('anna');

container.addEventListener('click', () => {
    console.log('Container clicked');
});

anna.addEventListener('click', (event) => {
    event.stopPropagation();
    console.log('Anna clicked');
});
```

What will be logged:

```md
Anna clicked
```

The click happened on the button. The parent didn't react - because the event stopped right there.

### When can we use stopPropagation()?

1. When we don't want parent elements to respond to a child's click

2. When we build modals, dropdowns, or custom UI components

3. When we want to isolate element behavior and prevent overlap

### Important to remember

1. `stopPropagation()` doesn't block default browser actions (like links or form submits). For that we can use `preventDefault()`

2. We can combine both:
```js
link.addEventListener('click', (event) => {
    event.preventDefault();
    event.stopPropagation();
    console.log('Handled and isolated.');
});
```

### Notes

Events bubble through the  DOM - unless we stop them

We can write `stopPropagation()` in any listener to block further flow

It's great when we want layers of UI to mind their own business
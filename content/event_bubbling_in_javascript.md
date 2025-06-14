+++
date = '2025-04-18T12:00:24+03:00'
title = 'Event bubbling in JavaScript'
categories = [ "javascript" ]
+++

In JavaScript, when an event happens on an element, it doesn't stop there. It rises - like a bubble - up through  the DOM tree, from the element itself to its ancestoes. This behavior is called `event bubbling`

Let's imagine we have a button inside a block:

html:

```html
<div id="container">
    <button id="mia">
        Click me!
    </button>
</div>
```

JavaScript:
```js
const container = document.getElementById('container');
const mia = document.getElementById('mia');

container.addEventListener('click', => {
    console.log('Container clicked');
});

mia.addEventListener('click', () => {
    console.log('Mia clicked');
});
```

What well be logged?

```md
1 - Mia clicked
2 - Container clicked
```

Because after the event is triggered on mia, it bubbles up and reaches container, which also has a click listener.

### How to stop bubbling?

We can stop the event from bubbling by calling `.stopPropagation();`

```js
mia.addEventListener('click', (event) => {
    event.stopPropogation();
    console.log('Only Mia reacted');
});
```

Now the click will only be handled on the button. It won't reach the parent container.

#### When is bubbling useful?

Event bubbling is not a bug - it's a feature. We can use to:

1. Attach a single event listener to a parent instead of every child.

2. Build event delegation system (we'll cover that separately)

3. Manage layered interactions across components

## Notes

Events rise from the target element up through the DOM

We can call stopPropagation() to stop them mid-way

By default, addEventListener() listens in the bubbling phase, not the capturing one
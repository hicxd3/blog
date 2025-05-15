+++
date = '2025-04-17T11:53:24+03:00'
title = 'Event capturing in JavaScript'
categories = [ "javascript" ]
+++

When an event happens on the page, it doesn't always hit he target directly. In fact, the browser first `captures` the event from the top - starting from document and going down through all parent elements - until it reaches the target. This is called the `capturing phase` or event capturing

By default, when we attach an event listener, it listens during the bubbling phase. But if we want to catch the event before it reaches the target, we can listen during the capturing phase

HTML:

```html 
<div id="wrapper">
    <button id="eva">
        Click me
    </button>
</div>
```

JavaScript:

```js
const wrapper = document.getElementById('wrapper');
const eva = document.getElementById('eva');

wrapper.addEventListener('click', () => {
    console.log('Parent first');
}, true); //true > use capturing phase

eva.addEventListener('ckick', () => {
    console.log('Then the button');
}, true);
```

Whay will we have in loggs

```md
Parent first 
Then the button
```

Becouse the browser descends through the DOM, it reaches the parent first (on capture), then this the target.

### How can we enable capturing?

To make the listener fire during capturing, we can pass a third argument to addEventListener - either true or { capture: true }

like this:

```js
element.addEventListener('click', handler, true); 
```

or:

```js
element.addEventListener('click', handler, { capture: true });
```

We can use capturing if:

1. We want to intercept the event before it hits the target

2. We need to modify or stop propagation early 

3. We're building advanced UIs and want full control (or just doing things like a pro, which we are)

### Notes

Events bubble by default

We can listen on the capturing phase by passing true as the third argument 

When we click the button, the parent listener can still fire first - if it's listening on capture
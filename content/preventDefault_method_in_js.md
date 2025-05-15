+++
date = '2025-04-16T11:53:24+03:00'
title = 'preventDefault() method in JavaScript'
categories = [ "javascript" ]
+++

When we click a link, the browser follows it. When we submit a form, the page reloads. 

But sometimes we want to stop that and handle things ourselves. That's where `preventDefault()` comes in.

We can use `event.preventDefault()` to stop the browser from foing its default action.

That means:

1. No page reload on form submit.

2. No junp when clicking a link.

3. No drag or drop unless we allow it.

4. And more control over how things behave.

Stopping a link from navigating

html:

```html
<a href="https://example.com" id="eva">
    Click me!
</a>
```

js:

```js
const eva = document.getElementBuId('eva');

eva.addEventListener('click', (event) => {
    event.preventDefault();
    console.log('We handled the click ourselves.');
});
```

The link still looks like a link, but the browser won't go anywhere. We stay in control.

Stopping a form from submitting

html:

```html
<form id="mia">
    <input type="text" placeholder="Your name" />
    <button type="submit">
        Send!
    </button>
</form>
```


JS:

```js
const mia = document.getElementById('mia');

mia.addEventListener('submit', (event) => {
    event.preventDefault();
    console.log('Now we can process theform manually.');
});
```

The form won't reload the page. We can collect the data, sendit with `fetch()` or axios, show a message - all without leaving the screen.

### When should we use preventDefault()

We can use it when:

1. We want to handle forms manuually (AJAX)

2. We build a sinle-page app and control the flow

3. We create custom UI components like dropdowns or madals

4. We want to stop the browser from doing something we didn't ask for

### Notes

`preventDefault()` does not stop bubbling - better use `stopPropagation()` for that

Not all events can be prevented (some system key events, for example)

We can call `preventDefault()` in aby event listener to block the browser's default behavior


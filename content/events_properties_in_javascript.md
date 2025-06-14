+++
date = '2025-03-31T10:00:24+03:00'
title = 'Event properties in JavaScript'
categories = [ "javascript" ]
+++

Each event in JavaScript contains many properties that provide information about what happened. 
These properties allow us to understand which elements were involved in the event, which keys were pressed, where the cursor was located, and other details.

In other words, event properties are data that contains information about an event when it occurs. These properties are available inside event handlers and make it possible to find out exactly what happened.

Example with an `event`

```js
document.getElementById('myButton').addEventListener('click', function(event) {
  console.log(event);
});
// Will show all event properties
```

#### Basic properties of events

1 - `type`

The type property tells you what type of event occurred for example, `click` `keydown`, `submit`.

```js
document.getElementById('myButton').addEventListener('click', function(event) {
  console.log(event.type); // "click"
});
```

2 - `target`

The `target` property returns the element where the event occurred. This allows you to find out which element was involved in the event.

```js
document.getElementById('myButton').addEventListener('click', function(event) {
  console.log(event.target); // Will show the clicked item
});
```

3 - `currentTarget`

The `currentTarget` property returns the element to which the event handler was bound, not the one on which the event occurred. This is especially useful when delegating events.

```js
document.getElementById('parent').addEventListener('click', function(event) {
  console.log(event.currentTarget); // Will show the parent element that the handler is attached to.
});
```

4 - `clientX` and `clientY`

These properties contain the coordinates of the mouse cursor at the moment the event occurs. The values are measured relative to the viewing area of the window (excluding scrolling).

```js
document.addEventListener('click', function(event) {
  console.log(`X: ${event.clientX}, Y: ${event.clientY}`);
});
```

5 - `pageX` and `pageY`

The `pageX` and `pageY` properties give the mouse coordinates relative to the entire page, including scrolling. These properties are useful when you need to take into account the scrolled part of the page.

```js
document.addEventListener('click', function(event) {
  console.log(`Page X: ${event.pageX}, Page Y: ${event.pageY}`);
});
```

6 - `keyCode` and `code`

The `keyCode` and code properties are used for keyboard events. The keyCode returns the numeric key code, and the code returns the physical key code, regardless of which key was pressed (for example, `Enter`, `Space`, `ArrowUp`).

```js
document.addEventListener('keydown', function(event) {
  console.log(`keyCode: ${event.keyCode}, code: ${event.code}`);
});
```

7 - `button`

The `button` property indicates which mouse button was pressed. For the right mouse button, this value will be `2`, for the middle one — `1`, and for the left — `0'.

```js
document.addEventListener('mousedown', function(event) {
  console.log(`Button: ${event.button}`); // Shows the number of the mouse button
});
```

8 - `detail`

The detail property stores the number of mouse clicks in the `click` events. This property is useful when tracking double clicks.

```js
document.addEventListener('click', function(event) {
  console.log(`Number of clicks: ${event.detail}`);
});
```

Event properties provide opportunities to get detailed information about what happened on the page. Using these properties allows for more flexible and precise handling of various events, providing more effective user interaction.
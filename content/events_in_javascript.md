+++
date = '2025-03-30T12:10:24+03:00'
title = 'Events in JavaScript'
categories = [ "javascript" ]
+++

Events in JavaScript are browser reactions to user actions or changes on the page. When a user clicks on a button, enters text, moves the mouse, or loads a page, the browser generates an appropriate event that can be handled using JavaScript.

An event is a browser's signal that some action has taken place. For example:

- The user clicked on the button (`click`).

- The mouse cursor hovered over the element (`mouseover`).

- The form has been submitted (`submit`).

- The key on the keyboard is pressed (`keydown').

- The page has loaded (`load`).

JavaScript allows you to track these events and perform the necessary actions using event handlers.

### The most common events in JavaScript

| Event | Description |
|--------------|-------------------------|
| `click`      | Click on an element |
| `dblclick` | Double click |
| `mousedown`  | Clicking the mouse button |
| `mouseup`    | Releasing the mouse button |
| `mousemove` | Mouse movement |
| `mouseover` | Hovering over an element |
| `mouseout`   | Moving the cursor away from the element |
| `keydown`    | Pressing a key |
| `keyup`      | Releasing the key |
| `input`      | Entering data in the field |
| `change`     | Changing the value |
| `submit`     | Submitting the form |
| `focus`      | Focus on the element |
| `blur`       | Loss of focus |
| `load`       | Page loading |
| `scroll`     | Scrolling |
| `resize`     | Changing the window size |

<br />

Event handlers are different, but here's an example with one of them

```js
<button onclick="alert('The button is pressed!')">Push me</button>
``
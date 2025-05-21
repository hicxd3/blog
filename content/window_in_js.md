+++
date = '2025-04-29T03:53:24+03:00'
title = 'Window Object in JavaScript'
categories = [ "javascript" ]
+++

In a browser environment, the window object is the global object. It represents the browser window or tab that is displaying the page.

All global variables and functions declared in the browser become properties of the window object.

For example:

```javascript
function greet() {
  console.log('Hello');
}

console.log(window.greet === greet); // true
```

We can also access built-in methods and properties through window:

```javascript
window.alert('Hi there!');
```

Or simply:

```javascript
alert('Hi there!');
```

Useful properties and methods:

```javascript
window.innerWidth;   // Width of the window viewport
window.innerHeight;  // Height of the window viewport

window.location;     // URL and navigation info
window.document;     // The DOM of the page

window.setTimeout(); // Timer method
window.clearTimeout();
```

Because window is the global object in the browser, we usually don’t need to write "window." — it’s implied.
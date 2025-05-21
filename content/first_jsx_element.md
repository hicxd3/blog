+++
date = '2025-05-04T00:10:24+03:00'
title = 'First JSX Element in React'
categories = [ "react" ]
+++

We can write a simple JSX element and render it to the page using ReactDOM.

Example:

```javascript
const elem = <h2>Hello Mia</h2>;
ReactDOM.render(
  elem,
  document.getElementById('root')
);
```

This code creates an `<h2>` element and renders it inside the `<div id="root">` in the HTML.

JSX lets us write HTML-like syntax inside JavaScript and needs to be compiled by Babel.

We import React to enable JSX and ReactDOM to render elements into the DOM.
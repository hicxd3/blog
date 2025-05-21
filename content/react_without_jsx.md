+++
date = '2025-05-04T00:30:24+03:00'
title = 'React Without JSX'
categories = [ "react" ]
+++

In React, we can create elements without using JSX by calling React.createElement directly.

This method takes three arguments:

1 The HTML tag name as a string (for example, 'h2').

2 An object with attributes or props (or null if there are no props).

3 The content inside the element.

Example — without any attributes:

```javascript
const elem = React.createElement('h2', null, 'Hello Mia');
ReactDOM.render(
  elem,
  document.getElementById('root')
);
```

If we want to add a CSS class, we pass it as part of the second argument using an object with the `className` property:

```javascript
const elem = React.createElement('h2', { className: 'my-title' }, 'Hello Mia');
```

This code creates an `<h2>` element with class `my-title` and content "Hello Mia".

JSX is a shortcut that compiles into React.createElement calls, so writing without JSX helps us understand how React works internally.
+++
date = '2025-06-21T15:34:00+03:00'
title = 'Function Inside Component in React'
description = 'How to declare and use a function inside a React component'
categories = [ "react" ]
+++

Function Inside Component in React

Sometimes we need a function that only belongs to one component — for example, to handle a click. We can declare this function *inside* the component.

Here’s a simple example:

```jsx
function App() {
  function handleClick() {
    alert("Clicked!");
  }

  return <button onClick={handleClick}>Click me</button>;
}
```

Key Points ^-^

The function handleClick is scoped inside App.

It's passed to onClick without parentheses.

It runs only when the user clicks the button.

This is a clean way to handle logic tied to a specific UI element 
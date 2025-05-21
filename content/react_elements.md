+++
date = '2025-05-06T00:30:24+03:00'
title = 'React elements'
categories = [ "react" ]
+++

When building React applications, everything starts with
elements and evolves into components. These are the core building blocks of a modern UI.

What Are Elements?

React elements are the smallest building blocks of a React app. They describe what you want to see on the screen.

```jsx
const elem = <h1>Hello, bunny!</h1>;
```

But here's an important rule:

React elements are immutable

Once you create an element, you cannot change it. React doesn't update the element itself—instead, it creates a new element, compares it with the old one (via Virtual DOM), and updates the actual DOM accordingly.
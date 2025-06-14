+++
date = '2025-05-09T00:30:24+03:00'
title = 'Custom Components in React'
categories = [ "react" ]
+++

Creating Custom Components in React

In this article, we’ll focus on how to write custom React components from scratch using modern syntax and best practices.

Define a Component with a Capital Letter

To define a custom component in React, its name must start with a capital letter. This helps React differentiate it from built-in HTML elements.

```jsx
function MyComponent() {
  return <h1>Hello from MyComponent!</h1>;
}
```

Or, using arrow function syntax:

Use Arrow Function Syntax to Define Components

Arrow functions offer a concise and modern way to write functional components:

```jsx
const Hello = () => {
  return <h1>Hello, Elle!</h1>;
};
```

This approach is common in modern React applications and works well with hooks and other advanced patterns.

Use Custom Components Inside Other Components

Once a component is defined, you can use it **inside another component** by writing it as a JSX tag:

```jsx
const Hello = () => {
  return <h1>Hello, Eva!</h1>;
};

function App() {
  return (
    <div>
      <Hello />
    </div>
  );
}
```

Note ^-^ 

Remember: custom components are used as JSX tags like `<Hello />`, not called as functions like `Hello()`.

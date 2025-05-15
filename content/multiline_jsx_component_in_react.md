+++
date = '2025-05-04T00:40:24+03:00'
title = 'Multiline JSX Components in React'
categories = [ "react" ]
+++

When working with React, you may want to write JSX code that spans multiple lines for better readability. To do this correctly, we need to follow a few important rules.

 Wrap JSX in Parentheses

When a JSX expression spans multiple lines, wrap it inside parentheses `()` so that JavaScript parses it correctly:

```jsx
const elem = (
  <div>
    <h1>Hello, Eva!</h1>
    <p>What are you doing this evening?</p>
  </div>
);

ReactDOM.render(elem, document.getElementById('root'));
```

JSX Must Have One Parent Element

JSX expressions must return one parent element. You cannot have sibling elements without a single parent wrapping them. Typically, we use a `<div>` or a `<React.Fragment>` for this:

Invalid JSX:

```jsx
const elem = (
  <h1>Hello, Eva!</h1>
  <p>What are you doing this evening?</p>
);
```

Valid JSX (with parent `<div>`):

```jsx
const elem = (
  <div>
    <h1>Hello, Eva!</h1>
    <p>What are you doing this evening?</p>
  </div>
);
```

Embedding Expressions Inside JSX

We can embed **JavaScript expressions** inside JSX by using curly braces `{}`. These expressions can include variables, function calls, or simple calculations:

```jsx
const userName = "Eva";

const elem = (
  <div>
    <h1>Hello, {userName}!</h1>
    <p>2 + 2 = {2 + 2}</p>
    <p>What are you doing this evening?</p>
  </div>
);

ReactDOM.render(elem, document.getElementById('root'));
```

You cannot embed objects directly in JSX

JSX does not allow objects to be directly rendered inside curly braces. 

This will throw an error:

```jsx
const user = { name: "Eva" };

const elem = (
  <div>
    <h1>{user}</h1> // ERROR: Objects are not valid as a React child
  </div>
);
```

Instead, access a property of the object:

```jsx
const user = { name: "Eva" };

const elem = (
  <div>
    <h1>Hello, {user.name}!</h1>
  </div>
);
```

Notes: ^-^

Always wrap multiline JSX in parentheses `()`.

JSX must return a single parent element.

You can embed JavaScript expressions inside JSX using `{}`.

You cannot embed objects directly—use object properties instead.

And that’s how we write multiline JSX components in React! 
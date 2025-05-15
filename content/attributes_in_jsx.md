+++
date = '2025-05-04T01:40:24+03:00'
title = 'Attributes in JSX'
categories = [ "react" ]
+++

When writing JSX in React, we need to follow some special rules for HTML attributes. JSX is not exactly HTML—it’s closer to JavaScript—so some attribute names are slightly different.

Use `className` instead of `class`

In JSX, you cannot use `class` because it’s a reserved keyword in JavaScript. Instead, we use `className` to assign CSS classes:

```jsx
const elem = (
  <div className="container">
    <h1 className="title">Hello, Eva!</h1>
    <p className="subtitle">What are you doing this evening?</p>
  </div>
);

ReactDOM.render(elem, document.getElementById('root'));
```

Writing `class` will throw an error:

```jsx
// ERROR: 'class' is not valid in JSX
<div class="container"></div>
```

Always use `className` instead.

Attributes Use camelCase Naming

In JSX, all multi-word attribute names must be written in **camelCase** (each word starts with a capital letter except the first word):

Example:

```js
<label htmlFor="username">Username:</label>
<input id="username" type="text" />
```

We use `htmlFor` instead of `for` (because `for` is a reserved word in JavaScript).

Any attribute with multiple words should follow camelCase: `onClick`, `tabIndex`, `readOnly`.

Inline Styles Are Objects

Inline CSS styles are passed as JavaScript **objects** inside double curly braces `{{}}`. The style names must also follow camelCase:

```jsx
const elem = (
  <h1 style={{ color: "blue", backgroundColor: "lightgray" }}>
    Hello, Mia! Will you go to the movies with me? ^-^
  </h1>
);

ReactDOM.render(elem, document.getElementById('root'));
```

Notes ^-^

Use `className` instead of `class`.

Use `htmlFor` instead of `for` in `<label>`.

Attribute names with more than one word must be in camelCase.

Inline styles are written as JavaScript objects.

By following these rules, we can write valid and readable JSX in our React components! 
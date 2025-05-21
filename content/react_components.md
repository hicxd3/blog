+++
date = '2025-05-07T00:30:24+03:00'
title = 'React components'
categories = [ "react" ]
+++


Components let us split the UI into independent, reusable pieces. This makes our code more modular and maintainable.

There are two types of components:

Functional Components

```jsx
function Greeting() {
  return <h1>Hello, Eva!</h1>;
}
```

Class Components - less common in modern React

```jsx
class Greeting extends React.Component {
  render() {
    return <h1>Hello, Eva!</h1>;
  }
}
```
Reusing Components

One of the biggest advantages of components is that you can reuse them just like functions. For example:

```jsx
function Card(props) {
  return (
    <div className="card">
      <h2>{props.title}</h2>
      <p>{props.content}</p>
    </div>
  );
}

const app = (
  <div>
    <Card title="First Post" content="This is the first post." />
    <Card title="Second Post" content="Here’s another post." />
  </div>
);

ReactDOM.render(app, document.getElementById('root'));
```

This makes the UI scalable and avoids repetition.

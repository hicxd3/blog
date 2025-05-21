+++
date = '2025-05-08T00:30:24+03:00'
title = 'Importing React Components'
categories = [ "react" ]
+++

Component Naming Convention

Component names must begin with a **capital letter**. This is how React distinguishes between regular HTML tags and custom components.

```jsx
function Welcome() {
  return <h1>Hello!</h1>;
}

ReactDOM.render(<Welcome />, document.getElementById('root'));
```

If you write a component starting with a lowercase letter, React will treat it like a built-in HTML tag:

```jsx
function welcome() {
  return <h1>Hello!</h1>;
}

ReactDOM.render(<welcome />, document.getElementById('root')); //  Not rendered as a component
```

---

Importing Components from Other Files

For a modular project structure, components are usually written in separate files and imported where needed:

**Greeting.js**

```jsx
function Greeting() {
  return <h1>Hello, Eva!</h1>;
}

export default Greeting;
```

App.js

```jsx
import Greeting from './Greeting';

function App() {
  return (
    <div>
      <Greeting />
    </div>
  );
}
```

This approach keeps the code organized and scalable.

Components Can Contain JSX Elements

Components can return JSX that includes other elements, layouts, or even other components. This allows for complex and rich UI compositions:

```jsx
function Layout() {
  return (
    <div>
      <header><h1>Welcome</h1></header>
      <main><p>This is the main content area.</p></main>
      <footer><small>© 2025</small></footer>
    </div>
  );
}
```
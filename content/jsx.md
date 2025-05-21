+++
date = '2025-05-04T00:00:24+03:00'
title = 'JSX and index.js with createRoot in React'
categories = [ "react" ]
+++


JSX stands for JavaScript XML. It is a syntax extension (or preprocessor) for JavaScript that allows us to write HTML-like code directly inside JavaScript. JSX is not valid JavaScript by itself — it needs to be compiled (transpiled) by tools like Babel into standard JavaScript that browsers can understand.

When we create a React project using Create React App, the entry point of the application is index.js.

In this file, we import necessary modules:

```javascript
import React from 'react';
import ReactDOM from 'react-dom/client';
import './index.css';
import App from './App';
import reportWebVitals from './reportWebVitals';
```

We import React to use JSX, ReactDOM to interact with the DOM, the App component, CSS styles, and an optional reportWebVitals module.

In the middle of index.js, we see the code that tells React to render the App component inside the page:

```javascript
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
```

Here we use `createRoot` to initialize the React application. Then we call `render()` and pass JSX code that renders the App component inside the `<div id="root">` in public/index.html.

The export statement in App.js allows the App component to be imported into index.js and used in the render function.

JSX looks similar to HTML but is JavaScript syntax that lets us describe UI elements declaratively inside JavaScript code.
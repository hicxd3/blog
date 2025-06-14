+++
date = '2025-05-03T00:00:24+03:00'
title = 'Create React App'
categories = [ "react" ]
+++

Create React App is a tool that sets up a React project with everything configured for us — no need to manually set up Webpack or Babel.

Example — creating a React app:

```bash
npx create-react-app my-app
cd my-app
npm start
```

We create and start a new app at 
```bash
http://localhost:3000
```

For a cleaner project, we can delete unused files like logo.svg, reportWebVitals.js, and related imports.

Create React App uses Webpack to bundle files and Babel to transpile modern JavaScript and JSX into code browsers can understand.

React uses Client-Side Rendering (CSR) by default, meaning the app runs in the browser after the JavaScript is downloaded. Server-Side Rendering (SSR) is a different approach we can explore later using tools like Next.js.

When we start the app, React renders our application inside the `<div id="root">` element in index.html, letting React take control of the UI.

With this setup, we successfully launched our first React project on localhost:3000 and confirmed that we are currently working with CSR.

When we create a project with Create React App, we get a default component inside src/App.js that looks like this:

```javascript
import logo from './logo.svg';
import './App.css';

function App() {
  return (
    <div className="App">
      <header className="App-header">
        <img src={logo} className="App-logo" alt="logo" />
        <p>
          Hello World
        </p>
      </header>
    </div>
  );
}

export default App;
```

We can clean up this file by removing the logo and unused content to start building our own application.
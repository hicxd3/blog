+++
date = '2025-04-22T12:53:24+03:00'
title = 'Async, Defer, and Dynamic Script Loading'
categories = [ "javascript" ]
+++

When working with web pages, it's important to understand when the DOM is ready and how scripts load and execute.  

Let's explore the key concepts: `DOMContentLoaded`, `load`, `defer`, `async`, and dynamic script creation.


#### DOMContentLoaded and load events

There are two key events to know:

DOMContentLoaded fires when the HTML is fully loaded and parsed, but images and styles may still be loading.

load fires when the entire page is fully loaded, including images, styles, and fonts.

Example:

```javascript
document.addEventListener('DOMContentLoaded', function() {
  console.log('DOM is fully loaded and parsed!');
});

window.addEventListener('load', function() {
  console.log('Everything is loaded, including images and styles!');
});
```

When to use each:

`DOMContentLoaded` is great for working with the structure of the page immediately.

`load` is better when you need to wait for all resources to be available.


#### Defer attribute

`defer` tells the browser:  

Download me in parallel with the HTML, but only execute me after the HTML is fully parsed.

Scripts with `defer` are loaded asynchronously but executed in order after `DOMContentLoaded`.

Great for DOM manipulation scripts.

Example:

```html
<script src="app.js" defer></script>
```

```javascript
// app.js
console.log('DOM is ready, now running deferred script!');
```

Quick summary:

`defer` = doesn't block HTML parsing + waits for the full document.


#### Async attribute

`async` works differently:  

Download me in parallel with the HTML, and execute me immediately once ready!

Scripts with `async` are loaded asynchronously and executed as soon as they are downloaded.

Execution order is not guaranteed.

Example:

```html
<script src="analytics.js" async></script>
```

```javascript
// analytics.js
console.log('Analytics script running independently!');
```

Quick summary:

`async` = script lives its own life.

Best for independent scripts like analytics or tracking codes.


#### Dynamically creating and loading scripts

Sometimes you may want to load a script dynamically — after an event or condition is met.  

You can create a `<script>` element, set its `src`, and add it to the `<head>`

Example:

```javascript
const script = document.createElement('script');
script.src = 'https://example.com/library.js';
script.defer = true; // or async = true if you want
document.head.appendChild(script);
```

Explanation:

We create a `script` element.

Set the loading address with `src`

(Optional) Add `defer` or `async`

Append the script to `<head>`, and it starts loading immediately.

Dynamic script loading gives you flexibility to control when and what scripts are loaded!

### Notes

Today we explored:

DOMContentLoaded and load events.

`defer` and `async` script loading.

Dynamically adding scripts with `script.src`

How and when to control script execution for better page performance.

Understanding these concepts helps you build faster, more efficient web pages!
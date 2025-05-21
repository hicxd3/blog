+++
date = '2025-04-29T02:00:00+03:00'
title = 'setTimeout and setInterval in JavaScript'
categories = [ "javascript" ]
+++

When we want to delay the execution of some code, we use setTimeout.
It allows us to run a function once after a specified delay in milliseconds.

Syntax for setTimeout:

```javascript
setTimeout(() => {
  console.log('Hello after 2 seconds');
}, 2000);
```

setTimeout returns an ID, which we can use if we need to cancel the timeout later.

Example of cancelling a timeout:

```javascript
const timeoutId = setTimeout(() => {
  console.log('This will not run');
}, 5000);

clearTimeout(timeoutId);
```

If we want to run some code repeatedly at fixed intervals, we use setInterval.

Syntax for setInterval:

```javascript
const intervalId = setInterval(() => {
  console.log('Repeating every 3 seconds');
}, 3000);
```

Just like with setTimeout, setInterval also returns an ID.
We can stop the repeated execution by using clearInterval.

Example of cancelling an interval:

```javascript
clearInterval(intervalId);
```

Timers like setTimeout and setInterval are very useful for animations, delayed actions, and periodic checks in our applications.

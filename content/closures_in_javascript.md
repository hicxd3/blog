
+++
date = '2025-03-30T14:43:24+03:00'
title = 'How Closures Work in JavaScript'
categories = [ "javascript" ]
+++

A closure is a function that remembers the environment in which it was created, even after that environment has ceased to exist.

### What's the point?

In JavaScript, a function has access to variables declared outside of it. But closures go a step further — they "capture" variables that were in scope when the function was created.

```js
function outer() {
  const message = 'Hello';

  function inner() {
    console.log(message); 
    // inner "remembers" message
  }

  return inner;
}

const sayHello = outer(); 
// outer() returns inner
sayHello(); 
// logs: Hello
```

Even though `outer()` has finished executing, `inner()` still has access to the `message` variable — this is closure in action.

### Closures and counters

Let's build a simple counter using closures:

```js
function createCounter() {
  let count = 0;

  return function() {
    count += 1;
    return count;
  };
}

const counter = createCounter();
console.log(counter()); // 1
console.log(counter()); // 2
```

Each call to `createCounter()` creates a new independent closure with its own `count`.

Closures are powerful for:

- Encapsulation
- Private variables
- Memoization
- Event handling
- Asynchronous logic

Understanding how closures work is a must for any serious JavaScript developer.
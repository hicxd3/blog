+++
date = '2025-03-17T12:53:24+03:00'
title = 'Common Mistakes with Closures in JavaScript'
categories = [ "javascript" ]
+++

Closures are a powerful tool, but they come with several pitfalls that can lead to mistakes. In this article, we'll explore common problems that arise when working with closures and how to avoid them.

### Memory Leaks

When a closure holds a reference to variables from an outer function, those variables cannot be garbage collected as long as the closure exists. If these variables contain large objects, this can result in memory leaks.

Example of a memory leak:

```js
function createLargeObject() {
    let largeArray = new Array(1000).fill('Large data');
    return function() {
        console.log(largeArray[0]);
    };
}

const largeObjectClosure = createLargeObject();
// Even after createLargeObject finishes,
// largeArray remains in memory as long as the closure exists.
```

To avoid memory leaks, ensure closures do not retain unnecessary references to large objects. If the data is no longer needed, remove references to help the garbage collector clean up.

### Mistake with Loops and Closures

One of the most common mistakes is using a closure inside a loop with variables that change on each iteration. This often leads to unexpected results.

Incorrect code with closure inside a loop:

```js
function createFunctions() {
    let funcs = [];
    for (var i = 0; i < 3; i++) {
        funcs.push(function() {
            console.log(i);
        });
    }
    return funcs;
}

const functions = createFunctions();
functions[0](); // 3
functions[1](); // 3
functions[2](); // 3
```

This happens because `i` is shared by all closures. Each function remembers a reference to the same variable, and at execution time, `i` is already 3.

To fix this, use `let` instead of `var`, creating a new scope per iteration:

```js
function createFunctions() {
    let funcs = [];
    for (let i = 0; i < 3; i++) {
        funcs.push(function() {
            console.log(i);
        });
    }
    return funcs;
}

const functions = createFunctions();
functions[0](); // 0
functions[1](); // 1
functions[2](); // 2
```

With `let`, each loop iteration has its own `i`, and closures behave correctly.

### Closures in Asynchronous Functions

Using closures in async functions like `setTimeout` or `setInterval` can be tricky. The closure may use outdated values of variables that have already changed.

Buggy `setTimeout` example:

```js
function createTimer() {
    let timeLeft = 5;
    for (var i = 0; i < 5; i++) {
        setTimeout(function() {
            console.log(timeLeft);
        }, i * 1000);
        timeLeft--;
    }
}

createTimer(); 
// All outputs will be "0"
```

Each `setTimeout` refers to the same `timeLeft` variable, which ends up being `0`.

Fixing the example:

```js
function createTimer() {
    let timeLeft = 5;
    for (let i = 0; i < 5; i++) {
        setTimeout(function() {
            console.log(timeLeft);
        }, i * 1000);
        timeLeft--;
    }
}

createTimer(); 
// Output: 5, 4, 3, 2, 1
```

Using `let` helps maintain the correct value for each timeout.

### Modifying Variables Inside Closures

Closures allow modifying external variables, which can cause unexpected side effects if not handled carefully.

```js
function makeCounter() {
    let count = 0;
    return function() {
        count++;
        return count;
    };
}

const counter = makeCounter();
console.log(counter()); // 1
console.log(counter()); // 2
```

Modifying variables inside closures can be useful, but it’s important to control when and how these modifications occur to avoid bugs.

Closures require caution. To use them effectively, be aware of memory leaks, asynchronous issues, and variable scoping inside loops or handlers.
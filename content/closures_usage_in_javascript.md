
+++
date = '2025-03-16T11:00:24+03:00'
title = 'Where Closures Are Used in JavaScript'
categories = [ "javascript" ]
+++

Closures are not just a theoretical concept, but a tool that is widely used in real-world projects. They help solve many problems—from creating private data to improving performance. Let's explore where closures can be useful in real development.

### Private Variables

JavaScript doesn't have built-in support for private variables like some other languages. However, closures allow us to emulate this functionality. This enables us to hide data from outside access and manipulate it only through explicitly provided methods.

```js
function createPerson(name, age) {
    let _name = name;  
    let _age = age;    

    return {
        getName() {
            return _name;
        },
        getAge() {
            return _age;
        },
        setName(name) {
            _name = name;
        },
        setAge(age) {
            _age = age;
        }
    };
}

const person = createPerson("Elle", 22);
console.log(person.getName()); 
// "Elle"
person.setName("Mia");
console.log(person.getName()); 
// "Mia"
```

In this example, `_name` and `_age` remain hidden, and access is possible only via the methods provided by the closure.

### Callbacks and Event Handlers

Closures are frequently used in asynchronous operations such as event handlers and timers. A closure allows the function inside the handler to keep accessing variables, even if it executes later.

```js
function createTimer() {
    let timeLeft = 5;

    setInterval(function() {
        timeLeft--;  
        console.log(`Time left: ${timeLeft} seconds`);
        if (timeLeft === 0) {
            console.log("Time's up!");
        }
    }, 1000);
}

createTimer();
```

Here the closure enables the function inside `setInterval` to continue using the `timeLeft` variable, which changes every second.

### Caching Results

Closures can also be used to cache computed results, helping to avoid expensive recalculations. This technique is known as memoization.

```js
function memoize(fn) {
    const cache = {};
    return function(arg) {
        if (cache[arg]) {
            console.log('Retrieved from cache');
            return cache[arg];
        } else {
            const result = fn(arg);
            cache[arg] = result;
            return result;
        }
    };
}

function slowFunction(x) {
    console.log('Doing heavy computation...');
    return x * 2;
}

const memoizedFunction = memoize(slowFunction);
console.log(memoizedFunction(5)); 
// Doing heavy computation... 10
console.log(memoizedFunction(5)); 
// Retrieved from cache 10
```

In this example, the closure stores the result of the function and returns it from the cache on subsequent calls, improving performance.

### Partial Application

Closures are used to create functions with pre-set arguments. This technique is called partial application.

```js
function multiply(a, b) {
    return a * b;
}

function partiallyApply(fn, arg1) {
    return function(arg2) {
        return fn(arg1, arg2);
    };
}

const double = partiallyApply(multiply, 2);
console.log(double(5));  
// 10
console.log(double(10)); 
// 20
```

In this case, the closure allows us to create a new function `double` that always multiplies by `2`, locking in the first argument of `multiply`.

### Use in Iterators and Generators

Another great use of closures is in iterators and generators. Closures allow us to maintain state between calls, which is ideal for iteration.

```js
function createCounter() {
    let count = 0;

    return {
        next() {
            count++;
            return count;
        },
        reset() {
            count = 0;
        }
    };
}

const counter = createCounter();
console.log(counter.next()); 
// 1
console.log(counter.next()); 
// 2
counter.reset();
console.log(counter.next()); 
// 1
```

Here the closure keeps track of the counter's state between calls to `next`, enabling reset and continuation.

Closures empower JavaScript developers to manage private data, asynchronous behavior, caching, and more. They are an essential part of writing clean and efficient code and give great flexibility in application design.

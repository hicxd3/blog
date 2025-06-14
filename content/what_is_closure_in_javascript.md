+++
date = '2025-03-14T11:00:24+03:00'
title = 'What is closures in JavaScript'
categories = [ "javascript" ]
+++

Let's imagine that I work in an office, and I have a personal locker with documents. The other employees have their own lockers too, but they can't look in mine, and I can't look in theirs. However, I remember what's inside my closet, even if I go out for lunch or on vacation.

In JavaScript, the situation is the same: when a function remembers variables from its scope, even if it is executed outside this scope, this is called closure.

A small example:

```js
function createGreeting(name) {
    return function() {
        console.log(`Hello, ${name}!`);
    };
}

const greetElle = createGreeting("Ellie");
greetElle(); // "Hello, Ellie!"

const greetAnna = createGreeting("Anna");
greetAnna(); // "Hi, Anna!"
```

Here, the `createGreeting` function gets a `name`
and returns a new function that simply outputs:

```js
Hello, ${name}!.
```

When we call createGreeting("Elle"), the name variable is saved inside.

Even after createGreeting is completed, the call to greetElle() still "remembers" the name "Ellie".

JavaScript is designed so that if an internal function uses variables from the external scope, the engine does not delete them.

### Let's see what closures look like in JavaScript under the hood

To better understand how JavaScript stores data, let's look at a small piece of code.:

```js 
function counter() {
    let count = 0; 
    // A variable inside a function

    return function() {
        count++; 
        console.log(count);
    };
}

const myCounter = counter();
myCounter(); // 1
myCounter(); // 2
myCounter(); // 3
```

Although `counter()` has been executed, the `count` variable does not disappear because the internal function refers to it. This is a closure: the function has "captured" the count variable, and it remains in memory.

Closures are most often used in creating private variables, in event handlers (onclick, setTimeout), and in caching calculations. 

Closure is a mechanism that allows functions to "remember" variables even after their parent function is completed. It is a powerful tool that makes JavaScript flexible and user-friendly.
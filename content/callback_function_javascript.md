+++
date = '2025-01-22T12:55:24+03:00'
title = 'Callback functions in JavaScript'
categories = [ "javascript" ]
+++

Callback functions in JavaScript are functions that are passed as arguments to other functions and executed after a specific operation or event is completed. They are widely used in asynchronous programming, event handling, and functional programming.

Example of passing a callback function as an argument to another function and calling it inside

```js
function greeting(name) {
    console.log("Hello, " + name);
}

function processUserInput(callback) {
    const name = prompt("Please enter your name.");
    callback(name);
}

processUserInput(greeting); // greeting — is callback funtion
```

Callback functions are often used to handle asynchronous operations like server requests, file reading, or timers

```js
setTimeout(function() {
    console.log("This text will be displayed after 2 senconds");
}, 2000);
```

Callback functions are used to handle events like mouse clicks, key presses, etc.

```js
document.querySelector("button").addEventListener("click", function() {
    console.log("Button clicked!");
});
```
But the topic of event handlers will be covered later in more detail.

One of the drawbacks of callback functions is the so-called `Callback Hell`

>With a large number of nested callback functions, the code becomes hard to read and maintain.

Example of "Callback Hell":

```js
getData(function(a) {
    getMoreData(a, function(b) {
        getEvenMoreData(b, function(c) {
            console.log("Final result:", c);
        });
    });
});
```

Callback functions remain an important part of JavaScript, but in modern applications, they are often replaced by promises and async/await to improve code readability and maintainability.
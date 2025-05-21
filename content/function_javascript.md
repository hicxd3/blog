+++
date = '2024-11-11T18:53:24+03:00'
title = 'Functions in JavaScript'
categories = [ "javascript" ]
+++

To avoid repeating the same code in different parts of the program, functions were created.

Functions serve as the building blocks of a program.

Here are a few examples of built-in functions:

```js
alert(msg);
prompt(msg, default);
confirm(question);
```

*Note: JavaScript actually has many more built-in functions.*

### Function Declaration

To create a function, use this syntax:

```js
function showMsg() {
  console.log('Hello Elle!');
}
```

*In this example, the argument list is empty.*

First, you write the keyword `function`, then the name of the function, followed by a list of parameters in parentheses (comma-separated), and finally the function body, enclosed in curly braces.

```js
function name(parameters) {
  // function body...
}
```

A function can be called by its name `showMsg()`:

```js
function showMsg() {
  console.log('Hello everyone!');
}
showMsg()
showMsg()
// Output:
// Hello everyone!
// Hello everyone!
```

Calling `showMsg()` executes the function code, and in this case, we see the message twice.

This example clearly shows one of the main benefits of functions: eliminating code duplication.

If you need to change the message or the way it's displayed, you only need to update it in one place — the function body.
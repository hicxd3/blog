+++
date = '2024-05-02T18:53:24+03:00'
title = 'Ternary Operator in JavaScript'
categories = [ "javascript" ]
+++

Let's take a function that returns the absolute value of a given number:

```js
const abs = (number) => {
    if (number >= 0) {
        return number;
    }
    return -number;
};
abs(10); // 10
abs(-10); // 10
```

Can we write this more concisely? Using `return "value depending on condition"`?

To do this, we need an expression next to `return`, but `if` is a statement.  
JavaScript has an expression similar to `if-else`, which is the ternary operator.

The ternary operator always takes three operands:

```js
const abs = (number) => {
    return number >= 0 ? number : -number;
};
```

A shorter version of the `abs` function using the ternary operator looks like this:

```js
const abs = (number) => (number >= 0 ? number : -number);
```

Pay attention to parentheses when writing code with the ternary operator. They're not required but recommended to avoid mistakes.
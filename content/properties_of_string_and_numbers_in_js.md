+++
date = '2025-01-16T18:53:24+03:00'
title = 'Properties of strings and numbers in JavaScript'
categories = [ "javascript" ]
+++

In JavaScript, strings and numbers have properties that provide useful information about them.

#### String properties

Strings in JavaScript have one basic property, `length`

>Returns the number of characters in a string

>This property is read-only (it cannot be changed)

```js
const str = "Hello, Elle!";
console.log(str.length); 
```

<p class="gray">
The syntax of the properties of strings and numbers, unlike the methods, is written 
without parentheses at the end.
</p>

#### Properties of numbers

Numbers have static properties such as `MAX_VALUE`, `MIN_VALUE`, `Non`, `POSITIVE_INFINITY`, `NEGATIVE_INFINITY`, `EPSILON`, `MAX_SAFE_INTEGER` and `MIN_SAFE_INTEGER` that provide information about numeric constants and constraints.
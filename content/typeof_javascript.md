+++
date = '2025-01-08T18:54:24+03:00'
title = 'The typeof() operator in JavaScript'
categories = [ "javascript" ]
+++

The `typeof()` operator returns the data type of the argument.

A useful command if you need to find out,
for example, what type of data
the form returns on the site.

Y `typeof()` there are two syntax options:

>Syntax of the `typeof x` operator

>Syntax of the function `typeof(x)`

Both syntaxes work the same way.

`typeof()` returns a string that contains
the data type.

```js
typeof undefined // "undefined"

typeof 0 // "number"

typeof 1n // "bigint"

typeof true // "boolean"

typeof "foo" // "string"

typeof Symbol() // "symbol"

typeof {} // "object"

typeof null // "object"  

typeof function(){} // "function" 
```

You need to pay attention to `null`, as it is not
an object of a separate data type. This is an officially recognized error in the language.
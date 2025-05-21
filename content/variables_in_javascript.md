
+++
date = '2024-10-29T18:53:24+03:00'
title = 'Variables in JavaScript'
categories = [ "javascript" ]
+++

Variables in JavaScript are used to store information. You can visualize them as boxes that hold something inside.

To declare a variable, there are three main ways.

Two keywords, `let` and `const`, belong to the modern version of JavaScript.

There's also the keyword `var`, which is considered outdated and is not recommended for use.

### let

The first method is using the keyword `let`.

To declare a variable, use the keyword `let`, followed by the variable name, then an equals sign `"="`, and finally the value to assign to that variable.

In programming, the equals sign `"="` means assignment.

```js
let name = "Cxd3";
// let — keyword for declaring a variable
// name — variable name
// = — assignment operator
// Cxd3 — value assigned to the variable
// ; — end of the code statement
```

### const

The second method is using the keyword `const`.

`const` stands for "constant", meaning the variable declared with `const` cannot be reassigned.

```js
const dateOfBirth = 29.06.1999;
```

A variable name can contain letters, digits, the dollar sign `$`, and underscores `_`. However, it cannot start with a digit.

Also, variable names must not use reserved words in JavaScript, such as `error`, `alert`, `prompt`, and so on.

Use `const` for values that do not change later, such as names, dates of birth, etc.

Note: the value of a `const` variable can be modified if the variable holds an object.

```js
const object = {
    age: 25
};
object.age = 35;
console.log(object.age); // output: 35
```

### var

`var` is the old way of declaring variables. It's found in legacy code.

Variables declared with `var` can also be reassigned like those declared with `let`.

The issue with `var` is that the variable exists even before it is declared in the code, making it visible everywhere.

If you try to access a `var` variable before its declaration, JavaScript will return `undefined`. For example:

```js
console.log(name); // undefined
var name = "Cxd3";
```

This behavior is called "hoisting".

Another feature of `let` and `const` is that they are scoped to the block (enclosed in curly braces).

```js
{
  let result = 29;
}
console.log(result); // result is not defined
```

If declared with `var`, the variable `result` would be accessible outside the block.

To check what features are supported by different browsers, use the service [Can I Use](https://caniuse.com/)

### "use strict"

This directive is placed at the beginning of a script and tells the browser to run the code in "strict mode".

```js
"use strict";
// this code runs in strict mode
```

Without `"use strict"`, it's possible to access undeclared variables. With `"use strict"`, accessing such variables will result in "is not defined" errors.
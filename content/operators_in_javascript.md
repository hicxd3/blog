+++
date = '2025-01-09T18:53:24+03:00'
title = 'Arithmetic Operators in JavaScript'
categories = [ "javascript" ]
+++

#### Arithmetic Operators

Used for performing mathematical operations:

`+` — addition  
`-` — subtraction  
`*` — multiplication  
`/` — division  
`%` — remainder  
`**` — exponentiation (ES6)  
`++` — increment (adds 1)  
`--` — decrement (subtracts 1)

> The unary plus is an operator used to convert a value to a number.

The unary plus tries to convert the value after it into a number type.  
This is useful when you explicitly want to cast a string or other type to a number.

It’s called "unary" because it works with one operand (unlike binary plus `a + b`, which uses two).

```js
let str = "42";
let num = +str;
console.log(num); // 42 (number)
console.log(typeof num); // "number"
```

#### Increment and Decrement

Increment (`++`) and decrement (`--`) are unary operators in JavaScript used to increase or decrease a variable’s value by 1.

#### Increment `++`

**Prefix form (`++x`)**:

> Increases the variable by 1.  
> Returns the new value (after increment).

```js
let x = 5;
let y = ++x; // x becomes 6, y gets the new value
console.log(x); // 6
console.log(y); // 6
```

**Postfix form (`x++`)**:

> Increases the variable by 1.  
> Returns the old value (before increment).

```js
let x = 5;
let y = x++; // y gets 5, then x becomes 6
console.log(x); // 6
console.log(y); // 5
```

#### Decrement `--`

The decrement operator decreases the value of a variable by 1.

**Prefix form (`--x`)**:

> Decreases the variable by 1.  
> Returns the new value (after decrement).

```js
let x = 5;
let y = --x; // x becomes 4, y gets the new value
console.log(x); // 4
console.log(y); // 4
```

**Postfix form (`x--`)**:

> Decreases the variable by 1.  
> Returns the old value (before decrement).

```js
let x = 5;
let y = x--; // y gets 5, then x becomes 4
console.log(x); // 4
console.log(y); // 5
```
+++
date = '2024-11-12T18:53:24+03:00'
title = 'Data types in JavaScript'
categories = [ "javascript" ]
+++

In JavaScript, each value always refers to a specific data type, for example
like a string or a number.

There are only 8 types of data.

A variable can store any type of data.

In one section of the code, a string can be stored in a variable, and in another, a number.

```js
let some = '123'; // String   
    some = 123; // Number
```

Because of this feature, the JavaScript programming language is called "dynamically
typed".

This means that although data types exist, variables are not bound to any
particular type.

### Number or number

The numeric data type represents both integers and floating point numbers

```js
let number = 123; // Prime number  
    number = 123.456; // Floating point number
```

There are many operations available in JavaScript for working with numbers, such as multiplication
"*", division "/", addition "+", subtraction "-" and others.

In addition to ordinary numbers, there are also so-called "special numeric values",
such as "Infinity", "-Infinity" and "NaN", which refer to the data type of numbers.

<p class="gray">
NaN - stands for - Not a number
</p>

Infinity represents mathematical infinity. This is a special value that exceeds any number.

The value of "Infinity" can be obtained by trying to divide something by zero.

```js
console.log( 1 / 0); // Infinity
```

Or call it explicitly

```js
console.log(infinity) // Infinity
```

NaN indicates a computational error. This is the result of an incorrect or undefined mathematical operation, for example:

```js
console.log("not a number" / 2 );
// NaN, this division is an error
```

The NaN value has the "sticking" property. Any mathematical operation with NaN also returns NaN.:

```js
console.log( NaN + 1 ); // NaN    
console.log( 3 * NaN ); // NaN
console.log( "not a number" / 2 - 1 ); // NaN
```

If NaN is present in the mathematical expression, it extends to the entire result.

<p class="gray">
There is only one exception: 
<br />
NaN ** 0 is equal to 1
</p>

### BigInt

In JavaScript, the number type cannot safely handle numbers greater than (2^53 -1)(i.e. 9007199254740991) or less than -(2^53 -1) for negative numbers.

Technically, the number type is capable of storing very large integers (up to 1.7976931348623157*10^308), but an accuracy error occurs outside the safe range of integers ±(2^53 -1), since not all digits can fit into a fixed 64-bit memory. As a result, only an "approximate" value can be stored.

For example, these two different calculations will give the same result.

```js
console.log(9007199254740991 + 1); // 9007199254740992    
console.log(9007199254740991 + 2); // 9007199254740992
```

<p class="gray">
At the moment, BigInt is supported only in Firefox, Chrome, Edge, and Safari browsers, but it is not supported in IE.
</p>

### String or string

In JavaScript, a string must be enclosed in quotation marks.

```js
let str = "Hello, friend!";
let str2 = 'Single quotes are also suitable';
let phrase = `Backquotes allow embedding variables ${str}`;   
```

There are 3 types of buckets in JavaScript:

- 1 Single forging: "
- 2 Double picks: ""
- 3 Reverse picks: `

Double and single quotes are considered "simple" and have no differences.

Backquotes, however, have extended functionality. They allow
you to embed expressions inside a string by enclosing them in ${...}.

```js
let name = "Cxd3";

// Insert
the console.log variable( `Hello, ${name}!` ); // Hello, Cxd3!    
    
// Insert the expression
console.log( `result: ${1 + 2}` ); // Result: 3
```

<p class="gray">
Reverse pickings are also called backtick and are used for interpolation.
</p>

### Boolean or Boolean (logical) type

The boolean type can take only two values: true and false.

This type is usually used to store yes/no values: true means "yes, true"
and false means "no, false".

```js
let nameFieldChecked = true; // yes, the field is marked
let ageFieldChecked = false; // no, the field is not marked
```

A Boolean data type can also be the result of comparison operations.:

```js
let isGreater = 4 > 1;
alert( isGreater ); // true (the result of the comparison will be "yes")
```

<p class="gray">
The topic of the Boolean data type will be covered in more detail later
</p>

### Null data type

The special null value does not apply to any of the above types.

It forms a separate type that includes only the null value.

```js
let age = null;
```

In JavaScript, null is not a "reference to a non-existent object" or a "null
pointer", as in some other languages.

It's just a special value that means "nothing", "empty", or
"value unknown".

### The value of "undefined"

The undefined special value creates a type from itself in the same way as null.

It indicates that 'no value has been assigned'.

If a variable is declared, but no value is assigned to it, then its the value will be undefined:

```js
let age;
console.log(age); // outputs "undefined"
```

You can also force the undefined value to be assigned to any variable.

```js
let age = 35;
// changing the value to undefined
age = undefined;
console.log(age); // "undefined"
```

However, this approach is not recommended.

Null is usually used to assign an "empty" or "unknown" value to a variable.

While undefined is used to check whether the variable has been initialized.

### Data type Object or object

Unlike other data types, object is not a primitive type.

All the others are called "marginal" because their values can only be simple data, such as strings or numbers, etc.

Objects store more complex structures, such as collections of data.

The study of objects requires special study, so the topic will be covered later in a new separate lecture.

Syntax of objects for example

```js
let user = {     // user object
    name: "John", // the value "John" is stored under the key "name"  
    age: 30 // the value 30 is stored under the "age" key
  };
```

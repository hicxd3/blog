
+++
date = '2025-01-16T19:53:24+03:00'
title = 'String and Number Methods in JavaScript'
categories = [ "javascript" ]
+++

The most basic and frequently used methods for strings and numbers in JavaScript.  
These methods help you perform common operations with ease.

### Basic String Methods

#### toUpperCase()

Converts a string to uppercase.

```js
const str = "hello";
console.log(str.toUpperCase()); 
// "HELLO"
```

#### toLowerCase()

Converts a string to lowercase.

```js
const str = "HELLO";
console.log(str.toLowerCase()); 
// "hello" 
```

#### trim()

Removes whitespace from both ends of a string.

```js
const str = "  Hello  ";
console.log(str.trim()); 
// "Hello"
```

#### slice(start, end)

Returns a part of a string from start to end (excluding end).

```js
const str = "Hello World";
console.log(str.slice(0, 5)); 
// "Hello"
```

#### replace(old, new)

Replaces the first occurrence of the substring `old` with `new`.

```js
const str = "Hello World";
console.log(str.replace("World", "JavaScript")); 
// "Hello JavaScript"
```

### Basic Number Methods

#### toFixed(digits)

Returns a string representing a number with a fixed number of decimal places.

```js
const num = 3.14159;
console.log(num.toFixed(2)); 
// "3.14"
```

#### toString(radix)

Converts a number to a string.

```js
const num = 10;
console.log(num.toString()); 
// "10"
```

#### Number()

The `Number()` function converts a value to a number.

```js
console.log(Number("42")); 
// 42
```

#### parseInt()

Parses a string and returns an integer.

```js
console.log(parseInt("42")); 
// 42
console.log(parseInt("42abc")); 
// 42
```

#### Unary plus (+)

The unary plus operator converts a value to a number.

```js
console.log(+"42"); 
// 42
console.log(+"42abc"); 
// NaN
console.log(+true); 
// 1
console.log(+false); 
// 0
```

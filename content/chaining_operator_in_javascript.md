+++
date = '2025-04-24T12:55:24+03:00'
title = 'Optional Chaining Operator (?.) in JavaScript'
categories = [ "javascript" ]
+++

The optional chaining operator (`?.`) allows us to safely access object properties or call functions without risking errors if part of the path is `null` or `undefined`.  

Instead of throwing errors, it simply returns `undefined` if something is missing.


Simple Example:

```javascript
let user = {};

console.log(user.address?.street); // undefined (no error!)
```

What happens: 
`user` has no `address`.

Instead of crashing with Cannot read property street of undefined, we get undefined quietly.


#### Without Optional Chaining

```javascript
let user = {};

console.log(user.address.street);
// ❌ Error! Cannot read property 'street' of undefined
```

Without `?.`, accessing a missing property would throw an error and break your script.


#### Optional Chaining with Functions

The `?.` operator also works when calling functions.

```javascript
let user = {};

user.sayHi?.(); // Nothing happens, no error
```

If `sayHi` doesn't exist, the code simply does nothing without crashing.



#### When to Use Optional Chaining

Use optional chaining when:

Working with complex or dynamic data structures.

You are not sure if intermediate properties or methods exist.

You want safer and cleaner code without too many manual `if` checks.


### Notes

The optional chaining operator (`?.`) is a powerful feature in JavaScript that improves code safety and readability.  

It allows you to work confidently with nested objects and functions, without worrying about errors from missing properties.
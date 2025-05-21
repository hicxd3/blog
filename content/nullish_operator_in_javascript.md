+++
date = '2025-04-23T12:53:24+03:00'
title = 'Nullish Coalescing Operator (??) in JavaScript'
categories = [ "javascript" ]
+++

The nullish coalescing operator (`??`) is a way to set a default value  only if the variable is `null` or `undefined`.  
It is different from the `||` operator, which treats more values like `0`, `''`, `false` as "empty."

Simple Example:

```javascript
let userName;
let defaultName = 'Guest';

let nameToShow = userName ?? defaultName;
console.log(nameToShow); // Guest
```

What happens:

`userName` is `undefined`.

The `??` operator picks `defaultName` instead.


#### Difference from `||`

The `||` operator checks for any falsy value: `0`, `''`, `false`, `null`, or `undefined`.  
The `??` operator only checks for `null` or `undefined`.

Example:

```javascript
let points = 0;

console.log(points || 100); // 100 (bad: 0 is treated as falsy)
console.log(points ?? 100); // 0 (good: 0 is kept)
```

Explanation:

With `||`, `0` is treated as "empty" and replaced.

With `??`, `0` is considered a valid value and kept.


#### When to Use (??)

Use `??` when:

You expect `0`, `false`, or `''` to be valid values.

You only want to provide a fallback for `null` or `undefined`.

This ensures that meaningful values are not accidentally replaced.


### Notes

The nullish coalescing operator (`??`) makes it easy to set safe default values in JavaScript without incorrectly replacing valid data like `0` or `false`.  

It is a clean and powerful tool for handling optional values.
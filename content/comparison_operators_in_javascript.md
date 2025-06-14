+++
date = '2025-01-09T19:53:24+03:00'
title = 'Comparison Operators in JavaScript'
categories = [ "javascript" ]
+++

Comparison operators in JavaScript are used to compare two values. They return a boolean value: `true` or `false`.

### Equal (==)

- Checks if two values are equal with type coercion.
- If types differ, JavaScript will try to convert them to a common type before comparing.
- Compares by value, not type.

```js
console.log(5 == 5); // true
console.log(5 == '5'); // true ('5' is converted to number)
```

### Not Equal (!=)

- Checks if two values are not equal with type coercion.
- Returns `true` if values are different.

```js
console.log(5 != 10); // true
console.log(5 != '5'); // false ('5' is converted to number)
```

### Strict Equal (===)

- Checks if two values are equal without type coercion.
- Returns `true` only if both value and type are the same.

```js
console.log(5 === 5); // true
console.log(5 === '5'); // false (number vs string)
```

### Strict Not Equal (!==)

- Checks if two values are not equal without type coercion.
- Returns `true` if either the value or the type is different.

```js
console.log(5 !== 10); // true
console.log(5 !== '5'); // true (number vs string)
```

### Greater Than (>)

- Checks if the left value is greater than the right.

```js
console.log(10 > 5); // true
console.log(5 > 10); // false
```

### Less Than (<)

- Checks if the left value is less than the right.

```js
console.log(5 < 10); // true
console.log(10 < 5); // false
```

### Greater Than or Equal (>=)

- Checks if the left value is greater than or equal to the right.

```js
console.log(10 >= 10); // true
console.log(10 >= 5); // true
console.log(5 >= 10); // false
```

### Less Than or Equal (<=)

- Checks if the left value is less than or equal to the right.

```js
console.log(5 <= 5); // true
console.log(5 <= 10); // true
console.log(10 <= 5); // false
```
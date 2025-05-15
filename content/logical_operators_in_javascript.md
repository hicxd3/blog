+++
date = '2024-03-05T18:53:24+03:00'
title = 'Logical Operators in JavaScript'
categories = [ "javascript" ]
+++


Logical expressions in JavaScript can be combined to create checks, such as password validation.

For example, if we want a password to be more than 8 characters and less than 20, 
we can write a validation function like this:

```js
const isStrongPassword = (password) => {
  const length = password.length;
  return length > 8 && length < 20;
};
isStrongPassword('qwerty'); // false
isStrongPassword('qwerty1234'); // true
isStrongPassword('zxcvbnmasdfghjkqwertyui'); // false
```

`&&` means "AND". The entire expression is considered true only if **both** operands — 
on the left and right — are true. In other words, `&&` means "this **and** that".

Besides `&&`, the `||` operator — meaning "OR" — is also often used. 
It means "this or that or both". You can use as many AND and OR operators 
as needed, and combine them in any quantity or order.

Logical AND and OR have lower precedence than comparison operators, 
so it's better to use parentheses when combining them. 
Here’s an improved version of the password check:

```js
const isStrongPassword = (password) => {
  const length = password.length;
  return length > 8 && (hasSpecialChars(password) || hasCapitalChars(password));
};
```

Truth table for the `&&` operator:

```js
(true) && (true)   // ==> true
(true) && (false)  // ==> false
(false) && (true)  // ==> false
(false) && (false) // ==> false
```

Truth table for the `||` operator:

```js
(true) || (true)   // ==> true
(true) || (false)  // ==> true
(false) || (true)  // ==> true
(false) || (false) // ==> false
```

### Logical NOT Operator

In addition to `&&` (AND) and `||` (OR), JavaScript has the NOT operator `!`. 
It flips a boolean value to the opposite.

For example, if you have a function that checks whether a number is even, 
you can use the NOT operator to check if it's **not** even:

```js
const isEven = (number) => number % 2 === 0;
isEven(10);  // true
!isEven(10); // false
```

By simply adding the NOT operator before the function call, 
we get the opposite result.

This operator lets us implement logical rules in code 
without having to write new functions.

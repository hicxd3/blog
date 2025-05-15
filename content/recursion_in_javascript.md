+++
date = '2025-04-21T12:00:24+03:00'
title = 'Recursion in JavaScript'
categories = [ "javascript" ]
+++


Recursion is a programming concept where a function calls itself in order to solve a problem.  
Instead of handling the entire task at once, the function solves a small piece and passes the rest back to itself.

## Example: recursive power function (pow)

Let's create a simple recursive function that calculates `x` raised to the power of `n`.

```javascript
function pow(x, n) {
  if (n === 1) {
    return x;
  } else {
    return x * pow(x, n - 1);
  }
}

console.log(pow(2, 3)); // 2 * 2 * 2 = 8
```

**How it works:**  
- If `n` is 1, we return `x` (base case).  
- Otherwise, we multiply `x` by the result of `pow(x, n - 1)`.


## Example: power function using a loop

We can also solve the same problem with a simple `for` loop — without recursion.

```javascript
function powLoop(x, n) {
  let result = 1;
  for (let i = 0; i < n; i++) {
    result *= x;
  }
  return result;
}

console.log(powLoop(2, 3)); // 2 * 2 * 2 = 8
```

**How it works:**  
- We start with `result = 1`.
- Each loop multiplies `result` by `x` one more time until we've done it `n` times.


## Base case and recursive step

Every recursion must have **two essential parts**:

1. **The base case** — the condition where the recursion stops. Without it, the function would call itself forever and crash.
2. **The recursive step** — the part where the function reduces the problem and calls itself again with smaller or simpler input.

**Example:**

```javascript
function countdown(n) {
  if (n < 0) return;       // Base case
  console.log(n);          // Action
  countdown(n - 1);        // Recursive step
}
```

**How it works:**  
- Base case: When `n` becomes less than 0, we stop.  
- Recursive step: Each call reduces `n` by 1 until we reach the base.


## Depth of recursion

**Recursion depth** is the number of nested function calls that happen before reaching the base case.

Each time a function calls itself, it **goes deeper** into the call stack.

**Example:**

```javascript
function countdownDepth(n) {
  if (n === 0) {
    console.log('Reached the bottom!');
    return;
  }
  console.log(n);
  countdownDepth(n - 1);
}

countdownDepth(5);
```

**Important:**  
Too much recursion can cause an error:  
> Maximum call stack size exceeded

## Using Object.values() with recursion

When working with objects, recursion often helps us explore nested structures.  
`Object.values()` returns an array of all the values inside an object.

**Example: sum all numbers in a nested object**

```javascript
const salaries = {
  frontend: 1000,
  backend: 1500,
  designers: 800,
  managers: {
    lead: 2000,
    director: 3000
  }
};

function sumSalaries(obj) {
  let sum = 0;
  
  for (const value of Object.values(obj)) {
    if (typeof value === 'object') {
      sum += sumSalaries(value); // Recursive step
    } else {
      sum += value;
    }
  }
  
  return sum;
}

console.log(sumSalaries(salaries)); // 8300
```

## Checking arrays with Array.isArray()

When working with recursion, it’s important to know if a value is an array.  
`Array.isArray()` helps us check whether a given value is an array.

**Example:**

```javascript
console.log(Array.isArray([1, 2, 3])); // true
console.log(Array.isArray('Mia'));     // false
console.log(Array.isArray({ name: 'Eva' })); // false
```

**How it works:**  
- `Array.isArray([])` returns `true`.  
- Strings, objects, and other types return `false`.


## Summary

Today we explored recursion in JavaScript:  
- We learned how functions can call themselves.
- We practiced building base cases and recursive steps.
- We compared recursion with regular loops.
- We used tools like `Object.values()` and `Array.isArray()` to work with complex structures.

Recursion is powerful, beautiful, and a bit magical. Use it wisely, and it will open doors to solving problems that loops alone cannot!
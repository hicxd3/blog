
+++
date = '2025-01-10T18:53:24+03:00'
title = 'Loops in JavaScript'
categories = [ "javascript" ]
+++

When writing scripts, it's often necessary to perform the same action multiple times. For example, you might want to display all products from a list or loop through numbers from 1 to 10, performing the same action for each.

In such cases, programming languages offer loops. Loops allow you to repeat a specific block of code multiple times, making the code more compact and convenient when working with large data sets or repetitive tasks.

#### While Loop

The `while` loop is a way to organize repeated actions in JavaScript. Unlike the `for` loop, where the number of iterations is usually known in advance, the `while` loop is used when you need to run a block of code as long as a certain condition is true.

```js
let i = 0;
while (i < 5) {
    console.log("Iteration number: " + i);
    i++;
}
```

`i++` is the increment operator in JavaScript. It increases the value of the variable `i` by 1. It's a shorthand for `i = i + 1`.

The `while` loop is useful when the number of iterations is unknown and execution depends on a condition.

Examples:

1. Reading data from a file or stream until the end.
2. Waiting for a state change (e.g., animation completion).
3. Handling user input until valid data is entered.

#### do...while Loop

The `do...while` loop is a variant of the `while` loop in JavaScript that guarantees the loop body will execute at least once, even if the condition is initially `false`. This differs from the regular `while`, which might not run at all if the condition is false from the start.

```js
do {
  // loop body
} while (condition);
```

The loop body is executed first, then the condition is checked. If true, the loop repeats. This continues while the condition remains true.

This syntax is useful when you want the body to run at least once. However, in practice, `while (...) { ... }` is used more often.

```js
let i = 0;
do {
  alert(i);
  i++;
} while (i < 3);
```

#### For Loop

One of the most popular and frequently used loops in JavaScript. It's ideal when you know the exact number of iterations needed.

```js
for (start; condition; step) {
  // ... loop body ...
}
```

Simple example — this loop shows `i` values from 0 to 2 (not including 3):

```js
for (let i = 0; i < 3; i++) {
  alert(i); 
  // Will display 0, then 1, then 2
}
```

Detailed breakdown:

1. **Start**:
   `let i = 0` — runs once at the beginning. Declares the variable `i` and sets it to 0.

2. **Condition**:
   `i < 3` — checked before each iteration. If `true`, the loop continues. If `false`, it stops.

3. **Body**:
   `alert(i)` — runs each iteration while the condition is `true`.

4. **Step**:
   `i++` — runs after the loop body on each iteration. Increments `i` by 1.

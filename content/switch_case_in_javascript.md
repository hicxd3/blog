+++
date = '2024-05-05T18:53:24+03:00'
title = 'Switch / Case in JavaScript'
categories = [ "javascript" ]
+++

Other programming languages, in addition to the if conditional construct, support the switch operator. This is a specialized alternative to if, intended for specific scenarios. It is useful when a chain of if...else is needed to check for equality. For example:

```js
if (status === 'processing') {
  // Do one
} else if (status === 'paid') {
  // Do two
} else if (status === 'new') {
  // Do three
} else {
  // Do four
}
```

One of the peculiarities of this complex check is that each branch depends on the value of the `status` variable. The switch operator allows you to rewrite this code more concisely and expressively:

```js
switch (status) {
  case 'processing': // status === 'processing' (strict equality)
    // Do one
    break;
  case 'paid': // status === 'paid'
    // Do two
    break;
  case 'new': // status === 'new'
    // Do three
    break;
  default: // else
    // Do four
}
```

The switch operator is a complex construct due to the following components:

1. The switch header contains the `switch` keyword and the variable to evaluate.
2. Curly braces `{}` enclose the different execution options.
3. `case` and `default` blocks define behavior for different values of the variable. Each `case` is like an if clause, and `default` is similar to an else branch. `default` is optional but recommended for cleaner code.
4. The `break` statement prevents fallthrough—execution continuing into the next `case` block unnecessarily.

As a result, the switch operator is a powerful tool for selecting different execution paths in code.

Unlike other constructs, the curly braces in `switch` do not define a code block in the usual sense. Only `case` and `default` statements are allowed inside. Within each `case` or `default`, you can write arbitrary code, offering flexibility for program logic.

```js
switch (count) {
  case 1:
    // Do something useful
    break;
  case 2:
    // Do something useful
    break;
  default:
    // Do something
}
```

Sometimes, executing code inside a case block can lead to function termination. In that case, it's necessary to return the resulting value. There are two ways to do this.

**Approach 1:** Declare a variable before the switch, assign a value inside a case, and return it at the end of the function.

```js
(count) => {
  let result;
  switch (count) {
    case 1:
      result = 'one';
      break;
    case 2:
      result = 'two';
      break;
    default:
      result = null;
  }
  return result;
};
```

**Approach 2:** Use `return` directly inside the case block to return from the function. Since `return` ends function execution, there's no need for `break`.

```js
(count) => {
  switch (count) {
    case 1:
      return 'one';
    case 2:
      return 'two';
    default:
      return null;
  }
};
```

Using the `switch` operator is not strictly necessary from a technical standpoint—everything it does can be achieved with if/else. However, its main benefit lies in making the programmer's intention more explicit when checking specific values.

Although using `switch` may slightly increase the physical size of your code, it improves readability and clarity compared to a chain of `else if` blocks.
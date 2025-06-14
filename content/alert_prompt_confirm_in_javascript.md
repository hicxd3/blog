+++
date = '2025-01-08T18:53:24+03:00'
title = 'Alert, Prompt and Confirm in JavaScript'
categories = [ "javascript" ]
+++

Simple user interaction on a website can be done  
using the `alert()`, `prompt()`, and `confirm()` methods in JavaScript.

Although these methods aren’t used in real-world projects,  
it’s still worth learning them as part of the language fundamentals.

All three are somewhat similar to `console.log()` in how they output info.

#### Alert()

The syntax is very simple — and so is its behavior.  
`alert()` creates a modal popup with a message you define:

```js
alert('Hello, friends!');
```

#### Confirm()

This method is used to ask the user a yes/no question.
For example: “Are you over 18?”

```js
let result = confirm('Are you over 18?');
console.log(result);
```

It also opens a modal dialog, but with two buttons: OK and Cancel.
Clicking OK stores `true` in the result variable
Clicking Cancel stores `false`

#### Prompt()

Use `prompt()` to ask the user to input some text.
You can also provide a `default` value, just like a placeholder in HTML.

```js
let answer = prompt('How old are you?', '');
console.log(answer);
```

Any value returned from a prompt() will be a string,
even if the user types a number.

Here’s how to collect multiple answers into an array:

```js
let answers = [];
answers[0] = prompt('What is your first name?', '');
answers[1] = prompt('What is your last name?', '');
answers[2] = prompt('How old are you?', '');
console.log(answers);
```

These methods — `alert`, `prompt`, and `confirm` —
block page rendering until the user interacts with them.
That’s why they’re rarely used in modern UIs,
but still useful to know for learning and debugging.
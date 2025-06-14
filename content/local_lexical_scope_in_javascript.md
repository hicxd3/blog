+++
date = '2024-12-02T17:30:00+03:00'
title = 'Local Lexical Scope in JavaScript'
categories = ["javascript"]
+++

Local Scope Is Created Every Time a Function Is Defined

A local (lexical) environment is created every time a function is defined.
Variables declared inside that function become available only within its context — that is, inside the function itself.

These variables cannot be accessed from outside unless they are returned by the function.

```js
function test() {
  let localVar = 'I am a local variable';
  console.log(localVar); 
  // Accessible here
}

console.log(localVar); 
// Error — the variable doesn’t exist outside the function
```

In this example, the variable localVar exists only inside test.
It’s completely invisible and inaccessible outside that function.

That’s the essence of a local lexical environment in JavaScript.
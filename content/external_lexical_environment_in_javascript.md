+++
date = '2025-03-25T12:00:24+03:00'
title = 'External lexical environment in JavaScript'
categories = [ "javascript" ]
+++

An external lexical environment is an environment that exists in a broader context, that is, outside of a local function. This can be a global environment or an environment that "wraps around" the function in which the work is going on. If the function does not have access to any variable, it will look for it in the external environment.

```js
const message = "I'm everywhere!";
function showMessage() {
  console.log(message); 
  // Access to a global variable
}
ShowMessage(); 
// 'I'm everywhere!'
```

In this example, the `message` variable is available inside `ShowMessage` because it exists in a global lexical environment that is external to this function.
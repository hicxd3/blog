+++
date = '2025-03-06T12:00:24+03:00'
title = 'The textContent property in JavaScript'
categories = [ "javascript" ]
+++

The `textContent` property allows you to get or change the text inside the element, ignoring the `HTML markup`. It is useful when you need to work only with text, without worrying about tags.

```js
element.textContent = 'New text';
```

Example of getting text from inside an element

```js
let text = document.getElementById('box').textContent;
console.log(text);
// Outputs all the text inside the #box
```

An example of changing the text inside an element

```js
document.getElementById('box').textContent = 'Updated text';
```

Resetting the content of the element, you just need to pass an empty string.

```js
document.getElementById('box').textContent = '';
```

 The `textContent` property helps you work with text without the risk of inserting malicious code. If you don't need to render the `HTML`, but just change or receive the text, then you should remember the syntax.
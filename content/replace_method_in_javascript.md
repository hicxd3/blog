+++
date = '2025-03-08T00:53:24+03:00'
title = 'The replaceWith() method in Javascript'
categories = [ "javascript" ]
+++

The `replaceWith()` method allows you to replace an existing element with another element or text, completely removing the old node from the `DOM'.

```js
element.replaceWith(new Element);
```

Here, a `new Element` is a new element, text, or several nodes that will replace the old element.

The replacement example 

```js
let old Item = document.getElementById('old');
let new Item = document.createElement('div');
newItem.textContent = 'I'm a new element!';
oldItem.replaceWith(newItem);
```

An example of replacing an element with text

```js
document.getElementById('title').replaceWith('There was a Cxd3');
```

The `replaceWith()` method is a tool for replacing elements without changing the parent structure. It is ideal when you need to replace a component without removing or modifying other elements.
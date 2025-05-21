+++
date = '2025-03-27T09:00:24+03:00'
title = 'The getElementsByClassName() Method in JavaScript'
categories = [ "javascript" ]
+++

`getElementsByClassName` lets you find all elements that have a specific class on the page. This is a useful tool when working with a group of elements sharing the same style or functionality.

```js
document.getElementsByClassName(class);
```

You can pass one or multiple class names to the method, such as just `menu` or `header menu`. 

The method returns an `HTMLCollection` — a live collection containing all elements with the specified class. If no such elements exist on the page, an empty collection is returned.

Performing a search on the page for a specific class

```js
let boxes = document.getElementsByClassName('box');
console.log(boxes); 
// Will output the collection of all elements with the class "box"
```

Now let's change the background color of all elements with the `box` class

```js
for (let item of boxes) {
  item.style.background = 'yellow';
}
```

`getElementsByClassName` is a quick and convenient way to get a group of elements by class. However, if you need a static list or a more complex CSS selector, it's better to use `querySelectorAll`.
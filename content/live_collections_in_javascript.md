+++
date = '2025-04-25T17:30:00+03:00'
title = 'Live Collections in JavaScript'
categories = ["javascript"]
+++

A live collection is a special browser object that automatically updates when the DOM changes.

In other words:

When you select elements using `getElementsByTagName`, `getElementsByClassName`, or `children`,

You get a live collection that always reflects the current state of the DOM, without needing a new query.


Example:

```javascript
const list = document.getElementsByTagName('li'); // HTMLCollection — live collection
console.log(list.length); // for example 3

const newLi = document.createElement('li');
document.body.appendChild(newLi);

console.log(list.length); // now 4!
```

What happens:

We selected `list` once.

Then we added a new `<li>`.

The `list.length` **automatically updated** without a new query!


### Key Features of Live Collections

They react to any changes in the DOM.

They don't require new selection calls.

They lack full array methods like `map`, `filter`, etc.

For iteration, you can use `for...of`, `for`, or convert them with `Array.from()` if needed.


### Examples of Live Collections

`getElementsByTagName('div')`

`getElementsByClassName('button')`

`element.children`


### Be Careful

If the DOM changes frequently during script execution, the live collection updates too, which might affect your logic unexpectedly.


### Notes

Live collections are powerful and reactive.  

They keep up with DOM changes automatically, but you should be careful when writing scripts that rely on a stable structure.  

Understanding them gives you better control and safer manipulation of your web pages.
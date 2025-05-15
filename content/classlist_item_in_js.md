+++
date = '2025-04-28T08:10:24+03:00'
title = 'ClassList.item() in JavaScript'
categories = [ "javascript" ]
+++


Sometimes, when working with classList, we need to get a specific class by its position.
That's where the item method comes in.

Since item is a method and performs an action, we must always use parentheses () when calling it.

```javascript
const box = document.querySelector('.box');
console.log(box.classList.item(0)); // outputs the first class name
```

item returns the class name based on the index we pass inside the parentheses.
If the index is out of range, it simply returns null.

Using item is a clean way to access classes without converting classList into an array.

### Notes

item is a method, so we always use parentheses.
It helps us get a specific class by index from classList.
If the index doesn't exist, item returns null.

And that's it.
Simple, quick, and super useful when dealing with classes dynamically.

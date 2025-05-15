+++
date = '2025-03-10T09:00:24+03:00'
title = 'The cssText property in JavaScript'
categories = [ "javascript" ]
+++

The cssText property allows you to set multiple CSS styles for an element in one line at once. This is useful when you need to quickly apply multiple styles without using separate properties of the `style` object.


```js
element.style.cssText = 'rule1; rule2; ...';
``` 

A real code example for applying multiple styles

```js
let box = document.getElementById('myBox');
box.style.cssText = 'width: 200px; height: 100px; background: black;';
```

An example of adding new styles without deleting the old ones

```js
box.style.cssText += 'border: 2px solid black;';
```

If you refer to `cssText`, it will return the data as a string

```js
console.log(box.style.cssText); 
// "width: 200px; height: 100px; background: black;"
```

If you want to add styles without overwriting existing ones, it is better to use `classList.add()` to work with classes or separate `style` properties.

cssText is a fast way to apply styles en masse, but you need to be careful with it: it removes all previous inline styles. If the style of the element changes dynamically, it is better to use `style.property` or classes.
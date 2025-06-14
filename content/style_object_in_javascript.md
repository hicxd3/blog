+++
date = '2025-03-28T09:00:24+03:00'
title = 'The style Object in JavaScript'
categories = [ "javascript" ]
+++

The `style` object allows you to modify CSS styles of elements directly through JavaScript. You can dynamically change colors, sizes, fonts, and any other styles without editing CSS files.

To change the styles of an element, first you need to select it in JavaScript and then access its `style` property:

```js
let element = document.getElementById('myElement'); 
element.style.color = 'red'; 
// Changes text color to red
```

The style object contains properties that match CSS styles. However, names are written in camelCase instead of using hyphens like in regular CSS:

| CSS Property      | JavaScript Equivalent        |
|-------------------|------------------------------|
| background-color | backgroundColor |
| font-size | fontSize |
| margin-top | marginTop |


<br />

let box = document.querySelector('.box');

```js
box.style.width = '200px';
box.style.height = '100px';
box.style.backgroundColor = 'yellow';
box.style.border = '2px solid black';
```

To remove a style, you can assign an empty string:

```js
box.style.backgroundColor = ''; 
// Resets background color
```

The style object is useful for dynamically updating the appearance of elements. But if you need to apply many styles at once, it's better to use classList.add() and classList.remove() to manage CSS classes.
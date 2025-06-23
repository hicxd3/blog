+++
date = '2025-06-23T15:00:00+03:00'
title = 'Rotate Element with CSS deg'
description = 'How to rotate elements in CSS using transform and deg units'
categories = [ "css" ]
+++

Sometimes we want to give an element a little twist — like turning a card or spinning a button. In CSS, we can use the transform property with degrees — written as deg.

Here’s an example

HTML:

```html
<div class="card">Click me!</div>
```

CSS styling:

```css
.card {
  transform: rotate(15deg);
}
```

This rotates the .card 15 degrees clockwise.

Key Points ^-^

- deg stands for degrees — it tells how much to rotate

- rotate(15deg) turns clockwise, rotate(-15deg) counter-clockwise

- Can be animated or combined with hover for fun effects

- Works on any HTML element
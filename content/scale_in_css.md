+++
date = '2025-06-23T15:30:00+03:00'
title = 'How to Scale Elements in CSS'
description = 'Learn how to resize elements using transform: scale() in CSS'
categories = [ "css" ]
+++

The `scale()` function lets you resize an element — to zoom it in or shrink it down. It’s perfect for hover effects, animations, or UI feedback.

For exapmle

```css
.card:hover {
  transform: scale(1.2);
}
```

This makes the .card 20% larger when hovered.

You can also scale only one axis:

```css
.card {
  transform: scaleX(2); /* twice as wide */
}
```
And like this:
```css
.card {
  transform: scaleY(0.7); /* 70% of original height */
}
```

Key Points ^-^

- scale(n) changes both width and height

- Values < 1 shrink, values > 1 grow

- Use scaleX() or scaleY() to transform one axis

- Add transition for smooth scaling

- Great for buttons, cards, icons

+++
date = '2024-10-12T18:53:24+03:00'
title = 'Margin and Padding in CSS'
categories = [ "css" ]
+++


### The `padding` Property

Padding is the space between the content of an element and its border.

![Padding Example](../images/padding.png)

The inner spacing of an element is set using the `padding` property. If the padding is the same on all sides, you can simply write:

```css
.main__content {
  padding: 15px;
}
```

This is called shorthand syntax.

If the paddings differ on each side, you can use the full syntax, specifying each side separately:

```css
.main__content {
  padding-top: 5px;
  padding-right: 10px;
  padding-bottom: 15px;
  padding-left: 20px;
}
```

- `padding-top` adds space at the top
- `padding-right` on the right
- `padding-bottom` at the bottom
- `padding-left` on the left

### The `margin` Property

Margin is the space between the outer border of an element and the boundaries of its parent or neighboring elements.

The `margin` property is used to manage outer spacing. Like `padding`, it supports both shorthand and full syntax.

```css
/* Shorthand */
margin: 20px;

/* Full syntax */
margin-top: 0;
margin-right: 5px;
margin-bottom: 10px;
margin-left: 15px;
```

- `margin-top` creates space above the element
- `margin-right` on the right
- `margin-bottom` below the element
- `margin-left` on the left
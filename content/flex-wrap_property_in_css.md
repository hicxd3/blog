+++
date = '2024-11-13T18:53:24+03:00'
title = 'The flex-wrap Property'
categories = [ "css", "flexbox" ]
+++

Lecture from HTML Academy about the `flex-wrap` property in CSS.

If there are more flex items in the container than it can hold, the following will happen:

- Items will shrink to the smallest possible size.
- Even if explicit widths are set, the flexbox model may shrink them.
- If the items still don’t fit in the container, they will overflow, but stay on a single line.

This behavior can be changed using the `flex-wrap` property on the flex container.

By default, it is set to `nowrap`, which prevents flex items from wrapping to a new line.

```css
.flex_div {
  display: flex;
  flex-wrap: wrap;
}
```

The wrap value allows flex items to wrap onto multiple lines if they don’t fit within the container.

The flex-wrap: wrap-reverse Property

When wrapping is allowed, rows of items are placed along the cross axis: the first row starts at the beginning of the cross axis, and the last row ends at the bottom. This is the default behavior when using wrap.

If flex-wrap: wrap-reverse is applied, the rows will still wrap, but in reverse order: the first row will appear at the bottom of the cross axis, and the last row at the top.

```css
.flex_div {
  display: flex;
  flex-wrap: wrap-reverse;
}
```
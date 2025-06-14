+++
date = '2024-11-23T18:53:24+03:00'
title = 'The align-content Property in CSS'
categories = [ "css", "flexbox" ]
+++

Lecture from HTML Academy on `align-content`

The `justify-content` property controls the alignment of flex items along the **main axis**,  
while `align-content` controls the alignment of **rows** of flex items along the **cross axis**.  
Both properties share similar values:

1. `flex-start`  
2. `flex-end`  
3. `center`  
4. `space-between`  
5. `stretch` — available **only** for `align-content`, and it's the default value.

The `align-content` property **overrides** the value of `align-items`,  
which controls the alignment of individual flex items along the cross axis.  
This applies to both **a single row** and **multiple rows** of items.

However, there’s a caveat: `align-content` **won’t work** if the container has `flex-wrap: nowrap`.  
That’s because in that case, there’s only one row, and its height equals the container’s height —  
leaving no free space along the cross axis.

As a result, `align-content` has no effect.  
Instead, only `align-items` and `align-self` will apply (if item sizes allow),  
and you’ll see alignment based on those properties.

---

### `align-content: stretch` and the Role of `align-items`

When both `align-items` and `align-content` are set,  
`align-items` is **not disabled** — it still affects how items behave **within** each row.

This is especially noticeable when `align-content` is set to the default value `stretch`.  
In this case, **rows** are stretched to fill all available space along the cross axis,  
and the remaining free space between the rows is evenly distributed.

How rows behave with `align-content: stretch` depends on the value of `align-items`:

1. If `align-items` is set to `stretch`, items inside the rows stretch to fill the full height of their row.  
2. If `align-items` is anything else (like `flex-start`, `center`, `flex-end`),  
   items shrink to fit their content and align according to the `align-items` value.

So even if `align-content` is set to `stretch`, `align-items` still determines  
how items inside the rows are aligned vertically.

---

### The `order` Property — Reordering Flex Items

Another useful property is `order`, which defines the **order number** of a flex item.

```css
.flex-element {
  /* this item will appear first */
  order: -1;
}

By default, the order of all flex items is 0, and they’re displayed in ascending order.

The order property is especially useful when you want to change the visual order
of elements without touching the `HTML` markup.
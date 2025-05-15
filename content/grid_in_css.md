+++
date = '2024-10-12T18:53:24+03:00'
title = 'Grid In Css'
categories = [ "css", "grid" ]
+++

A box container of the grid type contains child elements called grid items.  
Although the grid container looks like a regular block-level element for other elements like main content, the grid items inside behave differently.

For example, even inline elements begin to take up the full available area, and the margins of elements inside a grid container behave differently too.

By default, a grid container has a single column.  
To change this, you need to define a grid template using the `grid-template-columns` property.

```css
.grid-container {
  display: grid;
  grid-template-columns: 100px 150px 80px;
}
```

In addition to `grid-template-columns`, other properties like `grid-template-rows` and `grid-template-areas` can also be used to define the layout of the grid container.

If the number of items inside the grid container exceeds the number of columns, the extra elements automatically wrap to a new row and are distributed across the columns again.

### Grid Fractions with `fr`

The `fr` unit (short for “fraction”) represents a portion of the available space in the grid container.

```css
.grid-container {
  display: grid;
  grid-template-columns: 1fr 2fr;
}
```

In this example, the grid container will be divided into three equal parts.  
The first column will take one part of the container’s width, and the second column will take two parts.  
No matter how the container’s width changes, the column proportions will remain constant.

The `fr` unit can also be used in combination with pixels.  
For example, you can create a layout where the right column is fixed at 200 pixels and the left column takes up the remaining space:

```css
.grid-container {
  display: grid;
  grid-template-columns: 1fr 200px;
}
```

### The `gap` Property

The `gap` property defines the space between grid items but does not affect the space between items and the container’s border.

The `gap` property is applied to the grid container, while `margin` is applied to the items inside it.

Using `gap`, you can set spacing separately for rows and columns: `column-gap` defines space between columns, and `row-gap` defines space between rows.

```css
.grid-container {
  column-gap: 15px;
  row-gap: 5px;
}
```

If the spacing is the same, you can use the shorthand property `gap` for convenience:

```css
.grid-container {
  gap: 20px;
}
```

+++
date = '2025-07-01T23:00:00+03:00'
title = 'Spacing with column-gap'
description = 'Control the space between columns in multi-column layouts'
categories = [ 'css' ]
+++

## Column-gap in CSS

The `column-gap` property sets the space between columns created with `column-count`.

```css
.columned {
  column-count: 2;
  column-gap: 40px;
}
```

This code creates a two-column layout inside any element with the class columned. 

The column-gap of 40px sets a clear, readable space between the two columns — preventing the text from feeling too tight or overwhelming.

Key Points ^-^

- Works with column-count, column-width

- Controls the spacing between columns

- Default value is normal

- You can use px, em, %

Use it to improve readability and avoid cramped layouts.
+++
date = '2025-07-01T22:50:00+03:00'
title = 'Column-count for Multi column Layouts in CSS'
description = 'Split content into columns with column-count'
categories = [ 'css' ]
+++

## Column-count in CSS

The `column-count` property lets you split content into multiple columns.

```css
.columned {
  column-count: 2;
}
```

This will break the content into two vertical columns.

Key Points ^-^

- Works on block-level containers

- Common for articles, lists, or magazine-style layouts

- Combine with column-gap for spacing

- Use column-rule for visual dividers

Simple way to add structure without using flex or grid.
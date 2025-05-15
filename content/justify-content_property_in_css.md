+++
date = '2024-11-21T18:53:24+03:00'
title = 'The justify-content Property'
categories = [ "css", "flexbox" ]
+++

In Flexbox, the `justify-content` property allows you to evenly distribute items along the main axis:

- `space-between` — equal spacing between adjacent elements, with no space between the elements and the container edges.
- `space-around` — equal spacing between elements, but the spacing between the elements and the edges of the container is half the spacing between elements.
- `space-evenly` — equal spacing between all elements and the container edges.

The `justify-content` property controls how elements are aligned along the main axis and accepts the following values:

- Default value `flex-start` — aligns elements to the start of the main axis.

```css
justify-content: flex-start;
```

- `flex-end` — aligns elements to the end of the main axis.

> Note: `justify-content: flex-end` does not change the order of elements, unlike `flex-direction: row-reverse`.

```css
justify-content: flex-end;
```

- `space-between` — equal spacing between adjacent elements, with no spacing at the container edges.

```css
justify-content: space-between;
```

- `space-around` — equal spacing between elements; spacing at the container edges is half the spacing between elements.

```css
justify-content: space-around;
```

- `space-evenly` — equal spacing between all elements, including container edges.

```css
justify-content: space-evenly;
```
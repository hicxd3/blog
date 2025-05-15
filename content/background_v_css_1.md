+++
date = '2024-11-22T18:53:24+03:00'
title = 'Background in CSS (Part 1)'
categories = [ "css" ]
+++

The background color of an element in CSS is set using the `background-color` property.

CSS provides various ways to define colors — such as hexadecimal (HEX), RGB or RGBA formats, or predefined color names.

Example:

```js
background-color: red;
background-color: #ff0000;
background-color: rgba(255, 0, 0, 0.5);
```

---

A background image can be set using the CSS property `background-image`.

Use the following syntax:

```js
background-image: url("img/image.png");
```

The image URL must be placed inside the `url("...")` function.


The image address must be specified inside the url("...") function. Background image paths are similar to regular image paths. An element can simultaneously have both a background color and a background image. In this case, the image will appear on top of the background color.

## The background-repeat property

By default, the background image is repeated. This is especially noticeable when the image is smaller than the block. You can control this behavior using the CSS `background-repeat` property. It has four values:

- `repeat` — repeat in all directions (default).
- `repeat-x` — repeat horizontally only.
- `repeat-y` — repeat vertically only.
- `no-repeat` — do not repeat.

## The background-position property

The `background-position` property controls the placement of the background image. It consists of two values separated by a space: `x` and `y`.

- `x` defines the horizontal position.
- `y` defines the vertical position.

You can use keywords (`left`, `center`, `right`), percentages, and pixels as values for `x`. For `y`, you can also use keywords (`top`, `center`, `bottom`), percentages, and pixels.

Examples:

```css
background-position: 50% 50%; /* image will be centered */
background-position: right bottom; /* bottom right corner */
background-position: 50px 100px; /* 50px from left, 100px from top */
background-position: 0 100%; /* bottom left corner */
background-position: left bottom; /* bottom left corner */
```

Results of the examples:

- The image will be centered.
- The image will be in the bottom right corner.
- The image will be 50px from the left and 100px from the top.
- The image will be in the bottom left corner.
- The image will be in the bottom left corner.

If the background image is larger than the block, it will be cropped. You can control which part of the image is visible using the `background-position` property.

It is sometimes convenient to use relative values (percentages), and in other cases — absolute (pixels).

Moreover, you can use not only positive values, but also negative ones. It's also possible to combine pixels and percentages.

## The background-attachment property

Usually, the background image scrolls along with the content of the block. However, with the `background-attachment` property, you can fix the background in place so it doesn't scroll.

Property values:

- `scroll` — the background scrolls with the content (default).
- `fixed` — the background stays fixed and does not scroll.

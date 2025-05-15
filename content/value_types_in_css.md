+++
date = '2024-10-08T18:53:24+03:00'
title = 'Value Types in CSS'
categories = [ "css" ]
+++

### Absolute Values

The simplest type of values are absolute values, such as pixels. They are used to define the size of elements, text, and other properties.

```css
width: 1000px;
font-size: 16px;
```

Absolute values are advantageous because they are finite, clear, and easy to understand.

### Relative Values

The magnitude of relative values is not immediately clear — you must first know the previous value, multiply it, and only then get the output.

Relative values, unlike absolute ones, are more complex because they are not fixed — they depend on other values.

For example, the width of an element defined in percentages depends on the width of its parent element. The browser calculates the width by multiplying the parent's width by the specified percentage and then derives the absolute value in pixels.

Note: during page rendering, all relative values are ultimately converted into absolute values; otherwise, the page cannot be displayed correctly.

Besides percentages, there are other relative units:

```css
width: 50%;      /* Relative to parent width */
width: 100vw;    /* Relative to viewport width */
height: 100vh;   /* Relative to viewport height */
font-size: 2em;  /* Relative to parent font size */
font-size: 2rem; /* Relative to root element font size (html) */
```

`vh` and `vw` define the size relative to the viewport — the visible part of the browser window. `vh` depends on the viewport height and is often used to create full-screen sections.

`em` is relative to the font size of the parent element. For example, if the parent has a font size of 20px and the child element is set to 2em, the computed size will be 40px.

`rem` is similar to `em`, but it refers to the root element’s font size. On a typical page, the root element is the `<html>` tag.

So, if the root element’s font size is 16px, and a tag on the page is given a font size of 2rem, the resulting size will be 32px.

### Keyword Values

The next type of values are keywords. These are straightforward and only require memorization.

```css
text-transform: uppercase;
text-align: center;
display: block;
color: red;
```

### Color Values

Another specific type of value is colors, which can be represented in various formats.

```css
color: #f00;       /* shorthand hex */
color: #ff0000;    /* full hex */
color: rgb(255, 0, 0);
color: rgba(255, 0, 0, 0.5);
color: hsl(0, 100%, 50%);
color: hsla(0, 100%, 50%, 0.5);
```

Colors can be expressed in hex, rgb, or rgba formats. In hex, such as `#ff0000`, each pair of hex digits encodes red, green, and blue channels in a range from 0 to ff (or 0 to 255). The shorthand version duplicates digits, so `#f00` is equal to `#ff0000`.

In rgb and rgba, color channels are decimal values from 0 to 255, making them easier to understand. For instance, `color: #ff0000` and `color: rgb(255, 0, 0)` are equivalent.

The rgba format adds an alpha channel representing opacity from 0 (transparent) to 1 (fully opaque).

HSL and HSLA formats are similar to RGB but more familiar to graphic designers. Keywords can also be used to define colors.

### Function Values

Function values include expressions like `calc` and `linear-gradient`, which are especially useful.

```css
content: attr(href); 
/* Gets attribute content */
width: calc(100% - 100px); 
/* Performs calculations */
background-image: linear-gradient(45deg, yellow, green); 
/* Linear gradient */
```

`calc` enables complex behavior such as combining different units: "width: 200px + 10em".

`attr` is less commonly used but available.

### CSS Directives and @media Queries

Special constructs starting with `@` are called directives. These affect the entire document but do not apply styling directly.

For example, `@font-face` allows custom fonts to be imported and used in `font-family`.

Another example is `@media`, which enables or disables certain rules depending on conditions like screen size.

```css
@font-face {
  font-family: "Open Sans";
  src:
    url("OpenSans-Regular.woff2") format("woff2"),
    url("OpenSans-Regular.woff") format("woff");
}

@media (max-width: 600px) {
  .sidebar {
    display: none;
  }
}
```
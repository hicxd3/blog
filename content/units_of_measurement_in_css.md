
+++
date = '2024-10-08T18:53:24+03:00'
title = 'Units of Measurement in CSS'
categories = [ "css" ]
+++

Units of measurement in CSS are used to define the sizes of elements, spacing, fonts, and other properties.
They are divided into **absolute** and **relative** types.

This lecture covers five core units: `px`, `em`, `rem`, `fr`, and `%`.

### Pixels `px`

A pixel can be **physical** or **CSS-pixel**.

- A physical pixel is a single cell on a device's screen matrix.
  For example, if a screen width is 480px, this means there are 480 indivisible cells across it.
- A CSS pixel is a CSS unit equal to 1/96 of an inch.
  One CSS pixel does not always correspond to a physical screen cell — it depends on the screen density.
  The more physical pixels per inch, the more detailed the image.

```css
.content__main {
  width: 200px;
  height: 100px;
  background-color: FFA181;
  font-size: 24px;
  padding: 10px;
  margin: 20px;
}
```

### Font Size `rem`

The `rem` unit is relative to the root element’s font size (usually the `<html>` tag).
For example, if the root font size is `16px`, then:

```css
.body {
  font-size: 16px;
}
h1 {
  font-size: 2rem; 
  /* equals 32px */
}
p {
  font-size: 1.5rem; 
  /* equals 24px */
}
```

### Font Size `em`

The `em` unit is relative to the font size of the parent element.
If the parent has a font size of `16px`, then `font-size: 1.5em;` will result in `24px`.

```css
h1 {
  font-size: 2em;
  color: #FF0000;
}
p {
  font-size: 1.2em;
  color: #000000;
  line-height: 1.5em;
}
```

### Percentage `%`

Percentages are relative to the size of the parent element.
For example, if the parent is `100%` wide, then `width: 50%;` will set the child’s width to 50% of the parent.

```css
.container {
  width: 80%;
  margin: 0 auto;
  text-align: center;
}
.box {
  width: 50%;
  height: 200px;
  background-color: blue;
  margin: 20px auto;
}
```

The container takes 80% of the parent’s width, and `.box` takes 50% of the container’s width.

### Fractions `fr`

The `fr` unit stands for **fraction of available space**. It's used in **CSS Grid** to distribute free space between columns or rows.

```css
.container {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
  grid-gap: 10px;
}
```

In this example, the available space is divided into 4 parts — the first and third columns each take 1 part, and the second column takes 2.

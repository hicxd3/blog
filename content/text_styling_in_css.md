+++
date = '2024-11-14T18:53:24+03:00'
title = 'Text Styling in CSS'
categories = [ "css" ]
+++

In this lesson, we will go over the most common CSS properties used for text styling.

## `color`

The `color` property sets the text color of an element.

```css
p {
  color: red;
}
```

## `text-align`

The `text-align` property sets the horizontal alignment of the text. Common values:

- `left`
- `right`
- `center`
- `justify`

```css
h1 {
  text-align: center;
}
```

## `text-decoration`

The `text-decoration` property controls the text decoration, such as underline, overline, or line-through.

```css
a {
  text-decoration: none;
}
```

## `text-transform`

This property controls the letter case of the text:

- `uppercase` — transforms all letters to uppercase
- `lowercase` — transforms all letters to lowercase
- `capitalize` — capitalizes the first letter of each word

```css
p {
  text-transform: uppercase;
}
```

## `font-style`

The `font-style` property sets the style of the font, such as italic:

```css
em {
  font-style: italic;
}
```

## `font-weight`

This property sets the boldness of the text.

```css
strong {
  font-weight: bold;
}
```

You can also use numeric values from `100` to `900`.

## `font-size`

The `font-size` property sets the size of the text. You can use:

- pixels (`px`)
- em/rem
- percentages (`%`)

```css
h1 {
  font-size: 24px;
}
```

## `line-height`

This property controls the line spacing between lines of text:

```css
p {
  line-height: 1.5;
}
```

## `letter-spacing` and `word-spacing`

Use these properties to control the spacing between letters and words:

```css
h2 {
  letter-spacing: 2px;
  word-spacing: 5px;
}
```

These text styles help create more readable and aesthetically pleasing content on your websites. 
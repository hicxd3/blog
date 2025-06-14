+++
date = '2024-10-06T18:53:24+03:00'
title = 'Nested Selectors in CSS'
categories = [ "css" ]
+++

### Nested or Contextual Selector in CSS

This type of selector is a combination of two selectors separated by a space. These selectors are known as nested or contextual and are interpreted from right to left. It’s important to note that these references can be directly within the specified class tag or within nested tags at any depth.

```css
.nav__list a { 
  /* Targeting the <a> tag inside the .nav__list class */
  font-size: 16px;
}
```

You can combine any type of selectors using a space. In the example below, the selector targets all elements with the class `warning` that are inside elements with the class `text`.

```css
.text .warning { 
  /* Targeting the .warning class inside .text class */
  color: red;
}
```

You can also use combinations of three, four, or more selectors. However, it’s common practice to limit nesting to two levels, as simpler selectors are easier to read and maintain.

### Pseudo-elements and Pseudo-classes in CSS

Selectors can be extended using what are called pseudo-classes, which come in several forms.

Some pseudo-classes allow selection based on the element’s position relative to other elements. For example, you can select the first or last item, every second or every third item, etc.

There are also pseudo-classes that let you react to element states. For instance, an input field can change when hovered over with the mouse or when focused.

Additionally, there are special pseudo-classes for form elements, such as selecting all required fields or all optional ones.

Here’s a quick comparison between pseudo-elements and pseudo-classes in terms of syntax:

- Pseudo-elements use two colons `::`
  - For example: `::before` and `::after`

- Pseudo-classes use a single colon `:`
  - For example: `:hover`

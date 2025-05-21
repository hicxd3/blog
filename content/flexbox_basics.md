+++
date = '2024-10-13T18:53:24+03:00'
title = 'Flexbox Basics'
categories = [ "css", "flexbox" ]
+++

To take advantage of the unique properties of flex (from the English word "flexible"), you first need to change the element type using the `display` property:


```css
display: flex;
```

A container with `display: flex` is called a **flex container**, and its child elements are called **flex items**.

Flex items are automatically arranged along the main axis. By default, the main axis runs from left to right.

<img src="../images/flex1.1.png" />

By default, flex items do not wrap onto a new line and shrink to fit their content. Because of this behavior, it's often recommended to set a width or allow wrapping for flex items.
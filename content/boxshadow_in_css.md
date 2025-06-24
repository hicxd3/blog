+++
date = '2025-06-24T10:00:00+03:00'
title = 'Box-Shadow in CSS'
description = 'Learn how to add shadows to elements using box-shadow and its six parameters'
categories = [ "css" ]
+++

`box-shadow` in CSS adds a shadow around an element.
It’s a great way to create depth and highlight parts of your layout.

Let’s try it with Mia

```html
<div class="card">Hello from Mia!</div>
```

CSS Styling
```css
.card {
  box-shadow: 4px 6px 12px 0px rgba(0, 0, 0, 0.2);
}
```

Key Points ^-^

- offset-x → horizontal position of the shadow

- offset-y → vertical position of the shadow

- blur-radius → how soft or sharp the shadow is

- spread-radius → how much the shadow grows

- color → any valid color, usually with transparency

- inset → optional, makes the shadow go inside

You can layer multiple shadows too!
And with hover, they feel alive
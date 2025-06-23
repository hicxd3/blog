+++
date = '2025-06-23T15:45:00+03:00'
title = 'Using Opacity in CSS'
description = 'Learn how to fade elements in and out using opacity'
categories = [ "css" ]
+++

Sometimes you want to show something... softly.
`opacity` lets you fade elements in and out.

Let’s say we have a photo of Anna :)

```html
<img class="girl" src="anna.png" />
```

CSS styling
```css
.girl {
  opacity: 0.6;
  transition: opacity 0.3s ease;
}

.girl:hover {
  opacity: 1;
}
```

Anna becomes fully visible when you hover her 

Key Points ^-^

- opacity goes from 0 (invisible) to 1 (fully visible)

- Use transition for smooth fading

- Works great with :hover, :focus, or disabled

- Element stays in layout even if invisible

- Softens the UI, makes interactions gentle
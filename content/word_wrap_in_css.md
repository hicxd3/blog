+++
date = '2025-07-01T21:00:00+03:00'
title = 'How word-wrap Works'
description = 'Make long words behave with word-wrap in CSS'
categories = [ 'css' ]
+++

## How word-wrap Works in CSS

Sometimes, long words or links break your layout.

To handle that, use:

```css
word-wrap: break-word;
```

It tells the browser: if the word is too long — break it to the next line.

Key Points ^-^

`normal` — words stay in one line

`break-word` — breaks long words if needed

Same as overflow-wrap: break-word; in modern CSS

Use it to keep your layout clean and readable, even with wild content.
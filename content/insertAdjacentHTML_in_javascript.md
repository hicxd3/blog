+++
date = '2025-03-05T12:00:24+03:00'
title = 'The insertAdjacentHTML() Method in JavaScript'
categories = [ "javascript" ]
+++

The `insertAdjacentHTML()` method allows you to insert `HTML code` at a specific position relative to an existing element without overwriting its content.

```js
element.insertAdjacentHTML(position, htmlString);
```

In the `position` string, you specify where to insert the HTML markup.

In `htmlString`, you pass the actual `HTML` code.

List of possible values:

| Value           | Where it inserts                    |
|-----------------|-------------------------------------|
| beforebegin | Before the element (outside)        |
| afterbegin | Inside the element, at the beginning|
| beforeend | Inside the element, at the end      |
| afterend | After the element (outside)         |

<br />

Example of adding content before the element:

```js
let box = document.getElementById('box');
box.insertAdjacentHTML('beforebegin', '<p>Text before the block</p>');
```

The `insertAdjacentHTML()` method allows you to inject code exactly where you need it without unnecessary changes or creating temporary elements.

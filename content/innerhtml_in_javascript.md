+++
date = '2025-03-07T00:53:24+03:00'
title = 'The innerHTML Property in JavaScript'
categories = [ "javascript" ]
+++

`innerHTML` is a property that allows you to get and modify the `HTML content` inside an element. It gives full control over the content, including inserting new tags.

```js
element.innerHTML = 'new HTML-tag';
```

Example of replacing an element's content

```js
document.getElementById('box').innerHTML = '<strong>New Text</strong>';
```

You can also add new `HTML` markup by replacing the entire content

```js
let list = document.getElementById('list');
list.innerHTML = '<li>Element 1</li><li>Element 2</li>';
```

`innerHTML` lets you manipulate the contents of an element, but it requires caution. If you're working with dynamic data, you must be careful to avoid injecting unwanted `HTML` into the code.
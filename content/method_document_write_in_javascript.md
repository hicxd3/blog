+++
date = '2025-01-08T18:55:24+03:00'
title = 'The document.write Method in JavaScript'
categories = [ "javascript" ]
+++

The `document.write` method is one of the oldest ways to add text to a webpage.

The method `document.write(str)` works only during the loading of an HTML page. It adds text at the current location in the HTML document before the browser finishes building the DOM tree.

After rendering, the HTML document will contain the numbers **1 2 3**.

```html
<body>
  1
  <script>
    document.write(2);
  </script>
  3
</body>
```

The `document.write` method does not impose restrictions on the content being written. It simply inserts the string into the HTML document as if it were part of the original code, without validating the correctness of the tag structure.

For example:
```html
<script>
  document.write("<p>This text will be added to the document.</p>");
  document.write("<div>Even if tags are not closed, like <span>this text</div>");
</script>
```

In this example, even though the structure is incorrect (the `<span>` tag is not closed), the text will still be added to the document without any errors. However, this can lead to rendering or behavior issues on the page.
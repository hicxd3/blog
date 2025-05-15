+++
date = '2025-03-26T09:00:24+03:00'
title = 'The getElementsByTagName() method in JavaScript'
categories = [ "javascript" ]
+++

# The getElementsByTagName Method in JavaScript

The `getElementsByTagName()` method returns a collection of all elements with the specified tag name.

This method is often used when you want to retrieve all elements of a specific type, such as all `<p>` tags or `<div>` tags on the page.

## Syntax

```js
document.getElementsByTagName(tagName);
```

- `tagName`: The name of the tag you want to find (e.g., `'p'`, `'div'`, `'li'`).

This method returns an **HTMLCollection**, which is a live list of elements.

## Example

```js
const paragraphs = document.getElementsByTagName('p');
console.log(paragraphs.length); 
// Outputs the number of <p> elements

for (let i = 0; i < paragraphs.length; i++) {
  console.log(paragraphs[i].textContent);
}
```

## Notes

- This method is case-insensitive in HTML, so `'p'` and `'P'` are treated the same.
- If no elements are found, it returns an empty collection, not `null`.

Use this method when you want to get multiple elements of the same tag type and iterate through them.

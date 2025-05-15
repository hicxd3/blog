+++
date = '2025-04-20T18:53:24+03:00'
title = 'Navigating the DOM in JavaScript'
categories = ["javascript" ]
+++

When we work with the DOM, sometimes we don't just need to find one element — we need to **walk** through the tree: find parents, children, and siblings.  
Today, we'll learn how to do it easily and beautifully!


#### document.body and document.head

`document.body` gives access to everything visible on the page.  
`document.head` gives access to the invisible but important parts like styles and scripts.

```javascript
console.log(document.body);  // Visible content
console.log(document.head);  // Head section
```


#### documentElement

`document.documentElement` is the whole page — the entire `<html>` tag.

```javascript
console.log(document.documentElement); // <html>...</html>
```


#### Child Nodes: childNodes

`childNodes` contains everything inside an element: tags, text nodes, comments.

```javascript
const nodes = document.body.childNodes;
console.log(nodes);
```


#### First and Last Child: firstChild and lastChild

`firstChild` and `lastChild` get the first and last node — not necessarily an element!

```javascript
const first = document.body.firstChild;
const last = document.body.lastChild;
console.log(first, last);
```


Real Elements Only: firstElementChild and lastElementChild

`firstElementChild` and `lastElementChild` ignore text and focus only on real elements!

```javascript
const firstElement = document.body.firstElementChild;
const lastElement = document.body.lastElementChild;
console.log(firstElement, lastElement);
```


#### Parent Element: parentNode

`parentNode` gives you the parent of an element — the one holding it in the DOM.

```javascript
const miaButton = document.querySelector('button');
console.log(miaButton.parentNode);
```


#### Siblings: nextSibling, previousSibling

`nextSibling` and `previousSibling` can return any node — even whitespace or text.

```javascript
const node = document.querySelector('h1');
console.log(node.nextSibling);
console.log(node.previousSibling);
```


Real Siblings: nextElementSibling, previousElementSibling

`nextElementSibling` and `previousElementSibling` skip text nodes and find only real HTML neighbors!

```javascript
const realNode = document.querySelector('h1');
console.log(realNode.nextElementSibling);
console.log(realNode.previousElementSibling);
```


#### Working with data-attributes

`data-attributes` let you store extra information inside HTML elements, easily accessed via `.dataset`.

```html
<button data-current="5" data-user="eva">Click me</button>
```

```javascript
const btn = document.querySelector('button');
console.log(btn.dataset.current); // '5'
console.log(btn.dataset.user);    // 'eva'
```

#### Notes

Today, we learned to:
- Navigate up, down, and sideways through the DOM!
- Tell nodes apart from real elements.
- Work with parents and siblings.
- Store and access extra data with data-attributes.


+++
date = '2025-03-23T12:00:24+03:00'
title = 'The classList Property in JavaScript'
categories = [ "javascript" ]
+++

The `classList` property is a convenient way to work with an element’s classes in the DOM (Document Object Model). It provides methods for adding, removing, checking, and toggling element classes on a web page.

To use `classList`, you first need to get a reference to the DOM element. After that, you can manipulate its classes using this property.

```js
let element = document.querySelector('#myElement');
console.log(element.classList); 
// Outputs the list of classes on the element
```

### Common classList Methods

The `.add` method adds one or more classes to an element.

```js
element.classList.add('new-class'); 
// Adds the 'new-class'
```

The `.remove` method removes a specified class.

```js
element.classList.remove('old-class'); 
// Removes the 'old-class'
```

The `.contains` method checks if the element has a specified class. Returns `true` or `false`.

```js
console.log(element.classList.contains('active')); 
// true if the 'active' class is present
```

The `.item` method returns the class name at the specified index in the class list.

```js
console.log(element.classList.item(0)); 
// Returns the first class name of the element
```

Thanks to the `classList` property, working with element classes has become much simpler and more convenient. It provides direct access to class manipulation methods, helping avoid errors and making code cleaner.

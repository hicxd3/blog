+++
date = '2025-04-28T08:00:24+03:00'
title = 'Working with classList in JavaScript'
categories = [ "javascript" ]
+++

When we work with DOM elements, we often need to add, remove, or check CSS classes.
That's where the classList property comes in handy.

classList is a special property available only on DOM elements.
It allows us to easily manage the classes without touching the className string manually.

We can't use classList on pseudoelements or pseudocollections like NodeList or HTMLCollection.
classList belongs strictly to individual elements.

To use classList, we simply access it through the dot notation on a DOM element.

```javascript
const button = document.querySelector('.my-button');
console.log(button.classList); // outputs the list of classes
```

Here, classList gives us a live collection of all classes applied to the button element.

We can also quickly check how many classes an element has by using the .length property:

```javascript
const card = document.querySelector('.profile-card');
console.log(card.classList.length); // outputs the number of classes
```

This is super useful when you want to verify if an element has multiple classes applied.

### Notes

classList works only on real DOM elements, not on NodeLists or HTMLCollections.
We always access classList through the dot notation.
Using .length, we can easily count how many classes are on an element.

And that's it.
Simple, clean, and very useful for everyday work with DOM elements.
Let’s continue exploring JavaScript together!

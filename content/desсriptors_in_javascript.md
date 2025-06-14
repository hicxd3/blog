+++
date = '2025-04-26T18:53:24+03:00'
title = 'Property Descriptors and Useful Methods in JavaScript'
categories = [ "javascript" ]
+++


Every property in an object has hidden settings:  

Whether its value can be changed (`writable`),  

Whether it shows up during enumeration (`enumerable`),  

Whether it can be deleted or reconfigured (`configurable`).

These settings are called **property descriptors**.


### Getting a Property Descriptor

Use: getOwnPropertyDescriptor(obj, prop).

Example with Mia:

```javascript
const mia = {
  name: 'Mia',
  age: 23
};

let descriptor = Object.getOwnPropertyDescriptor(mia, 'age');
console.log(descriptor);
```


#### Defining a Property Descriptor

Use: defineProperty(obj, prop, descriptor).

Example with Eva:

```javascript
const eva = {};

Object.defineProperty(eva, 'isCoder', {
  value: true,
  writable: false,
  enumerable: true,
  configurable: true
});

console.log(eva.isCoder); // true
eva.isCoder = false;
console.log(eva.isCoder); // still true!
```


#### Defining Multiple Properties: defineProperties()

Example with Elle:

```javascript
const elle = {};

Object.defineProperties(elle, {
  city: {
    value: 'Paris',
    writable: true,
    enumerable: true
  },
  age: {
    value: 21,
    writable: false,
    enumerable: false
  }
});

console.log(elle.city); // Paris
console.log(elle.age);  // 21
```


### Fun Tricks:

Hidden property:

Make a property invisible during enumeration `enumerable: false`

```javascript
const anna = {};

Object.defineProperty(anna, 'secret', {
  value: 'I love coding',
  enumerable: false
});

console.log(Object.keys(anna)); // []
console.log(anna.secret); // "I love coding"
```


Immutable property:

Set `writable: false` to lock the value.

Protected structure:  
Set `configurable: false` to prevent deleting the property.


### Notes

`writable: false` locks a property's value.

`enumerable: false` hides a property during loops.

`configurable: false` makes a property undeletable and its settings permanent.

Mastering property descriptors gives you fine-grained control over how objects behave and interact in your applications.
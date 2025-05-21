+++
date = '2025-04-27T11:53:24+03:00'
title = 'Iterable Objects in JavaScript'
categories = [ "javascript" ]
+++

An **iterable** is an object that can be iterated over with `for...of` because it implements a special method: `Symbol.iterator`.

In simple words:  

If an object has `obj[Symbol.iterator]`, it is iterable!


#### Examples of Iterables

Arrays: `['Mia', 'Eva', 'Elle']`

Strings: `'Hello'`

Map: `new Map()`

Set: `new Set()`

NodeList: (querySelectorAll('div'))


#### Simple Example

```javascript
const girls = ['Mia', 'Eva', 'Elle'];

for (const girl of girls) {
  console.log(girl);
}
```

#### How It Works Under the Hood

When we use `for...of`, JavaScript looks for the `Symbol.iterator` method and calls it.  
This method returns an **iterator** object with a `next()` method.

Each call to `next()` gives the next value.


Mini-emulation:

```javascript
const girls = ['Mia', 'Eva', 'Elle'];
const iterator = girls[Symbol.iterator]();

console.log(iterator.next()); // { value: 'Mia', done: false }
console.log(iterator.next()); // { value: 'Eva', done: false }
console.log(iterator.next()); // { value: 'Elle', done: false }
console.log(iterator.next()); // { value: undefined, done: true }
```

#### Why It Matters

To create custom iterable objects.

To understand how `for...of`, destructuring, and spread operators `[...]` work.

To realize why plain objects `{}` are not iterable by default.


#### Custom Iterable Example

**Example with Anna and her skills:**

```javascript
const anna = {
  skills: ['HTML', 'CSS', 'JS'],
  
  [Symbol.iterator]() {
    let index = 0;
    let skills = this.skills;
    
    return {
      next() {
        if (index < skills.length) {
          return { value: skills[index++], done: false };
        } else {
          return { done: true };
        }
      }
    };
  }
};

for (const skill of anna) {
  console.log(skill);
}
```


#### Notes

1. Iterables are everywhere: arrays, strings, sets, maps, NodeLists.
2.  Understanding iterables opens the door to advanced techniques in JavaScript.
3.  You can build your own iterables to control how your data is accessed and used.
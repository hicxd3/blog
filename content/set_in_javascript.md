+++
date = '2024-11-23T18:53:24+03:00'
title = 'Set in JavaScript'
categories = [ "javascript" ]
+++

A Set object is a unique type of collection that represents a "set" of values in which each value is stored only once and has no keys.

Basic Set Methods

- `new Set(iterable)` — creates a Set, and if an iterable object was provided as an argument, usually an [array], then copies its values to the new Set.
- `set.add(value)` — Adds a value to the set (if it is already present, no changes occur) and returns the Set object itself.
- `set.delete(value)` — Removes a value from the set and returns `true` if the specified value was present in the set at the time of the call, otherwise it returns `false'.
- `set.has(value)` — Returns `true` if the specified value is in the set; otherwise— `false'.
- `set.clear()` — deletes all available values.
- `set.size` — returns the number of elements in the set.

The main feature is that with multiple calls to `set.add()` with the same value, nothing changes, so each value is stored in a single instance.

For example, we are waiting for guests and want to make a list of everyone who should come to us, but the list should not include entries about repeat visits. Set will help us here.

```js
let set = new Set();
let john = { name: "John" };
let mia = { name: "Mariah" };
let ann = { name: "Ann" };
// counting the guests, some come several times
set.add(john);
set.add(ann);
set.add(mia);
set.add(john);
set.add(mia);
// set stores only 3 unique values
alert(set.size); // 3
for (let user of set) {
alert(user.name ); // John (then Ann and Mariah)
}
```

### Iterating through the Set object

The contents of the set object can be iterated over using the `for' loop..of`, and through the `forEach` method:

```js
let set = new Set(["orange", "apple", "banana"]);
for (let value of set) alert(value);
// same with forEach:
set.forEach((value, valueAgain, set) => {
alert(value);
});
```

Interesting fact: the function passed to the `forEach` for the Set object takes three arguments: the value of `value', again the same value of `valueAgain', and only then the object itself. The value actually appears twice in the argument list.

This is done for compatibility with the Map object, where the callback for `forEach` also takes three arguments. Although it may look unusual, this structure makes it easy to switch between using `Map` and `Set'.

The Set object has the same iteration methods as the Map.:

- `set.values()` — returns an iterable object containing the values of the set;
- `set.keys()` — works the same way as `set.values()`, added for compatibility with Map;
- `set.entries()` — returns a traversable object containing pairs of the form `[value, value]`, also for compatibility with Map.
+++
date = '2024-11-23T18:53:24+03:00'
title = 'Map in JavaScript'
categories = [ "javascript" ]
+++


To work with complex data structures like arrays and objects, it is common to use `Map` and `Set`.

`Map` is a collection designed to store data of any type in the form of key-value pairs.

Each value is stored with a unique key, which is then used to access that value. Keys themselves can also be of any type.

### Map Methods and Properties

- `new Map()` › creates a collection
- `map.set(key, value)` › stores the value with the key
- `map.get(key)` › returns the value by the key or `undefined` if the key is not present
- `map.has(key)` › returns `true` if the key exists, otherwise `false`
- `map.delete(key)` › removes an element (key-value pair) by key
- `map.clear()` › clears the collection of all elements
- `map.size` › returns the current number of elements

### Example Usage

```js
let map = new Map();
map.set("1", "string1");    
// string as a key
map.set(1, "number1");      
// number as a key
map.set(true, "boolean1");  
// boolean as a key

// Unlike Object, Map preserves the type of keys
console.log(map.get(1));    
// "number1"
console.log(map.get("1"));  
// "string1"
console.log(map.size);      
// 3
```

As we can see, unlike objects, keys in `Map` are not converted to strings. This allows any data type to be used as a key.

> Using `map[key]` is not the correct way to work with Map. While `map[key]` might work (e.g., setting `map[key] = 2`), it treats `map` as a plain object, which brings all associated limitations (keys become strings, etc.).

Therefore, for working with `Map`, special methods like `set`, `get`, and others should be used.

### Using Objects as Keys in Map

```js
let john = { name: "John" };
// store visit count for each user
let visitsCountMap = new Map();
visitsCountMap.set(john, 123);
console.log(visitsCountMap.get(john)); 
// 123
```

Using objects as keys is one of the most notable and powerful features of `Map`. This is not possible with regular objects. In objects, keys can only be strings or symbols.

#### Example of object used as key in plain object:

```js
let john = { name: "John" };
let ben = { name: "Ben" };
let visitsCountObj = {};
visitsCountObj[ben] = 234;
visitsCountObj[john] = 123;

console.log(visitsCountObj["[object Object]"]); 
// 123
```

Because `visitsCountObj` is a regular object, it converts all object-type keys like `john` and `ben` to the same string `"[object Object]"`. Obviously, that’s not what we want.
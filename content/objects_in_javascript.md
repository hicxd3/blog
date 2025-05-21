
+++
date = '2024-11-17T18:53:24+03:00'
title = 'Objects in JavaScript'
categories = [ "javascript" ]
+++

Objects are used to store collections of various values and more complex entities. In JavaScript, objects play an important role and are one of the key parts of the language.

An object can be created using curly braces {…}, and the list of properties is optional.

A property of an object is a key-value pair where the key is a string (or "property name") and the value can be any data type.

An empty object can be created using one of the following syntax options:

```js
// "object constructor" syntax
let user = new Object();
// "object literal" syntax
let user = {};
```

Most often, the object literal `{...}` is used.

This kind of declaration is called an "object literal" or "literal notation."

### Literals and their properties

Using the literal syntax `{...}` you can immediately add multiple properties to an object in the "key: value" format:

```js
let user = {     // object
  name: "John",  // the key "name" holds the value "John"
  age: 30        // the key "age" holds the value 30
};
```

Each property in the object has a key.

Keys are also called 'names' or 'identifiers'.

A colon ':' follows the property name, and the value is specified after it.

If the object contains multiple properties, they are separated by commas.

The object 'user' currently contains two properties:

- A property named 'name' with the value 'John'.
- A property named 'age' with the value '30'.

To access object properties, use dot notation:

```js
// access object properties:
console.log(user.name); // John
console.log(user.age);  // 30
```

A property's value can be of any type. Let's add a boolean property:

```js
user.isAdmin = true;
```

To delete a property, use the 'delete' operator:

```js
delete user.age;
```

The property name can contain multiple words, but in that case, it must be enclosed in quotes:

```js
let user = {
  name: "John",
  age: 30,
  // property name with multiple words must be in quotes
  "likes music": true
};
```

The last property in an object can end with a comma.

This is called a trailing comma.

Using a trailing comma simplifies adding, removing, and rearranging properties, as all lines in the object become identical:

```js
let user = {
  name: "John",
  age: 30,  // trailing comma
}
```
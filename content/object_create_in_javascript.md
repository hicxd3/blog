+++
date = '2025-02-15T12:53:24+03:00'
title = 'The Object.create Method in JavaScript'
categories = [ "javascript" ]
+++

The `Object.create()` method in JavaScript is used to create a new object with a specified prototype. This is one of the ways to implement prototypal inheritance.

```js
let girl = {
  sayHello: function greet() {
    console.log("Hello");
  }
};

let elle = Object.create(girl);
elle.sayHello();
```

Now `elle` inherits the `sayHello` method from the `girl` object
and can say Hello.

`Object.create()` allows you to explicitly specify the prototype for a new object, which is useful for implementing inheritance.

If you pass `null` as the prototype, the object will not inherit any properties or methods, not even basic ones like `toString`.

The `Object.create()` method is often used in functional and prototypal programming styles.
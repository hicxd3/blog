+++
date = '2025-02-16T12:55:24+03:00'
title = 'Dynamic Typing in JavaScript'
categories = [ "javascript" ]
+++

Today, let's talk about dynamic typing in JavaScript.

Dynamic typing is the ability of one data type to transform into another. For example, a string can become a number, a number can become a string, an object can also become a string, and so on.

It's also worth knowing that other programming languages use static typing, where a number always remains a number.

### toString

Let’s look at an example of converting a value into a string using `String`.

We'll use the old operator `String`, which is rarely used in modern development:

```js
console.log(typeof(String(null)));
// Returns: string
```

This operator simply wraps the value in quotes, which converts it to a string data type.

You can also use this with a number:

```js
console.log(typeof(String(4)));
// Returns: string
```

The number 4 has now become a string.

### Concatenation

Concatenation is the process of adding strings to something else. You can add strings to strings, strings to numbers, numbers to numbers, etc.

Example:

```js
console.log(typeof(5 + "hello"));
// Returns: string
```

Keep in mind that whenever you add something to a string, the result will always be a string.

In JavaScript, concatenation is also useful for forming CSS styles.

Let’s see how this works.

Assume we receive a dynamic value of `26` that we want to use as a font size.

Keep in mind that all CSS properties require a unit of measurement. So our code would look like:

```js
let fontSize = 26 + "px";
```

Since all CSS data is stored as strings, concatenation helps us form valid string values.

### toNumber

Now let’s see how to convert to a number.

Just like we did with strings, numbers also have a constructor called `Number`:

```js
console.log(typeof(Number("4")));
// Returns: number
```

There’s also a shorter way to do this, called the "unary plus".

Simply put, placing a `+` in front of a value automatically converts it to a number:

```js
console.log(typeof(+'5'));
// Returns: number
```

Another method is `parseInt`, which accepts two arguments: the value to convert, and the base (use 10 for decimal):

```js
console.log(parseInt("15px", 10))
```

This method is not used very often in real-world projects.

<p class="gray">
Remember, any data received from users via a website is always a string.
</p>

### to Boolean

Let’s go over all the values that evaluate to `false`:

The first is `0`.

Next is an empty string, which also returns `false`.

<p class="gray">
A string with a space is not the same as an empty string.
</p>

Next come `null`, `undefined`, and `NaN`.

Everything else in JavaScript evaluates to `true`.

A small example with a boolean value:

```js 
let switcher = null;

if(switcher) {
    console.log("Working...");
}
// Won’t work — switcher is falsy
```

If we assign `1` to switcher, then:

```js 
let switcher = 1;

if(switcher) {
    console.log("Working...");
}
```

The condition will work because the value is now `true`.

### Boolean

Just like with other data types, booleans have their own constructor — `Boolean`.

```js 
console.log(Boolean("4"));
// Returns: true
```

There’s also a rare trick where you can place two exclamation marks in front of a value: `!!`.

Example:

```js 
console.log(!!"4")
// Returns: true
```

These are the basics of dynamic typing in JavaScript.

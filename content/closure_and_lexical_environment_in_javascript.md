+++
date = '2025-03-11T12:53:24+03:00'
title = 'Closure and lexical environment in JavaScript'
categories = [ "javascript" ]
+++

Today we will analyze the use of closures
in JavaScript.

Let's take a small piece of code that
has already been found in this course.

```js
let number = 5;
function logNumber() {
    console.log(number);
}
number = 6;
logNumber();
```

It must be remembered that JavaScript will execute this code
using an interpreter sequentially, line
by line. 

On the line `let number = 5`, the data type will initially
be `undefined`, we put the value `5` there

Next, the interpreter stumbles upon the creation of a function.

The 'logNumber` variable is written using the `functon declaration`
and therefore it already exists in the context even before 
the interpreter will reach it when it goes through the code line by line.
And we can call this function before declaring it. 
That's what we did.

Note that `logNumber` goes without arguments, which
means that the function will need to get a `number` from somewhere. 

That's what we're going to find out now. 

Next, the variable value is being overwritten in our code. 
`number` - we change the value of `5` to `6` 

And at the very bottom, the function itself is being launched. 
When it is played, the function accesses some
value of `number` and returns the value to us. Let
's find out more about this.

As expected, when running the code in the console, we get 
the number `6` is the actual value of the variable `number`

Since inside the function, first there is an appeal to 
for the variable `number` by reference, then our function 
first, it checks the first value, which is 5,
and then checks for further changes, and throws
the current value into the console.

Let's try to figure out why this is happening. 
not only at the level of logic, but also at the level
of the internals of the JavaScript language in general.

Here it is necessary to analyze such a concept as "Lexical Environment"

### Lexical Environment

In JavaScript, each executed function has a block of code
there is a hidden object called the "lexical environment"

<p class="gray">
It is an internal, technical and hidden object.
</p>

The lexical environment is divided into 2 parts,
internal and external.

In order to see what happens to the code in our example,
let's use a debugger and a breakpoint.

```js
let number = 5; debagger
function logNumber() {
    console.log(number);
}
number = 6;
logNumber(); debagger
```

Let's make some minor changes to our example and add a line
to the internal scope of the function,
with a new variable value.

```js
let number = 5; debagger
function logNumber() {
    let number = 4; debagger
    console.log(number);
}
number = 6;
logNumber(); debagger
```

The value of the local variable is displayed in the console
, which is `4`

A closure in a function, in simple terms,
is when a function searches for something locally, and if it does not
find it, then the global code is accessed.
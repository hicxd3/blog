+++
date = '2024-03-25T18:53:24+03:00'
title = 'if / else in JavaScript'
categories = [ "javascript" ]
+++

Conditional statements allow you to change the behavior of a program depending on certain conditions. Thanks to them, we can build complex programs that behave differently under various scenarios.

The `if` statement is a control structure in programming that manages the sequence of operations. It contains a predicate expression inside parentheses, followed by a block of code within curly braces. This block executes only if the predicate returns `true`.

If the predicate returns `false`, the program skips the block and continues execution. In this example, the next line `return 'general';` will execute, causing the function to return a string and terminate. Note that the `return` statement can be used anywhere in a function, including inside an `if` block.

If the `if` block only contains one line of code, curly braces can be omitted, for example:

```js
const getTypeOfSentence = (sentence) => {
  const lastChar = sentence[sentence.length - 1];
  if (lastChar === '?')
    return 'question';
  return 'general';
}; 
console.log(getTypeOfSentence('Hodor'));  // => general
console.log(getTypeOfSentence('Hodor?')); // => question
```

It’s recommended to always use curly braces, even for one-line statements. This makes the structure of your code more visible and easier to understand.

### else

Let’s create a `getTypeOfSentence()` function that analyzes the tone of a sentence: for declarative sentences – it returns *General sentence*, for questions – *Question sentence*.

```js
getTypeOfSentence('Hodor');  // General sentence
getTypeOfSentence('Hodor?'); // Question sentence
```

Here’s the function:

```js
const getTypeOfSentence = (sentence) => {
  // Declare a variable to hold the sentence type
  let sentenceType;

  // Predicate to check the sentence ending
  // If it ends with '?', it returns true
  if (sentence.endsWith('?')) {
    sentenceType = 'Question';
  } else {
    // Otherwise it's a general sentence
    sentenceType = 'General';
  }

  // Return the sentence type using interpolation
  return `${sentenceType} sentence`;
};
```

We added the `else` keyword with a new block. This block only executes if the `if` condition returns false.

### else if

The previous `getTypeOfSentence()` function only detects question and general sentences. Let’s expand it to also detect exclamatory sentences.

```js
const getTypeOfSentence = (sentence) => {
  const lastChar = sentence[sentence.length - 1];
  let sentenceType; 
  if (lastChar === '!') {
    sentenceType = 'exclamation';
  } else {
    sentenceType = 'normal';
  }
  if (lastChar === '?') {
    sentenceType = 'question';
  }
  return `Sentence is ${sentenceType}`;
};

getTypeOfSentence('Who?'); // Sentence is question
getTypeOfSentence('No');   // Sentence is normal
getTypeOfSentence('No!');  // Sentence is exclamation
```

We added a check for "exclamation" (`!`). Technically the function works, but semantically there are issues:

1) The question mark is checked regardless of whether an exclamation has already been detected.  
2) The second condition is not part of the else branch.

It’s better to use `else if` for cleaner logic:

```js
const getTypeOfSentence = (sentence) => {
  const lastChar = sentence[sentence.length - 1];
  let sentenceType;
  if (lastChar === '?') {
    sentenceType = 'question';
  } else if (lastChar === '!') {
    sentenceType = 'exclamation';
  } else {
    sentenceType = 'normal';
  }
  return `Sentence is ${sentenceType}`;
};

getTypeOfSentence('Who?'); // Sentence is question
getTypeOfSentence('No');   // Sentence is normal
getTypeOfSentence('No!');  // Sentence is exclamation
```

Now all conditions are merged into a single `if` block. The `else if` clause means: "if the previous condition wasn’t met, but this one is – then do this."

The execution logic will only trigger one of the branches inside the `if` statement.
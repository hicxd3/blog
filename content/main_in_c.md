+++
date = '2025-01-06T19:53:24+03:00'
title = 'The main() Function in C'
categories = [ "c" ]
+++

The most important part of a program written in C is the `main()` function.

In C, there are two types of functions:

>Built-in functions  
>Custom (user-defined) functions

Every C program must include the `main()` function.

The difference between a command and a function is the presence of parentheses, for example:

```js
main();
calcIt();
printf();
strlen();
```

Commands come without parentheses:

```md
return
while
int
iffloat
```

If a function name consists of multiple words, it should follow the camelCase format.

For example:

```js
doReportPrint();
calcIt();
```

The `main()` function name, as well as most built-in C function names, should only contain lowercase letters.

Even if the `main()` function is not listed first in your program, it still defines the entry point of program execution.

After the keyword `main()`, an opening curly brace `{` always follows.

The closing curly brace marks the end of the `main()` function block.

The expression `#include <stdio.h>` should be included in almost every C program, as it helps with outputting to the screen and receiving input.

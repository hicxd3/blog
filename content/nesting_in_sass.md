+++
date = '2025-02-18T18:53:24+03:00'
title = 'Nesting in the SASS preprocessor'
categories = [ "css"]
+++

The SASS preprocessor allows you to embed 
CSS rules are integrated into each other.

The rule nested in the element above applies
only to its selectors.

For example:

```css
#main p
    color: #F0F0F0;
    width: 100%;
    .graybox: 
        background-color: #A9A9A9;
```

As a result, we get in the CSS file:

```css
#main p {
    color: #F0F0F0;
    width: 100%;
}

#main p .graybox {
    background-color: #A9A9A9;
}
```

Using a preprocessor in a project
helps to avoid repetition of writing 
parent selectors. This makes it much
easier to write layouts with a large
amount of nested CSS selectors.

Another example:

```css
#main 
    width: 100%;

    p, div 
        font-size: 2rem;

        a 
            font-weight: bold;
    pre
        font-size: 3rem;
```

After processing, we get the CSS code:

```css
#main {
    width: 100%;
}
#main p, #main div {
    font-size: 2rem;
}
#main p a, #main div a {
    font-weight: bold;
}
#main pre {
    font-size: 3rem;
}
```

It's worth getting used to the syntax
of the preprocessor because it
saves writing CSS rules a lot.
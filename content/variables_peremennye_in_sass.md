
+++
date = '2024-10-29T18:53:24+03:00'
title = 'Variables in Sass'
categories = [ "sass" ]
+++

In Sass, variables are declared using the `$` symbol followed by the variable name and a value. This makes it easier to manage repeated values like colors, spacing, font sizes, etc.

For example:

```scss
$main-color: #3498db;
$padding: 10px;

.button {
  background-color: $main-color;
  padding: $padding;
}
```

### Why use variables?

- **Consistency:** You can reuse values throughout your styles.
- **Maintainability:** Updating a value in one place updates it everywhere.
- **Clarity:** Names of variables make the code easier to understand.

### Naming rules

- A variable name must start with `$`.
- Names can include letters, numbers, hyphens, and underscores.
- Avoid overly generic names — use descriptive ones.

```scss
$bg-color: #f1f1f1;
$font-stack: 'Helvetica, sans-serif';
```

### Changing variable values

You can overwrite a variable by redefining it. However, if the variable was defined inside a `:root` block or outside a specific scope, make sure you understand how scope affects its visibility.

```scss
$color: red;

.button {
  $color: blue;
  color: $color; // will be blue inside this block
}

.text {
  color: $color; // will be red
}
```

### Default values with `!default`

If you're writing a theme or library, you can allow users to override your variable values using `!default`.

```scss
$primary-color: blue !default;
```

If `$primary-color` is already set before this line, Sass will not overwrite it.


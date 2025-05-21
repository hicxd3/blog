+++
date = '2025-02-20T18:53:24+03:00'
title = 'Code Fragmentation in SASS Preprocessor'
categories = [ "css" ]
+++

Fragmentation in SASS means splitting the code into multiple files that can be reused in other parts of the codebase.

These files are also called `partials`.

The content from these files can easily be reused via imports.

In practice, this helps simplify code maintenance, reduce duplication, and make styles more modular.

To create a partial file, prefix its name with an underscore `_`, for example:
`_menu`, `_header`, or `_buttons`.

This naming tells the `SASS` compiler that the file is meant to be imported.

To import the code into the main file, such as `app.sass`, use the `@import` directive:

```css
/* app.sass */
@import '_menu';
@import '_header';
@import '_buttons';
```

> 💡 When importing files, the extension is not required.

During rendering, the compiler will merge all files into one. Example of project structure:

```md
styles/
├── _menu.scss
├── _buttons.scss
├── _header.scss
└── main.scss
```

In modern workflows, it's recommended to use `@use` instead of `@import`.  
This directive was introduced in `Dart Sass` to eliminate issues caused by `@import`.

```css
/* main.scss */
@use 'menu';
@use 'buttons';
@use 'header';
```
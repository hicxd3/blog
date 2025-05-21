
+++
date = '2025-03-01T12:53:24+03:00'
title = 'Mixins in SCSS/SASS Preprocessors'
categories = [ "css" ]
+++

Mixins are functions in Sass that allow you to create blocks of styles that can be reused throughout the project. They help avoid repetitive code and make CSS more flexible and convenient to work with. Mixins can take parameters, allowing them to be adapted to various needs.

To create a mixin in Sass, use the `@mixin` directive followed by the mixin's name and its contents.

```scss
@mixin button-style {
  padding: 10px 20px;
  background-color: #3498db;
  color: white;
  border-radius: 5px;
  border: none;
}

.button {
  @include button-style;
}
```

In this example, we create a `button-style` mixin that defines common button styles. Then, using the `@include` directive, we apply the mixin to the `.button` class.

Mixins can take parameters, making them even more flexible. Parameters are specified in parentheses and can be used within the mixin to change styles based on the provided values.

Example of a mixin with parameters:

```scss
@mixin button-style($bg-color, $font-size) {
  padding: 10px 20px;
  background-color: $bg-color;
  color: white;
  font-size: $font-size;
  border-radius: 5px;
  border: none;
}

.button {
  @include button-style(#3498db, 16px);
}

.secondary-button {
  @include button-style(#2ecc71, 14px);
}
```

Here, the mixin takes two parameters: `$bg-color` and `$font-size`. We can pass different values when using the mixin, allowing easy customization without duplicating code.

You can also set default values for parameters. This is useful when you want a parameter to be optional but still have a standard value.

Example of a mixin with default values:

```scss
@mixin button-style($bg-color: #3498db, $font-size: 16px) {
  padding: 10px 20px;
  background-color: $bg-color;
  color: white;
  font-size: $font-size;
  border-radius: 5px;
  border: none;
}

.button {
  @include button-style(); 
  // uses default values
}

.secondary-button {
  @include button-style(#2ecc71); 
  // only background color is changed
}
```

Here, if no parameters are passed, the default values are used. In the case of `.secondary-button`, only one parameter is provided, and the second remains default.

Mixins are often used to handle media queries. This allows centralizing media queries and making the code cleaner.

```scss
@mixin media-query($breakpoint) {
  @if $breakpoint == 'small' {
    @media (max-width: 600px) {
      @content;
    }
  }
  @else if $breakpoint == 'medium' {
    @media (max-width: 900px) {
      @content;
    }
  }
}

.container {
  @include media-query('small') {
    background-color: red;
  }
  @include media-query('medium') {
    background-color: blue;
  }
}
```

In this example, we create a `media-query` mixin that takes the `$breakpoint` parameter and changes styles depending on the screen size. With the `@content` directive, we insert the code inside the media query.

Mixins in Sass are used to simplify CSS work. They help avoid code duplication, improve structure, and make your project more flexible.

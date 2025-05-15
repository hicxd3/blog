+++
date = '2024-10-03T18:53:24+03:00'
title = 'CSS Selectors'
categories = [ "css" ]
+++

CSS is a language that is used to design HTML documents. Its syntax is much simpler than that of HTML, since CSS lacks complex rules related to the nesting of elements. In fact, CSS is a rather "flat" language where nesting is hardly used. A typical CSS file consists of a sequence of CSS rules. Each CSS rule includes a selector and a list of properties with corresponding values. Here is an example of a simple CSS rule:

```js
selector {
  property: the value of the property;
  property: the value of the property; 
  // these are CSS rules
  property: the value of the property;    
}
/*== And this is a comment ==*/
```

### Selectors

The first part of the CSS rule is the selector. It specifies which HTML tag or tag group this set of properties will be applied to.
 
There are many types of selectors, but the most common are:

Tag selector: Applies styles to all elements of a certain type, for example, p, h1, div
 
Class Selector: Applies styles to elements with a specific class, for example, .main\_\_page

Combined selectors: Also known as nested or contextual selectors, they allow you to apply styles to elements located inside other elements, such as div p
 
```js
p {...} 
/* Accessing the tag */
.main__title {...} 
/* Accessing the class */
p.nav__menu {...} 
/* Accessing the class inside the tag */
#nav__bar {...} 
/* Accessing the id */
h1#main__title {...} 
/* Accessing the tag with the id */
.header a {...} 
/* Accessing the tag, inside the tag with the class */
.header.nav__menu {...} 
/* Accessing the class, inside the class tag */
```

### Tag Name Selector

This type of selectors is the most basic. It is created by specifying the tag name without the angle brackets < and >. This selector selects all the elements with the corresponding tag name. For example, the selector 'p' will select all elements named 'p', i.e. all paragraphs.
 
For example

```js
p { // Accessing all p tags   
  color: #ff0000     
}
```

### Class Selector

This type of selector starts with a dot followed by the class name. It selects all the elements whose class attribute value matches the specified class name. 
 
```js
.main {  // Addressing the class 
  color: #ff0000  
}
```

You can combine selectors by tag and by class as follows: `tag.class `. It is important to note that there should be no space between the tag and the class. This combined selector will select only those elements that match the specified tag and have the specified class.
 
```js
p.main__title { // Accessing the p tag with the main__title class       
  color: #ff00000 
}
```

### ID Selector


This type of selector functions similarly to a class selector, but it starts with the grid symbol # followed by the identifier name. It selects all the elements for which the value of the id attribute corresponds to the specified identifier name.
 

```js
#nav-list { // Request by id      
  color: #ff0000
}
```

The op id selector can also be combined with the selector for the tag

```js
h1#main-title { // Accessing the h1 tag with the main-title id    
  color: #ff0000
}
```
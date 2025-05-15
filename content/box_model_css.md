+++
date = '2024-11-11T18:53:24+03:00'
title = 'Box Model in CSS'
categories = [ "css" ]
+++

Each element on a web page corresponds to a rectangular area known as a box.

The box includes:

1. 1 Content — the actual content of the element;
2. 2 Padding — the space between the content and the border;
3. 3 Border — the line surrounding the content and padding;
4. 4 Margin — the space outside the border, separating the element from others.

![Box Model in CSS](../images/box-model.png)

The appearance of a box on the page is largely determined by its type or the type of its parent element.

Block-level boxes start on a new line and take up the full width of their parent element. Tags like `p`, `div`, and `h1` are block-level elements by default.

Inline boxes are placed next to each other in a single line, and their width depends on the content. By default, `a`, `span`, and `b` are inline elements.

### Flow, Grids, and Page Layout

The interaction between boxes and their positioning on a page is determined by the concept of "flow". Flow can be controlled by changing the box types and their default properties.

A grid represents a structure that defines the placement of major blocks on a webpage. These typically include the header, footer, main content, sidebar, and various sections. The number of elements in a grid is usually fixed, and their sizes are defined according to the layout.

A layout is a graphical representation of a web page created by a designer. It serves as a blueprint for the developer when building the page.

Layouts are usually made in Figma or Photoshop.
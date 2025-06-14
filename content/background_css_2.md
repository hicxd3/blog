+++
date = '2024-09-30T18:53:24+03:00'
title = 'Background in CSS 2'
categories = [ "css" ]
+++

## Image Formats

### JPEG Format
The JPEG format works great for photos and paintings but is not well suited for diagrams, blueprints, text, and graphics.

When saving an image as JPEG, you can adjust the quality level. If the quality is set too low, artifacts may appear.

JPEG does not support transparency, so the image will always be rectangular. To simulate transparency, you can set the image background in your graphics editor to match the container where it will be placed.

Use JPEG for displaying photos with a good balance between file size and image quality.

### PNG Format
The PNG format includes two subtypes: PNG-8 and PNG-24, which are also available as save modes in Photoshop.

PNG-8 is similar to the GIF format. It's perfect for diagrams, blueprints, graphs, text, and images with a limited color palette. It supports up to 256 colors and transparency.

PNG-24 is suitable for diagrams, blueprints, graphs, text, and complex multicolor images, supporting almost unlimited colors. It's usually larger than JPEG in file size but superior in image quality. A key feature of PNG-24 is full support for semi-transparency, which is not available in other formats.

### GIF Format
The primary reason to use GIF is its support for animated images. In other cases, JPEG or PNG is usually preferred.

### Multiple Backgrounds
The most reliable way to create multiple backgrounds is by nesting elements and giving them the same size, then assigning each one a different background. Each element acts as a separate background layer.

Nested element backgrounds stack on top of each other—the deeper the element, the higher its background layer.

For convenience, it's recommended to set the width on the outermost element (since all nested elements will inherit that width) and set the height on the innermost element, which stretches its parent elements.

### Repeating Background Effects
Backgrounds with the values `repeat`, `repeat-x`, or `repeat-y` are often used to create decorative effects and are called repeating backgrounds.

The key is to choose an image with a suitable repetition pattern. A very small image can help reduce page weight significantly.

### Sprites
A sprite is one large image that contains many smaller images inside it.

Sprites are used to reduce the number of server requests. Small images are combined into one large image. Parts of the sprite are displayed in elements with small dimensions by using background position to show only the required part.

Icons and various decorative UI elements are commonly grouped into sprites.
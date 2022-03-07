The display property specifies the display behavior of the element. We have set it to inline-block, so that the link behaves as an inline block container.
We have also set the colors and font size, as well as the border-radius, resulting in rounded corners.

In order to position the feature divs next to each other horizontally, we will use display: inline-block to make them inline-level block containers and provide a width:

Because we have 3 features, we gave each feature div 32% of the width of their container.
The remaining space will be left for the space between the elements.
We also set the width of the images to be 40% of their containers.
By using only % values for the widths, the features will always remain next to each other and be positioned horizontally, irrespective of the browser width.

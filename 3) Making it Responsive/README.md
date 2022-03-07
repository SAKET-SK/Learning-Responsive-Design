Viewport


Before we start making our landing page responsive, we need to cover a few concepts.
The first concept is the viewport: the visible area of a web page.
Usually, a web page with a fixed width becomes too large to fit the viewport on a small screen, such as a mobile device or tablet. To fix this, browsers on those devices scaled down the entire web page to fit the screen.
You can control the viewport of your web pages.

You can control your viewport in HTML5 using a meta tag:
```
<meta name="viewport" content="width=device-width, initial-scale=1.0">  
```

width=device-width sets the width of the page to follow the screen-width of the device.
initial-scale=1.0 sets the initial zoom level when the page is first loaded by the browser.

You can also use custom values for the viewport tag, however in most cases it is recommended you use the defaults by applying the device-width value.

Media Queries


Media queries provide the ability to specify different CSS styles for different widths of the viewport, or other specifications.
This makes it possible for a web page to define different layout styles for different screen sizes and make the page responsive!

You define a media query using the @media rule inside of your existing style sheet:

```
@media screen and (max-width: 600px) {
   body {
     background-color: blue;
  }
}
```
The @media rule is followed by the media type we are targeting (the screen in our case) and sets the condition when the rules apply (max-width:600px in our case).
So now, the style will apply if the page has a width up to 600px.

You can also define multiple conditions, for example a max and min width of the viewport:
```
@media screen and (min-width: 800px) and (max-width: 1024px) {
   body {
     background-color: blue;
  }
} 
```
Now the style will apply for screen sizes from 800 to 1024px.

You can also define multiple media queries for a single web page.
Media queries allow you to define breakpoints when the page layout and style should change, as well as define the corresponding CSS styles for these breakpoints.

Responsive Header
Now, that we know how to define CSS styles for different screen sizes, we can start making our landing page responsive!

A typical breakpoint for a mobile screen is 480px width.
We will create separate styles for our sections when the screen size is lower than 480px in width.
480px is the typical breakpoint for mobile devices.

As you can see, we changed some font-size properties, changed the paddings of the section container, and changed the button's display property to block, making it a block level element which takes the whole width of its container.

Note, that we do not need to redefine the whole style for the elements in the media query. We only need to define the style we want to change.

We changed the width of each feature div to 100% and set the display property to flex which makes the div a flexbox container. This allows us to position the child features horizontally and also set the alignment of its child elements -- the icon and the text -- using the align-items and justify-content properties.
We also set the width of the icons and defined some margins.
Now, the features will be aligned next to each other on larger screens and under each other on smaller screens.

Flexbox


The flexbox layout model allows to create flexible layouts easily, without the need to use CSS positioning and floats.

Let's demonstrate how it works using a simple example:
```
<div class="container">
  <div>A</div>
  <div>B</div>
  <div>C</div>
</div> 
```
To use flexbox, we first define a container and set its display property to flex.
```
.container {
  display: flex;
}
```
```
<div class="container">
    <div>A</div>
    <div>B</div>
    <div>C</div>
</div>
```
```
.container {
  display: flex;
  align-items: stretch;
}
.container div {
  background-color: red;
  margin: 10px;
  text-align: center;
  line-height: 75px;
  font-size: 30px; 
  flex: 1;
}
```
This will make all child elements have the same width (flex: 1) and fill the entire container width.

The display:block; style makes the list items block level elements so they take the entire width of their container. This makes the items align under each other

CSS Units


An important part of our layout was not using any fixed units for our widths.
We used percentage values, which made the elements span relative to the width of their parents.
This approach allows elements to be more flexible, which is essential when putting together a responsive design.

CSS also allows you to define relative unit sizes for font-sizes:
The em unit size will be relative to the parent's font-size.
For example, if our page's body has a font size of 16px, using 1.5em will be equal to 24px (16*1.5)

This is useful because when you have to change the font-size, you need to change it only on the top parent. All child elements will get the corresponding relative size from it using the em units.
However, when you define all sizes using em, you would be hit by a cascading effect. In this situation, you have many nested elements which use font-sizes relative to their corresponding parents, which results in hard-to-control unit sizes.

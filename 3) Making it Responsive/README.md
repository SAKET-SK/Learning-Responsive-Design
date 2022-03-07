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

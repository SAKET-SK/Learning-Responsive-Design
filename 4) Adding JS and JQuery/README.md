A Submenu

Modern websites include interactive elements and animations, which improve the user experience and aesthetics.
Let's add a submenu to our responsive landing page that will open and close when tapping on the Download Now button.
Our submenu will be responsive as well -- it will appear over elements on desktop, and will push down the elements when on mobile.

We used a CSS hack in order to position our submenu in the center of the screen. The combination of absolute positioning, using the left and transform property, results in our submenu being positioned in the center of the screen and opened over the page elements.
We also used display: block; for our links, to make them behave as block-level elements.

We only need to change the width and the position property of the submenu.
Currently, the submenu is always open. We will add the open/close animation in the next lesson.

Animation

Let's use JavaScript to open/close the submenu when the button is tapped.
Since we want to open the submenu using a nice sliding animation, we will use the JQuery library, which supports simple animations.

We start by including jQuery in our page:
```
<head>
  <title>App Landing Page</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <script src="https://code.jquery.com/jquery-3.6.0.js"></script>
</head> 
```
We used the script tag to import the jQuery library.
jQuery is a fast, small, and feature-rich JavaScript library.
It makes things like HTML document traversal and manipulation, event handling, and animation much simpler.

We need to handle the click event of our button, which should open and close our submenu.

We will use the slideToggle() method, which switches between visible and invisible states of the element selected using a slide animation
we handled the click event of out .btn, selected the .submenu element and opened/closed it using the slideToggle method, providing 500ms for the animation speed.

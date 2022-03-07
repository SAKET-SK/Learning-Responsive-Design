A Submenu

Modern websites include interactive elements and animations, which improve the user experience and aesthetics.
Let's add a submenu to our responsive landing page that will open and close when tapping on the Download Now button.
Our submenu will be responsive as well -- it will appear over elements on desktop, and will push down the elements when on mobile.

We used a CSS hack in order to position our submenu in the center of the screen. The combination of absolute positioning, using the left and transform property, results in our submenu being positioned in the center of the screen and opened over the page elements.
We also used display: block; for our links, to make them behave as block-level elements.

We only need to change the width and the position property of the submenu.
Currently, the submenu is always open. We will add the open/close animation in the next lesson.

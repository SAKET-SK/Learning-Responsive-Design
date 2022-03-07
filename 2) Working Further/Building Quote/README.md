We used the blockquote tag as the container and reused our container class on it.
Inside the blockquote, we have a paragraph of text representing the quote, and a cite tag, containing the name of the customer.
The blockquote element specifies a section that is quoted, while cite is used to define a title.

First, we need to reset the padding/margin of the blockquote element since the browsers have some default values for them.
We also define the font sizes and margins for the elements.

Last but not least, we use the :before selector to set a dash before the cite element.
We could have added the dash in the text of the cite tag, but this is a fancier way of doing the same thing.

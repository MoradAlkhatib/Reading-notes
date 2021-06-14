# CSS layout
At this point we've already looked at CSS fundamentals, how to style text,
and how to style and manipulate the boxes that your content sits inside. 
Now it's time to look at how to place your boxes in the right place in relation to the viewport, and one another.
We have covered the necessary prerequisites so we can now dive deep into CSS layout,
looking at different display settings, modern layout tools like flexbox, CSS grid,
and positioning, and some of the legacy techniques you might still want to know about.

## Prerequisites
Before starting this module, you should already:

1.Have basic familiarity with HTML, as discussed in the Introduction to HTML module.
2.Be comfortable with CSS fundamentals, as discussed in Introduction to CSS.
3.Understand how to style boxes.

## Guides
These articles will provide instruction on the fundamental layout tools and techniques available in CSS.
At the end of the lessons is an assessment to help you check your understanding of layout methods, by laying out a webpage.

## The display property
The main methods of achieving page layout in CSS are all values of the display property. This property allows us to change the default way something displays. Everything in normal flow has a value of display, used as the default way that elements they are set on behave. For example, the fact that paragraphs in English display one below the other is due to the fact that they are styled with display: block. If you create a link around some text inside a paragraph, that link remains inline with the rest of the text, and doesn’t break onto a new line. This is because the <a> element is display: inline by default.

You can change this default display behavior. For example, the <li> element is display: block by default, meaning that list items display one below the other in our English document. If we change the display value to inline they now display next to each other, as words would do in a sentence. The fact that you can change the value of display for any element means that you can pick HTML elements for their semantic meaning, without being concerned about how they will look. The way they look is something that you can change.

In addition to being able to change the default presentation by turning an item from block to inline and vice versa, there are some bigger layout methods that start out as a value of display. However, when using these, you will generally need to invoke additional properties. The two values most important for our purposes when discussing layout are display: flex and display: grid.

## Flexbox
Flexbox is the short name for the Flexible Box Layout Module, designed to make it easy for us to lay things out in one dimension — either as a row or as a column. To use flexbox, you apply display: flex to the parent element of the elements you want to lay out; all its direct children then become flex items. We can see this in a simple example.

The HTML markup below gives us a containing element, with a class of wrapper, inside which are three <div> elements. By default these would display as block elements, below one another, in our English language document.

However, if we add display: flex to the parent, the three items now arrange themselves into columns. This is due to them becoming flex items and being affected by some initial values that flexbox sets on the flex container. They are displayed in a row, because the initial value of flex-direction set on their parent is row. They all appear to stretch to the height of the tallest item, because the initial value of the align-items property set on their parent is stretch. This means that the items stretch to the height of the flex container, which in this case is defined by the tallest item. The items all line up at the start of the container, leaving any extra space at the end of the row.

## Grid Layout
While flexbox is designed for one-dimensional layout, Grid Layout is designed for two dimensions — lining things up in rows and columns.

Once again, you can switch on Grid Layout with a specific value of display — display: grid. The below example uses similar markup to the flex example, with a container and some child elements. In addition to using display: grid, we are also defining some row and column tracks on the parent using the grid-template-rows and grid-template-columns properties respectively. We've defined three columns each of 1fr and two rows of 100px. I don’t need to put any rules on the child elements; they are automatically placed into the cells our grid has created.

## Floats
Floating an element changes the behavior of that element and the block level elements that follow it in normal flow. The element is moved to the left or right and removed from normal flow, and the surrounding content floats around the floated item.

The float property has four possible values:

- left — Floats the element to the left.
- right — Floats the element to the right.
- none — Specifies no floating at all. This is the default value.
- inherit — Specifies that the value of the float property should be inherited from the element's parent element.
  
## Positioning techniques
Positioning allows you to move an element from where it would be placed when in normal flow to another location. Positioning isn’t a method for creating your main page layouts, it is more about managing and fine-tuning the position of specific items on the page.

There are however useful techniques for certain layout patterns that rely on the position property. Understanding positioning also helps in understanding normal flow, and what it is to move an item out of normal flow.

There are five types of positioning you should know about:
  
## Absolute positioning
Absolute positioning is used to completely remove an element from normal flow, and place it using offsets from the edges of a containing block.

Going back to our original non-positioned example, we could add the following CSS rule to implement

Static positioning is the default that every element gets — it just means "put the element into its normal position in the document layout flow — nothing special to see here".
Relative positioning allows you to modify an element's position on the page, moving it relative to its position in normal flow — including making it overlap other elements on the page.
Absolute positioning moves an element completely out of the page's normal layout flow, like it is sitting on its own separate layer. From there, you can fix it in a position relative to the edges of the page's <html> element (or its nearest positioned ancestor element). This is useful for creating complex layout effects such as tabbed boxes where different content panels sit on top of one another and are shown and hidden as desired, or information panels that sit off screen by default, but can be made to slide on screen using a control button.
Fixed positioning is very similar to absolute positioning, except that it fixes an element relative to the browser viewport, not another element. This is useful for creating effects such as a persistent navigation menu that always stays in the same place on the screen as the rest of the content scrolls.
Sticky positioning is a newer positioning method which makes an element act like position: static until it hits a defined offset from the viewport, at which point it acts like position: fixed

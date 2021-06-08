
# HTML Links
Links are found in nearly all web pages. Links allow users to click their way from page to page.
![HTML Links](https://www.wikihow.com/images/thumb/3/37/Create-a-Link-With-Simple-HTML-Programming-Step-2-Version-3.jpg/v4-460px-Create-a-Link-With-Simple-HTML-Programming-Step-2-Version-3.jpg)
HTML Links - Hyperlinks
HTML links are hyperlinks.

You can click on a link and jump to another document.

When you move the mouse over a link, the mouse arrow will turn into a little hand.

HTML Links - Syntax
The HTML <a> tag defines a hyperlink. It has the following syntax:

<a href="url">link text</a>
The most important attribute of the <a> element is the href attribute, which indicates the link's destination.

The link text is the part that will be visible to the reader.

Clicking on the link text, will send the reader to the specified URL address.

HTML Links - The target Attribute
By default, the linked page will be displayed in the current browser window. To change this, you must specify another target for the link.

The target attribute specifies where to open the linked document.

The target attribute can have one of the following values:

_self - Default. Opens the document in the same window/tab as it was clicked
_blank - Opens the document in a new window or tab
_parent - Opens the document in the parent frame
_top - Opens the document in the full body of the window
Absolute URLs vs. Relative URLs
Both examples above are using an absolute URL (a full web address) in the href attribute.

A local link (a link to a page within the same website) is specified with a relative URL (without the "https://www" part):
HTML Links - Use an Image as a Link
To use an image as a link, just put the <img> tag inside the <a> tag:
Link to an Email Address
Use mailto: inside the href attribute to create a link that opens the user's email program (to let them send a new email):

# CSS layout
  ![layout](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTu4oXVAwnBhvziuWzyNXO5weIwjKo__8x4Rg&usqp=CAU)
At this point we've already looked at CSS fundamentals,
how to style text, and how to style and manipulate the boxes that your content sits inside.
Now it's time to look at how to place your boxes in the right place in relation to the viewport, and one another.
We have covered the necessary prerequisites so we can now dive deep into CSS layout, looking at different display settings, modern layout tools like flexbox,
CSS grid, and positioning, and some of the legacy techniques you might still want to know about.
Prerequisites
Before starting this module, you should already:

Have basic familiarity with HTML, as discussed in the Introduction to HTML module.
Be comfortable with CSS fundamentals, as discussed in Introduction to CSS.
Understand how to style boxes.
Guides
These articles will provide instruction on the fundamental layout tools and techniques available in CSS. At the end of the lessons is an assessment to help you check your understanding of layout methods, by laying out a webpage.

## Introduction to CSS layout
This article will recap some of the CSS layout features we've already touched upon in previous modules — such as different display values — and introduce some of the concepts we'll be covering throughout this module.
### Normal flow
Elements on webpages lay themselves out according to normal flow - until we do something to change that. This article explains the basics of normal flow as a grounding for learning how to change it.
### Flexbox
Flexbox is a one-dimensional layout method for laying out items in rows or columns. Items flex to fill additional space and shrink to fit into smaller spaces. This article explains all the fundamentals. After studying this guide you can test your flexbox skills to check your understanding before moving on.
### Grids
CSS Grid Layout is a two-dimensional layout system for the web. It lets you lay content out in rows and columns, and has many features that make building complex layouts straightforward. This article will give you all you need to know to get started with page layout, then test your grid skills before moving on.
### Floats
Originally for floating images inside blocks of text, the float property became one of the most commonly used tools for creating multiple column layouts on webpages. With the advent of Flexbox and Grid it has now returned to its original purpose, as this article explains.
### Positioning
Positioning allows you to take elements out of the normal document layout flow, and make them behave differently, for example sitting on top of one another, or always remaining in the same place inside the browser viewport. This article explains the different position values, and how to use them.
### Multiple-column layout
The multiple-column layout specification gives you a method of laying content out in columns, as you might see in a newspaper. This article explains how to use this feature.
### Responsive design
As more diverse screen sizes have appeared on web-enabled devices, the concept of responsive web design (RWD) has appeared: a set of practices that allows web pages to alter their layout and appearance to suit different screen widths, resolutions, etc. It is an idea that changed the way we design for a multi-device web, and in this article we'll help you understand the main techniques you need to know to master it.
### Beginner's guide to media queries
The CSS Media Query gives you a way to apply CSS only when the browser and device environment matches a rule that you specify, for example "viewport is wider than 480 pixels". Media queries are a key part of responsive web design, as they allow you to create different layouts depending on the size of the viewport, but they can also be used to detect other things about the environment your site is running on, for example whether the user is using a touchscreen rather than a mouse. In this lesson you will first learn about the syntax used in media queries, and then move on to use them in a worked example showing how a simple design might be made responsive.
### Legacy layout methods
Grid systems are a very common feature used in CSS layouts, and before CSS Grid Layout they tended to be implemented using floats or other layout features. You imagine your layout as a set number of columns (e.g. 4, 6, or 12), and then fit your content columns inside these imaginary columns. In this article we'll explore how these older methods work, in order that you understand how they were used if you work on an older project.
### Supporting older browsers
In this module we recommend using Flexbox and Grid as the main layout methods for your designs. However there will be visitors to your site who use older browsers, or browsers which do not support the methods you have used. This will always be the case on the web — as new features are developed, different browsers will prioritise different things. This article explains how to use modern web techniques without locking out users of older technology.

Assessment: Fundamental layout comprehension
An assessment to test your knowledge of different layout methods by laying out a webpage.
### See also
[Practical positioning examples
](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Practical_positioning_examples)
  
 
  
  
  # Functions Js
  
  Functions are one of the fundamental building blocks in JavaScript. A function in JavaScript is similar to a procedure—a set of statements that performs a task or calculates a value, but for a procedure to qualify as a function, it should take some input and return an output where there is some obvious relationship between the input and the output. To use a function, you must define it somewhere in the scope from which you wish to call it.

[See also the exhaustive reference chapter about JavaScript functions to get to know the details](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions)
  
  Defining functions
Function declarations
A function definition (also called a function declaration, or function statement) consists of the function keyword, followed by:

The name of the function.
A list of parameters to the function, enclosed in parentheses and separated by commas.
The JavaScript statements that define the function, enclosed in curly brackets, 
  The function square takes one parameter, called number. The function consists of one statement that says to return the parameter of the function (that is, number) multiplied by itself. The statement return specifies the value returned by the function:
  
  Primitive parameters (such as a number) are passed to functions by value; the value is passed to the function, but if the function changes the value of the parameter, this change is not reflected globally or in the calling function.

If you pass an object (i.e. a non-primitive value, such as Array or a user-defined object) as a parameter and the function changes the object's properties, that change is visible outside the function, as shown in the following example:
  
  Function expressions
While the function declaration above is syntactically a statement, functions can also be created by a [function expression](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/function)
  
  
  
  
  
  
  

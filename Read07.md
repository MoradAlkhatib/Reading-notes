# CSS [Learn More](https://www.w3schools.com/css/)
 #### IS Cascading Style Sheets) allows you to create great-looking web pages, but how does it work under the hood? This article explains what CSS is, with a simple syntax example, and also covers some key terms about the language.

 ## What is CSS for?
##### As we have mentioned before, CSS is a language for specifying how documents are presented to users — how they are styled, laid out, etc.

##### A document is usually a text file structured using a markup language — HTML is the most common markup language, but you may also come across other markup languages such as SVG or XML.

###### Presenting a document to a user means converting it into a form usable by your audience. Browsers, like Firefox, Chrome, or Edge , are designed to present documents visually, for example, on a computer screen, projector or printer.

## CSS syntax
###### CSS is a rule-based language — you define rules specifying groups of styles that should be applied to particular elements or groups of elements on your web page. For example "I want the main heading on my page to be shown as large red text."

###### The following code shows a very simple CSS rule that would achieve the styling described above:

### h1 {
  ### color: red;
  ### font-size: 5em;
### }
###### The rule opens with a selector . This selects the HTML element that we are going to style. In this case we are styling level one headings (<h1>).

###### We then have a set of curly braces { }. Inside those will be one or more declarations, which take the form of property and value pairs. Each pair specifies a property of the element(s) we are selecting, then a value that we'd like to give the property.

###### Before the colon, we have the property, and after the colon, the value. CSS properties have different allowable values, depending on which property is being specified. In our example, we have the color property, which can take various color values. We also have the font-size property. This property can take various size units as a value.

A CSS stylesheet will contain many such rules, written one after the other.

### h1 {
  
###   color: red;
  
###   font-size: 5em;

###  }


###  p {
 
###    color: black;

###  }

##### You will find that you quickly learn some values, whereas others you will need to look up. The individual property pages on MDN give you a quick way to look up properties and their values when you forget, or want to know what else you can use as a value.

## Three Ways to Insert CSS
There are three ways of inserting a style sheet:

### 1. External CSS 
### 2. Internal CSS
### 3. Inline CSS
## External CSS
## Use The Link element inside head like this
#### <!DOCTYPE html>
#### <html>
#### <head>
#### <link rel="stylesheet" href="mystyle.css">
#### </head>
#### <body>
#### <html>


## Internal CSS

#### <head>
#### <style>
#### body {
 ####  background-color: linen;
#### }

#### h1 {
  #### color: maroon;
 #### margin-left: 40px;
#### }
#### </style>

## Inline CSS
#### <!DOCTYPE html>
#### <html>
#### <body>

#### <h1 style="color:blue;text-align:center;">This is a heading</h1>
#### <p style="color:red;">This is a paragraph.</p>

#### </body>
#### </html>

 # [HTML](#HTML) & [Javascript](#JavaScript)
 
 # HTML : Is A HyperText Markup Language.
### INTRODUCTION

Webpages are written in HTML - a simple scripting language.

Hypertext is simply a piece of text that works as a link.

Markup Language is a way of writing layout information within documents.


Basically an HTML document is a plain text file that contains text and nothing else.

When a browser opens an HTML file, the browser will look for HTML codes in the text and use them to change the layout, insert images, or create links to other pages.

Since HTML documents are just text files they can be written in even the simplest text editor.

A more popular choice is to use a special HTML editor - maybe even one that puts focus on the visual result rather than the codes - a so-called WYSIWYG editor ("What You See Is What You Get").

Some of the most popular HTML editors, such as FrontPage or Dreamweaver will let you create pages more or less as you write documents in Word or whatever text editor you're using.

However, there are some very good reasons to create your own pages - or parts of them - by hand...


## Markup
HTML markup consists of several key components, including those called tags (and their attributes), character-based data types, character references and entity references. HTML tags most commonly come in pairs like <h1> and </h1>, although some represent empty elements and so are unpaired, for example <img>. The first tag in such a pair is the start tag, and the second is the end tag (they are also called opening tags and closing tags).

Another important component is the HTML document type declaration, which triggers standards mode rendering.

The following is an example of the classic "Hello, World!" program:

<!DOCTYPE html>
<html>
  <head>
    <title>This is a title</title>
  </head>
  <body>
    <div>
        <p>Hello world!</p>
    </div>
  </body>
</html>
The text between <html> and </html> describes the web page, and the text between <body> and </body> is the visible page content. The markup text <title>This is a title</title> defines the browser page title, and the tag <div> defines a division of the page used for easy styling.

The Document Type Declaration <!DOCTYPE html> is for HTML5. If a declaration is not included, various browsers will revert to "quirks mode" for rendering.[70]

## Elements
Main article: HTML element
HTML documents imply a structure of nested HTML elements. These are indicated in the document by HTML tags, enclosed in angle brackets thus: <p>.[71][better source needed]

In the simple, general case, the extent of an element is indicated by a pair of tags: a "start tag" <p> and "end tag" </p>. The text content of the element, if any, is placed between these tags.

Tags may also enclose further tag markup between the start and end, including a mixture of tags and text. This indicates further (nested) elements, as children of the parent element.

The start tag may also include attributes within the tag. These indicate other information, such as identifiers for sections within the document, identifiers used to bind style information to the presentation of the document, and for some tags such as the <img> used to embed images, the reference to the image resource in the format like this: <img src="example.com/example.jpg">

Some elements, such as the line break <br>, or <br /> do not permit any embedded content, either text or further tags. These require only a single empty tag (akin to a start tag) and do not use an end tag.

Many tags, particularly the closing end tag for the very commonly used paragraph element <p>, are optional. An HTML browser or other agent can infer the closure for the end of an element from the context and the structural rules defined by the HTML standard. These rules are complex and not widely understood by most HTML coders.

The general form of an HTML element is therefore: <tag attribute1="value1" attribute2="value2">''content''</tag>. Some HTML elements are defined as empty elements and take the form <tag attribute1="value1" attribute2="value2">. Empty elements may enclose no content, for instance, the <br> tag or the inline <img> tag. The name of an HTML element is the name used in the tags. Note that the end tag's name is preceded by a slash character, /, and that in empty elements the end tag is neither required nor allowed. If attributes are not mentioned, default values are used in each case.

## Element examples
See also: HTML element
## Header of the HTML document: <head>...</head>. The title is included in the head, for example:

<head>
  <title>The Title</title>
  <link rel="stylesheet" href="stylebyjimbowales.css" /> <!-- Imports Stylesheets -->
</head>
Headings: HTML headings are defined with the <h1> to <h6> tags with H1 being the highest (or most important) level and H6 the least:

<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
The effects are:

Heading Level 1
Heading Level 2
Heading Level 3
Heading Level 4
Heading Level 5
Heading Level 6
Note that CSS can drastically change the rendering.

## Paragraphs:

<p>Paragraph 1</p> <p>Paragraph 2</p>
Line breaks: <br>. The difference between <br> and <p> is that <br> breaks a line without altering the semantic structure of the page, whereas <p> sections the page into paragraphs. The element <br> is an empty element in that, although it may have attributes, it can take no content and it may not have an end tag.

<p>This <br> is a paragraph <br> with <br> line breaks</p>
This is a link in HTML. To create a link the <a> tag is used. The href attribute holds the URL address of the link.
## links
<a href="https://www.google.com/">A link to Wikipedia!</a>
Inputs:

There are many possible ways a user can give input/s like:

<input type="text" /> <!-- This is for text input -->
<input type="file" /> <!-- This is for uploading files -->
<input type="checkbox" /> <!-- This is for checkboxes -->
## Comments:

<!-- This is a comment -->
Comments can help in the understanding of the markup and do not display in the webpage.

There are several types of markup elements used in HTML:

Structural markup indicates the purpose of text
For example, <h2>Golf</h2> establishes "Golf" as a second-level heading. Structural markup does not denote any specific rendering, but most web browsers have default styles for element formatting. Content may be further styled using Cascading Style Sheets (CSS).[72]
Presentational markup indicates the appearance of the text, regardless of its purpose
For example, <b>bold text</b> indicates that visual output devices should render "boldface" in bold text, but gives little indication what devices that are unable to do this (such as aural devices that read the text aloud) should do. In the case of both <b>bold text</b> and <i>italic text</i>, there are other elements that may have equivalent visual renderings but that are more semantic in nature, such as <strong>strong text</strong> and <em>emphasized text</em> respectively. It is easier to see how an aural user agent should interpret the latter two elements. However, they are not equivalent to their presentational counterparts: it would be undesirable for a screen-reader to emphasize the name of a book, for instance, but on a screen such a name would be italicized. Most presentational markup elements have become deprecated under the HTML 4.0 specification in favor of using CSS for styling.
Hypertext markup makes parts of a document into links to other documents
An anchor element creates a hyperlink in the document and its href attribute sets the link's target URL. For example, the HTML markup <a href="https://www.google.com/">Wikipedia</a>, will render the word "Wikipedia" as a hyperlink. To render an image as a hyperlink, an img element is inserted as content into the a element. Like br, img is an empty element with attributes but no content or closing tag. <a href="https://example.org"><img src="image.gif" alt="descriptive text" width="50" height="50" border="0"></a>.
Attributes
Main article: HTML attribute
Most of the attributes of an element are name-value pairs, separated by = and written within the start tag of an element after the element's name. The value may be enclosed in single or double quotes, although values consisting of certain characters can be left unquoted in HTML (but not XHTML).[73][74] Leaving attribute values unquoted is considered unsafe.[75] In contrast with name-value pair attributes, there are some attributes that affect the element simply by their presence in the start tag of the element,[6] like the ismap attribute for the img element.[76]

There are several common attributes that may appear in many elements :

The id attribute provides a document-wide unique identifier for an element. This is used to identify the element so that stylesheets can alter its presentational properties, and scripts may alter, animate or delete its contents or presentation. Appended to the URL of the page, it provides a globally unique identifier for the element, typically a sub-section of the page. For example, the ID "Attributes" in https://en.wikipedia.org/wiki/HTML#Attributes.
The class attribute provides a way of classifying similar elements. This can be used for semantic or presentation purposes. For example, an HTML document might semantically use the designation <class="notation"> to indicate that all elements with this class value are subordinate to the main text of the document. In presentation, such elements might be gathered together and presented as footnotes on a page instead of appearing in the place where they occur in the HTML source. Class attributes are used semantically in microformats. Multiple class values may be specified; for example <class="notation important"> puts the element into both the notation and the important classes.
An author may use the style attribute to assign presentational properties to a particular element. It is considered better practice to use an element's id or class attributes to select the element from within a stylesheet, though sometimes this can be too cumbersome for a simple, specific, or ad hoc styling.
The title attribute is used to attach subtextual explanation to an element. In most browsers this attribute is displayed as a tooltip.
The lang attribute identifies the natural language of the element's contents, which may be different from that of the rest of the document. For example, in an English-language document:
<p>Oh well, <span lang="fr">c'est la vie</span>, as they say in France.</p>
The abbreviation element, abbr, can be used to demonstrate some of these attributes:

<abbr id="anId" class="jargon" style="color:purple;" title="Hypertext Markup Language">HTML</abbr>
This example displays as HTML; in most browsers, pointing the cursor at the abbreviation should display the title text "Hypertext Markup Language."

Most elements take the language-related attribute dir to specify text direction, such as with "rtl" for right-to-left text in, for example, Arabic, Persian or Hebrew.[77]

Character and entity references
See also: List of XML and HTML character entity references and Unicode and HTML
As of version 4.0, HTML defines a set of 252 character entity references and a set of 1,114,050 numeric character references, both of which allow individual characters to be written via simple markup, rather than literally. A literal character and its markup counterpart are considered equivalent and are rendered identically.

The ability to "escape" characters in this way allows for the characters < and & (when written as &lt; and &amp;, respectively) to be interpreted as character data, rather than markup. For example, a literal < normally indicates the start of a tag, and & normally indicates the start of a character entity reference or numeric character reference; writing it as &amp; or &#x26; or &#38; allows & to be included in the content of an element or in the value of an attribute. The double-quote character ("), when not used to quote an attribute value, must also be escaped as &quot; or &#x22; or &#34; when it appears within the attribute value itself. Equivalently, the single-quote character ('), when not used to quote an attribute value, must also be escaped as &#x27; or &#39; (or as &apos; in HTML5 or XHTML documents[78][79]) when it appears within the attribute value itself. If document authors overlook the need to escape such characters, some browsers can be very forgiving and try to use context to guess their intent. The result is still invalid markup, which makes the document less accessible to other browsers and to other user agents that may try to parse the document for search and indexing purposes for example.

Escaping also allows for characters that are not easily typed, or that are not available in the document's character encoding, to be represented within element and attribute content. For example, the acute-accented e (é), a character typically found only on Western European and South American keyboards, can be written in any HTML document as the entity reference &eacute; or as the numeric references &#xE9; or &#233;, using characters that are available on all keyboards and are supported in all character encodings. Unicode character encodings such as UTF-8 are compatible with all modern browsers and allow direct access to almost all the characters of the world's writing systems.[80]

Example HTML Escape Sequences[clarification needed]
Named	Decimal	Hexadecimal	Result	Description	Notes
&amp;	&#38;	&#x26;	&	Ampersand	
&lt;	&#60;	&#x3C;	<	Less Than	
&gt;	&#62;	&#x3e;	>	Greater Than	
&quot;	&#34;	&#x22;	"	Double Quote	
&apos;	&#39;	&#x27;	'	Single Quote	
&nbsp;	&#160;	&#xA0;		Non-Breaking Space	
&copy;	&#169;	&#xA9;	©	Copyright	
&reg;	&#174;	&#xAE;	®	Registered Trademark	
&dagger;	&#8224;	&#x2020;	†	Dagger	
&Dagger;	&#8225;	&#x2021;	‡	Double dagger	Names are case sensitive
&ddagger;	&#8225;	&#x2021;	‡	Double dagger	Names may have synonyms
&trade;	&#8482;	&#x2122;	™	Trademark	
## Data types
HTML defines several data types for element content, such as script data and stylesheet data, and a plethora of types for attribute values, including IDs, names, URIs, numbers, units of length, languages, media descriptors, colors, character encodings, dates and times, and so on. All of these data types are specializations of character data.

## Document type declaration
HTML documents are required to start with a Document Type Declaration (informally, a "doctype"). In browsers, the doctype helps to define the rendering mode—particularly whether to use quirks mode.

The original purpose of the doctype was to enable parsing and validation of HTML documents by SGML tools based on the Document Type Definition (DTD). The DTD to which the DOCTYPE refers contains a machine-readable grammar specifying the permitted and prohibited content for a document conforming to such a DTD. Browsers, on the other hand, do not implement HTML as an application of SGML and by consequence do not read the DTD.

HTML5 does not define a DTD; therefore, in HTML5 the doctype declaration is simpler and shorter:[81]

<!DOCTYPE html>
An example of an HTML 4 doctype

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "https://www.w3.org/TR/html4/strict.dtd">
This declaration references the DTD for the "strict" version of HTML 4.01. SGML-based validators read the DTD in order to properly parse the document and to perform validation. In modern browsers, a valid doctype activates standards mode as opposed to quirks mode.

In addition, HTML 4.01 provides Transitional and Frameset DTDs, as explained below. Transitional type is the most inclusive, incorporating current tags as well as older or "deprecated" tags, with the Strict DTD excluding deprecated tags. Frameset has all tags necessary to make frames on a page along with the tags included in transitional type.[citation needed]

## Semantic HTML
Main article: Semantic HTML
Semantic HTML is a way of writing HTML that emphasizes the meaning of the encoded information over its presentation (look). HTML has included semantic markup from its inception,[82] but has also included presentational markup, such as <font>, <i> and <center> tags. There are also the semantically neutral span and div tags. Since the late 1990s, when Cascading Style Sheets were beginning to work in most browsers, web authors have been encouraged to avoid the use of presentational HTML markup with a view to the separation of presentation and content.[83]

In a 2001 discussion of the Semantic Web, Tim Berners-Lee and others gave examples of ways in which intelligent software "agents" may one day automatically crawl the web and find, filter and correlate previously unrelated, published facts for the benefit of human users.[84] Such agents are not commonplace even now, but some of the ideas of Web 2.0, mashups and price comparison websites may be coming close. The main difference between these web application hybrids and Berners-Lee's semantic agents lies in the fact that the current aggregation and hybridization of information is usually designed in by web developers, who already know the web locations and the API semantics of the specific data they wish to mash, compare and combine.

An important type of web agent that does crawl and read web pages automatically, without prior knowledge of what it might find, is the web crawler or search-engine spider. These software agents are dependent on the semantic clarity of web pages they find as they use various techniques and algorithms to read and index millions of web pages a day and provide web users with search facilities without which the World Wide Web's usefulness would be greatly reduced.

In order for search-engine spiders to be able to rate the significance of pieces of text they find in HTML documents, and also for those creating mashups and other hybrids as well as for more automated agents as they are developed, the semantic structures that exist in HTML need to be widely and uniformly applied to bring out the meaning of published text.[85]

Presentational markup tags are deprecated in current HTML and XHTML recommendations. The majority of presentational features from previous versions of HTML are no longer allowed as they lead to poorer accessibility, higher cost of site maintenance, and larger document sizes.[86]

Good semantic HTML also improves the accessibility of web documents (see also Web Content Accessibility Guidelines). For example, when a screen reader or audio browser can correctly ascertain the structure of a document, it will not waste the visually impaired user's time by reading out repeated or irrelevant information when it has been marked up correctly.

## Delivery
HTML documents can be delivered by the same means as any other computer file. However, they are most often delivered either by HTTP from a web server or by email.

## HTTP
Main article: Hypertext Transfer Protocol
The World Wide Web is composed primarily of HTML documents transmitted from web servers to web browsers using the Hypertext Transfer Protocol (HTTP). However, HTTP is used to serve images, sound, and other content, in addition to HTML. To allow the web browser to know how to handle each document it receives, other information is transmitted along with the document. This meta data usually includes the MIME type (e.g., text/html or application/xhtml+xml) and the character encoding (see Character encoding in HTML).

In modern browsers, the MIME type that is sent with the HTML document may affect how the document is initially interpreted. A document sent with the XHTML MIME type is expected to be well-formed XML; syntax errors may cause the browser to fail to render it. The same document sent with the HTML MIME type might be displayed successfully, since some browsers are more lenient with HTML.

The W3C recommendations state that XHTML 1.0 documents that follow guidelines set forth in the recommendation's Appendix C may be labeled with either MIME Type.[87] XHTML 1.1 also states that XHTML 1.1 documents should[88] be labeled with either MIME type.[89]

## HTML e-mail
Main article: HTML email
Most graphical email clients allow the use of a subset of HTML (often ill-defined) to provide formatting and semantic markup not available with plain text. This may include typographic information like coloured headings, emphasized and quoted text, inline images and diagrams. Many such clients include both a GUI editor for composing HTML e-mail messages and a rendering engine for displaying them. Use of HTML in e-mail is criticized by some because of compatibility issues, because it can help disguise phishing attacks, because of accessibility issues for blind or visually impaired people, because it can confuse spam filters and because the message size is larger than plain text.

Naming conventions
The most common filename extension for files containing HTML is .html. A common abbreviation of this is .htm, which originated because some early operating systems and file systems, such as DOS and the limitations imposed by FAT data structure, limited file extensions to three letters.[90]

## HTML Application
Main article: HTML Application
An HTML Application (HTA; file extension ".hta") is a Microsoft Windows application that uses HTML and Dynamic HTML in a browser to provide the application's graphical interface. A regular HTML file is confined to the security model of the web browser's security, communicating only to web servers and manipulating only web page objects and site cookies. An HTA runs as a fully trusted application and therefore has more privileges, like creation/editing/removal of files and Windows Registry entries. Because they operate outside the browser's security model, HTAs cannot be executed via HTTP, but must be downloaded (just like an EXE file) and executed from local file system.

# JavaScript
  
  JavaScript  often abbreviated as JS, is a programming language that conforms to the ECMAScript specification.[9] JavaScript is high-level, often just-in-time compiled, and multi-paradigm. It has curly-bracket syntax, dynamic typing, prototype-based object-orientation, and first-class functions.

Alongside HTML and CSS, JavaScript is one of the core technologies of the World Wide Web.[10] Over 97% of websites use it client-side for web page behavior,[11] often incorporating third-party libraries.[12] All major web browsers have a dedicated JavaScript engine to execute the code on the user's device.

As a multi-paradigm language, JavaScript supports event-driven, functional, and imperative programming styles. It has application programming interfaces (APIs) for working with text, dates, regular expressions, standard data structures, and the Document Object Model (DOM).

The ECMAScript standard does not include any input/output (I/O), such as networking, storage, or graphics facilities. In practice, the web browser or other runtime system provides JavaScript APIs for I/O.

JavaScript engines were originally used only in web browsers, but they are now core components of other software systems, most notably servers and a variety of applications.

Although there are similarities between JavaScript and Java, including language name, syntax, and respective standard libraries, the two languages are distinct and differ greatly in design.

 ## Dynamic
Typing
JavaScript is dynamically typed like most other scripting languages. A type is associated with a value rather than an expression. For example, a variable initially bound to a number may be reassigned to a string.[45] JavaScript supports various ways to test the type of objects, including duck typing.[46]
## Run-time evaluation
JavaScript includes an eval function that can execute statements provided as strings at run-time.
Object-orientation (prototype-based)
Prototypal inheritance in JavaScript is described by Douglas Crockford as:
You make prototype objects, and then … make new instances. Objects are mutable in JavaScript, so we can augment the new instances, giving them new fields and methods. These can then act as prototypes for even newer objects. We don't need classes to make lots of similar objects… Objects inherit from objects. What could be more object oriented than that?[47]
In JavaScript, an object is an associative array, augmented with a prototype (see below); each key provides the name for an object property, and there are two syntactical ways to specify such a name: dot notation (obj.x = 10) and bracket notation (obj['x'] = 10). A property may be added, rebound, or deleted at run-time. Most properties of an object (and any property that belongs to an object's prototype inheritance chain) can be enumerated using a for...in loop.

## Prototypes
JavaScript uses prototypes where many other object-oriented languages use classes for inheritance.[48] It is possible to simulate many class-based features with prototypes in JavaScript.[49]
Functions as object constructors
Functions double as object constructors, along with their typical role. Prefixing a function call with new will create an instance of a prototype, inheriting properties and methods from the constructor (including properties from the Object prototype).[50] ECMAScript 5 offers the Object.create method, allowing explicit creation of an instance without automatically inheriting from the Object prototype (older environments can assign the prototype to null).[51] The constructor's prototype property determines the object used for the new object's internal prototype. New methods can be added by modifying the prototype of the function used as a constructor. JavaScript's built-in constructors, such as Array or Object, also have prototypes that can be modified. While it is possible to modify the Object prototype, it is generally considered bad practice because most objects in JavaScript will inherit methods and properties from the Object prototype, and they may not expect the prototype to be modified.[52]
Functions as methods
Unlike many object-oriented languages, there is no distinction between a function definition and a method definition. Rather, the distinction occurs during function calling; when a function is called as a method of an object, the function's local this keyword is bound to that object for that invocation.

## Functional
A function is first-class; a function is considered to be an object. As such, a function may have properties and methods, such as .call() and .bind().[53] A nested function is a function defined within another function. It is created each time the outer function is invoked. In addition, each nested function forms a lexical closure: The lexical scope of the outer function (including any constant, local variable, or argument value) becomes part of the internal state of each inner function object, even after execution of the outer function concludes.[54] JavaScript also supports anonymous functions.

## Delegative
JavaScript supports implicit and explicit delegation.

## Functions as roles (Traits and Mixins)
JavaScript natively supports various function-based implementations of Role[55] patterns like Traits[56][57] and Mixins.[58] Such a function defines additional behavior by at least one method bound to the this keyword within its function body. A Role then has to be delegated explicitly via call or apply to objects that need to feature additional behavior that is not shared via the prototype chain.
Object composition and inheritance
Whereas explicit function-based delegation does cover composition in JavaScript, implicit delegation already happens every time the prototype chain is walked in order to, e.g., find a method that might be related to but is not directly owned by an object. Once the method is found it gets called within this object's context. Thus inheritance in JavaScript is covered by a delegation automatism that is bound to the prototype property of constructor functions.

  Miscellaneous
JS is a zero-index language.
## Run-time environment
JavaScript typically relies on a run-time environment (e.g., a web browser) to provide objects and methods by which scripts can interact with the environment (e.g., a web page DOM). These environments are single-threaded. JavaScript also relies on the run-time environment to provide the ability to include/import scripts (e.g., HTML <script> elements). This is not a language feature per se, but it is common in most JavaScript implementations. JavaScript processes messages from a queue one at a time. JavaScript calls a function associated with each new message, creating a call stack frame with the function's arguments and local variables. The call stack shrinks and grows based on the function's needs. When the call stack is empty upon function completion, JavaScript proceeds to the next message in the queue. This is called the event loop, described as "run to completion" because each message is fully processed before the next message is considered. However, the language's concurrency model describes the event loop as non-blocking: program input/output is performed using events and callback functions. This means, for instance, that JavaScript can process a mouse click while waiting for a database query to return information.[59]
## Variadic functions
An indefinite number of parameters can be passed to a function. The function can access them through formal parameters and also through the local arguments object. Variadic functions can also be created by using the bind method.
## Array and object literals
Like many scripting languages, arrays and objects (associative arrays in other languages) can each be created with a succinct shortcut syntax. In fact, these literals form the basis of the JSON data format.
## Regular expressions
JavaScript also supports regular expressions in a manner similar to Perl, which provide a concise and powerful syntax for text manipulation that is more sophisticated than the built-in string functions.[60]
## Promises
JavaScript also supports promises, which are a way of handling asynchronous operations. There is a built-in Promise object that gives access to a lot of functionalities for handling promises, and defines how they should be handled. It allows one to associate handlers with an asynchronous action's eventual success value or failure reason. This lets asynchronous methods return values like synchronous methods: instead of immediately returning the final value, the asynchronous method returns a promise to supply the value at some point in the future. Recently, combinator methods were introduced in the JavaScript specification, which allows developers to combine multiple JavaScript promises and do operations on the basis of different scenarios. The methods introduced are: Promise.race, Promise.all, Promise.allSettled and Promise.any.
## Vendor-specific extensions
Historically, some JavaScript engines supported these non-standard features:

## conditional catch clauses (like Java)
array comprehensions and generator expressions (like Python)
concise function expressions (function(args) expr; this experimental syntax predated arrow functions)
ECMAScript for XML (E4X), an extension that adds native XML support to ECMAScript (unsupported in Firefox since version 21[61])

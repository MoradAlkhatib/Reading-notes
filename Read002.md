

![alt text](https://th.bing.com/th/id/Ra911febe269376087e9cbc95037b0a93?rik=fRZMTBmZbDmxQg&pid=ImgRaw "title")
# HTML
## HTML is short for HyperText Markup Language.
Hypertext is simply a piece of text that works as a link.


Markup Language is a way of writing layout information within documents.


Basically an HTML document is a plain text file that contains text and nothing else.

When a browser opens an HTML file, the browser will look for HTML codes in the text and use them to change the layout, insert images, or create links to other pages.

Since HTML documents are just text files they can be written in even the simplest text editor.

A more popular choice is to use a special HTML editor - maybe even one that puts focus on the visual result rather than the codes - a so-called WYSIWYG editor ("What You See Is What You Get").

Some of the most popular HTML editors, such as FrontPage or Dreamweaver will let you create pages more or less as you write documents in Word or whatever text editor you're using.

However, there are some very good reasons to create your own pages - or parts of them - by hand...

 HTML version information
A valid HTML document declares what version of HTML is used in the document. The document type declaration names the document type definition (DTD) in use for the document (see [ISO8879]).

HTML 4.01 specifies three DTDs, so authors must include one of the following document type declarations in their documents. The DTDs vary in the elements they support.

The HTML 4.01 Strict DTD includes all elements and attributes that have not been deprecated or do not appear in frameset documents. For documents that use this DTD, use this document type declaration:
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
        "http://www.w3.org/TR/html4/strict.dtd">
The HTML 4.01 Transitional DTD includes everything in the strict DTD plus deprecated elements and attributes (most of which concern visual presentation). For documents that use this DTD, use this document type declaration:
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN"
        "http://www.w3.org/TR/html4/loose.dtd">
The HTML 4.01 Frameset DTD includes everything in the transitional DTD plus frames as well. For documents that use this DTD, use this document type declaration:
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Frameset//EN"
        "http://www.w3.org/TR/html4/frameset.dtd">
The URI in each document type declaration allows user agents to download the DTD and any entity sets that are needed. The following (relative) URIs refer to DTDs and entity sets for HTML 4:

"strict.dtd" -- default strict DTD
"loose.dtd" -- loose DTD
"frameset.dtd" -- DTD for frameset documents
"HTMLlat1.ent" -- Latin-1 entities
"HTMLsymbol.ent" -- Symbol entities
"HTMLspecial.ent" -- Special entities
The binding between public identifiers and files can be specified using a catalog file following the format recommended by the Oasis Open Consortium (see [OASISOPEN]). A sample catalog file for HTML 4.01 is included at the beginning of the section on SGML reference information for HTML. The last two letters of the declaration indicate the language of the DTD. For HTML, this is always English ("EN").

Note. As of the 24 December version of HTML 4.01, the HTML Working Group commits to the following policy:

Any changes to future HTML 4 DTDs will not invalidate documents that conform to the DTDs of the present specification. The HTML Working Group reserves the right to correct known bugs.
Software conforming to the DTDs of the present specification may ignore features of future HTML 4 DTDs that it does not recognize.
This means that in a document type declaration, authors may safely use a system identifier that refers to the latest version of an HTML 4 DTD. Authors may also choose to use a system identifier that refers to a specific (dated) version of an HTML 4 DTD when validation to that particular DTD is required. W3C will make every effort to make archival documents indefinitely available at their original address in their original form.

7.3 The HTML element
<!ENTITY % html.content "HEAD, BODY">

<!ELEMENT HTML O O (%html.content;)    -- document root element -->
<!ATTLIST HTML
  %i18n;                               -- lang, dir --
  >
Start tag: optional, End tag: optional

Attribute definitions

version = cdata [CN]
Deprecated. The value of this attribute specifies which HTML DTD version governs the current document. This attribute has been deprecated because it is redundant with version information provided by the document type declaration.
Attributes defined elsewhere

lang (language information), dir (text direction)
After document type declaration, the remainder of an HTML document is contained by the HTML element. Thus, a typical HTML document has this structure:

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
"http://www.w3.org/TR/html4/strict.dtd">
<HTML>
...The head, body, etc. goes here...
</HTML>
7.4 The document head
7.4.1 The HEAD element
<!-- %head.misc; defined earlier on as "SCRIPT|STYLE|META|LINK|OBJECT" -->
<!ENTITY % head.content "TITLE & BASE?">

<!ELEMENT HEAD O O (%head.content;) +(%head.misc;) -- document head -->
<!ATTLIST HEAD
  %i18n;                               -- lang, dir --
  profile     %URI;          #IMPLIED  -- named dictionary of meta info --
  >
Start tag: optional, End tag: optional

Attribute definitions

profile = uri [CT]
This attribute specifies the location of one or more meta data profiles, separated by white space. For future extensions, user agents should consider the value to be a list even though this specification only considers the first URI to be significant. Profiles are discussed below in the section on meta data.
Attributes defined elsewhere

lang (language information), dir (text direction)
The HEAD element contains information about the current document, such as its title, keywords that may be useful to search engines, and other data that is not considered document content. User agents do not generally render elements that appear in the HEAD as content. They may, however, make information in the HEAD available to users through other mechanisms.

7.4.2 The TITLE element
<!-- The TITLE element is not considered part of the flow of text.
       It should be displayed, for example as the page header or
       window title. Exactly one title is required per document.
    -->
<!ELEMENT TITLE - - (#PCDATA) -(%head.misc;) -- document title -->
<!ATTLIST TITLE %i18n>
Start tag: required, End tag: required

Attributes defined elsewhere

lang (language information), dir (text direction)
Every HTML document must have a TITLE element in the HEAD section.

Authors should use the TITLE element to identify the contents of a document. Since users often consult documents out of context, authors should provide context-rich titles. Thus, instead of a title such as "Introduction", which doesn't provide much contextual background, authors should supply a title such as "Introduction to Medieval Bee-Keeping" instead.

For reasons of accessibility, user agents must always make the content of the TITLE element available to users (including TITLE elements that occur in frames). The mechanism for doing so depends on the user agent (e.g., as a caption, spoken).

Titles may contain character entities (for accented characters, special characters, etc.), but may not contain other markup (including comments). Here is a sample document title:

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
<TITLE>A study of population dynamics</TITLE>
... other head elements...
</HEAD>
<BODY>
... document body...
</BODY>
</HTML>
7.4.3 The title attribute
Attribute definitions

title = text [CS]
This attribute offers advisory information about the element for which it is set.
Unlike the TITLE element, which provides information about an entire document and may only appear once, the title attribute may annotate any number of elements. Please consult an element's definition to verify that it supports this attribute.

Values of the title attribute may be rendered by user agents in a variety of ways. For instance, visual browsers frequently display the title as a "tool tip" (a short message that appears when the pointing device pauses over an object). Audio user agents may speak the title information in a similar context. For example, setting the attribute on a link allows user agents (visual and non-visual) to tell users about the nature of the linked resource:

...some text...
Here's a photo of 
<A href="http://someplace.com/neatstuff.gif" title="Me scuba diving">
   me scuba diving last summer
</A>
...some more text...
The title attribute has an additional role when used with the LINK element to designate an external style sheet. Please consult the section on links and style sheets for details.

Note. To improve the quality of speech synthesis for cases handled poorly by standard techniques, future versions of HTML may include an attribute for encoding phonemic and prosodic information.

7.4.4 Meta data
Note. The W3C Resource Description Framework (see [RDF10]) became a W3C Recommendation in February 1999. RDF allows authors to specify machine-readable metadata about HTML documents and other network-accessible resources.

HTML lets authors specify meta data -- information about a document rather than document content -- in a variety of ways.

For example, to specify the author of a document, one may use the META element as follows:

<META name="Author" content="Dave Raggett">
The META element specifies a property (here "Author") and assigns a value to it (here "Dave Raggett").

This specification does not define a set of legal meta data properties. The meaning of a property and the set of legal values for that property should be defined in a reference lexicon called a profile. For example, a profile designed to help search engines index documents might define properties such as "author", "copyright", "keywords", etc.

Specifying meta data 
In general, specifying meta data involves two steps:

Declaring a property and a value for that property. This may be done in two ways:
From within a document, via the META element.
From outside a document, by linking to meta data via the LINK element (see the section on link types).
Referring to a profile where the property and its legal values are defined. To designate a profile, use the profile attribute of the HEAD element.
Note that since a profile is defined for the HEAD element, the same profile applies to all META and LINK elements in the document head.

User agents are not required to support meta data mechanisms. For those that choose to support meta data, this specification does not define how meta data should be interpreted.

The META element 
<!ELEMENT META - O EMPTY               -- generic metainformation -->
<!ATTLIST META
  %i18n;                               -- lang, dir, for use with content --
  http-equiv  NAME           #IMPLIED  -- HTTP response header name  --
  name        NAME           #IMPLIED  -- metainformation name --
  content     CDATA          #REQUIRED -- associated information --
  scheme      CDATA          #IMPLIED  -- select form of content --
  >
Start tag: required, End tag: forbidden

Attribute definitions

For the following attributes, the permitted values and their interpretation are profile dependent:

name = name [CS]
This attribute identifies a property name. This specification does not list legal values for this attribute.
content = cdata [CS]
This attribute specifies a property's value. This specification does not list legal values for this attribute.
scheme = cdata [CS]
This attribute names a scheme to be used to interpret the property's value (see the section on profiles for details).
http-equiv = name [CI]
This attribute may be used in place of the name attribute. HTTP servers use this attribute to gather information for HTTP response message headers.
Attributes defined elsewhere

lang (language information), dir (text direction)
The META element can be used to identify properties of a document (e.g., author, expiration date, a list of key words, etc.) and assign values to those properties. This specification does not define a normative set of properties.

Each META element specifies a property/value pair. The name attribute identifies the property and the content attribute specifies the property's value.

For example, the following declaration sets a value for the Author property:

<META name="Author" content="Dave Raggett">
The lang attribute can be used with META to specify the language for the value of the content attribute. This enables speech synthesizers to apply language dependent pronunciation rules.

In this example, the author's name is declared to be French:

<META name="Author" lang="fr" content="Arnaud Le Hors">
Note. The META element is a generic mechanism for specifying meta data. However, some HTML elements and attributes already handle certain pieces of meta data and may be used by authors instead of META to specify those pieces: the TITLE element, the ADDRESS element, the INS and DEL elements, the title attribute, and the cite attribute.

Note. When a property specified by a META element takes a value that is a URI, some authors prefer to specify the meta data via the LINK element. Thus, the following meta data declaration:

<META name="DC.identifier"
      content="http://www.ietf.org/rfc/rfc1866.txt">
might also be written:

<LINK rel="DC.identifier"
         type="text/plain"
         href="http://www.ietf.org/rfc/rfc1866.txt">
META and HTTP headers
The http-equiv attribute can be used in place of the name attribute and has a special significance when documents are retrieved via the Hypertext Transfer Protocol (HTTP). HTTP servers may use the property name specified by the http-equiv attribute to create an [RFC822]-style header in the HTTP response. Please see the HTTP specification ([RFC2616]) for details on valid HTTP headers.

The following sample META declaration:

<META http-equiv="Expires" content="Tue, 20 Aug 1996 14:25:27 GMT">
will result in the HTTP header:

Expires: Tue, 20 Aug 1996 14:25:27 GMT
This can be used by caches to determine when to fetch a fresh copy of the associated document.

Note. Some user agents support the use of META to refresh the current page after a specified number of seconds, with the option of replacing it by a different URI. Authors should not use this technique to forward users to different pages, as this makes the page inaccessible to some users. Instead, automatic page forwarding should be done using server-side redirects.

META and search engines
A common use for META is to specify keywords that a search engine may use to improve the quality of search results. When several META elements provide language-dependent information about a document, search engines may filter on the lang attribute to display search results using the language preferences of the user. For example,

<-- For speakers of US English -->
<META name="keywords" lang="en-us" 
         content="vacation, Greece, sunshine">
<-- For speakers of British English -->
<META name="keywords" lang="en" 
         content="holiday, Greece, sunshine">
<-- For speakers of French -->
<META name="keywords" lang="fr" 
         content="vacances, Gr&egrave;ce, soleil">
The effectiveness of search engines can also be increased by using the LINK element to specify links to translations of the document in other languages, links to versions of the document in other media (e.g., PDF), and, when the document is part of a collection, links to an appropriate starting point for browsing the collection.

Further help is provided in the section on helping search engines index your Web site.

META and PICS
The Platform for Internet Content Selection (PICS, specified in [PICS]) is an infrastructure for associating labels (meta data) with Internet content. Originally designed to help parents and teachers control what children can access on the Internet, it also facilitates other uses for labels, including code signing, privacy, and intellectual property rights management.
This example illustrates how one can use a META declaration to include a PICS 1.1 label:

<HEAD>
 <META http-equiv="PICS-Label" content='
 (PICS-1.1 "http://www.gcf.org/v2.5"
    labels on "1994.11.05T08:15-0500"
      until "1995.12.31T23:59-0000"
      for "http://w3.org/PICS/Overview.html"
    ratings (suds 0.5 density 0 color/hue 1))
 '>
  <TITLE>... document title ...</TITLE>
</HEAD>
META and default information
The META element may be used to specify the default information for a document in the following instances:

The default scripting language.
The default style sheet language.
The document character encoding.
The following example specifies the character encoding for a document as being ISO-8859-5

<META http-equiv="Content-Type" content="text/html; charset=ISO-8859-5"> 
Meta data profiles 
The profile attribute of the HEAD specifies the location of a meta data profile. The value of the profile attribute is a URI. User agents may use this URI in two ways:
As a globally unique name. User agents may be able to recognize the name (without actually retrieving the profile) and perform some activity based on known conventions for that profile. For instance, search engines could provide an interface for searching through catalogs of HTML documents, where these documents all use the same profile for representing catalog entries.
As a link. User agents may dereference the URI and perform some activity based on the actual definitions within the profile (e.g., authorize the usage of the profile within the current HTML document). This specification does not define formats for profiles.
This example refers to a hypothetical profile that defines useful properties for document indexing. The properties defined by this profile -- including "author", "copyright", "keywords", and "date" -- have their values set by subsequent META declarations.

 <HEAD profile="http://www.acme.com/profiles/core">
  <TITLE>How to complete Memorandum cover sheets</TITLE>
  <META name="author" content="John Doe">
  <META name="copyright" content="&copy; 1997 Acme Corp.">
  <META name="keywords" content="corporate,guidelines,cataloging">
  <META name="date" content="1994-11-06T08:49:37+00:00">
 </HEAD>
As this specification is being written, it is common practice to use the date formats described in [RFC2616], section 3.3. As these formats are relatively hard to process, we recommend that authors use the [ISO8601] date format. For more information, see the sections on the INS and DEL elements.

The scheme attribute allows authors to provide user agents more context for the correct interpretation of meta data. At times, such additional information may be critical, as when meta data may be specified in different formats. For example, an author might specify a date in the (ambiguous) format "10-9-97"; does this mean 9 October 1997 or 10 September 1997? The scheme attribute value "Month-Day-Year" would disambiguate this date value.

At other times, the scheme attribute may provide helpful but non-critical information to user agents.

For example, the following scheme declaration may help a user agent determine that the value of the "identifier" property is an ISBN code number:

<META scheme="ISBN"  name="identifier" content="0-8230-2355-9">
Values for the scheme attribute depend on the property name and the associated profile.

# CSS
  Cascading Style Sheets (CSS) is a style sheet language used for describing the presentation of a document written in a markup language such as HTML.[1] CSS is a cornerstone technology of the World Wide Web, alongside HTML and JavaScript.[2]

CSS is designed to enable the separation of presentation and content, including layout, colors, and fonts.[3] This separation can improve content accessibility, provide more flexibility and control in the specification of presentation characteristics, enable multiple web pages to share formatting by specifying the relevant CSS in a separate .css file which reduces complexity and repetition in the structural content as well as enabling the .css file to be cached to improve the page load speed between the pages that share the file and its formatting.

Separation of formatting and content also makes it feasible to present the same markup page in different styles for different rendering methods, such as on-screen, in print, by voice (via speech-based browser or screen reader), and on Braille-based tactile devices. CSS also has rules for alternate formatting if the content is accessed on a mobile device.[4]

The name cascading comes from the specified priority scheme to determine which style rule applies if more than one rule matches a particular element. This cascading priority scheme is predictable.

The CSS specifications are maintained by the World Wide Web Consortium (W3C). Internet media type (MIME type) text/css is registered for use with CSS by RFC 2318 (March 1998). The W3C operates a free CSS validation service for CSS documents.[5]

In addition to HTML, other markup languages support the use of CSS including XHTML, plain XML, SVG, and XUL.
  Selector
In CSS, selectors declare which part of the markup a style applies to by matching tags and attributes in the markup itself.

Selectors may apply to the following:

all elements of a specific type, e.g. the second-level headers h2
elements specified by attribute, in particular:
id: an identifier unique within the document, identified with a hash prefix e.g. #id
class: an identifier that can annotate multiple elements in a document, identified with a period prefix e.g. .classname
elements depending on how they are placed relative to others in the document tree.
Classes and IDs are case-sensitive, start with letters, and can include alphanumeric characters, hyphens, and underscores. A class may apply to any number of instances of any elements. An ID may only be applied to a single element.

Pseudo-classes are used in CSS selectors to permit formatting based on information that is not contained in the document tree. One example of a widely used pseudo-class is :hover, which identifies content only when the user "points to" the visible element, usually by holding the mouse cursor over it. It is appended to a selector as in a:hover or #elementid:hover. A pseudo-class classifies document elements, such as :link or :visited, whereas a pseudo-element makes a selection that may consist of partial elements, such as ::first-line or ::first-letter.[6]

Selectors may be combined in many ways to achieve great specificity and flexibility.[7] Multiple selectors may be joined in a spaced list to specify elements by location, element type, id, class, or any combination thereof. The order of the selectors is important. For example, div .myClass {color: red;} applies to all elements of class myClass that are inside div elements, whereas .myClass div {color: red;} applies to all div elements that are inside elements of class myClass. This is not to be confused with concatenated identifiers such as div.myClass {color: red;} which applies to div elements of class myClass.

The following table provides a summary of selector syntax indicating usage and the version of CSS that introduced it.[8]
  
 # Javascript
  JavaScript (/ˈdʒɑːvəˌskrɪpt/),[8] often abbreviated as JS, is a programming language that conforms to the ECMAScript specification.[9] JavaScript is high-level, often just-in-time compiled, and multi-paradigm. It has curly-bracket syntax, dynamic typing, prototype-based object-orientation, and first-class functions.

Alongside HTML and CSS, JavaScript is one of the core technologies of the World Wide Web.[10] Over 97% of websites use it client-side for web page behavior,[11] often incorporating third-party libraries.[12] All major web browsers have a dedicated JavaScript engine to execute the code on the user's device.

As a multi-paradigm language, JavaScript supports event-driven, functional, and imperative programming styles. It has application programming interfaces (APIs) for working with text, dates, regular expressions, standard data structures, and the Document Object Model (DOM).

The ECMAScript standard does not include any input/output (I/O), such as networking, storage, or graphics facilities. In practice, the web browser or other runtime system provides JavaScript APIs for I/O.

JavaScript engines were originally used only in web browsers, but they are now core components of other software systems, most notably servers and a variety of applications.

Although there are similarities between JavaScript and Java, including language name, syntax, and respective standard libraries, the two languages are distinct and differ greatly in design.
  Creation at Netscape
The Mosaic web browser was released in 1993. As the first browser with a graphical user interface accessible to non-technical people, it played a prominent role in the rapid growth of the nascent World Wide Web.[13] The lead developers of Mosaic then founded the Netscape corporation, which released a more polished browser, Netscape Navigator, in 1994. Navigator quickly became the most used browser.[14]

During these formative years of the Web, web pages could only be static, lacking the capability for dynamic behavior after the page was loaded in the browser. There was a desire in the burgeoning web development scene to remove this limitation, so in 1995, Netscape decided to add a scripting language to Navigator. They pursued two routes to achieve this: collaborating with Sun Microsystems to embed the Java programming language, while also hiring Brendan Eich to embed the Scheme language.[5]

Netscape management soon decided that the best option was for Eich to devise a new language, with syntax similar to Java and less like Scheme or other extant scripting languages.[4][5] Although the new language and its interpreter implementation were called LiveScript when first shipped as part of a Navigator beta in September 1995, the name was changed to JavaScript for the official release in December.[5][1][15]

The choice of the JavaScript name has caused confusion, implying that it is directly related to Java. Since Java was the hot new programming language at the time, this has been characterized as a marketing ploy by Netscape to give its own new language cachet.[16]

Adoption by Microsoft
Microsoft debuted Internet Explorer in 1995, leading to a browser war with Netscape. On the JavaScript front, Microsoft reverse-engineered the Navigator interpreter to create its own, called JScript.

JScript was first released in 1996, alongside initial support for CSS and extensions to HTML. Each of these implementations was noticeably different from their counterparts in Navigator.[17][18] These differences made it difficult for developers to make their websites work well in both browsers, leading to widespread use of "best viewed in Netscape" and "best viewed in Internet Explorer" logos for several years.[17][19]

The rise of JScript
In November 1996, Netscape submitted JavaScript to Ecma International, as the starting point for a standard specification that all browser vendors could conform to. This led to the official release of the first ECMAScript language specification in June 1997.

The standards process continued for a few years, with the release of ECMAScript 2 in June 1998 and ECMAScript 3 in December 1999. Work on ECMAScript 4 began in 2000.

Meanwhile, Microsoft gained an increasingly dominant position in the browser market. By the early 2000s, Internet Explorer's market share reached 95%.[20] This meant that JScript became the de facto standard for client-side scripting on the Web.

Microsoft initially participated in the standards process and implemented some proposals in its JScript language, but eventually it stopped collaborating on Ecma work. Thus ECMAScript 4 was mothballed.

Growth and standardization
During the period of Internet Explorer dominance in the early 2000s, client-side scripting was stagnant. This started to change in 2004, when the successor of Netscape, Mozilla, released the Firefox browser. Firefox was well received by many, taking significant market share from Internet Explorer.[21]

In 2005, Mozilla joined ECMA International, and work started on the ECMAScript for XML (E4X) standard. This led to Mozilla working jointly with Macromedia (later acquired by Adobe Systems), who were implementing E4X in their ActionScript 3 language, which was based on an ECMAScript 4 draft. The goal became standardizing ActionScript 3 as the new ECMAScript 4. To this end, Adobe Systems released the Tamarin implementation as an open source project. However, Tamarin and ActionScript 3 were too different from established client-side scripting, and without cooperation from Microsoft, ECMAScript 4 never reached fruition.

Meanwhile, very important developments were occurring in open-source communities not affiliated with ECMA work. In 2005, Jesse James Garrett released a white paper in which he coined the term Ajax and described a set of technologies, of which JavaScript was the backbone, to create web applications where data can be loaded in the background, avoiding the need for full page reloads. This sparked a renaissance period of JavaScript, spearheaded by open-source libraries and the communities that formed around them. Many new libraries were created, including jQuery, Prototype, Dojo Toolkit, and MooTools.

Google debuted its Chrome browser in 2008, with the V8 JavaScript engine that was faster than its competition.[22][23] The key innovation was just-in-time compilation (JIT),[24] so other browser vendors needed to overhaul their engines for JIT.[25]

In July 2008, these disparate parties came together for a conference in Oslo. This led to the eventual agreement in early 2009 to combine all relevant work and drive the language forward. The result was the ECMAScript 5 standard, released in December 2009.

Reaching maturity
Ambitious work on the language continued for several years, culminating in an extensive collection of additions and refinements being formalized with the publication of ECMAScript 6 in 2015.[26]

The draft specification is currently maintained openly on GitHub, and ECMAScript editions are produced via regular annual snapshots.[27] Potential revisions to the language are vetted through a comprehensive proposal process.[28][29] Now, instead of edition numbers, developers check the status of upcoming features individually.[27]

The current JavaScript ecosystem has many libraries and frameworks, established programming practices, and increased usage of JavaScript outside of web browsers. Plus, with the rise of single-page applications and other JavaScript-heavy websites, a number of transpilers have been created to aid the development process.[30]

Trademark
"JavaScript" is a trademark of Oracle Corporation in the United States.[31][32]

Website client-side usage
JavaScript is the dominant client-side scripting language of the Web, with 97% of websites using it for this purpose.[11] Scripts are embedded in or included from HTML documents and interact with the DOM. All major web browsers have a built-in JavaScript engine that executes the code on the user's device.

Examples of scripted behavior
Loading new web page content without reloading the page, via Ajax or a WebSocket. For example, users of social media can send and receive messages without leaving the current page.
Web page animations, such as fading objects in and out, resizing, and moving them.
Playing browser games.
Controlling the playback of streaming media.
Generating pop-ups.
Validating input values of a web form before the data is sent to a web server.
Logging data about the user's behavior then sending it to a server. The website owner can use this data for analytics, ad tracking, and personalization.
Libraries and frameworks
Over 80% of websites use a third-party JavaScript library or web framework for their client-side scripting.[12]

jQuery is by far the most popular library, used by over 75% of websites.[12] Facebook created the React library for its website and later released it as open source; other sites, including Twitter, now use it. Likewise, the Angular framework created by Google for its websites, including YouTube and Gmail, is now an open source project used by others.[12]

In contrast, the term "Vanilla JS" has been coined for websites not using any libraries or frameworks, instead relying entirely on standard JavaScript functionality.[33]

Other usage
The use of JavaScript has expanded beyond its web browser roots. JavaScript engines are now embedded in a variety of other software systems, both for server-side website deployments and non-browser applications.

Initial attempts at promoting server-side JavaScript usage were Netscape Enterprise Server and Microsoft's Internet Information Services,[34][35] but they were small niches.[36] Server-side usage eventually started to grow in the late 2000s, with the creation of Node.js and other approaches.[36]

Electron, Cordova, React Native, and other application frameworks have been used to create many applications with behavior implemented in JavaScript. Other non-browser applications include Adobe Acrobat support for scripting PDF documents[37] and GNOME Shell extensions written in JavaScript.[38]

JavaScript has recently begun to appear in some embedded systems, usually by leveraging Node.js.[39][40][41]

Features
The following features are common to all conforming ECMAScript implementations, unless explicitly specified otherwise.

Imperative and structured
JavaScript supports much of the structured programming syntax from C (e.g., if statements, while loops, switch statements, do while loops, etc.). One partial exception is scoping: originally JavaScript only had function scoping with var; then block scoping was added in ECMAScript 2015 with the keywords let and const. Like C, JavaScript makes a distinction between expressions and statements. One syntactic difference from C is automatic semicolon insertion, which allow semicolons (which terminate statements) to be omitted.[42]

Weakly typed
JavaScript is weakly typed, which means certain types are implicitly cast depending on the operation used.[43]

The binary + operator casts both operands to a string unless both operands are numbers. This is because the addition operator doubles as a concatenation operator
The binary - operator always casts both operands to a number
Both unary operators (+, -) always cast the operand to a number
Values are cast to strings like the following:[43]

Strings are left as-is
Numbers are converted to their string representation
Arrays have their elements cast to strings after which they are joined by commas (,)
Other objects are converted to the string [object Object] where Object is the name of the constructor of the object
Values are cast to numbers by casting to strings and then casting the strings to numbers. These processes can be modified by defining toString and valueOf functions on the prototype for string and number casting respectively.

JavaScript has received criticism for the way it implements these conversions as the complexity of the rules can be mistaken for inconsistency.[44][43] For example, when adding a number to a string, the number will be cast to a string before performing concatenation, but when subtracting a number from a string, the string is cast to a number before performing subtraction.

JavaScript type conversions
left operand	operator	right operand	result
[] (empty array)	+	[] (empty array)	"" (empty string)
[] (empty array)	+	{} (empty object)	"[object Object]" (string)
false (boolean)	+	[] (empty array)	"false" (string)
"123"(string)	+	1 (number)	"1231" (string)
"123" (string)	-	1 (number)	122 (number)
Often also mentioned is {} + [] resulting in 0 (number). This is misleading: the {} is interpreted as an empty code block instead of an empty object, and the empty array is cast to a number by the remaining unary + operator. If you wrap the expression in parentheses ({} + []) the curly brackets are interpreted as an empty object and the result of the expression is "[object Object]" as expected.[43]

Dynamic
Typing
JavaScript is dynamically typed like most other scripting languages. A type is associated with a value rather than an expression. For example, a variable initially bound to a number may be reassigned to a string.[45] JavaScript supports various ways to test the type of objects, including duck typing.[46]
Run-time evaluation
JavaScript includes an eval function that can execute statements provided as strings at run-time.
Object-orientation (prototype-based)
Prototypal inheritance in JavaScript is described by Douglas Crockford as:

You make prototype objects, and then … make new instances. Objects are mutable in JavaScript, so we can augment the new instances, giving them new fields and methods. These can then act as prototypes for even newer objects. We don't need classes to make lots of similar objects… Objects inherit from objects. What could be more object oriented than that?[47]

In JavaScript, an object is an associative array, augmented with a prototype (see below); each key provides the name for an object property, and there are two syntactical ways to specify such a name: dot notation (obj.x = 10) and bracket notation (obj['x'] = 10). A property may be added, rebound, or deleted at run-time. Most properties of an object (and any property that belongs to an object's prototype inheritance chain) can be enumerated using a for...in loop.

Prototypes
JavaScript uses prototypes where many other object-oriented languages use classes for inheritance.[48] It is possible to simulate many class-based features with prototypes in JavaScript.[49]
Functions as object constructors
Functions double as object constructors, along with their typical role. Prefixing a function call with new will create an instance of a prototype, inheriting properties and methods from the constructor (including properties from the Object prototype).[50] ECMAScript 5 offers the Object.create method, allowing explicit creation of an instance without automatically inheriting from the Object prototype (older environments can assign the prototype to null).[51] The constructor's prototype property determines the object used for the new object's internal prototype. New methods can be added by modifying the prototype of the function used as a constructor. JavaScript's built-in constructors, such as Array or Object, also have prototypes that can be modified. While it is possible to modify the Object prototype, it is generally considered bad practice because most objects in JavaScript will inherit methods and properties from the Object prototype, and they may not expect the prototype to be modified.[52]
Functions as methods
Unlike many object-oriented languages, there is no distinction between a function definition and a method definition. Rather, the distinction occurs during function calling; when a function is called as a method of an object, the function's local this keyword is bound to that object for that invocation.
Functional
A function is first-class; a function is considered to be an object. As such, a function may have properties and methods, such as .call() and .bind().[53] A nested function is a function defined within another function. It is created each time the outer function is invoked. In addition, each nested function forms a lexical closure: The lexical scope of the outer function (including any constant, local variable, or argument value) becomes part of the internal state of each inner function object, even after execution of the outer function concludes.[54] JavaScript also supports anonymous functions.

Delegative
JavaScript supports implicit and explicit delegation.

Functions as roles (Traits and Mixins)
JavaScript natively supports various function-based implementations of Role[55] patterns like Traits[56][57] and Mixins.[58] Such a function defines additional behavior by at least one method bound to the this keyword within its function body. A Role then has to be delegated explicitly via call or apply to objects that need to feature additional behavior that is not shared via the prototype chain.
Object composition and inheritance
Whereas explicit function-based delegation does cover composition in JavaScript, implicit delegation already happens every time the prototype chain is walked in order to, e.g., find a method that might be related to but is not directly owned by an object. Once the method is found it gets called within this object's context. Thus inheritance in JavaScript is covered by a delegation automatism that is bound to the prototype property of constructor functions.
Miscellaneous
JS is a zero-index language.

Run-time environment
JavaScript typically relies on a run-time environment (e.g., a web browser) to provide objects and methods by which scripts can interact with the environment (e.g., a web page DOM). These environments are single-threaded. JavaScript also relies on the run-time environment to provide the ability to include/import scripts (e.g., HTML <script> elements). This is not a language feature per se, but it is common in most JavaScript implementations. JavaScript processes messages from a queue one at a time. JavaScript calls a function associated with each new message, creating a call stack frame with the function's arguments and local variables. The call stack shrinks and grows based on the function's needs. When the call stack is empty upon function completion, JavaScript proceeds to the next message in the queue. This is called the event loop, described as "run to completion" because each message is fully processed before the next message is considered. However, the language's concurrency model describes the event loop as non-blocking: program input/output is performed using events and callback functions. This means, for instance, that JavaScript can process a mouse click while waiting for a database query to return information.[59]
Variadic functions
An indefinite number of parameters can be passed to a function. The function can access them through formal parameters and also through the local arguments object. Variadic functions can also be created by using the bind method.
Array and object literals
Like many scripting languages, arrays and objects (associative arrays in other languages) can each be created with a succinct shortcut syntax. In fact, these literals form the basis of the JSON data format.
Regular expressions
JavaScript also supports regular expressions in a manner similar to Perl, which provide a concise and powerful syntax for text manipulation that is more sophisticated than the built-in string functions.[60]
Promises
JavaScript also supports promises, which are a way of handling asynchronous operations. There is a built-in Promise object that gives access to a lot of functionalities for handling promises, and defines how they should be handled. It allows one to associate handlers with an asynchronous action's eventual success value or failure reason. This lets asynchronous methods return values like synchronous methods: instead of immediately returning the final value, the asynchronous method returns a promise to supply the value at some point in the future. Recently, combinator methods were introduced in the JavaScript specification, which allows developers to combine multiple JavaScript promises and do operations on the basis of different scenarios. The methods introduced are: Promise.race, Promise.all, Promise.allSettled and Promise.any.
Vendor-specific extensions
Historically, some JavaScript engines supported these non-standard features:

conditional catch clauses (like Java)
array comprehensions and generator expressions (like Python)
concise function expressions (function(args) expr; this experimental syntax predated arrow functions)
ECMAScript for XML (E4X), an extension that adds native XML support to ECMAScript (unsupported in Firefox since version 21[61])

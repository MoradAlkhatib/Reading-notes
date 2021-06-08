# Images in HTML
In the beginning, the Web was just text, and it was really quite boring.
Fortunately, it wasn't too long before the ability to embed images (and other more interesting types of content) inside web pages was added. There are other types of multimedia to consider, but it is logical to start with the humble <img> element, used to embed a simple image in a webpage. In this article we'll look at how to use it in depth, including the basics,
annotating it with captions using <figure>, and detailing how it relates to CSS background images.
  How do we put an image on a webpage?
In order to put a simple image on a webpage, we use the <img> element. This is an empty element (meaning that it has no text content or closing tag) that requires a minimum of one attribute to be useful — src (sometimes spoken as its full title, source). The src attribute contains a path pointing to the image you want to embed in the page, 
  which can be a relative or absolute URL, in the same way as href attribute values in <a> elements.
  Warning: Most images are copyrighted. Do not display an image on your webpage unless:

You own the image.
You have received explicit, written permission from the image owner.
You have ample proof that the image is, in fact, in the public domain.

Copyright violations are illegal and unethical. In addition, never point your src attribute at an image hosted on someone else's website that you don't have permission to link to. This is called "hotlinking". Again, stealing someone's bandwidth is illegal. It also slows down your page,
  leaving you with no control over whether the image is removed or replaced with something embarrassing.
  So, why would you ever see or need alt text? It can come in handy for a number of reasons:

The user is visually impaired, and is using a screen reader to read the web out to them. In fact, having alt text available to describe images is useful to most users.
As described above, the spelling of the file or path name might be wrong.
The browser doesn't support the image type. Some people still use text-only browsers, such as Lynx, which displays the alt text of images.
You may want to provide text for search engines to utilize; for example, search engines can match alt text with search queries.
Users have turned off images to reduce data transfer volume and distractions. This is especially common on mobile phones, and in countries where bandwidth is limited or expensive.
What exactly should you write inside your alt attribute? It depends on why the image is there in the first place. In other words, what you lose if your image doesn't show up:

Decoration. You should use CSS background images for decorative images, but if you must use HTML, add a blank alt="". If the image isn't part of the content, a screen reader shouldn't waste time reading it.
Content. If your image provides significant information, provide the same information in a brief alt text – or even better, in the main text which everybody can see. Don't write redundant alt text. How annoying would it be for a sighted user if all paragraphs were written twice in the main content? If the image is described adequately by the main text body, you can just use alt="".
Link. If you put an image inside <a> tags, to turn an image into a link, you still must provide accessible link text. In such cases you may, either, write it inside the same <a> element, or inside the image's alt attribute – whichever works best in your case.
Text. You should not put your text into images. If your main heading needs a drop shadow, for example, use CSS for that rather than putting the text into an image. However, If you really can't avoid doing this, you should supply the text inside the alt attribute.
Essentially, the key is to deliver a usable experience, even when the images can't be seen. This ensures all users are not missing any of the content. Try turning off images in your browser and see how things look. You'll soon realize how helpful alt text is if the image cannot be seen.
  
 # CSS Text
  
  Text Color
The color property is used to set the color of the text. The color is specified by:

a color name - like "red"
a HEX value - like "#ff0000"
an RGB value - like "rgb(255,0,0)"
Look at CSS Color Values for a complete list of possible color values.

The default text color for a page is defined in the body selector.
  Text Color and Background Color
In this example, we define both the background-color property and the color property:


  

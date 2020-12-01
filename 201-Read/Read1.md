## HTML Describes the Structure of Pages
 - HTML consists of tag elements, usually
It consists of two tags: an opening tag and a closing tag. (Close tag
Contains an additional slash.) Each HTML element that tells the browser
Something about the information that lies between the opening and
Closing signs.
```
<html>
<body>
 <h1>This is the Main Heading</h1>
 <p>This text might be an introduction to the rest of
 the page. And if the page is a long one it might
 be split up into several sub-headings.<p>
 <h2>This is a Sub-Heading</h2>
 <p>Many long articles have sub-headings so to help
 you follow the structure of what is being written.
 There may even be sub-sub-headings (or lower-level
 headings).</p>
 <h2>Another Sub-Heading</h2>
 <p>Here you can see another sub-heading.</p>
</body>
</html>
````
> Opening Tag
```
<p>
left-angle bracket
(less-than sign)
RIGHT-angle bracket
(MORE-than sign)
Ch
```
> Closing Tag
```
</p>
left-angle bracket
(less-than sign)
RIGHT-angle bracket
(MORE-than sign)
Forward Slash
```
`<div>`
The `<div>`element allows you to group a group of items together into a single block at the block level.
What does the container allow you to do?
> DOCTYPES tell browsers which version of HTML you
are using.
>  You can add comments to your code between the
`<!-- and -->` markers.
> The id and class attributes allow you to identify
particular elements.
 > The `<div>` and `<span>` elements allow you to group
block-level and inline elements together.
 `<iframes>` cut windows into your web pages through
which other pages can be displayed.
> The `<meta>` tag allows you to supply all kinds of
information about your web page.
>  Escape characters are used to include special
characters in your pages such as `<, >,` and .
------
 - It's important to understand who your target audience
is, why they would come to your site, what information
they want to find and when they are likely to return.
-  Site maps allow you to plan the structure of a site.
X Wireframes allow you to organize the information that
will need to go on each page.
-  Design is about communication. Visual hierarchy helps
visitors understand what you are trying to tell them.
-  You can differentiate between pieces of information
using size, color, and style.
- You can use grouping and similarity to help simplify
the information you present.
---
The new HTML5 elements indicate the purpose of
different parts of a web page and help to describe
its structure.
> The new elements provide clearer code (compared
with using multiple `<div>` elements).
> Older browsers that do not understand HTML5
elements need to be told which elements are
block-level elements.
> To make HTML5 elements work in Internet Explorer 8
(and older versions of IE), extra JavaScript is needed,
which is available free from Google.
 # JS :
 How do write a script for a web page?
 It is best to keep JavaScript code in its own JavaScript
file. JavaScript files are text files (like HTML pages and
CSS style sheets), but they have the . j s extension.
The HTML `<script> element is used in HTML pages`
to tell the browser to load the JavaScript file (rather like
the `<link>` element can be used to load a CSS file).
If you view the source code of the page in the browser,
the JavaScript will not have changed the HTML,
because the script works with the model of the web
page that the browser has created.
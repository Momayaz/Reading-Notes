# How we manage the code content to creat a correct and perfect code.
* HTML pages are text documents.
* X HTML uses tags (characters that sit inside angled
* brackets) to give the information they surround special
meaning.
* X Tags are often referred to as elements.
* X Tags usually come in pairs. The opening tag denotes
the start of a piece of content; the closing tag denotes
the end.
* X Opening tags can carry attributes, which tell us more
about the content of that element.
* X Attributes require a name and a value.
* X To learn HTML you need to know what tags are
available for you to use, what they do, and where they
can go.
## Adding HTML5 Audio to Your Pages
<audiosrc="audio/test-audio.ogg"
 controls autoplay>
 to give <audio src="audio/test-audio.ogg"
 controls autoplay>
 * Flash allows you to add animations, video and audio to
the web.
* Flash is not supported on iPhone or iPad.
* HTML5 introduces new <video> and <audio>
elements for adding video and audio to web pages, but
these are only supported in the latest browsers.
* Browsers that support the HTML5 elements do not
all support the same video and audio formats, so you
need to supply your files in different formats to ensure
that everyone can see/hear them.
## CSS Associates Style rules with HTML elements

 Using Internal CSS
You can also include CSS rules
within an HTML page by placing
them inside a <styl e> element,
which usually sits inside the
<head > element of the page.
The < style > element should use
the type attribute to indicate
that the styles are specified in
CSS. The value should be text/
css.
When building a site with more
than one page, you should use
an external CSS style sheet. This:
● Allows all pages to use the
same style rules (rather than
repeating them in each page).
● Keeps the content separate
from how the page looks.
● Means you can change the
styles used across all pages
by altering just one file
(rather than each individual
page).
 * CSS treats each HTML element as if it appears inside
its own box and uses rules to indicate how that
element should look.
* Rules are made up of selectors (that specify the
elements the rule applies to) and declarations (that
indicate what these elements should look like).
* Different types of selectors allow you to target your
rules at different elements.
* Declarations are made up of two parts: the properties
of the element that you want to change, and the values
of those properties. For example, the font-family
property sets the choice of font, and the value arial
specifies Arial as the preferred typeface.
* CSS rules usually appear in a separate document,
although they may appear within an HTML page.

* Every color on a computer screen is created by mixing amounts of red,
green, and blue. To find the color you want, you can use a color picker.
Understanding Color
Computer monitors are made
up of thousands of tiny squares
called pixels (if you look very
closely at your monitor you
should be able to see them).
When the screen is not turned
on, it's black because it's not
emitting any light. When it's
on, each pixel can be a different
color, creating a picture.
The color of every pixel on the
screen is expressed in terms of
a mix of red, green, and blue —
just like on a television screen.

* Superscript &
Subscrip
<sup >
The <su p> element is used
to contain characters that
should be superscript such
as the suffixes of dates or
mathematical concepts like
raising a number to a power such
as 22
.
<su b>
The <su b> element is used to
contain characters that should
be subscript. It is commonly
used with foot notes or chemical
formulas such as H2
* <b r />
As you have already seen, the
browser will automatically show
each new paragraph or heading
on a new line. But if you wanted
to add a line break inside the
middle of a paragraph you can
use the line break tag <b r />.
* <h r />
To create a break between
themes — such as a change of
topic in a book or a new scene
in a play — you can add a
horizontal rule between sections
using the <h r /> tag.
* <str ong>
The use of the <st rong>
element indicates that its
content has strong importance.
For example, the words
contained in this element might
be said with strong emphasis.
By default, browsers will show
the contents of a <stro ng>
element in bold.
* <e m>
The <e m> element indicates
emphasis that subtly changes
the meaning of a sentence.
By default browsers will show
the contents of an <e m> element
in italic.
* <bloc kquote>
The <bloc kquote> element is
used for longer quotes that take
up an entire paragraph. Note
how the < p> element is still
used inside the <block quote>
element.
Browsers tend to indent the
contents of the <block quote>
element, however you should not
use this element just to indent a
piece of text — rather you should
achieve this effect using CSS. 
* <q >
The < q> element is used for
shorter quotes that sit within
a paragraph. Browsers are
supposed to put quotes around
the <q > element, however
Internet Explorer does not —
therefore many people avoid
using the <q > element.
* The <tabl e> element is used to add tables to a web
page.
* A table is drawn out row by row. Each row is created
with the <tr > element.
* Inside each row there are a number of cells
represented by the < td> element (or < th> if it is a
header).
* You can make cells of a table span more than one row
or column using the rowspan and colspan attributes.
* For long tables you can split the table into a <th ead>,
<t body>, and <tf oot>.
<in put>
type="password"
When the type attribute has
a value of password it creates
a text box that acts just like a
single-line text input, except
the characters are blocked out.
They are hidden in this way so
that if someone is looking over
the user's shoulder, they cannot
see sensitive data such as
passwords.
________________
java script
A script is a series of instructions that a computer can follow one-by-one. Each individual instruction or step is known as a statement. Statements should end with a semicolon.
COMMENTS
You should write comments to explain what your code does. They help make your code easier to read and understand. This can help you and others who read your code.
what is VARIABLE?
A script will have to temporarily store the bits of information it needs to do its job. It can store this data in variabls
 var 
 ![image2](./img/image-read2-2.jpg)
 _______________
 ![image1](./img/image-read2-1.jpg)

Decisions and Loops
 loop 

also in java script Conditional statements allow your code to make decisions about what to do next.
Comparison operators (===, ! ==, ==, ! =, <, >, <=, =>) are used to compare two operands.
Why good commit messages matter??
If you browse the log of any random Git repository, you will probably find its commit messages are more or less a mess.
example $ git log --oneline -5 --author cbeams --before "Fri Mar 26 2009"
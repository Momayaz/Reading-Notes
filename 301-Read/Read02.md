# jQuery, Events, and The DOM
## JQuery
JQuery offers a simple way to achieve a variety of common JavaScript tasks quickly and consistently, across all major browsers and without any fallback code needed. As you will see, jQuery is powerful when combined with traditional JavaScript techniques, but you need to understand JavaScript to make full use of jQuery. SELECT ELEMENTS PERFORM TASKS HANDLE EVENTS

It is simpler to access jQuery's methods let you jQuery includes methods elements using jQuery's update the DOM tree, that allow you to attach CSS-style selectors than it animate elements into event listeners to selected is using DOM queries. The and out of view, and loop elements without having selectors are also more through a set of elements, to write any tailback code powerful and flexible. all in one line of code. to support older browsers.
```
 $(' :header').addClass('headline'); 
  $(' l i :lt(3) ').hide(). fadeln(lSOO); 
  $('li').on('click', function() { $(this) . remove(); } ) ; 
```
1. The first line selects all of the -

headings, and adds a value of headline to their cl ass attributes.
2. The second line selects the first three list items and does two things:

* The elements are hidden (in order to allow the next step).
* The elements fade into view
3. The last three lines of the script set an event listener on each of the elements. When a user clicks on one, it triggers an anonymous function to remove that element from the page.
jQuery's motto is "Write less, do more," because it allows you to achieve the same goals but in fewer lines of code than you would need to write with plain JavaScript. 
In plain JavaScript, if you wanted to do the same thing to several elements, you would need to write code to loop through all of the elements you selected.

With jQuery, when a selector returns multiple elements, you can update all of them using the one method. There is no need to use a loop.

In this code, the same value is added to the cl ass attribute for all of the elements that are found using the selector. It doesn't matter if there are one or many.
```
$('li em') .addClass('seasonal '); 
$( 'li .hot') .addClass('favorite'); 
```
The .ready() method offers a way to run JavaScript code as soon as the page's Document Object Model (DOM) becomes safe to manipulate. This will often be a good time to perform tasks that are needed before the user views or interacts with the page, for example to add event handlers and initialize plugins. When multiple functions are added via successive calls to this method, they run when the DOM is ready in the order in which they are added. As of jQuery 3.0, jQuery ensures that an exception occuring in one handler does not prevent subsequently added handlers from executing.

Browsers also provide the load event on the window object. When this event fires it indicates that all assets on the page have loaded, including images. This event can be watched in jQuery using $( window ).on( "load", handler ). In cases where code relies on loaded assets (for example, if the dimensions of an image are required), the code should be placed in a handler for the load event instead.

The • on () method is used to handle all events. Behind the scenes, jQuery handles all of the cross-browser issues you saw in the last chapter.

When a page loads jQuery from a CDN, you will often see a syntax like the one shown below. It starts with a 
```
<script>`` tag that tries to load the jQuery file from the CDN. But note that the URL for the script starts with two forward slashes (not http:). liillfill LOADING JQUERY FROM A CDN This is known as a protocol relative URL. If the user is looking at the current page through https, then they will not see an error that tells them there are unsecure items on the page. Note: This does not work locally with the f i l e:// protocol. This is often followed by a second <script>``
```
 tag that contains a logical operator, which checks to see if jQuery has loaded. If it has not loaded, the browser tries to load the jQuery script from the same server as the rest of the website.
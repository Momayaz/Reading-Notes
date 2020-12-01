# Jquery

jQuery is a fast, small, and feature-rich JavaScript library. It makes things like HTML document traversal and manipulation, event handling, and animation much simpler.

First, let's take a look at an example HTML manipulation with JavaScript. To get the element with the id="start" and change its html to "Go" we will need to do the following:


```var el = document.getElementById("start");
el.innerHTML = "Go";
To do the same manipulation with jQuery, we need just a single line of code:

$("#start").html("Go");
```
____

You can download a copy of the jQuery library from www.jquery.com, or, as an alternative, you can include it from a CDN (Content Delivery Network), like Google or Microsoft. We will use the CDN from the official jQuery website. To start using jQuery, we first need to add it to the head of our HTML document using the script tag:

```
<!DOCTYPE html>
<html>
    <head>
        <title>Page Title</title>
        <script src="https://code.jquery.com/jquery-3.1.1.js"></script>
    </head>
    <body>
    </body>
</html>
```

jQuery is a JavaScript library, so it has the .js file extension.

It is a good practice to wait for the HTML document to be fully loaded and ready before working with it. For that we use the ready event of the document object:
```
$(document).ready(function() {
   // jQuery code goes here
});
```
The $ is used to access jQuery. From here, the code accesses the document object and defines a function to be called when the document's ready event is fired. This prevents any jQuery code from running before the document is finished loading. Since the code above is used in almost all cases when using jQuery, there is a handy shortcut for writing it:
```
$(function() {
   // jQuery code goes here
});
```
This code performs the same task as the longer code above.

Now, having the jQuery library in our head section and having defined the document ready event, we can start our first jQuery manipulation! Let's change the content of the div element. The HTML:
```
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
    <script src="https://code.jquery.com/jquery-3.1.1.js"></script>
  </head>
  <body>
    <div id="start">Start</div>
  </body>
</html>
```

The JavaScript:
```
$(function() {
  $("#start").html("Go!");
});
```
This changes the HTML of the element with id="start" to "Go!".
____

## ummary
The following jQuery methods are available to get and set content and attributes of selected HTML elements: text() sets or returns the text content of selected elements. html() sets or returns the content of selected elements (including HTML markup). val() sets or returns the value of form fields. attr() sets or returns the value of attributes. removeAttr() removes the specified attribute.

Write code and test every method at least one time.

Adding Content

As we have seen in the previous lessons, the html() and text() methods can be used to get and set the content of a selected element. However, when these methods are used to set content, the existing content is lost. jQuery has methods that are used to add new content to a selected element without deleting the existing content: append() inserts content at the end of the selected elements. prepend() inserts content at the beginning of the selected elements. after() inserts content after the selected elements. before() inserts content before the selected elements.

Adding Content

The append() method inserts content AT THE END of the selected HTML element. For example: HTML:
```
<p id="demo">Hi </p>
```
JS:
```
$(function() {
  $("#demo").append("David");
});
//Outputs "Hi David"
```
_____

## Manipulating CSS

The removeClass() method removes one or more class names from the selected elements. For example:
```
$("div").removeClass("red");
```
The code above removes the class "red" from the div element.

Again, multiple class names can be specified by separating them using spaces.

toggleClass()

The toggleClass() method toggles between adding/removing classes from the selected elements, meaning that if the specified class exists for the element, it is removed, and if it does not exist, it is added. To demonstrate this in action, we will handle a button click event to toggle a class. We will learn more about events and their syntax in the coming modules. HTML:
```
<p>Some text</p>
<button>Toggle Class</button>
```
CSS:
```
.red { 
  color:red; 
  font-weight: bold;
}
``
JS:
```
$(function() {
  $("button").click(function() {
    $("p").toggleClass("red");
  });
});


The code above toggles the class name "red" upon clicking the button.


_____________________

## Dimensions

The width() and height() methods can be used to get and set the width and height of HTML elements.

Let's set both the width and height of a div to 100px, as well as set a background color for it:

$("div").css("background-color", "red");
$("div").width(100);
$("div").height(100);
Dimensions

The width() and height() methods get and set the dimensions without the padding, borders and margins. The innerWidth() and innerHeight() methods also include the padding. The outerWidth() and outerHeight() methods include the padding and borders. Check out this image to understand how they work:

image

The following example demonstrates how the methods work: HTML:

<div></div>
CSS:
```
div {
  width: 300px;
  height: 100px;
  padding: 10px;
  margin: 20px;
  border: 3px solid blue;
  background-color: red;
  color: white;
}
```
JS:

```
$(function() {
  var txt = "";
  txt += "width: " + $("div").width() + " ";
  txt += "height: " + $("div").height() + "<br/>";
  txt += "innerWidth: " + $("div").innerWidth() + "  ";
  txt += "innerHeight: " + $("div").innerHeight() + "<br/>";
  txt += "outerWidth: " + $("div").outerWidth() + "  ";
  txt += "outerHeight: " + $("div").outerHeight();
    
  $("div").html(txt);
});
```

When you open any webpage in a browser, the HTML of the page is loaded and rendered visually on the screen. To accomplish this, the browser builds the Document Object Model (DOM) of that page, which is an object oriented model of its logical structure. The DOM of an HTML document can be represented as a nested set of boxes:

## image

The DOM represents a document as a tree structure where HTML elements are interrelated nodes in the tree. Nodes can have child nodes. Nodes on the same tree level are called siblings. jQuery traversing is the term used to describe the process of moving through the DOM and finding (selecting) HTML elements based on their relation to other elements.

jQuery makes it easy to traverse the DOM and work with HTML elements.

DOM Traversal

For example, consider the HTML represented by the following structure:

image

The element is the parent of and an ancestor of everything below it. The element is the parent of the

and elements. The
and elements are child elements of the element and descendants of . The
and elements are siblings (they share the same parent).
Summary An ancestor is a parent, grandparent, great-grandparent, and so on. A descendant is a child, grandchild, great-grandchild, and so on. Siblings share the same parent.

Understanding the relationship between the DOM elements is important to be able to traverse the DOM correctly.

DOM Traversal

jQuery has many useful methods for DOM traversal. The parent() method returns the direct parent element of the selected element. For example: HTML:
```
<div> div element
  <p>paragraph</p> 
</div>
```
JS:
```
var e = $("p").parent();
e.css("border", "2px solid red");
```
The code above selects the parent element of the paragraph and sets a red border for it.

The parent() method can only traverse a single level up the DOM tree. To get all ancestors of the selected element you can use the parents() method. For example: HTML:
```
<body>  body
  <div style="width:300px;"> div
    <ul> ul
      <li> li
        <p>paragraph</p>
      </li>
    </ul>   
  </div>
</body>
```
JS:
```
$(function() {
  var e = $("p").parents();
  e.css("border", "2px solid red");
});
```
The code above sets a red border for all parents of the paragraph.

Some of the most used traversal methods are presented below:

image

DOM Traversal

The eq() method can be used to select a specific element from multiple selected elements. For example, if the page contains multiple div elements and we want to select the third one:

$("div").eq(2);
The index numbers start at 0, so the first element will have the index number 0.

Remove Elements

We remove selected elements from the DOM using the remove() method.For example: HTML:
```
<p style="color:red">Red</p>
<p style="color:green">Green</p>
<p style="color:blue">Blue</p>
```
JS:
```
$("p").eq(1).remove();
```
This removes Green, the second paragraph element. You can also use the remove() method on multiple selected elements, for example $("p").remove() removes all paragraphs.

The jQuery remove() method removes the selected element(s), as well as its child elements.

Removing Content

The empty() method is used to remove the child elements of the selected element(s). For example: HTML:
```
   <p style="color:red">Red</p>
   <p style="color:green">Green</p>
   <p style="color:blue">Blue</p>
</div>
```
CSS:
```
div {
  background-color: aqua;
  width: 300px;
  height: 200px;
}
```
JS:
```
$("div").empty();
```
This removes all the three child elements of the div, leaving it empty.

Handling Events

JQuery provides an efficient way to handle events. Events occur when the user performs an action, such as clicking an element, moving the mouse, or submitting a form. When an event occurs on a target element, a handler function is executed. For example, let's say we want to handle the click event on an element with id="demo" and display the current date when the button is clicked. Using pure JavaScript, the code looks like:

var x = document.getElementById("demo");
x.onclick = function () {
  document.body.innerHTML = Date();
}
The same event could be handled using jQuery with the following code:

$("#demo").click(function() {
  $("body").html(Date());
});
As you can see, the jQuery code is shorter and easier to read and write. Notice, that the event name is provided without the "on" prefix (i.e., onclick in JavaScript is click in jQuery)

The function that is executed when an event is fired is called the event handler.

Common Events

The following are the most commonly used events: Mouse Events: click occurs when an element is clicked. dblclick occurs when an element is double-clicked. mouseenter occurs when the mouse pointer is over (enters) the selected element. mouseleave occurs when the mouse pointer leaves the selected element. mouseover occurs when the mouse pointer is over the selected element.

Keyboard Events: keydown occurs when a keyboard key is pressed down. keyup occurs when a keyboard key is released.

Form Events: submit occurs when a form is submitted. change occurs when the value of an element has been changed. focus occurs when an element gets focus. blur occurs when an element loses focus.

Document Events: ready occurs when the DOM has been loaded. resize occurs when the browser window changes size. scroll occurs when the user scrolls in the specified element.

As an example, let's change the content of a div when the user types in an input field. To do that, we need to handle the keydown event, which occurs when a key on the keyboard is pressed: HTML:
```
 <input type="text" id="name" />
<div id="msg"></div>
```
JS:
```
$("#name").keydown(function() {
  $("#msg").html($("#name").val());
});
```
The code above handles the keydown event for the element with id="name" and assigns the content of the div with id="msg" the value of the input field.

The code above handles the keydown event for the element with id="name" and assigns the content of the div with id="msg" the value of the input field.

Another way to handle events in jQuery is by using the on() method. The on() method is used to attach an event to the selected element. For example:
```
$( "p" ).on( "click", function() {
  alert("clicked");
});
```
As you can see, the event name is passed as the first argument to the on() method. The second argument is the handler function.

The on() method is useful for binding the same handler function to multiple events. You can provide multiple event names separated by spaces as the first argument. For example, you could use the same event handler for the click and dblclick event

off()

You can remove event handlers using the off() method. For example:
```
$("div").on("click", function() { 
  alert('Hi there!'); 
  $("div").off("click");
}); 
```
The argument of the off() method is the event name you want to remove the handler for.

The Event Object

Every event handling function can receive an event object, which contains properties and methods related to the event: pageX, pageY the mouse position (X & Y coordinates) at the time the event occurred, relative to the top left of the page. type the type of the event (e.g. "click"). which the button or key that was pressed. data any data that was passed in when the event was bound. target the DOM element that initiated the event. preventDefault() prevent the default action of the event (e.g., following a link). stopPropagation() Stop the event from bubbling up to other elements.

You can check out our JavaScript course for more information on event properties.

For example, let’s handle the click event on an element and prevent it from following the link provided in the href attribute: HTML:
```
<a href="https://www.sololearn.com">Click me</a>
```
JS:
```
$( "a" ).click(function(event) {
  alert(event.pageX);
  event.preventDefault();
});
```
The code above alerts the mouse position at the time of the click and prevents following the link.

As you can see, the event object is passed to the event handler function as an argument.

Trigger Events

We can also trigger events programmatically using the trigger() method. For example, you can trigger a click event without the user actually clicking on an element:
```
$("div").click(function() {
   alert("Clicked!");
});
```
```
$("div").trigger("click");
```
This code triggers the click event for the selected element.

The trigger() method cannot be used to mimic native browser events, such as clicking on a file input box or an anchor tag. Only events in the jQuery event system can be handled.

To-Do List

Let's create a To-Do list project using the concepts we have learned. The To-Do list will be able to add new items to a list, as well as remove existing items. First, we create the HTML:

```
<h1>My To-Do List</h1>
<input type="text" placeholder="New item" />
<button id="add">Add</button>
<ol id="mylist"></ol>
```
Clicking the button should add the value of the input field to our

list.
Now, having the HTML ready, we can start writing our jQuery code. First, we handle the click event for the button:
```
$(function() {
  $("#add").on("click", function() {
    //event handler
  });
});
```
Inside the event handler we select the value of the input field and create a new

element, adding it to the list:
```
var val = $("input").val();
if(val !== '') {
  var elem = $("<li></li>").text(val);
  $(elem).append("<button class='rem'>X</button>");
  $("#mylist").append(elem);
  $("input").val(""); //clear the input
};
```

The code above takes the value of the input field, assigns it to the val variable. The if statement checks that the value is not blank and then creates a new

element. A button for removing it is added, after which the newly created element is added to the
list. Here's the complete code in action:
```
$(function() {
  $("#add").on("click", function() {
    var val = $("input").val();
    if(val !== '') {
      var elem = $("<li></li>").text(val);
      $(elem).append("<button class='rem'>X</button>");
      $("#mylist").append(elem);
      $("input").val("");
    }
  });
});
```
The remove button is not working yet. We will handle it in the next section!

All that is left to do is handle the click event on the class="rem" button and remove the corresponding

element from the list.
```
$(".rem").on("click", function() {
  $(this).parent().remove();
});
```
Remember, this is the current object. The code above removes the parent of the current object, which in our case is the parent of the remove button, the

element.
The complete code:
```
$(function() {
  $("#add").on("click", function() {
    var val = $("input").val();
    if(val !== '') {
     var elem = $("<li></li>").text(val);
     $(elem).append("<button class='rem'>X</button>");
     $("#mylist").append(elem);
     $("input").val("");
     $(".rem").on("click", function() {
      $(this).parent().remove();
     });
    }
  });
});
```
The To-Do List was just a short demonstration of how to handle events and build a simple project.

Hide/Show

jQuery has some easy-to-implement effects to create animations. The hide() and show() methods are used to hide and show the selected elements. The toggle() method is used to toggle between hiding and showing elements. For example:
```
$(function() {
  $("p").click(function() {
    $("div").toggle();
  });
});
```
The hide/show/toggle methods can take an optional argument, speed, which specifies the animation speed in milliseconds. For example, let's pass 1000 millisecond as the speed argument to the toggle() method:
```
$(function() {
  $("p").click(function() {
    $("div").toggle(1000);
  });
});
```
The hide/show/toggle methods can also take a second optional parameter callback, which is a function to be executed after the animation completes.

Fade In/Out

Similar to the hide/show methods, jQuery provides the fadeIn/fadeOut methods, which fade an element in and out of visibility. Just like the toggle() method switches between hiding and showing, the fadeToggle() method fades in and out. Let's see fadeToggle() in action:
```
$(function() {
  $("p").click(function() {
    $("div").fadeToggle(1000);
  });
});
```
Just like toggle(), fadeToggle() takes two optional parameters: speed and callback.

Another method used for fading is fadeTo(), which allows fading to a given opacity (value between 0 and 1). For example: $("div").fadeTo(1500, 0.7);

____
## Animation Queue

By default, jQuery comes with queue functionality for animations. This means that if you write multiple animate() calls one after another, jQuery creates an "internal" queue for these method calls. Then it runs the animate calls one-by-one. For example:
```
var div = $("div");
div.animate({opacity: 1});
div.animate({height: '+=100px', width: '+=100px', top: '+=100px'}, 500);
div.animate({height: '-=100px', width: '-=100px', left: '+=100px'}, 500);
div.animate({height: '+=100px', width: '+=100px', top: '-=100px'}, 500);
div.animate({height: '-=100px', width: '-=100px', left: '-=100px'}, 500);
div.animate({opacity: 0.5});
```

Each animate() method call will run one after another. Remember, to manipulate the position of elements, you need to set the CSS position property of the element to relative, fixed, or absolute.

The animate() method, just like the hide/show/fade/slide methods, can take an optional callback function as its parameter, which is executed after the current effect is finished.

Drop-Down Menu

Let's create a simple drop-down menu that will open upon clicking on the menu item. HTML:
```
<div class="menu">
  <div id="item">Drop-Down</div>
  <div id="submenu">
    <a href="#">Link 1</a>
    <a href="#">Link 2</a>
    <a href="#">Link 3</a>
  </div>
</div>
```
JS:
```
$("#item").click(function() {
  $("#submenu").slideToggle(500);
}); 
```

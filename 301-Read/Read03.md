# Javascript Templating Language and Engine— Mustache.js with Node and Express
## Javascript Templating
Javascript templating is a fast and efficient technique to render client-side view templates with Javascript by using a JSON data source. The template is HTML markup, with added templating tags that will either insert variables or run programming logic. The template engine then replaces variables and instances declared in a template file with actual values at runtime, and convert the template into an HTML file sent to the client.

## Mustache
Mustache is a logic-less template syntax. It can be used for HTML, config files, source code — anything. It works by expanding tags in a template using values provided in a hash or object. It is often referred to as “logic-less” because there are no if statements, else clauses, or for loops. Instead, there are only tags. Some tags are replaced with a value, some nothing, and others a series of values.

Mustache.render(“Hello, {{name}}”, { name: “Sherlynn” }); // returns: Hello, Sherlynn

## Properties for the Parent
(flex container) display This defines a flex container; inline or block depending on the given value. It enables a flex context for all its direct children.

.container { display: flex; /* or inline-flex */ }

flex-direction This establishes the main-axis, thus defining the direction flex items are placed in the flex container. Flexbox is (aside from optional wrapping) a single-direction layout concept. Think of flex items as primarily laying out either in horizontal rows or vertical columns.

.container { flex-direction: row | row-reverse | column | column-reverse; }

row (default): left to right in ltr; right to left in rtl row-reverse: right to left in ltr; left to right in rtl column: same as row but top to bottom column-reverse: same as row-reverse but bottom to top

## FLEXBOX
* flex-start: Items align to the left side of the container.
* flex-end: Items align to the right side of the container.
* center: Items align at the center of the container.
* space-between: Items display with equal spacing between them.
* space-around: Items display with equal spacing around them.
**For example, justify-content: flex-end; will move the frog to the right.**
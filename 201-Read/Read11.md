
# Charts
Charts are far better for displaying data visually than tables and have the added benefit that no one is ever going to press-gang them into use as a layout tool. They’re easier to look at and convey data quickly, but they’re not always easy to create.
## how to use chart
1. Setting up: in this step we need to download charts.js like;
 Copy the Chart.min.js out of the unzipped folder and into the directory you’ll be working in. Then create a new html page and import the script:
 ``` html 
 <!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <title>Chart.js demo</title>
        <script src='Chart.min.js'></script>
    </head>
    <body>
    </body>
</html>
```
The next  step is to deawing a line chart;
we need to do is create a canvas element in our HTML in which Chart.js can draw our chart. So add this to the body of our HTML page:
``` css

<canvas id="buyers" width="600" height="400"></canvas>
```
Next, we need to write a script that will retrieve the context of the canvas, so add this to the foot of your body element:
``` css

<script>
    var buyers = document.getElementById('buyers').getContext('2d');
    new Chart(buyers).Line(buyerData);
</script>
```
Then we have to drawing a pie chart and drawing a bar chart, finally we see the results on our browser.
___________
How to put canvas in your html? Canvas tag is not like image tag, as canvas tag needs opening and closing like; 
```html
<canvas id="stockGraph" width="150" height="150">
  current stock price: $3.15 + 0.15
</canvas>

<canvas id="clock" width="150" height="150">
  <img src="images/clock.png" width="150" height="150" alt=""/>
</canvas>
```
________
## How to apply color 
it is so easy all of we need is to add these elemnts, so that we can apply color;
```
function draw() {
  var ctx = document.getElementById('canvas').getContext('2d');
  for (var i = 0; i < 6; i++) {
    for (var j = 0; j < 6; j++) {
      ctx.fillStyle = 'rgb(' + Math.floor(255 - 42.5 * i) + ', ' +
                       Math.floor(255 - 42.5 * j) + ', 0)';
      ctx.fillRect(j * 25, i * 25, 25, 25);
    }
  }

}
```
## drawing text;
we have to ways of appling text;
* The first one: fillText(text, x, y [, maxWidth])
Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.
* The second one :
strokeText(text, x, y [, maxWidth])
Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.
=======
# images:
## Centering images Using C,
whe use three elemnts to center any image:
1. display: block;
2. margin:0px auto;
like;
``` html
<p><img src="images/magnolia-medium.jpg"
 alt="Magnolia" class="align-center medium" />
 <b><i>Magnolia</i></b> is a large genus that
 contains over 200 flowering plant species. It
 is named after French botanist Pierre Magnol and,
 having evolved before bees appeared, the
 flowers were developed to encourage pollination
 by beetle.</p>
 ```
 ``` css
 img.align-center {
display: block;
margin: 0px auto;}
img.medium {
width: 250px;
height: 250px;}
```
_________
## background-repeat background-attachment
* reaprt.
* repeat-x.
* repeat-y.
* fixed.
* scroll.
_________
## Background Position background-position;
* left top
*  left center
*  left bottom
* center top
* center center
* center bottom
* right top
* right center
* right bottom
____________
## Analytics: Learning about your Visitors:

1. Signing Up
The Google Analytics service
relies on you signing up for an
account at:
www.google.com/analytics
The site will give you a piece of
tracking code which you need to
put on every page of your site.
2. How it Works
Every time someone loads a
page of your site, the tracking
code sends data to the Google
servers where it is stored.
Google then provides a webbased interface that allows you
to see how visitors use your site.
3. The Tracking Code
A tracking code is provided
by Google Analytics for each
website you are tracking. It
should appear just before the
closing ```</head>``` tag. The code
does not alter the appearance of
your web pages.
___________
## what is FTP?!
FTP  allows
you to transfer files across the
Internet from your computer to
the web server hosting your site. 
For example;

***FileZilla***

filezilla-project.org
Windows, Mac, Linux

***FireFTP***

fireftp.mozdev.org
Windows, Mac, Linux

***CuteFTP***

cuteftp.com
Windows, Mac

***SmartFTP***

smartftp.com
WIndows

***Transmit***

panic.com/transmit
Mac
_________
## For Flashing:
Since 2005, a number of factors have meant
that fewer websites are written in Flash or even
use elements of Flash in their pages.
![image17](/img/img17.png)
 and we have the development of flashing through aras
 ![image18](/img/img18.png).

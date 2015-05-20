# Intro to jQuery - Full Lecture

## SWBATS

***Students will be able to understand the fundamentals of jQuery and incorporate them into their projects***

+ Understand that Javascript provides a language to add behaviors to our web pages.
+ Include Javascript in their HTML using `<script>` tags with `src` and in-line Javascript.
+ Include jQuery in their web pages from a CDN host.
+ Understand that Javascript creates a Document Object Model where you can represent the HTML nodes and elements from Week 1 as "Objects" that you can manipulate.
+ Use `$` or `jQuery` and CSS Selectors to select an element from their page.
+ Call basic methods on those jQuery DOM elements.
+ Manipulate existing DOM elements through jQuery methods (change text, change properties).
+ Insert DOM and modify the page with methods like `append` and `prepend`.
+ Understand what a DOM Event is and how to add a handler for an event.


## Motivation/ Why Should You Care

jQuery is a powerful JavaScript library that can control all the magic you see on your page, from sliding menus to animations. [Beyonce](http://www.beyonce.com/) has some amazing jQuery on her page. Using Javascript and jQuery makes our pages interactive and awesome.

## Lesson  Plan

### Intro

+ So far, we've used HTML and CSS to structure and style our pages and present information to our users. However, it doesn't let our users interact with our page. Let's say we wanted part of our page to animate when a user clicks on it. What would we need to be able to do? 
  + First, say what the page should look like when it loads. 
  + Identify when a user clicks on a certain part of a page. 
  + Say what should happen after the user clicks. 

+ We can do this with Javascript, a programming language built to run in a web browser, and jQuery, a Javascript library that gives us some awesome functionality for manipulating the DOM. 

### The DOM

Before we can really dive into jQuery we need to understand the DOM. The DOM, stands for *Document Object Model* and it is a structural representation of our HTML in tree form. Like this:

<img src="https://s3.amazonaws.com/after-school-assets/jquery4.png">

+ Take a look at this image - these are all HTML elements that we know and love. 
+ This model enables us to modify the content and visual presentation on our HTML document with scripting languages such as jQuery (and plain JavaScript).
+ What kind of things can we do with JS + DOM?
  + Add/remove/hide/show HTML elements in the page
  + Add/remove/change HTML attributes
  + Add/remove/change CSS styles
  + Listen for key presses or mouse events upon Elements
  + Animate Elements

<img src="https://s3.amazonaws.com/after-school-assets/tumblr_mo32apssfq1r8lg7to1_500.jpg">

### jQuery Intro

+ We can use vanilla Javascript to manipulate the DOM, but it's a lot easier to use jQuery. 
+ So what is jQuery?
  + jQuery is a JavaScript library
+ What is a library?
  + A library is a  collection of code that extends the abilities and features of a core programming language, offering additional methods and often simplifying the process to build in that native language.
  + You can even look at the text file that makes up jQuery by navigating to `https://ajax.googleapis.com/ajax/libs/jquery/1.8.2/jquery.js` in your browser!
+ Why use jQuery?
  + Since it's just JavaScript, it works everywhere JavaScript does, and it's much simpler to write than vanilla Javascript!

### Setup

+ To setup a document to run jQuery we must link to the jQuery core library first, just like linking your HTML and CSS! Imagine that JavaScript is like a pet dog. On it’s own it knows how to eat, sleep, and play. Loading jQuery is like teaching the dog new tricks such as roll over, fetch, etc… Imagine what would happen if we gave the command for our dog to fetch before we had taught it this trick (linked to jQuery). Therefore, we always link to the jQuery core library first.
+ Inside your `<head></head>`, remote link: 
`<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.8.2/jquery.min.js"></script>`
  * This is hosted for us, just like Bootstrap. We can also download the files and include them with our project
+ Inside your `<head></head>`, local link (downloaded from jquery.com):
`<script src=”js/jquery-1.8.2.min.js"></script>`
+ Inside your `<head></head>`, both using local as fallback solution:

```html
<head>
  ... Other stuff that goes in between the head tags ...
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.8.2/jquery.min.js"></script>
  <script>window.jQuery || document.write('<script src="js/jquery-1.8.2.min.js"> <  \/script>')</script>
</head>
```

### Syntax, Selectors, and Methods

+ jQuery syntax 
+ Here is an example of the syntax for using a jQuery method
  + `$("selector").method(parameters);`
  + `$` refers to the jQuery object.
    + Wriing a `$` is like saying, 'hey, jQuery, wake up!'
+ `selector` asks jQuery to go out into the DOM (Document Object Model) web page and select an element(s). In jQuery we can use all of the familiar HTML tags and selectors we use in CSS yay!
  + Note that we always write our selectors in quotation marks.
+ `.method` these are various actions and commands attached to the jQuery object that allow us to do things like fade elements in an out or change the content of the DOM and much much more
+ `parameters` are options we can set for each method.
+ An example of real code:
  + `$('h1').css({'background':'yellow'});`
  + `$` refers to the jQuery object.
  + `h1` asks jQuery to go out into the DOM (Document Object Model) web page and select all `<h1>`.
  + `css` method applies some CSS upon the selected element(s).
  + `{'background':'yellow'}` changes the background color to yellow.
+ A few more examples of jQuery selectors:
  **Write these on the board and have students guess what they select**
  + Select Elements
    + `$('h1')` // all the h1s
  + Select ID
    + `$('#nav')` // all elements with the ID of `nav`
  + Select Class
    + `$('.celeb')` // all elements with the Class of `celeb`
  + Select Attribute
    + `$('a[href^=http://]')` // all `a` elements with a specific `href` value
  + Select Descendent(s)
    + `$('#nav li')` // any `li` that's nested inside an element with the ID of `nav`
  + Select Child(ren)
    + `$('#nav > li')` // any `li` directly inside an element with the ID of `nav`
  + Select Sibling(s)
    + `$('h3 + p')` // h3s and ps
  + Select by position
  + `$('li:eq(1)')` //selects the second list item



+ A few examples of jQuery methods
  + Effects
    + `animate()`, `fadeTo()`, `show()`, `hide()`,  `slideToggle()`
  + Events
    + `click()`, `hover()`, `focus()`, `blur()`, `keypress()`
  + Manipulation
    + `addClass()`, `clone()`, `empty()`, `attr()`, `val()`
  + Traversing
    + `eq()`, `each()`, `has()`, `closest()`, `find()`
+ If you want to do something to your DOM jQuery probably has a method for it. 
+ Note that to execute a method, you put `()` after it. That means, "hey, run this method now!"
+ YOU DO NOT HAVE TO MEMORIZE ALL OF THE METHODS
+ Having an idea of what possibilities are available is useful, and familiarizing yourself with some that you will use from day to day is useful, unless you’re a jQuery guru you probably will not memorize every method. Fortunately we can look them up and see their usage at sites like:
  + [API](http://api.jquery.com/)
  + [Documentation](http://docs.jquery.com/)
  + Or nifty [cheatsheets](http://oscarotero.com/jquery/)
  + [Overview](http://overapi.com/jquery)

### Using jQuery 

+ Set up steps for using jQuery in your websites:
  +  Include link to jQuery core library between your `<head>` tags:
   `<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.10.1/jquery.min.js"></script>`
  + Link to your custom js file
  `<script src=”./js/app.js"></script>`
  + Start your `app.js` with document ready command:

    ```js
    $(document).ready(function() {
       // your app code goes here.
    });
    ```

### Events

#### Document Ready
+ You’ll notice that here we are calling the ready method on the `$(document)` object and that ready function takes an argument that is another function. This happens a lot in jQuery. 
+ Our javascript files often get loaded before any other elements on our page. This can be dangerous if we want to access the DOM before it has loaded 
+ If we apply jQuery selectors before any DOM elements have loaded on our page then nothing will happen since those elements don't exist yet
+ Using Document Ready is the same as saying, "Okay, as soon as the page is done loading, apply all of our cool jQuery methods"

#### Click

+ One jQuery method that you will probably be using a lot is the `.click()` method.
+ The `.click()` method also takes a function as an argument - a function that describes what should be done when that particular part of the DOM is clicked. Here is an example (demo this in jsFiddle):

HTML:

```html
<button id="alert">Push to Alert</button>
```

JS:

```js
$(document).ready(function(){
  $('#alert').click(function(){
    alert('hello there');
  });
});
```

+ There's a lot happening here, so let's break it down step by step. 
  + First, we're calling our document ready method. 
  + Inside of our document ready function, we use the jQuery object `$` to select anything with the id (`#`) of `"alert"`. In this case, that's our button.
  + We call a method, `.click()`, which fires a function whenever the item is clicked on. 
 
+ We can get even fancier and include jQuery methods within the function. 
+ For instance - what if we want to add some text to our page every time the button is clicked? 
+ We can use a very handy jQuery append method. The append method will add HTML to any piece of the DOM indicated. 
  + For example if I add `<div id="alert-tracker"></div> `to my dom I can append “alert clicked!” every time the button is pushed and keep track of how many times the alert button has been pushed like this:

HTML:

```html
<button id="alert">Push to Alert</button>
```

JS:

```js
$(document).ready(function(){
  $('#alert').click(function(){
    alert('hello there');
    $('#alert-tracker').append("<p>alert clicked!</p>");
  });
});
```

+ Pretty cool, huh! 
+ Now go get some practice with the labs on Learn.co!

## Conclusion
jQuery is magic - it lets users interact with our pages in awesome ways and allows those pages to do awesome things.

## Hints and Hurdles
+ The `$` is like saying "hey jQuery, wake up. It's time for you to get to work"
+ Make sure the page is loaded using `$(document).ready()` before trying to hook jQuery up to the DOM

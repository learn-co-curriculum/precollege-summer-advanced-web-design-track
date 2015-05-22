# jQuery

## SWBATs

+ Understand the DOM (Document Object Model)
+ Understand how jQuery is just a *library* of JavaScript functions and that anything jQuery does you can do with plain JavaScript
+ Import and Initialize the jQuery library
+ Understand why you need to wait for the document to be ready
+ Use `$` and `jQuery` to access jQuery functionality
+ Use jQuery and CSS selectors to access HTML elements
+ Create, Read, Update, and Delete (CRUD) HTML elements using jQuery
+ Iterate through a jQuery Collection

## Motivation /Why Should You Car?

> jQuery is a fast, small, and feature-rich JavaScript library. It makes things like HTML document traversal and manipulation, event handling, animation, and Ajax much simpler with an easy-to-use API that works across a multitude of browsers. With a combination of versatility and extensibility, jQuery has changed the way that millions of people write JavaScript.
- jquery.com

In plainer English, jQuery is simply a library that makes things that are hard/annoying in JavaScript, like finding elements, really easy. It allows us to add/remove/change HTML and CSS with ease.

## Lesson Plan

### DOM

Before we dive into jQuery it makes sense to do a quick review of working the DOM. 
*Does anyone remember what DOM stands for?*
This stands for *document object model* and it is a structural representation of our HTML in tree form. Like this:
<img src="https://s3.amazonaws.com/after-school-assets/advanced_jquery2.png">
This model enables us to easily find elements and change their content, styles, and structure.

What kind of things can we do with JS/jQuery + DOM.
+ Add/remove/hide/show HTML elements in the page.
+ Add/remove/change HTML attributes.
+ Add/remove/change CSS styles.
+ Listen for key presses or mouse events on Elements
+ Create events in the page.

### jQuery Review

#### Installation

+ To set up a document to run jQuery we must link to the jQuery core library first! Imagine that JavaScript is like a pet dog. On it’s own it knows how to eat, sleep, and play. Loading jQuery is like teaching the dog new tricks such as roll over, fetch, etc… Imagine what would happen if we gave the command for our dog to fetch before we had taught it this trick (linked to jQuery). Therefore, we always link to the jQuery core library first, usually within the `<head>` tag.

+ Remote link: `<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.8.2/jquery.min.js"></script>`
+ Local link (downloaded from jquery.com):
`<script src=”js/jquery-1.8.2.min.js"></script>`
+ Both using local as fallback solution:
`<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.8.2/jquery.min.js"></script>
<script>window.jQuery || document.write('<script src="js/jquery-1.8.2.min.js"> <\/script>')</script>`

> ProTip: Have your students navigate to `https://ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js` in their browser to see the actual jQuery file that is being used. Notice that this file has `.min`, that means its 'minified' js (all the whitespace has been removed to make the file smaller).  Now have them go to `https://ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.js` - This file should make more sense!

#### Using jQuery from your own JS code

Set up steps for using jQuery in your websites:
+ Include link to jQuery core library:
`<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.10.1/jquery.min.js"></script>`
+ Link to your custom js file
`<script src=”./js/app.js"></script>`
+ Start your app.js with document ready command:

```js
  $(document).ready(function() {
    // your app code goes here.
  });
```

#### $(document).ready()
With jQuery you'll generally put code that uses HTML elements inside of the `$(document).ready()` method. This makes sure that the document has loaded all of the HTML before it tries to do anything with it. You can think of it as making sure your students have arrived to class before giving out directions. If no one has showed up and you start giving directions it won't be very effective. But if you wait till the students are seated and ready (`$(document).ready`) then they'll be able to follow instructions.

#### Selectors

jQuery allows us to find and manipulate HTML elements by using CSS selectors. For example this CSS

```
p.red-cls {
  background-color: red;
}
```
gets all the paragraphs `<p>` with `class="red-cls"` and sets the background color to red.

jQuery uses the same selector syntax. So, getting the HTML `<p class="red-cls">` elements with jQuery looks like this:

`jQuery("p.red-cls");` or `$("p.red-cls")`

The `$` symbol is just shorthand for `jQuery`. They both get the jQuery object.

#### Manipulation and Syntax

We manipulate content like this: 
```
$("#foo").text("hello world"); //this sets the text in #foo div to “hello world”
```

Here is an example of the syntax for using a jQuery method
`$(selector).method(parameters);`
+ `$` refers to the jQuery object.
+ `selector` asks jQuery to go out into the DOM (Document Object Model) web page and select an element(s). In jQuery we can use all of the familiar selectors we use in CSS. Yay!
+ `method` these are various actions and commands attached to the jQuery object that allow us to do things like fade elements in an out or change the content of the DOM and much much more.
+ `parameters` are options we can set for each method.
+ An example of real code:
  + `$('h1').css({'background':'yellow'})`;
  + `$` refers to the jQuery object.
  + `h1` asks jQuery to go out into the DOM (Document Object Model) web page and select all `<h1>`.
  + `css` method applies some CSS upon the selected element(s).
  + `{'background':'yellow'}` changes the background color to yellow.


#### Array Traversal

+ Understanding how to iterate through a JS array with a for loop is important and useful, but there is an even easier way to iterate through an array using the jQuery `.each` method.
+ We’re going to do a lot more jQuery review today but for now we’ll just walk through how to use `.each` like this:

```js
$(numbers).each(function(i, value){
  alert(value+1);      
});
```

+ You can see that we start with a `$` sign - which is the jQuery object and kind of how we say “Hey, jQuery! Got something for you.” And the thing that we have - numbers - goes in parentheses - kind of like an argument - and we are going to call .each on this numbers array. 
+ `.each` does exactly what you think it would do - it takes out each item in the array and it does whatever we tell it to do with each one.
+ The way that we tell it what to do is by feeding the `.each` method a function as an argument. You might remember this from Intro to Web Design class - arguments can be functions. We do this a lot with jQuery.
+ You can see that the function that goes into `.each` has two arguments - the `i` stands for index and the `value` is the actual thing in the array. Go ahead and try using `.each` to iterate through your numbers array.

#### Notes

If you want to do something to your DOM jQuery probably has a method for it. 
+ YOU DO NOT HAVE TO MEMORIZE ALL OF THE METHODS
+ Having an idea of what possibilities are available is useful, and familiarizing yourself with some that you will use from day to day is useful, unless you’re a jQuery guru you probably will not memorize every method. Fortunately we can look them up and see their usage at sites like:

+ API: [http://api.jquery.com/](http://api.jquery.com/)
+ Documentation: [http://docs.jquery.com/](http://docs.jquery.com/)
+ Or nifty cheatsheets like: [http://oscarotero.com/jquery/](http://oscarotero.com/jquery/)
+ and http://overapi.com/jquery

### jQuery vs JavaScript

*How will I know when to use jQuery versus core JavaScript?*
+ Firstly, jQuery is written in JavaScript so you can think of them as variations of the same thing instead of two separate things. To help answer this, jQuery methods are useful for many things; however there are certain fundamental parts of JavaScript that we still need in order to make flexible web applications. For example jQuery on its own does not have method for declaring variables, functions, if statements, or doing math…
+ This means that we can get a lot more mileage by integrating jQuery with core JavaScript. 
+ An example of JS and jQuery working together (demo in JSfiddle):

```js
  var x = 12, 
  y = 5,
  total = x + y;

  If (total === 17) {
   $(’p').text('Correct!');
  } else {
  $(’p').text('Incorrect.');
  }
```

+ It just works everywhere! jQuery has been written to solve many cross browser issues that exist in core JavaScript.
+ Terse code. You can often write fewer lines of code than you would in using core JavaScript to accomplish the same thing. Hence jQuery’s slogan “Write Less Do More”.
+ Popularity. jQuery is, at the time of writing this, by far the most popular JavaScript library. That means more forums, more code sharing, and more plugins.
+ Easy extending methods. Coders can create and share their own custom plugins easily.
+ Familiar DOM selectors. If you already know CSS you’re a step ahead as jQuery uses all our familiar CSS selector statements.

## Conclusion / So What?

jQuery brings out a lot of the functionality that is possible with JavaScript and makes it really easy. 

Also, over half a BILLION sites use jQuery, and it was written by a 20 year old in his downtime in college.  

## Hints and Hurdles

+ Passing in a new function as an argument to a jQuery function can feel weird at first, but stick with the syntax and it'll start making sense quickly
+ Remember, you just need to know how to use CSS selectors to find HTML elements with jQuery
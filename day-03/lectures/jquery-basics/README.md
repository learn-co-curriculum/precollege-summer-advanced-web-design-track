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

## Motivation / Why Should You Care?

jQuery is a powerful JavaScript library that can control all the magic you see on your page, from sliding menus to animations. [Beyonce](http://www.beyonce.com/) has some amazing jQuery on her page. Using Javascript and jQuery makes our pages interactive and awesome. Over half of all websites use jQuery, including 75% of the top 100 sites. That's half of ALL WEBSITES. IN. THE. WORLD. 

## Lesson Plan

### DOM

This stands for *document object model* and it is a structural representation of our HTML in tree form. Like this:

<img src="https://s3.amazonaws.com/after-school-assets/advanced_jquery2.png">

This model enables us to easily find elements and change their content, styles, and structure.

### jQuery Review

#### Installation

+ To set up a document to run jQuery we must link to the jQuery core library first!
+ Remote link: `<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.8.2/jquery.min.js"></script>`
+ Local link (downloaded from jquery.com):
`<script src=”js/jquery-1.8.2.min.js"></script>`
+ Both using local as fallback solution:
`<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.8.2/jquery.min.js"></script>
<script>window.jQuery || document.write('<script src="js/jquery-1.8.2.min.js"> <\/script>')</script>`

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

With jQuery you'll generally put code that uses HTML elements inside of the `$(document).ready()` method. This makes sure that the document has loaded all of the HTML before it tries to do anything with it. 

#### Selectors

jQuery allows us to find and manipulate HTML elements by using CSS selectors. 

jQuery uses the same selector syntax. So, getting the HTML `<p class="red-cls">` elements with jQuery looks like this:

`jQuery("p.red-cls");` or `$("p.red-cls")`

#### Manipulation and Syntax

We manipulate content like this: 
```
$("#foo").text("hello world"); //this sets the text in #foo div to “hello world”
```


#### Array Traversal

```js
$(numbers).each(function(i, value){
  alert(value+1); 
});
```

### jQuery vs JavaScript

+ Firstly, jQuery is written in JavaScript so you can think of them as variations of the same thing instead of two separate things. To help answer this, jQuery methods are useful for many things; however there are certain fundamental parts of JavaScript that we still need in order to make flexible web applications. For example jQuery on its own does not have method for declaring variables, functions, if statements, or doing math…

## Conclusion / So What?

jQuery brings out a lot of the functionality that is possible with JavaScript and makes it really easy. 

Also, over half a BILLION sites use jQuery, and it was written by a 20 year old in his downtime in college. 

## Hints and Hurdles

+ Passing in a new function as an argument to a jQuery function can feel weird at first, but stick with the syntax and it'll start making sense quickly
+ Remember, you just need to know how to use CSS selectors to find HTML elements with jQuery
+ If it seems like your jQuery isn't hooked up to your elements make sure you wrote your code within the `$(document).ready()` method
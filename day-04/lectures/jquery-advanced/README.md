# jQuery - Advanced

## SWBATs

+ Understand what constitutes an *event*
+ Attach jQuery event handlers (like 'click') to HTML elements
+ Add callback functions to event handlers
+ Use the `$(this)` selector in event handlers
+ Add animations to HTML elements using jQuery
+ Implement the jQuery UI library and other jQuery plugins
+ Parse through the jQuery documentation as a resource

## Motivation / Why Should You Care?

jQuery has *event handlers* that respond to user actions. This allows us to make all sorts of amazing behaviors and websites that respond naturally to user actions.

## Lesson Plan

### What are Events

jQuery [Events](https://api.jquery.com/category/events/) are user actions such as mouse clicks, anytime a key is pressed, or if the window is resized. 

### jQuery Click Handler

One very popular event handler is the `click()` handler. It runs code when the element it's attached to is clicked.

### What is a Callback function

A callback function is the function (aka: the code) that is run when an event handler is triggered. 

### Other Event handlers

jQuery can respond to a wide variety of Events which you should read about in the documentation. Some popular ones are:

+ Mouse clicks
+ Page load finishing
+ Moving the mouse over an element (often used for menu highlights)
+ Submitting an HTML form
+ Pressing the keyboard buttons
+ And [MORE](https://api.jquery.com/category/events/)!! 

### Document Ready as an Event

If you remember our `$(document).ready()` function, you can now see that it is just an event handler responding to the jQuery object of `$(document)` firing off the Event that it's `ready()`.

```js
$( document ).ready(function() {
  // Here are all the functions that 
  // will be run when the document is ready.
});
```

### `$(this)` inside Event callbacks

If you want to do something to the element that fired an event (fade out the button you just clicked) `$(this)` allows you to easily access that element.

### Animations

jQuery also has support for basic animations. They work by selecting the element and calling the function on it with a `.` between the functions. 

```js
// Show the HTML element with id="panel"
$("#panel").show(); 

// Hide that same element
$("#panel").hide();
```

 Here are some favorites:

+ `.show()` - Shows the selected element 
+ `.hide()` - Hide an element
+ `.fadeIn()` - Show an element with a slow fade
+ `.fadeOut()` - Fade out the element

Check the [documentation](https://api.jquery.com/category/effects/) for more examples and explanations.

### jQuery UI

[jQuery UI](https://jqueryui.com/) is another JavaScript library that is built on regular jQuery. It has support for more advanced animations and UI elements (things that look great and do cool stuff). To get a feel for what it can do check out some [demos](http://jqueryui.com/demos/).

### Using Documentation

As with all coding the internet is your friend!!! Whenever you are stuck, try a search for your issue, or start reading the documentation.  It's amazing what's out there. Don't let it scare you!

## Conclusion / So What?

jQuery and other libraries allow you to do amazingly complex stuff with a simple function call. Any developer worth their salt will want to make a website that responds to the user. jQuery events let you do that. 

## Hints and Hurdles
+ `$(this)` can be confusing, remember it refers to the element that the event handler was called on
+ `$(document).ready()` is just one big event that all your code should go inside
+ Event handlers take functions, anonymous or named, to call when that event happens
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

What happens when you click a button on site? Can we make code that responds to user actions?  What if we want something to turn blue when your mouse moves over it?

jQuery has *event handlers* that respond to user actions. This allows us to make all sorts of amazing behaviors and websites that respond naturally to user actions.

## Lesson Plan

### What are Events

jQuery [Events](https://api.jquery.com/category/events/) are user actions such as mouse clicks, anytime a key is pressed, or if the window is resized. In response to these events we can define some code that will be run everytime that happens. We can be notified of events that happen anywhere on the webpage or only on a specific HTML element.

### jQuery Click Handler

One very popular event handler is the `click()` handler. The code defined in this handler will be run anytime the HTML element that we are *listening* to is *clicked*.

Suppose we have HTML that looks like this

```html
<html>
  <head>...</head>
  <body>
    <button class=".the-button">Push the Button</button>
  </body>
</html>
```

We could *attach* a click handler to the element with jQuery so that code is run anytime the button is *clicked*.

```js
$(".the-button").click(function()
{
  alert("House Music!! Boots, and Cats, and Boots, and Cats");
});
```

Because we have created a jQuery event handler and attached it to the HTML element with the class `the-button`, when we click on the button, an alert will pop up that says "House Music!! Boots, and Cats, and Boots, and Cats".

### What is a Callback function

A callback function is the function (aka: the code) that is run when an event handler is triggered. In the previous example `.click()` takes an entire function as its input. If you count the parenthesis you'll see that this function on it's own looks like this:

```js
function()
{
  alert("House Music!! Boots, and Cats, and Boots, and Cats");
}
```

This is called an *anonymous* function, and is our callback function. It has no name and will only be run when the event handler is triggered. JS/jQuery allows you to also passed in a named function.  Our code in this case could look like this:

js```
// Define the function
function houseMusic()
{
  alert("House Music!! Boots, and Cats, and Boots, and Cats");
}

// Pass the function to the event handler
$(".the-button").click(houseMusic);
```

A trick to notice here is that when we pass in the function `houseMusic` we DO NOT include the parenthesis `()`, because we are not calling the function at this point. We are only telling the event handler where to find it.

### Other Event handlers

### `$(this)` inside Events

### Animations

### jQuery UI

### Using Documentation

## Conclusion / So What?

## Hints and Hurdles

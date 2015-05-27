# Week 1 Review

## Motivation/Why Should I Care?

We've learned a TON this week - let's take a few minutes to go over everything we've learned. *Teacher - feel free to spend more/less time depending on how your week went and how the students did*

## Lesson Plan

### HTML

+ Who can tell me the basic structure of our HTML document?
	+ We start out with `<!DOCTYPE html>`
	+ Then we have opening and closing `<html>` tags
	+ Inside of our `html` tags, we have two sections. 
		+ `<head>` and `<body>`
+ What are some of the different tags we can use to section off our page?
	+ `div`, `section`, `article`, `nav`, `header`, `footer`
+ That's great. What about multimedia? How can we include multimedia in our pages?
	+ `audio`, `video`, `img`

### CSS

+ You guys are doing great! Let's talk quickly about styling. 
+ We style our pages using CSS. How can we tell our html pages about our stylesheets?
	+ `<link rel="stylesheet" type="text/css" href="location">`
+ What are some styles we can change about our pages using CSS?
	+ Font, font size, font color, background image, background color

### Javascript Basics

+ We've learned a ton of JavaScript this week! Let's practice some of the things that we've learned. Open Google Chrome and go to your JavaScript Console.
+ Great, let's declare a variable and assign it to a string. What's the syntax for defining a variable?
	+ `var variableName = "string"`
+ What are some other types of data that we can use in JavaScript?
	+ Integer
	+ Float
	+ boolean
+ Who remembers how we can combine two strings together? 
	+ `"my string" + " is great"` returns `"my string is great"`
+ Another cool thing we can do is send alerts and confirmation messages - how can we do that?
	+ `alert("My message!")` - a user can click "ok" to get rid of this
	+ `confirm("Are you sure?")` - a user can click either "ok" or "cancel"
	+ `prompt("Who are you?")` - prompts a user for input
+ We can do comparisons using logic operators. What are three types of comparisons we can do?
	+ `===`, `>`, `<`, `>=`, `<=`, `!==`
+ Using our operators, can someone help me write a conditional statement? 
```js
var name = prompt("What is your name?")
if ( name === "Beyonce" ){
	alert("OMG I LOVE YOUR MUSIC!");
} else {
	alert("Hello, " + name + "!");
}
```
### Arrays, Loops, and Functions

+ So we can store data in variables, but what's a way that we can group variables together? 
	+ Remember, our variables are a bunch of muffins. We need a way to hold our muffins. 
	+ We can use an array - it's like a muffin tin.
+ Can someone help me setup an array?
	+ `var animals = ["dog", "cat", "bird"]
+ Awesome. Now, what if we want to loop through this array and print out each name?
```js
var animals = ["dog", "cat", "bird"]
for (var i = 0; i < animals.length; i++){
	alert(animals[i] + " is a great animal!");
}
```

+ This is great, but what if we want to package this code to be reused later?
+ We can save it as a function!
+ Let's save our conditional statement from before as a function so we can run it again. 
```js
function sayHello(name){
	if ( name === "Beyonce" ){
		alert("OMG I LOVE YOUR MUSIC!");
} else {
		alert("Hello, " + name + "!");
	}
}
```
+ We can now run this function whenever we want, without having to type the whole thing over again
	+`sayHello("Ian")`
	+ `sayHello("Beyonce")`

### jQuery

+ So we know about functions - these are super cool when we're using jQuery. 
+ Remember, we can use jQuery to select and manipulate elements in our HTML. 
+ First, we need to tell jQuery to wake up. How do we do that?
	+ `$`
+ That's great! Now how do we select all of the h1s? What about all of the h1s with an id of title?
	+ `$("h1")`
	+ `$("h1#title")`
+ Awesome. Now that we've selected our h1, let's add an event handler to it. 
	+ An event handler is a way to "watch" an item for a certain event, like click or hover
	+ Below are two ways to do this - they do the same thing.
	```js
	$("h1").click(function(){
		// we can put our code here!
	})

	$("h1").on("click", function(){
		// code here!!
	})
	```
+ And can someone remind me what's going on with that function after the "click"?
	+ That's our callback. This is code that fires after our event happens. 
	+ It can be an "anonymous function", like in the example above, or a predefined function. 
	```js
	$("h1").click(sayHello);
	```
+ Let's say we want to manipulate the element that was clicked on. How can we select that?
	+ By using `this`! 
	+ The concept of `this` can be confusing, but in general in jQuery it refers to whatever fired the event. 
+ Pretend we have five `lis` on the page - we want to remove any one that is clicked on. 
	+ We can put one event handler, and use `this` to select the one that was clicked.
	```js
	$("li").click(function(){
		$(this).remove();
	})
	```
+ Remember that we need to control when our event handlers get added - if we add them before our elements load, we won't be listening for them properly. 
+ We can do this by using document ready!
	```js
	$(document).ready(
		//all of our event handlers should go here!
	)
	```
	+ Here's a shortcut way to do the same thing: 
	```js
	$(function(){

	})
	```




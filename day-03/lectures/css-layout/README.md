# CSS Layout - Lecture Notes

## Objective

Students will be able to use the box model to create cohesive page layouts

## SWBATS

+ Understand box model and how it is affected by padding, margin and border
+ Understand how to use box-sizing property to standardize the box-model across browsers
+ Use content overflow property - visible, hidden, scroll, auto
+ Understand inline vs. block vs. inline-block element displays
+ Understand how to use float and clear properties
+ Understand how to apply clearfix solution
+ Understand how to use CSS position properties - relative, absolute and fixed
+ Use background properties for box styling


## Motivation

Yesterday we used CSS to style the fonts, images and backgrounds of our page. Today we’re going to learn how to use CSS to break up and arrange the content on our page.

## Lesson Plan

### Box Model

 You probably want to set your `div`s to a certain width and height.
+ There are several important elements that go into determining the total size of the div though. These include:
	+ Margin - the space that you want between your divs
	+ Border - you might want to include a bold border around your div
	+ Padding - how much space you want between the edge of your div and the content inside your div
+ For instance - this is what your page might look like if you do not take these things into account: <a href="no-padding.html">here is an example</a>.
  * Play around with inspect element and noticing what changes when you modify each param
+ These sizing attributes are part of something that we call the box model.

<img src="https://s3.amazonaws.com/after-school-assets/box_model.png">

+ Unfortunately, not all browsers treat these attributes the same. Most browsers follow the WC3 model but Internet Explorer is a rogue. Here are the two models:

<img src="https://s3.amazonaws.com/after-school-assets/w3c_box_model.png">


+ Luckily we have a box-sizing property that allows us to choose which model we want to follow. Here are the two options:
	* For IE model
	```css
	 div {
	 box-size: border-box;
	}
	```
	* W3C model:
	```css
	div {
	box-size: content-box;
	}
	```
+ There are a few different measurements that we can use to scale divs:
	* Fixed (px)
	* Fluid (%)
+ Each of these have their own pros and cons.
+ Fixed px (what we’ve been using) gives the developer a lot of control over what the user sees, but it is not flexible.
	* No matter what size the screen is the div will be the same size - which means there might be a lot of white space on larger screens or the user might have to scroll when not all of the content fits on the page. 
+ A fluid design uses percentages. So width and height can be set to take up a certain amount of the screen.
	* This is a major part of creating a “responsive site”.
	* We are going to talk more about responsive web design later but in a nutshell - RWD is hugely important because people access web applications from a ton of different types of devices - from cell phones to giant wide screen desktop monitors and you want your website to look good on all of these devices. 
+ Another option is set min and max width and heights.
	+ This is a pretty good compromise in that it gives you more control over what the user sees, while also making the site flexible for multiple screen sizes.
	+ 960px is generally the max-width for a smaller screen and 1180px for a larger screen
	+ Note that setting the height of a div to 100% will only make it 100% as tall as its parent div. If you want it to take up 100% of the page, make sure that the parent div also has a height and min-height that is set to 100%.
+ ***[Demo](height.html) these things for students and have them practice/test.*** 

### Overflow Visibility 

+ If you do not set a height for a div it will automatically be tall enough to fit the content. If you set a height you have a few options for how you display the content with the overflow property.
+ Demonstrate how each of these (`visible`, `hidden`, `scroll`, `auto`) 
	```css
	div {
		overflow: visible | hidden | scroll | auto;
	 }
	```
+ Have students practice with [this example](http://jsfiddle.net/flatiron_school/sFfw5/)

### Display Type

Most browsers display `div`,`p`,`h` in `block` style. That means that each element on the page will be displayed directly below the next one and take up the whole width of the page. 
+ There are a few other elements, such as `span`s and `img`s which display inline - meaning they show up side by side. 
	+ Appears side by side does not accept width or top and bottom margins
	+ [Example](http://jsfiddle.net/flatiron_school/352A6/1/)
+ We can change the default display property in CSS like this: 
	+ `display: block;`
	+ `display: inline;`
	+ `display: inline-block;`
+ Margins will overlap for block elements (above and below) but not for inline elements (horizontal)

<img src="https://s3.amazonaws.com/after-school-assets/display-property.png">

+ The `inline-block` is sort of a combo of the other two - the content of each item stays seperate, but display inline next to each other. 

+ This seems like the best of both worlds - except that using inline-block doesn’t give us as much control - this element is kind of floating here instead of aligning at the top - display with jsfiddle. You can use inline-block just be aware of how it affects your layout.

### Float

+ By using the `float` property with display: block; you should have good control over how things are displayed on the page - including placement AND width/height + margins.
+ The float property accepts two values: right and left.
	+ ***[Demo](https://jsfiddle.net/qjjqv315/) how float works with three divs.***
+ Float only affects elements after it. So we can leave this first div as block display and adding float: right to the second div will cause it to float to the right of the last div but still below the first one.
+ You may run into a situation where you are floating your elements and something like the footer is sneaking up

<img src="https://s3.amazonaws.com/after-school-assets/float-propert.png">

+ To fix this you can add a `clear` property set to the value of both. This means clear divs floating both right and left and it will sink the footer to the bottom of the page.
+ One more thing to be aware of is collapsing parents.
	* If all of the divs inside of a parent are floating then the parent loses a reference for how big it should be. This often happens when you have a larger div like a wrapper - that might be controlling the width of the page - with floating divs - like articles inside. 
+ Demo an example. To solve this you can set up a clearfix class like this:
```css
		.clearfix:after {
			content: ".";  /* Content property - inserts the text in quotes */ 
    	display: block; /* Display: block (take up the whole width of page) */
    	clear: both; /* Clear: says which side (right or left) of this element floating elements are allowed - in this case no elements can float right or left */
    	visibility: hidden; /* Hides the element but leaves it in the layout */
    	height: 0; /* Height: how tall the element is, in this case, not at all */
    	line-height: 0; /* Line-Height: on block elements (like this one), specifies the minimum height of line boxes within the element */
		}
```
### Positioning and Z-Index

+ We can also control the positioning of our divs more granularly with CSS positioning techniques like:
+ `relative` - will position a `div` relative to its parent
+ `absolute` - will position a `div` in absolute relation to the screen UNLESS it is within a `div` that is positioned in some way.
+ `fixed` - Will position the `div` at a fixed place relative to the browser window - even if the person scrolls down the fixed `div` will stay on their screen.
+ Let’s take a look at how this works with this [example](http://jsfiddle.net/flatiron_school/rgyPC/1/).
+ One last thing you can control when it comes to positioning is the `z-index` which lets you layer divs and control their position into the third dimension!
+ Divs with a higher z-index will be positioned on top of elements with a lower z-index or no z index at all.
+ Here is an example:
```css
.bluebox {
   position: relative;
   top: 125px;
   left: 125px;
   z-index: 3;
 }
```
<img src="https://s3.amazonaws.com/after-school-assets/z-index.png">

+ Let’s take a closer look with this [jsfiddle](http://jsfiddle.net/flatiron_school/nWGts/ )
+ ***Now it’s time for you to apply your skills to your personal page!***


### Conclusion 
With CSS, we can controls the entire layout of our page, and how elements relate to each other.

### Hints/Hurdles
+ Make sure you are familiar with all the coding examples, or create your own examples before class. Layout can get tricky and CSS elements can compete with each other. It's easy to break things live and not be able to dig yourself out.

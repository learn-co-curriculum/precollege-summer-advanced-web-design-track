# Bootstrap - Lecture Notes

## SWBATs

+ Understand the concept of a CSS library
+ Include CSS libraries such as Bootstrap by using the `<link>` tab
+ Use Bootstrap Resources to add styling to their sites
+ Understand the concept of the 'grid' and how to use it to create responsive designs

## Motivation/Why Should I Care? 

CSS is awesome, but can be time consuming to write. Bootstrap allows developers to make beautiful sites very quickly.

## Lesson Plan

### Bootstrap Setup

+ You've already been writing CSS to see how you can style your pages. Writing your own CSS is a great way to style your pages, but it can take a long time. 
+ Sometimes, you want to get up and running more quickly. Enter Bootstrap. 
+ Bootstrap is a CSS library, which means it's just a big CSS file with pre-defined class styles ready to go.  The actual file can be viewed by navigating to it's [URL](https://maxcdn.bootstrapcdn.com/bootstrap/3.3.4/css/bootstrap.css)
+ Let's checkout Bootstrap here: [Get Bootstrap](https://www.getbootstrap.com/getting-started)
+ Bootstrap gives different options to get up and running. 
	* We can download the files and include them with our project, the same way we include our own custom css files. 
	* These files are also hosted for us to use by MaxCDN. By simply including a link in our `<head>` section, we can get the same access to those files. 
+ Make sure to include this link on any projects that you want to use Bootstrap: `<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.4/css/bootstrap.min.css">`

### Styling Your Page With Classes

+ Once we have bootstrap included in our project, we can add pre-defined classes to our HTML elements and they'll automatically get that style. 
+ Check out this example *open this [page](./bootstrap.html) in your browser*
+ Here's a button with no styling at all. 
+ When I give the button a class of `btn-primary`, it changes. What changed? 
	* Color
	* Font
	* Shape
+ What defined those changes? Bootstrap. 

### Grid System

+ Bootstrap comes with some great layout features as well. Imagine if we divied our site into twelve equal-sized columns. Rather than describing the size of our elements in pixels or percentages, we could describe them by number of columns they take up.
+ The human brain is good at identifying patterns and one way that patterns are reflected in design is through the use of grids.
+ A grid is a tool that can be used to establish a spacial hierarchy of the content. It can be fixed or fluid, horizontal or vertical, uniform or responsive. Grids should be viewed as guides, not boundaries; good designers know how to use grids, great designers know how and when to break them.
+ The rules of threes or four 
	+ Dividing a page up into threes or fours tends to be pleasing to the eye - and to take advantage of both these ratios web design tends to split up a page into a 12 column grid (12 = 3 * 4)
	+ This way you can easily split the page in half, thirds or fourths

+ Here are some examples of how you can split up the 12-grid:

<img src="https://s3.amazonaws.com/after-school-assets/grid-system.png">

+ We can use Bootstrap classes to setup our elements on a nice-looking 12 column grid. 
+ First, we need a container to hold everything. For this, we can use a `<div>` with the class of `container`. 
+ Inside of our container, we should define our rows. Again, we can use a `div` with an class of `row`. 
+ Now that we're in our row, we can divide our content into columns. Take a look at this example: 

```html
<div class='container'>
	<div class="row">
		<div class="col-md-6">
		</div>
	</div>
</div>
```

+ In our div with the class of `col-md-6` will take up half the row on a medium-sized screen (the `md` stands for medium.)
+ On smaller screens, the div will take up the whole row. 
+ In the below example, the div will take up the entire row on small and extra small screens, like phones and tablets, and half the screen on larger devices, like laptops and large displays. 

```html
<div class='container'>
	<div class="row">
		<div class="col-lg-6">
		</div>
	</div>
</div>
```
+ This will help our site look great on a bunch of different screens. 
+ Look at the example [here](http://learn-co-curriculum.github.io/bootstrap-grid-example/)
	* Notice that the arrangement changes based on the size of the window. 

### Conclusions

Bootstrap helps us make our sites looks great without having to write new CSS every time. 

### Next Steps

Check out [this walkthrough](https://github.com/learn-co-curriculum/Hs-Bootstrap-Walkthrough) to start playing around with Bootstrap!



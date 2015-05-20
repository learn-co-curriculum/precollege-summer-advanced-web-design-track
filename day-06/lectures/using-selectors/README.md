# Interactive Practice - jQuery Selectors

## Motivation/Why Should You Care? 

We've seen how powerful jQuery can be, but the syntax can be a little hard to pick up. Let's practice together to start getting the hang of it. 

## Lesson Plan

### Selecting an Element

+ Open Google Chrome and navigate to [beyonce.com](http://www.beyonce.com)
	*If Beyonce is down, you can use [Instagram](https://www.instagram.com)*
+ In the toolbar, click "View" > "Developer" > "Javascript Console"
+ Remember that Javascript was built to run in our browser - the console lets us type in Javascript and jQuery commands to test things out and play around. 
+ Let's write some jQuery. What do we type to tell jQuery "hey, jQuery, wake up"?
	* *Let students answer, "The dollar sign!"*
+ Great, go ahead and type a dollar sign. Next, in parenthesis, we need a selector. Let's see if we can figure out what text the h1 has. How can I tell jQuery, "hey, jQuery, show me all of the h1s on this page"?
	* *type h1 in quotes and parenthesis after the dollar sign
+ Nice, so we'll type `$( "h1" )` and press enter. 
+ Boom! There's our h1!
	* *If there are more than one h1s, they'll show up in brackets like this. We'll talk more about this tomorrow.*
+ So that's how we select h1s, how could I select all the p tags? What about h2, or a?

### Modifying an Element

+ So we can know select an h1 element. What if I want to know what text it contains? I can do this by calling a jQuery method on the element. 
+ Does anyone know what method I can use to get the text from the h1?
	* `.text()`
+ Let's try it. First, we'll type `$( "h1" )` to select the h1 tag. Next, we'll add `.text()` - the whole thing looks like `$( "h1" ).text()`
	* Remember that the parenthesis after `.text()` tell Javascript to run that function!
+ Go ahead and press enter - you should see the text that's contained in that h1! 
+ If we want to, we can change the text by putting it in the parenthesis at the end of our method. 
+ Type: `$( "h1" ).text("Flatiron Rules!")`
+ All of the h1 tags should now say, Flatiron Rules!
+ Try this again - change the text to whatever you like!
+ There's a lot going on here, can someone explain to me all of the steps?
	+ *Teachers - have a student walk through all of the steps going on. Make sure that they understand they are selecting an element and modifying it with a method. 

### Bonus Fun - Animation Methods

+ Do you guys want to see something cool? jQuery has lots of great animation methods built into it. Try selecting our h1 again, but this time call the `slideUp()` method on it. 
	* `$( "h1" ).slideUp()`
+ Pretty cool right? Take a few minutes to try out some other jQuery methods. Feel free to use the documentation, or use Google to find more. 
	* Example - "how do I fade out using jQuery?"

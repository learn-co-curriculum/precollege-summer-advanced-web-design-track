## SWABATs 

***Students will be able to create their own functions in JavaScript and use Jasmine to test their code.***
+ Declare JS functions with and without parameters
+ Call JS functions with and without passing arguments
+ Understand the concept of a return value
+ Understand local and global variable scope
+ Understand when to use semicolons with functions

## Motivation

In this class we’re going to dive much deeper in JS so that you can create full scale dynamic web sites using JavaScript and jQuery to add magic to our pages! To make sure we’re all ready to go deep into JS we’re going to do a little review of JS fundamentals - datatypes, data structures and program flow - and then launch into building JS functions - which are the real building bricks behind building programs with JS. Let the programming begin!

## Lesson Plan

+ Now that we’re getting comfortable with the basics of JS we’re going to move on to JS functions.
+ A JS function is essentially a set of instructions that we write out and can reuse over and over again.
+ (Pick a kid in the class to call on). Joe - I want you to close your computer, stand up and walk out the door.
+ Jk, come back. These essentially are the steps that Joe would follow if he was getting ready to head out to lunch.
+ Computers need explicit step by step instructions like this because they cannot infer what you mean when you say something like go get lunch.
+ But we can essentially teach the computer what go get lunch means by wrapping up these instructions in a function called `goGetLunch`.
+ Let’s create a `goGetLunch` function in JSfiddle.
+ The syntax for writing JS functions is very specific. It looks like this:

```js
function goGetLunch() {
};
```

+ The instructions go inside this function. Let’s alert each of the steps inside of our function and try running the program.

```js
	function goGetLunch() {
		alert("Close Computer");
		alert("Stand up");
		alert("Walk out the door")
	};
```

+ Nothing happened. Why is that? We declared our function - which is like adding the `goGetLunch` function to the computer’s dictionary - but we didn’t actually tell the computer to execute the function.
+ We need call a function like this `goGetLunch();` to make it run.
+ This is the equivalent of telling the computer - do those steps in the `goGetLunch` function. Test it out.
+ What’s up with those parentheses? Those are like a placeholder for something called an argument. 
+ Our instructions are pretty generic right now. What if we wanted to direct them towards a specific student? Like adding a step that says “hey, Joe”.

```js
function goGetLunch(student) {
  alert('hey, '+student);
  alert('close your computer');
  alert('stand up');
  alert('walk out the door');
}
```

+ We can reuse this function and just change the name of the student we address by adding a student argument.
+ Then we can call it like this:

```js
goGetLunch("Joe");
goGetLunch("Jill");
goGetLunch("Josie");
```

+ There is one more VERY IMPORTANT thing about functions - return values.
+ We are going to get some help explaining this concept from Cheddar the mouse.
+ https://docs.google.com/a/flatironschool.com/presentation/d/1USGrpdEBhsYdP4b8LpVTabOHzMVKDLb0ZXen0Un3MPA/edit#slide=id.gacf625b88_0_11
+ A function is kind of like placing a mouse in a box and that mouse will only perform the actions he was trained to do whenever you tell him to do a certain action.
+ Here is Cheddar in his box. We’ve trained him to doMath (addition really) with two variables x and y.

```js
function doMath(x,y){
	return x+y;
}
```

+ Notice there is a return statement. We need to include return in order to get something back from the function. In essence if we left of the return statement Cheddar might perform the math in his head but not give us the answer. By saying return we’re telling the function give us back the answer.
+ This is important because most of the time functions don’t live all alone by themselves they rely on other functions - so getting something back is very important. Don’t forget the return! 
+ So functions are pretty cool, huh? From now on ALL of your code should be wrapped in functions. 
+ Let’s get some practice with a lab. Everyone go to Learn.co and fork and clone the Teenager.js lab.
+ From now on we’ll be working on labs that have built in tests to tell you whether or not your code is correct.
+ Testing is an important part of building and maintaining applications. Automated testing is <u>essential</u> for large scale programs like Facebook and Twitter.
	+ When you have a very simple application it’s easy to test it by just running it - like we’ve been doing with JSfiddle.
	+ If you have a really large complex application it would take a ton of time for someone to manually go through thousands of lines of code and check every piece of the application.
	+ So instead we write tests - essentially code to test our code.
+ Let’s dive right in.
+ In the Teenager.js Lab: We’ll be using a JS library called Jasmine to test our code. And you can find all the tests in the spec folder. Spec is short for specifications - as in we expect this program to run according to these specifications. Let’s take a look at isTeenager.spec.js.
+ The first thing you see at the top of the page is `use strict` which just means that the spec should follow the conventions of the latest version of JS (ECMA script 5).
+ The next word is describe - as in the following will describe what the isTeenager function should do.
+ There are several different specs that are being tested inside of this describe block:
	+ `it` statements tells you what the test is expecting to get back
	+ `expect` statements is where Jasmine is actually going to call the function define in `isTeenager.js`
	+ `.toBe` is where Jasmine states what it expects will happen when that function is called
	+ **Can anyone walk me through this in their own words?**
+ Now let’s take a look at `isTeenager.js`. We’ve already gotten you started by declaring the function. Now you just have to fill it in. Give it a shot!
+ To test run `learn -b` in your terminal. You’ll see the tests run in your terminal and also in your browser. The browser will probably be more helpful.
+ We have one more lab for you guys to practice flow control. One thing I want to point out about this lab - if you take a look at `fizzbuzz.js` in the Fizz Buzz lab the function is declared in a slightly different way. 
+ This style of declaring a function is called function expression instead of a function declaration. We’re going to stick with function declarations but other people use this style so it’s good for you to know that it exists. Take a look at the README and spec and then give this lab a shot.
+ There are a few more things that you need to know about functions.
+ Hoisting: JavaScript tries to be helpful and it will go through a function and look for all of your variables before it runs the function. This seems like a good thing because if you try to use a variable `name` at the top of your function (before you declare it like this - var name) JS will be like - oh ok, I know there is a variable `name` in here somewhere. 
```js
function sayHey(){
	name = "Victoria";
	console.log(name);
	var name;
}
```
BUT it’s not really that helpful because JS will only know that the variable exists. So if you declare `var name = "Victoria"` somewhere lower down in the function it will know that `var name` exists but it will not know that you set the variable name `equal` to `"Victoria"`
+ This is really just a roundabout way to tell you DECLARE ALL OF YOUR VARIABLES AT THE TOP OF A FUNCTION. It’s best practice and it will help you avoid complications later. DECLARE YOUR VARIABLES AT THE TOP OF YOUR FUNCTION.
+ Another thing that is important to understand about JS functions is variable scope. 
	+ When you declare a variable outside of a function it will also be available inside of the function. For example (open up the console in Chrome and paste this in):
	+ var milkType = "whole milk";
	+ function isWholeMilk() {
	      + if (milkType === "whole milk”) {
	          + return true;
	      + } else {
	         + return false;         
	      + }
	+ }
	+ If I run isWholeMilk(); we’ll get back true. The function isWholeMilk has access to the variable milkType that was declared outside of the function.
	+ BUT if you declare a variable inside of a function it will only be available inside of the function.
	+ Here is an example:
	+ function milkTheCow() {	
	      + var bessyCow = 'milked'; //local var
	      + return bessyCow;
	+ }
	+ If we type bessyCow we’ll get back undefined. We are trying to access bessyCow from outside of the function and she only exists inside of the function.
	+ The only way you can get access to bessyCow is if you run the function. Then bessyCow will be returned - like when Cheddar tossed out the answer to those math equations - and we’ll be able to see the value that way.
	+ One last brain teaser for you guys. 
	+ var tiger = 2,
	      + lion = 3; \\we can declare two variables at the same time like this
		
	+ function countAnimals(giraffe) {
	      + tiger = tiger - 1;
	      + var total = lion + tiger + giraffe;
	      + return total;	
	+ }
	+ What will the total equal (what value will be returned when I run countAnimals(3);
+ Variable scope - and not being able to access variables outside of a function - seems annoying but it’s really important and helpful because you will know exactly what your variable is equal to - it can only be set from within your function so it can only be equal to the value that you set within your function.
Every head to Learn.co and fork and clone LAB I NEED TO CREATE for more practice. 
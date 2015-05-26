# Functions

## SWABATs 

+ Understand N.I.C.O (Name, Input, Code, Output)
+ Declare JS functions with and without parameters
+ Call JS functions with and without passing arguments
+ Understand the concept of a return value
+ Understand local and global variable scope
+ Understand when to use semicolons with functions

## Motivation

Today we will learn about functions in JavaScript. This is important because functions let us package code into blocks that we can reuse. It connects to what we've previously learned because we can take the code we've written before and package it into functions. This will prevent us from writing the same code over and over again. We've also been using a handful functions already and this lesson will explain how and why we've been doing that.

## Lesson Plan

### Concept

In programming, a function holds a set of actions that will only run when we call that function. This ultimately helps us control the flow of our program and allows us to easily repeat a set of actions multiple times.

If you prefer a metaphor:
A function is kind of like placing a mouse in a box and that mouse will only perform the actions he was trained to do whenever you call his name.

### Declaration

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

### Calling a function

+ We need call a function like this `goGetLunch();` to make it run.
+ This is the equivalent of telling the computer - do those steps in the `goGetLunch` function. Test it out.
+ What’s up with those parentheses? Those are like a placeholder for something called an argument. 
+ Our instructions are pretty generic right now. What if we wanted to direct them towards a specific student? Like adding a step that says “hey, Joe”.

```js
function goGetLunch(student) {
  alert('hey, ' + student);
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

### Return Values

+ There is one more VERY IMPORTANT thing about functions - return values.
+ We are going to get some help explaining this concept from [Cheddar the mouse](https://docs.google.com/presentation/d/1yoZyfQbvEfw53Pp03Bd_ziY8-Ai0jqCeQ0NKy4EAce8/edit#slide=id.p60).
+ A function is kind of like placing a mouse in a box and that mouse will only perform the actions he was trained to do whenever you tell him to do a certain action.
+ Here is Cheddar in his box. We’ve trained him to `doMath` (addition really) with two variables x and y.

```js
function doMath(x,y){
	return x+y;
}
```

+ Notice there is a `return` statement. We need to include `return` in order to get something back from the function. In essence if we left of the return statement Cheddar might perform the math in his head but not give us the answer. By saying return we’re telling the function give us back the answer.
+ This is important because most of the time functions don’t live all alone by themselves they rely on other functions - so getting something back is very important. Don’t forget the return! 
+ So functions are pretty cool, huh? From now on ALL of your code should be wrapped in functions. 

### N.I.C.O

We can break down the creation of functions into four things that every function has:

+ **Name   ** - Decide an appropriate name for the function
+ **Inputs ** - Figure out what inputs, if any, are needed to accomplish what the name describes
+ **Code   ** - Put the code inside the function to be run when it is called
+ **Outputs** - A value that the function can return though it can be `undefined`


### Hoisting

JavaScript tries to be helpful and it will go through a function and look for all of your variables before it runs the function. This seems like a good thing because if you try to use a variable `name` at the top of your function (before you declare it like this - var name) JS will be like - oh ok, I know there is a variable `name` in here somewhere. 
```js
function sayHey(){
	name = "Victoria";
	console.log(name);
	var name;
}
```
BUT it’s not really that helpful because JS will only know that the variable exists. So if you declare `var name = "Victoria"` somewhere lower down in the function it will know that `var name` exists but it will not know that you set the variable name `equal` to `"Victoria"`
+ This is really just a roundabout way to tell you DECLARE ALL OF YOUR VARIABLES AT THE TOP OF A FUNCTION. It’s best practice and it will help you avoid complications later. DECLARE YOUR VARIABLES AT THE TOP OF YOUR FUNCTION.

### Variable Scope

Another thing that is important to understand about JS functions is variable scope. 
	
+ When you declare a variable outside of a function it will also be available inside of the function. For example (open up the console in Chrome and paste this in):

```js
var milkType = "whole milk"
function isWholeMilk() {
  if (milkType === "whole milk”) {
      return true;
  } else {
      return false;
  }
}
```
+ If I run `isWholeMilk();` we’ll get back true. The function `isWholeMilk` has access to the variable milkType that was declared outside of the function.
+ BUT if you declare a variable inside of a function it will only be available inside of the function.
+ Here is an example:
```js
function milkTheCow() {	
  var bessyCow = 'milked'; //local var
  return bessyCow;
}
```
+ If we type `bessyCow` we’ll get back undefined. We are trying to access `bessyCow` from outside of the function and she only exists inside of the function.
+ The only way you can get access to `bessyCow` is if you run the function. Then `bessyCow` will be returned - like when Cheddar tossed out the answer to those math equations - and we’ll be able to see the value that way.
+ One last brain teaser for you guys. 
+ `var tiger = 2,lion = 3; \\we can declare two variables at the same time like this`
	
```js
function countAnimals(giraffe) {
      tiger = tiger - 1;
      var total = lion + tiger + giraffe;
      return total;	
}
```
+ What will the total equal (what value will be returned when I run `countAnimals(3);`
+ *Variable scope* - and not being able to access variables outside of a function - seems annoying but it’s really important and helpful because you will know exactly what your variable is equal to - it can only be set from within your function so it can only be equal to the value that you set within your function.

## Conclusion / So What?

Functions are the building block of any developer. They let you create little machines (mice) that you can use and re-use from other parts of your code. This can make life a lot easier and save a ton of typing!

## Hints and Hurdles

+ Syntax is important! Missing an opening `{` or closing `}` brace could change all of the behavior in your program
	+ A way to check this manually, is have people start counting at 0 and add 1 for every opening `{` brace and subtract 1 for every closing `}` brace.  If you do it right you should always end up back at 0.
+ Function names should be descriptive and helpful. Trust me, 'future you' who doesn't remember your code at all will thank you.
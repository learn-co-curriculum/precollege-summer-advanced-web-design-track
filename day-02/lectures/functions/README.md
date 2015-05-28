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

### Calling a function

+ We need call a function like this `goGetLunch();` to make it run.

### Passing in Paramaters (inputs)

```js
function goGetLunch(student) {
  alert('hey, ' + student);
  alert('close your computer');
  alert('stand up');
  alert('walk out the door');
}
```

+ We can reuse this function and just change the name of the student we address by adding a student argument.

```js
goGetLunch("Joe");
goGetLunch("Jill");
goGetLunch("Josie");
```

### Return Values

```js
function doMath(x,y){
	return x+y;
}
```

+ Notice there is a `return` statement. We need to include `return` in order to get something back from the function. 

### N.I.C.O

We can break down the creation of functions into four things that every function has:

+ **Name   ** - Decide an appropriate name for the function
+ **Inputs ** - Figure out what inputs, if any, are needed to accomplish what the name describes
+ **Code   ** - Put the code inside the function to be run when it is called
+ **Outputs** - A value that the function can return though it can be `undefined`


### Hoisting

Hoisting moves all variable declarations to the top of the function.  This can cause problems. Declare all of your variables at the top of your functions

### Variable Scope

+ When you declare a variable outside of a function it will also be available inside of the function. 
+ If you declare a variable inside of a function it will only be available inside of the function.
+ *Variable scope* - and not being able to access variables outside of a function - seems annoying but it’s really important and helpful because you will know exactly what your variable is equal to - it can only be set from within your function so it can only be equal to the value that you set within your function.

## Conclusion / So What?

Functions are the building block of any developer. They let you create little machines (mice) that you can use and re-use from other parts of your code. This can make life a lot easier and save a ton of typing!

## Hints and Hurdles

+ Syntax is important! Missing an opening `{` or closing `}` brace could change all of the behavior in your program
	+ A way to check this manually, is have people start counting at 0 and add 1 for every opening `{` brace and subtract 1 for every closing `}` brace.  If you do it right you should always end up back at 0.
+ Function names should be descriptive and helpful. Trust me, 'future you' who doesn't remember your code at all will thank you.
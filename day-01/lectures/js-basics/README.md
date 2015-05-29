# JavaScript Basics

## SWBATs

***Students will be able understand the fundamentals of JavaScript***
+ Display text in the console
+ Perform math with JS
+ Declare JavaScript variables
+ Declare JS constants
+ Understand JS datatypes
+ Execute string concatenate
+ Utilize string methods
+ Execute string concatenate
+ Understand datatype conversion and why/when to use it
+ Use different types of dialogue boxes like alert, prompt, and confirm
+ Understand comparison and logic operators
+ Use conditional statements to control program flow (if/else and switch)


## Motivation
JavaScript is a coding language that is supported by every browser and allows developers to write code that can do amazing things on any platform. It is supported by every browser out there, and allows developers to write code for any platform.

## Lesson Plan

### Syntax Basics

+ A simple variable declaration
+ Whitespace has no meaning outside of quotation marks
+ Parentheses indicate precedence
+ Tabs enhance readability, but have no special meaning

### Variables

+ A variable is like a bucket with a Name and Value, that we can store some data inside and then later change the data it stores.

### Math

+ JavaScript supports the basic math operators you would expect (`+`, `-`, `*`, `/`)
+ JS also supports something called "Modulo", which we represent with the `%`
+ `x%y` returns the remainder of `x/y`. `5%2` equals 1. `4%2` equals 0.

### Constants

+ A constant is like a bucket (variable) with a lid that is glued shut, and once you store a value inside it, you cannot change that value again.
	+ `const STAY_THE_SAME = 1;`

### JavaScript data types

JavaScript has a small set of primitive data types:
1. Number
2. String
3. Boolean
4. Undefined
5. Null

Checking the data type:
+ `typeof` is a keyword that allows us to check the data type.

### Concatenation

+ JavaScript uses `+` symbol for math when surrounded by numbers, but when any content is a string, it will concatenate the text. 

### String Methods:

+ String methods can be called on a string to modify the string in some way. 

### Data Type Conversion

+ Concatenating empty string changes number to a string.
+ `parseInt()` changes a string to a whole number.
+ `parseFloat()` changes a string to a floating number.

### Dialog Boxes and JS Console

+ alerts (Outputs a string)
+ confirm (Boolean values)
+ prompt
+ Log

### Doing math with JavaScript

#### Arithmetic Operators

<img src= "https://s3.amazonaws.com/after-school-assets/jquery.png">

#### Shorthand Operators

| shortcut  | original  | 
|---|---|
| x += y  | x = x + y  | 
| x -= y  |  x = x - y | 
|  x *= y  | x = x * y  |
|	x *= y	| x = x * y|
| x /= y | x = x / y |
|	x %= y | x = x % y | 

### Conditional Statements

+ A conditional statement is a set of commands that executes *if* a specified condition is `true`. 

```js
if (condition)
  statement_1
[else
  statement_2]
```

### Syntax details

+ JS requires that the conditions in your `if` statement be surrounded by `()`
+ You’ll need to encapsulate your conditional statement with `{}
+ **almost** every line of JS ends with a `;`


### Comparison Operators

+ You can also see that we have a funny looking triple equals `===`. This is how we compare the values of two things. One equal to assign value, triple equals to compare values. The equality operator
+ Here is a list of all of JS comparison values and what they do

<img src="https://s3.amazonaws.com/after-school-assets/jquery2.png">

### Complex Conditionals

+ We can add additional branches to a conditional statement with the `else if` keywords like this:
```js
if (gasTank === 34) {
   console.log('Tank is full.');
 } else if (gasTank > 34) {
    console.log('Oops, tank is overfilled!');
 } else {
  	console.log(’Tank refill mandatory!');
 }
```

### Logical Operators 

+ Here is a list of all the Logical Operators and what they do:

<img src="https://s3.amazonaws.com/after-school-assets/jquery3.png">

### Linking to HTML and websites

+ What do I do with my JavaScript. You write out your JS in a `.js` file and require it in your html files like this:
	+ `<script src="js/myScript.js"></script>`
+ *Go to Learn.co and get some practice using js with the Donut App lab.*

## Conclusions

JavaScript is the foundation that much of the Internet is built upon. These simple building blocks can be combined to do just about anything you can imagine. 
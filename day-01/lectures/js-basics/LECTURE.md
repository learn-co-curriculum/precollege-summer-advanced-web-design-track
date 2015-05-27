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

Welcome to JavaScript! First thing first, let's get the absolute basics down before you do anything else.

**A simple variable declaration**

```javascript
var foo = 'hello world';
```

**Whitespace has no meaning outside of quotation marks**

```javascript
var foo =         'hello world';
```

**Parentheses indicate precedence**

```javascript
2 * 3 + 5;    // returns 11; multiplication happens first

2 * (3 + 5);  // returns 16; addition happens first
```

**Tabs enhance readability, but have no special meaning**

```javascript
var foo = function() {
    console.log('hello');
};
```

### Variables

+ A variable is like a bucket that we can store some data inside and then later change the data it stores.
	+ The bucket has a name that is arbitrary but should make it easy for a developer to understand what goes inside
+ You need to declare variables explicitly in JavaScript with the `var` keyword like this:
	+ `var x;` 
	+ `var` lets JavaScript know that you've just made a variable
+ Naming variables: start with letter (a-z) and can contain 0-9, a-z, A-Z, you can also use `_ `never use spaces ' ' or or illegal characters (! % ?)
+ For variable names consisting of multiple words you should use camelCase or snake_case (camelCase is generally what JS developers use by convention and is called that becauseTheLettersMakeHumpsInTheName)
+ Let's assign a value in x (remember we declared var x; previously)
	+ `x = 10;`
+ I can refer directly to x and change its value using `=` symbol
+ We can also declare and assign a value simultaneously.
	+ `var y = 20;`
+ Declare multiple variables at once using comma separation.
	```js
	var a = 1,
	b = 2, 
	c = 3;
	```
+ We end our statements with semicolons

### Math

+ JavaScript supports the basic math operators you would expect (`+`, `-`, `*`, `/`)
+ Anytime we see an equation in code JS will try to run the equations
	+ So `10*3` becomes `30` to the computer running your code.  
+ Perform math on variables
	```js
	var x = 10, 
	y = 20,
	myMath = x + y;
	//What does myMath equal? (30)

	x = 5;
	myMath = x + y;
	//What does myMath equal now? (25)
```
+ JS also supports something called "Modulo", which we represent with the `%`
+ `x%y` returns the remainder of `x/y`. `5%2` equals 1. `4%2` equals 0.

### Constants

+ A constant is like a bucket (variable) with a lid that is glued shut, and once you store a value inside it, you cannot change that value again.
	+ `const STAY_THE_SAME = 1;`
+ Just like `var`, `const` is a keyword that declares a constant
	+ `STAY_THE_SAME = 2;`
+ How much does STAY_THE_SAME equal now?
	+ Still equals 1… Always equals 1…
+ `const` variables are often named with ALL_CAPS so that developers know not to try and change them

*What are the types of values that I can store inside of variables?*

### JavaScript data types

JavaScript has a small set of primitive data types:
  1. Number
    - examples include: 1, 3.14, 0.13, 100, ...

  2. String
    - examples include:  "a", "World Wide Web"

  3. Boolean
    - true, false

  4. Undefined
    - refers to an absent or unknown value

  5. Null
    - this is a special keyword that means one of two things: no value or empty.  The difference from undefined is that when a variable is null, it is still defined

Checking the data type:
+ `typeof` is a keyword that allows us to check the data type.
```js
const STAY_THE_SAME = 1;
typeof STAY_THE_SAME; //reports type of number 
var hamburger = 'Yumm';
typeof hamburger; //reports type of string
```

### Concatenation

+ JavaScript uses `+` symbol for math when surrounded by numbers, but when any content is a string, it will concatenate the text. If Boolean and a number: `true = 1` and `false = 0`. So `true + 2 = 3`… weird huh? This can produce unexpected results unless we are careful how we use `+` symbol. It’s also good idea to be aware what data types are involved.

```js
var combine = '10' + 5;` //string concatenation
combine; //returns "105"
// adding a string and an integer gives you a string
```

### String Methods:

+ String methods can be called on a string to modify the string in some way. Usually you can figure out what a method is going to do just based on its name. Some examples:
```js
//toUpperCase
	"Foobar”.toUpperCase(); //returns "FOOBAR"
//toLowerCase
	"Foobar".toLowerCase(); //returns "foobar"
//replace
	"Foobar".replace("bar", "baz"); //returns "Foobaz"
	"Foobar".replace(/o/g, "x"); //returns "Fxxbar
```
+ Method Chaining is also possible with the output of one statement feeds into the next one.
	+ `"Foobar".replace(/o/g, "x").toUpperCase(); //returns "FXXBAR"`

### Data Type Conversion

+ Concatenating empty string changes number to a string.
```js
	var stringy = 12 + ' ';
	typeof stringy; //prints “string”
```
+ `parseInt` changes a string to a whole number.
```js
	combineStuff = parseInt('10') + 5;
	combineStuff; //prints 15
```
+ What the heck happens if I try converting text to a number?
```js
	var userName = parseInt('bob'); //returns NaN
	//NaN stands for Not a Number
```
+ What if I want to convert to a floating number instead of an integer?
```js
	var gallonsGas = parseFloat('10.25');
	gallonsGas; //reports 10.25 as number
```
+ `parseInt` stops at whole number and ignores characters that are not numbers. 10xffffff same as 10.12345 becomes 10. Where as `parseFloat` maintains decimal values.

### Dialog Boxes and JS Console

+ alerts (Outputs a string)
	+ `alert('warning do not attempt to cook food using this website!');`
+ confirm (Boolean values)
	+ `var delete = confirm('Are you sure you want to delete this?');` //true or false
+ prompt
	+ `var age = prompt('Please enter your age: ');` //captures the value inserted.
+ Log
	+ `console.log(age);` 
	+ reports the age they entered into the JS Console located in the developer tool window.
	+ *ProTip: This can be a great way to show output of code as you're working. [JSbin](http://jsbin.com/?js,console) or similar editors usually have a console window

### Doing math with JavaScript: 
	+ Arithmetic Operators

<img src= "https://s3.amazonaws.com/after-school-assets/jquery.png">

### Shorthand Operators

| shortcut  | original  | 
|---|---|
| x += y  | x = x + y  | 
| x -= y  |  x = x - y | 
|  x *= y  | x = x * y  |
|	x *= y	| x = x * y|
| x /= y | x = x / y |
|	x %= y | x = x % y | 

### Conditional Statements

+ Who here has done if-then statements in math class? This is a conditional statements
+ A conditional statement is a set of commands that executes *if* a specified condition is `true`. 
+ JavaScript supports two conditional statements: `if-else` and `switch`.
+ Use the `if` statement to execute a statement if a logical condition is `true`. Use the optional `else` clause to execute a statement if the condition is `false`. An `if` statement looks as follows:

```js
if (condition)
  statement_1
[else
  statement_2]
```

+ Example:
```js
var gasTank = 34; //gallons of gas

if (gasTank === 34) {
   console.log('Tank is full');
} else {
    console.log('Tank is not full');
}
```

### Syntax details

+ You can see that there are a few syntax details that you’ll need to pay attention to. What is syntax? Syntax is like the grammar of a programming language. There are certain conventions that you need to follow in order for your program to run properly.
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
+ We can also make more complex conditional statements with logical operators, like this:
```js
if (gasTank === 34) {
    console.log('Tank is full.');
 } else if (gasTank > 34) {
    console.log('Oops, tank is overfilled!');
 } else if (gasTank < 34 && gasTank > 5) {
 		console.log(’Tank refill suggested.');
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
# Loops

## SWBATs
+ Understand how loops run an operation multiple times
+ Understand how an *exit condition* stops a loop
+ Iterate over arrays using for loops and while loops
+ Convert repeatable tasks into loops

## Motivation/Why Should I Care?
+ We've already seen how using Arrays helps us keep track of data in our programs, but what can we do with it? Using loops let's us manipulate our data in powerful ways. 

## Key Points

+ Loops let you repeat a bit of code until an *exit condition* is met
+ A loops *exit condition* is a boolean statement that is evaluated during each loop, if it's false, the loop stops
+ Loops can be very useful for iterating (stepping through) an array and doing something to each element
+ A loop that doesn't have a valid exit condition will run forever and is called an *infinite loop*. These are bad

## Lesson Plan

### Concept  

A loop is one of the foundational tools in any programmers toolkit. It allows a bit of code to be repeated many times. 

### While loop

Let's say we want to make a while loop that adds one to every number in our `numbers` array. It would look like this:

```
var numbers = [0, 1, 2, 5, 9];
var i = 0;
while (i < numbers.length) 
{
  numbers[i] = numbers[i] + 1;
  i = i + 1;
}
```

### For loop

We can accomplish the exact same thing with the more concise `for` loop. It would look like this:

```
var numbers = [0, 1, 2, 5, 9];
for(var i = 0; i < numbers.length; i = i + 1;)
{
  numbers[i] = numbers[i] + 1;
}
```

In a for loop, our *initialization*, *exit condition*, and *increment* all happen in one line separated by a semicolon `;`.
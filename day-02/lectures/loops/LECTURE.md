# Loops

## SWBATs
+ Understand how loops run an operation multiple times
+ Understand how an *exit condition* stops a loop
+ Iterate over arrays using for loops and while loops
+ Convert repeatable tasks into loops

## Key Points
+ Loops let you repeat a bit of code until an *exit condition* is met
+ A loops *exit condition* is a boolean statement that is evaluated during each loop, if it's false, the loop stops
+ Loops can be very useful for iterating (stepping through) an array and doing something to each element
+ A loop that doesn't have a valid exit condition will run forever and is called an *infinite loop*. These are bad

## Lesson Plan

### Concept  

A loop is one of the foundational tools in any programmers toolkit. It allows a bit of code to be repeated many times. This can be useful in many circumstances but is often used in conjunction with arrays. Arrays can have any number of elements and a loop allows us to access each one of those elements and do something with it. 

Let's start with an example array of numbers.
*Get an example set from a student and make an integer based array. (Ask a few review questions: add a number? index? etc…)*

Ok, what if we want to do something to each number. Like add one to each number. We could do it manually: 
```
numbers[0] = numbers[0] + 1;
numbers[1] = numbers[1] + 1;
```
This would take forever though, and what happens when we add or remove something to the array? We would have to add or remove a line of code. This is bad.

A better way to do this is to set up a little machine with instructions on how to iterate (go through) every number in the array and do something specific to each one. We call this a loop.

There are two basic types of loops in JavaScript: `for` loops and `while` loops. They generally accomplish the same thing but their syntax is different.

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

Let's break this down.
+ `var i = 0;` is the *initialization* of our counter variable. Because we increment it with `i = i + 1` it keeps count of which *iteration* (or cycle) we're on. 
+ `i < numbers.length` is our *exit condition*. This is evaluated at the beginning of every loop, if it isn't `true` we stop looping and move to the code after the loop.
+ `numbers[i] = numbers[i] + 1;` is the code we execute on every loop. This adds 1 to each number in the array.
+ `i = i + 1` is where we *increment* our counter. This will usually increase by 1, but doesn't have to. *What would happen if we incremented by 2?*

Try using `console.log(numbers);` both before and after the loop to see how our array has changed. Try using `alert(numbers);` instead

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

Let’s walk through each part of this.

+ `for` is the keyword that we use to set up a loop
+ Inside of the parentheses is where we set up the conditions of our loop
+ We start off by declaring the starting conditions, or *initialization*
+ We usually have a counter variable `i` set to `0`. 
+ *Why do we set it at 0?*
  + Because the first index in our array is 0 - so we want to set up our little machine to pull out each item in the array starting with the item at index 0
+ *Why do we use the variable `i`?* 
  + It’s convention to use the variable `i` because `i` is short for *index* - we are counting through the *indices* of the of the array
+ We close this condition with a `;` to indicate that we are done with these starting instructions for our machine and we’re ready to declare the *exit condition*


+ In the next part of our for loop we set up the *exit condition* for our machine - it’s like saying this machine should keep going until this condition is true
+ The condition here is that our variable `i` must be less than `numbers.length`. 
+ *Why is this the ending condition for our machine? What is numbers.length equal to? Does numbers[5] exist?* 
  + No it doesn’t. We want to make sure we stop our machine before it starts requesting indices that don’t exist. Or in other words - keep going ONLY while `i` is less than the length of the array (5 in this case). 
+ The last condition of the for loop are instructions for how to keep our machine moving. Here we are saying - at the end of each iteration in the loop add one to var `i`. 
+ *What would happen if we didn’t have this condition set?*   
  + We wouldn’t get anywhere! We wouldn’t be iterating at all, because we would just keep trying to change numbers[0] over and over again in an infinite loop.

### Practice

*Everyone create a `iteration.js` doc and try setting up a for loop with a numbers array and alert each number doubled.*

*Do you guys remember what we said yesterday about ALWAYS HAVING YOUR CODE WRAPPED UP IN FUNCTIONS?* 
Everyone go into your `iteration.js` doc and wrap your for loop in a function called `doubleNumbers`. Did you put your numbers array in your function? Is there a better way to do this?

What if we set up the function to accept a numbers array instead of hardcoding one specific array into the function? 
+ Why would that be better? 
+ Set up a new numbers array and call your doubleNumbers array with your new array.

Let’s do one more practice lab with iteration and strings instead of numbers. 
+ Everyone create an array of your top 5 favorites movies.
+ Now create a function called `myFavorites()`
+ This function should take in an array of favorites and for each favorite it should alert to the screen something like “The Shawshank Redemption? That is my favorite too!”
+ Now create a new array of your favorite songs. Try calling the `myFavorites()` function with your favorite songs array.a
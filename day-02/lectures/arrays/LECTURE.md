# Arrays

## SWBAT
+ Understand what an array is and when to use it
+ Initialize, access, and manipulate arrays

## Key Points
+ Arrays are used to store a series of related items
+ Arrays are made up of individual elements
+ Each element has a unique index
+ Arrays have a size
+ Computers start counting at 0

## Lesson Plan

### Concept
Arrays are an ordered list of individual elements.
+ If a variable is a muffin, arrays are the muffin tin.  
+ They make it easy to pass around a bunch of elements (muffins). 
+ Instead of giving someone 12 muffins (variables) and having them juggle, you can give them a muffin tin (array) filled with muffins.  

One example of a real world array is a grocery list. Each item on the list has a index (number) and a element (food item).  Another example would be a parking lot, each space is numbered (index) and contains a car (element).

*Can anyone give me more examples of real world arrays?*

(Draw on board, using one of the students’ examples):

You can also visualize an array as a two-column table where the left column is the index (or the order) and the right column is the thing you’re listing 
<img src= "https://s3.amazonaws.com/after-school-assets/advanced_jquery1.png">

Notice that the index starts at 0. This is a quirk about data structures in computer science The first item in an array is always 0, and it increments by one.
+ One way to think about this is that the computer counts indexes the way we count ages.
+ We start at age '0' and only after our first full year do we turn '1'.

### Initializing arrays

So how do we translate this table into code?
```
[“Danny”, “Lyel”, “Victoria”, “Vanessa”]
```
Remember that the names are data so they must be in quotes as strings.

An array with just numbers would look like this:
```
[3, 345, 42, 98, 7]
```
Square brackets `[ ]` denote the contents of an array.  An array can be stored in a variable just like a number or string.

You'll notice that we don't write the *index* of the *elements* anywhere. The computer automatically makes an index starting at 0 and incrementing by 1 for each element.

(show the index above each item on the board)

Great, we’ve made an array. Let’s go ahead and assign it to a variable so that whenever we call the variable names we have the array returned to us.

```
var names = [“Danny”, “Lyel”, “Victoria”, “Vanessa”];
```
*Model and then have students create a new file in their development directories to hold their array practice code. Have students create their own array of their choice and assign it to a variable. Have students turn to partners and check with each other.*

### Access array elements

Great. We’ve created the array. Now what if I just want to get out one item from the array instead of the whole thing. For example, What if I want to get the third item listed in my array?

We access items in an array using the brackets and the index of the thing you want.

`names[3]` will give me what? (the fourth). how do I get the third item? (0 index means the 1st item is `names[0]`, the second `names[1]` ....)

###Change array element
*So what if we want to change one of the items in the array? Any thoughts on how we can reassign/change an item?*

`names[2] = “Joe”` will change the third item in the array to Joe. (Model this)

### Get the size of an array

Every array also has a *property* that is it's length. 
```
console.log(names.length);
```
Would print out '4' since our names array contains 4 names.  (Notice though that the last element of our array only has an index of '3', this will become important when discussing loops.)

### Add and Remove items from an array

We can also add and remove items from an array. Arrays actually have methods built in to them. Remember that methods are just a set of instructions.

`names.push(“Alfred”)` will add an item with the contents of the argument to the end of the array it is called on. In this case the argument is `"Alfred"` and the array is `names`.
`var lastName = names.pop()` will remove the last item in an array and return it. Since we just added "Alfred" to the end that is what `names.pop()` returns and stores in `lastName`.

Here are some other cool methods: `.sort()`, `.splice()`, `split()`.

[Mini Lab](https://learn.co/admin/lessons/5206): Manipulating arrays (start with array and then have 10 instructions, what does array look like at the end?)
*Answer: ["Peru", "Laos", "Chad", "Cuba", "Togo", "Iraq", "Iran", "Mali", "Oman", "Fiji"]*
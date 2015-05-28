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

Notice that the index starts at 0. This is a quirk about data structures in computer science The first item in an array is always 0, and it increments by one.
+ One way to think about this is that the computer counts indexes the way we count ages.
+ We start at age '0' and only after our first full year do we turn '1'.

### Initializing arrays

```js
[“Danny”, “Lyel”, “Victoria”, “Vanessa”]
```

Square brackets `[ ]` denote the contents of an array.  An array can be stored in a variable just like a number or string.

You'll notice that we don't write the *index* of the *elements* anywhere. The computer automatically makes an index starting at 0 and incrementing by 1 for each element.

```
var names = [“Danny”, “Lyel”, “Victoria”, “Vanessa”];
```

### Access array elements

We access items in an array using the brackets and the index of the thing you want.

`names[3]` will give me what? (the fourth). how do I get the third item? (0 index means the 1st item is `names[0]`, the second `names[1]` ....)

### Change array element

`names[2] = “Joe”` will change the third item in the array to Joe. (Model this)

### Get the size of an array

Every array also has a *property* that is it's length. 

```js
console.log(names.length);
```

### Add and Remove items from an array

`names.push(“Alfred”)` will add an item with the contents of the argument to the end of the array it is called on. In this case the argument is `"Alfred"` and the array is `names`.
`var lastName = names.pop()` will remove the last item in an array and return it. Since we just added "Alfred" to the end that is what `names.pop()` returns and stores in `lastName`.

Here are some other cool methods: `.sort()`, `.splice()`, `split()`.
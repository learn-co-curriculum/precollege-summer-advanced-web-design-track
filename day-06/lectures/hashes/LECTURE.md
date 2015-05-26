# JavaScript Hashes

## SWBATs

+ Understand how a the Hash data structure works conceptually
+ Create Hashes
+ Add, remove, and edit elements
+ Iterate through a hash
+ Nest hashes within one another

## Motivation / Why Should You Care?

Hashes are how the Web talks to itself. Pretty much all the data you see is passed around in a format called JSON which is just a big hash. Hashes allow developers to store and access data without worrying about its order.  

## Lesson Plan

### Key-Value Pairs

Hashes are can be thought of as a grouping of variables. A Hash contains a number of Key-Value pairs, where the Key is the name and the Value can be anything you would store in a variable.

### Create and Initialize a Hash

```js
var ancientMystery = {"dog" : "woof", "cat" : "meow", "fox" : "????"};
```

This syntax defines a Hash and assigns it to a variable called `ancientMystery` with the following Key - Value pairs.

| Key   	| Value  	|
|-------	|--------	|
| "dog" 	| "woof" 	|
| "cat" 	| "meow" 	|
| "fox" 	| "????"  	|  

Notice that the list of Key-Value pairs is contained between `{}` curly braces, has a `:` between the Key and Value, and has a `,` between each Key Value pair.

### Access a Value of a Hash

Accessing the Value associated with a key is very similiar to Array syntax

To discover what a dog says we could type:

```js
console.log(ancientMystery["dog"]);
// outputs "woof"
```

But what does the fox say??

### Change the Value of a Key

If we found out what the fox says we could update the Value like so:

```js
ancientMystery["fox"] = "ring-ding-ding"
```

Our Hash now looks like this:

| Key   	| Value  	|
|-------	|--------	|
| "dog" 	| "woof" 	|
| "cat" 	| "meow" 	|
| "fox" 	| "ring-ding-ding"  	|  

### Delete a Key

### Iterate through a hash

### Nest Hashes

## Conclusion / So What?

## Hints and Hurdles
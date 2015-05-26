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

Hashes are can be thought of as a grouping of variables. A Hash contains a number of Key-Value pairs, where the Key is the name and the Value can be anything you would store in a variable. Hashes are great for storing unordered data that you want to access quickly.

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

Notice that the list of Key-Value pairs is contained between `{}` curly braces, has a `:` between the Key and Value, and has a `,` between each Key-Value pair.

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

But what if we don't want people to know the ancient mystery of what the fox says? We can delete a Key-Value pair like so:

```js
delete ancientMystery["fox"];
```

Now our Hash looks like this: 

| Key   	| Value  	|
|-------	|--------	|
| "dog" 	| "woof" 	|
| "cat" 	| "meow" 	|

### Iterate through a hash

What if we want to discover and iterate through every Key-Value pair in the hash? We can do that using a special `for` loop.

```js
for (keyVariable in ancientMystery)
{
	console.log("The Key is: " + keyVariable);
	console.log("The Value is: " + ancientMystery[keyVariable]);
}
```

Notice that we iterate through each Key in the Hash and give it an arbitrary name, `keyVariable` in this case. To get the Value we need to use the Key and the Hash name, `ancientMystery[keyVariable]`. 

### Nest Hashes

Remember how we said that a Value can be anything that you could store in a variable? Well we can store Hashes in variables, so it follows that we can store a Hash as the Value of our Hash. Nested Hashes! 

```js
var nestedHash = {
	"simple" : "simpleValue", 
	"nested" : {
		"first" : "firstValue", 
		"second" : "secondValue"
	} 
};
```

Here we have a Hash stored as the Value of the Key `nested`:

| Key   	| Value  	|
|-------	|--------	|
| "simple" 	| "simpleValue" 	|
| "nested" 	| {"first" : "firstValue", "second" : "secondValue" } 	|

To access the simple value our syntax is the same as before, `nestedHash[simple]`. To access the Values in our nested hash we would use this syntax

```js
console.log(nestedHash["nested"]["first"]);

// We could also get the nested Hash and store it in a new variable and use that:
var innerHash = nestedHash["nested"];
console.log(innerHash["first"]);

// Both variations print "firstValue" to the console
```

### Dot Notation

Hashes can also be accessed using *Dot Notation*, where instead of brackets `[]` you can place a dot between the Hash and the Keys.  This looks like:

```js
console.log(ancientMystery.dog); // Logs "woof"
console.log(nestedHash.nested.second); // Logs "secondValue"
```

## Conclusion / So What?

Hashes are a great way to quickly store and access data that we want to stay together but isn't ordered and doesn't belong in an array. They are also the foundation for JSON which is how the majority of websites talk to each other and exchange data.

## Hints and Hurdles

+ Be careful about your commas!! They go between Key-Value pairs
+ You generally don't want spaces in your Key's so that you can use dot notation
+ When iterating through a Hash you get the Key and have to use that to access the Value
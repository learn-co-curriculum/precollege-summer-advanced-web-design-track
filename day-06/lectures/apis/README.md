## Intro to APIs

## SWBATs

### JSON

+ Understand how JSON is used on the web
+ Relate JSON to hashes
+ Navigate through JSON structures

### API's

+ Connect to any public facing API
+ Store and access the returned JSON of an API
+ Use callbacks to interpret and act on the returned data 
+ Surface that data to the UI

## Motivation

There are TONS of cool ways to connect other applications to extend our app's functionality API's let us do this.

## Lesson Notes

### What is JSON? 

+ JSON is short for JavaScript Object Notation - it's basically a way of packaging data and sending it out to other places. 

### What is an API?

![Web APIs](http://www.apiacademy.co/sites/default/files/Web-APIs-v5_0.png)
+ API stands for "Application Programming Interface". 
+ In a nutshell, an API is a set of instructions that allows developers to change and control existing web applications. It's a way for the developers of existing applications to allow other people to get their data in a controlled way. 


+ Many of the biggest web applications have APIs: Facebook, Twitter, YouTube, Google Maps, and many more. These APIs allow developers to connect to these applications to use the apps' data in their own development work. 

See if you can identify the use of APIs next time you use the internet.

### Using an API

+ Every API is a little bit different, but in general we can follow a process for connecting to them. 

1. Read the documentation. This is the most important part. Since every API is different, you need to get to know the specific functionality and figure out how to integrate the API.
2. Setup an "API call" - going to get the data
3. Deciding what to do when you get the data back

+ For the most part, the APIs we use will give us back JSON objects that we can use to manipulate our DOM. We can make API calls using jQuery's [getJSON method](http://api.jquery.com/jquery.getjson/)
+ Here's an example: 
```js
$.getJSON("http://api.giphy.com/v1/gifs/search?q=fat+cat&api_key=dc6zaTOxFJmzC", function(response){
	//do something with the response data here!
})
```

## Conclusion/So What? 

+ JSON is a language that allows us to easily access data across multiple platforms.
+ It looks daunting, but it's really just a nested hash. 
+ APIs give us access to ALL kinds of data from all over the internet. We can use this data to make really powerful apps. 
+ Using jQuery, we can make API calls that consist of three parts: 
	+ The call - this is our `$.getJSON` method
	+ The address where we're making our call
	+ Our callback - what should we do with the data when we get it back.
	
```js
$.getJSON(address, function(response){
	//what do to goes here!!
})
```

## Hints and Hurdles

+ This is more complicated than what we covered before - if it takes a little of time to sink in, that's okay! Go slow, break down the problem into steps. 
+ We've pre-selected a few APIs that have nice interfaces - students are HIGHLY encouraged to stick to these for their projects. 




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

There are TONS of cool ways to connect other applications to extend our app's functionality. Want to include GIFs based on user searches? Show Tweets related to your site? We can do this and much, much more using APIs!

## Lesson Notes

### What is JSON? 

+ JSON is short for JavaScript Object Notation - it's basically a way of packaging data and sending it out to other places. 
+ It's essentially just a giant string that we can parse through. 
+ Take a look at this example: http://api.giphy.com/v1/gifs/search?q=fat+cat&api_key=dc6zaTOxFJmzC *Teacher - open have this link open in Google Chrome. Click the "View Source" button to see without the JSON viewer. 
+ So this is just a giant string, but does it remind you of anything? 
	+ It has curly braces
	+ There seem to be key value pairs like this "key": "value", 
	+ Yep, we can treat this like a hash!
+ *Go back to the JSON viewer view* 
+ This Google Chrome Extension formats the JSON object nicely for us to view. 
	+ In this example, we see that this is basically just a hash with three top-level keys - "data", "meta", and "pagination"
+ The "data" key points to an array - if we expand, we see that the array contains more hashes. 
+ Each one represents one search result from Giphy.
+ How could we access the first result from the data array?
	+ `data[0]`
+ Great, now we're in the first result. Inside, there's a key called `images` that points to another hash. How could we access that hash?
	+ `data[0]["images"]`
+ Now inside of the images hash, there are more hashes for different sizes of the images. Let's get inside of the `fixed_height` hash. 
	+ `data[0]["images"]["fixed_height"]`
+ So we can keep going deeper and deeper into the hashes. Now, we can get a url for that image. 
	+ `data[0]["images"]["fixed_height"]["url"]`

+ Now that we're familiar with JSON, let's look at how we can use APIs to make our applications awesome! 

### What is an API?

![Web APIs](http://www.apiacademy.co/sites/default/files/Web-APIs-v5_0.png)
+ API stands for "Application Programming Interface". 
+ In a nutshell, an API is a set of instructions that allows developers to change and control existing web applications. It's a way for the developers of existing applications to allow other people to get their data in a controlled way. 
+ For example, the facebook API has a specific function that allows developers to integrate posting to a facebook wall. The Twitter API has a function that allows developers to display all of a user's tweets.

+ Many of the biggest web applications have APIs: Facebook, Twitter, YouTube, Google Maps, and many more. These APIs allow developers to connect to these applications to use the apps' data in their own development work. Here are just a few ways APIs work in the real world:

+ Signing in to a new website using your Facebook account (OAuth)
+ Using Google Maps inside of the Uber application
+ Being able to send a tweet when you are playing a video game and want to show your progress to friends.

See if you can identify the use of APIs next time you use the internet.

[Here's a great Quora page on APIs for laypeople.](http://www.quora.com/In-laymans-terms-what-is-an-API-1)

[And here's an excellent explanation of API's from How Stuff Works](http://money.howstuffworks.com/business-communications/how-to-leverage-an-api-for-conferencing1.htm)

### Using an API

+ Every API is a little bit different, but in general we can follow a process for connecting to them. 

1. Read the documentation. This is the most important part. Since every API is different, you need to get to know the specific functionality and figure out how to integrate the API.
2. Sign up for an account. 
3. Register your app/get an "API Key"
4. Setup an "API call" - going to get the data
5. Deciding what to do when you get the data back

+ For the most part, the APIs we use will give us back JSON objects that we can use to manipulate our DOM. We can make API calls using jQuery's [getJSON method](http://api.jquery.com/jquery.getjson/)
+ Here's an example: 
```js
$.getJSON("http://api.giphy.com/v1/gifs/search?q=fat+cat&api_key=dc6zaTOxFJmzC", function(response){
	//do something with the response data here!
})
```
+ Let's break that down into pieces.
	+ First, we have our beloved `$` to say "Hey, jQuery, wake up!"
	+ We then call the .getJSON method - a special method which requests and parses a JSON object for us.
	+ getJSON takes two arguments - the first is the URL where it's getting the JSON from. In this case, we're using the Giphy API URL and appending our API key and search keywords. 
	+ The second argument is our callback function - this is what runs when we get our response back. We "pass in" our response as an argument. 
	+ Inside of our callback function, we can do whatever we want with the data we get back. Any jQuery methods could be valid here, such as append HTML to the page
+ For example, we could have our image display on a page by adding an image tag and updating the URL. 

```js
$.getJSON("http://api.giphy.com/v1/gifs/search?q=fat+cat&api_key=dc6zaTOxFJmzC", function(response){
	var url = response["data"][0]["images"]["fixed_height"]["url"]; //sets the URL based on our JSON response
	var image = "<img src='" + url + "'>"; //creates an <img> tag with the src set as the url
	$("body").append(image); // adds the <img> tag to our page!
})
```

+ Let's break down what's happening in our callback. 
	+ We declare a variable, `url`, and set it equal to the fixed_height url from our API call. 
+ We declare a variable, `image`, and save an image tag with a `src` attritube of our `url` variable. This will look something like this: `<img src="http://media1.giphy.com/media/QYR3iycj8fxMQ/200.gif">`
+ We then append that image onto our body. 

Conclusion/So What? 

+ JSON is a language that allows us to easily access data across multiple platforms.
+ It looks daunting, but it's really just a nested hash. 
+ APIs give us access to ALL kinds of data from all over the internet. We can use this data to make really powerful apps. 
+ Using jQuery, we can make API calls that consist of three parts: 
	+ The call - this is our `$.getJSON method
	+ The address where we're making our call
	+ Our callback - what should we do with the data when we get it back.
```js
$.getJSON(address, function(response){
	//what do to goes here!!
})
```

Hints and Hurdles
+ This is more complicated than what we covered before - if it takes a little of time to sink in, that's okay! Go slow, break down the problem into steps. 
+ We've pre-selected a few APIs that have nice interfaces - students are HIGHLY encouraged to stick to these for their projects. 




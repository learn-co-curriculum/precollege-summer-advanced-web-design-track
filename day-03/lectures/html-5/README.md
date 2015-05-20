# HTML-5 - Lecture Notes

## SWBATs

+ Break up a page with divs
+ Understand how to use HTML5 semantic elements - header, footer, nav, etc.
+ Understand how to use HTML5 `audio` and `video` tags

## Motivation

We've already learned some of the basics of using html tags. Today, we're going to use semantic tags to break up and describe the content of our page. We'll also learn about some awesome media tags that are new in HTML5. 

## Why Should I Care?

HTML code can be hard for a human being to read! Breaking up and describing our content makes it easier to collaborate with other programmers. 

### Lesson Plan 


+ We've already learned about some html tags to identify content on our page. *What are some of the different tags we know how to use?* 
	* Let students call some out - p, h1, img, etc. 
+ But what if we have content that goes together? Say that I have an h1, p, and an image that go should stay together on my page. How can I tell my differnet tags that they're in a group together? 

+ We can break up a page with a generic sort of container called a `div`. Div is short for division - it's a very basic way of dividing up our page. We write it like this: 

```html
<div></div>
```
+ Inside of our divs, we can put any other tags that we want. h1, p, img, even other divs. 
+ We can add `class`es and `id`s to these divs to style them however we want. Adding `id`s and `class`es is the only way to differentiate these generic div containers.
+ A `div` can be used for anything - it doesn't describe the content that it's surrounding, which can be confusing and hard to read. 
+ HTML5 provides us with some helpful elements that we can use to break up our page and describe what each section is being used for. These are:
	+ `header`
	+ `footer`
	+ `nav`
	+ `aside`
	+ `section`
	+ `article`
+ These are effectively just `div` elements. You’ll still need to apply styles to these items like:
```css
footer {
	background-color: purple;
	color: white;
	display:block;
	float: right;
}
```
+ But it is a little cleaner and saves you some time by eliminating the need to add a div with the class or ID footer.
+ Not all older browsers support these HTML5 semantic elements and in this case they just show up as a normal `div` element

## Fancy audio/video tags

+ HTML5 makes it super easy to embed video and audio into your website with these tags:
+ Audio:
  ```html
    <audio>
        <source src="audio.mp3" type="audio/mp3">
        <source src="audio.ogg" type="audio/ogg”> 
        <!-– fallback content here -->
    </audio>
  ```
+ Video
  ```html
    <video>
        <source src="movie.mp4" type="video/mp4">
        <source src="movie.ogv" type="video/ogg">
        <source src="movie.webm" type="video/webm”>
        <!-– fall back content here -->
      </video>
  ```
+ The fallback content is important because there are still old browsers out there that are not good at handling HTML5 audio and video elements.
+ Check out this great [resource](http://caniuse.com/) for checking out HTML5 compatibility
+ You can also embed YouTube video's really easily. Just go to the YouTube site for a video you like. Follow these steps:

[Embed a Youtube Video](https://support.google.com/youtube/answer/171780?hl=en)

+ *Try adding an audio or video to your personal website.*
+ iTunes encrypts audio files so they won't be able to be played with the audio tags. Students have to use legally acquired mp3 files - You can download Girl Talk's album for free [here](http://illegalart.net/girltalk/shop/)

### Conclusions

+ So how do we style these `div`s with CSS? Let's find out!!!



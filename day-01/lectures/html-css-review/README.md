#HTML Fundamentals

## SWBATs

+ Structure an html page using `doctype`, `html`, `head` and `body` tags
+ Explain what goes into the head of the document
+ Add text to a page using `p` and `h1` tags
+ Add images using `img` tag
+ Add links using `a` tags and understand the difference between relative and absolute paths
+ Create multiple pages and link them
+ Create an ordered list using `ul` and `ol` tags
+ Use Github Pages to send their websites to family and friends


## Motivation / Why Should You Care?

HTML is the foundational technology for the Internet, every one of your favorite websites is HTML at its core. 

Yesterday you used a prepared template to create personal pages for our student directory. Today you are going to learn how to create an HTML site from scratch, create your own styles for the page and deploy it to the world wide web with GitHub.

## Lesson Plan

### Setup

*Students should be able to follow along with this demo*
+ In Nitrous terminal/command line from inside `development` directory make a directory (`mkdir`) called `my_website`
+ `cd` into that directory and make a `css` directory and an `index.html` file.
+ Add this HTML to `index.html`:

```html
<!doctype html> 
<html></html>
<head></head>
<body></body>
```
### Ideation

People make websites about all sorts of stuff
*Ask the students for some website ideas about things they love.*

### Tag syntax
Every HTML tag has an opening and closing tag with its content in the middle. The tag names are contained within angle brackets, and a closing tag has a `/` before the tag name.

Tags can also have attributes applied to them. These can be thought of as modifying or providing additional information to a tag. A tag can have any number of attributes. These are placed in the opening tag.

### Tag Nesting and Whitespace

Most tags can contain other tags inside of them. When we do this it is customary to indent the nested tags and their content by 2 or 4 spaces. This is to make it easier to read for humans. Using whitespace allows us to much more easily see at-a-glance how the HTML is structured.

However, be careful to close (`</tag>`) the nested tag before closing it's parent tag.

### Headers

One important type of tag is a header. Headers tell your visitors what your site is about. 
+ We also have subheaders we can use - our header tags range from `<h1>` through `<h6>`, which range from largest to smallest.

### Other Tags
+ `<p>` tags, delineate paragraph text
+ `<strong>` will make any text contained within bold
+ `<em>` will italicize text or add *emphasis* 

#### Lists
+ Bullet point lists start with `<ul>` for *unordered list*
+ Numbered lists (computer will automatically count up from 1) start with `<ol>` for *ordered list*
+ The actual list items go between `<li>` tags for, you guessed it, *list items*

#### Links
Links use an `<a>` tag, which stands for *anchor*. If you wanted a link to Google it would look like this:
```html
<a href="http://www.google.com">Super secret link</a>
```
Notice that the `<a>` tag has an `href=""` attribute! href stands for *hypertext reference*. This is where the link will tell the browser to go when clicked. The text between the opening and closing tags are what the user will see.

#### Images
Images use an `<img>` tag to embed an image in a webpage.
```html
<img src="your_image_location">
```
The `src` attribute can be a URL of an image from the Internet or a relative link to an asset on your computer.

## Practice

### Adding sections
For your new website about a thing you love, create three sections describing why you love that thing using the following format:
+ a subheader for the top (using h2-h6 tags)
+ a `p` tag with a short descriptive paragraph
+ an image that goes along with the thing 
+ a link to somewhere on the web where I can find more information about the topic. 

### Adding pages
Add pages to your site by creating three separate html files 
+ Start each page with the proper HTML tag structure (`html`, `body`, `title`, ...)
+ To link to pages in the same site, use an `<a>` tag.
+ Put links in an unordered list using `ul` and `li` tags

## Conclusion / So What?
HTML allows us to define and label the content of our page. Across browsers, there isn't a specification about how text without tags should be rendered. You have no control over how it's displayed, and in future versions of a browser, your code might not be displayed.

## Hints and Hurdles
+ An HTML element is composed of an opening tag, content, and a closing tag
+ Students should have their HTML files in both the browser and in the text editor.

# CSS Fundamentals

## SWBATs

+ Explain the purpose of CSS
+ Use selectors
+ Write CSS Syntax
+ Link a CSS stylesheet to an HTML page
+ Adjust basic properties of text: `font-size`, `font-family`, `text-align`, `font-color`
+ Adjust basic properties of images: `height`, `width`
+ Adjust backgrounds elements
+ Use hexadecimal, rgba, and rgb color values

## Motivation / Why Should You Care?

Have Beyonce’s twitter page up with all stylesheets unlinked (with dev tools can just delete all the link tags). Explain that this is what her twitter looks like with JUST HTML. It’s a lot like what our sites look like with just HTML.

Have students point out things that look different, from what it normally looks like -- all the styling.
So far, all we’ve been able to do is put content on a page with HTML to make some ugly looking websites. So how do we actually make our sites stuff look good? CSS!
CSS stands for Cascading Style Sheets. We write CSS in separate files, so that each file of our web site does one job and one job only. Single purpose files.

*Ask your students what they would want to style about their website? Or the one you have shown.*

## Lesson Plan

### Intro - Selectors and Linking our Stylesheet

+ We write our CSS in a separate file - style is a different job than structure. 
+ Using the `my_website` project we started earlier with HTML, make a `style.css` file inside the `css` directory
+ In `style.css`, let's make our `<h1>`s a different color. 
+ Property and value go between curly braces with colons and semi-colons 
+ Refresh your browser: won't see change because we haven't linked our stylesheet. 
+ Add `<link rel="stylesheet" type="text/css" href="css/style.css">` inside head tag in `index.html`
+ Other styling to play around with:text size, image size, centering text, background color, background image and have them style their page (see code snippets [here](./code_snippet1.md))

### Colors

+ RGB vs Hexadecimal color 
  * RGB- stands for Red, Green, Blue. RGB color model is the ways of getting different colors through adding different amounts of Red, Green, and Blue count up from 0 amounts of each to 255 of each
  * Hexademical is a different notation for the amount of Red, Green, and Blue that gets added to your color.
    * count: 0, 1, 2, 3, 4, 5, 6, 7, ,8, 9, a, b, c, d, e, f (6 values: two red, two green, two blue)
  * [Color Picker](http://www.w3schools.com/tags/ref_colorpicker.asp) is a great resource to find other color tones

### Fonts

+ Google fonts (http://www.google.com/fonts) 
  * Browsers can only display whatever fonts are downloaded on that computer. 
  * Scroll down the page till you see this and make sure `import` is selected: <img src="https://s3.amazonaws.com/after-school-assets/google-font-import.png"> and copy and paste into the top of the CSS file

+ If you haven't already added three pages to your site: create three separate html files and put links to your other pages in an unordered list using ul and li tags

## Deploying to Github Pages

+ Making web pages is really fun, but it's nice to be able to share them with family and friends. Luckily, Github makes it really easy for us to preview our sites using Github Pages!
+ First, we need to initialize a git repository. In the command line from our main project directory, type `git init`. 
+ Next, let's commit our changes.
	+ `git add .` to add all of the files
	+ `git commit -m "a message about our changes"` to make the commit
+ Awesome, let's make a remote repository. 
	+ Go to github.com and click the "+" in the upper right hand corner. 
	+ Give your project the same name as your directory. 
	+ The description is optional.
	+ Choose public
	+ You don't need a README.
+ Nice work! Github now gives us great instructions to add this as a remote repository.
+ The first few lines we've already taken care of, but let's copy the line that begins `git remote add origin` and paste it into our command line.
+ Next, do `git push -u origin master`. We've now pushed our repository up to Github!
+ Lastly, we'll create a branch called `gh-pages`. From the terminal, type `git checkout -b gh-pages`
	+ add and commit your changes on this branch like we did before.
	+ push this branch to your remote repository by doing `git push origin gh-pages`
+ Your site should now be live - nice work! Go to your github repostiory and click settings - you should see a link to the live example. Feel free to share this with your family and friends!

### Conclusion / So What?

CSS allows us to add styling to our page. Together, HTML and CSS give us the web as we know it. In just a few steps, we can publish a live site to the internet to share with family and friends. Nice work! 

### Hints and Hurdles

+ Test all your CSS examples first and know how you're going to live code them

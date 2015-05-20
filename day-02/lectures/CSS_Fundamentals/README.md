# CSS Fundamentals

## Overview

Create a brand new HTML page and style it with CSS

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

Have Beyonce’s twitter page up with all stylesheets unlinked (with dev tools can just delete all the link tags). Explain that this is what his twitter looks like with JUST HTML. It’s a lot like what our sites look like with just HTML.

Have students point out things that look different, from what it normally looks like -- all the styling.
So far, all we’ve been able to do is put content on a page with HTML to make some ugly looking websites. So how do we actually make our sites stuff look good? CSS!
CSS stands for Cascading Style Sheets. We write CSS in separate files, so that each file of our web site does one job and one job only. Single purpose files.

*Ask your students what they would want to style about their website? Or the one you have shown.*


## Lesson Plan


### Intro - Selectors and Linking our Stylesheet

+ We write our CSS in a separate file - style is a different job than structure. 
+ Using the `my_website` project we started earlier with HTML, make a `style.css` file inside the `css` directory
+ In `style.css`, let's make our `<h1>`s a different color. 
+ To make `<h1>` the color red: 
```CSS
h1 { 
  color: red; 
}
```
+ h1 is CSS selector - it selects all of the h1s from our HTML. 
+ Property and value go between curly braces - in this case the property is `color` and the value is `red`
+ Colons and semi-colons are important - they end our statements. 
+ Refresh your browser: won't see change because we haven't linked our stylesheet. 
  * * Aw, it's not working. Does anyone know why it isn't working? *
  * * Our HTML page doesn't know anything about our stylesheet. How can we tell them about each other? *
+ Add `<link rel="stylesheet" type="text/css" href="css/style.css">` inside head tag in `index.html`
  * `rel` attribute: relationship of file being linking
  * `type` attribute: the type of file being linked
  * `href` attribute: where to find the file being linked
    * We have to tell our `index.html` how to find `style.css`, so it needs to go inside css directory first
+ Other styling to play around with:text size, image size, centering text, background color, background image and have them style their page.
  * see code snippets [here](./code_snippet1.md)

### Colors

+ RGB vs Hexadecimal color 
  * There are a few ways to get more specific with color value other than just writing "red". There are many tones of red
  * RGB- stands for Red, Green, Blue. RGB color model is the ways of getting different colors through adding different amounts of Red, Green, and Blue.
    * Count up from 0 amounts of each to 255 of each
    * `rgb(0,0,0)` gives you black
    * `rgb(255,255,255)` gives you white
  * Hexademical is a different notation for the amount of Red, Green, and Blue that gets added to your color.
    * count: 0, 1, 2, 3, 4, 5, 6, 7, ,8, 9, a, b, c, d, e, f
    * 6 values: two red, two green, two blue
    * `#000000` is black
    * `#ffffff` is white
    * `#0000FF` is blue (zero amounts of red and green)
  * [Color Picker](http://www.w3schools.com/tags/ref_colorpicker.asp) is a great resource to find other color tones

### Fonts

+ Google fonts 
  * Browsers can only display whatever fonts are downloaded on that computer. 
  * If a web application is using some random font that my computer doesn't have, I won't be able to see it
  * [Google fonts](http://www.google.com/fonts) is a great resource
  * Click the quick view button <img src="https://s3.amazonaws.com/after-school-assets/google-font-quick-view.png" height="30px">
  * Scroll down the page till you see this and make sure `import` is selected: <img src="https://s3.amazonaws.com/after-school-assets/google-font-import.png">
  * Copy that the `@import`... text and paste it at the top of your CSS file
  * Step 4 shows you how to use the font: <img src="https://s3.amazonaws.com/after-school-assets/google-font-usage.png">
    * They chose to style the `font-weight` property as well, you can ignore that
  ```css
    h1 {
      font-family: 'Metrophobic', Arial, serif;
    }
  ```


+ If you haven't already added three pages to your site: create three separate html files 
+ Inside of those files set up your html file structure
+ Put links to your other pages in an unordered list using ul and li tags
  * We will style these links as a nav bar in our next class. 

### Conclusion / So What?
CSS allows us to add styling to our page. Together, HTML and CSS give us the web as we know it. 

### Hints and Hurdles
+ Test all your CSS examples first and know how you're going to live code them. It's easy to make mistakes here that are hard to get out of on the spot. 

###SWBATS
***Students will create their own profile page using HTML!***

  + Create, read, and understand a simple page using html tags
  + Add an image to a page using the img tag
  + Experiment with unknown CSS tags
  + Add text to a page using p and h1-h6 tags
  + Create an ordered and unordered list using the ol, ul, li tags
  + Structure an html page using doctype, html, head, title, body tags
  + Organize chunks of html with div tags
  + Add a link to a page using the a tag
  + Create relative links within a site

### Motivation / Why Should You Care?
+ Start with an altered tweet from Justin Bieber on the screen using the dev tools that says “I LOVE FLATIRON SCHOOL AND CODING. EVERYONE SHOULD ATTEND AFTER SCHOOL.”  
  * Don’t have dev tools up. 
  * Let them know by the end of the lesson they’ll learn how we did that.
+ Ask students for their favorite websites and bring it up on the screen and click ‘view source’
  * This code is all the code that was written for this page. and by the end of the day some of that code will make total sense. 
+ Web pages are made up of two things: HTML and CSS. First we’re going to start with HTML. HTML, hypertext markup language, is the structure and content of a web page. HTML doesn’t have anything to do with the layout of text on a page, or of how the page looks. All it does is tell the browser what different types of content is on the page. 
  * We use HTML to mark a navigation bar, tell the browser that this piece of content is an article, this is a caption related to this image, this is a menu with items on it, etc.
  * Computers are stupid and can’t infer knowledge the way we can. "Semantic tags" (descriptive tags that tell us what type of content the tags contain) let computers know the type of content. 
    * Web crawlers like google’s use HTML to actual determine what text on a page is content, which helps Google put your page in search results. 
    * Services like Pocket and Embedly use it to pull articles to save to your reading list, without pulling the entire site. 
    * Ever been frustrated that you didn't have an option to translate a page from another language into English? HTML tags control that

### Lesson Plan

[Lab: Student Directory Project](https://github.com/learn-co-curriculum/hs-intro-web-student-directory)

Today, we'll be building a student directory with all of your profile information on it. By the end of this project, you'll have deployed live, working code to the internet the same way professional web developers do. 

+ `cd` into this new directory we just cloned and open up the entire thing in your text editor
+ Open up index.html in your text editor - then right click on the page and click `open in browser` 
  * This is what the home page of our student directory looks like. 
  * I’ll be adding your photos and names here. 
  * Click on the sample student to see what your personal profile page will look like. - just a template. You'll be customizing your own
+ Walkthrough of the directories and files in this directory. I’m going to go from the bottom to the top. 
+ `README.md`: holds instructions on how to complete the lab. There will always be a README file in the labs and it contains the text that is displayed on Learn.
+ `index.html`: It is standard convention to name a home page index.html. 
  * When we deploy this student directory, the browser rendering the page will automatically look for an `index.html` file in the root of the project and render that as the homepage. We’ll be talking more about this process tomorrow.
+ `students` directory: It’s going to hold all of the individual files for each of your profiles. 
  * Click on the arrow to expand the page. You can see we have our student template page there, but you need to add your own page. 
+ In terminal from inside the main directory for this project:
  * enter `ls` 
  * `cd students` 
  * Create a new html file create a new file that is named like this ‘vanessa-dean.html’ except with your own name.
    * `touch your-name.html`
+ `css` directory: holds all of the files in charge of styling our pages. 
  * We have a directory for our custom fonts
  * A `font-awesome` directory that holds the custom icons we are using on the page
  * `style.css` CSS stands for cascading style sheets. Our styles are all set for this project, but you’re going to learn how to create your own custom style sheets in the next class.
+ `img`directory: You are going to be adding your own files here inside of the `students` directory. 
  * We’ll need an image of your face and also a background image.
+ `js` directory: You’ll be learning more about javascript later in this course
+ open `student-profile.html` and copy all of the code there and paste it into your new `your-name.html` file
  * We are going to use this student profile as a template for today so you can get used to HTML structure and syntax.

+ `<!doctype html>`:  tells our browser we're using HTML5 
+ `<html>`: opening HTML tag. Closing tag `</html>` is at the bottom.
+ Opening a closing tags create little baskets. Inside of this html basket we are going to nest all of our html.
+ `<head> </head>`You can see our head opening tag here and closing tag here. 
  * The head of our document is where we store all of the meta data - stuff that is important to our site but we don't see in the browser
+ `<title></title>`: shows text in the tab in the browser
+ `<link>`: link to stylesheets
  * Styling stays separate
  * `<style></style>`: bad practice
+ `<body></body>`: 
  + `ids` and `classes`: use these to help with CSS. We'll get into this later
+ Header: Comments mark the header
  *This grayed out text is called a comment.
  * HTML structure for our header or nav bar. You can see that I’ve made a note that this is the beginning of the header. 
+ Scroll to where you see the comment: `<!--Begin Splash Image-->`
+ `<img>`  tag:
    * Doesn't have a closing tag
    * `src="#"`: attribute of the img tag. stands for source
    * Which photo does this src point to now?
+ Students save a photo of themselves in the `img/students` directory and change the `src` 
+ `<h4></h4>`: header tags
  * h1-h6
  * Add Student name
+ `<a href="#"></a>`: link.
  * `href=""` attribute. hyper-reference - where the link goes
  * text between the opening and closing tags is the text you click
  * Change their social icons
+ `<div></div>`: invisible box that clumps content together
+ `<p></p>` paragraph tags. 
+ `<ul></ul>`: unordered list.
+ `<li></li>`: list item. 
+ Give them time to customize their pages
+ For students who finish this up really quickly have them try out the [HTML Playground lab](https://github.com/learn-co-curriculum/html-playground).

### Conclusion / So What?
HTML makes up every single page on the internet. You can't create a web page without it. 

### Hints and Hurdles
+ Indentation does not matter to our browser when it reads the html and displays it but it is SUPER important for humans reading our code.
  * Indentation helps us keep track of what is nested where and helps us to check for our opening and closing brackets. 

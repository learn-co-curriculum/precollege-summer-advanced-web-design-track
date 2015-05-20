
###Motivation
We’re starting to make some complex HTML pages and sometimes you need to get really specific about the element you are styling. Today we are going to go into more depth about how to use selectors to be very specific about styling elements on the page and keep our CSS stylesheets nice and clean.

###Lesson Plan

+ We’ve already learned how to use selectors. What are selectors? html tags `<p>`,`<h1>`, etc. and classes and IDs.
+ We can target elements on our page by specifying where one selector is in relation to another with a few different selector - today we'll talk about two:
  + Descendent Selectors
    + `#nav li`
  + Pseudo Selectors
    + `a:hover`

#### Descendent Selectors

+ A descendent selector targets the last selector listed (li in the example above), using the previously listed selectors to narrow its scope. Let's look at `#nav li`: What this css selector is saying is that we should target only those li’s that are nested within `#nav`. Any `li` element outside of the element with the `#nav` id would be unaffected.
+ To select descendents, your selection should list the 'parent' element and then the child(ren) that you're looking to select. For example, an `<a>` tag (child) inside of `<div id="pop">` (parent) would be listed as `#pop a` OR `div#pop a`. The space in between the two selectors indicates descendence.
+ If we have a list within a list like this:
```html
  <ul id="nav”>
    <li>child
     <ul><li>grandchild</li></ul>
     </li>
  </ul>
```
+ Remember, because of cascading `#nav li` will target not only the child `<li>`, but it will also affect grandchildren, etc.

+ There are a few other helpful selectors that we can use: Universal `* {…}`, Attribute `img[alt="Cat"] {…}` and Pseudo selectors `li:first-child {…}`, `a:link {…}`
+ The universal selector will do exactly what you think it will. It will affect every element on the page. 

#### Pseudo Selectors

+ Pseudo class selectors are especially helpful in styling links. For example:

<img src= "https://s3.amazonaws.com/after-school-assets/css-selector2.png">

+ Cleaning up and streamlining your CSS stylesheet is another way to make it easier to keep track of which elements you are styling and make sure you are targeting the right elements. If there are several things on the page that you want styled in a similar fashion you can use compound selectors. For example, if I want all my h2 and h3 tags to be purple I can indicate that like this:
```css
  h2, h3 {
    color: purple;
  }
  ```

+ One last important bit of CSS are the rules around authority and inheritance.
+ If you use conflicting styles on the same element, ID over rules class which overrules type which over rules * (universal). 
  + Generally the more specific a selector the more authority it has. If a more specific selector is not defined for an element it will inherit styles from a previously defined general selector statement.
+ If multiple Classes are applied to the same element the Class listed furthest to the right overrules its neighbors to the left.
+ Uses “last man” rule. When conflicts with equal authority arise, CSS will listen to the last style it was told to apply. 
+ Now you know everything about CSS! *Time for some practice!*

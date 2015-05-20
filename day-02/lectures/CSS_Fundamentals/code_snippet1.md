##CSS Examples To Get You Through

###Text Size

```html
  <p> Here is a small paragraph. </p>
```

```css
  p {
    font-size: 30px;
  }
```

###Image Size
Note that setting both `width` and `height` may cause an image to stretch. Typically It's best practice to set one or the other and let the image scale appropriately.
```html 
  <img src="https://s3.amazonaws.com/after-school-assets/kitten-teacup.jpg">
```
```css
  img {
    width: 50px;
  }
```

### Centering Text

```html
  <h2> I love kittens </h2>
```

```css
  h2 {
    text-align: center;
  }
```

###Centering an Image
The text-align property doesn't work on images, BUT you can place the image in a div and apply the styling directly to the div. Any of the content in the div, (any other text or images) will all be centered as well.

```html
  <div id="center-image">
    <img src="https://s3.amazonaws.com/after-school-assets/kitten-teacup.jpg">
  </div>
```

```css
  #center-image {
    text-align: center;
  }
```

###Background Color

```html
  <body>
    <!--code for page goes here -->
  </body>
```

```css
  body {
    background-color: green;
  }
```

###Background Image
```html
  <body>
    <!--code for page goes here -->
  </body>
```

```css
  body {
    background-image: url("https://s3.amazonaws.com/after-school-assets/kitten-teacup.jpg");
  }
```
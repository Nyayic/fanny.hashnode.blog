---
title: "How to Create a Responsive Navigation Menu using HTML, CSS and JavaScript"
seoTitle: "How to create a Responsive navigation menu using HTML and CSS"
seoDescription: "Are you ready to learn how to create a responsive navigation menu using HTML and CSS? It's easier than you might think!"
datePublished: Tue Mar 28 2023 05:00:39 GMT+0000 (Coordinated Universal Time)
cuid: clfrsi1w801tarunvdbu5dia8
slug: how-to-create-a-responsive-navigation-menu-using-html-css-and-javascript
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679561459322/457bcec4-88f1-4da9-af58-08361fca1864.jpeg
tags: css, javascript, html5, navigation, 2articles1week

---

Are you ready to learn how to create a responsive navigation menu using HTML, CSS and some small Javascript? It's easier than you might think! Follow these simple steps and you'll have a sleek and professional-looking navigation menu in no time.

## Step 1: Set up your HTML structure

First, open your favorite text editor and create a new HTML document. For this example, let us call it `index.html`.

Inside the `index.html` create an HTML structure by pressing `Shift+!` and hit enter and you will have `HTML boilerplate` set up for you which will look like this:

```xml
<!DOCTYPE html>
<html>
  <head>
    <title>Document</title>
   </head>
  <body>
       
  </body>
</html>
```

You will rename the title to:

```xml
<title>Responsive Navigation Menu</title>
```

## Step 2: Link Necessary files

So after creating the HTML structure and modifying the title, let us link some files that we shall use for the project: These files are 

* The font awesome file: is responsible for the menu icon got from [CDN here](https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css).
    
* Our CSS file which we shall separately create as `index.css`
    
* The javascript file that we shall create as `index.js`
    

we shall link them to our HTML file within the `<head>` region of the HTML structure

```xml
<!-- FONTAWESOME FROM CDN -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
    <!-- CSS FROM OUR CUSTOM STYLE -->
    <link rel="stylesheet" href="./index.css">
    <!-- SCRIPT -->
    <script src="./index.js"></script>
```

## Step 3: Add HTML code for Navigation

Here's an example of what your HTML code should look like:

```xml
<div class="nav" id="navbar">
   <a href="#home" class="active">Home</a>
   <a href="#about">About</a>
   <a href="#blog">Blog</a>
   <a href="#contact">Contact</a>
   <a href="javascript:void(0);" class="icon" onclick="myNav()">
     <i class="fa fa-bars"></i>
   </a>
</div>
```

  Let's go understand each of these

```xml
<div class="nav" id="navbar">
```

This line of code creates a div element with two attributes: class and id. `class` is set to `"nav"`, and `id` is set to `"navbar"`. This div will contain all the links for the navigation bar.

```xml
<a href="#home" class="active">Home</a>
```

This line of code creates an anchor element `(<a>)` that represents the `"Home"` link. The `href` attribute is set to `"#home"`, which means that when the link is clicked, it will navigate to the element on the page that has an id attribute of `"home"`.

The class attribute is set to `"active"`, which means that this link will be highlighted or styled differently to indicate that it is the current page.

```xml
<a href="#about">About</a>
```

This line creates an anchor element that represents the `"About"` link. The `href` attribute is set to `"#about"`, which means that when the link is clicked, it will navigate to the element on the page that has an `id` attribute of `"about"`.

***The same explanation applies to the other contact, blog, pages***

```xml
<a href="javascript:void(0);" class="icon" onclick="myNav()"
  <i class="fa fa-bars"></i>
</a>
```

This line defines another anchor element with a `href` attribute of `"javascript:void(0);"`. This means that clicking on this link will not navigate to a new page, but instead will execute the JavaScript function called `"myNav()"`. 

This function will be defined elsewhere in the code `(in index.js)`. 

The class `"icon"` is added to this link, which may be used to style it as an icon. The `<i>` element inside this link defines an icon using the Font Awesome library. The `"fa-bars"` class is used to display the `"bars"` icon, which is commonly used to represent a navigation menu.

## Step 4: Style your navigation menu with CSS

Now that you have your HTML structure in place, it's time to style your navigation menu with CSS.

```css
body {
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
}
```

This sets the margin of the body element to zero and sets the font family to Arial, Helvetica, and sans-serif.

```css
.nav {
  overflow: hidden;
  background-color: #0e0439;
}
```

This code sets the overflow of the nav element to hidden and sets the background color to `#0e0439`.

```css
.nav a {
  float: left;
  display: block;
  color: #f2f2f2;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 17px;
}
```

This block styles the anchor elements within the `nav` element. It sets the `float` to `left` so that the links appear next to each other, sets the `display` to `block` so that they take up the full width of the `nav` element sets the `color` to `white`, set the `padding` to `14 pixels` on top and bottom and `16 pixels` on the left and right, text-decoration none, remove the underline from the links and sets the font size to `17 pixels`.

```css
.nav a:hover {
  background-color: #3abef6;
  color: black;
}
```

This block styles the `hover` state of the `anchor` elements. When the mouse hovers over a link, the background color changes to a lighter blue and the text color changes to black.

```css
.nav a.active {
  background-color: #3abef6;
  color: white;
}
```

This code styles the active state of the anchor elements. When a link is currently active (meaning it is the current page), the background color changes to a lighter blue and the text color changes to white.

```css
.nav .icon {
  display: none;
}
```

This block of code hides the `icon` element within the nav element. This is used for mobile devices where the navigation links are hidden and replaced with icons.

## Step 5: Make your navigation menu responsive

To make your navigation menu responsive, add a media query to your CSS code. This will adjust the layout of your menu for smaller screens such as mobile devices.

```css
@media screen and (max-width: 600px) {
  .nav a:not(:first-child) {display: none;}
  .nav a.icon {
      float: right;
      display: block;
  }
}
```

This code defines a media query that applies styles only when the screen width is less than or equal to `600 pixels`. It hides all the navigation links except for the first one and shows the icon element on the right side of the nav element.

```css
@media screen and (max-width: 600px) {
  .nav.responsive {position: relative;}
  .nav.responsive .icon {
      position: absolute;
      right: 0;
      top: 0;
  }
  .nav.responsive a {
      float: none;
      display: block;
      text-align: left;
  }
}
}
```

This block of code defines another media query that applies styles only when the screen width is less than or equal to `600 pixels`. 

It sets the position of the `nav` element to `relative`, sets the `position` of the icon element to `absolute` so that it appears on top of the navigation links, and changes the alignment of the navigation links to `left`. This creates a dropdown menu when the icon is clicked.

## Step 6: Add some Javascript

So let us add a simple JavaScript function that is triggered when the user clicks on the icon element in the navigation bar.

```javascript
function myNav() {
  var x = document.getElementById("navbar");
  if (x.className === "nav") {
    x.className += " responsive";
  } 
  else {
    x.className = "nav";
  }
}
```

### Let’s understand what each line does:

```javascript
function myNav() {
```

This line declares a function called `myNav()`.

```javascript
  var x = document.getElementById("navbar");
```

This line uses the `document.getElementById()` method to get the HTML element with the ID `"navbar"` (do you remember the id we created in our index.html ?)and assigns it to a variable called `x`. This element is the navigation bar that we want to manipulate.

```javascript
  if (x.className === "nav") {
```

This line checks if the `className` property of the x element is equal to `"nav"`. This is the class name for the navigation bar.

```javascript
    x.className += " responsive";
```

If the `className` is equal to `"nav"`, this line adds the class name `"responsive"` to the x element's `className` property. This class is defined in the CSS code and it changes the display of the navigation links to a dropdown menu.

```javascript
 } else {
    x.className = "nav";
  }
```

If the `className` is not equal to `"nav"`, this line sets the className property of the `x` element back to "nav". This removes the `"responsive"` class from the `x` element and restores the default display of the navigation links.

So essentially, this function toggles the `"responsive"` class on and off the navigation bar when the user clicks on the icon, which changes the display of the navigation links to a dropdown

## Step 7: Let's put it all together

So here is  a summary of all that we have done in all the three files:

### Index.html

Our `index.html` file shall look like this:

```xml
<!DOCTYPE html>
<html>
  <head>
    <title>Responsive Navigation Menu</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
    <link rel="stylesheet" href="./index.css">
    <!-- SCRIPT -->
    <script src="./index.js"></script>
  </head>
  <body>
    <div class="nav" id="navbar">
        <a href="#home" class="active">Home</a>
        <a href="#about">About</a>
        <a href="#blog">Blog</a>
        <a href="#contact">Contact</a>
        <a href="javascript:void(0);" class="icon" onclick="myNav()">
          <i class="fa fa-bars"></i>
        </a>
    </div>
  </body>
</html>
```

### Index.css

And our `index.css` file shall have the:

```css
body {
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
}
.nav {
  overflow: hidden;
  background-color: #0e0439;
}
.nav a {
  float: left;
  display: block;
  color: #f2f2f2;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 17px;
}
.nav a:hover {
  background-color: #3abef6;
  color: black;
}
.nav a.active {
  background-color: #3abef6;
  color: white;
}
.nav .icon {
  display: none;
}

@media screen and (max-width: 600px) {
  .nav a:not(:first-child) {display: none;}
  .nav a.icon {
      float: right;
      display: block;
  }
}

@media screen and (max-width: 600px) {
  .nav.responsive {position: relative;}
  .nav.responsive .icon {
      position: absolute;
      right: 0;
      top: 0;
  }
  .nav.responsive a {
      float: none;
      display: block;
      text-align: left;
  }
}
```

### Index.js

And finally, our `index.js` file shall look like this:

```javascript
function myNav() {
  var x = document.getElementById("navbar");
  if (x.className === "nav") {
    x.className += " responsive";
  } 
  else {
    x.className = "nav";
  }
}
```

## The Outcome

Congratulations! You've just created a simple responsive navigation menu using HTML, CSS and Javascript. Now you can add this code to your website and impress your visitors with sleek and user-friendly navigation.

[View Demo](https://thecode-chic.github.io/responsive-html-css-navigation-menu/)
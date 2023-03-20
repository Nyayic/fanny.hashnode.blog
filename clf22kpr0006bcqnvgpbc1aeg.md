---
title: "How to Create a Custom tooltip with HTML and CSS"
seoTitle: "How to Create a Custom tooltip with HTML and CSS"
seoDescription: "Tooltips are a great way to provide additional information or context to your website visitors without cluttering up your design."
datePublished: Fri Mar 10 2023 05:00:39 GMT+0000 (Coordinated Universal Time)
cuid: clf22kpr0006bcqnvgpbc1aeg
slug: how-to-create-a-custom-tooltip-with-html-and-css
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679302031053/2ec4522f-e869-44ce-883a-0b50c4bd809f.jpeg
tags: css3, css, tooltips

---

Have you ever hovered over an element on a website and a little box appeared with some extra information? That's called a tooltip! Tooltips are a great way to provide additional information or context to your website, and visitors, without cluttering up your design.

In this article, we'll go over how to create a custom tooltip using HTML and CSS, perfect for beginners who want to spice up their websites.

Let's start by creating the HTML structure for our tooltip. We'll need a container element that will hold the tooltip text and an element to which we want to attach the tooltip to. Here's an example:

```xml
<div class="tooltip">
  <span class="tooltip-text">Tooltip text goes here</span>
  Hover over me to see the tooltip!
</div>
```

In the above we've created a `div` element with a class of **"tooltip"**. Inside that `div`, we have a `span` element with a class of **"tooltip-text"**, which will hold the text that will be displayed in the tooltip. Finally, we have some text that we want to attach the tooltip to.

Now, let's add some CSS to make our tooltip look nice. We'll start by hiding the tooltip text by default and setting up the basic styles for the container and text:

```css
.tooltip { 
    position: relative; 
    display: inline-block; 
    padding-top:20px ;
}

.tooltip .tooltip-text { 
    display: none; 
    position: absolute; 
    z-index: 1; 
    bottom: 100%; 
    left: 50%; 
    margin-bottom: 5px; 
    padding: 5px; 
    border-radius: 5px; 
    background-color: #333; 
    color: #fff;
    transform: translateX(-50%); 
}
```

Let's break down what we're doing here. First, we set the position of the container to `relative` so that we can position the tooltip text relative to it.

Then, we set the display of the tooltip text to `none` so that it's hidden by default. We position the tooltip text absolutely and give it a high `z-index` so that it appears on top of other elements.

We position it `bottom: 100%` so that it appears above the container element, and `left: 50%` so that it's centered horizontally.

We add some margin and padding to make it look nice and give it a `border-radius` to make it `rounded`. Finally, we give it a background color and text color to make it stand out, and use `transform: translateX(-50%)` to center it horizontally.

Now that we have our basic styles set up, let's add some interactivity to show the tooltip text when we hover over the container element:

```css
.tooltip:hover .tooltip-text { 
    display: block; 
}
```

Here, we're using *the* `: hover` pseudo-class to target the tooltip text when the container element is being hovered over. We set the display of the tooltip text to block to make it appear when the container is being hovered over.

And that's it! With just a few lines of HTML and CSS, we've created a custom tooltip that looks great and adds some extra functionality to our website. Here's the full code:

```xml
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tooltip Example</title>
  <style>
    .tooltip {
      position: relative;
      display: inline-block;
      justify-content: center;
      padding-top: 20px;
    }
    .tooltip .tooltip-text {
      display: none;
      position: absolute;
      z-index: 1;
      left: 50%;
      margin-bottom: 5px;
      padding: 5px;
      border-radius: 5px;
      background-color: #333;
      color: #fff;
      transform: translateX(-50%);
      }
    .tooltip:hover .tooltip-text {
        display: block;
    }
  </style>
</head>
<body>
  <div class="tooltip">
    <span class="tooltip-text">Tooltip text goes here</span>
    Hover over me to see the tooltip!
  </div>
</body>
</html>
```

One thing to keep in mind when using tooltips is to make sure they're accessible to everyone, including users who rely on assistive technologies like screen readers.

To make your tooltips accessible, you can use the `aria-describedby` attribute to associate the tooltip text with the container element, like this:

*Feel free to play around with the styles to create your own custom tooltip. You can change the colors, font size, and position to fit your design.*

```html
<div class="tooltip" aria-describedby="tooltip-text">
  Hover over me to see the tooltip!
  <span id="tooltip-text" class="tooltip-text">
    Tooltip text goes here
  </span>
</div>
```

By using the `aria-describedby` attribute, you're telling screen readers that the tooltip text is related to the container element, and they can announce it to the user accordingly.

In conclusion, creating a custom tooltip using HTML and CSS is one of the ways to add some extra functionality to your website without cluttering up your design. By following the steps outlined in this article, you can create your own custom tooltips in no time.

Just remember to keep accessibility in mind and have fun!
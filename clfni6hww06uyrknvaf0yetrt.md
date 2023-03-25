---
title: "Understanding CSS Grid: A Comprehensive Guide"
seoTitle: "Basics of CSS Gride"
seoDescription: "With CSS Grid, you can create rows and columns, and then place elements within those rows and columns."
datePublished: Sat Mar 25 2023 05:00:39 GMT+0000 (Coordinated Universal Time)
cuid: clfni6hww06uyrknvaf0yetrt
slug: understanding-css-grid-a-comprehensive-guide
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679462927626/111eebb6-e92b-40e0-8371-414041aec998.jpeg
tags: css3, css, css-grid, 2articles1week

---

CSS Grid is a powerful tool that allows web developers to create complex layouts quickly and easily. It's a relatively new addition to the CSS language, but it's already changing the way we think about web design.

Let us take a comprehensive look at CSS Grid and everything you need to know to use it effectively in your projects.

## What is CSS Grid?

CSS Grid is a layout system that allows you to create two-dimensional grid layouts with rows and columns. It provides an intuitive and flexible way to structure content on a web page.

With CSS Grid, you can control the size, position, and alignment of elements in a grid container, which makes it an ideal choice for creating responsive designs.

## How Does CSS Grid Work?

With CSS Grid, you can create rows and columns, and then place elements within those rows and columns.

An example of how CSS Grid works:

First, you need to create a container element that will hold all of your grid items. You can use any HTML element as the container, but an `<div>` element is often used.

Next, you'll define the grid template for your container element. This is done using the `grid-template-columns` and `grid-template-rows` properties.

For example, if you want a grid with three columns and two rows, you would use the following CSS:

```css
.container { 
    display: grid; 
    grid-template-columns: repeat(3, 1fr); 
    grid-template-rows: repeat(2, 1fr); 
} 
```

This code creates a grid with three columns and two rows, where each column and row is one fraction of the available space `(1fr)`.

Now that you've defined the grid template, you can start placing elements within the grid using the grid-column and grid-row properties.

For example, if you want to place an element in the second column and first row of the grid, you would use the following CSS:

```css
 .item { 
    grid-column: 2; 
    grid-row: 1; 
} 
```

This code places the `.item` element in the second column and first row of the grid.

You can also use the `grid-area` property to define both the starting and ending grid lines for an item in one go.

For example:

```css
.item { grid-area: 1 / 1 / 2 / 3; } 
```

This code places the .item element in the first row and spans two columns (from grid line 1 to grid line 3).

You can also use the `grid-gap` property to add space between grid items. For example:

```css
.container { grid-gap: 20px; } 
```

This adds a `20px` gap between all grid items in the `.container` element.

That's the basics of how CSS Grid works!

### **The grid container**

The Grid container is an element that contains all the grid items. It defines the grid's overall structure by specifying the number of rows and columns and their sizes.

A grid container is an element that contains grid items and defines the overall structure of a CSS grid layout. It's created using the display: grid property.

Here's an example of a grid container:

```css
.container { 
    display: grid; 
    grid-template-columns: repeat(3, 1fr); 
    grid-template-rows: repeat(3, 100px); 
    gap: 10px; 
}
```

In this example, we're creating a grid container with three columns and three rows. The `grid-template-columns` property defines the width of each column, and the grid-template-rows property defines the height of each row.

We're using the `repeat()` function to specify that we want three columns and three rows with a height of `100 pixels` each. The `1fr` value for the columns means that each column should take up an equal amount of space.

We're also using the `gap property` to add a `10 pixel` gap between grid items. This property sets the gap between grid rows and columns, so in this case, it will create a `10 pixel` gap between each grid item.

An illustration of what this grid container might look like:

```css
 _______________________________
|             Row 1             |
|__________|__________|_________|
|          |          |         |
| Column 1 | Column 2 | Column 3|
|          |          |         |
|__________|__________|_________|
|             Row 2             |
|__________|__________|_________|
|          |          |         |
| Column 1 | Column 2 | Column 3|
|          |          |         |
|__________|__________|_________|
|             Row 3             |
|__________|__________|_________|
|          |          |         |
| Column 1 | Column 2 | Column 3|
|          |          |         |
|__________|__________|_________|
```

In the above example, we have a grid container with three columns and three rows. Each column is `1/3` of the container's width, and each row is `100` pixels high.

The gap property adds a `10 pixel` gap between each grid item. We could then add grid items to this container and position them using the `grid-column` and `grid-row` properties.

### **Grid Items**

Grid Items are elements that are placed inside the grid container. Each item can span across one or more grid cells, which allows for flexible layouts.

Grid items can be positioned using grid lines, which are horizontal and vertical lines that define the grid's rows and columns.

Grid items are the elements that are placed inside a grid container and are positioned using the grid lines created by the grid tracks. Grid items can span one or multiple grid tracks and are placed at the intersection of the grid tracks.

In this way, grid items can be positioned precisely within the grid layout, allowing for flexible and dynamic layouts.

Examples of grid items:

```css
.item-a {
  grid-column: 1 / span 2;
  grid-row: 1 / 2;
}
.item-b {
  grid-column: 3 / 4;
  grid-row: 2 / span 2;
}
.item-c {
  grid-column: 2 / 3;
  grid-row: 2 / 3;
}
```

In this example, we have three grid items: item-a, item-b, and item-c. Let's break down what each of these grid items is doing:

`item-a:` This grid item spans two columns starting from the first column (grid-column: 1) and goes up to the second column `(grid-column: span 2)`. It also spans one row starting from the first row `(grid-row: 1)` and going up to the second row `(grid-row: 2)`.

`item-b:` This grid item spans one column starting from the third column `(grid-column: 3)` and goes up to the fourth column `(grid-column: 4)`. It also spans two rows starting from the second row `(grid-row: 2)` and goes up to the third row `(grid-row: span 2)`.

`item-c:` This grid item spans one column starting from the second column `(grid-column: 2)` and goes up to the third column `(grid-column: 3)`. It also spans one row starting

## Creating a Grid Layout

To create a grid layout, you need to define a grid container and grid items. Here's an example:

```css
.grid-container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: auto auto auto;
}
.grid-item {
  grid-column: 1 / 3;
  grid-row: 1 / 2;
}
```

In this example, we're creating a grid container with three columns and three rows. The `grid-template-columns` property specifies the width of each column, and the `grid-template-rows` property specifies the height of each row.

The `auto` value for the row height means that the row height will adjust to fit the content.

We're also creating a grid item that spans two columns and one row using the `grid-column` and `grid-row` properties. The `grid-column` property specifies the start and end columns, and the `grid-row` property specifies the start and end rows.

## CSS Grid vs. Flexbox

CSS Grid and Flexbox are both layout systems that allow you to create responsive designs.

However, they have different use cases. Flexbox is designed for one-dimensional layouts, while CSS Grid is designed for two-dimensional layouts.

Flexbox is ideal for creating layouts that need to be vertically or horizontally centered, such as navigation menus or form inputs.

CSS Grid, on the other hand, is ideal for creating complex layouts with multiple rows and columns, such as magazine-style layouts or dashboard designs.

## Conclusion

CSS Grid is a powerful layout system that allows you to create complex layouts quickly and easily. It provides a flexible and intuitive way to structure content on a web page, making it an ideal choice for creating responsive designs.

When you understand the basics of CSS Grid and its properties, you are capable of creating beautiful and functional layouts for your web projects.

Let me know your thoughts on this in the comments section.

Happy Coding!
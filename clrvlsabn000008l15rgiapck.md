---
title: "How To Create a Colorful Pie Chart Generator Using HTML, CSS, and JavaScript"
datePublished: Sat Jan 27 2024 05:00:12 GMT+0000 (Coordinated Universal Time)
cuid: clrvlsabn000008l15rgiapck
slug: how-to-create-a-colorful-pie-chart-generator-using-html-css-and-javascript
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1705910483012/5250c2de-0592-4757-b8f3-162c2e403f76.png
tags: css, javascript, html5, javascript-piechart

---

Data visualization is a crucial aspect of web development, and pie charts are a popular choice for representing data in an easily digestible format.

In this tutorial, we will walk through the process of building a Colorful Pie Chart Generator using the fundamental trio of web development languages: HTML, CSS, and JavaScript.

This project not only allows you to demonstrate your expertise in these languages but also provides an opportunity to infuse creativity into a practical application.

## **Getting Started**

Before we dive into the code, let's outline the basic structure of our project. We will create an HTML form for user input, utilize CSS for styling, and employ JavaScript to dynamically generate and update the pie chart. The result will be a visually appealing representation of data that users can interact with.

## Thought Process

### HTML Structure

Let us start by defining the HTML structure, which includes an input form for users to enter data and a canvas element to draw the pie chart.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Pie Chart Generator</title>
</head>
<body>
    <div class="container">
        <form id="dataForm">
            <!-- Input fields for data -->
            <label for="percentage">Percentage:</label>
            <input type="number" id="percentage" min="0" max="100" required>
            <label for="label">Label:</label>
            <input type="text" id="label" required>
            <!-- Add Data button -->
            <button type="button" onclick="addData()">Add Data</button>
        </form>
        <!-- Canvas for the pie chart -->
        <canvas id="pieChart" width="400" height="400"></canvas>
    </div>
    <!-- JavaScript file -->
    <script src="script.js"></script>
</body>
</html>
```

### CSS Styling

Let us apply minimal CSS styling to make the form and chart visually appealing.

```css
body {
    font-family: 'Arial', sans-serif;
    background-color: #f4f4f4;
    margin: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
}
.container {
    text-align: center;
}
form {
    margin-bottom: 20px;
}
/* button style */
button {
    background-color: #05869d;
    border: none;
    color: white;
    padding: 10px 30px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
}
/* input styles*/
input{
    width: 20%;
    padding: 12px;
    border: 1px solid #ccc;
    border-radius: 4px;
    resize: vertical;
}
canvas {
    border: 1px solid #ccc;
    border-radius: 8px;
}
```

### JavaScript Logic

The core functionality is implemented in the JavaScript file.

```javascript
// Data array to store user input
let data = [];
// Function to add data to the array
function addData() {
    const percentage = document.getElementById('percentage').value;
    const label = document.getElementById('label').value;
    // Validate input
    if (percentage && label) {
        data.push({ percentage: parseFloat(percentage), label });
        // Update the pie chart
        updateChart();
    }
}
// Function to update the pie chart
function updateChart() {
    const canvas = document.getElementById('pieChart');
    const ctx = canvas.getContext('2d');
    // Clear the canvas
    ctx.clearRect(0, 0, canvas.width, canvas.height);
    // Draw the pie chart
    let startAngle = 0;
    data.forEach((slice) => {
        const sliceAngle = (slice.percentage / 100) * 2 * Math.PI;
        ctx.fillStyle = getRandomColor();
        ctx.beginPath();
        ctx.moveTo(canvas.width / 2, canvas.height / 2);
        ctx.arc(canvas.width / 2, canvas.height / 2, canvas.width / 2, startAngle, startAngle + sliceAngle);
        ctx.closePath();
        ctx.fill();
        // Update start angle for the next slice
        startAngle += sliceAngle;
    });
}
// Function to generate a random color
function getRandomColor() {
    const letters = '0123456789ABCDEF';
    let color = '#';
    for (let i = 0; i < 6; i++) {
        color += letters[Math.floor(Math.random() * 16)];
    }
    return color;
}
```

## Innovative Approaches

### Random Color Generation

We implemented a function (`getRandomColor()`) to generate random colors for each pie chart slice, enhancing the visual appeal of the chart.

### Dynamic Chart Updates

The chart is updated dynamically whenever a user adds data, providing a seamless and responsive user experience.

### Watch the video tutorial.

%[https://youtu.be/oMJ9ArFCTGM?si=wGKPiomQLjiX7UHT] 

## Showcase of Technical and Creative Abilities

This project demonstrates your proficiency in HTML, CSS, and JavaScript. The well-organized code structure, comments, and thoughtful design showcase a commitment to writing clean and maintainable code.

The dynamic nature of the chart reflects creative problem-solving skills.

## Alternative Solutions

* Instead of using percentages, you can input absolute values, and the system will calculate the percentages automatically.
    
* Utilizing a chart library like Chart.js for a more feature-rich solution.
    

Overall, this simple, colorful pie chart generator is a visually engaging and user-friendly project that highlights basic technical skills and creativity in web development.

***Happy Coding!***
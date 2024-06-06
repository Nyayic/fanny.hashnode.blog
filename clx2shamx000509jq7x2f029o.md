---
title: "How To Create a Simple Pomodoro Timer Tool"
datePublished: Thu Jun 06 2024 05:00:31 GMT+0000 (Coordinated Universal Time)
cuid: clx2shamx000509jq7x2f029o
slug: how-to-create-a-simple-pomodoro-timer-tool
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1717306560095/765050ff-ce0f-4516-be85-c2f3c5defe9a.png
tags: css, javascript, html5, pomodoro

---

In this guide, let's build a simple Pomodoro timer tool. This project is ideal for you to practice HTML, CSS and Javascript.

## Step 1: Set up your Project

Create a new folder for your project and inside it create three files which are: \` `index.html,` \``styles.css,` \``script.js`\`\`.

Then open the folder in your code editor I will be using VS Code.

## Step 2: Set up your HTML Structure

In the \``index.html file, create an HTML structure by pressing SHIFT+!`\`

```xml
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pomodoro Timer Tool</title>
</head>
<body>
   
</body>
</html>
```

Change the document title to your project name which is "Pomodoro Timer Tool"

Link your CSS file below the title by adding this code.

```xml
<link rel="stylesheet" href="styles.css">
```

Link your external javascript file within the body.

```xml
   <script src="script.js"></script>
```

Create a container in your HTML file containing the heading and the different controls.

```xml
<div class="timer-container">
        <h1>Pomodoro Timer</h1>
        <div id="timer-display">25:00</div>
        <button id="start-btn">Start</button>
        <button id="stop-btn">Stop</button>
        <button id="reset-btn">Reset</button>
</div>
```

This is how the code will look for this step

```xml
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pomodoro Timer Tool</title>
    <!-- Link Your CSS File -->
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="timer-container">
        <h1>Pomodoro Timer</h1>
        <div id="timer-display">25:00</div>
        <button id="start-btn">Start</button>
        <button id="stop-btn">Stop</button>
        <button id="reset-btn">Reset</button>
    </div>
     <!-- Link your Javascript File -->
    <script src="script.js"></script>
</body>
</html>
```

* timer-display ID will show the display of the display of the timer.
    
* \``start-btn`\`: this is the ID for the start timer button.
    
* \``stop-btn`\`: This is the ID used to stop the button.
    
* \``reset-btn`\`: an ID to reset the button.
    

## Step 3: Style Using CSS

Open your CSS file and style the HTML elements:

```css
body{
    font-family: Arial, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #f3f4f6;
}
```

This will set the\``font-family`\`. display and set content to the center of the web page, the height and the background color will be set to the specified values.

Write the rest of the element styles for the classes and IDs In our HTML file.

```css
.timer-container{
    text-align: center;
    background: #fff;
    padding: 40px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}
#timer-display{
    font-size: 48px;
    margin-bottom: 20px;
}
button{
    padding: 10px 20px;
    font-size: 16px;
    margin: 5px;
    cursor: pointer;
    background-color: #ff6347;
    color: #fff;
    border-radius: 5px;
    border: none;
}
button:hover{
    background-color: #e55337;
}
```

This is how the webpage will appear after adding your CSS code.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1717305363340/6998c36c-01cb-4914-b33d-07473526b2c9.png align="center")

## Step 4: Javascript Functionality

Go to the Javascript file and create variables to fetch IDs from your HTML file.

```javascript
// Create variables to get elements
const display = document.getElementById('timer-display');
const StartBtn= document.getElementById('start-btn');
const StopBtn= document.getElementById('stop-btn');
const ResetBtn= document.getElementById('reset-btn');

let timer = null;
let time = 25 * 60; // 25 minutes
```

Create a function to update the time display and a math object functionality.

```javascript
const updateTimeDisplay = () => {
    let minutes = Math.floor(time/60);
    let seconds = time % 60;
    display.textContent = `${minutes.toString().padStart('2', '0')}:${seconds.toString().padStart('2','0')}`;
};
```

Create a function to start the timer and set the interval to 25 minutes.

```javascript
// function to start the timer
const startTimer = () =>{
    if (!timer){
        timer = setInterval(() => {
            time--;
            updateTimeDisplay();
            if (time === 0){
                timer = null;
                alert('Time is Up!');
            }
        }, 1000);
    }
};
```

Create a function to stop the timer.

```javascript
// function to stop the timer
const stopTimer = () => {
    clearInterval(timer);
    timer = null;
}
```

Create a function to reset the timer.

```javascript
// reset timer
const resetTimer = () => {
    stopTimer();
    time = 25 * 60;
    updateTimeDisplay();
}
```

Add an event listener \``on click`\` for all these buttons.

```javascript
StartBtn.addEventListener('click', startTimer);
StopBtn.addEventListener('click', stopTimer);
ResetBtn.addEventListener('click', resetTimer);

window.onload = updateTimeDisplay;
```

## Step 5: Project Overview and Outcome

The final project will have a 25-minute timer and will stop after clicking the stop button, and reset on clicking the reset button.

Watch Video Tutorial

%[https://youtu.be/Kh-7vBfDFKk?si=rUUneA-RsApokfNs] 

## Final Thoughts

This is an ideal project to practice your HTML, CSS and Javascript Skills especially if you are a beginner. Try this out and modify it in your favorite ways.  
Happy Coding!
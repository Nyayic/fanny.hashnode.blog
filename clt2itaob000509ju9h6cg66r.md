---
title: "How to Create a Simple Digital Clock in Javascript"
datePublished: Mon Feb 26 2024 05:51:06 GMT+0000 (Coordinated Universal Time)
cuid: clt2itaob000509ju9h6cg66r
slug: how-to-create-a-simple-digital-clock-in-javascript
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1708925610591/13492425-142e-4b03-812f-9c3673c3c77d.png
tags: javascript, digital-clock, javascript-digital-clock

---

In this step-by-step guide, we'll explore the fascinating world of web development by creating a simple yet sleek digital clock using HTML, CSS, and JavaScript. This is a simple project to practice your Javascript.

### **Step 1: Set Up Your Project**

Create a new folder for your project and inside it, create a file: `index.html` . Alternatively, you can create three files: `index.html`, `styles.css`, and `script.js`.

In this case, I will just create one and it in a code editor of your choice.

### **Step 2: HTML Structure**

In the `index.html` file, and set up the basic HTML structure. It will look like this:

```xml
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Clock</title>
</head>
<body>
    <div class="clock">
        <div id="time"></div>
    </div>
</body>
</html>
```

If you created three files. Link the CSS file for styling and the JavaScript file for functionality. It will Look like this:

```xml
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Clock</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="clock">
        <div id="time"></div>
    </div>
    <script src="script.js"></script>
</body>
</html>
```

### **Step 3: CSS Styling**

In the `styles.css` file, style the clock to make it visually appealing.

```css
body{
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      background-color: #f2f2f2;
   }
   .clock{
      font-family: Arial, sans-serif;
      font-size: 2em;
      color:#fff;
      background-color: #052727;
      padding: 40px;
      border-radius: 15px;
 }
```

### **Step 4: JavaScript Functionality**

In the `script.js` file, and write JavaScript code to create and update the digital clock.

```javascript
function updateClock() {
    const now = new Date();
    const hours = now.getHours().toString().padStart(2, '0');
    const minutes = now.getMinutes().toString().padStart(2, '0');
    const seconds = now.getSeconds().toString().padStart(2, '0');
    const timeString = `${hours}:${minutes}:${seconds}`;

    document.getElementById('time').innerText = timeString;
}
// Update the clock every second
setInterval(updateClock, 1000);

// Initial call to display the clock immediately
updateClock();
```

### **Step 5: Understanding the Code**

* The `updateClock` function gets the current time, formats it, and updates the content of the HTML element with the id `time`.
    
* The `setInterval` function is used to call `updateClock` every second, creating a real-time updating clock.
    
* The initial call to `updateClock` ensures that the clock is displayed immediately when the page loads.
    

### **Step 6: Testing**

Save all the files and open the `index.html` file in a web browser. You should see a simple and functional digital clock displaying the current time.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708931940261/97a9e45d-dd36-48c5-840b-58188c03b32c.png align="center")

### **Watch Video Tutorial**

%[https://youtu.be/8JT2uYTjRII?si=uksQYuqR1h3ELiq7] 

Congratulations! You have successfully created a digital clock using HTML, CSS, and JavaScript. Feel free to customize the styles or add additional features to enhance the clock based on your preferences.
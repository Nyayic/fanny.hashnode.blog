---
title: "How to build a simple Calculator in JavaScript"
seoTitle: "How to build a simple Calculator in JavaScript"
datePublished: Mon Apr 24 2023 18:33:51 GMT+0000 (Coordinated Universal Time)
cuid: clh0w7kbp000809mo1cfr51n2
slug: how-to-build-a-simple-calculator-in-javascript
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1682706634105/bb7921d4-6b7c-459c-b9bd-fa1da732bb55.jpeg
tags: javascript, 2articles1week, codenewbies

---

To build a simple calculator app in JavaScript, we can follow these steps:

1. Create an HTML file with the calculator UI elements like buttons and display. (index.html)
    
    ```bash
    <!DOCTYPE html>
    <html>
    <head>
      <title>Calculator</title>
      <link rel="stylesheet" href="style.css">
    </head>
    <body>
      <div id="calculator">
        <input type="text" id="display" readonly>
        <button onclick="appendToDisplay('7')">7</button>
        <button onclick="appendToDisplay('8')">8</button>
        <button onclick="appendToDisplay('9')">9</button>
        <button onclick="performOperation('/')">/</button>
        <button onclick="appendToDisplay('4')">4</button>
        <button onclick="appendToDisplay('5')">5</button>
        <button onclick="appendToDisplay('6')">6</button>
        <button onclick="performOperation('*')">*</button>
        <button onclick="appendToDisplay('1')">1</button>
        <button onclick="appendToDisplay('2')">2</button>
        <button onclick="appendToDisplay('3')">3</button>
        <button onclick="performOperation('-')">-</button>
        <button onclick="appendToDisplay('0')">0</button>
        <button onclick="appendToDisplay('.')">.</button>
        <button onclick="calculate()">=</button>
        <button onclick="performOperation('+')">+</button>
        <button onclick="clearDisplay()">C</button>
      </div>
      <script src="script.js"></script>
    </body>
    </html>
    ```
    
2. Style the HTML using CSS: Make sure your CSS file is linked to your HTML
    

```css
#calculator {
    width: 300px;
    margin: 0 auto;
    text-align: center;
  }
  #display {
    width: 100%;
    margin-bottom: 10px;
    font-size: 24px;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
  }  
  button {
    width: 50px;
    height: 50px;
    font-size: 18px;
    margin-right: 5px;
    margin-bottom: 5px;
    border: 1px solid #ccc;
    border-radius: 5px;
    background-color: #fff;
    cursor: pointer;
  }
  button:hover {
    background-color: #eee;
  }
  button:active {
    background-color: #ddd;
  }
  button:focus {
    outline: none;
  }
  #calculator button:last-child {
    width: 100%;
    margin-right: 0;
  }
  #calculator button:nth-child(4),
  #calculator button:nth-child(8),
  #calculator button:nth-child(12),
  #calculator button:last-child {
    background-color: #f5f5f5;
    color: #333;
  }
  #calculator button:nth-child(4):hover,
  #calculator button:nth-child(8):hover,
  #calculator button:nth-child(12):hover,
  #calculator button:last-child:hover {
    background-color: #ddd;
  }
  #calculator button:nth-child(4):active,
  #calculator button:nth-child(8):active,
  #calculator button:nth-child(12):active,
  #calculator button:last-child:active {
    background-color: #ccc;
  }  
```

1. Add event listeners to the calculator buttons to capture user inputs.
    
    Define functions to perform arithmetic operations based on the user inputs.
    
    Update the display with the result of the operations. Here is what we shall have in our script.js
    

```javascript
let display = document.getElementById('display');
let firstOperand = '';
let secondOperand = '';
let currentOperation = null;

function appendToDisplay(number) {
  display.value += number;
}

function clearDisplay() {
  display.value = '';
  firstOperand = '';
  secondOperand = '';
  currentOperation = null;
}

function performOperation(operation) {
  if (currentOperation !== null) {
    calculate();
  }
  firstOperand = display.value;
  currentOperation = operation;
  display.value = '';
}

function calculate() {
  if (currentOperation === null) {
    return;
  }
  secondOperand = display.value;
  if (currentOperation === '/' && secondOperand === '0') {
    alert('Cannot divide by zero');
    clearDisplay();
    return;
  }
  let result = 0;
  switch (currentOperation) {
    case '+':
      result = parseFloat(firstOperand) + parseFloat(secondOperand);
      break;
    case '-':
      result = parseFloat(firstOperand) - parseFloat(secondOperand);
      break;
    case '*':
      result = parseFloat(firstOperand) * parseFloat(secondOperand);
      break;
    case '/':
      result = parseFloat(firstOperand) / parseFloat(secondOperand);
      break;
    default:
      break;
  }
  display.value = result;
  firstOperand = result;
  secondOperand = '';
  currentOperation = null;
}
```

Run your index.html file to test the functionality of your calculator, you can modify it to suit what you need, you can tweak the CSS to add more beauty to it.  
Happy Coding!
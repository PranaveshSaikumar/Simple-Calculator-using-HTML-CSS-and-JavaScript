# Simple Calculator using HTML, CSS, and JavaScript

### Name: Pranavesh Saikumar

### Regno: 212223040149

## Aim:
To create a simple calculator using HTML, CSS, and JavaScript that performs addition, subtraction, multiplication, and division of two numbers.

## Procedure:
Create an HTML file with:

Two input fields for numbers.

A dropdown menu for operation selection.

A button to perform the calculation.

A result display area.

Write a CSS file to style the calculator with background, layout, colors, and button hover effects.

Write a JavaScript file (script.js) that:

Reads the input numbers.

Gets the selected operation.

Performs the calculation using switch-case.

Handles invalid input and division by zero.

Displays the result on the webpage.

Link HTML, CSS, and JavaScript together and run the project in a web browser.
## Program:
```
.html
    <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Simple Calculator</title>
  <link rel="stylesheet" href="activityStyle.css">
</head>
<body>
  <div class="calculator">
    <h2>Simple Calculator</h2>
    <input type="number" id="num1" placeholder="Enter first number">
    <input type="number" id="num2" placeholder="Enter second number">
    
    <select id="operation">
      <option value="add">Add</option>
      <option value="subtract">Subtract</option>
      <option value="multiply">Multiply</option>
      <option value="divide">Divide</option>
    </select>
    
    <button onclick="calculate()">Calculate</button>
    <p id="result"></p>
  </div>

  <script src="activityScript.js"></script>
</body>
</html>
```
```
.css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background: linear-gradient(135deg, #89f7fe, #66a6ff);
  margin: 0;
}

.calculator {
  background: #ffffff;
  padding: 25px;
  border-radius: 15px;
  box-shadow: 0 6px 12px rgba(0,0,0,0.2);
  text-align: center;
  width: 320px;
}

h2 {
  color: #333;
  margin-bottom: 15px;
}

input, select {
  margin: 10px 0;
  padding: 12px;
  width: 90%;
  font-size: 16px;
  border: 2px solid #66a6ff;
  border-radius: 8px;
  outline: none;
  transition: 0.3s;
}

input:focus, select:focus {
  border-color: #ff6a95;
  box-shadow: 0 0 8px rgba(255, 106, 149, 0.5);
}

button {
  margin-top: 15px;
  padding: 12px;
  width: 95%;
  font-size: 16px;
  background: #66a6ff;
  border: none;
  color: white;
  font-weight: bold;
  border-radius: 8px;
  cursor: pointer;
  transition: 0.3s;
}

button:hover {
  background: #ff6a95;
  transform: scale(1.05);
}

#result {
  margin-top: 20px;
  font-weight: bold;
  font-size: 20px;
  color: #444;
}
```
```
.script
function calculate() {
  let num1 = parseFloat(document.getElementById("num1").value);
  let num2 = parseFloat(document.getElementById("num2").value);
  let operation = document.getElementById("operation").value;
  let result = "";

  if (isNaN(num1) || isNaN(num2)) {
    result = "Please enter valid numbers!";
  } else {
    switch (operation) {
      case "add":
        result = num1 + num2;
        break;
      case "subtract":
        result = num1 - num2;
        break;
      case "multiply":
        result = num1 * num2;
        break;
      case "divide":
        result = num2 !== 0 ? num1 / num2 : "Cannot divide by zero!";
        break;
    }
  }

  document.getElementById("result").innerText = "Result: " + result;
}
```

## Output:
<img width="1208" height="878" alt="image" src="https://github.com/user-attachments/assets/656a8f9f-ee46-4230-a266-415ae3d36e25" />


## Result:
A simple calculator was successfully developed using HTML, CSS, and JavaScript.

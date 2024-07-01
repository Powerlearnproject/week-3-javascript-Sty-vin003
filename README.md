<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Web Page with Chart.js</title>
    <style>
        #result {
            margin-top: 10px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <h1>Interactive Web Page</h1>

    <div>
        <input type="number" id="num1" placeholder="Enter first number">
        <input type="number" id="num2" placeholder="Enter second number">
        <button id="addBtn">Add</button>
        <button id="subtractBtn">Subtract</button>
        <button id="multiplyBtn">Multiply</button>
        <button id="divideBtn">Divide</button>
    </div>

    
    <div id="result"></div>

 
    <script src="script.js"></script>


    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
</body>
</html>



///// script


// Declare variables of different data types
var name = "John Doe";
var age = 30;
var isDeveloper = true;

// Define functions for simple operations
function add(a, b) {
    return a + b;
}

function subtract(a, b) {
    return a - b;
}

function multiply(a, b) {
    return a * b;
}

function divide(a, b) {
    if (b === 0) {
        return 'Error: Division by zero';
    }
    return a / b;
}


document.getElementById('addBtn').addEventListener('click', function() {
    var num1 = parseFloat(document.getElementById('num1').value);
    var num2 = parseFloat(document.getElementById('num2').value);
    var result = add(num1, num2);
    document.getElementById('result').textContent = 'Result: ' + result;
});

document.getElementById('subtractBtn').addEventListener('click', function() {
    var num1 = parseFloat(document.getElementById('num1').value);
    var num2 = parseFloat(document.getElementById('num2').value);
    var result = subtract(num1, num2);
    document.getElementById('result').textContent = 'Result: ' + result;
});

document.getElementById('multiplyBtn').addEventListener('click', function() {
    var num1 = parseFloat(document.getElementById('num1').value);
    var num2 = parseFloat(document.getElementById('num2').value);
    var result = multiply(num1, num2);
    document.getElementById('result').textContent = 'Result: ' + result;
});

document.getElementById('divideBtn').addEventListener('click', function() {
    var num1 = parseFloat(document.getElementById('num1').value);
    var num2 = parseFloat(document.getElementById('num2').value);
    var result = divide(num1, num2);
    document.getElementById('result').textContent = 'Result: ' + result;
});


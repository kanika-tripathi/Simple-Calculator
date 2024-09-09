# Simple-Calculator
This is a simple calculator program created using HTML, CSS and JavaScript
1. *HTML Structure*:
html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Calculator</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="calculator">
        <input type="text" id="screen" disabled>
        <div class="keys">
            <button onclick="clearScreen()">C</button>
            <button onclick="appendToScreen('7')">7</button>
            <button onclick="appendToScreen('8')">8</button>
            <button onclick="appendToScreen('9')">9</button>
            <button onclick="appendToScreen('+')">+</button>
            <button onclick="appendToScreen('4')">4</button>
            <button onclick="appendToScreen('5')">5</button>
            <button onclick="appendToScreen('6')">6</button>
            <button onclick="appendToScreen('-')">-</button>
            <button onclick="appendToScreen('1')">1</button>
            <button onclick="appendToScreen('2')">2</button>
            <button onclick="appendToScreen('3')">3</button>
            <button onclick="appendToScreen('*')">*</button>
            <button onclick="appendToScreen('0')">0</button>
            <button onclick="appendToScreen('.')">.</button>
            <button onclick="calculate()">=</button>
            <button onclick="appendToScreen('/')">/</button>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>
2. *CSS Styling* (styles.css):
css
.calculator {
    width: 300px;
    margin: 0 auto;
    text-align: center;
}
#screen {
    width: 100%;
    height: 50px;
    font-size: 24px;
    margin-bottom: 10px;
}
.keys {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 5px;
}
button {
    width: 100%;
    height: 50px;
    font-size: 20px;
}
3. *JavaScript Logic* (script.js):
javascript
function appendToScreen(value) {
    document.getElementById('screen').value += value;
}
function clearScreen() {
    document.getElementById('screen').value = '';
}
function calculate() {
    try {
        let result = eval(document.getElementById('screen').value);
        document.getElementById('screen').value = result;
    } catch (error) {
        document.getElementById('screen').value = 'Error';
    }
}


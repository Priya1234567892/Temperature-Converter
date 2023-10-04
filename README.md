# Temperature-Converter
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Temperature Converter</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1>Temperature Converter</h1>
        <div class="input-container">
            <input type="number" id="celsiusInput" placeholder="Enter Celsius">
            <button onclick="convertToFarhenheit()">Convert to Fahrenheit</button>
        </div>
        <div class="result">
            <p><span id="result">Result</span> °F</p>
        </div>
    </div>

    <script src="script.js"></script>
</body>
</html>

body {
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;
    text-align: center;
    margin: 0;
    padding: 0;
}

.container {
    background-color: #fff;
    border-radius: 10px;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.2);
    max-width: 400px;
    margin: 100px auto;
    padding: 20px;
}

h1 {
    color: #333;
}

.input-container {
    margin-top: 20px;
}

input[type="number"] {
    width: 70%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
}

button {
    width: 30%;
    padding: 10px;
    background-color: #007bff;
    color: #fff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

.result {
    margin-top: 20px;
    font-size: 24px;
}
function convertToFarhenheit() {
    const celsiusInput = document.getElementById("celsiusInput").value;
    const result = (celsiusInput * 9/5) + 32;
    document.getElementById("result").textContent = result.toFixed(2);
}

# temperature-converter

<!DOCTYPE html>
<html>
<head>
    <title>Temperature Converter</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
        }
        .container {
            margin-top: 50px;
        }
        h1 {
            color: #333;
        }
        input[type="number"] {
            padding: 5px;
            width: 60px;
        }
        button {
            padding: 5px 10px;
            background-color: #0074d9;
            color: white;
            border: none;
            cursor: pointer;
        }
        #result {
            font-weight: bold;
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Temperature Converter</h1>
        <label for="celsius">Enter Temperature in Celsius:</label>
        <input type="number" id="celsius" placeholder="Celsius">
        <button onclick="convertToCelsius()">Convert to Fahrenheit</button>
        <br><br>
        <label for="fahrenheit">Enter Temperature in Fahrenheit:</label>
        <input type="number" id="fahrenheit" placeholder="Fahrenheit">
        <button onclick="convertToFahrenheit()">Convert to Celsius</button>
        <div id="result"></div>
    </div>

    <script>
        function convertToCelsius() {
            let celsius = parseFloat(document.getElementById("celsius").value);
            let fahrenheit = (celsius * 9/5) + 32;
            document.getElementById("result").innerHTML = celsius + " Celsius = " + fahrenheit.toFixed(2) + " Fahrenheit";
        }

        function convertToFahrenheit() {
            let fahrenheit = parseFloat(document.getElementById("fahrenheit").value);
            let celsius = (fahrenheit - 32) * 5/9;
            document.getElementById("result").innerHTML = fahrenheit + " Fahrenheit = " + celsius.toFixed(2) + " Celsius";
        }
    </script>
</body>
</html>

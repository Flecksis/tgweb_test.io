# tgweb_test.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Clicker</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
        }
        #clickCount {
            font-size: 24px;
            margin-bottom: 20px;
        }
        #clickButton {
            padding: 10px 20px;
            font-size: 18px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <h1>Flecksis_coin</h1>
    <div id="clickCount">Количество кликов: 0</div>
    <button id="clickButton" onclick="incrementClick()">Кликни здесь!</button>

    <script>
        let clickCount = 0;

        function incrementClick() {
            clickCount++;
            document.getElementById("clickCount").innerText = "Количество кликов: " + clickCount;
        }
    </script>
</body>
</html>

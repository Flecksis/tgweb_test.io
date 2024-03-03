<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Clicker</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .container {
            background-color: #fff;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h1 {
            color: #333;
            margin-bottom: 20px;
        }
        #clickCount {
            font-size: 24px;
            margin-bottom: 20px;
        }
        #clickButton {
            padding: 10px 20px;
            font-size: 18px;
            cursor: pointer;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 5px;
            transition: background-color 0.3s ease;
        }
        #clickButton:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Rust clicker</h1>
        <div id="clickCount">Количество скрапа: 0</div>
        <div class="xsmall">говорят что-бы изучить всё нужно 15к скрапа</div>
        <img id="clickImage" src="click.png" alt="Кликни здесь!" width="200" height="200" onclick="incrementClick()">
        <div class="xsmall">by flecksis</div>
    </div>

    <script>
        let clickCount = 0;

        function incrementClick() {
            clickCount++;
            document.getElementById("clickCount").innerText = "Количество кликов: " + clickCount;
        }
    </script>
</body>

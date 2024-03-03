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
        #clickButton, #wipeButton {
            padding: 10px 20px;
            font-size: 18px;
            cursor: pointer;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 5px;
            transition: background-color 0.3s ease;
            margin-right: 10px;
        }
        #clickButton:hover, #wipeButton:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Rust clicker</h1>
        <div id="clickCount">Количество скрапа: 0</div>
        <div class="xsmall">говорят что-бы изучить всё нужно 15к скрапа</div>
        <!-- Добавлен элемент audio для воспроизведения звука -->
        <audio id="clickSound" src="click_sound.mp3"></audio>
        <img id="clickImage" src="click.png" alt="Кликни здесь!" width="200" height="200" onclick="incrementClick()">
        <div>
            <button id="wipeButton" onclick="buyWipe()">Вайп: <span id="wipeCostValue">10</span> Скрапа</button>
        </div>
        <div class="xsmall">by flecksis</div>
    </div>

    <script>
        let clickCount = 0;
        let wipeCost = 10;
        let clickMultiplier = 1;

        function incrementClick() {
            clickCount += clickMultiplier;
            document.getElementById("clickCount").innerText = "Количество скрапа: " + clickCount;
            // Воспроизводим звук при клике
            document.getElementById("clickSound").play();
        }

        function buyWipe() {
            if (clickCount >= wipeCost) {
                clickCount -= wipeCost;
                clickMultiplier *= 2;
                wipeCost *= 3;
                document.getElementById("clickCount").innerText = "Количество скрапа: " + clickCount;
                document.getElementById("wipeCostValue").innerText = wipeCost;
                alert("Вы купили вайп. Теперь ваш множитель кликов увеличен вдвое!");
            } else {
                alert("У вас недостаточно скрапа для покупки вайпа.");
            }
        }
    </script>
</body>
</html>

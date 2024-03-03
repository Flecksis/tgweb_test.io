# tgweb_test.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Telegram Clicker</title>
</head>
<body>
    <h1>Click Count: {{ click_count }}</h1>
    <form action="/click" method="post">
        <button type="submit">Click Me</button>
    </form>
</body>
</html>

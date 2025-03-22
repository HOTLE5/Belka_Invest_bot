<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Инвестиции</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f4f4f9;
        }

        .container {
            text-align: center;
            background-color: #ffffff;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            width: 100%;
            max-width: 500px;
        }

        .button {
            padding: 15px 30px;
            font-size: 16px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            margin-top: 20px;
        }

        .button.vip {
            background-color: #FFD700;
        }

        .button:hover {
            opacity: 0.8;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>Добро пожаловать в наш инвестиционный сервис!</h1>
        <p>Выберите вариант инвестирования:</p>

        <button class="button" onclick="sendInvestmentChoice('5%')">5% стандартный</button>
        <button class="button vip" onclick="sendInvestmentChoice('10% VIP')">10% VIP</button>
    </div>

    <script>
        function sendInvestmentChoice(choice) {
            // Передаем выбор пользователя в Telegram
            window.Telegram.WebApp.sendData(choice);
        }

        // Инициализация Web App
        window.Telegram.WebApp.onEvent('webAppData', function(event) {
            console.log('Получены данные из WebApp:', event.data);
        });
    </script>

</body>
</html>

    </script>

</body>
</html>

<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Инвестирование</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f4f4f9;
            padding: 20px;
        }
        .header {
            margin-bottom: 20px;
        }
        .footer {
            margin-top: 30px;
            display: flex;
            justify-content: space-between;
            padding: 10px;
        }
        button {
            padding: 12px 30px;
            font-size: 16px;
            cursor: pointer;
            margin: 10px;
            border: none;
            border-radius: 5px;
            background-color: #007bff;
            color: white;
        }
        button:hover {
            background-color: #0056b3;
        }
        .footer button {
            flex: 1;
        }
    </style>
</head>
<body>

    <!-- Заголовок -->
    <div class="header">
        <h1>Название Компании</h1>
        <p id="username">Загрузка имени пользователя...</p> <!-- Имя пользователя будет динамически обновлено -->
    </div>

    <!-- Кнопка Инвестировать -->
    <div>
        <button id="invest" onclick="invest()">Инвестировать</button>
    </div>

    <!-- Кнопки снизу -->
    <div class="footer">
        <button onclick="goToMain()">Главное</button>
        <button onclick="goToFriends()">Друзья</button>
        <button onclick="goToMap()">Карта</button>
    </div>

    <script>
        // Загрузка имени пользователя из Telegram Web App
        if (window.Telegram.WebApp) {
            const userName = window.Telegram.WebApp.initDataUnsafe?.user?.first_name || 'Неизвестный';
            document.getElementById('username').textContent = `Привет, ${userName}`;
        }

        // Функция открытия ссылки для инвестирования
        function invest() {
            window.Telegram.WebApp.openLink("https://your-web-app-url.com/invest");
        }

        // Логика кнопок снизу
        function goToMain() {
            alert('Перейти на главную страницу');
            // Здесь можно добавить логику для перехода или открытия новой страницы
        }

        function goToFriends() {
            alert('Перейти к друзьям');
            // Добавьте логику для раздела "Друзья"
        }

        function goToMap() {
            alert('Открыть карту');
            // Логика для карты
        }
    </script>

</body>
</html>

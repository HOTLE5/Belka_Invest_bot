
<!DOCTYPE html>
<html>
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Belka Invest</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1>💼 Инвестировать</h1>
        
        <!-- Форма для инвестиций -->
        <form id="investForm">
            <input type="number" placeholder="Сумма в USD" required>
            <button type="submit">Подтвердить</button>
        </form>

        <!-- Уведомление -->
        <div class="success-message" id="successMessage"></div>
    </div>

    <script>
        document.getElementById('investForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const amount = document.querySelector('input').value;
            document.getElementById('successMessage').textContent = `Инвестиция на ${amount}$ успешно оформлена!`;
        });
    </script>
</body>
</html>
:root {
    --primary-green: #4CAF50;
    --dark-green: #2E7D32;
    --light-green: #E8F5E9;
}

body {
    background: var(--light-green);
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 20px;
}

.container {
    max-width: 600px;
    margin: 0 auto;
    background: white;
    padding: 25px;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0,0,0,0.1);
}

h1 {
    color: var(--dark-green);
    text-align: center;
}

input {
    width: 100%;
    padding: 12px;
    margin: 10px 0;
    border: 2px solid var(--primary-green);
    border-radius: 5px;
    font-size: 16px;
}

button {
    width: 100%;
    padding: 15px;
    background: var(--primary-green);
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
    transition: background 0.3s;
}

button:hover {
    background: var(--dark-green);
}

.success-message {
    margin-top: 20px;
    padding: 15px;
    background: #dff0d8;
    color: #3c763d;
    border-radius: 5px;
    text-align: center;
    display: none;
}

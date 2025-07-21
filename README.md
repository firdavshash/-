<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Милая Кола</title>
    <!-- Подключение Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Пользовательские стили для анимации колы */
        @keyframes colaMove {
            0% { transform: translate(0, 0) scale(1); opacity: 0.8; }
            25% { transform: translate(10vw, 5vh) scale(1.05); opacity: 0.9; }
            50% { transform: translate(0, 10vh) scale(1.1); opacity: 1; }
            75% { transform: translate(-10vw, 5vh) scale(1.05); opacity: 0.9; }
            100% { transform: translate(0, 0) scale(1); opacity: 0.8; }
        }

        .cola-background-animation {
            background-image: url('https://placehold.co/200x200/FF0000/FFFFFF?text=Милая+Кола'); /* Placeholder image for cute cola */
            background-repeat: no-repeat;
            background-size: contain;
            position: absolute;
            width: 200px;
            height: 200px;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            animation: colaMove 15s infinite ease-in-out;
            z-index: 0; /* Убедитесь, что она находится на заднем плане */
        }
    </style>
</head>
<body class="font-sans antialiased text-white min-h-screen flex flex-col relative overflow-hidden">
    <!-- Фоновый градиент -->
    <div class="absolute inset-0 bg-gradient-to-br from-red-800 to-black z-0"></div>

    <!-- Анимированная кола на заднем плане -->
    <div class="cola-background-animation"></div>

    <!-- Основное содержимое сайта -->
    <header class="relative z-10 p-4 text-center">
        <h1 class="text-5xl font-extrabold text-red-300 drop-shadow-lg">Добро Пожаловать в Мир Милой Колы!</h1>
    </header>

    <main class="relative z-10 flex-grow flex items-center justify-center p-4">
        <div class="bg-white bg-opacity-10 backdrop-filter backdrop-blur-lg p-8 rounded-xl shadow-2xl max-w-sm w-full text-center border border-red-500">
            <h2 class="text-4xl font-bold text-red-200 mb-4">Милая Кола</h2>
            <!-- Изображение продукта -->
            <img src="https://placehold.co/300x300/FF0000/FFFFFF?text=Милая+Кола" alt="Милая Кола" class="w-48 h-48 mx-auto mb-6 rounded-lg shadow-lg border-2 border-red-400">
            <p class="text-2xl font-semibold text-red-100 mb-6">Цена: <span class="text-red-300">6 000 Сумов</span></p>
            <button id="buyButton" class="bg-red-600 hover:bg-red-700 text-white font-bold py-3 px-8 rounded-full shadow-lg transform transition-transform duration-200 hover:scale-105 focus:outline-none focus:ring-4 focus:ring-red-500 focus:ring-opacity-50">
                Купить Сейчас!
            </button>
        </div>
    </main>

    <footer class="relative z-10 p-4 text-center text-gray-300 text-sm">
        <p>&copy; 2025 Милая Кола. Все права защищены.</p>
    </footer>

    <script>
        // JavaScript для обработки нажатия кнопки "Купить"
        document.getElementById('buyButton').addEventListener('click', function() {
            // Вместо alert() можно было бы использовать модальное окно или перенаправление на страницу оплаты
            alert('Спасибо за покупку Милой Колы! Ваша покупка успешно оформлена.');
        });
    </script>
</body>
</html>


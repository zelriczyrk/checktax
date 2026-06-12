<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Check Tax</title>
</head>
<body>
    <button id="taxBtn">Check Tax</button>
    <div id="result"></div>

    <script>
        // Функция для генерации случайного налога каждые 15 минут
        function getTax() {
            const now = new Date();
            const interval = Math.floor(now.getUTCMinutes() / 15);
            // Использование времени для фиксации значения на 15 минут
            const seed = now.getUTCFullYear() + now.getUTCMonth() + now.getUTCDate() + now.getUTCHours() + interval;
            
            // Псевдослучайное число на основе seed
            const random = Math.abs(Math.sin(seed) * 10000) % 1;
            const tax = (5 + random * 3).toFixed(2);
            
            return {
                tax: tax,
                time: now.toUTCString()
            };
        }

        document.getElementById('taxBtn').addEventListener('click', () => {
            const data = getTax();
            document.getElementById('result').innerText = `Tax: ${data.tax}% | Time (UTC): ${data.time}`;
        });
    </script>
</body>
</html>

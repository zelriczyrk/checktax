
<html lang="ru">
<head>
    <style>
        #taxBtn {
            background: transparent;
            color: #fff;
            border: 2px solid #0ff;
            padding: 10px 20px;
            cursor: pointer;
            text-transform: uppercase;
            font-weight: bold;
            box-shadow: 0 0 10px #0ff, 0 0 20px #0ff;
            transition: 0.3s;
        }
        #taxBtn:hover {
            background: #0ff;
            color: #000;
        }
    </style>
</head>
<body>
    <button id="taxBtn">Check Tax</button>
    <div id="result"></div>

    <script>
        // Функция генерации налога (интервал 15 минут)
        function getTax() {
            const now = new Date();
            const interval = Math.floor(now.getUTCMinutes() / 15);
            const seed = now.getUTCDate() + now.getUTCHours() + interval;
            const random = Math.abs(Math.sin(seed) * 10000) % 1;
            const tax = (5 + random * 3).toFixed(2);
            return { tax: tax, time: now.toUTCString() };
        }

        document.getElementById('taxBtn').addEventListener('click', () => {
            const data = getTax();
            document.getElementById('result').innerText = `Tax: ${data.tax}% | Time (UTC): ${data.time}`;
        });
    </script>
</body>
</html>


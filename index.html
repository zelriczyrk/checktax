
<html lang="ru">
<head>
    <style>
        body {
            background: #050505;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            box-shadow: inset 0 0 50px #f0f;
            border: 10px solid #f0f;
        }

        #taxBtn {
            background: transparent;
            color: #0ff;
            border: 2px solid #0ff;
            padding: 15px 30px;
            cursor: pointer;
            text-transform: uppercase;
            font-size: 20px;
            box-shadow: 0 0 10px #0ff, 0 0 20px #0ff;
            transition: 0.3s;
        }

        #taxBtn:hover {
            background: #0ff;
            color: #000;
        }

        #result {
            margin-top: 20px;
            color: #0f0;
            text-shadow: 0 0 10px #0f0;
            font-family: monospace;
            display: none;
        }
    </style>
</head>
<body>

    <button id="taxBtn">Check Tax</button>
    <div id="result"></div>

    <script>
        // Функция расчета налога
        function getTax() {
            const now = new Date();
            const interval = Math.floor(now.getUTCMinutes() / 15);
            const seed = now.getUTCDate() + now.getUTCHours() + interval;
            const random = Math.abs(Math.sin(seed) * 10000) % 1;
            const tax = (5 + random * 3).toFixed(2);
            return { tax: tax, time: now.toUTCString() };
        }

        document.getElementById('taxBtn').addEventListener('click', () => {
            const btn = document.getElementById('taxBtn');
            const res = document.getElementById('result');
            
            btn.disabled = true;
            btn.innerText = "Loading...";

            // Задержка 3 секунды
            setTimeout(() => {
                const data = getTax();
                res.innerText = `Tax: ${data.tax}% | Time (UTC): ${data.time}`;
                res.style.display = "block";
                btn.disabled = false;
                btn.innerText = "Check Tax";
            }, 3000);
        });
    </script>
</body>
</html>

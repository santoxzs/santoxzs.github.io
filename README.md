<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Amor por Você</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            text-align: center;
        }
        .container {
            background-color: white;
            padding: 50px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        h1 {
            font-size: 2.5rem;
            color: #e74c3c;
        }
        .countdown {
            font-size: 2rem;
            margin-top: 20px;
            color: #2c3e50;
            font-weight: bold;
        }
        img {
            max-width: 100%;
            height: auto;
            border-radius: 10px;
            margin-bottom: 20px;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Há quanto tempo estou amando você!</h1>
    
    <!-- IMAGEM ADICIONADA AQUI -->
    <img src="https://raw.githubusercontent.com/santoxzs/santoxzs.github.io/main/IMG-20250128-WA0023.jpg" alt="Minha imagem">

    <div class="countdown" id="countdown"></div>
</div>

<script>
    const startDate = new Date("September 20, 2024 00:00:00").getTime();

    function updateCountdown() {
        const now = new Date().getTime();
        const timeDiff = now - startDate;

        const days = Math.floor(timeDiff / (1000 * 60 * 60 * 24));
        const hours = Math.floor((timeDiff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        const minutes = Math.floor((timeDiff % (1000 * 60 * 60)) / (1000 * 60));
        const seconds = Math.floor((timeDiff % (1000 * 60)) / 1000);

        document.getElementById("countdown").innerHTML = `${days} dias, ${hours} horas, ${minutes} minutos e ${seconds} segundos`;
    }

    setInterval(updateCountdown, 1000);
</script>

</body>
</html>

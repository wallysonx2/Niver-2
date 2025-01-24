<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>O início da jornada</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f4f4f9;
            margin: 0;
            padding: 20px;
        }
        h1 {
            color: #4CAF50;
        }
        p {
            font-size: 18px;
            color: #333;
        }
        iframe {
            width: 100%;
            max-width: 720px;
            height: 405px;
            border: none;
            border-radius: 15px;
            margin-top: 20px;
            display: none;
        }
        .proxima-pista {
            display: none;
            margin-top: 20px;
            padding: 15px;
            background-color: #e0ffe0;
            border: 2px solid #4CAF50;
            border-radius: 10px;
            font-size: 18px;
            color: #333;
        }
        .senha-container {
            margin-top: 20px;
            display: none;
        }
        input[type="text"] {
            padding: 10px;
            font-size: 16px;
            border: 1px solid #ccc;
            border-radius: 5px;
            margin-right: 10px;
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
            background-color: #4CAF50;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
    </style>
    <script>
        function mostrarSenha() {
            document.querySelector('.senha-container').style.display = 'block';
        }

        function verificarSenha() {
            const senhaCorreta = "1808";
            const senhaDigitada = document.getElementById("senha").value;
            if (senhaDigitada === senhaCorreta) {
                document.querySelector('iframe').style.display = 'block';
                document.querySelector('.proxima-pista').style.display = 'block';
                document.querySelector('.senha-container').style.display = 'none';
            } else {
                alert("Senha incorreta! Tente novamente.");
            }
        }
    </script>
</head>
<body>
    <h1>O início da jornada</h1>
    <p>Clique no botão abaixo para começar sua jornada!</p>
    <button onclick="mostrarSenha()">Surpresa</button>

    <div class="senha-container">
        <p>Digite a senha para desbloquear:</p>
        <input type="text" id="senha" placeholder="Digite a senha">
        <button onclick="verificarSenha()">Confirmar</button>
    </div>

    <iframe src="https://www.youtube.com/embed/sYriFTQlzBA" allowfullscreen></iframe>

    <div class="proxima-pista">
        <p>Sua próxima pista está no local onde compartilhamos nosso primeiro abraço especial! 🌟</p>
    </div>
</body>
</html>

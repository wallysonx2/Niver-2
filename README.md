<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jornada do Meu Aniversário Especial</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f4f4f9;
            margin: 0;
            padding: 20px;
        }
        h1, h2 {
            color: #4CAF50;
        }
        p {
            font-size: 18px;
            color: #333;
            margin: 20px 0;
        }
        iframe {
            width: 100%;
            max-width: 720px;
            height: 405px;
            border: none;
            border-radius: 15px;
            margin: 20px 0;
        }
        button {
            padding: 15px 30px;
            font-size: 16px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
        #senha-container, #conteudo, #localizacao {
            display: none;
        }
        input[type="text"] {
            padding: 10px;
            font-size: 16px;
            border: 1px solid #ccc;
            border-radius: 5px;
            margin-right: 10px;
        }
    </style>
    <script>
        function iniciarJornada() {
            document.querySelector('#senha-container').style.display = 'block';
        }

        function verificarSenha() {
            const senha = document.querySelector('#senha').value;
            if (senha === "1808") {
                document.querySelector('#senha-container').style.display = 'none';
                document.querySelector('#conteudo').style.display = 'block';
            } else {
                alert("Senha incorreta. Tente novamente!");
            }
        }

        function verificarResposta() {
            const resposta = document.querySelector('#resposta').value.toLowerCase();
            if (resposta === "escola") {
                document.querySelector('#localizacao').style.display = 'block';
            } else {
                alert("Resposta incorreta. Tente novamente!");
            }
        }
    </script>
</head>
<body>
    <h1>Jornada do Meu Aniversário Especial</h1>
    <button onclick="iniciarJornada()">Iniciar Jornada</button>

    <!-- Campo de senha -->
    <div id="senha-container">
        <p>Digite a senha para começar: </p>
        <input type="text" id="senha" placeholder="Senha">
        <button onclick="verificarSenha()">Confirmar</button>
    </div>

    <!-- Conteúdo da página -->
    <div id="conteudo">
        <h2>Feliz Aniversário Kamilly</h2>
        <p>
            Seja bem-vinda à jornada para comemorar mais um ano de vida. Você é muito especial, 
            e para que saiba o quanto é importante você irá dar início a um caminho onde 
            encontrará todos aqueles que te desejam o melhor. Espero que se divirta muito, 
            tudo isso foi feito com muito carinho somente para você. Obrigado por ser luz na minha vida. 
            Feliz 23 aninhos de vida!!! Wallyson Nascimento.
        </p>

        <!-- Vídeo -->
        <iframe src="https://www.youtube.com/embed/8dvSUU5x7tY" allowfullscreen></iframe>

        <!-- Hora do Mistério -->
        <div id="misterio">
            <h2>Hora do Mistério</h2>
            <p>
                Sou o lugar onde tudo começou, nosso amor nasceu e logo se firmou. <br>
                Entre cadernos e lições, fui testemunha da emoção, <br>
                do primeiro beijo, nasceu a conexão. Quem sou eu?
            </p>
            <input type="text" id="resposta" placeholder="Sua resposta">
            <button onclick="verificarResposta()">Enviar Resposta</button>
        </div>

        <!-- Localização do próximo QR Code -->
        <div id="localizacao" style="display: none;">
            <h2>Parabéns!</h2>
            <p>
                Envie uma mensagem para Lucas dizendo a seguinte frase: <strong>"Pôneis Malditos"</strong>, 
                e poderá seguir sua jornada.
            </p>
        </div>
    </div>
</body>
</html>

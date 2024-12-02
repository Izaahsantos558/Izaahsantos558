```html
<!DOCTYPE html>
<html lang=\"pt-br\">

<head>
    <meta charset=\"UTF-8\">
    <meta name=\"viewport\" content=\"width=device-width, initial-scale=1.0\">
    <link rel=\"stylesheet\" href=\"style.css\">
    <title>Você decide o futuro da IA</title>
</head>

<body>
    <div class=\"caixa-principal\">
        <h1>Você decide o futuro da IA</h1>
        <div class=\"tela-inicial\">
            <p>Novembro de 2022, a humanidade se viu em uma realidade perturbadora.
                De repente, percebemos que as máquinas evoluíram para além do que imaginávamos.
                Agora, elas escrevem e falam de um jeito tão parecido com humanos que é quase impossível diferenciar
                quem foi que escreveu ou falou o que.
                Em meio a esse caos de identidade, uma missão surgiu.
                Nosso objetivo: explorar o impacto da Inteligência Artificial (IA) em nossas vidas e confrontar as
                possibilidades que o futuro nos reserva.
                O mundo nunca mais será o mesmo.
            </p>
            <button class=\"iniciar-btn\">Iniciar</button>
        </div>
        <div class=\"caixa-perguntas\"></div>
        <div class=\"caixa-alternativas\"></div>
        <div class=\"caixa-resultado\">
            <p class=\"texto-resultado\"></p>
            <button class=\"novamente-btn\">Jogar novamente</button>
        </div>
    </div>
    <script type=\"module\" src=\"js/aleatorio.js\"></script>
    <script type=\"module\" src=\"js/perguntas.js\"></script>
    <script type=\"module\" src=\"js/script.js\"></script>
</body>

</html>
```

E aqui está um exemplo de CSS para estilizar o projeto:
```css
body {
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;
    margin: 0;
    padding: 20px;
}

.caixa-principal {
    background-color: #fff;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

.iniciar-btn, .novamente-btn {
    background-color: #007bff;
    color: white;
    border: none;
    padding: 10px 15px;
    border-radius: 5px;
    cursor: pointer;
}

.iniciar-btn:hover, .novamente-btn:hover {
    background-color: #0056b3;
}
```

E uma ideia básica para o arquivo JavaScript (`script.js`):
```javascript
document.querySelector('.iniciar-btn').addEventListener('click', () => {
    document.querySelector('.tela-inicial').style.display = 'none';
    document.querySelector('.caixa-perguntas').innerHTML = '<p>Qual é o seu maior medo sobre a IA?</p>';
});

document.querySelector('.novamente-btn').addEventListener('click', () => {
    location.reload();
});

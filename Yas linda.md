<!DOCTYPE html>
<html>
<head>
    <title>Yas linda </title>
    <style>
        body {
            background-color: black;
            color: white;
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        h2 {
            font-size: 24px;
        }
        .buttons-container {
            display: flex;
            justify-content: center;
            align-items: center;
            margin-top: 20px;
        }
        .button {
            background-color: white;
            color: blue;
            border: 1px solid blue;
            border-radius: 10px;
            padding: 10px 20px;
            margin: 10px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <h2>vai me ver amanhã?</h2>
    <div class="buttons-container">
        <div class="button" onclick="showMessage('Sim')">Sim</div>
        <div class="button" id="noButton" onmouseover="moveRandomly()">Não</div>
    </div>

    <script>
        function showMessage(answer) {
            if (answer === 'Sim') {
                alert('Finalmente, Eu te gosto minha sapequinha .');
            }
        }

        function moveRandomly() {
            const noButton = document.getElementById('noButton');
            const windowWidth = window.innerWidth;
            const windowHeight = window.innerHeight;

            const randomX = Math.random() * (windowWidth - 100);
            const randomY = Math.random() * (windowHeight - 40);

            noButton.style.position = 'absolute';
            noButton.style.left = `${randomX}px`;
            noButton.style.top = `${randomY}px`;
        }
    </script>
</body>
</html>

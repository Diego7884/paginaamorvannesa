<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mensaje de Amor</title>   
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #ffdde1;
            margin: 0;
            overflow: hidden;
        }
        .video-background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            z-index: -1;
        }
        .container {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: white;
            font-size: 24px;
            font-weight: bold;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
            width: 80%;
            max-width: 600px;
            text-align: center;
            background: rgba(0, 0, 0, 0.5);
            padding: 20px;
            border-radius: 10px;
        }
        .title {
            font-size: 32px;
            font-weight: bold;
            margin-bottom: 20px;
            position: absolute;
            top: 10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100%;
            text-align: center;
            color: #ff33007a; /* Color amarillo */
        }
    </style>
</head>
<body>
    <button onclick="document.getElementById('musica').play()">Reproducir música</button>
    <audio id="musica" loop>
        <source src="musica.mp3" type="audio/mpeg">
        Tu navegador no soporta audio.
    </audio>
    <script>
        document.addEventListener("click", function() {
            document.getElementById("musica").play();
        }, { once: true });
    </script>

    <video class="video-background" autoplay loop muted>
        <source src="video.mp4" type="video/mp4">
        Tu navegador no soporta videos.
    </video>

    <div class="title">Un Mensaje Especial Para Ti Mis Ojitos ❤️</div>
    <div class="container">
        <div id="messageContainer">Cargando...</div>
    </div>
    

    <script>
        const messages = [
            "Eres la persona más especial en mi vida ❤️",
            "Cada día a tu lado es un regalo 🎁",
            "Tu sonrisa ilumina mi mundo ✨",
            "Te amo más de lo que las palabras pueden expresar 💖",
            "Tus ojitos son los mas preciosos mi princesa👸",
            " Mi niña consentida sus besos sosn encatadores 💏",
        ];
        let index = 0;
        const messageContainer = document.getElementById("messageContainer");

        function showMessage() {
            messageContainer.innerHTML = messages[index];
            index = (index + 1) % messages.length; // Reinicia el índice cuando llega al final
        }

        // Mostrar el primer mensaje de inmediato
        showMessage();

        // Cambiar el mensaje cada 3 segundos
        setInterval(showMessage, 3000);
    </script>
</body>
</html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Para Katheee 💖</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;700;900&family=Dancing+Script:wght@400;700&display=swap');
        
        /* Estilo general de la página */
        body {
            text-align: center;
            background: url('https://www.ecoticias.com/wp-content/uploads/2024/02/avion.jpg') no-repeat center center fixed;
            background-size: cover;
            font-family: 'Poppins', sans-serif;
            color: white;
            animation: fadeIn 2s ease-in-out;
            min-height: 100vh;
            margin: 0; /* Eliminar márgenes por defecto */
        }

        .container {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 40px;
            border-radius: 20px;
            background: rgba(0, 0, 0, 0.7);
            box-shadow: 0 6px 20px rgba(255, 255, 255, 0.3);
            width: 100%; /* Aseguramos que ocupe todo el ancho disponible */
            max-width: 960px; /* Limitar el tamaño máximo */
            margin: 0 auto; /* Centrado */
        }

        h1 {
            font-size: 6rem;
            margin-bottom: 20px;
            text-shadow: 6px 6px 15px rgba(0, 0, 0, 0.7);
            animation: slideDown 1.5s ease-in-out;
            font-weight: 900;
            font-family: 'Dancing Script', cursive;
            word-wrap: break-word; /* Asegura que el título se ajuste a la pantalla */
        }

        p {
            font-size: 1.6rem;
            max-width: 800px;
            padding: 0 20px;
            text-shadow: 3px 3px 7px rgba(0, 0, 0, 0.7);
            animation: fadeIn 2.5s ease-in-out;
            font-weight: 600;
            margin-bottom: 30px;
            word-wrap: break-word; /* Evita que el texto se desborde */
        }

        img {
            width: 80%;
            max-width: 600px;
            margin-top: 20px;
            border-radius: 15px;
            box-shadow: 0px 6px 15px rgba(0, 0, 0, 0.6);
            animation: fadeIn 3s ease-in-out;
            cursor: pointer;
            transition: transform 0.3s ease-in-out;
        }

        .separator {
            width: 60%;
            height: 2px;
            background: white;
            margin: 20px 0;
        }

        .music {
            margin-top: 40px;
        }

        .play-btn {
            background: linear-gradient(to right, #ff758c, #ff7eb3);
            color: white;
            padding: 15px 40px;
            font-size: 2rem;
            border: none;
            border-radius: 30px;
            cursor: pointer;
            box-shadow: 0px 6px 12px rgba(0, 0, 0, 0.6);
            transition: 0.3s;
            font-weight: 900;
        }

        .play-btn:hover {
            background: linear-gradient(to right, #ff4e50, #ff2024);
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes slideDown {
            from { transform: translateY(-50px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }

        /* Estilos adicionales para móviles */
        @media (max-width: 768px) {
            h1 {
                font-size: 4.5rem;
            }

            p {
                font-size: 1.5rem;
            }

            .container {
                padding: 20px;
            }

            .separator {
                width: 80%;
            }

            .music {
                margin-top: 30px;
            }

            .play-btn {
                font-size: 1.8rem;
            }

            img {
                width: 90%; /* Imágenes más grandes en móviles */
            }
        }

        /* Evitar el desplazamiento horizontal */
        html, body {
            overflow-x: hidden;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Katheee 💖</h1>
        <p>Eres una persona, única y especial. Tu nombre refleja la luz y la belleza que llevas dentro. Gracias por estar en mi vida. En tan poco tiempo aprendiste cómo entrar a mi corazón, enseñarme a ser berraco y pelear por todo... ✨</p>
        
        <!-- Imagen especial con funcionalidad de clic para ampliar -->
        <img src="https://i.imgur.com/kVt8uvm.jpeg" alt="Imagen especial" class="expandable" onclick="toggleImageSize(this)">  
        
        <div class="music">
            <audio id="song" preload="auto">
                <source src="https://www.dropbox.com/scl/fi/qm1v2zvm6wjfrfesmoxoy/Coldplay-Yellow-Official-Video-Coldplay.mp3?rlkey=55c6o2xrneylygb9xlc7ns401&st=bxwh74b3&dl=1" type="audio/mpeg">
            </audio>
            <button class="play-btn" onclick="togglePlay()">▶️ Reproducir</button>
        </div>
        <div class="separator"></div>
        <img src="https://media.cnn.com/api/v1/images/stellar/prod/cnne-1446530-el-tierno-momento-en-el-que-unos-pandas-bebes-comen-en-china.jpg?c=original" alt="Panda">
        <p>Tu ternura y calidez me recuerdan a un panda, ese ser adorable que con solo verlo da ganas de abrazarlo. Así eres tú, con tu dulzura haces que el mundo se sienta más lindo. 🐼💕</p>
        <div class="separator"></div>
        <img src="https://images.unsplash.com/photo-1647673542835-ca8c891674cc?fm=jpg&q=60&w=3000" alt="Mariposa">
        <p>Las mariposas simbolizan transformación y belleza. Eres como una mariposa, trayendo luz y color a la vida de quienes te rodean. 🦋✨</p>
        <div class="separator"></div>
        <img src="https://i.pinimg.com/564x/8f/9e/86/8f9e86a4eea6e55aa4e2ca6f32714f0f.jpg" alt="Pollo">
        <p>Los pollos pueden ser pequeños, pero tienen un gran espíritu. Me recuerdas a ellos porque aunque parezcas frágil, tienes una fuerza y valentía increíble. 🐔❤️</p>
    </div>

    <script>
        function togglePlay() {
            var song = document.getElementById("song");
            var button = document.querySelector(".play-btn");
            if (song.paused) {
                song.currentTime = 2; // Iniciar la canción desde el segundo 2
                song.play();
                fadeInAudio(song); // Llamamos a la función fade-in
                button.textContent = "⏸️ Pausar";
            } else {
                song.pause();
                button.textContent = "▶️ Reproducir";
            }
        }

        function fadeInAudio(audio) {
            audio.volume = 0; // Comienza el volumen en 0
            var fadeInInterval = setInterval(function() {
                if (audio.volume < 1) {
                    audio.volume += 0.05; // Aumentar el volumen de manera gradual
                } else {
                    clearInterval(fadeInInterval);
                }
            }, 200); // Aumentar cada 200 ms para lograr un fade-in de 4 segundos
        }

        // Función para alternar el tamaño de la imagen al hacer clic
        function toggleImageSize(img) {
            if (img.classList.contains("expanded")) {
                img.classList.remove("expanded");
                img.style.transform = "scale(1)";
            } else {
                img.classList.add("expanded");
                img.style.transform = "scale(2)";
            }
        }
    </script>
</body>
</html>

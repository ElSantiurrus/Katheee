<html lang="es">
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
        <!-- Imágenes de Panda, Mariposa y Pollo más grandes -->
        <img src="https://media.cnn.com/api/v1/images/stellar/prod/cnne-1446530-el-tierno-momento-en-el-que-unos-pandas-bebes-comen-en-china.jpg?c=original" alt="Panda" style="width: 80%;">
        <p>Tu ternura y calidez me recuerdan a un panda, ese ser adorable que con solo verlo da ganas de abrazarlo. Así eres tú, con tu dulzura haces que el mundo se sienta más lindo. 🐼💕</p>
        <div class="separator"></div>
        <img src="https://images.unsplash.com/photo-1647673542835-ca8c891674cc?fm=jpg&q=60&w=3000" alt="Mariposa" style="width: 80%;">
        <p>Las mariposas simbolizan transformación y belleza. Eres como una mariposa, trayendo luz y color a la vida de quienes te rodean. 🦋✨</p>
        <div class="separator"></div>
        <img src="https://i.pinimg.com/564x/8f/9e/86/8f9e86a4eea6e55aa4e2ca6f32714f0f.jpg" alt="Pollo" style="width: 80%;">
        <p>Los pollos pueden ser pequeños, pero tienen un gran espíritu. Me recuerdas a ellos porque aunque parezcas frágil, tienes una fuerza y valentía increíble. 🐔❤️</p>
    </div>
    <script>
        function togglePlay() {
            var song = document.getElementById("song");
            var button = document.querySelector(".play-btn");
            if (song.paused) {
                song.currentTime = 2;
                song.play();
                fadeInAudio(song); // Llamamos a la función fade-in
                button.textContent = "⏸️ Pausar";
            } else {
                song.pause();
                button.textContent = "▶️ Reproducir";
            }
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

        // Función para hacer un fade-in en el audio
        function fadeInAudio(audio) {
            let fadeDuration = 5; // Duración del fade en segundos
            let fadeStep = 0.02;  // Cuánto aumentar el volumen por intervalo
            let interval = fadeDuration * 1000 * fadeStep; // Intervalo en milisegundos
            let volume = 0;
            audio.volume = volume;

            let fadeInInterval = setInterval(function() {
                if (volume < 1) {
                    volume += fadeStep;
                    audio.volume = volume;
                } else {
                    clearInterval(fadeInInterval);
                }
            }, interval);
        }
    </script>
</body>
</html>

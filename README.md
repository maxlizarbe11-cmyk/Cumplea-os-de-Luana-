# Cumplea-os-de-Luana-
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>¡Feliz Cumpleaños Luana!</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        body {
            background: linear-gradient(135deg, #ffe5ec, #ffc2d1);
            font-family: 'Arial Rounded MT Bold', 'Helvetica', sans-serif;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
            overflow: hidden;
            text-align: center;
            padding: 20px;
        }
        .card {
            background: rgba(255, 255, 255, 0.9);
            padding: 30px;
            border-radius: 25px;
            box-shadow: 0 10px 30px rgba(255, 75, 110, 0.2);
            max-width: 400px;
            width: 100%;
            z-index: 10;
            transform: scale(0.9);
            animation: aparecer 1s forwards ease-out;
        }
        .fox-container {
            width: 100%;
            border-radius: 15px;
            overflow: hidden;
            margin-bottom: 20px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        .fox-container img {
            width: 100%;
            display: block;
        }
        h1 {
            font-size: 2rem;
            color: #ff477e;
            margin-bottom: 15px;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.1);
        }
        p {
            color: #6c757d;
            font-size: 1.1rem;
            line-height: 1.5;
            margin-bottom: 20px;
        }
        .btn {
            background: #ff477e;
            color: white;
            border: none;
            padding: 12px 25px;
            font-size: 1.1rem;
            border-radius: 50px;
            cursor: pointer;
            font-weight: bold;
            transition: transform 0.2s, background 0.2s;
            box-shadow: 0 5px 15px rgba(255, 75, 110, 0.4);
        }
        .btn:active {
            transform: scale(0.95);
            background: #ff5c8a;
        }
        /* Corazones flotantes */
        .heart {
            position: absolute;
            color: #ff7096;
            font-size: 20px;
            pointer-events: none;
            animation: flotar 4s linear infinite;
            opacity: 0;
        }
        @keyframes aparecer {
            to { transform: scale(1); }
        }
        @keyframes flotar {
            0% {
                transform: translateY(100vh) rotate(0deg);
                opacity: 1;
            }
            100% {
                transform: translateY(-10vh) rotate(360deg);
                opacity: 0;
            }
        }
    </style>
</head>
<body>

    <div class="card">
        <div class="fox-container">
            <!-- Aquí usamos la imagen del zorrito que generamos antes -->
            <img src="https://squarespace-cdn.com" id="fox-img" alt="Zorrito Kawaii">
        </div>
        <h1>¡Feliz Cumpleaños, Luana! 💖</h1>
        <p>Eres la persona más especial del mundo entero. Presiona el botón para recibir todo mi amor en este día.</p>
        <button class="btn" onclick="lanzarCorazones()">¡Presióname! ✨</button>
    </div>

    <script>
        // Cambia este enlace por el enlace directo de TU imagen del zorrito si la subes a internet
        const URL_IMAGEN_ZORRITO = "https://ibb.co"; 
        
        // Reemplazar la demo con la imagen real si quieres
        // document.getElementById('fox-img').src = URL_IMAGEN_ZORRITO;

        function crearCorazon() {
            const heart = document.createElement('div');
            heart.classList.add('heart');
            heart.innerHTML = '💖';
            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.animationDuration = Math.random() * 2 + 3 + 's';
            heart.style.fontSize = Math.random() * 20 + 15 + 'px';
            document.body.appendChild(heart);
            
            setTimeout(() => {
                heart.remove();
            }, 5000);
        }

        // Crea corazones automáticos al cargar
        setInterval(crearCorazon, 400);

        // Explosión de corazones al presionar el botón
        function lanzarCorazones() {
            for(let i = 0; i < 30; i++) {
                setTimeout(crearCorazon, i * 50);
            }
        }
    </script>
</body>
</html>

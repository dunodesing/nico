<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para mi reina</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #ffafbd, #ffc3a0);
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
        }

        .card {
            background: rgba(255, 255, 255, 0.9);
            padding: 40px 30px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            text-align: center;
            max-width: 450px;
            width: 90%;
            transition: all 0.5s ease;
        }

        .heart-icon {
            font-size: 50px;
            color: #ff4b5c;
            margin-bottom: 20px;
            animation: pulse 1.5s infinite;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }

        h2 {
            color: #d81b60;
            margin-bottom: 15px;
            font-size: 24px;
        }

        .btn-open {
            background-color: #ff4b5c;
            color: white;
            border: none;
            padding: 12px 28px;
            font-size: 18px;
            font-weight: bold;
            border-radius: 50px;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(255, 75, 92, 0.4);
            transition: transform 0.2s, background-color 0.2s;
        }

        .btn-open:hover {
            background-color: #e03848;
            transform: translateY(-2px);
        }

        .btn-open:active {
            transform: translateY(1px);
        }

        .letter-content {
            display: none;
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.8s ease, transform 0.8s ease;
        }

        .letter-content.show {
            display: block;
            opacity: 1;
            transform: translateY(0);
        }

        .message {
            color: #555;
            font-size: 17px;
            line-height: 1.6;
            margin-bottom: 25px;
            text-align: justify;
        }

        .signature {
            font-family: 'Georgia', serif;
            font-size: 20px;
            font-weight: bold;
            color: #d81b60;
            font-style: italic;
        }
    </style>
</head>
<body>

    <div class="card" id="mainCard">
        <div class="heart-icon">❤️</div>
        
        <!-- Vista inicial -->
        <div id="initialView">
            <h2>Tengo algo que decirte...</h2>
            <p style="color: #777; margin-bottom: 25px;">Presiona el botón para descubrirlo.</p>
            <button class="btn-open" onclick="revealLetter()">Abrir con amor</button>
        </div>

        <!-- Texto oculto que se revelará -->
        <div id="letterView" class="letter-content">
            <p class="message">
                Desde que llegaste a mi vida, todo tiene un color diferente, más bonito y alegre. Cada momento a tu lado se ha convertido en mi parte favorita del día, y no hay nada que me haga más feliz que ver tu sonrisa. Gracias por ser mi apoyo, mi confidente y la persona que me complementa en cada detalle. Este es solo un pequeño detalle para recordarte lo especial que eres para mí todos los días.
            </p>
            <p class="signature">Te amo mi vida, con amor Alan...</p>
        </div>
    </div>

    <script>
        function revealLetter() {
            // Oculta la vista inicial
            document.getElementById('initialView').style.display = 'none';
            
            // Muestra la carta con animación
            const letter = document.getElementById('letterView');
            letter.classList.add('show');
        }
    </script>

</body>
</html>

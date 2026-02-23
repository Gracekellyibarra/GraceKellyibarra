<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Grace Kelly Ibarra | Full Stack Portfolio</title>
    <style>
        :root {
            --matrix-green: #00ff41;
            --dark-green: #003b00;
            --bg-black: #0d0208;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Courier New', Courier, monospace;
            background-color: var(--bg-black);
            color: var(--matrix-green);
            overflow-x: hidden;
            line-height: 1.6;
        }

        /* Canvas para el efecto de lluvia */
        #matrix-canvas {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            opacity: 0.8;
        }

        /* Contenedor principal con efecto de terminal */
        .container {
            max-width: 900px;
            margin: 40px auto;
            padding: 20px;
            background: rgba(0, 0, 0, 0.85);
            border: 1px solid var(--matrix-green);
            box-shadow: 0 0 15px var(--dark-green);
            position: relative;
        }

        header {
            text-align: center;
            border-bottom: 2px solid var(--matrix-green);
            padding-bottom: 20px;
            margin-bottom: 30px;
        }

        h1 {
            font-size: 2.2rem;
            text-transform: uppercase;
            letter-spacing: 3px;
            text-shadow: 0 0 8px var(--matrix-green);
        }

        .subtitle {
            font-size: 1.1rem;
            color: #fff;
            text-shadow: 0 0 5px var(--matrix-green);
        }

        h2 {
            font-size: 1.8rem;
            margin: 20px 0;
            border-left: 5px solid var(--matrix-green);
            padding-left: 10px;
            text-transform: uppercase;
        }

        .proyecto {
            border: 1px dashed var(--matrix-green);
            padding: 15px;
            margin-bottom: 20px;
            transition: 0.3s;
        }

        .proyecto:hover {
            background: rgba(0, 255, 65, 0.1);
            transform: scale(1.02);
        }

        .highlight {
            color: #fff;
            font-weight: bold;
        }

        /* Botones estilo terminal */
        .redes {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
            justify-content: center;
            margin-top: 20px;
        }

        .redes a {
            color: var(--bg-black);
            background-color: var(--matrix-green);
            padding: 10px 20px;
            text-decoration: none;
            font-weight: bold;
            border: 2px solid var(--matrix-green);
            transition: 0.3s;
        }

        .redes a:hover {
            background-color: transparent;
            color: var(--matrix-green);
            box-shadow: 0 0 10px var(--matrix-green);
        }

        footer {
            text-align: center;
            margin-top: 40px;
            font-size: 0.8rem;
            opacity: 0.7;
        }

        /* Animación de cursor */
        .cursor {
            display: inline-block;
            width: 10px;
            height: 20px;
            background: var(--matrix-green);
            animation: blink 1s infinite;
            vertical-align: middle;
        }

        @keyframes blink {
            50% { opacity: 0; }
        }
    </style>
</head>
<body>

    <canvas id="matrix-canvas"></canvas>

    <div class="container">
        <header>
            <h1>Grace Kelly Ibarra<span class="cursor"></span></h1>
            <p class="subtitle">Full Stack Dev | Data Analyst | Cybersecurity</p>
        </header>

        <section id="sobre-mi">
            <h2>> /Sobre_mí</h2>
            <p>Egresada de <span class="highlight">Ingeniería de Software</span>. Especialista en construir soluciones digitales escalables y seguras.</p>
            <p>Estado actual: <span class="highlight">Preparando IELTS 5.0 / Destino Australia 2026</span>.</p>
        </section>

        <section id="proyectos">
            <h2>> /Proyectos_destacados</h2>
            
            <div class="proyecto">
                <h3>[01] Predicción Riesgo Neonatal</h3>
                <p>Stacking Machine Learning para análisis preventivo de salud.</p>
            </div>

            <div class="proyecto">
                <h3>[02] Web Corporativa - RDH</h3>
                <p>Desarrollo Full Stack con calculadora de inversión integrada.</p>
            </div>

            <div class="proyecto">
                <h3>[03] Dashboard KPIs</h3>
                <p>Inteligencia de negocios con Power BI y DAX.</p>
            </div>
        </section>

        <section id="contacto">
            <h2>> /Conectar</h2>
            <div class="redes">
                <a href="#">LINKEDIN</a>
                <a href="#">WHATSAPP</a>
                <a href="#">GMAIL</a>
            </div>
        </section>

        <footer>
            <p>SISTEMA OPERATIVO GRACE v2.0.26 - © TODOS LOS DERECHOS RESERVADOS</p>
        </footer>
    </div>

    <script>
        const canvas = document.getElementById('matrix-canvas');
        const ctx = canvas.getContext('2d');

        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;

        const letters = "ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789@#$%^&*()*&^";
        const fontSize = 16;
        const columns = canvas.width / fontSize;

        const drops = [];
        for (let x = 0; x < columns; x++) {
            drops[x] = 1;
        }

        function draw() {
            ctx.fillStyle = "rgba(0, 0, 0, 0.05)";
            ctx.fillRect(0, 0, canvas.width, canvas.height);

            ctx.fillStyle = "#00ff41";
            ctx.font = fontSize + "px monospace";

            for (let i = 0; i < drops.length; i++) {
                const text = letters.charAt(Math.floor(Math.random() * letters.length));
                ctx.fillText(text, i * fontSize, drops[i] * fontSize);

                if (drops[i] * fontSize > canvas.height && Math.random() > 0.975) {
                    drops[i] = 0;
                }
                drops[i]++;
            }
        }

        setInterval(draw, 33);

        window.addEventListener('resize', () => {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
        });
    </script>
</body>
</html>

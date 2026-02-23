<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Grace Kelly Ibarra | Portfolio System</title>
    <style>
        :root {
            --matrix-green: #00ff41;
            --dark-green: #003b00;
            --bg-black: #0d0208;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            font-family: 'Courier New', Courier, monospace;
            background-color: var(--bg-black);
            color: var(--matrix-green);
            line-height: 1.4;
            overflow-x: hidden;
        }

        #matrix-canvas {
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            z-index: -1;
            opacity: 0.6;
        }

        .container {
            max-width: 1000px;
            margin: 20px auto;
            padding: 20px;
            background: rgba(0, 0, 0, 0.9);
            border: 1px solid var(--matrix-green);
            box-shadow: 0 0 20px var(--dark-green);
        }

        header {
            text-align: center;
            border-bottom: 2px solid var(--matrix-green);
            padding-bottom: 20px;
            margin-bottom: 30px;
        }

        .lang-section { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; }
        .en { color: #88ff88; font-style: italic; border-left: 1px solid var(--dark-green); padding-left: 15px; }
        
        h1 { font-size: 2rem; text-transform: uppercase; letter-spacing: 2px; }
        h2 { font-size: 1.4rem; margin: 20px 0 10px; border-bottom: 1px solid var(--matrix-green); display: inline-block; }
        h3 { color: #fff; margin-top: 10px; }

        .skill-grid { display: flex; flex-wrap: wrap; gap: 10px; margin: 10px 0; }
        .skill-tag { 
            border: 1px solid var(--matrix-green); 
            padding: 3px 8px; 
            font-size: 0.85rem;
            background: rgba(0, 59, 0, 0.3);
        }

        .project-card {
            border: 1px solid var(--matrix-green);
            margin: 15px 0;
            padding: 15px;
            transition: 0.3s;
        }

        .project-card:hover { background: rgba(0, 255, 65, 0.1); }

        .btn {
            display: inline-block;
            margin-top: 10px;
            padding: 5px 15px;
            background: var(--matrix-green);
            color: #000;
            text-decoration: none;
            font-weight: bold;
            text-transform: uppercase;
        }

        .btn:hover { background: #fff; }

        ul { list-style: none; }
        li::before { content: "> "; color: var(--matrix-green); }

        .thesis-box {
            background: rgba(255, 255, 255, 0.05);
            padding: 15px;
            border-left: 4px solid var(--matrix-green);
        }
    </style>
</head>
<body>

<canvas id="matrix-canvas"></canvas>

<div class="container">
    <header>
        <h1>Grace Kelly Ibarra</h1>
        <p>Software Engineer | Full Stack | Data Analyst | Cybersecurity</p>
    </header>

    <section class="lang-section">
        <div class="es">
            <h2>🔹 RESUMEN PROFESIONAL</h2>
            <p>Egresada de Ingeniería de Software (Tercio Superior) con enfoque en Desarrollo Full Stack. Experiencia en construcción de aplicaciones web end-to-end con Java, Node.js y Arquitectura MVC. Certificada por IBM, Google y Microsoft en ciberseguridad y análisis de datos.</p>
        </div>
        <div class="en">
            <h2>🔹 PROFESSIONAL SUMMARY</h2>
            <p>Software Engineering graduate (Top 30%) focused on Full Stack Development. Experienced in building end-to-end web applications using Java, Node.js, and MVC Architecture. Certified by IBM, Google, and Microsoft in cybersecurity and data analysis.</p>
        </div>
    </section>

    <section>
        <h2>🔬 TESIS: PREDICCIÓN DE RIESGO NEONATAL</h2>
        <div class="thesis-box">
            <p><strong>Stacking Machine Learning Model:</strong> Implementación de un modelo predictivo avanzado para evaluar riesgos prenatales basados en datos clínicos.</p>
            <p><strong>Detalle Técnico:</strong> Uso de técnicas de ensamble (Stacking) para combinar múltiples algoritmos, optimizando la precisión en el diagnóstico preventivo de salud neonatal.</p>
        </div>
    </section>

    <h2>💻 COMPETENCIAS TÉCNICAS / TECHNICAL SKILLS</h2>
    <div class="skill-grid">
        <span class="skill-tag">Java (Intermediate)</span> <span class="skill-tag">JavaScript</span> 
        <span class="skill-tag">Node.js</span> <span class="skill-tag">C#</span> <span class="skill-tag">SQL Server</span>
        <span class="skill-tag">Kali Linux</span> <span class="skill-tag">Power BI (DAX)</span> <span class="skill-tag">Cisco Networking</span>
    </div>

    <section class="lang-section">
        <div class="es">
            <h2>💼 EXPERIENCIA LABORAL</h2>
            <h3>Asistente de Soporte y Desarrollo - RDH Industrial</h3>
            <ul>
                <li>Desarrollo de sitio corporativo con Node.js y MVC.</li>
                <li>Configuración de Hosting y DNS.</li>
                <li>Optimización de procesos con Excel avanzado.</li>
            </ul>
        </div>
        <div class="en">
            <h2>💼 WORK EXPERIENCE</h2>
            <h3>Support & Development Assistant - RDH Industrial</h3>
            <ul>
                <li>Corporate website development using Node.js and MVC.</li>
                <li>Hosting and DNS configuration.</li>
                <li>Process optimization via advanced Excel automation.</li>
            </ul>
        </div>
    </section>

    <h2>🚀 PROYECTOS / PROJECTS</h2>
    
    <div class="project-card">
        <h3>🎬 Cine App (Full Stack)</h3>
        <p>Sistema de gestión y cartelera desarrollado con Node.js y bases de datos relacionales.</p>
        <a href="#" class="btn">View Project</a>
    </div>

    <div class="project-card">
        <h3>🏗️ RDH Constructora Web</h3>
        <p>Sitio corporativo con arquitectura MVC, incluyendo calculadora de inversión para clientes.</p>
        <a href="#" class="btn">View Project</a>
    </div>

    <div class="project-card">
        <h3>📊 Dashboard KPIs - Power BI</h3>
        <p>Visualización de indicadores comerciales y académicos usando DAX.</p>
        <a href="#" class="btn">View Data Analysis</a>
    </div>

    <section class="lang-section">
        <div class="es">
            <h2>📜 CERTIFICACIONES</h2>
            <ul>
                <li>Ethical Hacking (CEH) – CTIC UNI</li>
                <li>Especialización Ciberseguridad – IBM</li>
                <li>Business Analytics – Johns Hopkins</li>
            </ul>
        </div>
        <div class="en">
            <h2>📜 CERTIFICATIONS</h2>
            <ul>
                <li>Ethical Hacking (CEH) – CTIC UNI</li>
                <li>Cybersecurity Specialization – IBM</li>
                <li>Business Analytics – Johns Hopkins</li>
            </ul>
        </div>
    </section>

    <section style="text-align: center; margin-top: 20px; border-top: 1px solid var(--matrix-green); padding: 10px;">
        <p><strong>LANGUAGES:</strong> Spanish (Native) | English (Intermediate - Preparing for IELTS)</p>
    </section>
</div>

<script>
    const canvas = document.getElementById('matrix-canvas');
    const ctx = canvas.getContext('2d');
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;

    const latin = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ';
    const nums = '0123456789';
    const alphabet = latin + nums;

    const fontSize = 16;
    const columns = canvas.width / fontSize;
    const rainDrops = Array.from({ length: columns }).fill(1);

    const draw = () => {
        ctx.fillStyle = 'rgba(0, 0, 0, 0.05)';
        ctx.fillRect(0, 0, canvas.width, canvas.height);
        ctx.fillStyle = '#0F0';
        ctx.font = fontSize + 'px monospace';

        for (let i = 0; i < rainDrops.length; i++) {
            const text = alphabet.charAt(Math.floor(Math.random() * alphabet.length));
            ctx.fillText(text, i * fontSize, rainDrops[i] * fontSize);
            if (rainDrops[i] * fontSize > canvas.height && Math.random() > 0.975) {
                rainDrops[i] = 0;
            }
            rainDrops[i]++;
        }
    };
    setInterval(draw, 30);
</script>

</body>
</html>

<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Alejandro Sánchez Rojas | Software Engineer & Data</title>
    <!-- Font Awesome para Iconos -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&family=Fira+Code:wght@400;500&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --bg-color: #0f172a;
            --card-bg: #1e293b;
            --card-border: #334155;
            --accent-color: #38bdf8;
            --accent-hover: #0284c7;
            --text-main: #f8fafc;
            --text-muted: #94a3b8;
            --tag-bg: rgba(56, 189, 248, 0.1);
            --tag-text: #38bdf8;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--bg-color);
            color: var(--text-main);
            line-height: 1.6;
            padding: 40px 20px;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
        }

        /* Hero / Header Section */
        header {
            background: linear-gradient(135deg, #1e293b 0%, #0f172a 100%);
            border: 1px solid var(--card-border);
            padding: 40px;
            border-radius: 16px;
            margin-bottom: 30px;
            box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.3);
            position: relative;
            overflow: hidden;
        }

        header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(90deg, #38bdf8, #818cf8, #c084fc);
        }

        .profile-title {
            font-size: 2.2rem;
            font-weight: 700;
            color: var(--text-main);
            margin-bottom: 6px;
            letter-spacing: -0.5px;
        }

        .subtitle {
            font-size: 1.1rem;
            color: var(--accent-color);
            font-weight: 600;
            margin-bottom: 16px;
            font-family: 'Fira Code', monospace;
        }

        .bio-short {
            color: var(--text-muted);
            font-size: 1rem;
            margin-bottom: 24px;
            max-width: 750px;
        }

        .social-links {
            display: flex;
            gap: 12px;
            flex-wrap: wrap;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background-color: rgba(255, 255, 255, 0.05);
            color: var(--text-main);
            padding: 10px 18px;
            border-radius: 8px;
            text-decoration: none;
            font-size: 0.9rem;
            font-weight: 600;
            border: 1px solid var(--card-border);
            transition: all 0.25s ease;
        }

        .btn:hover {
            background-color: var(--accent-color);
            color: #0f172a;
            border-color: var(--accent-color);
            transform: translateY(-2px);
        }

        .btn-primary {
            background-color: var(--accent-color);
            color: #0f172a;
            border-color: var(--accent-color);
        }

        .btn-primary:hover {
            background-color: var(--accent-hover);
            border-color: var(--accent-hover);
            color: #ffffff;
        }

        /* Sections */
        section {
            background-color: var(--card-bg);
            border: 1px solid var(--card-border);
            border-radius: 16px;
            padding: 32px;
            margin-bottom: 30px;
        }

        section h2 {
            font-size: 1.4rem;
            color: var(--text-main);
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
            border-bottom: 1px solid var(--card-border);
            padding-bottom: 12px;
        }

        section h2 i {
            color: var(--accent-color);
        }

        .about-text p {
            color: var(--text-muted);
            margin-bottom: 14px;
            font-size: 0.98rem;
        }

        /* Projects Grid */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 15px;
        }

        .project-card {
            background-color: rgba(15, 23, 42, 0.6);
            border: 1px solid var(--card-border);
            border-radius: 12px;
            padding: 22px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            transition: transform 0.25s ease, border-color 0.25s ease;
        }

        .project-card:hover {
            transform: translateY(-4px);
            border-color: var(--accent-color);
        }

        .project-card h3 {
            font-size: 1.15rem;
            color: var(--text-main);
            margin-bottom: 10px;
        }

        .project-card p {
            color: var(--text-muted);
            font-size: 0.9rem;
            margin-bottom: 14px;
        }

        .tags {
            display: flex;
            flex-wrap: wrap;
            gap: 6px;
            margin-bottom: 18px;
        }

        .tag {
            background-color: var(--tag-bg);
            color: var(--tag-text);
            font-size: 0.75rem;
            font-weight: 600;
            padding: 4px 10px;
            border-radius: 20px;
            font-family: 'Fira Code', monospace;
        }

        .card-link {
            display: inline-flex;
            align-items: center;
            gap: 6px;
            color: var(--accent-color);
            text-decoration: none;
            font-size: 0.88rem;
            font-weight: 600;
            margin-top: auto;
        }

        .card-link:hover {
            text-decoration: underline;
        }

        /* Footer */
        footer {
            text-align: center;
            color: var(--text-muted);
            font-size: 0.85rem;
            margin-top: 40px;
            padding-bottom: 20px;
        }

        /* Responsive */
        @media (max-width: 640px) {
            header, section {
                padding: 24px;
            }
            .profile-title {
                font-size: 1.8rem;
            }
            .projects-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

    <div class="container">
        
        <!-- Header / Hero Section -->
        <header>
            <h1 class="profile-title">Alejandro Sánchez Rojas</h1>
            <div class="subtitle">&lt;Software Engineering Student /&gt;</div>
            <p class="bio-short">
                Especializado en sistemas de datos, desarrollo de software y apasionado por la creación e industria de los videojuegos.
            </p>
            <div class="social-links">
                <a href="https://www.linkedin.com/in/alejandro-sanchez-rojas-a18376445/?isSelfProfile=true" target="_blank" class="btn btn-primary">
                    <i class="fab fa-linkedin"></i> LinkedIn
                </a>
                <a href="https://github.com/Alejosan05" target="_blank" class="btn">
                    <i class="fab fa-github"></i> GitHub
                </a>
            </div>
        </header>

        <!-- About Me Section -->
        <section>
            <h2><i class="fas fa-user-code"></i> Sobre mí / About Me</h2>
            <div class="about-text">
                <p>
                    <strong>Software Engineering student</strong> focused on software development, data management systems, and game creation. Experienced in building practical applications with <strong>Python</strong>, structured data processing using <strong>Excel</strong>, and implementing interactive software logic.
                </p>
                <p>
                    Más allá de las herramientas técnicas, enfoco mi aprendizaje en el pensamiento lógico para la resolución de problemas (<em>problem-solving</em>), la validación y limpieza de datos, y el diseño de sistemas interactivos. Busco la constante mejora de habilidades técnicas para construir aplicaciones eficientes y escalables.
                </p>
            </div>
        </section>

        <!-- Projects Section -->
        <section>
            <h2><i class="fas fa-cubes"></i> Proyectos Destacados / Projects</h2>
            
            <div class="projects-grid">
                
                <!-- Project 1 -->
                <div class="project-card">
                    <div>
                        <h3>Gestor de Inventario con Listas</h3>
                        <p><strong>Objetivo:</strong> Sistema para la administración, almacenamiento y manipulación de datos de inventario utilizando estructuras de datos optimizadas.</p>
                        <p><strong>Aprendizaje:</strong> Algoritmos de manipulación de listas, validación de datos y lógica de control de inventarios.</p>
                        <div class="tags">
                            <span class="tag">Python</span>
                            <span class="tag">Data Structures</span>
                            <span class="tag">CLI</span>
                        </div>
                    </div>
                    <a href="https://github.com/Alejosan05/gestor-inventario-listas" target="_blank" class="card-link">
                        Ver en GitHub <i class="fas fa-arrow-right"></i>
                    </a>
                </div>

                <!-- Project 2 -->
                <div class="project-card">
                    <div>
                        <h3>Sistemas de Datos & Proyectos Web</h3>
                        <p><strong>Objetivo:</strong> Desarrollo de aplicaciones interactivas y herramientas orientadas al procesamiento de información y lógica web.</p>
                        <p><strong>Aprendizaje:</strong> Maquetación estructurada, diseño adaptable y manejo de flujos de datos.</p>
                        <div class="tags">
                            <span class="tag">HTML5 / CSS3</span>
                            <span class="tag">JavaScript</span>
                            <span class="tag">Python</span>
                        </div>
                    </div>
                    <a href="https://github.com/Alejosan05" target="_blank" class="card-link">
                        Explorar repositorios <i class="fas fa-arrow-right"></i>
                    </a>
                </div>

            </div>
        </section>

        <!-- Contact Section -->
        <section>
            <h2><i class="fas fa-envelope"></i> Contacto Profesional / Contact</h2>
            <p style="color: var(--text-muted); margin-bottom: 20px;">
                ¿Te interesa conocer más sobre mis proyectos o colaborar en desarrollo de software y análisis de datos?
            </p>
            <div class="social-links">
                <a href="https://www.linkedin.com/in/alejandro-sanchez-rojas-a18376445/?isSelfProfile=true" target="_blank" class="btn btn-primary">
                    <i class="fab fa-linkedin"></i> Conectar en LinkedIn
                </a>
                <a href="https://github.com/Alejosan05" target="_blank" class="btn">
                    <i class="fab fa-github"></i> Seguir en GitHub
                </a>
            </div>
        </section>

        <footer>
            &copy; 2026 Alejandro Sánchez Rojas — Portafolio de Ingeniería de Software
        </footer>

    </div>

</body>
</html>

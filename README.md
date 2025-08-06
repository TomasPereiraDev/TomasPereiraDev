<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Portafolio Dev | Tu Nombre</title>
  <meta name="description" content="Portafolio profesional especializado en JavaScript, TypeScript, React y más">
  <meta name="keywords" content="desarrollador, JavaScript, TypeScript, React, Python, Ruby, Java, Docker">
  
  <!-- Preload -->
  <link rel="preload" href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;700&family=Space+Mono:wght@400;700&display=swap" as="style">
  <link rel="preload" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" as="style">
  
  <!-- Fuentes -->
  <link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;700&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  
  <style>
    /* Variables CSS */
    :root {
      --primary: #58a6ff;
      --secondary: #1f6feb;
      --accent: #f78166;
      --bg-dark: #0d1117;
      --bg-darker: #010409;
      --text: #c9d1d9;
      --text-light: #8b949e;
      --neon-effect: 0 0 10px currentColor;
      --transition: all 0.25s cubic-bezier(0.65, 0, 0.35, 1);
      --border-color: #30363d;
    }

    /* Reset y estilos base */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
      scroll-padding-top: 80px;
    }

    body {
      font-family: 'Space Mono', monospace;
      background-color: var(--bg-dark);
      color: var(--text);
      line-height: 1.6;
      overflow-x: hidden;
      -webkit-font-smoothing: antialiased;
    }

    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
    }

    /* Header */
    header {
      background-color: var(--bg-darker);
      border-bottom: 1px solid var(--border-color);
      position: fixed;
      width: 100%;
      top: 0;
      z-index: 100;
      padding: 20px 0;
    }

    .header-container {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      font-family: 'Fira Code', monospace;
      font-weight: 700;
      font-size: 1.5rem;
      color: var(--primary);
      text-decoration: none;
      transition: var(--transition);
    }

    .logo:hover {
      text-shadow: var(--neon-effect);
    }

    /* Navegación */
    .nav-links {
      display: flex;
      gap: 30px;
    }

    .nav-link {
      color: var(--text);
      text-decoration: none;
      font-family: 'Fira Code', monospace;
      font-size: 0.95rem;
      transition: var(--transition);
      position: relative;
      padding: 5px 0;
    }

    .nav-link:hover {
      color: var(--primary);
    }

    .nav-link::after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      width: 0;
      height: 2px;
      background: var(--primary);
      transition: var(--transition);
    }

    .nav-link:hover::after {
      width: 100%;
    }

    /* Hero Section */
    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      padding: 120px 0 80px;
      background: linear-gradient(to bottom, var(--bg-darker), var(--bg-dark));
    }

    .hero-content {
      max-width: 800px;
    }

    h1 {
      font-family: 'Fira Code', monospace;
      font-size: clamp(2rem, 5vw, 3.5rem);
      margin-bottom: 20px;
      line-height: 1.2;
      color: var(--primary);
    }

    .hero-title {
      background: linear-gradient(90deg, var(--primary), var(--accent));
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      display: inline-block;
    }

    .typewriter {
      font-size: clamp(1rem, 3vw, 1.25rem);
      color: var(--text-light);
      border-right: 2px solid var(--primary);
      white-space: nowrap;
      overflow: hidden;
      max-width: fit-content;
      animation: 
        typing 3.5s steps(40, end),
        blink-caret 0.75s step-end infinite;
    }

    @keyframes typing {
      from { width: 0 }
      to { width: 100% }
    }

    @keyframes blink-caret {
      from, to { border-color: transparent }
      50% { border-color: var(--primary) }
    }

    .hero-description {
      margin: 30px 0;
      font-size: 1.1rem;
      max-width: 600px;
    }

    /* Botones */
    .btn {
      padding: 12px 24px;
      border-radius: 6px;
      font-family: 'Fira Code', monospace;
      font-size: 0.95rem;
      text-decoration: none;
      transition: var(--transition);
      display: inline-flex;
      align-items: center;
      gap: 8px;
    }

    .btn-primary {
      background-color: var(--primary);
      color: var(--bg-darker);
      border: 1px solid var(--primary);
    }

    .btn-primary:hover {
      background-color: transparent;
      color: var(--primary);
      box-shadow: 0 0 15px rgba(88, 166, 255, 0.3);
    }

    .btn-outline {
      border: 1px solid var(--text-light);
      color: var(--text);
    }

    .btn-outline:hover {
      border-color: var(--primary);
      color: var(--primary);
      background-color: rgba(88, 166, 255, 0.1);
    }

    /* Secciones generales */
    section {
      padding: 80px 0;
      border-bottom: 1px solid var(--border-color);
    }

    .section-title {
      font-family: 'Fira Code', monospace;
      font-size: 2rem;
      margin-bottom: 40px;
      color: var(--primary);
      position: relative;
      display: inline-block;
    }

    .section-title::after {
      content: '';
      position: absolute;
      bottom: -8px;
      left: 0;
      width: 100%;
      height: 3px;
      background: linear-gradient(90deg, var(--primary), transparent);
    }

    /* Sobre mí */
    .about-content {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 40px;
      align-items: center;
    }

    .about-text {
      font-size: 1.1rem;
      line-height: 1.7;
    }

    .about-text p {
      margin-bottom: 20px;
    }

    .about-image {
      position: relative;
      border-radius: 10px;
      overflow: hidden;
      border: 1px solid var(--border-color);
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
    }

    .about-image img {
      width: 100%;
      height: auto;
      display: block;
    }

    /* Habilidades */
    .skills-container {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
      gap: 30px;
    }

    .skill-category {
      background-color: var(--bg-darker);
      border: 1px solid var(--border-color);
      border-radius: 10px;
      padding: 25px;
      transition: var(--transition);
    }

    .skill-category:hover {
      border-color: var(--primary);
      transform: translateY(-5px);
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
    }

    .skill-category-title {
      font-family: 'Fira Code', monospace;
      font-size: 1.25rem;
      margin-bottom: 20px;
      color: var(--primary);
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .skill-list {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }

    .skill {
      background-color: rgba(88, 166, 255, 0.1);
      border: 1px solid rgba(88, 166, 255, 0.3);
      color: var(--primary);
      padding: 6px 12px;
      border-radius: 20px;
      font-size: 0.85rem;
      font-family: 'Fira Code', monospace;
      transition: var(--transition);
    }

    .skill:hover {
      background-color: var(--primary);
      color: var(--bg-darker);
      transform: scale(1.05);
    }

    /* Proyectos */
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
      gap: 30px;
    }

    .project-card {
      background-color: var(--bg-darker);
      border: 1px solid var(--border-color);
      border-radius: 10px;
      overflow: hidden;
      transition: var(--transition);
    }

    .project-card:hover {
      border-color: var(--primary);
      transform: translateY(-5px);
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
    }

    .project-image {
      height: 200px;
      overflow: hidden;
      border-bottom: 1px solid var(--border-color);
    }

    .project-image img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: var(--transition);
    }

    .project-card:hover .project-image img {
      transform: scale(1.05);
    }

    .project-content {
      padding: 20px;
    }

    .project-title {
      font-family: 'Fira Code', monospace;
      font-size: 1.25rem;
      margin-bottom: 10px;
      color: var(--primary);
    }

    .project-description {
      color: var(--text-light);
      margin-bottom: 20px;
      font-size: 0.95rem;
    }

    .project-tech {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-bottom: 20px;
    }

    .tech-tag {
      background-color: rgba(88, 166, 255, 0.1);
      color: var(--primary);
      padding: 4px 10px;
      border-radius: 20px;
      font-size: 0.75rem;
      font-family: 'Fira Code', monospace;
    }

    .project-links {
      display: flex;
      gap: 15px;
    }

    .project-link {
      display: flex;
      align-items: center;
      gap: 5px;
      font-size: 0.9rem;
      color: var(--text);
      text-decoration: none;
      transition: var(--transition);
    }

    .project-link:hover {
      color: var(--primary);
    }

    /* Contacto */
    .contact-container {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 40px;
    }

    .contact-info {
      display: flex;
      flex-direction: column;
      gap: 20px;
    }

    .contact-item {
      display: flex;
      align-items: center;
      gap: 15px;
    }

    .contact-icon {
      width: 50px;
      height: 50px;
      border-radius: 50%;
      background-color: rgba(88, 166, 255, 0.1);
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--primary);
      font-size: 1.25rem;
    }

    .contact-text h3 {
      font-family: 'Fira Code', monospace;
      font-size: 1.1rem;
      margin-bottom: 5px;
      color: var(--primary);
    }

    .contact-text p, .contact-text a {
      color: var(--text-light);
      text-decoration: none;
      transition: var(--transition);
    }

    .contact-text a:hover {
      color: var(--primary);
    }

    .contact-form {
      background-color: var(--bg-darker);
      border: 1px solid var(--border-color);
      border-radius: 10px;
      padding: 30px;
    }

    .form-group {
      margin-bottom: 20px;
    }

    .form-label {
      display: block;
      margin-bottom: 8px;
      font-family: 'Fira Code', monospace;
      font-size: 0.9rem;
      color: var(--text);
    }

    .form-control {
      width: 100%;
      padding: 12px 15px;
      background-color: var(--bg-dark);
      border: 1px solid var(--border-color);
      border-radius: 6px;
      color: var(--text);
      font-family: 'Space Mono', monospace;
      transition: var(--transition);
    }

    .form-control:focus {
      outline: none;
      border-color: var(--primary);
      box-shadow: 0 0 0 3px rgba(88, 166, 255, 0.2);
    }

    textarea.form-control {
      min-height: 150px;
      resize: vertical;
    }

    .submit-btn {
      background-color: var(--primary);
      color: var(--bg-darker);
      border: none;
      padding: 12px 24px;
      border-radius: 6px;
      font-family: 'Fira Code', monospace;
      font-size: 0.95rem;
      cursor: pointer;
      transition: var(--transition);
      display: inline-flex;
      align-items: center;
      gap: 8px;
    }

    .submit-btn:hover {
      background-color: transparent;
      color: var(--primary);
      box-shadow: 0 0 15px rgba(88, 166, 255, 0.3);
      border: 1px solid var(--primary);
    }

    /* Footer */
    footer {
      background-color: var(--bg-darker);
      padding: 30px 0;
      text-align: center;
    }

    .social-links {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin-bottom: 20px;
    }

    .social-link {
      width: 40px;
      height: 40px;
      border-radius: 50%;
      background-color: rgba(88, 166, 255, 0.1);
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--text);
      font-size: 1.1rem;
      transition: var(--transition);
      text-decoration: none;
    }

    .social-link:hover {
      background-color: var(--primary);
      color: var(--bg-darker);
      transform: translateY(-3px);
    }

    .copyright {
      color: var(--text-light);
      font-size: 0.9rem;
    }

    /* Responsive */
    @media (max-width: 992px) {
      .about-content,
      .contact-container {
        grid-template-columns: 1fr;
      }
      
      .about-image {
        order: -1;
      }
    }

    @media (max-width: 768px) {
      .nav-links {
        position: fixed;
        top: 80px;
        left: 0;
        width: 100%;
        background-color: var(--bg-darker);
        flex-direction: column;
        align-items: center;
        padding: 20px 0;
        gap: 15px;
        display: none;
        border-bottom: 1px solid var(--border-color);
      }
      
      .nav-links.active {
        display: flex;
      }
      
      .hero-buttons {
        flex-direction: column;
        gap: 15px;
      }
      
      .projects-grid {
        grid-template-columns: 1fr;
      }
    }

    /* Animaciones */
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .fade-in {
      opacity: 0;
      animation: fadeIn 0.8s ease-out forwards;
    }

    .delay-1 { animation-delay: 0.2s; }
    .delay-2 { animation-delay: 0.4s; }
    .delay-3 { animation-delay: 0.6s; }
  </style>
</head>
<body>
  <!-- Header -->
  <header>
    <div class="container header-container">
      <a href="#" class="logo">dev@tuusuario</a>
      <nav class="nav-links">
        <a href="#about" class="nav-link">Sobre mí</a>
        <a href="#skills" class="nav-link">Habilidades</a>
        <a href="#projects" class="nav-link">Proyectos</a>
        <a href="#contact" class="nav-link">Contacto</a>
      </nav>
      <button class="mobile-menu-btn" aria-label="Menú">
        <i class="fas fa-bars"></i>
      </button>
    </div>
  </header>

  <!-- Hero -->
  <section class="hero">
    <div class="container">
      <div class="hero-content fade-in">
        <h1>Hola, soy <span class="hero-title">Tu Nombre</span></h1>
        <div class="typewriter delay-1">Desarrollador Full Stack | Especialista en JavaScript y TypeScript</div>
        <p class="hero-description delay-2">
          Apasionado por crear soluciones tecnológicas innovadoras con código limpio y eficiente. 
          Experiencia en desarrollo frontend y backend con las últimas tecnologías.
        </p>
        <div class="hero-buttons delay-3">
          <a href="#projects" class="btn btn-primary">
            <i class="fas fa-code"></i> Ver Proyectos
          </a>
          <a href="#contact" class="btn btn-outline">
            <i class="fas fa-paper-plane"></i> Contactar
          </a>
        </div>
      </div>
    </div>
  </section>

  <!-- Sobre mí -->
  <section id="about">
    <div class="container">
      <h2 class="section-title fade-in">Sobre mí</h2>
      <div class="about-content">
        <div class="about-text fade-in delay-1">
          <p>
            Desarrollador con 5+ años de experiencia creando aplicaciones web modernas y escalables. 
            Especializado en JavaScript, TypeScript y frameworks como React y Node.js.
          </p>
          <p>
            Mi enfoque combina diseño atractivo con funcionalidad robusta, asegurando experiencias 
            de usuario fluidas y código mantenible. Apasionado por aprender y adoptar nuevas tecnologías.
          </p>
          <p>
            Actualmente enfocado en arquitecturas de microservicios, desarrollo de componentes 
            reutilizables y optimización de performance.
          </p>
        </div>
        <div class="about-image fade-in delay-2">
          <img src="https://via.placeholder.com/500x500" alt="Tu Nombre - Desarrollador" loading="lazy">
        </div>
      </div>
    </div>
  </section>

  <!-- Habilidades -->
  <section id="skills">
    <div class="container">
      <h2 class="section-title fade-in">Habilidades</h2>
      <div class="skills-container">
        <!-- Lenguajes -->
        <div class="skill-category fade-in delay-1">
          <h3 class="skill-category-title"><i class="fas fa-code"></i> Lenguajes</h3>
          <div class="skill-list">
            <span class="skill">JavaScript</span>
            <span class="skill">TypeScript</span>
            <span class="skill">HTML5</span>
            <span class="skill">CSS3</span>
            <span class="skill">Ruby</span>
            <span class="skill">Python</span>
            <span class="skill">Java</span>
          </div>
        </div>
        
        <!-- Frontend -->
        <div class="skill-category fade-in delay-2">
          <h3 class="skill-category-title"><i class="fas fa-laptop-code"></i> Frontend</h3>
          <div class="skill-list">
            <span class="skill">React</span>
            <span class="skill">Redux</span>
            <span class="skill">Styled Components</span>
            <span class="skill">Storybook</span>
            <span class="skill">Jest</span>
            <span class="skill">Testing Library</span>
            <span class="skill">Webpack</span>
          </div>
        </div>
        
        <!-- Backend -->
        <div class="skill-category fade-in delay-3">
          <h3 class="skill-category-title"><i class="fas fa-server"></i> Backend</h3>
          <div class="skill-list">
            <span class="skill">Node.js</span>
            <span class="skill">Express</span>
            <span class="skill">Ruby on Rails</span>
            <span class="skill">Django</span>
            <span class="skill">Spring Boot</span>
            <span class="skill">GraphQL</span>
            <span class="skill">REST APIs</span>
          </div>
        </div>
        
        <!-- Herramientas -->
        <div class="skill-category fade-in delay-1">
          <h3 class="skill-category-title"><i class="fas fa-tools"></i> Herramientas</h3>
          <div class="skill-list">
            <span class="skill">Git</span>
            <span class="skill">Docker</span>
            <span class="skill">Kubernetes</span>
            <span class="skill">CI/CD</span>
            <span class="skill">AWS</span>
            <span class="skill">PostgreSQL</span>
            <span class="skill">MongoDB</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Proyectos -->
  <section id="projects">
    <div class="container">
      <h2 class="section-title fade-in">Proyectos Destacados</h2>
      <div class="projects-grid">
        <!-- Proyecto 1 -->
        <div class="project-card fade-in delay-1">
          <div class="project-image">
            <img src="https://via.placeholder.com/600x400" alt="Proyecto 1" loading="lazy">
          </div>
          <div class="project-content">
            <h3 class="project-title">Sistema de Componentes</h3>
            <p class="project-description">
              Biblioteca de componentes UI reutilizables construida con React, TypeScript y Storybook.
            </p>
            <div class="project-tech">
              <span class="tech-tag">React</span>
              <span class="tech-tag">TypeScript</span>
              <span class="tech-tag">Storybook</span>
              <span class="tech-tag">Styled Components</span>
            </div>
            <div class="project-links">
              <a href="#" class="project-link">
                <i class="fas fa-external-link-alt"></i> Demo
              </a>
              <a href="#" class="project-link">
                <i class="fab fa-github"></i> Código
              </a>
            </div>
          </div>
        </div>
        
        <!-- Proyecto 2 -->
        <div class="project-card fade-in delay-2">
          <div class="project-image">
            <img src="https://via.placeholder.com/600x400" alt="Proyecto 2" loading="lazy">
          </div>
          <div class="project-content">
            <h3 class="project-title">API E-commerce</h3>
            <p class="project-description">
              API RESTful para plataforma de e-commerce desarrollada con Node.js, Express y MongoDB.
            </p>
            <div class="project-tech">
              <span class="tech-tag">Node.js</span>
              <span class="tech-tag">Express</span>
              <span class="tech-tag">MongoDB</span>
              <span class="tech-tag">Jest</span>
              <span class="tech-tag">Docker</span>
            </div>
            <div class="project-links">
              <a href="#" class="project-link">
                <i class="fas fa-external-link-alt"></i> Docs
              </a>
              <a href="#" class="project-link">
                <i class="fab fa-github"></i> Código
              </a>
            </div>
          </div>
        </div>
        
        <!-- Proyecto 3 -->
        <div class="project-card fade-in delay-3">
          <div class="project-image">
            <img src="https://via.placeholder.com/600x400" alt="Proyecto 3" loading="lazy">
          </div>
          <div class="project-content">
            <h3 class="project-title">App de Tareas</h3>
            <p class="project-description">
              Aplicación full stack para gestión de tareas con autenticación y sincronización en tiempo real.
            </p>
            <div class="project-tech">
              <span class="tech-tag">React</span>
              <span class="tech-tag">Redux</span>
              <span class="tech-tag">Ruby on Rails</span>
              <span class="tech-tag">WebSockets</span>
            </div>
            <div class="project-links">
              <a href="#" class="project-link">
                <i class="fas fa-external-link-alt"></i> Demo
              </a>
              <a href="#" class="project-link">
                <i class="fab fa-github"></i> Código
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Contacto -->
  <section id="contact">
    <div class="container">
      <h2 class="section-title fade-in">Contacto</h2>
      <div class="contact-container">
        <div class="contact-info">
          <div class="contact-item fade-in delay-1">
            <div class="contact-icon">
              <i class="fas fa-envelope"></i>
            </div>
            <div class="contact-text">
              <h3>Email</h3>
              <a href="mailto:tuemail@ejemplo.com">tuemail@ejemplo.com</a>
            </div>
          </div>
          
          <div class="contact-item fade-in delay-2">
            <div class="contact-icon">
              <i class="fab fa-github"></i>
            </div>
            <div class="contact-text">
              <h3>GitHub</h3>
              <a href="https://github.com/tuusuario" target="_blank" rel="noopener noreferrer">github.com/tuusuario</a>
            </div>
          </div>
          
          <div class="contact-item fade-in delay-3">
            <div class="contact-icon">
              <i class="fab fa-linkedin"></i>
            </div>
            <div class="contact-text">
              <h3>LinkedIn</h3>
              <a href="https://linkedin.com/in/tuusuario" target="_blank" rel="noopener noreferrer">linkedin.com/in/tuusuario</a>
            </div>
          </div>
        </div>
        
        <div class="contact-form fade-in delay-2">
          <form id="contactForm">
            <div class="form-group">
              <label for="name" class="form-label">Nombre</label>
              <input type="text" id="name" class="form-control" required>
            </div>
            
            <div class="form-group">
              <label for="email" class="form-label">Email</label>
              <input type="email" id="email" class="form-control" required>
            </div>
            
            <div class="form-group">
              <label for="message" class="form-label">Mensaje</label>
              <textarea id="message" class="form-control" required></textarea>
            </div>
            
            <button type="submit" class="submit-btn">
              <i class="fas fa-paper-plane"></i> Enviar Mensaje
            </button>
          </form>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="fade-in">
    <div class="container">
      <div class="social-links">
        <a href="#" class="social-link" aria-label="GitHub"><i class="fab fa-github"></i></a>
        <a href="#" class="social-link" aria-label="LinkedIn"><i class="fab fa-linkedin"></i></a>
        <a href="#" class="social-link" aria-label="Twitter"><i class="fab fa-twitter"></i></a>
        <a href="#" class="social-link" aria-label="Dev.to"><i class="fab fa-dev"></i></a>
      </div>
      <p class="copyright">© <span id="currentYear"></span> Tu Nombre. Todos los derechos reservados.</p>
    </div>
  </footer>

  <script>
    // Función para inicializar el portafolio
    document.addEventListener('DOMContentLoaded', function() {
      // Actualizar año en el footer
      document.getElementById('currentYear').textContent = new Date().getFullYear();
      
      // Menú móvil
      const menuBtn = document.querySelector('.mobile-menu-btn');
      const navLinks = document.querySelector('.nav-links');
      
      menuBtn.addEventListener('click', function() {
        navLinks.classList.toggle('active');
        const icon = this.querySelector('i');
        icon.classList.toggle('fa-bars');
        icon.classList.toggle('fa-times');
      });
      
      // Formulario de contacto
      const contactForm = document.getElementById('contactForm');
      if (contactForm) {
        contactForm.addEventListener('submit', function(e) {
          e.preventDefault();
          
          // Validación simple
          const name = document.getElementById('name').value;
          const email = document.getElementById('email').value;
          const message = document.getElementById('message').value;
          
          if (name && email && message) {
            alert('Mensaje enviado (simulado). ¡Gracias por contactarme!');
            contactForm.reset();
          } else {
            alert('Por favor completa todos los campos');
          }
        });
      }
      
      // Efecto máquina de escribir
      const typewriter = document.querySelector('.typewriter');
      if (typewriter) {
        const text = typewriter.textContent;
        typewriter.textContent = '';
        
        let i = 0;
        function typeWriter() {
          if (i < text.length) {
            typewriter.textContent += text.charAt(i);
            i++;
            setTimeout(typeWriter, Math.random() * 100 + 50);
          }
        }
        
        setTimeout(typeWriter, 1000);
      }
      
      // Observador de intersección para animaciones
      const observerOptions = {
        threshold: 0.1,
        rootMargin: '0px 0px -50px 0px'
      };
      
      const observer = new IntersectionObserver(function(entries) {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.classList.add('animate');
          }
        });
      }, observerOptions);
      
      document.querySelectorAll('.fade-in').forEach(element => {
        observer.observe(element);
      });
    });
  </script>
</body>
</html>

<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Jorge Rossell · Full Stack Developer</title>
  <!-- Google Fonts & Font Awesome -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700;14..32,800&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: linear-gradient(135deg, #0a0f1c 0%, #0e1a2a 100%);
      font-family: 'Inter', sans-serif;
      color: #eef4ff;
      line-height: 1.5;
      padding: 2rem 1rem;
    }

    .container {
      max-width: 1200px;
      margin: 0 auto;
    }

    /* Tarjeta principal con efecto neumórfico oscuro */
    .profile-card {
      background: rgba(18, 25, 40, 0.9);
      backdrop-filter: blur(8px);
      border-radius: 2rem;
      overflow: hidden;
      box-shadow: 0 25px 45px -12px rgba(0, 0, 0, 0.5), 0 0 0 1px rgba(255, 255, 255, 0.05);
      border: 1px solid rgba(255, 255, 255, 0.08);
    }

    /* Header con gradiente tecnológico */
    .hero {
      background: linear-gradient(145deg, #0f212e 0%, #1a3a4f 100%);
      padding: 2.5rem 2rem;
      position: relative;
      border-bottom: 3px solid #f39c12;
    }

    .hero::after {
      content: "<frontend /> <backend />";
      position: absolute;
      bottom: 0.8rem;
      right: 1.5rem;
      font-family: monospace;
      font-size: 0.7rem;
      opacity: 0.4;
      color: #ffd966;
      letter-spacing: 1px;
    }

    .hero-content {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
      gap: 2rem;
    }

    .profile-info h1 {
      font-size: 2.5rem;
      font-weight: 800;
      background: linear-gradient(120deg, #fff, #f5b042);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
      margin-bottom: 0.25rem;
    }

    .badge {
      display: inline-block;
      background: rgba(243, 156, 18, 0.2);
      backdrop-filter: blur(4px);
      padding: 0.3rem 1rem;
      border-radius: 40px;
      font-size: 0.8rem;
      font-weight: 600;
      margin: 0.5rem 0 1rem 0;
      border: 1px solid rgba(243, 156, 18, 0.5);
    }

    .tagline {
      font-size: 1rem;
      opacity: 0.85;
      max-width: 550px;
    }

    .avatar-icon {
      background: #1e4a6e;
      width: 100px;
      height: 100px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 3.2rem;
      box-shadow: 0 10px 25px -5px rgba(0,0,0,0.4);
      border: 2px solid #f39c12;
    }

    /* Secciones */
    .section {
      padding: 2rem 2rem;
      border-bottom: 1px solid rgba(255, 255, 255, 0.08);
    }

    .section:last-child {
      border-bottom: none;
    }

    .section-title {
      display: flex;
      align-items: center;
      gap: 0.7rem;
      font-size: 1.6rem;
      font-weight: 700;
      margin-bottom: 1.5rem;
      color: #f5c97b;
    }

    .section-title i {
      background: #f39c12;
      padding: 0.5rem;
      border-radius: 1rem;
      color: #0a0f1c;
      font-size: 1.2rem;
      width: 2.5rem;
      text-align: center;
    }

    /* Skills grid */
    .skills-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 0.8rem;
      margin-top: 0.5rem;
    }

    .skill-tag {
      background: rgba(30, 50, 70, 0.7);
      padding: 0.5rem 1.1rem;
      border-radius: 40px;
      font-size: 0.85rem;
      font-weight: 500;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      transition: all 0.2s;
      border: 1px solid rgba(243, 156, 18, 0.3);
    }

    .skill-tag i {
      color: #f39c12;
    }

    .skill-tag:hover {
      transform: translateY(-3px);
      background: #f39c12;
      color: #0a0f1c;
      border-color: #fff;
    }
    .skill-tag:hover i {
      color: #0a0f1c;
    }

    /* Tarjetas experiencia / estudios */
    .card-list {
      display: flex;
      flex-direction: column;
      gap: 1.2rem;
    }

    .exp-item, .study-item {
      background: rgba(10, 20, 35, 0.6);
      border-radius: 1.2rem;
      padding: 1.2rem 1.5rem;
      border-left: 4px solid #f39c12;
      transition: 0.2s;
    }

    .exp-item:hover, .study-item:hover {
      background: rgba(30, 55, 80, 0.5);
      transform: translateX(5px);
    }

    .exp-title, .study-title {
      font-size: 1.2rem;
      font-weight: 700;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      margin-bottom: 0.4rem;
    }

    .exp-date, .study-date {
      font-size: 0.8rem;
      color: #f39c12;
    }

    .exp-company, .study-place {
      font-size: 0.85rem;
      opacity: 0.8;
      margin-bottom: 0.6rem;
    }

    /* contacto */
    .contact-links {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      justify-content: center;
      margin-top: 1rem;
    }

    .contact-btn {
      background: #1e2f3a;
      color: white;
      padding: 0.7rem 1.3rem;
      border-radius: 50px;
      text-decoration: none;
      font-weight: 600;
      display: inline-flex;
      align-items: center;
      gap: 0.6rem;
      transition: 0.2s;
      border: 1px solid #2f4b5c;
    }
    .contact-btn i {
      font-size: 1.1rem;
    }
    .contact-btn.github { background: #171515; }
    .contact-btn.email { background: #f39c12; color: #0a0f1c; }
    .contact-btn.phone { background: #2c6e8f; }
    .contact-btn:hover {
      transform: translateY(-3px);
      filter: brightness(1.1);
    }

    footer {
      text-align: center;
      padding: 1.2rem;
      font-size: 0.75rem;
      opacity: 0.7;
      border-top: 1px solid rgba(255,255,255,0.05);
    }

    @media (max-width: 700px) {
      .hero-content { flex-direction: column; text-align: center; }
      .section-title { font-size: 1.3rem; }
      .section { padding: 1.5rem; }
    }
  </style>
</head>
<body>
<div class="container">
  <div class="profile-card">
    <div class="hero">
      <div class="hero-content">
        <div class="profile-info">
          <h1>Jorge Rossell</h1>
          <div class="badge">
            <i class="fas fa-code"></i> Full Stack Developer · Frontend & Backend
          </div>
          <div class="tagline">
            Apasionado por construir soluciones web completas: desde interfaces intuitivas con React, HTML, CSS, 
            hasta backend robusto con Python, JavaScript y bases de datos como MongoDB.
          </div>
        </div>
        <div class="avatar-icon">
          <i class="fas fa-laptop-code"></i>
        </div>
      </div>
    </div>

    <!-- Sobre mí / perfil profesional -->
    <div class="section">
      <div class="section-title">
        <i class="fas fa-user-cog"></i>
        <span>Perfil profesional</span>
      </div>
      <p style="margin-bottom: 1rem;">
        Desarrollador web con formación universitaria y cursos especializados en desarrollo de páginas web, 
        mantenimiento de equipos y redes. Con experiencia laboral en programación de software de ventas 
        y community manager. Me caracterizo por ser <strong>puntual, aprender rápido, trabajar en equipo</strong> 
        y cumplir con los objetivos. Busco crear aplicaciones que conecten el frontend y backend de forma eficiente.
      </p>
      <div style="display: flex; flex-wrap: wrap; gap: 0.8rem; margin-top: 0.8rem;">
        <span><i class="fas fa-birthday-cake"></i> 30/03/2000</span>
        <span><i class="fas fa-id-card"></i> C.I. 30.350.696</span>
        <span><i class="fas fa-heart"></i> Soltero</span>
        <span><i class="fas fa-map-pin"></i> Maracay, Venezuela</span>
      </div>
    </div>

    <!-- Stack Tecnológico: Frontend + Backend (según tu CV) -->
    <div class="section">
      <div class="section-title">
        <i class="fas fa-layer-group"></i>
        <span>Habilidades técnicas full stack</span>
      </div>
      
      <div style="margin-bottom: 1.5rem;">
        <h3 style="margin-bottom: 0.75rem; font-size: 1.1rem;"><i class="fas fa-paint-brush"></i> Frontend</h3>
        <div class="skills-grid">
          <span class="skill-tag"><i class="fab fa-html5"></i> HTML5</span>
          <span class="skill-tag"><i class="fab fa-css3-alt"></i> CSS3</span>
          <span class="skill-tag"><i class="fab fa-js"></i> JavaScript</span>
          <span class="skill-tag"><i class="fab fa-react"></i> React</span>
          <span class="skill-tag"><i class="fas fa-mobile-alt"></i> Responsive Design</span>
          <span class="skill-tag"><i class="fab fa-adobe"></i> Adobe Photoshop</span>
        </div>
      </div>

      <div style="margin-bottom: 1.5rem;">
        <h3 style="margin-bottom: 0.75rem; font-size: 1.1rem;"><i class="fas fa-server"></i> Backend & Bases de datos</h3>
        <div class="skills-grid">
          <span class="skill-tag"><i class="fab fa-python"></i> Python</span>
          <span class="skill-tag"><i class="fas fa-database"></i> MongoDB</span>
          <span class="skill-tag"><i class="fas fa-code"></i> Visual Basic</span>
          <span class="skill-tag"><i class="fas fa-network-wired"></i> Instalación de redes</span>
        </div>
      </div>

      <div>
        <h3 style="margin-bottom: 0.75rem; font-size: 1.1rem;"><i class="fas fa-tools"></i> Otras herramientas</h3>
        <div class="skills-grid">
          <span class="skill-tag"><i class="fas fa-chart-line"></i> Excel avanzado</span>
          <span class="skill-tag"><i class="fas fa-file-word"></i> Word</span>
          <span class="skill-tag"><i class="fas fa-file-powerpoint"></i> PowerPoint</span>
          <span class="skill-tag"><i class="fas fa-laptop"></i> Mantenimiento PC</span>
        </div>
      </div>
    </div>

    <!-- Estudios realizados (de tu CV) -->
    <div class="section">
      <div class="section-title">
        <i class="fas fa-graduation-cap"></i>
        <span>Formación académica</span>
      </div>
      <div class="card-list">
        <div class="study-item">
          <div class="study-title">
            <span>📘 Instituto Universitario de Tecnología Juan Pablo Pérez Alfonso</span>
            <span class="study-date">Título Universitario</span>
          </div>
          <div class="study-place">Maracay, Estado Carabobo</div>
          <div>Educación superior completa.</div>
        </div>
        <div class="study-item">
          <div class="study-title">
            <span>🎓 Unidad Educativa Colegio Milagro de María</span>
            <span class="study-date">Bachiller</span>
          </div>
          <div class="study-place">Sector 19 Abril, Maracay - Carabobo</div>
          <div>Graduado de Bachiller (4to y 5to año).</div>
        </div>
        <div class="study-item">
          <div class="study-title">
            <span>📖 Educación Primaria y Media</span>
          </div>
          <div class="study-place">Colegio Jesús Rosas Marcano · U.E. Guedez Toro · U.E. Madre de la Candelaria</div>
          <div>Desde inicial hasta 3er año de media completa.</div>
        </div>
      </div>
    </div>

    <!-- Cursos realizados -->
    <div class="section">
      <div class="section-title">
        <i class="fas fa-certificate"></i>
        <span>Cursos especializados</span>
      </div>
      <div class="skills-grid">
        <span class="skill-tag"><i class="fas fa-desktop"></i> Mantenimiento y reparación de PC</span>
        <span class="skill-tag"><i class="fab fa-html5"></i> Desarrollo de páginas web</span>
        <span class="skill-tag"><i class="fas fa-network-wired"></i> Instalación de redes</span>
      </div>
      <p style="margin-top: 0.8rem; font-size: 0.85rem;">Centro de Formación Maracay · Certificaciones prácticas</p>
    </div>

    <!-- Experiencia laboral -->
    <div class="section">
      <div class="section-title">
        <i class="fas fa-briefcase"></i>
        <span>Experiencia profesional</span>
      </div>
      <div class="card-list">
        <div class="exp-item">
          <div class="exp-title">
            <span>💻 Programador de Software de Ventas (Pasantías)</span>
          </div>
          <div class="exp-company">Plastiproductos Pincord C.A · Maracay, Carabobo</div>
          <div>Desarrollo e implementación de software de ventas, apoyo en el área de sistemas y lógica de inventarios.</div>
        </div>
        <div class="exp-item">
          <div class="exp-title">
            <span>📱 Community Manager</span>
          </div>
          <div class="exp-company">Ferretería y Transporte Aragua</div>
          <div>Gestión de redes sociales, contenido digital y atención al cliente online.</div>
        </div>
      </div>
    </div>

    <!-- Habilidades blandas + destrezas -->
    <div class="section">
      <div class="section-title">
        <i class="fas fa-hand-peace"></i>
        <span>Habilidades y destrezas</span>
      </div>
      <div class="skills-grid">
        <span class="skill-tag"><i class="fas fa-users"></i> Trabajo en equipo</span>
        <span class="skill-tag"><i class="fas fa-clock"></i> Puntualidad</span>
        <span class="skill-tag"><i class="fas fa-chart-line"></i> Cumplir expectativas</span>
        <span class="skill-tag"><i class="fas fa-rocket"></i> Aprendizaje rápido</span>
        <span class="skill-tag"><i class="fas fa-calendar-check"></i> Constancia laboral</span>
        <span class="skill-tag"><i class="fas fa-lightbulb"></i> Aportar ideas</span>
        <span class="skill-tag"><i class="fas fa-check-circle"></i> Cumplimiento de normas</span>
        <span class="skill-tag"><i class="fas fa-database"></i> Desarrollo de inventarios (VB)</span>
      </div>
    </div>

    <!-- Contacto y redes (adaptado a tus datos) -->
    <div class="section">
      <div class="section-title">
        <i class="fas fa-address-card"></i>
        <span>Contacto profesional</span>
      </div>
      <div class="contact-links">
        <a href="mailto:30350696@example.com" class="contact-btn email"><i class="fas fa-envelope"></i> 30350696</a>
        <a href="tel:+58412740194" class="contact-btn phone"><i class="fas fa-phone-alt"></i> 0412-740194</a>
        <a href="#" class="contact-btn github"><i class="fab fa-github"></i> /JorgeRossellDev</a>
        <a href="#" class="contact-btn" style="background:#0a66c2;"><i class="fab fa-linkedin"></i> LinkedIn</a>
      </div>
      <p style="text-align: center; margin-top: 1.2rem; font-size: 0.8rem;">
        <i class="fas fa-map-marker-alt"></i> Dirección: Jorge Rossell Pestano, Maracay · 
        <i class="fas fa-calendar-alt"></i> Nacimiento: 30 marzo 2000
      </p>
      <div style="background: rgba(0,0,0,0.2); border-radius: 1rem; padding: 0.8rem; margin-top: 1rem; text-align: center;">
        <i class="fas fa-users"></i> <strong>Referencias:</strong> Jorge Hernan Rossell Hernández (0412-8950330) · Julia Pestano (0424-4296156)
      </div>
    </div>

    <footer>
      <i class="far fa-copyright"></i> 2025 Jorge Rossell — Full Stack Developer · Perfil diseñado para GitHub | HTML + CSS + JS
    </footer>
  </div>
</div>
</body>
</html>

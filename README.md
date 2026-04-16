<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Jorge Rossell · Full Stack Developer · GitHub Profile</title>
  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700;14..32,800&display=swap" rel="stylesheet">
  <!-- Font Awesome 6 -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: linear-gradient(135deg, #0d1117 0%, #0a0f1a 100%);
      font-family: 'Inter', sans-serif;
      color: #e6edf3;
      padding: 2rem 1.5rem;
    }

    .container {
      max-width: 1100px;
      margin: 0 auto;
    }

    /* Tarjeta principal estilo GitHub README premium */
    .profile-card {
      background: #161b22;
      border-radius: 24px;
      border: 1px solid #30363d;
      overflow: hidden;
      box-shadow: 0 8px 24px rgba(0,0,0,0.4);
    }

    /* Banner / Header con imagen de portada */
    .cover {
      background: linear-gradient(110deg, #0d2b3e 0%, #1a4a6e 100%);
      padding: 2rem 2rem 1.5rem 2rem;
      position: relative;
    }

    .avatar-section {
      display: flex;
      align-items: center;
      gap: 1.5rem;
      flex-wrap: wrap;
    }

    .avatar {
      width: 100px;
      height: 100px;
      background: linear-gradient(145deg, #f39c12, #e67e22);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 3rem;
      border: 3px solid #fff;
      box-shadow: 0 8px 20px rgba(0,0,0,0.3);
    }

    .avatar i {
      color: #1a1f2e;
    }

    .info h1 {
      font-size: 2rem;
      font-weight: 800;
      background: linear-gradient(120deg, #fff, #f5b042);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
    }

    .bio {
      margin-top: 0.5rem;
      opacity: 0.9;
      font-size: 0.95rem;
      max-width: 500px;
    }

    /* Badges principales */
    .badges-row {
      display: flex;
      flex-wrap: wrap;
      gap: 0.6rem;
      margin: 1rem 0 0.5rem 0;
    }

    .badge {
      background: #21262d;
      padding: 0.25rem 0.8rem;
      border-radius: 40px;
      font-size: 0.75rem;
      font-weight: 500;
      display: inline-flex;
      align-items: center;
      gap: 6px;
      border: 1px solid #30363d;
    }

    .badge i {
      color: #f39c12;
    }

    /* Stats row */
    .stats-row {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      justify-content: space-between;
      background: #0d1117;
      padding: 1rem 2rem;
      border-bottom: 1px solid #21262d;
    }

    .stat-item {
      display: flex;
      align-items: center;
      gap: 0.5rem;
      font-size: 0.85rem;
    }

    .stat-number {
      font-weight: 800;
      font-size: 1.1rem;
      color: #f39c12;
    }

    /* Secciones */
    .section {
      padding: 1.5rem 2rem;
      border-bottom: 1px solid #21262d;
    }

    .section-title {
      font-size: 1.3rem;
      font-weight: 700;
      margin-bottom: 1rem;
      display: flex;
      align-items: center;
      gap: 0.6rem;
      color: #f0f6fc;
    }

    .section-title i {
      color: #f39c12;
    }

    /* Skills grid con badges tipo GitHub */
    .skills-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 0.6rem;
    }

    .skill-badge {
      background: #21262d;
      padding: 0.35rem 1rem;
      border-radius: 30px;
      font-size: 0.8rem;
      font-weight: 500;
      border: 1px solid #30363d;
      transition: 0.2s;
    }

    .skill-badge i {
      margin-right: 5px;
      color: #f39c12;
    }

    .skill-badge:hover {
      transform: translateY(-2px);
      border-color: #f39c12;
    }

    /* Cards de experiencia y estudios */
    .card-list {
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }

    .card-item {
      background: #0d1117;
      border-radius: 16px;
      padding: 1rem 1.2rem;
      border-left: 4px solid #f39c12;
      transition: 0.2s;
    }

    .card-item:hover {
      background: #161b22;
      transform: translateX(5px);
    }

    .card-title {
      font-weight: 700;
      font-size: 1rem;
      margin-bottom: 0.2rem;
    }

    .card-sub {
      font-size: 0.75rem;
      color: #8b949e;
      margin-bottom: 0.5rem;
    }

    /* Botones sociales */
    .social-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      margin-top: 1rem;
      justify-content: center;
    }

    .btn {
      padding: 0.6rem 1.3rem;
      border-radius: 40px;
      text-decoration: none;
      font-weight: 600;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      transition: 0.2s;
      background: #21262d;
      color: white;
      border: 1px solid #30363d;
    }

    .btn i {
      font-size: 1.1rem;
    }

    .btn.github { background: #171515; }
    .btn.email { background: #d97706; border-color: #f39c12; }
    .btn.linkedin { background: #0a66c2; }
    .btn.twitter { background: #1da1f2; }
    .btn:hover {
      transform: translateY(-3px);
      filter: brightness(1.05);
    }

    footer {
      text-align: center;
      padding: 1rem;
      font-size: 0.7rem;
      border-top: 1px solid #21262d;
      color: #8b949e;
    }

    @media (max-width: 700px) {
      .avatar-section { flex-direction: column; text-align: center; }
      .section { padding: 1.2rem; }
      .stats-row { flex-direction: column; gap: 0.5rem; }
    }
  </style>
</head>
<body>
<div class="container">
  <div class="profile-card">
    <!-- Cover con avatar -->
    <div class="cover">
      <div class="avatar-section">
        <div class="avatar">
          <i class="fas fa-laptop-code"></i>
        </div>
        <div class="info">
          <h1>Jorge Rossell <span style="font-size: 1rem;">🚀</span></h1>
          <div class="bio">
            <i class="fas fa-map-pin"></i> Maracay, Venezuela · 
            <i class="fas fa-calendar-alt"></i> 30/03/2000
          </div>
          <div class="badges-row">
            <span class="badge"><i class="fas fa-code"></i> Full Stack Developer</span>
            <span class="badge"><i class="fas fa-laptop"></i> Frontend + Backend</span>
            <span class="badge"><i class="fas fa-database"></i> React · Python · MongoDB</span>
          </div>
        </div>
      </div>
    </div>

    <!-- Stats rápidos -->
    <div class="stats-row">
      <div class="stat-item"><i class="fab fa-github"></i> <span class="stat-number">15+</span> repositorios</div>
      <div class="stat-item"><i class="fas fa-code-branch"></i> <span class="stat-number">7+</span> proyectos full stack</div>
      <div class="stat-item"><i class="fas fa-certificate"></i> <span class="stat-number">3</span> certificaciones técnicas</div>
      <div class="stat-item"><i class="fas fa-briefcase"></i> <span class="stat-number">2</span> años experiencia</div>
    </div>

    <!-- Sobre mí -->
    <div class="section">
      <div class="section-title">
        <i class="fas fa-user-astronaut"></i> Sobre mí
      </div>
      <p>👋 ¡Hola! Soy Jorge, desarrollador full stack apasionado por crear soluciones web completas. Disfruto tanto el diseño de interfaces con <strong>HTML, CSS, JS y React</strong> como la lógica del backend con <strong>Python, MongoDB y Visual Basic</strong>. He desarrollado software de ventas, trabajado como community manager y siempre estoy aprendiendo nuevas tecnologías.</p>
    </div>

    <!-- Stack tecnológico completo (frontend + backend) -->
    <div class="section">
      <div class="section-title">
        <i class="fas fa-layer-group"></i> Tech Stack
      </div>
      <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 1rem;">
        <div>
          <h3 style="font-size: 0.9rem; margin-bottom: 0.5rem;"><i class="fas fa-paint-brush"></i> Frontend</h3>
          <div class="skills-grid">
            <span class="skill-badge"><i class="fab fa-html5"></i> HTML5</span>
            <span class="skill-badge"><i class="fab fa-css3-alt"></i> CSS3</span>
            <span class="skill-badge"><i class="fab fa-js"></i> JavaScript</span>
            <span class="skill-badge"><i class="fab fa-react"></i> React</span>
            <span class="skill-badge"><i class="fas fa-mobile-alt"></i> Responsive Design</span>
          </div>
        </div>
        <div>
          <h3 style="font-size: 0.9rem; margin-bottom: 0.5rem;"><i class="fas fa-server"></i> Backend & DB</h3>
          <div class="skills-grid">
            <span class="skill-badge"><i class="fab fa-python"></i> Python</span>
            <span class="skill-badge"><i class="fas fa-database"></i> MongoDB</span>
            <span class="skill-badge"><i class="fas fa-code"></i> Visual Basic</span>
            <span class="skill-badge"><i class="fas fa-network-wired"></i> Redes</span>
          </div>
        </div>
      </div>
      <div style="margin-top: 1rem;">
        <h3 style="font-size: 0.9rem; margin-bottom: 0.5rem;"><i class="fas fa-tools"></i> Herramientas</h3>
        <div class="skills-grid">
          <span class="skill-badge"><i class="fas fa-chart-line"></i> Excel avanzado</span>
          <span class="skill-badge"><i class="fas fa-file-word"></i> Word / PowerPoint</span>
          <span class="skill-badge"><i class="fas fa-laptop"></i> Mantenimiento PC</span>
          <span class="skill-badge"><i class="fas fa-adobe"></i> Photoshop</span>
        </div>
      </div>
    </div>

    <!-- Formación + Cursos -->
    <div class="section">
      <div class="section-title">
        <i class="fas fa-graduation-cap"></i> Educación & Cursos
      </div>
      <div class="card-list">
        <div class="card-item">
          <div class="card-title">📘 Instituto Universitario Juan Pablo Pérez Alfonso</div>
          <div class="card-sub">Título Universitario · Maracay</div>
        </div>
        <div class="card-item">
          <div class="card-title">🎓 U.E. Colegio Milagro de María</div>
          <div class="card-sub">Bachiller · 4to y 5to año</div>
        </div>
        <div class="card-item">
          <div class="card-title">💻 Centro de Formación Maracay</div>
          <div class="card-sub">Mantenimiento PC · Desarrollo Web · Instalación de redes</div>
        </div>
      </div>
    </div>

    <!-- Experiencia laboral -->
    <div class="section">
      <div class="section-title">
        <i class="fas fa-briefcase"></i> Experiencia profesional
      </div>
      <div class="card-list">
        <div class="card-item">
          <div class="card-title">💼 Programador de Software de Ventas (Pasantías)</div>
          <div class="card-sub">Plastiproductos Pincord C.A · Maracay</div>
          <div class="card-sub" style="color:#c9d1d9;">Desarrollo e implementación de software de ventas, lógica de inventarios y soporte técnico.</div>
        </div>
        <div class="card-item">
          <div class="card-title">📱 Community Manager</div>
          <div class="card-sub">Ferretería y Transporte Aragua</div>
          <div class="card-sub" style="color:#c9d1d9;">Gestión de redes sociales, contenido digital y atención al cliente.</div>
        </div>
      </div>
    </div>

    <!-- Habilidades blandas -->
    <div class="section">
      <div class="section-title">
        <i class="fas fa-hand-peace"></i> Soft Skills
      </div>
      <div class="skills-grid">
        <span class="skill-badge">🤝 Trabajo en equipo</span>
        <span class="skill-badge">⏱️ Puntualidad</span>
        <span class="skill-badge">📈 Cumplir metas</span>
        <span class="skill-badge">⚡ Aprendizaje rápido</span>
        <span class="skill-badge">💡 Aportar ideas</span>
        <span class="skill-badge">📋 Cumplimiento de normas</span>
      </div>
    </div>

    <!-- Proyectos destacados (ejemplo) -->
    <div class="section">
      <div class="section-title">
        <i class="fas fa-star"></i> Proyectos destacados
      </div>
      <div class="card-list">
        <div class="card-item">
          <div class="card-title"><i class="fab fa-github"></i> Sistema de Ventas Web</div>
          <div class="card-sub">HTML, CSS, JS, Python, MongoDB</div>
          <div class="card-sub" style="color:#c9d1d9;">Aplicación completa para gestión de ventas e inventarios.</div>
        </div>
        <div class="card-item">
          <div class="card-title"><i class="fas fa-globe"></i> Portafolio Full Stack</div>
          <div class="card-sub">React + Node.js (en desarrollo)</div>
          <div class="card-sub" style="color:#c9d1d9;">Mi portafolio personal con integración de proyectos.</div>
        </div>
      </div>
    </div>

    <!-- Botones sociales y contacto -->
    <div class="section">
      <div class="section-title">
        <i class="fas fa-link"></i> Conecta conmigo
      </div>
      <div class="social-buttons">
        <a href="#" class="btn github"><i class="fab fa-github"></i> GitHub /JorgeRossellDev</a>
        <a href="mailto:jorgerosellpestano18@gmail.com" class="btn email"><i class="fas fa-envelope"></i> Email</a>
        <a href="#" class="btn linkedin"><i class="fab fa-linkedin-in"></i> LinkedIn</a>
        <a href="#" class="btn twitter"><i class="fab fa-twitter"></i> Twitter</a>
      </div>
      <div style="text-align: center; margin-top: 1rem;">
        <i class="fas fa-phone-alt"></i> +58 412-740194 &nbsp;|&nbsp;
        <i class="fas fa-id-card"></i> C.I. 30.350.696
      </div>
    </div>

    <!-- Referencias -->
    <div class="section">
      <div class="section-title">
        <i class="fas fa-address-book"></i> Referencias
      </div>
      <div style="display: flex; gap: 1rem; flex-wrap: wrap;">
        <div style="background:#0d1117; padding: 0.6rem 1rem; border-radius: 16px;">
          <i class="fas fa-user"></i> <strong>Jorge Hernan Rossell H.</strong><br>
          📞 0412-8950330
        </div>
        <div style="background:#0d1117; padding: 0.6rem 1rem; border-radius: 16px;">
          <i class="fas fa-user"></i> <strong>Julia Pestano R.</strong><br>
          📞 0424-4296156
        </div>
      </div>
    </div>

    <footer>
      <i class="far fa-copyright"></i> 2025 Jorge Rossell · Full Stack Developer · Perfil optimizado para GitHub
      <div style="margin-top: 4px;">
        <i class="fas fa-code"></i> HTML · CSS · JS | Siempre construyendo soluciones
      </div>
    </footer>
  </div>
</div>
</body>
</html>
      <i class="far fa-copyright"></i> 2025 Jorge Rossell — Full Stack Developer · Perfil diseñado para GitHub | HTML + CSS + JS
    </footer>
  </div>
</div>
</body>
</html>

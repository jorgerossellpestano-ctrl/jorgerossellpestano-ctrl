<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Jorge Rossell · Desarrollador Full Stack</title>
  <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #f0f2f5;
      font-family: 'Plus Jakarta Sans', sans-serif;
      color: #1a2c3e;
      line-height: 1.5;
      padding: 2rem;
    }

    .container {
      max-width: 1100px;
      margin: 0 auto;
    }

    /* Tarjeta principal estilo CV moderno */
    .profile-card {
      background: white;
      border-radius: 28px;
      box-shadow: 0 20px 35px -12px rgba(0,0,0,0.1);
      overflow: hidden;
      transition: all 0.2s;
    }

    /* Cabecera profesional */
    .header {
      background: linear-gradient(110deg, #0b2b3b 0%, #1a4a6e 100%);
      padding: 2.5rem 2rem;
      color: white;
    }

    .name {
      font-size: 2.8rem;
      font-weight: 800;
      letter-spacing: -0.02em;
      margin-bottom: 0.25rem;
    }

    .badge {
      display: inline-block;
      background: rgba(255,255,240,0.15);
      padding: 0.25rem 1rem;
      border-radius: 40px;
      font-size: 0.85rem;
      font-weight: 600;
      margin: 0.75rem 0 1rem 0;
      border: 1px solid rgba(255,200,100,0.4);
    }

    .contact-row {
      display: flex;
      flex-wrap: wrap;
      gap: 1.2rem;
      margin-top: 1rem;
      font-size: 0.85rem;
    }

    .contact-row i {
      width: 1.2rem;
      color: #f5b642;
    }

    /* Secciones */
    .section {
      padding: 1.8rem 2rem;
      border-bottom: 1px solid #e9eef2;
    }

    .section:last-child {
      border-bottom: none;
    }

    .section-title {
      font-size: 1.4rem;
      font-weight: 700;
      margin-bottom: 1.2rem;
      display: flex;
      align-items: center;
      gap: 0.6rem;
      color: #0f3b4f;
    }

    .section-title i {
      color: #f39c12;
      font-size: 1.3rem;
    }

    /* Grid de skills */
    .skills-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 0.7rem;
    }

    .skill {
      background: #eef3fa;
      padding: 0.4rem 1rem;
      border-radius: 30px;
      font-size: 0.85rem;
      font-weight: 500;
    }

    .skill i {
      margin-right: 6px;
      color: #e67e22;
    }

    /* Listas de estudios / experiencia */
    .list-item {
      margin-bottom: 1.2rem;
      padding-left: 0.5rem;
      border-left: 3px solid #f39c12;
    }

    .item-title {
      font-weight: 700;
      font-size: 1rem;
      margin-bottom: 0.2rem;
    }

    .item-sub {
      font-size: 0.85rem;
      color: #5f7f8c;
      margin-bottom: 0.3rem;
    }

    .item-desc {
      font-size: 0.9rem;
      color: #2c3e46;
    }

    .two-columns {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 1.5rem;
    }

    @media (max-width: 700px) {
      .two-columns { grid-template-columns: 1fr; }
      .name { font-size: 2rem; }
      body { padding: 1rem; }
    }

    .ref {
      background: #f9fafc;
      padding: 0.8rem;
      border-radius: 1rem;
      margin-top: 0.5rem;
    }
  </style>
</head>
<body>
<div class="container">
  <div class="profile-card">
    <!-- Encabezado -->
    <div class="header">
      <div class="name">Jorge Rossell</div>
      <div class="badge">
        <i class="fas fa-code"></i> Full Stack Developer · Frontend + Backend
      </div>
      <div class="contact-row">
        <span><i class="fas fa-phone-alt"></i> +58 412-740194</span>
        <span><i class="fas fa-envelope"></i> jorgerosellpestano18@gmail.com</span>
        <span><i class="fas fa-map-marker-alt"></i> Maracay, Venezuela</span>
        <span><i class="fas fa-calendar-alt"></i> 30/03/2000</span>
      </div>
    </div>

    <!-- Perfil / Sobre mí -->
    <div class="section">
      <div class="section-title">
        <i class="fas fa-user-astronaut"></i> Perfil profesional
      </div>
      <p style="margin-bottom: 0.5rem;">
        Desarrollador web con formación universitaria y cursos especializados en <strong>HTML, CSS, JavaScript, Python y React</strong>. 
        Experiencia en desarrollo de software de ventas, community manager y mantenimiento de equipos. 
        Persona puntual, con capacidad de aprendizaje rápido, trabajo en equipo y enfoque en resultados.
      </p>
    </div>

    <!-- Stack técnico dividido en front y back -->
    <div class="section">
      <div class="section-title">
        <i class="fas fa-layer-group"></i> Stack tecnológico
      </div>
      <div class="two-columns">
        <div>
          <h3 style="margin-bottom: 0.6rem; font-size: 1rem;"><i class="fas fa-paint-brush"></i> Frontend</h3>
          <div class="skills-grid">
            <span class="skill"><i class="fab fa-html5"></i> HTML5</span>
            <span class="skill"><i class="fab fa-css3-alt"></i> CSS3</span>
            <span class="skill"><i class="fab fa-js"></i> JavaScript</span>
            <span class="skill"><i class="fab fa-react"></i> React</span>
            <span class="skill"><i class="fas fa-mobile-alt"></i> Responsive</span>
          </div>
        </div>
        <div>
          <h3 style="margin-bottom: 0.6rem; font-size: 1rem;"><i class="fas fa-server"></i> Backend & DB</h3>
          <div class="skills-grid">
            <span class="skill"><i class="fab fa-python"></i> Python</span>
            <span class="skill"><i class="fas fa-database"></i> MongoDB</span>
            <span class="skill"><i class="fas fa-code"></i> Visual Basic</span>
            <span class="skill"><i class="fas fa-network-wired"></i> Redes</span>
          </div>
        </div>
      </div>
      <div style="margin-top: 1rem;">
        <h3 style="margin-bottom: 0.5rem; font-size: 1rem;"><i class="fas fa-tools"></i> Otras herramientas</h3>
        <div class="skills-grid">
          <span class="skill"><i class="fas fa-chart-line"></i> Excel (avanzado)</span>
          <span class="skill"><i class="fas fa-file-alt"></i> Word / PPT</span>
          <span class="skill"><i class="fas fa-laptop"></i> Mantenimiento PC</span>
          <span class="skill"><i class="fas fa-adobe"></i> Photoshop</span>
        </div>
      </div>
    </div>

    <!-- Formación académica -->
    <div class="section">
      <div class="section-title">
        <i class="fas fa-graduation-cap"></i> Educación
      </div>
      <div class="list-item">
        <div class="item-title">Instituto Universitario Juan Pablo Pérez Alfonso</div>
        <div class="item-sub">Título Universitario · Maracay</div>
      </div>
      <div class="list-item">
        <div class="item-title">U.E. Colegio Milagro de María</div>
        <div class="item-sub">Bachiller · 4to y 5to año</div>
      </div>
      <div class="list-item">
        <div class="item-title">Educación Primaria y Media</div>
        <div class="item-sub">Colegio Jesús Rosas Marcano · U.E. Guedez Toro · U.E. Madre de la Candelaria</div>
      </div>
    </div>

    <!-- Cursos -->
    <div class="section">
      <div class="section-title">
        <i class="fas fa-certificate"></i> Cursos especializados
      </div>
      <div class="skills-grid">
        <span class="skill"><i class="fas fa-desktop"></i> Mantenimiento y reparación de PC</span>
        <span class="skill"><i class="fab fa-html5"></i> Desarrollo de páginas web</span>
        <span class="skill"><i class="fas fa-network-wired"></i> Instalación de redes</span>
      </div>
      <div class="item-sub" style="margin-top: 0.5rem;">Centro de Formación Maracay</div>
    </div>

    <!-- Experiencia laboral -->
    <div class="section">
      <div class="section-title">
        <i class="fas fa-briefcase"></i> Experiencia profesional
      </div>
      <div class="list-item">
        <div class="item-title">Programador de Software de Ventas (Pasantías)</div>
        <div class="item-sub">Plastiproductos Pincord C.A · Maracay</div>
        <div class="item-desc">Desarrollo e implementación de software de ventas, lógica de inventarios y soporte técnico.</div>
      </div>
      <div class="list-item">
        <div class="item-title">Community Manager</div>
        <div class="item-sub">Ferretería y Transporte Aragua</div>
        <div class="item-desc">Gestión de redes sociales, contenido digital y atención al cliente.</div>
      </div>
    </div>

    <!-- Habilidades blandas -->
    <div class="section">
      <div class="section-title">
        <i class="fas fa-hand-peace"></i> Habilidades personales
      </div>
      <div class="skills-grid">
        <span class="skill">🤝 Trabajo en equipo</span>
        <span class="skill">⏱️ Puntualidad</span>
        <span class="skill">📈 Cumplir metas</span>
        <span class="skill">⚡ Aprendizaje rápido</span>
        <span class="skill">💡 Aportar ideas</span>
        <span class="skill">📋 Cumplimiento de normas</span>
      </div>
    </div>

    <!-- Referencias -->
    <div class="section">
      <div class="section-title">
        <i class="fas fa-address-book"></i> Referencias
      </div>
      <div class="two-columns">
        <div class="ref">
          <i class="fas fa-user"></i> <strong>Jorge Hernan Rossell H.</strong><br>
          📞 0412-8950330
        </div>
        <div class="ref">
          <i class="fas fa-user"></i> <strong>Julia de la C. Pestano R.</strong><br>
          📞 0424-4296156
        </div>
      </div>
    </div>

    <!-- GitHub / enlace profesional -->
    <div style="background: #f8fafc; padding: 1.2rem 2rem; text-align: center; border-top: 1px solid #e2edf2;">
      <i class="fab fa-github"></i> <strong>GitHub:</strong> /JorgeRossellDev 
      &nbsp;|&nbsp; <i class="fas fa-envelope"></i> jorgerosellpestano18@gmail.com
      <div style="font-size: 0.75rem; margin-top: 0.5rem;">Disponible para colaboraciones full stack · HTML, CSS, JS, Python, React, MongoDB</div>
    </div>
  </div>
</div>
</body>
</html>
    <footer>
      <i class="far fa-copyright"></i> 2025 Jorge Rossell — Full Stack Developer · Perfil diseñado para GitHub | HTML + CSS + JS
    </footer>
  </div>
</div>
</body>
</html>

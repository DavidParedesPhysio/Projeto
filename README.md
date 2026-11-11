<!DOCTYPE html>
<html lang="pt">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>David Paredes | Fisioterapeuta Desportivo</title>
  
  <style>
    /* Variáveis Globais & Paleta Editorial Clínico */
    :root {
      --bg-dark: #121412;
      --card-bg: rgba(255, 255, 255, 0.03);
      --card-bg-hover: rgba(255, 255, 255, 0.06);
      --text-main: #e2e8f0;
      --text-muted: #9ca3af;
      --accent-gold: #c5a059;
      --border-color: rgba(197, 160, 89, 0.25);
      --font-stack: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: var(--font-stack);
      background-color: var(--bg-dark);
      color: var(--text-main);
      line-height: 1.6;
    }

    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
    }

    /* Cabeçalho / Hero Section */
    header {
      padding: 60px 0 40px 0;
      border-bottom: 1px solid var(--border-color);
      text-align: center;
    }

    .brand-name {
      font-size: 2.8rem;
      font-weight: 700;
      letter-spacing: 2px;
      color: #ffffff;
      text-transform: uppercase;
    }

    .brand-title {
      font-size: 1.2rem;
      color: var(--accent-gold);
      letter-spacing: 3px;
      text-transform: uppercase;
      margin-top: 8px;
    }

    /* Secção Sobre Mim / About Me */
    .about-section {
      padding: 80px 0;
      border-bottom: 1px solid var(--border-color);
    }

    .about-container {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 48px;
      align-items: center;
    }

    .about-image {
      width: 100%;
      border-radius: 8px;
      overflow: hidden;
      box-shadow: 0 12px 32px rgba(0, 0, 0, 0.5);
      border: 1px solid var(--border-color);
      background-color: #1a1c1a;
      min-height: 250px;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .about-image img {
      width: 100%;
      height: auto;
      display: block;
      object-fit: cover;
    }

    /* Alternador de Idioma (PT | EN) */
    .lang-switch {
      display: flex;
      align-items: center;
      gap: 8px;
      margin-bottom: 24px;
    }

    .lang-btn {
      background: none;
      border: none;
      color: var(--text-muted);
      font-weight: 600;
      font-size: 0.95rem;
      cursor: pointer;
      padding: 4px 8px;
      transition: color 0.3s ease;
      letter-spacing: 1px;
    }

    .lang-btn.active {
      color: var(--accent-gold);
      border-bottom: 2px solid var(--accent-gold);
    }

    .lang-divider {
      color: #4a5568;
    }

    /* Gestão de Visibilidade do Idioma - Corrigida */
    .lang-content {
      display: none;
    }

    .lang-content.active {
      display: block;
    }

    .section-title {
      font-size: 2.2rem;
      color: #ffffff;
      margin-bottom: 20px;
      font-weight: 700;
    }

    .lead-text {
      font-size: 1.15rem;
      line-height: 1.6;
      color: #e5e7eb;
      margin-bottom: 16px;
    }

    .body-text {
      font-size: 0.98rem;
      line-height: 1.65;
      color: var(--text-muted);
      margin-bottom: 28px;
    }

    .credentials-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 16px;
    }

    .credential-card {
      background: var(--card-bg);
      border-left: 3px solid var(--accent-gold);
      padding: 16px 20px;
      border-radius: 4px;
    }

    .credential-card h3 {
      font-size: 1.05rem;
      color: #ffffff;
      margin-bottom: 8px;
    }

    .credential-card p {
      font-size: 0.88rem;
      color: var(--text-muted);
      line-height: 1.45;
    }

    /* Secção de Serviços e Preços */
    .services-section {
      padding: 80px 0;
    }

    .services-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 24px;
      margin-top: 40px;
    }

    .service-card {
      background: var(--card-bg);
      border: 1px solid var(--border-color);
      border-radius: 8px;
      padding: 32px 24px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      transition: background 0.3s ease;
    }

    .service-card:hover {
      background: var(--card-bg-hover);
    }

    .service-card h3 {
      font-size: 1.3rem;
      color: #ffffff;
      margin-bottom: 12px;
    }

    .service-price {
      font-size: 2rem;
      font-weight: 700;
      color: var(--accent-gold);
      margin-bottom: 16px;
    }

    .service-price span {
      font-size: 0.9rem;
      color: var(--text-muted);
      font-weight: 400;
    }

    .service-desc {
      font-size: 0.95rem;
      color: var(--text-muted);
      margin-bottom: 24px;
    }

    .btn-contact {
      display: inline-block;
      text-align: center;
      background: transparent;
      color: var(--accent-gold);
      border: 1px solid var(--accent-gold);
      padding: 12px 20px;
      border-radius: 4px;
      text-decoration: none;
      font-weight: 600;
      transition: all 0.3s ease;
    }

    .btn-contact:hover {
      background: var(--accent-gold);
      color: var(--bg-dark);
    }

    /* Rodapé */
    footer {
      padding: 40px 0;
      text-align: center;
      border-top: 1px solid var(--border-color);
      color: var(--text-muted);
      font-size: 0.9rem;
    }

    /* Responsivo */
    @media (max-width: 900px) {
      .about-container {
        grid-template-columns: 1fr;
        gap: 32px;
      }
      .services-grid {
        grid-template-columns: 1fr;
      }
      .credentials-grid {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>

  <!-- Cabeçalho -->
  <header>
    <div class="container">
      <h1 class="brand-name">David Paredes</h1>
      <div class="brand-title">Fisioterapeuta Desportivo</div>
    </div>
  </header>

  <!-- Secção Sobre Mim / About Me -->
  <section id="about" class="about-section">
    <div class="container about-container">
      
      <!-- Imagem Editorial -->
      <div class="about-image">
        <img src="placa-bronze-david-paredes.jpg" alt="David Paredes - Fisioterapeuta Desportivo" onerror="this.style.display='none'" />
      </div>

      <!-- Conteúdo Bilingue -->
      <div class="about-content">
        
        <!-- Alternador PT | EN -->
        <div class="lang-switch">
          <button id="btn-pt" class="lang-btn active" type="button" onclick="switchLang('pt')">PT</button>
          <span class="lang-divider">|</span>
          <button id="btn-en" class="lang-btn" type="button" onclick="switchLang('en')">EN</button>
        </div>

        <!-- Conteúdo em Português -->
        <div id="content-pt" class="lang-content active">
          <h2 class="section-title">Sobre Mim</h2>
          <p class="lead-text">
            Fisioterapeuta Desportivo com mais de 4 anos de experiência clínica e no desporto de alta performance, a atuar na área da Grande Lisboa e disponível para projetos internacionais.
          </p>
          <p class="body-text">
            Atualmente, exerço funções como Fisioterapeuta e Coordenador de Turno Clínico na <strong>Fisiogaspar</strong>, onde lidero uma equipa multidisciplinar e acompanho diretamente patologias musculoesqueléticas, pós-operatórios e processos de <em>return-to-sport</em>.
          </p>
          
          <div class="credentials-grid">
            <div class="credential-card">
              <h3>Padel de Elite</h3>
              <p>Fisioterapeuta Oficial da <strong>Seleção Nacional de Padel Veteranos</strong>, acompanhando a equipa em competições mundiais desde 2023, bem como em torneios internacionais do circuito WPT e FIP Platinum.</p>
            </div>
            <div class="credential-card">
              <h3>Escalada de Competição</h3>
              <p>Colaborador da Equipa Médica da <strong>Seleção Nacional de Escalada de Competição (FPME)</strong>, prestando suporte especializado em fisioterapia desportiva num contexto multidisciplinar.</p>
            </div>
          </div>
        </div>

        <!-- Content in English -->
        <div id="content-en" class="lang-content">
          <h2 class="section-title">About Me</h2>
          <p class="lead-text">
            Sports Physiotherapist with 4+ years of clinical and high-performance experience, based in Lisbon and available for international opportunities.
          </p>
          <p class="body-text">
            Currently working as a Physiotherapist and Clinical Shift Coordinator at <strong>Fisiogaspar</strong>, leading a multidisciplinary team while managing complex musculoskeletal, post-surgical, and return-to-sport rehabilitation plans.
          </p>
          
          <div class="credentials-grid">
            <div class="credential-card">
              <h3>Elite Padel</h3>
              <p>Official Physiotherapist for the <strong>Portuguese Veterans National Padel Team</strong>, providing medical support across global championships since 2023 and major international events (WPT &amp; FIP Platinum).</p>
            </div>
            <div class="credential-card">
              <h3>Competition Climbing</h3>
              <p>Medical Team Collaborator for the <strong>Portuguese Competition Climbing National Team (FPME)</strong>, delivering specialized sports physiotherapy within an elite setting.</p>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>

  <!-- Secção de Serviços -->
  <section id="services" class="services-section">
    <div class="container">
      <h2 class="section-title" style="text-align: center;">Serviços &amp; Acompanhamento</h2>
      
      <div class="services-grid">
        <!-- Serviço 1: Domicílio -->
        <div class="service-card">
          <div>
            <h3>Fisioterapia ao Domicílio</h3>
            <div class="service-price">€50 <span>/ sessão</span></div>
            <p class="service-desc">Atendimento presencial individualizado na área da Grande Lisboa e periferia. Avaliação clínica, tratamento musculoesquelético e reabilitação funcional.</p>
          </div>
          <a href="https://wa.me/351910326002" target="_blank" class="btn-contact">Agendar Sessão</a>
        </div>

        <!-- Serviço 2: Online Coaching -->
        <div class="service-card">
          <div>
            <h3>Online Coaching</h3>
            <div class="service-price">€100 <span>/ mês</span></div>
            <p class="service-desc">Acompanhamento à distância com plano de treino e reabilitação personalizado, reavaliação clínica online semanal/mensal e ajuste contínuo de carga.</p>
          </div>
          <a href="https://wa.me/351910326002" target="_blank" class="btn-contact">Saber Mais</a>
        </div>

        <!-- Serviço 3: Pack Híbrido -->
        <div class="service-card">
          <div>
            <h3>Pack Híbrido</h3>
            <div class="service-price">€135 <span>/ mês</span></div>
            <p class="service-desc">Combinação de sessões presenciais ao domicílio com acompanhamento contínuo e plano de treino digital para máxima performance e recuperação.</p>
          </div>
          <a href="https://wa.me/351910326002" target="_blank" class="btn-contact">Aderir ao Pack</a>
        </div>
      </div>
    </div>
  </section>

  <!-- Rodapé -->
  <footer>
    <div class="container">
      <p>&copy; David Paredes - Fisioterapia Desportiva &amp; Alta Performance</p>
      <p style="margin-top: 8px; font-size: 0.85rem;">WA: +351 910 326 002 | davidparedes.fisio@gmail.com</p>
    </div>
  </footer>

  <!-- Script de Alternância de Idioma Corrigido -->
  <script>
    function switchLang(lang) {
      // Ocultar todos os blocos de conteúdo
      var contents = document.querySelectorAll('.lang-content');
      contents.forEach(function(el) {
        el.classList.remove('active');
      });

      // Desativar todos os botões
      var buttons = document.querySelectorAll('.lang-btn');
      buttons.forEach(function(btn) {
        btn.classList.remove('active');
      });

      // Ativar o conteúdo e o botão correspondentes
      var targetContent = document.getElementById('content- ' + lang); // tratado abaixo se houver espaço
      var targetContentClean = document.getElementById('content-' + lang);
      var targetBtn = document.getElementById('btn-' + lang);

      if (targetContentClean) {
        targetContentClean.classList.add('active');
      }
      if (targetBtn) {
        targetBtn.classList.add('active');
      }
    }
  </script>
</body>
</html>

# CandelaGeyfirtrepository
Prueba de repositorio 
Segunda prueba
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Candela Gey</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300..700;1,9..144,400..600&family=Manrope:wght@400;500;600;700;800&display=swap" rel="stylesheet">
<style>
  /* ---------- Tokens ---------- */
  :root{
    --bg: #F3ECE1;
    --surface: #FBF8F2;
    --surface-alt: #E9DECB;
    --text: #211C18;
    --text-muted: #6B5F53;
    --accent: #C15D70;
    --accent-strong: #8A3C4C;
    --accent-soft: #EFD2CC;
    --border: #DACBB2;

    --font-display: 'Fraunces', Georgia, 'Iowan Old Style', serif;
    --font-body: 'Manrope', -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;

    --radius-sm: 4px;
    --radius-md: 12px;

    --space-1: .5rem;
    --space-2: 1rem;
    --space-3: 1.5rem;
    --space-4: 2.25rem;
    --space-5: 3.5rem;
    --space-6: 5.5rem;
    --space-7: 8rem;

    --shadow-card: 0 1px 2px rgba(33,28,24,.04), 0 12px 28px -14px rgba(33,28,24,.22);
    --shadow-lift: 0 10px 20px -8px rgba(33,28,24,.06), 0 24px 48px -20px rgba(33,28,24,.28);

    color-scheme: light;
  }

  @media (prefers-color-scheme: dark){
    :root:not([data-theme="light"]){
      --bg: #1B1613;
      --surface: #241E1A;
      --surface-alt: #2B2420;
      --text: #F2E9DC;
      --text-muted: #B7A997;
      --accent: #E3909D;
      --accent-strong: #F0B0B8;
      --accent-soft: #3B262A;
      --border: #3C332B;
      --shadow-card: 0 1px 2px rgba(0,0,0,.3), 0 12px 28px -14px rgba(0,0,0,.5);
      --shadow-lift: 0 10px 20px -8px rgba(0,0,0,.35), 0 24px 48px -20px rgba(0,0,0,.6);
      color-scheme: dark;
    }
  }
  :root[data-theme="dark"]{
    --bg: #1B1613;
    --surface: #241E1A;
    --surface-alt: #2B2420;
    --text: #F2E9DC;
    --text-muted: #B7A997;
    --accent: #E3909D;
    --accent-strong: #F0B0B8;
    --accent-soft: #3B262A;
    --border: #3C332B;
    --shadow-card: 0 1px 2px rgba(0,0,0,.3), 0 12px 28px -14px rgba(0,0,0,.5);
    --shadow-lift: 0 10px 20px -8px rgba(0,0,0,.35), 0 24px 48px -20px rgba(0,0,0,.6);
    color-scheme: dark;
  }

  /* ---------- Base ---------- */
  *,*::before,*::after{ box-sizing: border-box; }
  html{ scroll-behavior: smooth; }
  @media (prefers-reduced-motion: reduce){ html{ scroll-behavior: auto; } }

  body{
    margin: 0;
    background: var(--bg);
    color: var(--text);
    font-family: var(--font-body);
    font-size: 1rem;
    line-height: 1.6;
    -webkit-font-smoothing: antialiased;
  }

  h1,h2,h3{ font-family: var(--font-display); font-weight: 600; margin: 0; text-wrap: balance; color: var(--text); }
  p{ margin: 0; }
  a{ color: inherit; }
  img,svg{ max-width: 100%; display: block; }
  button{ font: inherit; }

  :focus-visible{ outline: 2px solid var(--accent-strong); outline-offset: 3px; border-radius: 2px; }

  .container{
    max-width: 1120px;
    margin-inline: auto;
    padding-inline: clamp(1.25rem, 4vw, 3rem);
  }

  .eyebrow{
    font-family: var(--font-body);
    font-size: .75rem;
    font-weight: 700;
    letter-spacing: .14em;
    text-transform: uppercase;
    color: var(--accent-strong);
  }

  .lede{
    font-size: 1.0625rem;
    color: var(--text-muted);
    max-width: 62ch;
  }

  /* ---------- Manifest divider (recurring motif) ---------- */
  .manifest-divider{
    display: flex;
    align-items: center;
    gap: var(--space-2);
    margin-block: 0;
    color: var(--text-muted);
  }
  .manifest-divider::before,
  .manifest-divider::after{
    content: "";
    flex: 1;
    height: 1px;
    background: var(--border);
  }
  .manifest-divider span{
    font-family: var(--font-body);
    font-size: .6875rem;
    font-weight: 700;
    letter-spacing: .16em;
    text-transform: uppercase;
    white-space: nowrap;
    font-variant-numeric: tabular-nums;
  }

  /* ---------- Header ---------- */
  .site-header{
    position: fixed;
    inset-block-start: 0;
    inset-inline: 0;
    z-index: 100;
    background: color-mix(in srgb, var(--bg) 88%, transparent);
    backdrop-filter: blur(10px) saturate(1.1);
    -webkit-backdrop-filter: blur(10px) saturate(1.1);
    border-bottom: 1px solid transparent;
    transition: border-color .35s ease, box-shadow .35s ease;
  }
  .site-header.is-scrolled{
    border-bottom-color: var(--border);
    box-shadow: 0 8px 24px -20px rgba(0,0,0,.4);
  }
  .site-header .container{
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding-block: 1.05rem;
  }
  .brand{
    font-family: var(--font-display);
    font-size: 1.15rem;
    font-weight: 600;
    letter-spacing: .01em;
    text-decoration: none;
  }
  .brand span{ color: var(--accent-strong); }

  .site-nav ul{
    list-style: none;
    display: flex;
    gap: var(--space-4);
    margin: 0;
    padding: 0;
  }
  .site-nav a{
    text-decoration: none;
    font-size: .8125rem;
    font-weight: 600;
    letter-spacing: .06em;
    text-transform: uppercase;
    color: var(--text-muted);
    position: relative;
    padding-block: .2rem;
    transition: color .2s ease;
  }
  .site-nav a::after{
    content: "";
    position: absolute;
    left: 0; right: 100%;
    bottom: -4px;
    height: 1.5px;
    background: var(--accent-strong);
    transition: right .25s ease;
  }
  .site-nav a:hover,
  .site-nav a:focus-visible{ color: var(--text); }
  .site-nav a:hover::after,
  .site-nav a:focus-visible::after{ right: 0; }

  .nav-toggle{
    display: none;
    background: none;
    border: 1px solid var(--border);
    border-radius: var(--radius-sm);
    width: 40px; height: 36px;
    align-items: center; justify-content: center;
    cursor: pointer;
    color: var(--text);
  }
  .nav-toggle svg{ width: 18px; height: 18px; }
  .nav-toggle .icon-close{ display: none; }

  @media (max-width: 720px){
    .nav-toggle{ display: inline-flex; }
    .site-nav{
      position: fixed;
      inset-inline: 0;
      top: 64px;
      background: var(--surface);
      border-bottom: 1px solid var(--border);
      transform: translateY(-8px);
      opacity: 0;
      visibility: hidden;
      pointer-events: none;
      transition: opacity .22s ease, transform .22s ease, visibility .22s;
    }
    .site-nav ul{
      flex-direction: column;
      gap: 0;
      padding: var(--space-2) clamp(1.25rem,4vw,3rem) var(--space-3);
    }
    .site-nav li{ border-top: 1px solid var(--border); }
    .site-nav li:first-child{ border-top: none; }
    .site-nav a{ display: block; padding-block: .9rem; }
    .site-nav a::after{ display: none; }
    body.nav-open .site-nav{
      opacity: 1; visibility: visible; transform: none; pointer-events: auto;
    }
    body.nav-open .nav-toggle .icon-open{ display: none; }
    body.nav-open .nav-toggle .icon-close{ display: block; }
    body.nav-open{ overflow: hidden; }
  }

  /* ---------- Hero ---------- */
  .hero{
    position: relative;
    padding-block: calc(96px + var(--space-6)) var(--space-6);
    overflow: hidden;
  }
  .hero .container{
    position: relative;
    z-index: 1;
    display: grid;
    gap: var(--space-3);
    max-width: 780px;
  }
  .hero-route{
    position: absolute;
    right: -6%;
    top: 8%;
    width: min(46vw, 560px);
    height: auto;
    color: var(--accent);
    opacity: .5;
    z-index: 0;
    pointer-events: none;
  }
  .hero-route path{
    fill: none;
    stroke: currentColor;
    stroke-width: 1.4;
    stroke-linecap: round;
    stroke-dasharray: 1;
    stroke-dashoffset: 1;
    pathLength: 1;
    animation: draw-route 2.4s .3s cubic-bezier(.4,0,.2,1) forwards;
  }
  .hero-route circle{ fill: currentColor; opacity: 0; animation: fade-in .6s 2.1s ease forwards; }
  @keyframes draw-route{ to{ stroke-dashoffset: 0; } }
  @keyframes fade-in{ to{ opacity: 1; } }

  .hero-name{
    font-size: clamp(2.75rem, 4.4vw + 1.2rem, 5.25rem);
    line-height: .98;
    letter-spacing: -.01em;
    opacity: 0;
    transform: translateY(14px);
    animation: rise .7s .05s cubic-bezier(.16,1,.3,1) forwards;
  }
  .hero-role{
    font-family: var(--font-display);
    font-style: italic;
    font-weight: 500;
    font-size: clamp(1.1rem, 1vw + 1rem, 1.4rem);
    color: var(--accent-strong);
    opacity: 0;
    transform: translateY(14px);
    animation: rise .7s .18s cubic-bezier(.16,1,.3,1) forwards;
  }
  .hero-desc{
    font-size: 1.125rem;
    max-width: 54ch;
    color: var(--text-muted);
    opacity: 0;
    transform: translateY(14px);
    animation: rise .7s .3s cubic-bezier(.16,1,.3,1) forwards;
  }
  .hero-actions{
    display: flex;
    flex-wrap: wrap;
    gap: var(--space-2);
    align-items: center;
    margin-top: var(--space-1);
    opacity: 0;
    transform: translateY(14px);
    animation: rise .7s .42s cubic-bezier(.16,1,.3,1) forwards;
  }
  @keyframes rise{ to{ opacity: 1; transform: none; } }
  @media (prefers-reduced-motion: reduce){
    .hero-name,.hero-role,.hero-desc,.hero-actions{ animation: none; opacity: 1; transform: none; }
    .hero-route path{ animation: none; stroke-dashoffset: 0; }
    .hero-route circle{ animation: none; opacity: 1; }
  }

  /* ---------- Buttons ---------- */
  .btn{
    display: inline-flex;
    align-items: center;
    gap: .5rem;
    padding: .8rem 1.6rem;
    border-radius: var(--radius-sm);
    font-weight: 700;
    font-size: .9rem;
    text-decoration: none;
    border: 1px solid transparent;
    cursor: pointer;
    transition: transform .18s ease, box-shadow .18s ease, background .18s ease, border-color .18s ease;
  }
  .btn:active{ transform: translateY(1px); }
  .btn-primary{
    background: var(--accent-strong);
    color: var(--surface);
  }
  .btn-primary:hover{ box-shadow: var(--shadow-lift); transform: translateY(-2px); }
  .btn-ghost{
    background: transparent;
    border-color: var(--border);
    color: var(--text);
  }
  .btn-ghost:hover{ border-color: var(--accent-strong); color: var(--accent-strong); }

  /* ---------- Sections ---------- */
  section{ padding-block: var(--space-6); }
  .section-head{
    display: flex;
    align-items: baseline;
    justify-content: space-between;
    gap: var(--space-3);
    margin-bottom: var(--space-5);
    flex-wrap: wrap;
  }
  .section-title{ font-size: clamp(1.8rem, 1.4vw + 1.3rem, 2.4rem); }

  /* ---------- About ---------- */
  .about-grid{
    display: grid;
    grid-template-columns: 1.5fr 1fr;
    gap: var(--space-5);
    align-items: start;
  }
  .about-copy p + p{ margin-top: var(--space-2); }
  .about-copy p{ color: var(--text-muted); font-size: 1.03rem; max-width: 60ch; }
  .about-copy p strong{ color: var(--text); font-weight: 700; }

  .stat-tile{
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: var(--radius-md);
    padding: var(--space-4) var(--space-3);
    box-shadow: var(--shadow-card);
  }
  .stat-tile .stat-num{
    font-family: var(--font-display);
    font-size: 3.6rem;
    line-height: 1;
    font-variant-numeric: tabular-nums;
    color: var(--accent-strong);
  }
  .stat-tile .stat-label{
    margin-top: .6rem;
    font-size: .85rem;
    font-weight: 600;
    color: var(--text-muted);
    letter-spacing: .02em;
  }
  .stat-tile .stat-tags{
    margin-top: var(--space-3);
    display: flex;
    flex-wrap: wrap;
    gap: .4rem;
    padding-top: var(--space-3);
    border-top: 1px solid var(--border);
  }
  .tag{
    font-size: .6875rem;
    font-weight: 700;
    letter-spacing: .06em;
    text-transform: uppercase;
    color: var(--text-muted);
    background: var(--surface-alt);
    border-radius: 999px;
    padding: .3rem .65rem;
  }

  /* ---------- Services ---------- */
  .services-grid{
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: var(--space-3);
  }
  .service-card{
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: var(--radius-md);
    padding: var(--space-4);
    box-shadow: var(--shadow-card);
    transition: transform .25s ease, box-shadow .25s ease, border-color .25s ease;
  }
  .service-card:hover{
    transform: translateY(-5px);
    box-shadow: var(--shadow-lift);
    border-color: var(--accent-soft);
  }
  .service-icon{
    width: 44px; height: 44px;
    display: flex; align-items: center; justify-content: center;
    border-radius: var(--radius-sm);
    background: var(--accent-soft);
    color: var(--accent-strong);
    margin-bottom: var(--space-3);
  }
  .service-icon svg{ width: 24px; height: 24px; stroke: currentColor; fill: none; stroke-width: 1.6; stroke-linecap: round; stroke-linejoin: round; }
  .service-card h3{ font-size: 1.2rem; margin-bottom: .55rem; }
  .service-card p{ color: var(--text-muted); font-size: .95rem; }

  /* ---------- Contact ---------- */
  .contact{
    background: var(--surface-alt);
    border-radius: var(--radius-md);
    padding: var(--space-5) clamp(1.5rem, 4vw, 4rem);
    display: grid;
    gap: var(--space-3);
    justify-items: start;
    text-align: left;
  }
  .contact .section-title{ max-width: 20ch; }
  .contact-actions{
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: var(--space-3);
    margin-top: var(--space-1);
  }
  .email-copy{
    display: inline-flex;
    align-items: center;
    gap: .5rem;
    background: none;
    border: none;
    padding: 0;
    color: var(--text-muted);
    font-size: .95rem;
    font-family: var(--font-body);
    cursor: pointer;
    border-bottom: 1px dashed var(--border);
    transition: color .2s ease, border-color .2s ease;
  }
  .email-copy:hover{ color: var(--accent-strong); border-color: var(--accent-strong); }
  .email-copy svg{ width: 15px; height: 15px; stroke: currentColor; fill: none; stroke-width: 1.6; }
  .copy-toast{
    font-size: .8rem;
    font-weight: 600;
    color: var(--accent-strong);
    opacity: 0;
    transition: opacity .25s ease;
  }
  .copy-toast.is-shown{ opacity: 1; }

  /* ---------- Footer ---------- */
  .site-footer{
    border-top: 1px solid var(--border);
    padding-block: var(--space-4);
  }
  .site-footer .container{
    display: flex;
    flex-wrap: wrap;
    gap: var(--space-2);
    align-items: center;
    justify-content: space-between;
  }
  .site-footer p{ font-size: .8125rem; color: var(--text-muted); }
  .site-footer .brand{ font-size: .95rem; }

  /* ---------- Scroll reveal ---------- */
  .js-reveal .reveal{
    opacity: 0;
    transform: translateY(18px);
    transition: opacity .7s cubic-bezier(.16,1,.3,1), transform .7s cubic-bezier(.16,1,.3,1);
  }
  .js-reveal .reveal.is-visible{ opacity: 1; transform: none; }
  .js-reveal .reveal-stagger.is-visible > *{ transition-delay: calc(var(--i, 0) * 90ms); }

  @media (max-width: 860px){
    .about-grid{ grid-template-columns: 1fr; }
  }
  @media (max-width: 600px){
    .hero{ padding-block: calc(80px + var(--space-4)) var(--space-5); }
    section{ padding-block: var(--space-5); }
    .hero-route{ width: 70vw; top: 2%; opacity: .35; }
    .contact{ padding-inline: var(--space-3); }
    .site-footer .container{ flex-direction: column; align-items: flex-start; }
  }
</style>
</head>
<body>

<header class="site-header">
  <div class="container">
    <a href="#inicio" class="brand">Candela <span>Gey</span></a>
    <nav class="site-nav" id="site-nav">
      <ul>
        <li><a href="#sobre-mi">Sobre mí</a></li>
        <li><a href="#servicios">Servicios</a></li>
        <li><a href="#contacto">Contacto</a></li>
      </ul>
    </nav>
    <button class="nav-toggle" id="nav-toggle" aria-expanded="false" aria-controls="site-nav" aria-label="Abrir menú">
      <svg class="icon-open" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round"><line x1="3" y1="6" x2="21" y2="6"/><line x1="3" y1="12" x2="21" y2="12"/><line x1="3" y1="18" x2="21" y2="18"/></svg>
      <svg class="icon-close" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round"><line x1="5" y1="5" x2="19" y2="19"/><line x1="19" y1="5" x2="5" y2="19"/></svg>
    </button>
  </div>
</header>

<main>
  <section class="hero" id="inicio">
    <svg class="hero-route" viewBox="0 0 480 300" aria-hidden="true">
      <path pathLength="1" d="M10 240 C 120 260, 160 90, 260 100 S 420 190, 470 70"/>
      <circle cx="10" cy="240" r="4"/>
      <circle cx="260" cy="100" r="4"/>
      <circle cx="470" cy="70" r="4"/>
    </svg>
    <div class="container">
      <p class="eyebrow hero-role" style="animation-delay:0s;">Licenciada en Comercio Internacional</p>
      <h1 class="hero-name">Candela Gey</h1>
      <p class="lede hero-desc">Ayudo a emprendedoras a incursionarse en el mundo del comex: procesos de importación y exportación explicados sin vueltas, para que tomes decisiones de negocio con más confianza.</p>
      <div class="hero-actions">
        <a href="#contacto" class="btn btn-primary">Conversemos</a>
        <a href="#servicios" class="btn btn-ghost">Ver servicios</a>
      </div>
    </div>
  </section>

  <div class="container">
    <p class="manifest-divider" aria-hidden="true"><span>FOB · CIF · EXW</span></p>
  </div>

  <section id="sobre-mi">
    <div class="container">
      <div class="section-head reveal">
        <div>
          <p class="eyebrow">Sobre mí</p>
          <h2 class="section-title">Comex con cercanía</h2>
        </div>
      </div>
      <div class="about-grid">
        <div class="about-copy reveal">
          <p>Soy <strong>Licenciada en Comercio Internacional</strong> con más de 5 años de experiencia en operaciones de comercio exterior. Hoy mi trabajo se enfoca en acompañar a emprendedoras que quieren dar sus primeros pasos en el comex: entender procesos de importación y exportación, ordenar la parte operativa y animarse a un mundo que suele parecer reservado a unos pocos.</p>
          <p>Fuera de la operatoria diaria, me apasionan las <strong>finanzas personales</strong> y la <strong>inteligencia artificial</strong> — dos herramientas que hoy uso para pensar mejor cada proyecto y cada decisión de negocio.</p>
        </div>
        <div class="stat-tile reveal">
          <p class="stat-num">5+</p>
          <p class="stat-label">Años de experiencia en comercio exterior</p>
          <div class="stat-tags">
            <span class="tag">Comex</span>
            <span class="tag">Finanzas</span>
            <span class="tag">IA aplicada</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <div class="container">
    <p class="manifest-divider" aria-hidden="true"><span>AWB · B/L · HS CODE</span></p>
  </div>

  <section id="servicios">
    <div class="container">
      <div class="section-head reveal">
        <div>
          <p class="eyebrow">Servicios</p>
          <h2 class="section-title">Cómo puedo ayudarte</h2>
        </div>
        <p class="lede" style="max-width:34ch;">Acompañamiento pensado para emprendedoras que están construyendo su propio negocio.</p>
      </div>
      <div class="services-grid">
        <article class="service-card reveal">
          <div class="service-icon">
            <svg viewBox="0 0 40 40"><circle cx="20" cy="20" r="15"/><path d="M25.5 14.5l-4 8-8 4 4-8z"/><circle cx="20" cy="20" r="1.3" fill="currentColor" stroke="none"/></svg>
          </div>
          <h3>Primeros pasos en comex</h3>
          <p>Acompañamiento para dar tus primeros pasos en importación y exportación, con la experiencia de más de 5 años trabajando en comercio exterior.</p>
        </article>
        <article class="service-card reveal">
          <div class="service-icon">
            <svg viewBox="0 0 40 40"><polyline points="6,30 15,20 21,25 33,11"/><polyline points="25,11 33,11 33,19"/></svg>
          </div>
          <h3>Finanzas personales</h3>
          <p>Una mirada práctica sobre el dinero, pensada para quienes están construyendo su propio negocio y necesitan ordenar sus finanzas.</p>
        </article>
        <article class="service-card reveal">
          <div class="service-icon">
            <svg viewBox="0 0 40 40"><circle cx="10" cy="12" r="2.8"/><circle cx="30" cy="12" r="2.8"/><circle cx="20" cy="30" r="2.8"/><path d="M12.4 13.6L18 27.5M27.6 13.6L22 27.5M13 12H27"/></svg>
          </div>
          <h3>IA aplicada al negocio</h3>
          <p>Herramientas de inteligencia artificial para optimizar procesos, analizar mercados y tomar mejores decisiones de negocio.</p>
        </article>
      </div>
    </div>
  </section>

  <div class="container">
    <p class="manifest-divider" aria-hidden="true"><span>INCOTERMS 2020 · DDP</span></p>
  </div>

  <section id="contacto">
    <div class="container">
      <div class="contact reveal">
        <p class="eyebrow">Contacto</p>
        <h2 class="section-title">Demos el primer paso juntas</h2>
        <p class="lede">¿Querés incursionar en el comercio exterior o necesitás una mano para ordenar tu negocio? Escribime y charlamos.</p>
        <div class="contact-actions">
          <a href="mailto:gey.candela@gmail.com" class="btn btn-primary">Escribime</a>
          <button class="email-copy" id="copy-email" type="button">
            <svg viewBox="0 0 24 24"><rect x="8" y="8" width="12" height="12" rx="2"/><path d="M16 8V6a2 2 0 0 0-2-2H6a2 2 0 0 0-2 2v8a2 2 0 0 0 2 2h2"/></svg>
            gey.candela@gmail.com
          </button>
          <span class="copy-toast" id="copy-toast" role="status">¡Copiado!</span>
        </div>
      </div>
    </div>
  </section>
</main>

<footer class="site-footer">
  <div class="container">
    <a href="#inicio" class="brand">Candela <span>Gey</span></a>
    <p>© 2026 Candela Gey — Licenciada en Comercio Internacional</p>
  </div>
</footer>

<script>
  (function(){
    var header = document.querySelector('.site-header');
    var onScroll = function(){
      header.classList.toggle('is-scrolled', window.scrollY > 8);
    };
    onScroll();
    addEventListener('scroll', onScroll, { passive: true });

    var toggle = document.getElementById('nav-toggle');
    var nav = document.getElementById('site-nav');
    toggle.addEventListener('click', function(){
      var open = document.body.classList.toggle('nav-open');
      toggle.setAttribute('aria-expanded', open ? 'true' : 'false');
      toggle.setAttribute('aria-label', open ? 'Cerrar menú' : 'Abrir menú');
    });
    nav.querySelectorAll('a').forEach(function(a){
      a.addEventListener('click', function(){
        document.body.classList.remove('nav-open');
        toggle.setAttribute('aria-expanded', 'false');
        toggle.setAttribute('aria-label', 'Abrir menú');
      });
    });

    var reduceMotion = window.matchMedia('(prefers-reduced-motion: reduce)').matches;
    if (!reduceMotion && 'IntersectionObserver' in window){
      document.documentElement.classList.add('js-reveal');
      var io = new IntersectionObserver(function(entries){
        entries.forEach(function(entry){
          if (entry.isIntersecting){
            entry.target.classList.add('is-visible');
            io.unobserve(entry.target);
          }
        });
      }, { threshold: 0.15, rootMargin: '0px 0px -8% 0px' });
      document.querySelectorAll('.reveal').forEach(function(el){ io.observe(el); });
    }

    var copyBtn = document.getElementById('copy-email');
    var toast = document.getElementById('copy-toast');
    var toastTimer;
    copyBtn.addEventListener('click', function(){
      var email = 'gey.candela@gmail.com';
      var showToast = function(){
        clearTimeout(toastTimer);
        toast.classList.add('is-shown');
        toastTimer = setTimeout(function(){ toast.classList.remove('is-shown'); }, 2000);
      };
      if (navigator.clipboard && navigator.clipboard.writeText){
        navigator.clipboard.writeText(email).then(showToast).catch(function(){});
      }
    });
  })();
</script>
</body>
</html>

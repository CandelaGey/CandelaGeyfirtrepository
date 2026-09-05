<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Candela Gey — Comercio Internacional</title>
<meta name="description" content="Candela Gey, Licenciada en Comercio Internacional. Ayudo a emprendedoras a incursionar en el mundo del comex.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,400;0,9..144,500;0,9..144,600;1,9..144,500&family=IBM+Plex+Sans:wght@400;500;600&family=IBM+Plex+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --beige: #F3E9DA;
    --beige-deep: #E8DAC0;
    --beige-line: #D5C3A2;
    --ink: #211C17;
    --ink-soft: #58493C;
    --rose: #C67C90;
    --rose-deep: #8B4457;
    --rose-pale: #F1D9DD;
    --paper: #FBF6EC;
    --header-h: 76px;
    --ease: cubic-bezier(.22,.61,.36,1);
  }

  *,*::before,*::after{ box-sizing: border-box; }
  html{ scroll-behavior: smooth; }

  body{
    margin:0;
    background: var(--beige);
    color: var(--ink);
    font-family: "IBM Plex Sans", -apple-system, sans-serif;
    line-height: 1.6;
    -webkit-font-smoothing: antialiased;
  }

  h1,h2,h3{
    font-family: "Fraunces", Georgia, serif;
    font-weight: 500;
    line-height: 1.08;
    margin: 0;
    color: var(--ink);
  }

  p{ margin: 0 0 1rem; color: var(--ink-soft); max-width: 62ch; }
  a{ color: inherit; }
  img,svg{ display:block; max-width:100%; }

  a:focus-visible,
  button:focus-visible{
    outline: 2px solid var(--rose-deep);
    outline-offset: 3px;
    border-radius: 2px;
  }

  .wrap{
    width: 100%;
    max-width: 1120px;
    margin: 0 auto;
    padding: 0 clamp(1.25rem, 4vw, 2.5rem);
  }

  /* ---------- Buttons ---------- */
  .btn{
    display: inline-flex;
    align-items: center;
    gap: .5rem;
    font-family: "IBM Plex Sans", sans-serif;
    font-weight: 500;
    font-size: .95rem;
    padding: .8rem 1.5rem;
    border-radius: 2px;
    border: 1.5px solid var(--ink);
    text-decoration: none;
    cursor: pointer;
    transition: background-color .25s var(--ease), color .25s var(--ease), border-color .25s var(--ease);
  }
  .btn-primary{
    background: var(--ink);
    color: var(--beige);
  }
  .btn-primary:hover{ background: var(--rose-deep); border-color: var(--rose-deep); }
  .btn-ghost{
    background: transparent;
    color: var(--ink);
  }
  .btn-ghost:hover{ background: var(--rose-pale); border-color: var(--rose-deep); }
  .btn-small{ padding: .55rem 1.1rem; font-size: .85rem; }
  .btn-on-dark{ border-color: var(--beige); color: var(--beige); }
  .btn-on-dark.btn-primary{ background: var(--rose); border-color: var(--rose); color: var(--ink); }
  .btn-on-dark.btn-primary:hover{ background: var(--beige); border-color: var(--beige); }
  .btn-on-dark.btn-ghost:hover{ background: rgba(243,233,218,.1); }

  /* ---------- Header ---------- */
  .site-header{
    position: fixed;
    top: 0; left: 0; right: 0;
    height: var(--header-h);
    display: flex;
    align-items: center;
    background: rgba(243,233,218,.88);
    backdrop-filter: blur(8px);
    border-bottom: 1px solid transparent;
    z-index: 100;
    transition: border-color .3s var(--ease), box-shadow .3s var(--ease);
  }
  .site-header.is-scrolled{
    border-bottom-color: var(--beige-line);
    box-shadow: 0 6px 18px -14px rgba(33,28,23,.35);
  }
  .header-inner{
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 1rem;
  }
  .brand{
    font-family: "Fraunces", serif;
    font-size: 1.2rem;
    font-weight: 600;
    text-decoration: none;
    color: var(--ink);
    white-space: nowrap;
  }
  .nav{
    display: flex;
    gap: clamp(1rem, 2.5vw, 2.2rem);
  }
  .nav a{
    text-decoration: none;
    font-size: .95rem;
    color: var(--ink-soft);
    padding: .3rem 0;
    border-bottom: 1.5px solid transparent;
    transition: color .2s var(--ease), border-color .2s var(--ease);
  }
  .nav a:hover{ color: var(--ink); border-color: var(--rose); }

  .header-actions{ display: flex; align-items: center; gap: .9rem; }

  .nav-toggle{
    display: none;
    width: 40px; height: 40px;
    background: transparent;
    border: none;
    cursor: pointer;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 5px;
  }
  .nav-toggle span{
    width: 22px; height: 2px;
    background: var(--ink);
    transition: transform .3s var(--ease), opacity .3s var(--ease);
  }
  .nav-toggle[aria-expanded="true"] span:nth-child(1){ transform: translateY(7px) rotate(45deg); }
  .nav-toggle[aria-expanded="true"] span:nth-child(2){ opacity: 0; }
  .nav-toggle[aria-expanded="true"] span:nth-child(3){ transform: translateY(-7px) rotate(-45deg); }

  /* ---------- Sections shared ---------- */
  section{ padding: clamp(4rem, 9vw, 7.5rem) 0; }
  .section-head{ margin-bottom: clamp(2rem, 5vw, 3.2rem); }
  .section-head h2{ font-size: clamp(1.9rem, 3vw, 2.5rem); }
  .section-head p{ margin-top: .7rem; }

  /* ---------- Hero ---------- */
  .hero{
    padding-top: calc(var(--header-h) + clamp(3rem, 8vw, 5rem));
    padding-bottom: clamp(3rem, 8vw, 5rem);
    scroll-margin-top: var(--header-h);
  }
  .hero-inner{
    display: grid;
    grid-template-columns: 1.15fr .85fr;
    gap: clamp(2rem, 5vw, 4rem);
    align-items: center;
  }
  .hero-role{
    font-size: clamp(1.05rem, 2vw, 1.3rem);
    color: var(--rose-deep);
    font-weight: 500;
    margin: .9rem 0 1.1rem;
  }
  .hero-name{
    font-size: clamp(2.8rem, 6.4vw, 5.4rem);
    letter-spacing: -.01em;
  }
  .hero-desc{ font-size: 1.08rem; max-width: 46ch; }
  .hero-actions{
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
    margin-top: 1.6rem;
  }
  .hero-visual{ display: flex; justify-content: center; }
  .hero-visual svg{ width: min(100%, 340px); height: auto; }

  .stamp-group{
    transform-origin: 250px 322px;
    opacity: 0;
    animation: stampIn .9s var(--ease) .5s forwards;
  }
  @keyframes stampIn{
    0%{ opacity: 0; transform: scale(2.4) rotate(-20deg); }
    55%{ opacity: 1; transform: scale(.92) rotate(-9deg); }
    75%{ transform: scale(1.05) rotate(-7.5deg); }
    100%{ transform: scale(1) rotate(-8deg); }
  }
  .route-line{
    stroke-dasharray: 190;
    stroke-dashoffset: 190;
    animation: drawRoute 1.1s var(--ease) .3s forwards;
  }
  @keyframes drawRoute{ to{ stroke-dashoffset: 0; } }
  .route-mark{
    opacity: 0;
    animation: fadeIn .4s var(--ease) forwards;
  }
  .route-mark.mark-start{ animation-delay: .3s; }
  .route-mark.mark-end{ animation-delay: 1.3s; }
  @keyframes fadeIn{ to{ opacity: 1; } }

  /* ---------- About ---------- */
  .about-inner{
    display: grid;
    grid-template-columns: .8fr 1.2fr;
    gap: clamp(2.5rem, 6vw, 4.5rem);
    align-items: start;
  }
  .monogram{
    width: 128px; height: 128px;
    border-radius: 50%;
    border: 1.5px solid var(--ink);
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: "Fraunces", serif;
    font-size: 2.4rem;
    font-weight: 500;
    background: var(--paper);
    position: relative;
  }
  .monogram::after{
    content: "";
    position: absolute;
    inset: -10px;
    border: 1px dashed var(--beige-line);
    border-radius: 50%;
  }
  .focus-tags{
    list-style: none;
    margin: 1.8rem 0 0;
    padding: 0;
    display: flex;
    flex-direction: column;
    gap: .6rem;
    max-width: 220px;
  }
  .focus-tags li{
    background: var(--rose-pale);
    color: var(--rose-deep);
    font-size: .88rem;
    font-weight: 500;
    padding: .5rem .9rem;
    border-radius: 2px;
  }
  .about-content h2{ font-size: clamp(1.9rem, 3vw, 2.5rem); margin-bottom: 1.2rem; }
  .about-content p{ max-width: 58ch; }

  /* ---------- Services ---------- */
  .services{ background: var(--beige-deep); }
  .cards{
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.6rem;
  }
  .card{
    background: var(--paper);
    border: 1px solid var(--beige-line);
    border-top: 3px solid var(--rose);
    border-radius: 2px;
    padding: 2rem 1.7rem;
  }
  .card:nth-child(2){ border-top-color: var(--rose-deep); }
  .card:nth-child(3){ border-top-color: var(--ink); }
  .card-icon{ margin-bottom: 1.3rem; color: var(--ink); }
  .card h3{
    font-size: 1.2rem;
    font-weight: 500;
    margin-bottom: .6rem;
  }
  .card p{ font-size: .95rem; margin-bottom: 0; }

  /* ---------- Contact ---------- */
  .contact{
    background: var(--ink);
    color: var(--beige);
    scroll-margin-top: var(--header-h);
  }
  .contact .section-head h2{ color: var(--beige); }
  .contact .section-head p{ color: rgba(243,233,218,.72); }
  .contact-panel{
    background: rgba(243,233,218,.05);
    border: 1px solid rgba(243,233,218,.22);
    border-radius: 3px;
    padding: clamp(1.8rem, 4vw, 2.8rem);
    max-width: 560px;
  }
  .contact-row{
    display: flex;
    justify-content: space-between;
    gap: 1rem;
    padding: .85rem 0;
    border-bottom: 1px dashed rgba(243,233,218,.25);
    font-family: "IBM Plex Mono", monospace;
    font-size: .88rem;
  }
  .contact-row:last-of-type{ border-bottom: none; }
  .contact-row span:first-child{ color: rgba(243,233,218,.6); }
  .contact-row span:last-child{ color: var(--beige); }
  .contact-actions{
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
    margin-top: 1.6rem;
  }
  #copyFeedback{
    display: inline-block;
    font-size: .85rem;
    color: var(--rose);
    margin-left: .3rem;
    opacity: 0;
    transition: opacity .3s var(--ease);
  }
  #copyFeedback.is-visible{ opacity: 1; }

  /* ---------- Footer ---------- */
  .site-footer{
    background: var(--ink);
    color: rgba(243,233,218,.6);
    border-top: 1px solid rgba(243,233,218,.14);
  }
  .footer-inner{
    padding: 1.8rem 0;
    display: flex;
    flex-wrap: wrap;
    gap: .5rem 1.5rem;
    justify-content: space-between;
    font-size: .85rem;
  }

  /* ---------- Scroll reveal ---------- */
  .reveal{
    opacity: 0;
    transform: translateY(22px);
    transition: opacity .7s var(--ease), transform .7s var(--ease);
  }
  .reveal.is-visible{ opacity: 1; transform: translateY(0); }
  .reveal-stagger.is-visible > *{ opacity: 1; transform: translateY(0); }
  .reveal-stagger > *{
    opacity: 0;
    transform: translateY(18px);
    transition: opacity .6s var(--ease), transform .6s var(--ease);
  }
  .reveal-stagger > *:nth-child(1){ transition-delay: .05s; }
  .reveal-stagger > *:nth-child(2){ transition-delay: .16s; }
  .reveal-stagger > *:nth-child(3){ transition-delay: .27s; }

  @media (prefers-reduced-motion: reduce){
    html{ scroll-behavior: auto; }
    .reveal, .reveal-stagger > *, .stamp-group, .route-line, .route-mark{
      opacity: 1 !important;
      transform: none !important;
      animation: none !important;
      transition: none !important;
      stroke-dashoffset: 0 !important;
    }
  }

  /* ---------- Responsive ---------- */
  @media (max-width: 900px){
    .hero-inner{ grid-template-columns: 1fr; }
    .hero-visual{ order: -1; max-width: 260px; margin: 0 auto; }
    .about-inner{ grid-template-columns: 1fr; }
    .about-figure{ display: flex; align-items: center; gap: 1.6rem; }
    .focus-tags{ margin: 0; flex-direction: row; flex-wrap: wrap; max-width: none; }
    .cards{ grid-template-columns: 1fr 1fr; }
  }

  @media (max-width: 720px){
    .nav, .header-cta{ display: none; }
    .nav-toggle{ display: flex; }
    .site-header.nav-open .nav{
      display: flex;
      flex-direction: column;
      position: absolute;
      top: var(--header-h);
      left: 0; right: 0;
      background: var(--beige);
      border-bottom: 1px solid var(--beige-line);
      padding: 1rem clamp(1.25rem, 4vw, 2.5rem) 1.5rem;
      gap: .3rem;
    }
    .site-header.nav-open .header-cta{
      display: inline-flex;
      position: absolute;
      top: calc(var(--header-h) + 1px);
      right: clamp(1.25rem, 4vw, 2.5rem);
      transform: translateY(160px);
    }
    .cards{ grid-template-columns: 1fr; }
  }

  @media (max-width: 480px){
    .about-figure{ flex-direction: column; align-items: flex-start; }
    .focus-tags{ flex-direction: column; }
    .contact-row{ flex-direction: column; gap: .2rem; }
    .footer-inner{ flex-direction: column; }
  }
</style>
</head>
<body>

<header class="site-header" id="siteHeader">
  <div class="wrap header-inner">
    <a href="#top" class="brand">Candela Gey</a>
    <nav class="nav" id="mainNav">
      <a href="#sobre-mi">Sobre mí</a>
      <a href="#servicios">Servicios</a>
      <a href="#contacto">Contacto</a>
    </nav>
    <div class="header-actions">
      <a href="#contacto" class="btn btn-primary btn-small header-cta">Escribime</a>
      <button class="nav-toggle" id="navToggle" aria-label="Abrir menú" aria-expanded="false">
        <span></span><span></span><span></span>
      </button>
    </div>
  </div>
</header>

<main>

  <section class="hero" id="top">
    <div class="wrap hero-inner">
      <div class="hero-text">
        <h1 class="hero-name">Candela Gey</h1>
        <p class="hero-role">Licenciada en Comercio Internacional</p>
        <p class="hero-desc">Ayudo a emprendedoras a incursionar en el mundo del comercio exterior, con las finanzas y la tecnología como aliadas.</p>
        <div class="hero-actions">
          <a href="#contacto" class="btn btn-primary">Conversemos</a>
          <a href="#servicios" class="btn btn-ghost">Ver servicios</a>
        </div>
      </div>
      <div class="hero-visual" aria-hidden="true">
        <svg viewBox="0 0 360 420" xmlns="http://www.w3.org/2000/svg">
          <rect x="24" y="20" width="280" height="368" rx="4" fill="#FBF6EC" stroke="#211C17" stroke-width="1.5"/>
          <rect x="40" y="36" width="248" height="336" rx="2" fill="none" stroke="#D5C3A2" stroke-width="1" stroke-dasharray="4 5"/>

          <rect x="60" y="66" width="10" height="10" fill="#8B4457" class="route-mark mark-start"/>
          <line x1="70" y1="71" x2="220" y2="71" stroke="#8B4457" stroke-width="1.6" class="route-line"/>
          <circle cx="228" cy="71" r="6" fill="none" stroke="#8B4457" stroke-width="1.6" class="route-mark mark-end"/>

          <rect x="60" y="112" width="170" height="7" rx="3" fill="#E8DAC0"/>
          <rect x="60" y="134" width="130" height="7" rx="3" fill="#E8DAC0"/>
          <rect x="60" y="156" width="150" height="7" rx="3" fill="#E8DAC0"/>
          <rect x="60" y="178" width="90" height="7" rx="3" fill="#E8DAC0"/>

          <g class="stamp-group">
            <circle cx="250" cy="322" r="56" fill="none" stroke="#8B4457" stroke-width="2.5"/>
            <circle cx="250" cy="322" r="46" fill="none" stroke="#8B4457" stroke-width="1"/>
            <text x="250" y="315" text-anchor="middle" font-family="IBM Plex Mono, monospace" font-size="15" fill="#8B4457" font-weight="500">COMEX</text>
            <text x="250" y="335" text-anchor="middle" font-family="IBM Plex Mono, monospace" font-size="10" fill="#8B4457">C. GEY</text>
          </g>
        </svg>
      </div>
    </div>
  </section>

  <section class="about" id="sobre-mi">
    <div class="wrap about-inner">
      <div class="about-figure reveal">
        <div class="monogram">CG</div>
        <ul class="focus-tags">
          <li>Comercio exterior</li>
          <li>Finanzas personales</li>
          <li>Inteligencia artificial</li>
        </ul>
      </div>
      <div class="about-content reveal">
        <h2>Sobre mí</h2>
        <p>Soy Licenciada en Comercio Internacional con más de 5 años de experiencia acompañando procesos de importación y exportación. Me especializo en traducir la letra chica del comex en pasos concretos para quienes recién empiezan.</p>
        <p>Además, me apasionan las finanzas personales y la inteligencia artificial, y hoy combino ambas disciplinas para ayudar a emprendedoras a tomar decisiones de negocio más informadas, ordenadas y con menos vueltas.</p>
      </div>
    </div>
  </section>

  <section class="services" id="servicios">
    <div class="wrap">
      <div class="section-head reveal">
        <h2>Servicios</h2>
        <p>Acompañamiento pensado para emprendedoras que quieren dar el salto al comercio exterior sin perderse en el camino.</p>
      </div>
      <div class="cards reveal-stagger">
        <article class="card">
          <div class="card-icon">
            <svg width="34" height="34" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6">
              <rect x="3" y="8" width="18" height="12" rx="1"/>
              <path d="M3 12h18"/>
              <path d="M8 8V6a4 4 0 0 1 8 0v2"/>
            </svg>
          </div>
          <h3>Asesoría en comercio exterior</h3>
          <p>Guía práctica para importar o exportar por primera vez: trámites, costos y decisiones clave antes de dar el primer paso.</p>
        </article>
        <article class="card">
          <div class="card-icon">
            <svg width="34" height="34" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6">
              <path d="M4 19V9"/>
              <path d="M10 19V5"/>
              <path d="M16 19v-7"/>
              <circle cx="19" cy="6" r="2.4"/>
            </svg>
          </div>
          <h3>Estrategia financiera</h3>
          <p>Orden de cuentas y criterios claros para tomar decisiones financieras aplicadas a la realidad de tu negocio.</p>
        </article>
        <article class="card">
          <div class="card-icon">
            <svg width="34" height="34" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6">
              <circle cx="6" cy="6" r="2.2"/>
              <circle cx="18" cy="6" r="2.2"/>
              <circle cx="12" cy="18" r="2.2"/>
              <path d="M7.8 7.3 10.5 16"/>
              <path d="M16.2 7.3 13.5 16"/>
              <path d="M8.2 6h7.6"/>
            </svg>
          </div>
          <h3>Automatización con IA</h3>
          <p>Procesos de comex y finanzas más livianos, apoyados en inteligencia artificial aplicada a tareas del día a día.</p>
        </article>
      </div>
    </div>
  </section>

  <section class="contact" id="contacto">
    <div class="wrap">
      <div class="section-head reveal">
        <h2>Hablemos de tu proyecto</h2>
        <p>Contame en qué etapa estás y vemos juntas cómo avanzar.</p>
      </div>
      <div class="contact-panel reveal">
        <div class="contact-row"><span>Para</span><span>Candela Gey</span></div>
        <div class="contact-row"><span>Rol</span><span>Lic. en Comercio Internacional</span></div>
        <div class="contact-row"><span>Email</span><span>gey.candela@gmail.com</span></div>
        <div class="contact-actions">
          <a href="mailto:gey.candela@gmail.com" class="btn btn-primary btn-on-dark">Escribime un email</a>
          <button class="btn btn-ghost btn-on-dark" id="copyEmailBtn" type="button">Copiar email</button>
          <span id="copyFeedback">Copiado</span>
        </div>
      </div>
    </div>
  </section>

</main>

<footer class="site-footer">
  <div class="wrap footer-inner">
    <span>Candela Gey — Licenciada en Comercio Internacional</span>
    <span>© <span id="year"></span> Todos los derechos reservados.</span>
  </div>
</footer>

<script>
(function(){
  "use strict";

  document.getElementById('year').textContent = new Date().getFullYear();

  var header = document.getElementById('siteHeader');
  function onScroll(){
    if (window.scrollY > 12) header.classList.add('is-scrolled');
    else header.classList.remove('is-scrolled');
  }
  onScroll();
  window.addEventListener('scroll', onScroll, { passive: true });

  var navToggle = document.getElementById('navToggle');
  navToggle.addEventListener('click', function(){
    var isOpen = header.classList.toggle('nav-open');
    navToggle.setAttribute('aria-expanded', isOpen ? 'true' : 'false');
  });
  document.getElementById('mainNav').addEventListener('click', function(e){
    if (e.target.tagName === 'A'){
      header.classList.remove('nav-open');
      navToggle.setAttribute('aria-expanded', 'false');
    }
  });

  var reduceMotion = window.matchMedia('(prefers-reduced-motion: reduce)').matches;
  var revealTargets = document.querySelectorAll('.reveal, .reveal-stagger');
  if ('IntersectionObserver' in window && !reduceMotion){
    var io = new IntersectionObserver(function(entries){
      entries.forEach(function(entry){
        if (entry.isIntersecting){
          entry.target.classList.add('is-visible');
          io.unobserve(entry.target);
        }
      });
    }, { threshold: 0.15, rootMargin: '0px 0px -60px 0px' });
    revealTargets.forEach(function(el){ io.observe(el); });
  } else {
    revealTargets.forEach(function(el){ el.classList.add('is-visible'); });
  }

  var copyBtn = document.getElementById('copyEmailBtn');
  var copyFeedback = document.getElementById('copyFeedback');
  var email = 'gey.candela@gmail.com';
  copyBtn.addEventListener('click', function(){
    function showFeedback(){
      copyFeedback.classList.add('is-visible');
      setTimeout(function(){ copyFeedback.classList.remove('is-visible'); }, 2000);
    }
    if (navigator.clipboard && navigator.clipboard.writeText){
      navigator.clipboard.writeText(email).then(showFeedback).catch(function(){
        fallbackCopy();
      });
    } else {
      fallbackCopy();
    }
    function fallbackCopy(){
      var t = document.createElement('textarea');
      t.value = email;
      t.style.position = 'fixed';
      t.style.opacity = '0';
      document.body.appendChild(t);
      t.select();
      try { document.execCommand('copy'); } catch(e){}
      document.body.removeChild(t);
      showFeedback();
    }
  });
})();
</script>

</body>
</html>
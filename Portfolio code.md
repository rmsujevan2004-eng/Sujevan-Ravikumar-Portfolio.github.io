# Portfolio code  
  
<!DOCTYPE html>  
<html lang="en">  
<head>  
  <meta charset="UTF-8" />  
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />  
  <title>Sujevan Ravikumar — Creative Portfolio</title>  
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet" />  
  <style>  
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }  
  
    :root {  
      --cream: #F7F4EF;  
      --ink: #1A1814;  
      --ink-light: #4A4640;  
      --accent: #C8A96E;  
      --accent-light: #E8D9BC;  
      --rule: #D9D3C8;  
      --white: #FFFFFF;  
    }  
  
    html { scroll-behavior: smooth; }  
  
    body {  
      background: var(--cream);  
      color: var(--ink);  
      font-family: 'DM Sans', sans-serif;  
      font-weight: 300;  
      line-height: 1.6;  
      overflow-x: hidden;  
    }  
  
    /* ── NAV ── */  
    nav {  
      position: fixed; top: 0; left: 0; right: 0; z-index: 100;  
      display: flex; justify-content: space-between; align-items: center;  
      padding: 1.5rem 4rem;  
      background: rgba(247, 244, 239, 0.92);  
      backdrop-filter: blur(8px);  
      border-bottom: 1px solid var(--rule);  
    }  
  
    .nav-logo {  
      font-family: 'Cormorant Garamond', serif;  
      font-size: 1.15rem;  
      font-weight: 400;  
      letter-spacing: 0.08em;  
      text-transform: uppercase;  
      color: var(--ink);  
      text-decoration: none;  
    }  
  
    .nav-links { display: flex; gap: 2.5rem; list-style: none; }  
    .nav-links a {  
      font-size: 0.75rem;  
      letter-spacing: 0.12em;  
      text-transform: uppercase;  
      color: var(--ink-light);  
      text-decoration: none;  
      transition: color 0.2s;  
    }  
    .nav-links a:hover { color: var(--accent); }  
  
    /* ── HERO ── */  
    #hero {  
      min-height: 100vh;  
      display: grid;  
      grid-template-columns: 1fr 1fr;  
      align-items: center;  
      padding: 6rem 4rem 4rem;  
      gap: 4rem;  
    }  
  
    .hero-text { animation: fadeUp 1s ease both; }  
  
    .hero-eyebrow {  
      font-size: 0.7rem;  
      letter-spacing: 0.2em;  
      text-transform: uppercase;  
      color: var(--accent);  
      margin-bottom: 1.5rem;  
      display: flex;  
      align-items: center;  
      gap: 1rem;  
    }  
  
    .hero-eyebrow::before {  
      content: '';  
      display: block;  
      width: 2.5rem;  
      height: 1px;  
      background: var(--accent);  
    }  
  
    h1 {  
      font-family: 'Cormorant Garamond', serif;  
      font-size: clamp(3.5rem, 7vw, 6rem);  
      font-weight: 300;  
      line-height: 1.05;  
      letter-spacing: -0.01em;  
      margin-bottom: 1.5rem;  
    }  
  
    h1 em {  
      font-style: italic;  
      color: var(--accent);  
    }  
  
    .hero-desc {  
      font-size: 1rem;  
      color: var(--ink-light);  
      max-width: 38ch;  
      line-height: 1.75;  
      margin-bottom: 2.5rem;  
    }  
  
    .hero-tags {  
      display: flex;  
      gap: 0.75rem;  
      flex-wrap: wrap;  
      margin-bottom: 3rem;  
    }  
  
    .tag {  
      font-size: 0.7rem;  
      letter-spacing: 0.1em;  
      text-transform: uppercase;  
      padding: 0.4rem 0.9rem;  
      border: 1px solid var(--rule);  
      color: var(--ink-light);  
      border-radius: 2px;  
    }  
  
    .btn {  
      display: inline-flex;  
      align-items: center;  
      gap: 0.75rem;  
      font-size: 0.75rem;  
      letter-spacing: 0.15em;  
      text-transform: uppercase;  
      color: var(--white);  
      background: var(--ink);  
      text-decoration: none;  
      padding: 0.9rem 2rem;  
      transition: background 0.25s, gap 0.25s;  
    }  
  
    .btn:hover { background: var(--accent); gap: 1.25rem; }  
    .btn-outline {  
      background: transparent;  
      color: var(--ink);  
      border: 1px solid var(--ink);  
      margin-left: 1rem;  
    }  
    .btn-outline:hover { background: var(--ink); color: var(--white); }  
  
    .hero-visual {  
      position: relative;  
      animation: fadeIn 1.2s ease both 0.3s;  
    }  
  
    .hero-frame {  
      width: 100%;  
      aspect-ratio: 4/5;  
      background: var(--ink);  
      overflow: hidden;  
      position: relative;  
    }  
  
    .hero-frame-inner {  
      width: 100%;  
      height: 100%;  
      background: linear-gradient(135deg, #2A2620 0%, #1A1814 50%, #3A3028 100%);  
      display: flex;  
      align-items: center;  
      justify-content: center;  
    }  
  
    .hero-monogram {  
      font-family: 'Cormorant Garamond', serif;  
      font-size: 8rem;  
      font-weight: 300;  
      color: rgba(200, 169, 110, 0.25);  
      letter-spacing: -0.05em;  
      line-height: 1;  
      user-select: none;  
    }  
  
    .hero-frame-caption {  
      position: absolute;  
      bottom: 1.5rem;  
      left: 1.5rem;  
      font-size: 0.65rem;  
      letter-spacing: 0.15em;  
      text-transform: uppercase;  
      color: rgba(247, 244, 239, 0.5);  
    }  
  
    .hero-float-stat {  
      position: absolute;  
      bottom: -2rem;  
      right: -2rem;  
      background: var(--white);  
      border: 1px solid var(--rule);  
      padding: 1.25rem 1.75rem;  
      text-align: center;  
    }  
  
    .stat-number {  
      font-family: 'Cormorant Garamond', serif;  
      font-size: 2.5rem;  
      font-weight: 300;  
      color: var(--accent);  
      line-height: 1;  
      display: block;  
    }  
  
    .stat-label {  
      font-size: 0.65rem;  
      letter-spacing: 0.12em;  
      text-transform: uppercase;  
      color: var(--ink-light);  
      margin-top: 0.25rem;  
    }  
  
    /* ── SECTION SHARED ── */  
    section { padding: 6rem 4rem; }  
  
    .section-header {  
      display: flex;  
      align-items: baseline;  
      gap: 2rem;  
      margin-bottom: 4rem;  
      border-bottom: 1px solid var(--rule);  
      padding-bottom: 1.5rem;  
    }  
  
    .section-num {  
      font-family: 'Cormorant Garamond', serif;  
      font-size: 0.85rem;  
      color: var(--accent);  
      letter-spacing: 0.1em;  
    }  
  
    h2 {  
      font-family: 'Cormorant Garamond', serif;  
      font-size: clamp(2rem, 4vw, 3rem);  
      font-weight: 300;  
      letter-spacing: -0.01em;  
    }  
  
    /* ── SERVICES ── */  
    #services { background: var(--white); }  
  
    .services-grid {  
      display: grid;  
      grid-template-columns: repeat(3, 1fr);  
      gap: 0;  
      border: 1px solid var(--rule);  
    }  
  
    .service-card {  
      padding: 3rem 2.5rem;  
      border-right: 1px solid var(--rule);  
      position: relative;  
      overflow: hidden;  
      transition: background 0.3s;  
    }  
  
    .service-card:last-child { border-right: none; }  
    .service-card:hover { background: var(--cream); }  
  
    .service-icon {  
      font-size: 1.75rem;  
      margin-bottom: 1.5rem;  
      display: block;  
    }  
  
    .service-title {  
      font-family: 'Cormorant Garamond', serif;  
      font-size: 1.5rem;  
      font-weight: 400;  
      margin-bottom: 1rem;  
    }  
  
    .service-desc {  
      font-size: 0.875rem;  
      color: var(--ink-light);  
      line-height: 1.8;  
      margin-bottom: 1.5rem;  
    }  
  
    .service-list {  
      list-style: none;  
      display: flex;  
      flex-direction: column;  
      gap: 0.5rem;  
    }  
  
    .service-list li {  
      font-size: 0.75rem;  
      letter-spacing: 0.05em;  
      color: var(--ink-light);  
      display: flex;  
      align-items: center;  
      gap: 0.5rem;  
    }  
  
    .service-list li::before {  
      content: '—';  
      color: var(--accent);  
      font-size: 0.65rem;  
    }  
  
    .service-accent-line {  
      position: absolute;  
      top: 0; left: 0;  
      width: 0; height: 2px;  
      background: var(--accent);  
      transition: width 0.4s ease;  
    }  
  
    .service-card:hover .service-accent-line { width: 100%; }  
  
    /* ── WORK ── */  
    #work { background: var(--cream); }  
  
    .work-grid {  
      display: grid;  
      grid-template-columns: 1fr 1fr;  
      gap: 2px;  
    }  
  
    .work-item {  
      position: relative;  
      aspect-ratio: 16/10;  
      overflow: hidden;  
      cursor: pointer;  
      background: var(--ink);  
    }  
  
    .work-item.tall { grid-row: span 2; aspect-ratio: auto; }  
  
    .work-item-bg {  
      width: 100%;  
      height: 100%;  
      background: linear-gradient(135deg, #2A2620 0%, #1A1814 100%);  
      transition: transform 0.5s ease;  
      display: flex;  
      align-items: center;  
      justify-content: center;  
    }  
  
    .work-item:hover .work-item-bg { transform: scale(1.04); }  
  
    .work-placeholder {  
      font-family: 'Cormorant Garamond', serif;  
      font-size: 4rem;  
      color: rgba(200, 169, 110, 0.15);  
      user-select: none;  
    }  
  
    .work-overlay {  
      position: absolute;  
      inset: 0;  
      background: linear-gradient(to top, rgba(26,24,20,0.85) 0%, transparent 60%);  
      opacity: 0;  
      transition: opacity 0.3s;  
      display: flex;  
      flex-direction: column;  
      justify-content: flex-end;  
      padding: 2rem;  
    }  
  
    .work-item:hover .work-overlay { opacity: 1; }  
  
    .work-cat {  
      font-size: 0.65rem;  
      letter-spacing: 0.15em;  
      text-transform: uppercase;  
      color: var(--accent);  
      margin-bottom: 0.5rem;  
    }  
  
    .work-title {  
      font-family: 'Cormorant Garamond', serif;  
      font-size: 1.5rem;  
      font-weight: 300;  
      color: var(--white);  
    }  
  
    .work-note {  
      margin-top: 3rem;  
      font-size: 0.8rem;  
      color: var(--ink-light);  
      text-align: center;  
      font-style: italic;  
      font-family: 'Cormorant Garamond', serif;  
    }  
  
    /* ── ABOUT ── */  
    #about {  
      background: var(--ink);  
      color: var(--cream);  
    }  
  
    #about .section-header { border-bottom-color: rgba(247,244,239,0.15); }  
    #about h2 { color: var(--cream); }  
    #about .section-num { color: var(--accent); }  
  
    .about-grid {  
      display: grid;  
      grid-template-columns: 1fr 1fr;  
      gap: 6rem;  
      align-items: start;  
    }  
  
    .about-body {  
      font-size: 1.05rem;  
      line-height: 1.85;  
      color: rgba(247,244,239,0.75);  
    }  
  
    .about-body p + p { margin-top: 1.25rem; }  
  
    .about-pull {  
      font-family: 'Cormorant Garamond', serif;  
      font-size: 1.75rem;  
      font-weight: 300;  
      font-style: italic;  
      color: var(--accent);  
      line-height: 1.4;  
      border-left: 2px solid var(--accent);  
      padding-left: 2rem;  
      margin: 2.5rem 0;  
    }  
  
    .skills-block { margin-top: 1rem; }  
  
    .skill-row {  
      display: flex;  
      justify-content: space-between;  
      align-items: center;  
      padding: 1rem 0;  
      border-bottom: 1px solid rgba(247,244,239,0.1);  
    }  
  
    .skill-name {  
      font-size: 0.75rem;  
      letter-spacing: 0.1em;  
      text-transform: uppercase;  
      color: rgba(247,244,239,0.6);  
    }  
  
    .skill-bar {  
      flex: 1;  
      height: 1px;  
      background: rgba(247,244,239,0.1);  
      margin: 0 2rem;  
      position: relative;  
    }  
  
    .skill-fill {  
      position: absolute;  
      top: -0.5px;  
      left: 0;  
      height: 2px;  
      background: var(--accent);  
      transition: width 1.5s ease;  
    }  
  
    .skill-pct {  
      font-family: 'Cormorant Garamond', serif;  
      font-size: 1rem;  
      color: var(--accent);  
    }  
  
    /* ── CONTACT ── */  
    #contact { background: var(--cream); text-align: center; }  
  
    .contact-inner { max-width: 600px; margin: 0 auto; }  
  
    .contact-heading {  
      font-family: 'Cormorant Garamond', serif;  
      font-size: clamp(2.5rem, 6vw, 4.5rem);  
      font-weight: 300;  
      line-height: 1.1;  
      margin-bottom: 1.5rem;  
    }  
  
    .contact-heading em { font-style: italic; color: var(--accent); }  
  
    .contact-sub {  
      font-size: 0.9rem;  
      color: var(--ink-light);  
      margin-bottom: 3rem;  
      line-height: 1.75;  
    }  
  
    .contact-links {  
      display: flex;  
      justify-content: center;  
      gap: 1.5rem;  
      flex-wrap: wrap;  
    }  
  
    /* ── FOOTER ── */  
    footer {  
      background: var(--ink);  
      color: rgba(247,244,239,0.4);  
      text-align: center;  
      padding: 2rem 4rem;  
      font-size: 0.7rem;  
      letter-spacing: 0.1em;  
      display: flex;  
      justify-content: space-between;  
      align-items: center;  
    }  
  
    footer span { color: var(--accent); }  
  
    /* ── ANIMATIONS ── */  
    @keyframes fadeUp {  
      from { opacity: 0; transform: translateY(30px); }  
      to { opacity: 1; transform: translateY(0); }  
    }  
  
    @keyframes fadeIn {  
      from { opacity: 0; }  
      to { opacity: 1; }  
    }  
  
    .reveal {  
      opacity: 0;  
      transform: translateY(24px);  
      transition: opacity 0.7s ease, transform 0.7s ease;  
    }  
    .reveal.visible { opacity: 1; transform: none; }  
  
    /* ── RESPONSIVE ── */  
    @media (max-width: 900px) {  
      nav { padding: 1.25rem 2rem; }  
      .nav-links { gap: 1.5rem; }  
      #hero { grid-template-columns: 1fr; padding: 6rem 2rem 4rem; }  
      .hero-visual { display: none; }  
      section { padding: 4rem 2rem; }  
      .services-grid { grid-template-columns: 1fr; }  
      .service-card { border-right: none; border-bottom: 1px solid var(--rule); }  
      .work-grid { grid-template-columns: 1fr; }  
      .about-grid { grid-template-columns: 1fr; gap: 3rem; }  
      footer { flex-direction: column; gap: 0.5rem; }  
    }  
  </style>  
</head>  
<body>  
  
  <!-- NAV -->  
  <nav>  
    <a href="#hero" class="nav-logo">Sujevan Ravikumar</a>  
    <ul class="nav-links">  
      <li><a href="#services">Services</a></li>  
      <li><a href="#work">Work</a></li>  
      <li><a href="#about">About</a></li>  
      <li><a href="#contact">Contact</a></li>  
    </ul>  
  </nav>  
  
  <!-- HERO -->  
  <section id="hero">  
    <div class="hero-text">  
      <p class="hero-eyebrow">Creative Director & Filmmaker</p>  
      <h1>Story told<br>through <em>every</em><br>frame.</h1>  
      <p class="hero-desc">  
        I craft compelling visual narratives — from social media campaigns that stop the scroll, to cinematic films and VFX-driven content that leave a lasting impression.  
      </p>  
      <div class="hero-tags">  
        <span class="tag">Social Media Marketing</span>  
        <span class="tag">Film & Videography</span>  
        <span class="tag">Content Creation</span>  
        <span class="tag">VFX</span>  
      </div>  
      <div>  
        <a href="#work" class="btn">View Work →</a>  
        <a href="#contact" class="btn btn-outline">Get in Touch</a>  
      </div>  
    </div>  
    <div class="hero-visual">  
      <div class="hero-frame">  
        <div class="hero-frame-inner">  
          <div class="hero-monogram">SR</div>  
        </div>  
        <p class="hero-frame-caption">Add your showreel here</p>  
      </div>  
      <div class="hero-float-stat">  
        <span class="stat-number">3+</span>  
        <p class="stat-label">Fields of Expertise</p>  
      </div>  
    </div>  
  </section>  
  
  <!-- SERVICES -->  
  <section id="services">  
    <div class="section-header reveal">  
      <span class="section-num">01</span>  
      <h2>What I Do</h2>  
    </div>  
    <div class="services-grid reveal">  
  
      <div class="service-card">  
        <div class="service-accent-line"></div>  
        <span class="service-icon">📱</span>  
        <h3 class="service-title">Social Media Marketing</h3>  
        <p class="service-desc">Strategies and content that build brands, grow audiences, and drive real engagement across every major platform.</p>  
        <ul class="service-list">  
          <li>Platform Strategy & Growth</li>  
          <li>Short-Form Content (Reels, TikTok)</li>  
          <li>Brand Identity & Tone of Voice</li>  
          <li>Campaign Planning & Analytics</li>  
          <li>Influencer & Paid Collaboration</li>  
        </ul>  
      </div>  
  
      <div class="service-card">  
        <div class="service-accent-line"></div>  
        <span class="service-icon">🎬</span>  
        <h3 class="service-title">Film & Videography</h3>  
        <p class="service-desc">Cinematic storytelling from concept to final cut — commercials, documentaries, events, and narrative projects.</p>  
        <ul class="service-list">  
          <li>Concept Development & Pre-Production</li>  
          <li>Direction & Cinematography</li>  
          <li>Interview & Documentary Style</li>  
          <li>Colour Grading & Post-Production</li>  
          <li>Commercial & Brand Films</li>  
        </ul>  
      </div>  
  
      <div class="service-card">  
        <div class="service-accent-line"></div>  
        <span class="service-icon">✨</span>  
        <h3 class="service-title">Content Creation & VFX</h3>  
        <p class="service-desc">High-impact visual content powered by motion graphics, compositing, and creative effects that elevate any production.</p>  
        <ul class="service-list">  
          <li>Visual Effects & Compositing</li>  
          <li>Motion Graphics & Animation</li>  
          <li>Creative Content Packages</li>  
          <li>Thumbnail & Graphic Design</li>  
          <li>YouTube & Long-Form Production</li>  
        </ul>  
      </div>  
  
    </div>  
  </section>  
  
  <!-- WORK -->  
  <section id="work">  
    <div class="section-header reveal">  
      <span class="section-num">02</span>  
      <h2>Selected Work</h2>  
    </div>  
    <div class="work-grid reveal">  
  
      <div class="work-item tall">  
        <div class="work-item-bg">  
          <div class="work-placeholder">01</div>  
        </div>  
        <div class="work-overlay">  
          <p class="work-cat">Film & Videography</p>  
          <p class="work-title">Your Featured Project</p>  
        </div>  
      </div>  
  
      <div class="work-item">  
        <div class="work-item-bg">  
          <div class="work-placeholder">02</div>  
        </div>  
        <div class="work-overlay">  
          <p class="work-cat">Social Media Marketing</p>  
          <p class="work-title">Campaign Project</p>  
        </div>  
      </div>  
  
      <div class="work-item">  
        <div class="work-item-bg">  
          <div class="work-placeholder">03</div>  
        </div>  
        <div class="work-overlay">  
          <p class="work-cat">VFX & Content</p>  
          <p class="work-title">VFX Showcase</p>  
        </div>  
      </div>  
  
      <div class="work-item">  
        <div class="work-item-bg">  
          <div class="work-placeholder">04</div>  
        </div>  
        <div class="work-overlay">  
          <p class="work-cat">Content Creation</p>  
          <p class="work-title">Content Series</p>  
        </div>  
      </div>  
  
      <div class="work-item">  
        <div class="work-item-bg">  
          <div class="work-placeholder">05</div>  
        </div>  
        <div class="work-overlay">  
          <p class="work-cat">Film & Videography</p>  
          <p class="work-title">Cinematic Short</p>  
        </div>  
      </div>  
  
    </div>  
    <p class="work-note reveal">Replace placeholders with your own images, videos, or project thumbnails</p>  
  </section>  
  
  <!-- ABOUT -->  
  <section id="about">  
    <div class="section-header reveal">  
      <span class="section-num">03</span>  
      <h2>About</h2>  
    </div>  
    <div class="about-grid">  
      <div class="reveal">  
        <div class="about-body">  
          <p>  
            I'm Sujevan Ravikumar — a filmmaker, social media strategist, and content creator with a passion for visual storytelling across every medium.  
          </p>  
          <p>  
            My work sits at the intersection of creative direction and digital strategy. Whether I'm behind a camera crafting a cinematic short, designing a social media campaign to grow a brand, or compositing VFX sequences that push a project further — I bring the same level of care and intention to every frame.  
          </p>  
          <blockquote class="about-pull">  
            "Great content doesn't just look good — it makes people feel something."  
          </blockquote>  
          <p>  
            I believe the best work comes from understanding both the technical craft and the human story behind it. Let's make something worth watching.  
          </p>  
        </div>  
      </div>  
      <div class="skills-block reveal">  
        <div class="skill-row">  
          <span class="skill-name">Videography</span>  
          <div class="skill-bar"><div class="skill-fill" style="width:90%"></div></div>  
          <span class="skill-pct">90</span>  
        </div>  
        <div class="skill-row">  
          <span class="skill-name">Social Media Strategy</span>  
          <div class="skill-bar"><div class="skill-fill" style="width:85%"></div></div>  
          <span class="skill-pct">85</span>  
        </div>  
        <div class="skill-row">  
          <span class="skill-name">Content Creation</span>  
          <div class="skill-bar"><div class="skill-fill" style="width:88%"></div></div>  
          <span class="skill-pct">88</span>  
        </div>  
        <div class="skill-row">  
          <span class="skill-name">VFX & Compositing</span>  
          <div class="skill-bar"><div class="skill-fill" style="width:75%"></div></div>  
          <span class="skill-pct">75</span>  
        </div>  
        <div class="skill-row">  
          <span class="skill-name">Colour Grading</span>  
          <div class="skill-bar"><div class="skill-fill" style="width:80%"></div></div>  
          <span class="skill-pct">80</span>  
        </div>  
        <div class="skill-row">  
          <span class="skill-name">Motion Graphics</span>  
          <div class="skill-bar"><div class="skill-fill" style="width:70%"></div></div>  
          <span class="skill-pct">70</span>  
        </div>  
      </div>  
    </div>  
  </section>  
  
  <!-- CONTACT -->  
  <section id="contact">  
    <div class="contact-inner">  
      <h2 class="contact-heading reveal">Let's create<br>something <em>great.</em></h2>  
      <p class="contact-sub reveal">  
        Whether you have a project in mind or just want to talk — I'm always open to new collaborations, briefs, and conversations.  
      </p>  
      <div class="contact-links reveal">  
        <a href="mailto:hello@sujevan.com" class="btn">Email Me →</a>  
        <a href="#" class="btn btn-outline">Instagram</a>  
        <a href="#" class="btn btn-outline">LinkedIn</a>  
      </div>  
    </div>  
  </section>  
  
  <!-- FOOTER -->  
  <footer>  
    <span>Sujevan Ravikumar</span>  
    <p>© 2026 — All rights reserved</p>  
    <p>Social Media · Film · VFX</p>  
  </footer>  
  
  <script>  
    // Scroll reveal  
    const revealEls = document.querySelectorAll('.reveal');  
    const observer = new IntersectionObserver((entries) => {  
      entries.forEach(entry => {  
        if (entry.isIntersecting) {  
          entry.target.classList.add('visible');  
        }  
      });  
    }, { threshold: 0.12 });  
  
    revealEls.forEach(el => observer.observe(el));  
  </script>  
</body>  
</html>  

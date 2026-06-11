<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>World Scholars Cup 2026 — The Tournament of Champions</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400;1,700&family=DM+Sans:wght@300;400;500;600&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --void: #060412;
    --deep: #0E0A22;
    --cosmos: #150F2E;
    --violet: #7C3AED;
    --violet-light: #A78BFA;
    --violet-glow: rgba(124,58,237,0.18);
    --gold: #F5A623;
    --gold-light: #FFD173;
    --gold-pale: rgba(245,166,35,0.12);
    --mint: #2DFFD4;
    --mint-dim: rgba(45,255,212,0.08);
    --cream: #F0EEF9;
    --cream-dim: rgba(240,238,249,0.65);
    --muted: rgba(240,238,249,0.4);
    --line: rgba(240,238,249,0.08);
  }

  html { scroll-behavior: smooth; }

  body {
    background: var(--void);
    color: var(--cream);
    font-family: 'DM Sans', sans-serif;
    font-weight: 400;
    line-height: 1.7;
    overflow-x: hidden;
  }

  /* ─── NAV ─────────────────────────────────────────── */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    padding: 1.1rem 4rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: rgba(6,4,18,0.7);
    backdrop-filter: blur(14px);
    border-bottom: 1px solid var(--line);
    transition: background 0.3s;
  }

  .nav-logo {
    font-family: 'Space Mono', monospace;
    font-size: 0.78rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--gold);
    text-decoration: none;
  }

  .nav-links {
    display: flex;
    gap: 2.5rem;
    list-style: none;
  }

  .nav-links a {
    font-size: 0.82rem;
    font-weight: 500;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    color: var(--cream-dim);
    text-decoration: none;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--cream); }

  .nav-cta {
    font-family: 'Space Mono', monospace;
    font-size: 0.75rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--gold) !important;
    border: 1px solid rgba(245,166,35,0.4);
    padding: 0.45rem 1.1rem;
    border-radius: 2px;
    transition: all 0.2s !important;
  }
  .nav-cta:hover { background: rgba(245,166,35,0.08) !important; border-color: var(--gold) !important; }

  /* ─── HERO ────────────────────────────────────────── */
  #hero {
    position: relative;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    overflow: hidden;
    padding: 8rem 4rem 6rem;
  }

  #star-canvas {
    position: absolute;
    inset: 0;
    width: 100%;
    height: 100%;
    pointer-events: none;
  }

  .hero-eyebrow {
    font-family: 'Space Mono', monospace;
    font-size: 0.72rem;
    letter-spacing: 0.28em;
    text-transform: uppercase;
    color: var(--mint);
    margin-bottom: 1.8rem;
    position: relative;
    z-index: 2;
    display: flex;
    align-items: center;
    gap: 0.8rem;
  }

  .hero-eyebrow::before,
  .hero-eyebrow::after {
    content: '';
    display: block;
    width: 3rem;
    height: 1px;
    background: var(--mint);
    opacity: 0.5;
  }

  .hero-headline {
    font-family: 'Playfair Display', serif;
    font-size: clamp(3.5rem, 8vw, 8rem);
    font-weight: 900;
    line-height: 1.0;
    text-align: center;
    position: relative;
    z-index: 2;
    max-width: 900px;
    letter-spacing: -0.02em;
  }

  .hero-headline em {
    font-style: italic;
    color: var(--gold);
    display: block;
  }

  .hero-sub {
    font-size: clamp(1rem, 1.6vw, 1.25rem);
    color: var(--cream-dim);
    text-align: center;
    max-width: 560px;
    margin: 2rem auto 0;
    position: relative;
    z-index: 2;
    font-weight: 300;
    line-height: 1.8;
  }

  .hero-actions {
    display: flex;
    gap: 1.2rem;
    margin-top: 3rem;
    position: relative;
    z-index: 2;
  }

  .btn-primary {
    font-family: 'Space Mono', monospace;
    font-size: 0.78rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--void);
    background: var(--gold);
    border: none;
    padding: 1rem 2.2rem;
    border-radius: 2px;
    cursor: pointer;
    text-decoration: none;
    transition: all 0.2s;
    font-weight: 700;
  }
  .btn-primary:hover { background: var(--gold-light); transform: translateY(-2px); }

  .btn-ghost {
    font-family: 'Space Mono', monospace;
    font-size: 0.78rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--cream);
    background: transparent;
    border: 1px solid rgba(240,238,249,0.25);
    padding: 1rem 2.2rem;
    border-radius: 2px;
    cursor: pointer;
    text-decoration: none;
    transition: all 0.2s;
  }
  .btn-ghost:hover { border-color: rgba(240,238,249,0.6); transform: translateY(-2px); }

  .hero-scroll-hint {
    position: absolute;
    bottom: 2.5rem;
    left: 50%;
    transform: translateX(-50%);
    z-index: 2;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0.5rem;
    color: var(--muted);
    font-family: 'Space Mono', monospace;
    font-size: 0.62rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    animation: bounce 2.5s ease-in-out infinite;
  }
  .scroll-arrow { width: 1px; height: 2.5rem; background: linear-gradient(to bottom, var(--muted), transparent); }

  @keyframes bounce {
    0%, 100% { transform: translateX(-50%) translateY(0); }
    50% { transform: translateX(-50%) translateY(8px); }
  }

  /* ─── STATS BAR ───────────────────────────────────── */
  .stats-bar {
    background: var(--cosmos);
    border-top: 1px solid var(--line);
    border-bottom: 1px solid var(--line);
    padding: 2.5rem 4rem;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 0;
  }

  .stat-item {
    text-align: center;
    padding: 1rem 2rem;
    border-right: 1px solid var(--line);
  }
  .stat-item:last-child { border-right: none; }

  .stat-number {
    font-family: 'Playfair Display', serif;
    font-size: 3rem;
    font-weight: 900;
    color: var(--gold);
    line-height: 1;
    letter-spacing: -0.02em;
  }

  .stat-label {
    font-family: 'Space Mono', monospace;
    font-size: 0.68rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--muted);
    margin-top: 0.5rem;
  }

  /* ─── SUBJECTS ────────────────────────────────────── */
  #subjects {
    padding: 8rem 4rem;
    position: relative;
  }

  .section-label {
    font-family: 'Space Mono', monospace;
    font-size: 0.68rem;
    letter-spacing: 0.28em;
    text-transform: uppercase;
    color: var(--violet-light);
    margin-bottom: 1.2rem;
  }

  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2rem, 4vw, 3.5rem);
    font-weight: 700;
    line-height: 1.15;
    max-width: 520px;
    margin-bottom: 1.5rem;
  }

  .section-title span { color: var(--gold); }

  .section-desc {
    color: var(--cream-dim);
    font-size: 1.05rem;
    max-width: 480px;
    margin-bottom: 4rem;
    font-weight: 300;
  }

  .subjects-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1px;
    background: var(--line);
    border: 1px solid var(--line);
  }

  .subject-card {
    background: var(--deep);
    padding: 2.5rem 2rem;
    position: relative;
    overflow: hidden;
    transition: background 0.3s;
    cursor: default;
  }

  .subject-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0;
    width: 3px;
    height: 0;
    background: var(--accent, var(--violet));
    transition: height 0.4s ease;
  }

  .subject-card:hover { background: var(--cosmos); }
  .subject-card:hover::before { height: 100%; }

  .subject-icon {
    font-size: 2.2rem;
    margin-bottom: 1.2rem;
    display: block;
    line-height: 1;
  }

  .subject-name {
    font-family: 'Playfair Display', serif;
    font-size: 1.2rem;
    font-weight: 700;
    margin-bottom: 0.5rem;
    color: var(--cream);
  }

  .subject-theme {
    font-family: 'Space Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--accent, var(--violet-light));
    margin-bottom: 0.8rem;
  }

  .subject-desc {
    font-size: 0.88rem;
    color: var(--cream-dim);
    line-height: 1.65;
  }

  /* ─── THEME SECTION ───────────────────────────────── */
  #theme {
    background: var(--cosmos);
    border-top: 1px solid var(--line);
    border-bottom: 1px solid var(--line);
    padding: 8rem 4rem;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 6rem;
    align-items: center;
  }

  .theme-quote {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.6rem, 3vw, 2.5rem);
    font-weight: 400;
    font-style: italic;
    line-height: 1.4;
    color: var(--cream);
    position: relative;
    padding-left: 2rem;
  }

  .theme-quote::before {
    content: '';
    position: absolute;
    left: 0; top: 0.3em;
    width: 3px;
    height: 80%;
    background: linear-gradient(to bottom, var(--gold), transparent);
  }

  .theme-quote strong {
    color: var(--gold);
    font-style: normal;
    font-weight: 900;
    display: block;
    font-size: 1.3em;
    margin-top: 0.3em;
  }

  .theme-right .section-label { margin-bottom: 1rem; }

  .theme-body {
    font-size: 1rem;
    color: var(--cream-dim);
    line-height: 1.8;
    margin-bottom: 1.5rem;
    font-weight: 300;
  }

  .theme-badge {
    display: inline-block;
    font-family: 'Space Mono', monospace;
    font-size: 0.68rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--mint);
    border: 1px solid rgba(45,255,212,0.3);
    padding: 0.35rem 0.9rem;
    border-radius: 2px;
    margin: 0.2rem;
  }

  /* ─── ROUNDS ──────────────────────────────────────── */
  #rounds {
    padding: 8rem 4rem;
    position: relative;
  }

  .rounds-header {
    text-align: center;
    margin-bottom: 5rem;
  }

  .rounds-header .section-title {
    margin: 0 auto 1rem;
    text-align: center;
  }

  .rounds-header .section-desc {
    margin: 0 auto;
    text-align: center;
  }

  .rounds-timeline {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2rem;
    position: relative;
  }

  .rounds-timeline::before {
    content: '';
    position: absolute;
    top: 3.2rem;
    left: calc(16.67% + 1rem);
    right: calc(16.67% + 1rem);
    height: 1px;
    background: linear-gradient(to right, transparent, var(--violet), var(--gold), var(--violet), transparent);
  }

  .round-card {
    background: var(--deep);
    border: 1px solid var(--line);
    padding: 2.5rem 2rem 2rem;
    position: relative;
    text-align: center;
    transition: border-color 0.3s, transform 0.3s;
  }

  .round-card:hover {
    border-color: rgba(124,58,237,0.4);
    transform: translateY(-4px);
  }

  .round-number {
    font-family: 'Space Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--violet-light);
    margin-bottom: 1rem;
  }

  .round-city {
    font-family: 'Playfair Display', serif;
    font-size: 1.5rem;
    font-weight: 700;
    color: var(--cream);
    margin-bottom: 0.3rem;
  }

  .round-date {
    font-family: 'Space Mono', monospace;
    font-size: 0.68rem;
    color: var(--gold);
    letter-spacing: 0.1em;
    margin-bottom: 1.2rem;
  }

  .round-desc {
    font-size: 0.88rem;
    color: var(--cream-dim);
    line-height: 1.6;
  }

  .round-dot {
    width: 12px;
    height: 12px;
    border-radius: 50%;
    background: var(--violet);
    border: 2px solid var(--deep);
    position: absolute;
    top: -6px;
    left: 50%;
    transform: translateX(-50%);
    box-shadow: 0 0 16px var(--violet);
  }

  .round-card.tournament .round-dot { background: var(--gold); box-shadow: 0 0 16px var(--gold); }

  /* ─── HOW IT WORKS ────────────────────────────────── */
  #how {
    background: var(--cosmos);
    border-top: 1px solid var(--line);
    border-bottom: 1px solid var(--line);
    padding: 8rem 4rem;
  }

  .how-header {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    margin-bottom: 5rem;
    align-items: end;
  }

  .events-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1.5rem;
  }

  .event-card {
    background: var(--deep);
    border: 1px solid var(--line);
    padding: 2rem 1.8rem;
    position: relative;
    overflow: hidden;
    transition: all 0.3s;
  }

  .event-card::after {
    content: '';
    position: absolute;
    bottom: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(to right, var(--violet), var(--gold));
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.4s ease;
  }

  .event-card:hover { border-color: var(--violet-glow); }
  .event-card:hover::after { transform: scaleX(1); }

  .event-letter {
    font-family: 'Playfair Display', serif;
    font-size: 3.5rem;
    font-weight: 900;
    color: rgba(124,58,237,0.18);
    position: absolute;
    top: 1rem;
    right: 1.2rem;
    line-height: 1;
    pointer-events: none;
  }

  .event-name {
    font-family: 'Playfair Display', serif;
    font-size: 1.1rem;
    font-weight: 700;
    color: var(--cream);
    margin-bottom: 0.5rem;
  }

  .event-detail {
    font-size: 0.85rem;
    color: var(--cream-dim);
    line-height: 1.6;
  }

  /* ─── TESTIMONIAL ─────────────────────────────────── */
  #voices {
    padding: 8rem 4rem;
    background: var(--deep);
  }

  .voices-header {
    text-align: center;
    margin-bottom: 4rem;
  }

  .testimonials-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.5rem;
  }

  .testimonial-card {
    background: var(--cosmos);
    border: 1px solid var(--line);
    padding: 2.2rem;
    position: relative;
    transition: border-color 0.3s;
  }

  .testimonial-card:hover { border-color: rgba(245,166,35,0.25); }

  .quote-mark {
    font-family: 'Playfair Display', serif;
    font-size: 4rem;
    color: var(--gold);
    opacity: 0.3;
    line-height: 0.8;
    margin-bottom: 1rem;
    display: block;
  }

  .testimonial-text {
    font-size: 0.95rem;
    color: var(--cream-dim);
    line-height: 1.75;
    margin-bottom: 1.5rem;
    font-style: italic;
  }

  .testimonial-author {
    display: flex;
    align-items: center;
    gap: 0.8rem;
  }

  .author-avatar {
    width: 38px;
    height: 38px;
    border-radius: 50%;
    background: var(--violet-glow);
    border: 1px solid rgba(124,58,237,0.3);
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Space Mono', monospace;
    font-size: 0.7rem;
    color: var(--violet-light);
    font-weight: 700;
  }

  .author-name {
    font-weight: 600;
    font-size: 0.88rem;
    color: var(--cream);
    line-height: 1.3;
  }

  .author-school {
    font-family: 'Space Mono', monospace;
    font-size: 0.62rem;
    color: var(--muted);
    letter-spacing: 0.06em;
  }

  /* ─── REGISTER ────────────────────────────────────── */
  #register {
    background: var(--cosmos);
    border-top: 1px solid var(--line);
    padding: 10rem 4rem;
    text-align: center;
    position: relative;
    overflow: hidden;
  }

  #register::before {
    content: '';
    position: absolute;
    top: 50%; left: 50%;
    transform: translate(-50%, -50%);
    width: 600px;
    height: 600px;
    background: radial-gradient(circle, rgba(124,58,237,0.12) 0%, transparent 70%);
    pointer-events: none;
  }

  .register-headline {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.5rem, 5vw, 5rem);
    font-weight: 900;
    line-height: 1.1;
    margin-bottom: 1.5rem;
    position: relative;
    z-index: 1;
  }

  .register-headline .accent { color: var(--gold); }

  .register-sub {
    font-size: 1.1rem;
    color: var(--cream-dim);
    max-width: 500px;
    margin: 0 auto 3rem;
    font-weight: 300;
    line-height: 1.8;
    position: relative;
    z-index: 1;
  }

  .register-actions {
    display: flex;
    gap: 1.2rem;
    justify-content: center;
    flex-wrap: wrap;
    position: relative;
    z-index: 1;
  }

  .register-note {
    margin-top: 2rem;
    font-family: 'Space Mono', monospace;
    font-size: 0.68rem;
    letter-spacing: 0.1em;
    color: var(--muted);
    position: relative;
    z-index: 1;
  }

  /* ─── FOOTER ──────────────────────────────────────── */
  footer {
    background: var(--void);
    border-top: 1px solid var(--line);
    padding: 3rem 4rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .footer-logo {
    font-family: 'Space Mono', monospace;
    font-size: 0.72rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--gold);
  }

  .footer-links {
    display: flex;
    gap: 2rem;
    list-style: none;
  }

  .footer-links a {
    font-size: 0.8rem;
    color: var(--muted);
    text-decoration: none;
    transition: color 0.2s;
  }
  .footer-links a:hover { color: var(--cream); }

  .footer-copy {
    font-family: 'Space Mono', monospace;
    font-size: 0.62rem;
    color: var(--muted);
    letter-spacing: 0.08em;
  }

  /* ─── SCROLL REVEAL ───────────────────────────────── */
  .reveal {
    opacity: 0;
    transform: translateY(28px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }
  .reveal.visible {
    opacity: 1;
    transform: translateY(0);
  }
  .reveal-delay-1 { transition-delay: 0.1s; }
  .reveal-delay-2 { transition-delay: 0.2s; }
  .reveal-delay-3 { transition-delay: 0.3s; }
  .reveal-delay-4 { transition-delay: 0.4s; }

  @media (prefers-reduced-motion: reduce) {
    .reveal { opacity: 1; transform: none; }
    * { transition-duration: 0.01ms !important; animation-duration: 0.01ms !important; }
  }

  @media (max-width: 900px) {
    nav { padding: 1rem 1.5rem; }
    .nav-links { display: none; }
    #hero, #subjects, #rounds, #how, #voices, #register, footer { padding-left: 1.5rem; padding-right: 1.5rem; }
    .stats-bar { grid-template-columns: repeat(2, 1fr); padding: 2rem 1.5rem; }
    .stat-item { border-right: none; border-bottom: 1px solid var(--line); }
    .stat-item:last-child, .stat-item:nth-child(2) { border-right: none; }
    .subjects-grid, .testimonials-grid { grid-template-columns: 1fr; }
    .rounds-timeline { grid-template-columns: 1fr; }
    .rounds-timeline::before { display: none; }
    #theme, .how-header { grid-template-columns: 1fr; gap: 3rem; }
    .events-grid { grid-template-columns: 1fr; }
    footer { flex-direction: column; gap: 1.5rem; text-align: center; }
    .footer-links { flex-wrap: wrap; justify-content: center; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a class="nav-logo" href="#hero">WSC // 2026</a>
  <ul class="nav-links">
    <li><a href="#subjects">Subjects</a></li>
    <li><a href="#rounds">Rounds</a></li>
    <li><a href="#how">Events</a></li>
    <li><a href="#voices">Voices</a></li>
    <li><a href="#register" class="nav-cta">Register</a></li>
  </ul>
</nav>

<!-- HERO -->
<section id="hero">
  <canvas id="star-canvas" aria-hidden="true"></canvas>

  <p class="hero-eyebrow">World Scholars Cup · Est. 2005</p>

  <h1 class="hero-headline">
    Where Ideas<br>
    <em>Change Everything</em>
  </h1>

  <p class="hero-sub">
    The global academic competition that challenges young scholars to think across disciplines, debate boldly, and discover the joy of learning.
  </p>

  <div class="hero-actions">
    <a href="#register" class="btn-primary">Register Your Team</a>
    <a href="#subjects" class="btn-ghost">Explore 2026 Theme</a>
  </div>

  <div class="hero-scroll-hint" aria-hidden="true">
    Scroll
    <div class="scroll-arrow"></div>
  </div>
</section>

<!-- STATS BAR -->
<div class="stats-bar">
  <div class="stat-item reveal">
    <div class="stat-number">80+</div>
    <div class="stat-label">Countries Represented</div>
  </div>
  <div class="stat-item reveal reveal-delay-1">
    <div class="stat-number">30K+</div>
    <div class="stat-label">Scholars Per Season</div>
  </div>
  <div class="stat-item reveal reveal-delay-2">
    <div class="stat-number">6</div>
    <div class="stat-label">Academic Subjects</div>
  </div>
  <div class="stat-item reveal reveal-delay-3">
    <div class="stat-number">20</div>
    <div class="stat-label">Years of Wonder</div>
  </div>
</div>

<!-- SUBJECTS -->
<section id="subjects">
  <div class="reveal">
    <p class="section-label">The Curriculum</p>
    <h2 class="section-title">Six Fields.<br><span>Infinite Questions.</span></h2>
    <p class="section-desc">Every year, six subjects explore a unifying theme through essays, debates, and collaborative scholarship.</p>
  </div>

  <div class="subjects-grid">
    <div class="subject-card reveal" style="--accent: #7C3AED;">
      <span class="subject-icon">🌍</span>
      <div class="subject-name">Social Studies</div>
      <div class="subject-theme" style="color: #A78BFA;">Power & Civilization</div>
      <p class="subject-desc">How societies organize, rise, fall, and reimagine themselves. From ancient empires to algorithmic governance — the human experiment in motion.</p>
    </div>
    <div class="subject-card reveal reveal-delay-1" style="--accent: #F5A623;">
      <span class="subject-icon">🔬</span>
      <div class="subject-name">Science & Technology</div>
      <div class="subject-theme" style="color: #FFD173;">Discovery & Ethics</div>
      <p class="subject-desc">The frontier where curiosity meets consequence. Explore the ideas reshaping biology, physics, and the machines we build in our own image.</p>
    </div>
    <div class="subject-card reveal reveal-delay-2" style="--accent: #2DFFD4;">
      <span class="subject-icon">📖</span>
      <div class="subject-name">Literature & Media</div>
      <div class="subject-theme" style="color: #2DFFD4;">Story & Meaning</div>
      <p class="subject-desc">What stories reveal about us. From ancient myth to streaming algorithms — how narrative constructs truth, identity, and empire.</p>
    </div>
    <div class="subject-card reveal" style="--accent: #EF4444;">
      <span class="subject-icon">🎭</span>
      <div class="subject-name">Art & Music</div>
      <div class="subject-theme" style="color: #FCA5A5;">Expression & Revolution</div>
      <p class="subject-desc">The movements that shook culture and the masterworks that survived them. Aesthetics as a form of argument — beauty as a kind of proof.</p>
    </div>
    <div class="subject-card reveal reveal-delay-1" style="--accent: #22D3EE;">
      <span class="subject-icon">💬</span>
      <div class="subject-name">Special Area</div>
      <div class="subject-theme" style="color: #67E8F9;">2026 Theme: The Impossible</div>
      <p class="subject-desc">The annual wildcard that binds all six subjects. This year scholars examine what it means to attempt the undoable — and why humans can't stop trying.</p>
    </div>
    <div class="subject-card reveal reveal-delay-2" style="--accent: #A3E635;">
      <span class="subject-icon">🧠</span>
      <div class="subject-name">Ethics & Philosophy</div>
      <div class="subject-theme" style="color: #BEF264;">Reason & Action</div>
      <p class="subject-desc">The hardest questions dressed in the lightest language. Thought experiments, moral paradoxes, and the stubborn wisdom of the examined life.</p>
    </div>
  </div>
</section>

<!-- THEME -->
<section id="theme">
  <div class="theme-left reveal">
    <blockquote class="theme-quote">
      "The reasonable man adapts himself to the world.
      <strong>The unreasonable one persists. So all progress depends on the unreasonable man."</strong>
    </blockquote>
    <p style="margin-top: 1.5rem; font-family: 'Space Mono', monospace; font-size: 0.68rem; letter-spacing: 0.1em; color: var(--muted);">— George Bernard Shaw</p>
  </div>
  <div class="theme-right reveal reveal-delay-2">
    <p class="section-label">2026 Annual Theme</p>
    <h2 class="section-title" style="max-width: 100%;">The <span>Impossible</span></h2>
    <p class="theme-body">
      This season, scholars across every discipline explore ideas, events, artworks, and inventions that were once declared impossible — and the audacious minds that proved otherwise.
    </p>
    <p class="theme-body">
      From double helixes to democratic revolutions, from sonatas that broke the rules to theorems that broke reality — the impossible has always been where the interesting begins.
    </p>
    <div>
      <span class="theme-badge">Heavier than Air Flight</span>
      <span class="theme-badge">Gödel's Incompleteness</span>
      <span class="theme-badge">The Paris Commune</span>
      <span class="theme-badge">DNA Synthesis</span>
      <span class="theme-badge">Quantum Entanglement</span>
    </div>
  </div>
</section>

<!-- ROUNDS -->
<section id="rounds">
  <div class="rounds-header reveal">
    <p class="section-label">The Journey</p>
    <h2 class="section-title">From Local to Global</h2>
    <p class="section-desc">Three rounds bring scholars from their home cities to the global stage. Each level raises the stakes — and the conversation.</p>
  </div>

  <div class="rounds-timeline">
    <div class="round-card reveal">
      <div class="round-dot"></div>
      <p class="round-number">Round I</p>
      <div class="round-city">Regional</div>
      <div class="round-date">February – April 2026</div>
      <p class="round-desc">Dozens of regional bowls held across six continents. Your first test — ace the Scholar's Challenge, debate a live motion, and write under pressure.</p>
    </div>
    <div class="round-card reveal reveal-delay-1">
      <div class="round-dot"></div>
      <p class="round-number">Round II</p>
      <div class="round-city">National</div>
      <div class="round-date">May – June 2026</div>
      <p class="round-desc">Top regional teams advance to their national bowl. Scores accumulate. Reputations form. The field narrows, and the debates grow fiercer.</p>
    </div>
    <div class="round-card tournament reveal reveal-delay-2">
      <div class="round-dot"></div>
      <p class="round-number">Round III · Final</p>
      <div class="round-city">Barcelona</div>
      <div class="round-date">November 2026</div>
      <p class="round-desc">The Tournament of Champions. 150+ teams. One city. The World Scholars Cup crowns its global finalists among the most rigorous academic competition on earth.</p>
    </div>
  </div>
</section>

<!-- HOW IT WORKS -->
<section id="how">
  <div class="how-header">
    <div class="reveal">
      <p class="section-label">The Events</p>
      <h2 class="section-title" style="max-width: 100%;">What Scholars <span>Actually Do</span></h2>
    </div>
    <div class="reveal reveal-delay-1">
      <p style="color: var(--cream-dim); font-size: 1rem; font-weight: 300; line-height: 1.8;">
        Four distinct events test different modes of thinking — no single event determines a team's fate. Every scholar competes individually and as part of their three-person team.
      </p>
    </div>
  </div>

  <div class="events-grid">
    <div class="event-card reveal">
      <span class="event-letter" aria-hidden="true">S</span>
      <div class="event-name">Scholar's Challenge</div>
      <p class="event-detail">A rapid-fire individual quiz spanning all six subjects. Tests breadth of knowledge, speed of recall, and the ability to connect ideas across disciplines. Scores stack for the team.</p>
    </div>
    <div class="event-card reveal reveal-delay-1">
      <span class="event-letter" aria-hidden="true">D</span>
      <div class="event-name">Collaborative Writing</div>
      <p class="event-detail">Teams write two essays together under timed conditions — one persuasive, one analytical. No notes. No internet. Just three minds and a shared argument.</p>
    </div>
    <div class="event-card reveal reveal-delay-2">
      <span class="event-letter" aria-hidden="true">D</span>
      <div class="event-name">Team Debate</div>
      <p class="event-detail">Oxford-style format. Motions are drawn from the annual theme. Scholars prepare arguments for and against each motion, with live speaker assignment at the round. Wit required.</p>
    </div>
    <div class="event-card reveal reveal-delay-3">
      <span class="event-letter" aria-hidden="true">B</span>
      <div class="event-name">Team Bowl</div>
      <p class="event-detail">Three scholars buzz in as a unit. Category questions cover all subjects, with a unique cooperative twist — teams can confer, argue, and change their answer once per question.</p>
    </div>
  </div>
</section>

<!-- TESTIMONIALS -->
<section id="voices">
  <div class="voices-header reveal">
    <p class="section-label">From the Field</p>
    <h2 class="section-title" style="margin: 0 auto 0.5rem; text-align: center;">Scholars Speak</h2>
    <p class="section-desc" style="margin: 0 auto; text-align: center;">The competition ends. The thinking doesn't.</p>
  </div>

  <div class="testimonials-grid">
    <div class="testimonial-card reveal">
      <span class="quote-mark" aria-hidden="true">"</span>
      <p class="testimonial-text">I came expecting a quiz competition. I left debating the epistemology of scientific models with a student from Singapore at 2am. WSC rewired how I think about learning itself.</p>
      <div class="testimonial-author">
        <div class="author-avatar">AK</div>
        <div>
          <div class="author-name">Ayaan Karim</div>
          <div class="author-school">Dubai, UAE · 2024 Gold Division</div>
        </div>
      </div>
    </div>
    <div class="testimonial-card reveal reveal-delay-1">
      <span class="quote-mark" aria-hidden="true">"</span>
      <p class="testimonial-text">Our team barely knew each other before regionals. After Barcelona, we'd co-authored eight essays, argued across every subject, and somehow became best friends. WSC does that.</p>
      <div class="testimonial-author">
        <div class="author-avatar">MV</div>
        <div>
          <div class="author-name">Mia Václavová</div>
          <div class="author-school">Prague, Czech Republic · 2025</div>
        </div>
      </div>
    </div>
    <div class="testimonial-card reveal reveal-delay-2">
      <span class="quote-mark" aria-hidden="true">"</span>
      <p class="testimonial-text">The essay prompts don't have right answers. That's what makes them terrifying and thrilling. You learn to commit to an argument under conditions that make you sharper.</p>
      <div class="testimonial-author">
        <div class="author-avatar">JT</div>
        <div>
          <div class="author-name">Joel Tanaka</div>
          <div class="author-school">Osaka, Japan · Coach, 3 Seasons</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- REGISTER CTA -->
<section id="register">
  <h2 class="register-headline reveal">
    Your Team.<br>Your <span class="accent">Ideas.</span><br>The World.
  </h2>
  <p class="register-sub reveal reveal-delay-1">
    Registration for the 2026 season is open now. Teams of three scholars, grades 6–12. All levels of experience welcome.
  </p>
  <div class="register-actions reveal reveal-delay-2">
    <a href="#" class="btn-primary">Register a Team</a>
    <a href="#" class="btn-ghost">Download Info Pack</a>
  </div>
  <p class="register-note reveal reveal-delay-3">
    Questions? · scholars@worldscholarscup.com · Individual scholar placement available
  </p>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo">World Scholars Cup</div>
  <ul class="footer-links">
    <li><a href="#">About WSC</a></li>
    <li><a href="#">Past Themes</a></li>
    <li><a href="#">Scoring Guide</a></li>
    <li><a href="#">Volunteers</a></li>
    <li><a href="#">Press</a></li>
  </ul>
  <div class="footer-copy">© 2026 World Scholars Cup. All Rights Reserved.</div>
</footer>

<script>
  /* ── STAR CONSTELLATION CANVAS ── */
  (function() {
    const canvas = document.getElementById('star-canvas');
    const ctx = canvas.getContext('2d');

    const SUBJECTS = [
      { label: 'Social Studies', x: 0.18, y: 0.28, color: '#A78BFA', size: 2.5 },
      { label: 'Science', x: 0.38, y: 0.18, color: '#67E8F9', size: 2 },
      { label: 'Literature', x: 0.62, y: 0.22, color: '#2DFFD4', size: 2.5 },
      { label: 'Art & Music', x: 0.78, y: 0.38, color: '#F5A623', size: 2 },
      { label: 'Special Area', x: 0.5, y: 0.42, color: '#F5A623', size: 3.5 },
      { label: 'Ethics', x: 0.25, y: 0.6, color: '#BEF264', size: 2 },
      { label: 'Philosophy', x: 0.72, y: 0.65, color: '#FCA5A5', size: 1.8 },
    ];

    const CONNECTIONS = [
      [0, 1], [1, 2], [2, 3], [3, 4], [4, 5], [5, 0],
      [4, 6], [1, 4], [2, 4], [0, 5], [3, 6]
    ];

    let stars = [];
    let W, H;

    function resize() {
      W = canvas.offsetWidth;
      H = canvas.offsetHeight;
      canvas.width = W;
      canvas.height = H;
    }

    function initStars() {
      stars = [];
      const count = Math.floor((W * H) / 4800);
      for (let i = 0; i < count; i++) {
        stars.push({
          x: Math.random() * W,
          y: Math.random() * H,
          r: Math.random() * 1.2 + 0.2,
          alpha: Math.random() * 0.6 + 0.1,
          twinkleSpeed: Math.random() * 0.015 + 0.003,
          twinkleOffset: Math.random() * Math.PI * 2
        });
      }
    }

    let t = 0;

    function draw() {
      ctx.clearRect(0, 0, W, H);

      /* background vignette */
      const vg = ctx.createRadialGradient(W * 0.5, H * 0.42, 0, W * 0.5, H * 0.5, W * 0.7);
      vg.addColorStop(0, 'rgba(21,15,46,0.0)');
      vg.addColorStop(1, 'rgba(6,4,18,0.5)');
      ctx.fillStyle = vg;
      ctx.fillRect(0, 0, W, H);

      /* background stars */
      for (const s of stars) {
        const alpha = s.alpha * (0.6 + 0.4 * Math.sin(t * s.twinkleSpeed + s.twinkleOffset));
        ctx.beginPath();
        ctx.arc(s.x, s.y, s.r, 0, Math.PI * 2);
        ctx.fillStyle = `rgba(240,238,249,${alpha})`;
        ctx.fill();
      }

      /* constellation lines */
      for (const [a, b] of CONNECTIONS) {
        const sa = SUBJECTS[a], sb = SUBJECTS[b];
        const ax = sa.x * W, ay = sa.y * H;
        const bx = sb.x * W, by = sb.y * H;
        const pulse = 0.08 + 0.04 * Math.sin(t * 0.008 + a);
        ctx.beginPath();
        ctx.moveTo(ax, ay);
        ctx.lineTo(bx, by);
        ctx.strokeStyle = `rgba(124,58,237,${pulse})`;
        ctx.lineWidth = 1;
        ctx.stroke();
      }

      /* subject nodes */
      for (const s of SUBJECTS) {
        const x = s.x * W, y = s.y * H;
        const twinkle = 0.75 + 0.25 * Math.sin(t * 0.012 + s.x * 8);
        const r = s.size * twinkle;

        /* glow */
        const grd = ctx.createRadialGradient(x, y, 0, x, y, r * 7);
        grd.addColorStop(0, s.color + '40');
        grd.addColorStop(1, s.color + '00');
        ctx.beginPath();
        ctx.arc(x, y, r * 7, 0, Math.PI * 2);
        ctx.fillStyle = grd;
        ctx.fill();

        /* core */
        ctx.beginPath();
        ctx.arc(x, y, r, 0, Math.PI * 2);
        ctx.fillStyle = s.color;
        ctx.fill();

        /* label */
        if (W > 600) {
          ctx.font = '500 11px "DM Sans", sans-serif';
          ctx.fillStyle = 'rgba(240,238,249,0.45)';
          ctx.textAlign = x < W * 0.5 ? 'right' : 'left';
          const offset = x < W * 0.5 ? -12 : 12;
          ctx.fillText(s.label, x + offset, y + 4);
        }
      }

      t++;
      requestAnimationFrame(draw);
    }

    window.addEventListener('resize', () => { resize(); initStars(); });
    resize();
    initStars();
    draw();
  })();

  /* ── SCROLL REVEAL ── */
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
  }, { threshold: 0.12 });
  document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
</script>
</body>
</html>

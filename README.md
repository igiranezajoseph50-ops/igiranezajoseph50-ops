<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Legacia – GitHub Profile README Preview</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Share+Tech+Mono&family=Rajdhani:wght@300;400;600&display=swap');

  :root {
    --bg: #020510;
    --panel: #050d1f;
    --border: #0ff3;
    --cyan: #00f5ff;
    --blue: #0057ff;
    --magenta: #ff00c8;
    --glow-cyan: 0 0 8px #00f5ff, 0 0 24px #00f5ff55;
    --glow-mag: 0 0 8px #ff00c8, 0 0 24px #ff00c855;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    background: var(--bg);
    color: #cce8ff;
    font-family: 'Rajdhani', sans-serif;
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* Animated starfield */
  body::before {
    content: '';
    position: fixed; inset: 0;
    background-image:
      radial-gradient(1px 1px at 10% 20%, #fff8, transparent),
      radial-gradient(1px 1px at 30% 60%, #fff6, transparent),
      radial-gradient(1px 1px at 55% 10%, #fff9, transparent),
      radial-gradient(1px 1px at 75% 80%, #fff5, transparent),
      radial-gradient(1px 1px at 90% 40%, #fff7, transparent),
      radial-gradient(1px 1px at 20% 90%, #fff6, transparent),
      radial-gradient(1px 1px at 65% 50%, #fff4, transparent),
      radial-gradient(1px 1px at 85% 15%, #fff8, transparent),
      radial-gradient(1px 1px at 42% 75%, #fff5, transparent),
      radial-gradient(1px 1px at 5%  50%, #fff7, transparent);
    pointer-events: none; z-index: 0;
    animation: twinkle 4s infinite alternate;
  }
  @keyframes twinkle { from { opacity:.6 } to { opacity:1 } }

  /* Scan-line overlay */
  body::after {
    content: '';
    position: fixed; inset: 0;
    background: repeating-linear-gradient(to bottom, transparent, transparent 2px, rgba(0,0,0,.08) 2px, rgba(0,0,0,.08) 4px);
    pointer-events: none; z-index: 1;
  }

  .readme {
    position: relative; z-index: 2;
    max-width: 860px;
    margin: 0 auto;
    padding: 40px 24px 80px;
  }

  /* ─── HERO ─── */
  .hero {
    position: relative;
    text-align: center;
    padding: 60px 0 40px;
    border-bottom: 1px solid var(--border);
    margin-bottom: 48px;
    overflow: hidden;
  }

  .hero-grid {
    position: absolute; inset: 0;
    background-image:
      linear-gradient(rgba(0,245,255,.06) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,245,255,.06) 1px, transparent 1px);
    background-size: 40px 40px;
    mask-image: radial-gradient(ellipse 80% 100% at 50% 50%, black 30%, transparent 100%);
  }

  .hero-badge {
    display: inline-block;
    font-family: 'Share Tech Mono', monospace;
    font-size: 11px;
    letter-spacing: 4px;
    color: var(--cyan);
    border: 1px solid var(--cyan);
    padding: 4px 14px;
    margin-bottom: 20px;
    text-transform: uppercase;
    box-shadow: var(--glow-cyan);
    animation: pulse-badge 3s infinite;
  }
  @keyframes pulse-badge {
    0%,100% { box-shadow: var(--glow-cyan) }
    50% { box-shadow: 0 0 4px #00f5ff, 0 0 12px #00f5ff44 }
  }

  .hero-name {
    font-family: 'Orbitron', monospace;
    font-size: clamp(42px, 8vw, 80px);
    font-weight: 900;
    letter-spacing: 6px;
    line-height: 1;
    background: linear-gradient(135deg, #00f5ff 0%, #fff 45%, #ff00c8 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    filter: drop-shadow(0 0 20px #00f5ff66);
    animation: name-flicker 8s infinite;
  }
  @keyframes name-flicker {
    0%,95%,100% { opacity:1 }
    96% { opacity:.85 }
    97% { opacity:1 }
    98% { opacity:.9 }
  }

  .hero-sub {
    font-family: 'Share Tech Mono', monospace;
    font-size: 13px;
    letter-spacing: 3px;
    color: var(--magenta);
    margin-top: 14px;
    text-shadow: var(--glow-mag);
  }

  .hero-tagline {
    font-size: 16px;
    color: #88aacc;
    margin-top: 20px;
    max-width: 560px;
    margin-left: auto; margin-right: auto;
    line-height: 1.7;
  }

  .hero-tagline span {
    color: var(--cyan);
    font-weight: 600;
  }

  /* Typing cursor */
  .cursor {
    display: inline-block;
    width: 2px; height: 1em;
    background: var(--cyan);
    margin-left: 3px;
    vertical-align: text-bottom;
    animation: blink .7s step-end infinite;
  }
  @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0} }

  /* ─── SECTION ─── */
  .section {
    margin-bottom: 52px;
    animation: fadeUp .6s both;
  }
  @keyframes fadeUp {
    from { opacity:0; transform:translateY(20px) }
    to   { opacity:1; transform:translateY(0) }
  }

  .section-header {
    display: flex;
    align-items: center;
    gap: 12px;
    margin-bottom: 24px;
  }

  .section-line {
    flex: 1;
    height: 1px;
    background: linear-gradient(to right, var(--cyan), transparent);
  }

  .section-title {
    font-family: 'Orbitron', monospace;
    font-size: 13px;
    font-weight: 700;
    letter-spacing: 4px;
    color: var(--cyan);
    text-transform: uppercase;
    white-space: nowrap;
  }

  .section-num {
    font-family: 'Share Tech Mono', monospace;
    font-size: 11px;
    color: var(--magenta);
  }

  /* ─── PROJECTS GRID ─── */
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
    gap: 16px;
  }

  .project-card {
    position: relative;
    background: var(--panel);
    border: 1px solid transparent;
    padding: 22px 20px 18px;
    cursor: default;
    overflow: hidden;
    transition: transform .25s, box-shadow .25s;
  }

  .project-card::before {
    content: '';
    position: absolute; inset: 0;
    border: 1px solid transparent;
    background: linear-gradient(135deg, #00f5ff22, #ff00c811, transparent 60%) border-box;
    -webkit-mask: linear-gradient(#fff 0 0) padding-box, linear-gradient(#fff 0 0);
    -webkit-mask-composite: destination-out;
    mask-composite: exclude;
    transition: opacity .3s;
  }

  .project-card::after {
    content: '';
    position: absolute;
    top: 0; left: -60%;
    width: 40%; height: 100%;
    background: linear-gradient(90deg, transparent, rgba(0,245,255,.08), transparent);
    transform: skewX(-20deg);
    transition: left .5s;
  }

  .project-card:hover { transform: translateY(-4px); box-shadow: 0 8px 32px rgba(0,245,255,.15); }
  .project-card:hover::after { left: 140%; }

  /* Corner decorations */
  .project-card .corner {
    position: absolute;
    width: 8px; height: 8px;
    border-color: var(--cyan);
    border-style: solid;
  }
  .corner.tl { top: 0; left: 0; border-width: 1px 0 0 1px; }
  .corner.tr { top: 0; right: 0; border-width: 1px 1px 0 0; }
  .corner.bl { bottom: 0; left: 0; border-width: 0 0 1px 1px; }
  .corner.br { bottom: 0; right: 0; border-width: 0 1px 1px 0; }

  .project-lang {
    font-family: 'Share Tech Mono', monospace;
    font-size: 10px;
    letter-spacing: 2px;
    color: var(--magenta);
    text-transform: uppercase;
    margin-bottom: 8px;
  }

  .project-name {
    font-family: 'Orbitron', monospace;
    font-size: 13px;
    font-weight: 700;
    color: #e0f4ff;
    margin-bottom: 10px;
    word-break: break-word;
  }

  .project-desc {
    font-size: 13px;
    line-height: 1.6;
    color: #6699aa;
  }

  .project-tag {
    display: inline-block;
    margin-top: 12px;
    font-family: 'Share Tech Mono', monospace;
    font-size: 10px;
    color: var(--cyan);
    border: 1px solid #00f5ff33;
    padding: 2px 8px;
  }

  /* ─── STATS BAR ─── */
  .stat-row {
    display: flex;
    gap: 2px;
    margin-bottom: 24px;
    flex-wrap: wrap;
  }

  .stat-item {
    flex: 1 1 120px;
    background: var(--panel);
    border: 1px solid #0ff1;
    padding: 18px 16px;
    position: relative;
    overflow: hidden;
  }
  .stat-item::before {
    content: '';
    position: absolute; bottom: 0; left: 0;
    height: 2px;
    background: linear-gradient(to right, var(--cyan), var(--magenta));
  }

  .stat-val {
    font-family: 'Orbitron', monospace;
    font-size: 28px;
    font-weight: 900;
    color: var(--cyan);
    text-shadow: var(--glow-cyan);
    line-height: 1;
  }

  .stat-label {
    font-family: 'Share Tech Mono', monospace;
    font-size: 10px;
    letter-spacing: 2px;
    color: #445566;
    margin-top: 6px;
    text-transform: uppercase;
  }

  /* ─── CONNECT ─── */
  .connect-row {
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
  }

  .connect-btn {
    font-family: 'Share Tech Mono', monospace;
    font-size: 12px;
    letter-spacing: 2px;
    color: var(--cyan);
    border: 1px solid #00f5ff55;
    padding: 10px 20px;
    text-decoration: none;
    position: relative;
    overflow: hidden;
    transition: color .2s, border-color .2s, box-shadow .2s;
    display: inline-block;
  }

  .connect-btn:hover {
    color: var(--bg);
    border-color: var(--cyan);
    box-shadow: var(--glow-cyan);
    background: var(--cyan);
  }

  /* ─── FOOTER ─── */
  .footer {
    text-align: center;
    margin-top: 64px;
    padding-top: 24px;
    border-top: 1px solid #0ff1;
  }

  .footer-text {
    font-family: 'Share Tech Mono', monospace;
    font-size: 11px;
    letter-spacing: 3px;
    color: #334455;
  }

  /* ─── ANIMATED BORDER (hero) ─── */
  .animated-line {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 8px;
    margin-top: 32px;
  }
  .anim-segment {
    height: 1px;
    background: linear-gradient(to right, transparent, var(--cyan), transparent);
    animation: grow 2s ease-in-out infinite alternate;
  }
  .anim-segment:nth-child(1) { width: 80px; animation-delay: 0s; }
  .anim-segment:nth-child(3) { width: 80px; animation-delay: .4s; }
  @keyframes grow { from { opacity:.3; transform: scaleX(.5) } to { opacity:1; transform: scaleX(1) } }
  .anim-diamond {
    width: 6px; height: 6px;
    background: var(--magenta);
    transform: rotate(45deg);
    box-shadow: var(--glow-mag);
    animation: pulse-diamond 2s infinite;
  }
  @keyframes pulse-diamond { 0%,100%{transform:rotate(45deg) scale(1)} 50%{transform:rotate(45deg) scale(1.4)} }

  /* README code box */
  .readme-box {
    background: #020a14;
    border: 1px solid #0ff2;
    padding: 24px;
    margin-bottom: 24px;
    position: relative;
  }
  .readme-box-label {
    position: absolute;
    top: -10px; left: 16px;
    font-family: 'Share Tech Mono', monospace;
    font-size: 10px;
    letter-spacing: 2px;
    background: var(--bg);
    padding: 0 8px;
    color: var(--magenta);
  }
  pre {
    font-family: 'Share Tech Mono', monospace;
    font-size: 12px;
    color: #88aacc;
    white-space: pre-wrap;
    word-break: break-all;
    line-height: 1.8;
  }
  pre .k { color: var(--cyan); }
  pre .v { color: var(--magenta); }
  pre .c { color: #334455; }

  /* Section stagger */
  .section:nth-child(1) { animation-delay: .1s }
  .section:nth-child(2) { animation-delay: .2s }
  .section:nth-child(3) { animation-delay: .3s }
  .section:nth-child(4) { animation-delay: .4s }
  .section:nth-child(5) { animation-delay: .5s }
</style>
</head>
<body>
<div class="readme">

  <!-- HERO -->
  <div class="hero">
    <div class="hero-grid"></div>
    <div class="hero-badge">// INITIALIZING PROFILE //</div>
    <h1 class="hero-name">LEGACIA</h1>
    <div class="hero-sub">@igiranezajoseph50-ops</div>
    <p class="hero-tagline">
      Building <span>tomorrow's web</span> from today's code.<br>
      Front-end architect. Creative technologist. <span>Digital craftsman.</span><span class="cursor"></span>
    </p>
    <div class="animated-line">
      <div class="anim-segment"></div>
      <div class="anim-diamond"></div>
      <div class="anim-segment"></div>
    </div>
  </div>

  <!-- STATS -->
  <div class="section">
    <div class="section-header">
      <span class="section-num">01</span>
      <span class="section-title">System Metrics</span>
      <div class="section-line"></div>
    </div>
    <div class="stat-row">
      <div class="stat-item">
        <div class="stat-val">6</div>
        <div class="stat-label">Repositories</div>
      </div>
      <div class="stat-item">
        <div class="stat-val">17</div>
        <div class="stat-label">Contributions</div>
      </div>
      <div class="stat-item">
        <div class="stat-val">3+</div>
        <div class="stat-label">Tech Stack</div>
      </div>
      <div class="stat-item">
        <div class="stat-val">∞</div>
        <div class="stat-label">Vision</div>
      </div>
    </div>
  </div>

  <!-- PROJECTS -->
  <div class="section">
    <div class="section-header">
      <span class="section-num">02</span>
      <span class="section-title">Active Projects</span>
      <div class="section-line"></div>
    </div>
    <div class="projects-grid">

      <div class="project-card">
        <div class="corner tl"></div><div class="corner tr"></div>
        <div class="corner bl"></div><div class="corner br"></div>
        <div class="project-lang">HTML</div>
        <div class="project-name">3D-LANDING-PAGE</div>
        <div class="project-desc">Immersive 3D landing experience built entirely in the browser.</div>
        <div class="project-tag">LIVE PROJECT</div>
      </div>

      <div class="project-card">
        <div class="corner tl"></div><div class="corner tr"></div>
        <div class="corner bl"></div><div class="corner br"></div>
        <div class="project-lang">HTML</div>
        <div class="project-name">EMPOWERING FUTURE THROUGH INTELLIGENCE</div>
        <div class="project-desc">A bold vision for AI-powered education and human potential.</div>
        <div class="project-tag">FLAGSHIP</div>
      </div>

      <div class="project-card">
        <div class="corner tl"></div><div class="corner tr"></div>
        <div class="corner bl"></div><div class="corner br"></div>
        <div class="project-lang">HTML</div>
        <div class="project-name">YOUTUBE</div>
        <div class="project-desc">Custom YouTube interface rebuild with a modern twist.</div>
        <div class="project-tag">UI CLONE</div>
      </div>

      <div class="project-card">
        <div class="corner tl"></div><div class="corner tr"></div>
        <div class="corner bl"></div><div class="corner br"></div>
        <div class="project-lang">CSS</div>
        <div class="project-name">CALCULATOR</div>
        <div class="project-desc">Sleek, precision-styled calculator with smooth interaction.</div>
        <div class="project-tag">UTILITY</div>
      </div>

      <div class="project-card">
        <div class="corner tl"></div><div class="corner tr"></div>
        <div class="corner bl"></div><div class="corner br"></div>
        <div class="project-lang">HTML</div>
        <div class="project-name">THREE-JS</div>
        <div class="project-desc">Exploring 3D graphics and WebGL through Three.js experiments.</div>
        <div class="project-tag">EXPERIMENT</div>
      </div>

      <div class="project-card">
        <div class="corner tl"></div><div class="corner tr"></div>
        <div class="corner bl"></div><div class="corner br"></div>
        <div class="project-lang">HTML</div>
        <div class="project-name">API</div>
        <div class="project-desc">Frontend integration patterns for consuming modern REST APIs.</div>
        <div class="project-tag">IN PROGRESS</div>
      </div>

    </div>
  </div>

  <!-- README CODE -->
  <div class="section">
    <div class="section-header">
      <span class="section-num">03</span>
      <span class="section-title">README.md Source</span>
      <div class="section-line"></div>
    </div>
    <div class="readme-box">
      <div class="readme-box-label">// COPY THIS INTO YOUR README.md //</div>
      <pre><span class="c">&lt;!-- Place this in your username/username repo as README.md --&gt;</span>

<span class="k">&lt;div align="center"&gt;</span>

<span class="c">&lt;!-- Banner --&gt;</span>
<span class="k">![header](</span><span class="v">https://capsule-render.vercel.app/api?type=waving&color=0:00f5ff,100:ff00c8&height=200&section=header&text=LEGACIA&fontSize=70&fontFamily=Orbitron&fontColor=ffffff&animation=fadeIn</span><span class="k">)</span>

<span class="c">&lt;!-- Typing intro --&gt;</span>
<span class="k">[![Typing SVG](</span><span class="v">https://readme-typing-svg.demolab.com?font=Share+Tech+Mono&size=16&pause=1000&color=00F5FF&center=true&vCenter=true&width=600&lines=Building+tomorrow's+web+from+today's+code.;Front-end+Architect.+Creative+Technologist.;Digital+Craftsman.+Futurist.+Builder.</span><span class="k">)](https://git.io/typing-svg)</span>

<span class="c">&lt;!-- Stats --&gt;</span>
<span class="k">![GitHub Stats](</span><span class="v">https://github-readme-stats.vercel.app/api?username=igiranezajoseph50-ops&show_icons=true&theme=midnight-purple&hide_border=true&bg_color=020510&title_color=00f5ff&icon_color=ff00c8&text_color=88aacc</span><span class="k">)</span>

<span class="c">&lt;!-- Top Languages --&gt;</span>
<span class="k">![Top Langs](</span><span class="v">https://github-readme-stats.vercel.app/api/top-langs/?username=igiranezajoseph50-ops&layout=compact&theme=midnight-purple&hide_border=true&bg_color=020510&title_color=00f5ff&text_color=88aacc</span><span class="k">)</span>

<span class="c">&lt;!-- Streak --&gt;</span>
<span class="k">[![GitHub Streak](</span><span class="v">https://streak-stats.demolab.com?user=igiranezajoseph50-ops&theme=midnight-purple&hide_border=true&background=020510&ring=00f5ff&fire=ff00c8&currStreakLabel=00f5ff</span><span class="k">)](https://git.io/streak-stats)</span>

<span class="c">&lt;!-- Footer wave --&gt;</span>
<span class="k">![footer](</span><span class="v">https://capsule-render.vercel.app/api?type=waving&color=0:ff00c8,100:00f5ff&height=100&section=footer</span><span class="k">)</span>

<span class="k">&lt;/div&gt;</span></pre>
    </div>
  </div>

  <!-- CONNECT -->
  <div class="section">
    <div class="section-header">
      <span class="section-num">04</span>
      <span class="section-title">Establish Connection</span>
      <div class="section-line"></div>
    </div>
    <div class="connect-row">
      <a class="connect-btn" href="#">GITHUB PROFILE</a>
      <a class="connect-btn" href="#">PROJECTS</a>
      <a class="connect-btn" href="#">CONTACT</a>
    </div>
  </div>

  <!-- FOOTER -->
  <div class="footer">
    <div class="footer-text">// LEGACIA · SYSTEM ONLINE · 2026 //</div>
  </div>

</div>
</body>
</html>

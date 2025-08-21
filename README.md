<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Preksha – Portfolio</title>
  <style>
    :root {
      --bg: #0b0f14;
      --card: #111827;
      --muted: #9aa4b2;
      --text: #e5e7eb;
      --accent: #7c3aed;
      --accent-2: #06b6d4;
      --ring: rgba(124, 58, 237, .35);
    }
    * { box-sizing: border-box; }
    html, body { margin: 0; padding: 0; background: var(--bg); color: var(--text); font: 16px/1.6 system-ui, -apple-system, Segoe UI, Roboto, Ubuntu, Cantarell, Noto Sans, Helvetica Neue, Arial, "Apple Color Emoji", "Segoe UI Emoji"; }
    a { color: inherit; text-decoration: none; }
    img { max-width: 100%; display: block; }
    .container { max-width: 1100px; margin: 0 auto; padding: 24px; }
    header { position: sticky; top: 0; z-index: 10; backdrop-filter: saturate(150%) blur(8px); background: linear-gradient(180deg, rgba(11, 15, 20, .9), rgba(11, 15, 20, .4) 60%, transparent); border-bottom: 1px solid rgba(255,255,255,.06); }
    .nav { display:flex; align-items:center; justify-content:space-between; gap: 16px; }
    .brand { font-weight: 800; letter-spacing: .3px; display:flex; align-items:center; gap:10px; }
    .brand .dot { width:10px; height:10px; border-radius:50%; background: linear-gradient(135deg, var(--accent), var(--accent-2)); box-shadow: 0 0 24px var(--ring); }
    .nav a.btn { padding: 10px 16px; border-radius: 999px; border: 1px solid rgba(255,255,255,.12); transition:.2s; }
    .nav a.btn:hover { border-color: rgba(255,255,255,.35); box-shadow: 0 6px 20px rgba(0,0,0,.35), 0 0 0 6px var(--ring); }.hero { padding: 80px 0 32px; display:grid; grid-template-columns: 1.2fr .8fr; gap: 24px; align-items:center; }
@media (max-width: 900px){ .hero{ grid-template-columns:1fr; padding-top: 56px; } }
h1 { font-size: clamp(2rem, 3.8vw + 1rem, 4rem); line-height: 1.1; margin: 0 0 12px; letter-spacing: -.5px; }
.sub { color: var(--muted); margin: 0 0 20px; font-size: clamp(1rem, 1.1vw + .8rem, 1.2rem); }
.cta { display:flex; gap:12px; flex-wrap: wrap; }
.btn-primary { background: linear-gradient(135deg, var(--accent), var(--accent-2)); color:#fff; padding: 12px 18px; border: 0; border-radius: 999px; box-shadow: 0 8px 24px rgba(124,58,237,.35); font-weight: 700; }
.btn-ghost { padding: 12px 18px; border-radius: 999px; border:1px solid rgba(255,255,255,.18); color: var(--text); background: transparent; }

.card { background: radial-gradient(1200px 600px at -10% -10%, rgba(124,58,237,.15), transparent 60%), radial-gradient(900px 600px at 110% -10%, rgba(6,182,212,.1), transparent 50%), var(--card);
        border: 1px solid rgba(255,255,255,.06); border-radius: 18px; box-shadow: 0 20px 60px rgba(0,0,0,.35); }

.about { margin-top: 24px; display:grid; grid-template-columns: 1fr 1fr; gap: 24px; }
@media (max-width: 900px){ .about{ grid-template-columns:1fr; } }
.about .card { padding: 24px; }
.kpis { display:grid; grid-template-columns: repeat(3,1fr); gap: 16px; margin-top: 12px; }
.kpi { padding: 16px; background: rgba(255,255,255,.03); border: 1px dashed rgba(255,255,255,.1); border-radius: 12px; text-align:center; }
.kpi b { font-size: 1.4rem; display:block; }

.chips { display:flex; gap:8px; flex-wrap: wrap; margin-top: 12px; }
.chip { border:1px solid rgba(255,255,255,.15); padding: 6px 10px; border-radius: 999px; color: var(--muted); font-weight:600; font-size:.9rem; }

.section-title { font-size: 1.8rem; margin: 40px 0 14px; letter-spacing: .2px; }

.grid { display:grid; grid-template-columns: repeat(3, 1fr); gap: 20px; }
@media (max-width: 900px){ .grid{ grid-template-columns:1fr; } }

.project { overflow: hidden; position: relative; }
.thumb { height: 180px; background: linear-gradient(135deg, rgba(124,58,237,.25), rgba(6,182,212,.25)), repeating-linear-gradient(45deg, rgba(255,255,255,.05) 0 6px, transparent 6px 12px); display:flex; align-items:flex-end; padding: 14px; }
.thumb span { font-weight: 800; letter-spacing:.5px; opacity:.9; }
.p-body { padding: 18px; display:flex; flex-direction: column; gap: 10px; }
.p-title { font-size: 1.15rem; font-weight: 800; margin: 2px 0; }
.p-text { color: var(--muted); }
.p-actions { display:flex; gap:10px; flex-wrap: wrap; margin-top: 6px; }
.p-actions a { padding:10px 14px; border-radius: 12px; border:1px solid rgba(255,255,255,.14); }
.p-actions a.primary { background: linear-gradient(135deg, var(--accent), var(--accent-2)); color:#fff; border:0; }

.contact { margin: 40px 0 80px; display:grid; grid-template-columns: 1fr 1fr; gap: 24px; }
@media (max-width: 900px){ .contact{ grid-template-columns:1fr; } }
form { display:grid; gap: 12px; }
input, textarea { background: rgba(255,255,255,.03); border:1px solid rgba(255,255,255,.15); color: var(--text); padding: 12px 14px; border-radius: 12px; }
input:focus, textarea:focus { outline: none; box-shadow: 0 0 0 4px var(--ring); }

footer { border-top:1px solid rgba(255,255,255,.08); color: var(--muted); padding: 24px; text-align: center; }

.toggle { cursor: pointer; }
.light { --bg: #f6f7fb; --card:#ffffff; --text:#0b0f14; --muted:#4b5563; --ring: rgba(124,58,237,.2); }

  </style>
</head>
<body>
  <header>
    <div class="container nav">
      <div class="brand"><span class="dot"></span> Preksha</div>
      <nav style="display:flex; gap:14px; align-items:center;">
        <a class="btn" href="#projects">Projects</a>
        <a class="btn" href="#about">About</a>
        <a class="btn" href="#contact">Contact</a>
        <a class="btn toggle" id="toggleTheme" title="Toggle theme">🌓</a>
      </nav>
    </div>
  </header>  <main class="container">
    <section class="hero card">
      <div>
        <h1>Front‑End Developer & Creative Designer</h1>
        <p class="sub">Hi, I'm <b>Preksha</b> — a fresher front‑end developer (BBA) who builds clean, responsive UI with a focus on clarity and modern design.</p>
        <div class="cta">
          <a class="btn-primary" href="#projects">See My Work</a>
          <a class="btn-ghost" href="mailto:tulsivirda51@gmail.com">Email Me</a>
        </div>
        <div class="kpis">
          <div class="kpi"><b>3+</b><small>Featured Projects</small></div>
          <div class="kpi"><b>Responsive</b><small>Mobile‑first layouts</small></div>
          <div class="kpi"><b>Clean</b><small>Readable code</small></div>
        </div>
      </div>
      <div class="card" style="padding:22px; display:grid; place-items:center; min-height: 260px;">
        <svg viewBox="0 0 360 220" width="100%" height="100%" preserveAspectRatio="xMidYMid meet" style="border-radius:14px; background: radial-gradient(300px 160px at 80% 0%, rgba(124,58,237,.25), transparent 40%), linear-gradient(135deg, rgba(6,182,212,.15), rgba(124,58,237,.05)); border:1px solid rgba(255,255,255,.12)">
          <defs>
            <linearGradient id="g" x1="0" x2="1" y1="0" y2="1">
              <stop offset="0%" stop-color="rgba(124,58,237,1)"/>
              <stop offset="100%" stop-color="rgba(6,182,212,1)"/>
            </linearGradient>
          </defs>
          <g fill="none" stroke="url(#g)" stroke-width="6">
            <path d="M20 60 Q150 10 340 60" opacity=".8"/>
            <path d="M20 110 Q150 60 340 110" opacity=".6"/>
            <path d="M20 160 Q150 110 340 160" opacity=".4"/>
          </g>
          <text x="24" y="190" font-size="18" fill="currentColor" opacity=".8">UI • UX • Accessibility • Performance</text>
        </svg>
      </div>
    </section><section id="about" class="about">
  <div class="card">
    <h2 class="section-title">About Me</h2>
    <p>I enjoy turning complex ideas into simple, beautiful interfaces. Comfortable with semantic HTML, modern CSS, vanilla JS, and basic React. Learning fast and open to front‑end internships or junior roles.</p>
    <div class="chips">
      <span class="chip">HTML5</span>
      <span class="chip">CSS3 / Flex / Grid</span>
      <span class="chip">JavaScript</span>
      <span class="chip">React (basics)</span>
      <span class="chip">Responsive</span>
      <span class="chip">Git & GitHub</span>
    </div>
  </div>
  <div class="card">
    <h2 class="section-title">Highlights</h2>
    <ul>
      <li>Pixel‑perfect layouts with clean typography.</li>
      <li>Reusable components and utility classes.</li>
      <li>Accessible color contrast and keyboard‑friendly navigation.</li>
    </ul>
  </div>
</section>

<h2 id="projects" class="section-title">Projects</h2>
<section class="grid">
  <!-- Project 1 -->
  <article class="card project">
    <div class="thumb"><span>Product Landing Page</span></div>
    <div class="p-body">
      <div class="p-title">Minimal Product Landing</div>
      <p class="p-text">A sleek, mobile‑first landing page with hero, feature grid, pricing, and CTA. Built with semantic HTML and modern CSS (grid + clamp typography).</p>
      <div class="chips">
        <span class="chip">HTML</span><span class="chip">CSS Grid</span><span class="chip">Responsive</span>
      </div>
      <div class="p-actions">
        <a class="primary" href="#" target="_blank" rel="noreferrer">Live Demo</a>
        <a href="https://github.com/Tulsi503" target="_blank" rel="noreferrer">View Code</a>
      </div>
    </div>
  </article>

  <!-- Project 2 -->
  <article class="card project">
    <div class="thumb"><span>Cashier / Change App</span></div>
    <div class="p-body">
      <div class="p-title">Cashier – Change Calculator</div>
      <p class="p-text">Takes bill amount and cash given; returns optimal notes/coins breakdown with validation and error states.</p>
      <div class="chips">
        <span class="chip">JavaScript</span><span class="chip">Form UX</span><span class="chip">Logic</span>
      </div>
      <div class="p-actions">
        <a class="primary" href="#" target="_blank" rel="noreferrer">Live Demo</a>
        <a href="https://github.com/Tulsi503" target="_blank" rel="noreferrer">View Code</a>
      </div>
    </div>
  </article>

  <!-- Project 3 -->
  <article class="card project">
    <div class="thumb"><span>Pokémon Search</span></div>
    <div class="p-body">
      <div class="p-title">Pokémon Finder</div>
      <p class="p-text">Search by name or ID. Shows sprite, types, and stats with an accessible results card layout. (Can plug into public API.)</p>
      <div class="chips">
        <span class="chip">Fetch API</span><span class="chip">Cards</span><span class="chip">Accessibility</span>
      </div>
      <div class="p-actions">
        <a class="primary" href="#" target="_blank" rel="noreferrer">Live Demo</a>
        <a href="https://github.com/Tulsi503" target="_blank" rel="noreferrer">View Code</a>
      </div>
    </div>
  </article>
</section>

<h2 id="contact" class="section-title">Contact</h2>
<section class="contact">
  <div class="card" style="padding: 24px;">
    <p class="p-text">Want to collaborate or hire me? Send a message—I'll reply soon.</p>
    <form onsubmit="event.preventDefault(); window.location.href='mailto:tulsivirda51@gmail.com?subject=Portfolio%20Inquiry&body=Hi%20Preksha,';">
      <input type="text" name="name" placeholder="Your name" required>
      <input type="email" name="email" placeholder="Your email" required>
      <textarea name="message" rows="4" placeholder="Your message"></textarea>
      <button class="btn-primary" type="submit">Send Email</button>
    </form>
  </div>
  <div class="card" style="padding: 24px;">
    <p><b>Email:</b> <a href="mailto:tulsivirda51@gmail.com">tulsivirda51@gmail.com</a><br>
    <b>GitHub:</b> <a href="https://github.com/Tulsi503" target="_blank" rel="noreferrer">github.com/Tulsi503</a><br>
    <b>LinkedIn:</b> <a href="https://linkedin.com/in/tulsi-virda" target="_blank" rel="noreferrer">linkedin.com/in/tulsi-virda</a></p>
  </div>
</section>

  </main>
  

<!---
Tulsi503/Tulsi503 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

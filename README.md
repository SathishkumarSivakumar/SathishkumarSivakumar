<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Sathishkumar S — Data Science &amp; AI Engineering</title>
<meta name="description" content="Sathishkumar S — Data Science & AI Engineering portfolio. Python, SQL, Machine Learning, NLP, Power BI." />

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=IBM+Plex+Mono:wght@400;500;600&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">

<style>
  :root{
    --bg:#070b10;
    --surface:#0d141b;
    --surface-2:#111a22;
    --line:rgba(232,237,242,0.09);
    --line-strong:rgba(232,237,242,0.16);
    --text:#e9eef2;
    --text-muted:#8ea0ac;
    --text-faint:#5a6b76;
    --cyan:#5fe3c8;
    --cyan-dim:rgba(95,227,200,0.14);
    --amber:#f2a154;
    --amber-dim:rgba(242,161,84,0.14);
    --font-display:'Space Grotesk', sans-serif;
    --font-mono:'IBM Plex Mono', monospace;
    --font-body:'Inter', sans-serif;
  }

  *{margin:0;padding:0;box-sizing:border-box;}

  html{scroll-behavior:smooth;}

  body{
    background:var(--bg);
    color:var(--text);
    font-family:var(--font-body);
    line-height:1.6;
    overflow-x:hidden;
  }

  ::selection{background:var(--cyan); color:#04110d;}

  a{color:inherit; text-decoration:none;}

  img{max-width:100%; display:block;}

  .wrap{
    max-width:1120px;
    margin:0 auto;
    padding:0 32px;
  }

  /* ---------- scanline / grid texture ---------- */
  .grid-overlay{
    position:fixed; inset:0;
    background-image:
      linear-gradient(rgba(232,237,242,0.028) 1px, transparent 1px),
      linear-gradient(90deg, rgba(232,237,242,0.028) 1px, transparent 1px);
    background-size:42px 42px;
    pointer-events:none;
    z-index:1;
    mask-image:radial-gradient(ellipse 80% 60% at 50% 0%, black 40%, transparent 90%);
  }

  /* ---------- nav ---------- */
  header{
    position:fixed; top:0; left:0; right:0;
    z-index:50;
    backdrop-filter:blur(10px);
    background:rgba(7,11,16,0.72);
    border-bottom:1px solid var(--line);
  }
  .nav{
    display:flex; align-items:center; justify-content:space-between;
    padding:18px 32px;
    max-width:1120px; margin:0 auto;
  }
  .logo{
    font-family:var(--font-mono);
    font-size:14px; font-weight:600;
    letter-spacing:0.02em;
    display:flex; align-items:center; gap:8px;
  }
  .logo .dot{
    width:7px;height:7px;border-radius:50%;
    background:var(--cyan);
    box-shadow:0 0 8px var(--cyan);
    animation:pulse 2.4s ease-in-out infinite;
  }
  @keyframes pulse{
    0%,100%{opacity:1;} 50%{opacity:0.35;}
  }
  nav ul{
    list-style:none; display:flex; gap:36px;
  }
  nav a{
    font-family:var(--font-mono);
    font-size:12.5px;
    color:var(--text-muted);
    letter-spacing:0.04em;
    text-transform:uppercase;
    transition:color .2s ease;
    position:relative;
  }
  nav a::before{content:'· ';color:var(--cyan); opacity:0;}
  nav a:hover{color:var(--text);}
  nav a:hover::before{opacity:1;}
  .nav-links{display:flex; align-items:center; gap:36px;}
  .nav-cta{
    font-family:var(--font-mono);
    font-size:12px;
    padding:8px 16px;
    border:1px solid var(--line-strong);
    border-radius:3px;
    color:var(--text);
  }
  .nav-cta:hover{border-color:var(--cyan); color:var(--cyan);}
  .menu-btn{display:none;}

  /* ---------- hero ---------- */
  .hero{
    position:relative;
    min-height:100vh;
    display:flex; align-items:center;
    padding-top:90px;
    overflow:hidden;
  }
  #hero-canvas{
    position:absolute; inset:0;
    z-index:0;
    opacity:0.9;
  }
  .hero-inner{
    position:relative; z-index:2;
    width:100%;
  }
  .eyebrow{
    font-family:var(--font-mono);
    font-size:12.5px;
    color:var(--cyan);
    letter-spacing:0.08em;
    text-transform:uppercase;
    display:flex; align-items:center; gap:10px;
    margin-bottom:22px;
  }
  .eyebrow::before{
    content:'';
    width:22px; height:1px;
    background:var(--cyan);
  }
  h1.hero-title{
    font-family:var(--font-display);
    font-weight:600;
    font-size:clamp(2.4rem, 6vw, 4.6rem);
    line-height:1.05;
    letter-spacing:-0.02em;
    max-width:820px;
    color:var(--text);
  }
  h1.hero-title em{
    font-style:normal;
    color:var(--cyan);
  }
  .hero-sub{
    margin-top:26px;
    max-width:560px;
    color:var(--text-muted);
    font-size:16.5px;
    line-height:1.75;
  }
  .hero-actions{
    margin-top:38px;
    display:flex; gap:16px; flex-wrap:wrap;
  }
  .btn{
    font-family:var(--font-mono);
    font-size:13px;
    padding:13px 24px;
    border-radius:3px;
    letter-spacing:0.02em;
    transition:all .2s ease;
    display:inline-flex; align-items:center; gap:8px;
  }
  .btn-primary{
    background:var(--cyan);
    color:#04110d;
    font-weight:600;
  }
  .btn-primary:hover{background:#7cf0d8; transform:translateY(-1px);}
  .btn-ghost{
    border:1px solid var(--line-strong);
    color:var(--text);
  }
  .btn-ghost:hover{border-color:var(--text-muted); background:var(--surface);}

  .hero-stats{
    margin-top:72px;
    display:flex; gap:56px; flex-wrap:wrap;
    border-top:1px solid var(--line);
    padding-top:28px;
    max-width:640px;
  }
  .stat-num{
    font-family:var(--font-display);
    font-size:2rem; font-weight:600;
    color:var(--text);
  }
  .stat-label{
    font-family:var(--font-mono);
    font-size:11.5px;
    color:var(--text-faint);
    text-transform:uppercase;
    letter-spacing:0.05em;
    margin-top:4px;
  }

  .scroll-cue{
    position:absolute; bottom:36px; left:32px;
    font-family:var(--font-mono);
    font-size:11px;
    color:var(--text-faint);
    display:flex; align-items:center; gap:10px;
    z-index:2;
  }
  .scroll-cue .line{
    width:1px; height:34px;
    background:linear-gradient(var(--cyan), transparent);
    animation:scrolldown 1.8s ease-in-out infinite;
  }
  @keyframes scrolldown{
    0%{transform:scaleY(0); transform-origin:top;}
    50%{transform:scaleY(1); transform-origin:top;}
    51%{transform-origin:bottom;}
    100%{transform:scaleY(0); transform-origin:bottom;}
  }

  /* ---------- section shared ---------- */
  section{
    position:relative; z-index:2;
    padding:120px 0;
    border-bottom:1px solid var(--line);
  }
  .section-head{
    display:flex; align-items:baseline; gap:18px;
    margin-bottom:56px;
  }
  .section-num{
    font-family:var(--font-mono);
    font-size:12.5px;
    color:var(--cyan);
  }
  .section-title{
    font-family:var(--font-display);
    font-size:clamp(1.7rem, 3.4vw, 2.5rem);
    font-weight:600;
    letter-spacing:-0.01em;
  }
  .section-kicker{
    font-family:var(--font-mono);
    font-size:12px;
    color:var(--text-faint);
    text-transform:uppercase;
    letter-spacing:0.08em;
    margin-bottom:10px;
  }

  /* ---------- skills (query console) ---------- */
  .console{
    background:var(--surface);
    border:1px solid var(--line);
    border-radius:8px;
    overflow:hidden;
  }
  .console-bar{
    display:flex; align-items:center; gap:8px;
    padding:12px 18px;
    border-bottom:1px solid var(--line);
    background:var(--surface-2);
  }
  .console-bar span{
    width:10px;height:10px;border-radius:50%;
    background:var(--line-strong);
  }
  .console-bar .title{
    font-family:var(--font-mono);
    font-size:12px;
    color:var(--text-faint);
    margin-left:8px;
  }
  .console-body{
    padding:32px;
    font-family:var(--font-mono);
    font-size:14.5px;
    line-height:1.9;
  }
  .kw{color:var(--cyan);}
  .str{color:var(--amber);}
  .cmt{color:var(--text-faint);}
  .fn{color:#9db4c0;}

  .skill-chips{
    display:flex; flex-wrap:wrap; gap:10px;
    margin-top:30px;
  }
  .chip{
    font-family:var(--font-mono);
    font-size:12.5px;
    padding:8px 14px;
    border:1px solid var(--line-strong);
    border-radius:20px;
    color:var(--text-muted);
    transition:all .2s ease;
  }
  .chip:hover{
    border-color:var(--cyan);
    color:var(--cyan);
    background:var(--cyan-dim);
  }

  /* ---------- projects ---------- */
  .projects-grid{
    display:grid;
    grid-template-columns:repeat(2, 1fr);
    gap:1px;
    background:var(--line);
    border:1px solid var(--line);
    border-radius:8px;
    overflow:hidden;
  }
  .project-card{
    background:var(--surface);
    padding:36px;
    perspective:900px;
    transition:background .25s ease;
  }
  .project-card.full{grid-column:1 / -1;}
  .project-card:hover{background:var(--surface-2);}
  .project-inner{
    transform-style:preserve-3d;
    transition:transform .35s ease;
  }
  .project-card:hover .project-inner{
    transform:rotateX(2deg) rotateY(-2deg) translateZ(6px);
  }
  .project-tag{
    font-family:var(--font-mono);
    font-size:11px;
    color:var(--amber);
    text-transform:uppercase;
    letter-spacing:0.06em;
    margin-bottom:14px;
    display:block;
  }
  .project-title{
    font-family:var(--font-display);
    font-size:1.4rem;
    font-weight:600;
    margin-bottom:14px;
  }
  .project-desc{
    color:var(--text-muted);
    font-size:14.5px;
    margin-bottom:20px;
  }
  .project-stack{
    display:flex; flex-wrap:wrap; gap:8px;
    margin-bottom:18px;
  }
  .stack-pill{
    font-family:var(--font-mono);
    font-size:11px;
    padding:5px 10px;
    border-radius:3px;
    background:var(--cyan-dim);
    color:var(--cyan);
  }
  .project-link{
    font-family:var(--font-mono);
    font-size:12.5px;
    color:var(--text);
    border-bottom:1px solid var(--line-strong);
    padding-bottom:2px;
    display:inline-flex; align-items:center; gap:6px;
  }
  .project-link:hover{color:var(--cyan); border-color:var(--cyan);}

  /* ---------- experience timeline ---------- */
  .timeline{
    position:relative;
    padding-left:32px;
  }
  .timeline::before{
    content:'';
    position:absolute; left:5px; top:6px; bottom:6px;
    width:1px;
    background:var(--line-strong);
  }
  .tl-item{
    position:relative;
    padding-bottom:44px;
  }
  .tl-item:last-child{padding-bottom:0;}
  .tl-item::before{
    content:'';
    position:absolute; left:-32px; top:5px;
    width:11px; height:11px; border-radius:50%;
    background:var(--bg);
    border:2px solid var(--cyan);
  }
  .tl-date{
    font-family:var(--font-mono);
    font-size:11.5px;
    color:var(--text-faint);
    text-transform:uppercase;
    letter-spacing:0.05em;
    margin-bottom:6px;
  }
  .tl-role{
    font-family:var(--font-display);
    font-size:1.2rem;
    font-weight:600;
  }
  .tl-org{
    font-family:var(--font-mono);
    font-size:12.5px;
    color:var(--cyan);
    margin-top:2px;
    margin-bottom:10px;
  }
  .tl-desc{color:var(--text-muted); font-size:14.5px; max-width:600px;}

  /* ---------- certifications ---------- */
  .cert-grid{
    display:grid;
    grid-template-columns:repeat(auto-fit, minmax(230px, 1fr));
    gap:16px;
  }
  .cert-card{
    border:1px solid var(--line);
    border-radius:8px;
    padding:24px;
    background:var(--surface);
    display:flex; gap:16px; align-items:flex-start;
  }
  .cert-icon{
    font-family:var(--font-mono);
    font-size:11px;
    font-weight:600;
    color:var(--bg);
    background:var(--cyan);
    width:38px; height:38px;
    border-radius:6px;
    display:flex; align-items:center; justify-content:center;
    flex-shrink:0;
  }
  .cert-name{font-family:var(--font-display); font-weight:600; font-size:1.02rem;}
  .cert-meta{font-family:var(--font-mono); font-size:11.5px; color:var(--text-faint); margin-top:4px;}

  /* ---------- contact ---------- */
  .contact-section{border-bottom:none;}
  .contact-grid{
    display:grid;
    grid-template-columns:1.2fr 1fr;
    gap:60px;
    align-items:start;
  }
  .contact-title{
    font-family:var(--font-display);
    font-size:clamp(1.9rem, 4vw, 3rem);
    font-weight:600;
    line-height:1.15;
    max-width:520px;
  }
  .contact-title .cyan{color:var(--cyan);}
  .contact-sub{
    margin-top:20px;
    color:var(--text-muted);
    max-width:460px;
  }
  .contact-list{margin-top:36px;}
  .contact-row{
    display:flex; align-items:center; justify-content:space-between;
    padding:18px 0;
    border-top:1px solid var(--line);
    font-family:var(--font-mono);
    font-size:13.5px;
  }
  .contact-row:last-child{border-bottom:1px solid var(--line);}
  .contact-row .label{color:var(--text-faint); text-transform:uppercase; font-size:11px; letter-spacing:0.06em;}
  .contact-row .value{color:var(--text);}
  .contact-row a.value:hover{color:var(--cyan);}
  .status-card{
    border:1px solid var(--line);
    border-radius:8px;
    padding:28px;
    background:var(--surface);
  }
  .status-badge{
    display:inline-flex; align-items:center; gap:8px;
    font-family:var(--font-mono);
    font-size:11.5px;
    color:var(--cyan);
    text-transform:uppercase;
    letter-spacing:0.05em;
    margin-bottom:18px;
  }
  .status-badge .dot{width:7px;height:7px;border-radius:50%;background:var(--cyan); box-shadow:0 0 8px var(--cyan); animation:pulse 2.4s ease-in-out infinite;}
  .status-card p{color:var(--text-muted); font-size:13.5px; margin-bottom:22px;}

  footer{
    padding:36px 0;
    text-align:center;
    font-family:var(--font-mono);
    font-size:11.5px;
    color:var(--text-faint);
  }

  @media (max-width:820px){
    .nav-links{position:fixed; top:64px; right:0; left:0; background:var(--bg); flex-direction:column; padding:24px 32px; border-bottom:1px solid var(--line); display:none; gap:20px;}
    .nav-links.open{display:flex;}
    .menu-btn{display:block; background:none; border:none; color:var(--text); font-size:20px; cursor:pointer;}
    .projects-grid{grid-template-columns:1fr;}
    .contact-grid{grid-template-columns:1fr; gap:40px;}
    .hero-stats{gap:36px;}
  }
</style>
</head>
<body>

<div class="grid-overlay"></div>

<header>
  <div class="nav">
    <div class="logo"><span class="dot"></span>SATHISHKUMAR.S</div>
    <div class="nav-links" id="navLinks">
      <ul>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#projects">Work</a></li>
        <li><a href="#experience">Experience</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
      <a class="nav-cta" href="mailto:kumar109662@gmail.com">Say hello</a>
    </div>
    <button class="menu-btn" id="menuBtn" aria-label="Toggle menu">☰</button>
  </div>
</header>

<main>
  <section class="hero">
    <canvas id="hero-canvas"></canvas>
    <div class="wrap hero-inner">
      <div class="eyebrow">Data Science &amp; AI Engineering · Chennai</div>
      <h1 class="hero-title">I turn messy data<br>into <em>decisions</em> people trust.</h1>
      <p class="hero-sub">Working across Python, SQL, Machine Learning, NLP, and Business Intelligence — from cleaning raw data to shipping the dashboard someone actually opens every morning.</p>
      <div class="hero-actions">
        <a class="btn btn-primary" href="#projects">View my work →</a>
        <a class="btn btn-ghost" href="#contact">Get in touch</a>
      </div>
      <div class="hero-stats">
        <div>
          <div class="stat-num">2+</div>
          <div class="stat-label">End-to-end projects</div>
        </div>
        <div>
          <div class="stat-num">2</div>
          <div class="stat-label">Internships completed</div>
        </div>
        <div>
          <div class="stat-num">8.3</div>
          <div class="stat-label">CGPA in Engineering</div>
        </div>
      </div>
    </div>
    <div class="scroll-cue"><div class="line"></div>SCROLL</div>
  </section>

  <section id="skills">
    <div class="wrap">
      <div class="section-head">
        <span class="section-num">01</span>
        <h2 class="section-title">What I work with</h2>
      </div>

      <div class="console">
        <div class="console-bar">
          <span></span><span></span><span></span>
          <span class="title">skills.sql</span>
        </div>
        <div class="console-body">
<span class="kw">SELECT</span> <span class="str">'Python'</span>, <span class="str">'SQL'</span>, <span class="str">'Machine Learning'</span>, <span class="str">'NLP'</span>,<br>
&nbsp;&nbsp;&nbsp;&nbsp;<span class="str">'Power BI'</span>, <span class="str">'DAX'</span>, <span class="str">'Pandas'</span>, <span class="str">'NumPy'</span>, <span class="str">'Scikit-learn'</span>, <span class="str">'MySQL'</span><br>
<span class="kw">FROM</span> <span class="fn">skills</span><br>
<span class="kw">WHERE</span> proficiency &gt;= <span class="str">'strong'</span><br>
<span class="kw">ORDER BY</span> impact <span class="kw">DESC</span>; <span class="cmt">-- always shipping, always learning</span>
        </div>
      </div>

      <div class="skill-chips">
        <span class="chip">Python</span>
        <span class="chip">SQL</span>
        <span class="chip">MySQL</span>
        <span class="chip">Machine Learning</span>
        <span class="chip">NLP</span>
        <span class="chip">Power BI</span>
        <span class="chip">DAX</span>
        <span class="chip">Pandas</span>
        <span class="chip">NumPy</span>
        <span class="chip">Scikit-learn</span>
        <span class="chip">Matplotlib</span>
        <span class="chip">Jupyter Notebook</span>
        <span class="chip">Git / GitHub</span>
        <span class="chip">VS Code</span>
      </div>
    </div>
  </section>

  <section id="projects">
    <div class="wrap">
      <div class="section-head">
        <span class="section-num">02</span>
        <h2 class="section-title">Projects I've built</h2>
      </div>

      <div class="projects-grid">
        <div class="project-card full">
          <div class="project-inner">
            <span class="project-tag">Final year project</span>
            <div class="project-title">AI-Enhanced Herbal Mosquito Repellent Kit</div>
            <p class="project-desc">An AI-driven herbal mosquito repellent system — Python-based detection identifies when a mosquito enters the room and automatically activates the herbal repellent kit, switching off once the mosquito is gone.</p>
            <div class="project-stack">
              <span class="stack-pill">Python</span>
              <span class="stack-pill">Machine Learning</span>
              <span class="stack-pill">Automation</span>
            </div>
          </div>
        </div>

        <div class="project-card">
          <div class="project-inner">
            <span class="project-tag">Full DB design</span>
            <div class="project-title">Apollocare Hospital Management System</div>
            <p class="project-desc">MySQL-based hospital management system handling patients, doctors, appointments, billing, pharmacy, and medical records — built with joins, subqueries, views, stored procedures, and triggers, with indexing for query performance.</p>
            <div class="project-stack">
              <span class="stack-pill">MySQL</span>
              <span class="stack-pill">Database Design</span>
              <span class="stack-pill">Triggers</span>
            </div>
            <a class="project-link" href="https://github.com/SathishkumarSivakumar/ApolloCare-Hospital-Management-System" target="_blank" rel="noopener">View on GitHub →</a>
          </div>
        </div>

        <div class="project-card">
          <div class="project-inner">
            <span class="project-tag">Sentiment model</span>
            <div class="project-title">Amazon User Review Analysis (NLP)</div>
            <p class="project-desc">NLP-based sentiment analysis on Amazon reviews — text cleaning, tokenization, and feature extraction with TF-IDF and Count Vectorizer, then classification models built and evaluated with Scikit-learn.</p>
            <div class="project-stack">
              <span class="stack-pill">Python</span>
              <span class="stack-pill">NLP</span>
              <span class="stack-pill">TF-IDF</span>
            </div>
            <a class="project-link" href="https://github.com/SathishkumarSivakumar/Project-Amazon-NLP-" target="_blank" rel="noopener">View on GitHub →</a>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section id="experience">
    <div class="wrap">
      <div class="section-head">
        <span class="section-num">03</span>
        <h2 class="section-title">Experience &amp; credentials</h2>
      </div>

      <div class="timeline">
        <div class="tl-item">
          <div class="tl-date">Jan – Mar 2024</div>
          <div class="tl-role">SQL Developer Intern</div>
          <div class="tl-org">Besant Technology</div>
          <p class="tl-desc">Developed and optimized SQL queries and database objects in MySQL — joins, views, stored procedures, functions, triggers, and indexes — with a focus on query performance.</p>
        </div>
        <div class="tl-item">
          <div class="tl-date">May 2024</div>
          <div class="tl-role">Data Science Intern</div>
          <div class="tl-org">Coapps.ai</div>
          <p class="tl-desc">Completed a Data Science internship with a satisfactory performance record — hands-on work across the data science lifecycle from EDA to model building.</p>
        </div>
        <div class="tl-item">
          <div class="tl-date">2024</div>
          <div class="tl-role">Certification — Data Science</div>
          <div class="tl-org">Coapps</div>
          <p class="tl-desc">Certified in core data science practice: data cleaning, EDA, feature engineering, and predictive modeling.</p>
        </div>
        <div class="tl-item">
          <div class="tl-date">Graduated</div>
          <div class="tl-role">BE, Electrical &amp; Electronics Engineering</div>
          <div class="tl-org">Kongunadu College of Engineering and Technology</div>
          <p class="tl-desc">Graduated with a CGPA of 8.3.</p>
        </div>
      </div>
    </div>
  </section>

  <section id="certifications">
    <div class="wrap">
      <div class="section-head">
        <span class="section-num">04</span>
        <h2 class="section-title">Credentials</h2>
      </div>
      <div class="cert-grid">
        <div class="cert-card">
          <div class="cert-icon">DS</div>
          <div>
            <div class="cert-name">Data Science</div>
            <div class="cert-meta">Coapps · May 2024</div>
          </div>
        </div>
        <div class="cert-card">
          <div class="cert-icon">SQL</div>
          <div>
            <div class="cert-name">SQL (Basic/Intermediate)</div>
            <div class="cert-meta">HackerRank</div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section id="contact" class="contact-section">
    <div class="wrap">
      <div class="section-head">
        <span class="section-num">05</span>
        <h2 class="section-title">Contact</h2>
      </div>
      <div class="contact-grid">
        <div>
          <div class="contact-title">Have a data problem <span class="cyan">worth solving?</span></div>
          <p class="contact-sub">Based in Chennai, open to full-time Data Science / Analytics roles. Reach out — happy to talk.</p>

          <div class="contact-list">
            <div class="contact-row">
              <span class="label">Email</span>
              <a class="value" href="mailto:kumar109662@gmail.com">kumar109662@gmail.com</a>
            </div>
            <div class="contact-row">
              <span class="label">Phone</span>
              <a class="value" href="tel:+919789704124">+91 97897 04124</a>
            </div>
            <div class="contact-row">
              <span class="label">LinkedIn</span>
              <a class="value" href="https://www.linkedin.com/in/sathishkumar-sivakumar/" target="_blank" rel="noopener">/in/sathishkumar-sivakumar</a>
            </div>
            <div class="contact-row">
              <span class="label">GitHub</span>
              <a class="value" href="https://github.com/SathishkumarSivakumar" target="_blank" rel="noopener">/SathishkumarSivakumar</a>
            </div>
          </div>
        </div>

        <div class="status-card">
          <div class="status-badge"><span class="dot"></span>Open to opportunities</div>
          <p>Currently exploring Data Science, Analytics, and AI Engineering roles — full-time, Chennai or remote.</p>
          <a class="btn btn-primary" href="mailto:kumar109662@gmail.com" style="width:100%; justify-content:center;">Email me →</a>
        </div>
      </div>
    </div>
  </section>

  <footer>
    © 2026 Sathishkumar S — Chennai. Built with data, coffee, and one too many SQL joins.
  </footer>
</main>

<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
<script>
  // mobile menu
  const menuBtn = document.getElementById('menuBtn');
  const navLinks = document.getElementById('navLinks');
  menuBtn.addEventListener('click', () => navLinks.classList.toggle('open'));
  navLinks.querySelectorAll('a').forEach(a => a.addEventListener('click', () => navLinks.classList.remove('open')));

  // ---------- 3D hero: rotating data-schema graph ----------
  (function(){
    const canvas = document.getElementById('hero-canvas');
    const scene = new THREE.Scene();
    const camera = new THREE.PerspectiveCamera(55, window.innerWidth/window.innerHeight, 0.1, 100);
    camera.position.set(0, 0, 13);

    const renderer = new THREE.WebGLRenderer({ canvas, alpha:true, antialias:true });
    renderer.setPixelRatio(Math.min(window.devicePixelRatio, 2));
    renderer.setSize(window.innerWidth, window.innerHeight);

    const group = new THREE.Group();
    scene.add(group);

    // node positions — clustered like a schema / knowledge graph
    const NODE_COUNT = 46;
    const nodes = [];
    const nodeGeo = new THREE.SphereGeometry(0.05, 10, 10);

    const cyan = new THREE.Color(0x5fe3c8);
    const amber = new THREE.Color(0xf2a154);
    const dim = new THREE.Color(0x2c3a42);

    for (let i = 0; i < NODE_COUNT; i++) {
      const radius = 5.4;
      const phi = Math.acos(-1 + (2 * i) / NODE_COUNT);
      const theta = Math.sqrt(NODE_COUNT * Math.PI) * phi;
      const x = radius * Math.cos(theta) * Math.sin(phi) + (Math.random()-0.5)*1.4;
      const y = radius * Math.sin(theta) * Math.sin(phi) + (Math.random()-0.5)*1.4;
      const z = radius * Math.cos(phi) + (Math.random()-0.5)*1.4;

      const isAccent = Math.random() < 0.16;
      const color = isAccent ? (Math.random() < 0.5 ? cyan : amber) : dim;
      const mat = new THREE.MeshBasicMaterial({ color });
      const mesh = new THREE.Mesh(nodeGeo, mat);
      mesh.position.set(x, y, z);
      group.add(mesh);
      nodes.push(mesh.position);
    }

    // connect nearby nodes with thin lines
    const lineMat = new THREE.LineBasicMaterial({ color: 0x2c3a42, transparent:true, opacity:0.35 });
    const linePositions = [];
    const MAX_DIST = 3.1;
    for (let i = 0; i < nodes.length; i++) {
      for (let j = i+1; j < nodes.length; j++) {
        if (nodes[i].distanceTo(nodes[j]) < MAX_DIST) {
          linePositions.push(nodes[i].x, nodes[i].y, nodes[i].z);
          linePositions.push(nodes[j].x, nodes[j].y, nodes[j].z);
        }
      }
    }
    const lineGeo = new THREE.BufferGeometry();
    lineGeo.setAttribute('position', new THREE.Float32BufferAttribute(linePositions, 3));
    const lines = new THREE.LineSegments(lineGeo, lineMat);
    group.add(lines);

    group.rotation.x = 0.3;

    let mouseX = 0, mouseY = 0;
    window.addEventListener('mousemove', (e) => {
      mouseX = (e.clientX / window.innerWidth - 0.5);
      mouseY = (e.clientY / window.innerHeight - 0.5);
    });

    function resize(){
      camera.aspect = window.innerWidth / window.innerHeight;
      camera.updateProjectionMatrix();
      renderer.setSize(window.innerWidth, window.innerHeight);
    }
    window.addEventListener('resize', resize);

    const clock = new THREE.Clock();
    const reduceMotion = window.matchMedia('(prefers-reduced-motion: reduce)').matches;

    function animate(){
      requestAnimationFrame(animate);
      const t = clock.getElapsedTime();
      if (!reduceMotion) {
        group.rotation.y = t * 0.06;
        group.rotation.x = 0.3 + mouseY * 0.25;
      }
      group.position.x += (mouseX * 1.2 - group.position.x) * 0.02;
      renderer.render(scene, camera);
    }
    animate();
  })();

  // reveal-on-scroll for sections
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.style.opacity = 1;
        entry.target.style.transform = 'translateY(0)';
      }
    });
  }, { threshold: 0.12 });

  document.querySelectorAll('section:not(.hero)').forEach(sec => {
    sec.style.opacity = 0;
    sec.style.transform = 'translateY(24px)';
    sec.style.transition = 'opacity .7s ease, transform .7s ease';
    observer.observe(sec);
  });
</script>

</body>
</html>

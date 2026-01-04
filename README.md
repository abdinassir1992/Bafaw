<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Milwaukee Somali Bantu Community Organization</title>
  <meta name="description" content="Serving the Somali Bantu community in Milwaukee since 2003 through human rights advocacy and social services." />

  <style>
    :root{
      /* New theme: warm + professional (gold + deep navy + soft cream) */
      --bg1: #fff8f1;
      --bg2: #f4f7ff;
      --card: rgba(255,255,255,0.88);
      --text: #0b1220;
      --muted: #4b5565;
      --line: rgba(15, 23, 42, 0.10);
      --brand: #0f3d5e;     /* deep navy */
      --brand2:#c08a2f;     /* warm gold */
      --accent:#0ea5a4;     /* teal accent */
      --shadow: 0 20px 60px rgba(16,24,40,0.12);
      --radius: 18px;
    }

    *{ box-sizing: border-box; }
    html,body{ margin:0; padding:0; font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Arial; color:var(--text); }

    body{
      background:
        radial-gradient(1100px 600px at 14% 10%, rgba(192,138,47,0.18), transparent 60%),
        radial-gradient(900px 520px at 88% 14%, rgba(15,61,94,0.16), transparent 55%),
        radial-gradient(700px 420px at 45% 92%, rgba(14,165,164,0.10), transparent 55%),
        linear-gradient(180deg, var(--bg1) 0%, #ffffff 28%, var(--bg2) 100%);
      overflow-x: hidden;
    }

    /* subtle premium texture */
    body::before{
      content:"";
      position: fixed;
      inset: 0;
      pointer-events:none;
      background:
        radial-gradient(circle at 1px 1px, rgba(15,23,42,0.06) 1px, transparent 1px);
      background-size: 26px 26px;
      opacity: 0.22;
      mask-image: radial-gradient(900px 520px at 20% 10%, #000 45%, transparent 75%);
    }

    a{ color:inherit; text-decoration:none; }
    .container{ width:min(1140px, calc(100% - 32px)); margin:0 auto; }

    /* topbar */
    .topbar{
      border-bottom: 1px solid var(--line);
      background: rgba(255,255,255,0.65);
      backdrop-filter: blur(10px);
      position: relative;
      z-index: 4;
    }
    .topbar-inner{
      display:flex; align-items:center; justify-content:space-between;
      padding:10px 0; gap:12px;
    }
    .topbar-left{ display:flex; align-items:center; gap:10px; color:var(--muted); font-size:14px; }
    .dot{
      width:10px; height:10px; border-radius:50%;
      background: var(--brand2);
      box-shadow: 0 0 0 6px rgba(192,138,47,0.16);
    }

    .lang-btn{
      border:1px solid var(--line);
      background: rgba(255,255,255,0.8);
      color: var(--muted);
      padding:7px 10px;
      border-radius: 12px;
      cursor:pointer;
      font-weight:800;
    }
    .lang-btn.active{
      border-color: rgba(15,61,94,0.35);
      color: var(--text);
      box-shadow: 0 10px 22px rgba(15,61,94,0.10);
    }

    /* header */
    .header{
      position: sticky;
      top:0;
      z-index: 10;
      border-bottom: 1px solid var(--line);
      background: rgba(255,255,255,0.70);
      backdrop-filter: blur(12px);
    }
    .header-inner{
      display:flex; align-items:center; justify-content:space-between;
      padding:14px 0; gap:16px;
    }
    .brand{
      display:flex; align-items:center; gap:12px;
    }
    .brand-mark{
      width:46px; height:46px;
      border-radius: 16px;
      display:grid; place-items:center;
      font-weight:900;
      letter-spacing:-0.4px;
      color:#fff;
      background: linear-gradient(135deg, rgba(15,61,94,1), rgba(192,138,47,0.95));
      box-shadow: 0 14px 30px rgba(15,61,94,0.18);
    }
    .brand-title{ font-weight:900; letter-spacing:-0.2px; }
    .brand-sub{ margin-top:2px; font-size:13px; color:var(--muted); }

    .nav{ display:flex; align-items:center; gap:18px; }
    .nav a{ color:var(--muted); font-weight:800; font-size:14px; }
    .nav a:hover{ color:var(--text); }
    .nav-cta{
      padding:10px 14px;
      border-radius: 14px;
      border:1px solid rgba(15,61,94,0.22);
      background: rgba(255,255,255,0.85);
      box-shadow: 0 10px 20px rgba(16,24,40,0.06);
      color: var(--text) !important;
    }

    /* hero */
    .hero{ padding:52px 0 18px; position: relative; z-index: 3; }
    .hero-grid{
      display:grid;
      grid-template-columns: 1.18fr 0.82fr;
      gap: 22px;
      align-items: start;
    }
    .pill{
      display:inline-flex;
      gap:10px;
      align-items:center;
      padding:9px 12px;
      border-radius: 999px;
      border:1px solid rgba(15,61,94,0.16);
      background: rgba(255,255,255,0.60);
      color: var(--muted);
      font-weight:800;
      font-size:13px;
      backdrop-filter: blur(10px);
    }
    .pill strong{ color: var(--brand); }
    .hero-title{
      margin:14px 0 10px;
      font-size: clamp(30px, 4.2vw, 48px);
      line-height: 1.06;
      letter-spacing: -0.8px;
    }
    .hero-desc{
      color: var(--muted);
      font-size: 16px;
      line-height: 1.65;
      max-width: 64ch;
    }

    .hero-actions{ display:flex; gap:12px; margin:18px 0 18px; flex-wrap:wrap; }
    .btn{
      border-radius: 16px;
      padding:12px 16px;
      font-weight:900;
      border:1px solid var(--line);
      display:inline-flex;
      align-items:center;
      justify-content:center;
      gap:10px;
    }
    .btn.primary{
      border:none;
      color:#fff;
      background: linear-gradient(135deg, rgba(15,61,94,1), rgba(14,165,164,1));
      box-shadow: 0 16px 30px rgba(15,61,94,0.18);
    }
    .btn.gold{
      border:none;
      color:#fff;
      background: linear-gradient(135deg, rgba(192,138,47,1), rgba(15,61,94,0.92));
      box-shadow: 0 16px 30px rgba(192,138,47,0.18);
    }
    .btn.ghost{
      background: rgba(255,255,255,0.80);
      box-shadow: 0 10px 18px rgba(16,24,40,0.06);
    }
    .btn.full{ width:100%; }

    .trust{
      display:grid;
      grid-template-columns: repeat(3, minmax(0,1fr));
      gap:12px;
      margin-top: 10px;
    }
    .trust-item{
      background: var(--card);
      border:1px solid var(--line);
      border-radius: var(--radius);
      padding:12px 12px;
      box-shadow: 0 10px 20px rgba(16,24,40,0.06);
    }
    .trust-num{ font-weight:900; color: var(--brand); }
    .trust-label{ color:var(--muted); font-size:13px; margin-top:4px; }

    /* cards */
    .card{
      background: var(--card);
      border:1px solid var(--line);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      overflow:hidden;
      position: relative;
    }
    .card-head{ padding:18px 18px 0; }
    .card-title{ margin:0; font-size:18px; font-weight:900; letter-spacing:-0.2px; }
    .card-sub{ margin:6px 0 0; color:var(--muted); font-size:13px; }

    .impact-card::before{
      content:"";
      position:absolute;
      inset:-2px;
      background:
        radial-gradient(700px 320px at 20% 10%, rgba(192,138,47,0.20), transparent 55%),
        radial-gradient(520px 260px at 95% 30%, rgba(15,61,94,0.16), transparent 55%),
        radial-gradient(560px 240px at 60% 85%, rgba(14,165,164,0.14), transparent 60%);
      opacity: 0.95;
      pointer-events:none;
    }
    .impact-card > *{ position: relative; z-index: 1; }

    .stat-grid{
      padding: 14px 18px 0;
      display:grid;
      grid-template-columns: repeat(3, minmax(0,1fr));
      gap: 10px;
    }
    .stat{
      border: 1px solid var(--line);
      background: rgba(255,255,255,0.72);
      border-radius: 16px;
      padding: 12px;
      box-shadow: 0 10px 18px rgba(16,24,40,0.06);
    }
    .stat-num{ font-weight: 900; color: var(--brand); }
    .stat-label{ margin-top: 4px; color: var(--muted); font-size: 12.5px; line-height: 1.45; }

    .impact-row{
      padding: 14px 18px 18px;
      display:grid;
      gap:12px;
    }
    .impact-item{
      display:flex;
      gap: 12px;
      align-items:flex-start;
      border: 1px solid var(--line);
      background: rgba(255,255,255,0.72);
      border-radius: 16px;
      padding: 12px;
      box-shadow: 0 10px 18px rgba(16,24,40,0.06);
    }
    .check{
      width: 28px;
      height: 28px;
      border-radius: 10px;
      display:grid;
      place-items:center;
      font-weight: 900;
      color: #0b1220;
      background: linear-gradient(135deg, rgba(192,138,47,0.25), rgba(14,165,164,0.16));
      border: 1px solid rgba(192,138,47,0.22);
      flex: 0 0 auto;
    }
    .impact-title{ font-weight: 900; letter-spacing: -0.2px; }
    .impact-desc{ margin-top: 4px; color: var(--muted); font-size: 13px; line-height: 1.5; }

    /* Human statue/person illustration */
    .statue-wrap{
      margin-top: 14px;
      border: 1px solid var(--line);
      border-radius: 18px;
      background: rgba(255,255,255,0.65);
      overflow:hidden;
    }
    .statue-cap{
      padding: 10px 12px;
      border-top: 1px solid var(--line);
      color: var(--muted);
      font-size: 12.5px;
      font-weight: 800;
    }
    .statue{
      width:100%;
      display:block;
    }

    /* sections */
    .section{ padding: 56px 0; position: relative; z-index: 3; }
    .section.alt{
      background: rgba(255,255,255,0.52);
      border-top:1px solid var(--line);
      border-bottom:1px solid var(--line);
      backdrop-filter: blur(10px);
    }
    .section-head{ margin-bottom: 22px; }
    .section-head h2{ margin:0 0 8px; font-size: 28px; font-weight: 900; letter-spacing:-0.3px; }
    .section-head p{ margin:0; color:var(--muted); max-width: 78ch; line-height:1.65; }

    .grid-3{
      display:grid;
      grid-template-columns: repeat(3, minmax(0,1fr));
      gap: 14px;
    }
    .info-card, .program-card{
      background: var(--card);
      border:1px solid var(--line);
      border-radius: var(--radius);
      padding: 16px;
      box-shadow: 0 10px 20px rgba(16,24,40,0.06);
    }
    .info-card h3, .program-card h3{ margin:0 0 8px; font-weight: 900; }
    .info-card p, .program-card p{ margin:0; color:var(--muted); line-height:1.65; }

    .board-grid{
      display:grid;
      grid-template-columns: repeat(5, minmax(0,1fr));
      gap: 12px;
    }
    .board-card{
      background: var(--card);
      border:1px solid var(--line);
      border-radius: 18px;
      padding: 14px;
      box-shadow: 0 10px 20px rgba(16,24,40,0.06);
    }
    .role{
      color: var(--muted);
      font-weight:900;
      font-size: 12px;
      text-transform: uppercase;
      letter-spacing: 0.6px;
    }
    .name{ margin-top: 6px; font-weight:900; }

    /* contact */
    .contact-grid{
      display:grid;
      grid-template-columns: 0.9fr 1.1fr;
      gap: 14px;
    }
    .contact-card, .form-card{
      background: var(--card);
      border:1px solid var(--line);
      border-radius: var(--radius);
      padding: 16px;
      box-shadow: 0 10px 20px rgba(16,24,40,0.06);
    }
    .small{ color: var(--muted); font-size: 12.5px; line-height: 1.55; }

    label{ display:grid; gap:6px; margin-bottom: 12px; }
    input, textarea{
      border:1px solid var(--line);
      border-radius: 14px;
      padding: 12px 12px;
      font: inherit;
      outline: none;
      background: rgba(255,255,255,0.9);
    }
    input:focus, textarea:focus{
      border-color: rgba(14,165,164,0.45);
      box-shadow: 0 0 0 4px rgba(14,165,164,0.12);
    }

    .footer{
      padding: 26px 0;
      border-top: 1px solid var(--line);
      background: rgba(255,255,255,0.60);
      backdrop-filter: blur(10px);
      position: relative;
      z-index: 3;
    }
    .footer-inner{
      display:flex;
      align-items:flex-start;
      justify-content:space-between;
      gap: 14px;
      flex-wrap: wrap;
    }
    .footer-title{ font-weight: 900; }
    .footer-sub{ color: var(--muted); font-size: 13px; margin-top: 4px; }
    .footer-links{ display:flex; gap: 14px; color: var(--muted); font-weight: 900; font-size: 14px; }
    .footer-links a:hover{ color: var(--text); }
    .footer-bottom{ margin-top: 12px; color: var(--muted); font-size: 13px; }

    @media (max-width: 980px){
      .hero-grid{ grid-template-columns: 1fr; }
      .board-grid{ grid-template-columns: repeat(2, minmax(0,1fr)); }
      .grid-3{ grid-template-columns: 1fr; }
      .contact-grid{ grid-template-columns: 1fr; }
      .stat-grid{ grid-template-columns: 1fr; }
      .nav{ display:none; }
    }
  </style>
</head>

<body>
  <!-- Top Bar -->
  <div class="topbar">
    <div class="container topbar-inner">
      <div class="topbar-left">
        <span class="dot"></span>
        <span data-i18n="tagline">Built with unity, dignity, and respect</span>
      </div>

      <div class="topbar-right">
        <button class="lang-btn active" id="lang-en" aria-label="English">EN</button>
        <button class="lang-btn" id="lang-so" aria-label="Somali">SO</button>
      </div>
    </div>
  </div>

  <!-- Header -->
  <header class="header">
    <div class="container header-inner">
      <a class="brand" href="#home" aria-label="Home">
        <div class="brand-mark" aria-hidden="true">MSBC</div>
        <div class="brand-text">
          <div class="brand-title" data-i18n="orgName">Milwaukee Somali Bantu Community Organization</div>
          <div class="brand-sub" data-i18n="orgType">Nonprofit • Milwaukee, Wisconsin • Since 2003</div>
        </div>
      </a>

      <nav class="nav" aria-label="Primary">
        <a href="#about" data-i18n="navAbout">About</a>
        <a href="#programs" data-i18n="navPrograms">Programs</a>
        <a href="#board" data-i18n="navBoard">Board</a>
        <a href="#contact" class="nav-cta" data-i18n="navContact">Contact</a>
      </nav>
    </div>
  </header>

  <!-- Hero -->
  <main id="home" class="hero">
    <div class="container hero-grid">
      <section class="hero-left">
        <div class="pill">
          <span data-i18n="since">Since 2003</span>
          <span>•</span>
          <strong data-i18n="pillStrong">Serving the community based on need</strong>
        </div>

        <h1 class="hero-title" data-i18n="heroTitle">
          Standing for what our community needs — built with unity, dignity, and respect.
        </h1>

        <p class="hero-desc" data-i18n="heroDesc">
          We support the Somali Bantu community in Milwaukee through human rights advocacy and social services.
          Our work includes resettlement support, youth sports, family & children services, referrals, and community programs.
        </p>

        <div class="hero-actions">
          <a class="btn primary" href="#contact" data-i18n="btnGetHelp">Get Help</a>
          <a class="btn ghost" href="#programs" data-i18n="btnExplore">Explore Programs</a>
          <a class="btn gold" href="tel:4142045297" aria-label="Call 4142045297">Call: 414-204-5297</a>
        </div>

        <div class="trust">
          <div class="trust-item">
            <div class="trust-num" data-i18n="t1Num">Since 2003</div>
            <div class="trust-label" data-i18n="t1">Community-led nonprofit service</div>
          </div>
          <div class="trust-item">
            <div class="trust-num" data-i18n="t2Num">Support</div>
            <div class="trust-label" data-i18n="t2">Resettlement, youth, and family services</div>
          </div>
          <div class="trust-item">
            <div class="trust-num" data-i18n="t3Num">Advocacy</div>
            <div class="trust-label" data-i18n="t3">Human rights & community protection</div>
          </div>
        </div>
      </section>

      <!-- Right side: Impact card + Human statue -->
      <aside class="hero-right">
        <div class="card impact-card">
          <div class="card-head">
            <h2 class="card-title" data-i18n="impactTitle">Our Promise</h2>
            <p class="card-sub" data-i18n="impactSub">We help, we advocate, and we serve with respect.</p>
          </div>

          <div class="stat-grid">
            <div class="stat">
              <div class="stat-num" data-i18n="s1">Human Rights</div>
              <div class="stat-label" data-i18n="s1d">Advocacy, referrals, and protection support</div>
            </div>
            <div class="stat">
              <div class="stat-num" data-i18n="s2">Resettlement</div>
              <div class="stat-label" data-i18n="s2d">Guidance for families and newcomers</div>
            </div>
            <div class="stat">
              <div class="stat-num" data-i18n="s3">Youth Sports</div>
              <div class="stat-label" data-i18n="s3d">Mentorship, leadership, and teamwork</div>
            </div>
          </div>

          <div class="impact-row">
            <div class="impact-item">
              <div class="check">✓</div>
              <div>
                <div class="impact-title" data-i18n="p1">Need-first service</div>
                <div class="impact-desc" data-i18n="p1d">We serve based on what the people need — not assumptions.</div>
              </div>
            </div>

            <div class="impact-item">
              <div class="check">✓</div>
              <div>
                <div class="impact-title" data-i18n="p2">Unity, dignity, respect</div>
                <div class="impact-desc" data-i18n="p2d">We protect dignity and strengthen community voice.</div>
              </div>
            </div>

            <!-- Human statue/person (SVG) -->
            <div class="statue-wrap" aria-label="Human statue illustration">
              <svg class="statue" viewBox="0 0 640 360" role="img" aria-hidden="true">
                <defs>
                  <linearGradient id="g1" x1="0" x2="1">
                    <stop offset="0" stop-color="rgba(15,61,94,0.95)"/>
                    <stop offset="1" stop-color="rgba(192,138,47,0.90)"/>
                  </linearGradient>
                  <radialGradient id="glow" cx="50%" cy="30%" r="70%">
                    <stop offset="0" stop-color="rgba(14,165,164,0.16)"/>
                    <stop offset="1" stop-color="rgba(14,165,164,0)"/>
                  </radialGradient>
                </defs>

                <rect width="640" height="360" fill="rgba(255,255,255,0.0)"/>
                <circle cx="420" cy="130" r="160" fill="url(#glow)"/>

                <!-- pedestal -->
                <rect x="160" y="290" width="320" height="28" rx="12" fill="rgba(15,23,42,0.10)"/>
                <rect x="210" y="270" width="220" height="22" rx="12" fill="rgba(15,23,42,0.12)"/>

                <!-- statue silhouette -->
                <g transform="translate(0,0)">
                  <!-- head -->
                  <circle cx="320" cy="110" r="38" fill="url(#g1)" opacity="0.95"/>
                  <!-- body -->
                  <path d="M290 150
                           C270 170, 260 210, 260 245
                           C260 285, 285 305, 320 305
                           C355 305, 380 285, 380 245
                           C380 210, 370 170, 350 150
                           C342 160, 331 166, 320 166
                           C309 166, 298 160, 290 150 Z"
                        fill="url(#g1)" opacity="0.95"/>
                  <!-- shoulders/arms -->
                  <path d="M260 200
                           C230 210, 205 230, 195 255
                           C190 268, 198 277, 210 275
                           C235 270, 250 250, 268 240 Z"
                        fill="rgba(15,61,94,0.85)"/>
                  <path d="M380 200
                           C410 210, 435 230, 445 255
                           C450 268, 442 277, 430 275
                           C405 270, 390 250, 372 240 Z"
                        fill="rgba(192,138,47,0.82)"/>
                  <!-- inner highlight -->
                  <path d="M320 166
                           C300 166, 288 188, 288 220
                           C288 260, 302 288, 320 288
                           C338 288, 352 260, 352 220
                           C352 188, 340 166, 320 166 Z"
                        fill="rgba(255,255,255,0.10)"/>
                </g>
              </svg>

              <div class="statue-cap" data-i18n="statueCap">A symbol of dignity, strength, and community.</div>
            </div>

            <a class="btn ghost full" href="#programs" data-i18n="impactBtn">See Programs</a>
          </div>
        </div>
      </aside>
    </div>
  </main>

  <!-- About -->
  <section id="about" class="section">
    <div class="container">
      <div class="section-head">
        <h2 data-i18n="aboutTitle">About Us</h2>
        <p data-i18n="aboutDesc">
          We are a Milwaukee-based nonprofit organization serving since 2003. We stand for what our community needs and what the people need.
          Our work is built on unity, dignity, and respect.
        </p>
      </div>

      <div class="grid-3">
        <div class="info-card">
          <h3 data-i18n="missionTitle">Mission</h3>
          <p data-i18n="missionDesc">
            To empower the Somali Bantu community in Milwaukee through advocacy, services, and programs that create opportunity and wellbeing.
          </p>
        </div>

        <div class="info-card">
          <h3 data-i18n="visionTitle">Vision</h3>
          <p data-i18n="visionDesc">
            A safe, thriving, respected community where families have access to support and a strong voice.
          </p>
        </div>

        <div class="info-card">
          <h3 data-i18n="valuesTitle">Values</h3>
          <p data-i18n="valuesDesc">
            Unity, dignity, respect, service, integrity, transparency, and accountability.
          </p>
        </div>
      </div>
    </div>
  </section>

  <!-- Programs -->
  <section id="programs" class="section alt">
    <div class="container">
      <div class="section-head">
        <h2 data-i18n="programsTitle">Programs & Services</h2>
        <p data-i18n="programsDesc">
          We provide support across multiple areas. If you need help, contact us and we will guide you to the right service.
        </p>
      </div>

      <div class="grid-3">
        <div class="program-card">
          <h3 data-i18n="prog1Title">Human Rights Advocacy</h3>
          <p data-i18n="prog1Desc">Support, referrals, and community education to protect civil rights and dignity.</p>
        </div>
        <div class="program-card">
          <h3 data-i18n="prog2Title">Resettlement Support</h3>
          <p data-i18n="prog2Desc">Guidance with resources, interpretation support, local referrals, and navigation.</p>
        </div>
        <div class="program-card">
          <h3 data-i18n="prog3Title">Community Services</h3>
          <p data-i18n="prog3Desc">Forms help, referrals, case support, and connecting families to services.</p>
        </div>
        <div class="program-card">
          <h3 data-i18n="prog4Title">Youth Sports</h3>
          <p data-i18n="prog4Desc">Sports programs and mentorship that promote leadership and wellbeing.</p>
        </div>
        <div class="program-card">
          <h3 data-i18n="prog5Title">Family & Children Services</h3>
          <p data-i18n="prog5Desc">Support and referrals for families, children, and youth wellbeing.</p>
        </div>
        <div class="program-card">
          <h3 data-i18n="prog6Title">Community Engagement</h3>
          <p data-i18n="prog6Desc">Outreach, partnerships, workshops, and community-led initiatives.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Board -->
  <section id="board" class="section">
    <div class="container">
      <div class="section-head">
        <h2 data-i18n="boardTitle">Board & Leadership</h2>
        <p data-i18n="boardDesc">Our leadership team serves with transparency, service, and accountability.</p>
      </div>

      <div class="board-grid">
        <div class="board-card"><div class="role" data-i18n="presRole">President</div><div class="name">Mohamed Sidi</div></div>
        <div class="board-card"><div class="role" data-i18n="vpRole">Vice President</div><div class="name">Sheikh Abdishakur Ali</div></div>
        <div class="board-card"><div class="role" data-i18n="secRole">Secretary</div><div class="name">Abdinasser Omar</div></div>
        <div class="board-card"><div class="role" data-i18n="edRole">Executive Director</div><div class="name">Sheiknoor Adan</div></div>
        <div class="board-card"><div class="role" data-i18n="aedRole">Assistant Executive Director</div><div class="name">Nuurto Jeylani</div></div>
        <div class="board-card"><div class="role" data-i18n="treRole">Treasury</div><div class="name">Anab Aden</div></div>
        <div class="board-card"><div class="role" data-i18n="pcRole">Program Coordinator</div><div class="name">Jafar Hussien</div></div>
        <div class="board-card"><div class="role" data-i18n="apcRole">Assistant Program Coordinator</div><div class="name">Mohamed Omar</div></div>
        <div class="board-card"><div class="role" data-i18n="fcRole">Family & Children Coordinator</div><div class="name">Fatuma Sharif</div></div>
        <div class="board-card"><div class="role" data-i18n="spRole">Spokesperson</div><div class="name">Muktar Hussien</div></div>
      </div>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact" class="section alt">
    <div class="container">
      <div class="section-head">
        <h2 data-i18n="contactTitle">Contact</h2>
        <p data-i18n="contactDesc">
          Tell us what you need help with. We will respond as soon as possible.
        </p>
      </div>

      <div class="contact-grid">
        <div class="contact-card">
          <h3 data-i18n="contactInfoTitle">Organization Info</h3>
          <p><strong data-i18n="locationLabel">Location:</strong> <span data-i18n="locationValue">Milwaukee, Wisconsin</span></p>
          <p><strong data-i18n="phoneLabel">Phone:</strong> <a href="tel:4142045297">414-204-5297</a></p>
          <p><strong data-i18n="emailLabel">Email:</strong> yourname@example.org</p>
          <p class="small" data-i18n="contactNote">Replace the email with your official nonprofit email anytime.</p>
        </div>

        <form class="form-card" onsubmit="return false;">
          <label>
            <span data-i18n="formName">Name</span>
            <input type="text" placeholder="Your name" />
          </label>
          <label>
            <span data-i18n="formEmail">Email</span>
            <input type="email" placeholder="you@email.com" />
          </label>
          <label>
            <span data-i18n="formMessage">Message</span>
            <textarea rows="5" placeholder="How can we help?"></textarea>
          </label>
          <button class="btn primary full" type="submit" data-i18n="formBtn">Send Message</button>
          <p class="small" data-i18n="formHint">This form is a demo (not sending yet). Tell me if you want it to send to your email.</p>
        </form>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="footer">
    <div class="container footer-inner">
      <div>
        <div class="footer-title" data-i18n="orgName">Milwaukee Somali Bantu Community Organization</div>
        <div class="footer-sub" data-i18n="footerSub">Nonprofit • Milwaukee, Wisconsin • Since 2003</div>
      </div>
      <div class="footer-links">
        <a href="#about" data-i18n="navAbout">About</a>
        <a href="#programs" data-i18n="navPrograms">Programs</a>
        <a href="#board" data-i18n="navBoard">Board</a>
        <a href="#contact" data-i18n="navContact">Contact</a>
      </div>
    </div>
    <div class="container footer-bottom">
      <span>© <span id="year"></span> <span data-i18n="orgName">Milwaukee Somali Bantu Community Organization</span></span>
    </div>
  </footer>

  <script>
    const dict = {
      en: {
        tagline: "Built with unity, dignity, and respect",
        orgName: "Milwaukee Somali Bantu Community Organization",
        orgType: "Nonprofit • Milwaukee, Wisconsin • Since 2003",
        navAbout: "About",
        navPrograms: "Programs",
        navBoard: "Board",
        navContact: "Contact",

        since: "Since 2003",
        pillStrong: "Serving the community based on need",

        heroTitle: "Standing for what our community needs — built with unity, dignity, and respect.",
        heroDesc: "We support the Somali Bantu community in Milwaukee through human rights advocacy and social services. Our work includes resettlement support, youth sports, family & children services, referrals, and community programs.",
        btnGetHelp: "Get Help",
        btnExplore: "Explore Programs",

        t1Num: "Since 2003",
        t1: "Community-led nonprofit service",
        t2Num: "Support",
        t2: "Resettlement, youth, and family services",
        t3Num: "Advocacy",
        t3: "Human rights & community protection",

        impactTitle: "Our Promise",
        impactSub: "We help, we advocate, and we serve with respect.",
        s1: "Human Rights",
        s1d: "Advocacy, referrals, and protection support",
        s2: "Resettlement",
        s2d: "Guidance for families and newcomers",
        s3: "Youth Sports",
        s3d: "Mentorship, leadership, and teamwork",
        p1: "Need-first service",
        p1d: "We serve based on what the people need — not assumptions.",
        p2: "Unity, dignity, respect",
        p2d: "We protect dignity and strengthen community voice.",
        statueCap: "A symbol of dignity, strength, and community.",
        impactBtn: "See Programs",

        aboutTitle: "About Us",
        aboutDesc: "We are a Milwaukee-based nonprofit organization serving since 2003. We stand for what our community needs and what the people need. Our work is built on unity, dignity, and respect.",
        missionTitle: "Mission",
        missionDesc: "To empower the Somali Bantu community in Milwaukee through advocacy, services, and programs that create opportunity and wellbeing.",
        visionTitle: "Vision",
        visionDesc: "A safe, thriving, respected community where families have access to support and a strong voice.",
        valuesTitle: "Values",
        valuesDesc: "Unity, dignity, respect, service, integrity, transparency, and accountability.",

        programsTitle: "Programs & Services",
        programsDesc: "We provide support across multiple areas. If you need help, contact us and we will guide you to the right service.",
        prog1Title: "Human Rights Advocacy",
        prog1Desc: "Support, referrals, and community education to protect civil rights and dignity.",
        prog2Title: "Resettlement Support",
        prog2Desc: "Guidance with resources, interpretation support, local referrals, and navigation.",
        prog3Title: "Community Services",
        prog3Desc: "Forms help, referrals, case support, and connecting families to services.",
        prog4Title: "Youth Sports",
        prog4Desc: "Sports programs and mentorship that promote leadership and wellbeing.",
        prog5Title: "Family & Children Services",
        prog5Desc: "Support and referrals for families, children, and youth wellbeing.",
        prog6Title: "Community Engagement",
        prog6Desc: "Outreach, partnerships, workshops, and community-led initiatives.",

        boardTitle: "Board & Leadership",
        boardDesc: "Our leadership team serves with transparency, service, and accountability.",
        presRole: "President",
        vpRole: "Vice President",
        secRole: "Secretary",
        edRole: "Executive Director",
        aedRole: "Assistant Executive Director",
        treRole: "Treasury",
        pcRole: "Program Coordinator",
        apcRole: "Assistant Program Coordinator",
        fcRole: "Family & Children Coordinator",
        spRole: "Spokesperson",

        contactTitle: "Contact",
        contactDesc: "Tell us what you need help with. We will respond as soon as possible.",
        contactInfoTitle: "Organization Info",
        locationLabel: "Location:",
        locationValue: "Milwaukee, Wisconsin",
        emailLabel: "Email:",
        phoneLabel: "Phone:",
        contactNote: "Replace the email with your official nonprofit email anytime.",
        formName: "Name",
        formEmail: "Email",
        formMessage: "Message",
        formBtn: "Send Message",
        formHint: "This form is a demo (not sending yet). Tell me if you want it to send to your email.",
        footerSub: "Nonprofit • Milwaukee, Wisconsin • Since 2003"
      },

      so: {
        tagline: "Waxaa lagu dhisay midnimo, karaamo, iyo ixtiraam",
        orgName: "Ururka Bulshada Soomaali Bantu ee Milwaukee",
        orgType: "Hay’ad Samafal • Milwaukee, Wisconsin • Tan iyo 2003",

        navAbout: "Ku Saabsan",
        navPrograms: "Barnaamijyada",
        navBoard: "Hoggaanka",
        navContact: "Xiriir",

        since: "Tan iyo 2003",
        pillStrong: "U adeegidda bulshada iyadoo lagu saleynayo baahida",

        heroTitle: "Waxaan u taaganahay waxa bulshadeennu u baahan tahay — midnimo, karaamo, iyo ixtiraam.",
        heroDesc: "Waxaan taageernaa bulshada Soomaali Bantu ee Milwaukee annagoo bixinna u-doodid xuquuqda aadanaha iyo adeegyo bulsho. Shaqadeennu waxay ka koobantahay dib-u-dejin, ciyaaro dhalinyaro, adeegyo qoys & carruur, gudbin, iyo barnaamijyo bulsho.",
        btnGetHelp: "Hel Caawimaad",
        btnExplore: "Eeg Barnaamijyada",

        t1Num: "Tan iyo 2003",
        t1: "Hay’ad bulsho hoggaamiso",
        t2Num: "Taageero",
        t2: "Dib-u-dejin, dhalinyaro, iyo adeegyo qoys",
        t3Num: "U-doodid",
        t3: "Xuquuqda aadanaha & ilaalinta bulshada",

        impactTitle: "Ballanqaadkeenna",
        impactSub: "Waan caawinnaa, waan u doodnaa, waxaana u adeegnaa si ixtiraam leh.",
        s1: "Xuquuqda Aadanaha",
        s1d: "U-doodid, gudbin, iyo taageero ilaalin",
        s2: "Dib-u-dejin",
        s2d: "Hagid qoysas iyo dadka cusub",
        s3: "Ciyaaraha Dhalinyarada",
        s3d: "Hagid, hoggaan, iyo wada-shaqayn",
        p1: "Adeeg ku saleysan baahi",
        p1d: "Waxaan u adeegnaa sida ay dadku u baahan yihiin — ma aha qiyaas.",
        p2: "Midnimo, karaamo, ixtiraam",
        p2d: "Waxaan ilaalinaa karaamada oo xoojinnaa codka bulshada.",
        statueCap: "Astaanta karaamo, adkaysi, iyo bulsho.",
        impactBtn: "Eeg Barnaamijyada",

        aboutTitle: "Ku Saabsan",
        aboutDesc: "Waxaan nahay hay’ad samafal oo fadhigeedu yahay Milwaukee oo u adeegta tan iyo 2003. Waxaan u taaganahay waxa bulshadeennu u baahan tahay iyo waxa dadka u baahan yihiin. Shaqadeennu waxay ku dhisan tahay midnimo, karaamo, iyo ixtiraam.",
        missionTitle: "Himiladeenna",
        missionDesc: "Inaan awood-siino bulshada Soomaali Bantu ee Milwaukee annagoo u marayna u-doodid, adeegyo, iyo barnaamijyo fura fursado iyo nolol-wanaag.",
        visionTitle: "Aragtideenna",
        visionDesc: "Bulsho ammaan ah, kobcaysa, oo la ixtiraamo—qoysaskuna helaan taageero iyo cod xooggan.",
        valuesTitle: "Qiyamkeenna",
        valuesDesc: "Midnimo, karaamo, ixtiraam, adeeg, daacadnimo, daahfurnaan, iyo isla-xisaabtan.",

        programsTitle: "Barnaamijyada & Adeegyada",
        programsDesc: "Waxaan bixinnaa taageero dhinacyo badan. Haddii aad u baahan tahay caawimo, nala soo xiriir—waan ku hagaynaa adeegga ku habboon.",
        prog1Title: "U-doodista Xuquuqda Aadanaha",
        prog1Desc: "Taageero, gudbin, iyo wacyigelin si loo ilaaliyo xuquuqda iyo karaamada.",
        prog2Title: "Taageerada Dib-u-dejinta",
        prog2Desc: "Hagid kheyraad, taageero luqadeed, gudbin, iyo hagitaan.",
        prog3Title: "Adeegyada Bulshada",
        prog3Desc: "Caawin foomam, gudbin, taageero kiis, iyo isku-xir adeegyo.",
        prog4Title: "Ciyaaraha Dhalinyarada",
        prog4Desc: "Barnaamijyo ciyaareed iyo hagid si loo dhiso hoggaan iyo nolol-wanaag.",
        prog5Title: "Adeegyada Qoyska & Carruurta",
        prog5Desc: "Taageero iyo gudbin qoysaska, carruurta, iyo daryeelka dhalinyarada.",
        prog6Title: "Ka-Qaybgalka Bulshada",
        prog6Desc: "Wacyigelin, iskaashi, tababarro, iyo hawlo bulsho hoggaamiso.",

        boardTitle: "Hoggaanka & Guddiga",
        boardDesc: "Hoggaankeenna wuxuu u adeegaa si daahfuran, adeeg, iyo isla-xisaabtan leh.",
        presRole: "Guddoomiye",
        vpRole: "Guddoomiye Ku-xigeen",
        secRole: "Xoghayn",
        edRole: "Agaasimaha Fulinta",
        aedRole: "Ku-xigeenka Agaasimaha Fulinta",
        treRole: "Khasnajiga",
        pcRole: "Isku-duwaha Barnaamijyada",
        apcRole: "Kaaliyaha Isku-duwaha Barnaamijyada",
        fcRole: "Isku-duwaha Qoyska & Carruurta",
        spRole: "Afhayeen",

        contactTitle: "Xiriir",
        contactDesc: "Noo sheeg caawimada aad u baahan tahay. Waxaan kuu soo jawaabi doonnaa sida ugu dhakhsaha badan.",
        contactInfoTitle: "Macluumaadka Hay’adda",
        locationLabel: "Goobta:",
        locationValue: "Milwaukee, Wisconsin",
        emailLabel: "Iimayl:",
        phoneLabel: "Telefoon:",
        contactNote: "Beddel iimaylka si uu u noqdo iimaylka rasmiga ah ee hay’adda.",
        formName: "Magaca",
        formEmail: "Iimayl",
        formMessage: "Fariin",
        formBtn: "Dir Fariinta",
        formHint: "Foomkan ma dirayo hadda. Haddii aad rabto, waan ku xirin karaa iimaylkaaga.",
        footerSub: "Hay’ad Samafal • Milwaukee, Wisconsin • Tan iyo 2003"
      }
    };

    function setLang(lang){
      document.querySelectorAll("[data-i18n]").forEach(el=>{
        const key = el.getAttribute("data-i18n");
        if(dict[lang] && dict[lang][key]) el.textContent = dict[lang][key];
      });

      document.getElementById("lang-en").classList.toggle("active", lang === "en");
      document.getElementById("lang-so").classList.toggle("active", lang === "so");
      localStorage.setItem("msbc_lang", lang);
      document.documentElement.lang = (lang === "so") ? "so" : "en";
    }

    document.getElementById("year").textContent = new Date().getFullYear();
    document.getElementById("lang-en").addEventListener("click", ()=>setLang("en"));
    document.getElementById("lang-so").addEventListener("click", ()=>setLang("so"));
    setLang(localStorage.getItem("msbc_lang") || "en");
  </script>
</body>
</html>

<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Milwaukee Somali Bantu Community Organization</title>
  <meta name="description" content="A nonprofit serving the Somali Bantu community in Milwaukee through human rights advocacy and social services." />

  <style>
    :root{
      --bg: #fbfcfe;
      --card: #ffffff;
      --text: #0b1220;
      --muted: #475467;
      --line: rgba(15, 23, 42, 0.08);
      --brand: #2563eb;
      --brand2: #06b6d4;
      --shadow: 0 18px 55px rgba(16,24,40,0.10);
      --radius: 18px;
    }

    *{ box-sizing: border-box; }
    a{ color:inherit; text-decoration:none; }
    img{ max-width:100%; display:block; }

    html,body{
      margin:0;
      padding:0;
      font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Arial;
      color:var(--text);
      background:
        radial-gradient(1200px 600px at 12% 6%, rgba(37,99,235,0.14), transparent 60%),
        radial-gradient(900px 520px at 88% 18%, rgba(6,182,212,0.14), transparent 55%),
        radial-gradient(720px 420px at 40% 92%, rgba(37,99,235,0.08), transparent 55%),
        linear-gradient(180deg, #ffffff 0%, #fbfcfe 30%, #f6f8ff 100%);
    }

    body::before{
      content:"";
      position: fixed;
      inset: 0;
      pointer-events: none;
      background:
        radial-gradient(circle at 1px 1px, rgba(15,23,42,0.06) 1px, transparent 1px);
      background-size: 28px 28px;
      opacity: 0.25;
      mask-image: radial-gradient(900px 500px at 20% 10%, #000 40%, transparent 70%);
    }

    .container{ width:min(1120px, calc(100% - 32px)); margin:0 auto; }

    .topbar{
      background: linear-gradient(90deg, rgba(37,99,235,0.10), rgba(6,182,212,0.10));
      border-bottom: 1px solid var(--line);
      position: relative;
      z-index: 2;
    }
    .topbar-inner{ display:flex; align-items:center; justify-content:space-between; padding:10px 0; gap:12px; }
    .topbar-left{ display:flex; align-items:center; gap:10px; color:var(--muted); font-size:14px; }
    .dot{ width:9px; height:9px; border-radius:50%; background:var(--brand); box-shadow: 0 0 0 6px rgba(37,99,235,0.12); }

    .lang-btn{
      border:1px solid var(--line);
      background: rgba(255,255,255,0.85);
      color: var(--muted);
      padding:7px 10px;
      border-radius: 12px;
      cursor:pointer;
      font-weight:700;
    }
    .lang-btn.active{
      border-color: rgba(37,99,235,0.35);
      color: var(--text);
      box-shadow: 0 8px 20px rgba(37,99,235,0.10);
    }

    .header{
      position: sticky;
      top:0;
      background: rgba(251,252,254,0.86);
      backdrop-filter: blur(12px);
      border-bottom:1px solid var(--line);
      z-index: 10;
    }
    .header-inner{ display:flex; align-items:center; justify-content:space-between; padding:14px 0; gap:16px; }

    .brand{ display:flex; align-items:center; gap:12px; position: relative; z-index: 2; }
    .brand-mark{
      width:44px; height:44px;
      border-radius: 14px;
      display:grid; place-items:center;
      font-weight:900;
      background: linear-gradient(135deg, rgba(37,99,235,0.95), rgba(6,182,212,0.9));
      color:#fff;
      box-shadow: 0 12px 25px rgba(37,99,235,0.20);
      letter-spacing: -0.3px;
    }
    .brand-title{ font-weight:900; letter-spacing:-0.2px; }
    .brand-sub{ font-size:13px; color:var(--muted); margin-top:2px; }

    .nav{ display:flex; align-items:center; gap:18px; }
    .nav a{ color:var(--muted); font-weight:700; font-size:14px; }
    .nav a:hover{ color:var(--text); }
    .nav-cta{
      padding:10px 14px;
      border-radius: 14px;
      border:1px solid rgba(37,99,235,0.25);
      background: rgba(255,255,255,0.85);
      color: var(--text) !important;
      box-shadow: 0 10px 20px rgba(16,24,40,0.06);
    }

    .hero{ padding:48px 0 22px; position: relative; z-index: 2; }
    .hero-grid{ display:grid; grid-template-columns: 1.25fr 0.75fr; gap:22px; align-items:start; }

    .pill{
      display:inline-flex;
      padding:8px 12px;
      border-radius: 999px;
      border:1px solid rgba(37,99,235,0.18);
      background: rgba(37,99,235,0.06);
      color: var(--muted);
      font-weight:700;
      font-size:13px;
    }

    .hero-title{
      margin:14px 0 10px;
      font-size: clamp(28px, 4vw, 44px);
      line-height:1.08;
      letter-spacing:-0.6px;
    }
    .hero-desc{ color:var(--muted); font-size:16px; line-height:1.6; max-width: 62ch; }

    .hero-actions{ display:flex; gap:12px; margin:18px 0 18px; flex-wrap: wrap; }
    .btn{
      border-radius: 16px;
      padding:12px 16px;
      font-weight:900;
      border:1px solid var(--line);
      display:inline-flex;
      align-items:center;
      justify-content:center;
    }
    .btn.primary{
      background: linear-gradient(135deg, rgba(37,99,235,1), rgba(6,182,212,1));
      color:#fff;
      border:none;
      box-shadow: 0 14px 25px rgba(37,99,235,0.25);
    }
    .btn.ghost{
      background: rgba(255,255,255,0.85);
      color: var(--text);
      box-shadow: 0 10px 20px rgba(16,24,40,0.06);
    }
    .btn.full{ width:100%; }

    .trust{
      display:grid;
      grid-template-columns: repeat(3, minmax(0,1fr));
      gap:12px;
      margin-top: 10px;
    }
    .trust-item{
      background: rgba(255,255,255,0.85);
      border:1px solid var(--line);
      border-radius: var(--radius);
      padding:12px 12px;
      box-shadow: 0 10px 20px rgba(16,24,40,0.05);
    }
    .trust-num{ font-weight:900; }
    .trust-label{ color:var(--muted); font-size:13px; margin-top:4px; }

    .card{
      background: rgba(255,255,255,0.85);
      border:1px solid var(--line);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      overflow:hidden;
      position: relative;
    }
    .card-head{ padding:18px 18px 0; }
    .card-title{ margin:0; font-size:18px; letter-spacing:-0.2px; font-weight: 900; }
    .card-sub{ margin:6px 0 0; color:var(--muted); font-size:13px; }

    .impact-card::before{
      content:"";
      position:absolute;
      inset:-2px;
      background:
        radial-gradient(700px 300px at 20% 10%, rgba(37,99,235,0.18), transparent 55%),
        radial-gradient(520px 260px at 95% 30%, rgba(6,182,212,0.18), transparent 55%);
      filter: blur(2px);
      opacity: 0.9;
      pointer-events:none;
    }
    .impact-card > *{ position: relative; z-index: 1; }

    .impact-stats{
      padding: 14px 18px 0;
      display:grid;
      gap:10px;
    }
    .stat{
      border: 1px solid var(--line);
      background: rgba(255,255,255,0.75);
      border-radius: 16px;
      padding: 12px;
      box-shadow: 0 10px 18px rgba(16,24,40,0.06);
    }
    .stat-num{ font-weight: 900; letter-spacing: -0.2px; }
    .stat-label{ margin-top: 4px; color: var(--muted); font-size: 13px; line-height: 1.45; }

    .impact-list{
      padding: 14px 18px 0;
      display:grid;
      gap: 12px;
    }
    .impact-item{
      display:flex;
      gap: 10px;
      align-items:flex-start;
      border: 1px solid var(--line);
      background: rgba(255,255,255,0.75);
      border-radius: 16px;
      padding: 12px;
      box-shadow: 0 10px 18px rgba(16,24,40,0.06);
    }
    .check{
      width: 26px;
      height: 26px;
      border-radius: 10px;
      display:grid;
      place-items:center;
      font-weight: 900;
      color: #0b1220;
      background: linear-gradient(135deg, rgba(37,99,235,0.22), rgba(6,182,212,0.18));
      border: 1px solid rgba(37,99,235,0.20);
      flex: 0 0 auto;
    }
    .impact-title{ font-weight: 900; letter-spacing: -0.2px; }
    .impact-desc{ margin-top: 4px; color: var(--muted); font-size: 13px; line-height: 1.45; }

    .card-foot{ padding:16px 18px 18px; }

    .section{ padding: 56px 0; position: relative; z-index: 2; }
    .section.alt{
      background: rgba(245,247,251,0.75);
      border-top:1px solid var(--line);
      border-bottom:1px solid var(--line);
      backdrop-filter: blur(6px);
    }
    .section-head{ margin-bottom: 22px; }
    .section-head h2{ margin:0 0 8px; font-size: 28px; letter-spacing:-0.3px; font-weight: 900; }
    .section-head p{ margin:0; color:var(--muted); max-width: 75ch; line-height:1.6; }

    .grid-3{
      display:grid;
      grid-template-columns: repeat(3, minmax(0,1fr));
      gap: 14px;
    }
    .info-card, .program-card{
      background: rgba(255,255,255,0.85);
      border:1px solid var(--line);
      border-radius: var(--radius);
      padding: 16px;
      box-shadow: 0 10px 20px rgba(16,24,40,0.05);
    }
    .info-card h3, .program-card h3{ margin:0 0 8px; font-weight: 900; }
    .info-card p, .program-card p{ margin:0; color:var(--muted); line-height:1.6; }

    .board-grid{
      display:grid;
      grid-template-columns: repeat(5, minmax(0,1fr));
      gap: 12px;
    }
    .board-card{
      background: rgba(255,255,255,0.85);
      border:1px solid var(--line);
      border-radius: 18px;
      padding: 14px;
      box-shadow: 0 10px 20px rgba(16,24,40,0.05);
    }
    .role{ color: var(--muted); font-weight:900; font-size: 12px; text-transform: uppercase; letter-spacing: 0.6px; }
    .name{ margin-top: 6px; font-weight:900; }

    .contact-grid{
      display:grid;
      grid-template-columns: 0.9fr 1.1fr;
      gap: 14px;
    }
    .contact-card, .form-card{
      background: rgba(255,255,255,0.85);
      border:1px solid var(--line);
      border-radius: var(--radius);
      padding: 16px;
      box-shadow: 0 10px 20px rgba(16,24,40,0.05);
    }
    .small{ color: var(--muted); font-size: 12.5px; line-height: 1.5; }

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
      border-color: rgba(37,99,235,0.45);
      box-shadow: 0 0 0 4px rgba(37,99,235,0.10);
    }

    .footer{
      padding: 26px 0;
      border-top: 1px solid var(--line);
      background: rgba(255,255,255,0.75);
      backdrop-filter: blur(6px);
      position: relative;
      z-index: 2;
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
    .footer-links{ display:flex; gap: 14px; color: var(--muted); font-weight: 800; font-size: 14px; }
    .footer-links a:hover{ color: var(--text); }
    .footer-bottom{
      margin-top: 12px;
      color: var(--muted);
      font-size: 13px;
    }

    @media (max-width: 980px){
      .hero-grid{ grid-template-columns: 1fr; }
      .board-grid{ grid-template-columns: repeat(2, minmax(0,1fr)); }
      .grid-3{ grid-template-columns: 1fr; }
      .contact-grid{ grid-template-columns: 1fr; }
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
        <span data-i18n="tagline">Unity • Justice • Dignity</span>
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
          <div class="brand-sub" data-i18n="orgType">Nonprofit • Milwaukee, Wisconsin</div>
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
        <div class="pill" data-i18n="pill">Serving the Somali Bantu community in Milwaukee</div>

        <h1 class="hero-title" data-i18n="heroTitle">
          Human rights advocacy and trusted community services — built with dignity.
        </h1>

        <p class="hero-desc" data-i18n="heroDesc">
          We support families through resettlement help, youth sports, referrals, case support, and community programs.
          We also advocate for civil rights, fair access, and respect for every person.
        </p>

        <div class="hero-actions">
          <a class="btn primary" href="#contact" data-i18n="btnGetHelp">Get Help</a>
          <a class="btn ghost" href="#programs" data-i18n="btnExplore">Explore Programs</a>
        </div>

        <div class="trust">
          <div class="trust-item">
            <div class="trust-num">Milwaukee</div>
            <div class="trust-label" data-i18n="trust1">Community-based nonprofit</div>
          </div>
          <div class="trust-item">
            <div class="trust-num" data-i18n="trust2Num">Support</div>
            <div class="trust-label" data-i18n="trust2">Resettlement & services</div>
          </div>
          <div class="trust-item">
            <div class="trust-num" data-i18n="trust3Num">Advocacy</div>
            <div class="trust-label" data-i18n="trust3">Human rights & protection</div>
          </div>
        </div>
      </section>

      <!-- Right side: Impact card -->
      <aside class="hero-right">
        <div class="card impact-card">
          <div class="card-head">
            <h2 class="card-title" data-i18n="impactTitle">Community Impact</h2>
            <p class="card-sub" data-i18n="impactSub">Practical support. Strong advocacy. Real results.</p>
          </div>

          <div class="impact-stats">
            <div class="stat">
              <div class="stat-num" data-i18n="stat1Num">Advocacy</div>
              <div class="stat-label" data-i18n="stat1Label">Human rights support & referrals</div>
            </div>
            <div class="stat">
              <div class="stat-num" data-i18n="stat2Num">Resettlement</div>
              <div class="stat-label" data-i18n="stat2Label">Guidance for families and newcomers</div>
            </div>
            <div class="stat">
              <div class="stat-num" data-i18n="stat3Num">Youth</div>
              <div class="stat-label" data-i18n="stat3Label">Sports, mentorship, and leadership</div>
            </div>
          </div>

          <div class="impact-list">
            <div class="impact-item">
              <div class="check">✓</div>
              <div>
                <div class="impact-title" data-i18n="impact1Title">Services that meet real needs</div>
                <div class="impact-desc" data-i18n="impact1Desc">Support for forms, referrals, and community navigation.</div>
              </div>
            </div>

            <div class="impact-item">
              <div class="check">✓</div>
              <div>
                <div class="impact-title" data-i18n="impact2Title">Advocacy with dignity</div>
                <div class="impact-desc" data-i18n="impact2Desc">Helping protect rights and promote fair access.</div>
              </div>
            </div>

            <div class="impact-item">
              <div class="check">✓</div>
              <div>
                <div class="impact-title" data-i18n="impact3Title">Community-led leadership</div>
                <div class="impact-desc" data-i18n="impact3Desc">Transparent leadership serving Milwaukee.</div>
              </div>
            </div>
          </div>

          <div class="card-foot">
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
          We are a Milwaukee-based nonprofit dedicated to serving the Somali Bantu community through practical support,
          protection of rights, and community-led programs.
        </p>
      </div>

      <div class="grid-3">
        <div class="info-card">
          <h3 data-i18n="missionTitle">Mission</h3>
          <p data-i18n="missionDesc">
            To strengthen and empower the Somali Bantu community in Milwaukee through human rights advocacy,
            social services, and programs that build opportunity.
          </p>
        </div>
        <div class="info-card">
          <h3 data-i18n="visionTitle">Vision</h3>
          <p data-i18n="visionDesc">
            A safe, thriving, and respected community where families have access, dignity, and a strong voice.
          </p>
        </div>
        <div class="info-card">
          <h3 data-i18n="valuesTitle">Values</h3>
          <p data-i18n="valuesDesc">
            Integrity, service, unity, accountability, and respect for every person.
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
          <p data-i18n="prog1Desc">Support, reporting help, referrals, and community education to protect civil rights and dignity.</p>
        </div>
        <div class="program-card">
          <h3 data-i18n="prog2Title">Resettlement Support</h3>
          <p data-i18n="prog2Desc">Guidance with resources, interpretation support, local referrals, and community navigation.</p>
        </div>
        <div class="program-card">
          <h3 data-i18n="prog3Title">Community Services</h3>
          <p data-i18n="prog3Desc">Case support, transportation resource guidance, forms help, and local service connections.</p>
        </div>
        <div class="program-card">
          <h3 data-i18n="prog4Title">Youth Sports</h3>
          <p data-i18n="prog4Desc">Sports programs and mentorship that promote health, leadership, teamwork, and confidence.</p>
        </div>
        <div class="program-card">
          <h3 data-i18n="prog5Title">Family & Children Support</h3>
          <p data-i18n="prog5Desc">Family-focused services, children support referrals, and youth wellbeing assistance.</p>
        </div>
        <div class="program-card">
          <h3 data-i18n="prog6Title">Community Engagement</h3>
          <p data-i18n="prog6Desc">Meetings, workshops, outreach, and partnerships that strengthen community voice.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Board -->
  <section id="board" class="section">
    <div class="container">
      <div class="section-head">
        <h2 data-i18n="boardTitle">Board & Leadership</h2>
        <p data-i18n="boardDesc">Our leadership team serves the community with transparency, service, and accountability.</p>
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
          <p><strong data-i18n="emailLabel">Email:</strong> yourname@example.org</p>
          <p><strong data-i18n="phoneLabel">Phone:</strong> (414) 000-0000</p>
          <p class="small" data-i18n="contactNote">Replace the email/phone with your real nonprofit contact info.</p>
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
          <p class="small" data-i18n="formHint">This demo form doesn’t send yet. If you want, I’ll connect it to Formspree or your email.</p>
        </form>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="footer">
    <div class="container footer-inner">
      <div>
        <div class="footer-title" data-i18n="orgName">Milwaukee Somali Bantu Community Organization</div>
        <div class="footer-sub" data-i18n="footerSub">Nonprofit • Milwaukee, Wisconsin</div>
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
        tagline: "Unity • Justice • Dignity",
        orgName: "Milwaukee Somali Bantu Community Organization",
        orgType: "Nonprofit • Milwaukee, Wisconsin",
        navAbout: "About",
        navPrograms: "Programs",
        navBoard: "Board",
        navContact: "Contact",
        pill: "Serving the Somali Bantu community in Milwaukee",
        heroTitle: "Human rights advocacy and trusted community services — built with dignity.",
        heroDesc: "We support families through resettlement help, youth sports, referrals, case support, and community programs. We also advocate for civil rights, fair access, and respect for every person.",
        btnGetHelp: "Get Help",
        btnExplore: "Explore Programs",
        trust1: "Community-based nonprofit",
        trust2Num: "Support",
        trust2: "Resettlement & services",
        trust3Num: "Advocacy",
        trust3: "Human rights & protection",

        impactTitle: "Community Impact",
        impactSub: "Practical support. Strong advocacy. Real results.",
        stat1Num: "Advocacy",
        stat1Label: "Human rights support & referrals",
        stat2Num: "Resettlement",
        stat2Label: "Guidance for families and newcomers",
        stat3Num: "Youth",
        stat3Label: "Sports, mentorship, and leadership",
        impact1Title: "Services that meet real needs",
        impact1Desc: "Support for forms, referrals, and community navigation.",
        impact2Title: "Advocacy with dignity",
        impact2Desc: "Helping protect rights and promote fair access.",
        impact3Title: "Community-led leadership",
        impact3Desc: "Transparent leadership serving Milwaukee.",
        impactBtn: "See Programs",

        aboutTitle: "About Us",
        aboutDesc: "We are a Milwaukee-based nonprofit dedicated to serving the Somali Bantu community through practical support, protection of rights, and community-led programs.",
        missionTitle: "Mission",
        missionDesc: "To strengthen and empower the Somali Bantu community in Milwaukee through human rights advocacy, social services, and programs that build opportunity.",
        visionTitle: "Vision",
        visionDesc: "A safe, thriving, and respected community where families have access, dignity, and a strong voice.",
        valuesTitle: "Values",
        valuesDesc: "Integrity, service, unity, accountability, and respect for every person.",

        programsTitle: "Programs & Services",
        programsDesc: "We provide support across multiple areas. If you need help, contact us and we will guide you to the right service.",
        prog1Title: "Human Rights Advocacy",
        prog1Desc: "Support, reporting help, referrals, and community education to protect civil rights and dignity.",
        prog2Title: "Resettlement Support",
        prog2Desc: "Guidance with resources, interpretation support, local referrals, and community navigation.",
        prog3Title: "Community Services",
        prog3Desc: "Case support, transportation resource guidance, forms help, and local service connections.",
        prog4Title: "Youth Sports",
        prog4Desc: "Sports programs and mentorship that promote health, leadership, teamwork, and confidence.",
        prog5Title: "Family & Children Support",
        prog5Desc: "Family-focused services, children support referrals, and youth wellbeing assistance.",
        prog6Title: "Community Engagement",
        prog6Desc: "Meetings, workshops, outreach, and partnerships that strengthen community voice.",

        boardTitle: "Board & Leadership",
        boardDesc: "Our leadership team serves the community with transparency, service, and accountability.",
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
        contactNote: "Replace the email/phone with your real nonprofit contact info.",
        formName: "Name",
        formEmail: "Email",
        formMessage: "Message",
        formBtn: "Send Message",
        formHint: "This demo form doesn’t send yet. If you want, I’ll connect it to Formspree or your email.",
        footerSub: "Nonprofit • Milwaukee, Wisconsin"
      },

      so: {
        tagline: "Midnimo • Cadaalad • Karaamo",
        orgName: "Ururka Bulshada Soomaali Bantu ee Milwaukee",
        orgType: "Hay’ad Samafal • Milwaukee, Wisconsin",
        navAbout: "Ku Saabsan",
        navPrograms: "Barnaamijyada",
        navBoard: "Hoggaanka",
        navContact: "Xiriir",
        pill: "U adeegidda bulshada Soomaali Bantu ee Milwaukee",
        heroTitle: "Difaaca xuquuqda aadanaha iyo adeegyo bulsho oo lagu kalsoon yahay — si sharaf leh.",
        heroDesc: "Waxaan taageernaa qoysaska anagoo bixinayna caawinta dib-u-dejinta, ciyaaraha dhalinyarada, gudbinta adeegyada, taageerada kiisaska, iyo barnaamijyada bulshada. Sidoo kale waxaan u doodnaa xuquuqda madaniga, helitaanka caddaaladda, iyo ixtiraamka qof walba.",
        btnGetHelp: "Hel Caawimaad",
        btnExplore: "Eeg Barnaamijyada",
        trust1: "Hay’ad bulsho ku dhisan",
        trust2Num: "Taageero",
        trust2: "Dib-u-dejin & adeegyo",
        trust3Num: "U-doodid",
        trust3: "Xuquuqda aadanaha & ilaalin",

        impactTitle: "Saameynta Bulshada",
        impactSub: "Taageero dhab ah. U-doodid xooggan. Natiijo la taaban karo.",
        stat1Num: "U-doodid",
        stat1Label: "Taageero xuquuq & gudbin adeegyo",
        stat2Num: "Dib-u-dejin",
        stat2Label: "Hagid qoysas & dadka cusub",
        stat3Num: "Dhalinyaro",
        stat3Label: "Ciyaaro, hagid, & hoggaan",
        impact1Title: "Adeegyo la jaanqaada baahida",
        impact1Desc: "Caawin foomam, gudbin, iyo hagid adeegyada deegaanka.",
        impact2Title: "U-doodid si karaamo leh",
        impact2Desc: "Ka caawinta ilaalinta xuquuqda iyo helitaanka caddaaladda.",
        impact3Title: "Hoggaan bulshadu hoggaamiso",
        impact3Desc: "Hoggaan daahfuran oo u adeegaya Milwaukee.",
        impactBtn: "Eeg Barnaamijyada",

        aboutTitle: "Ku Saabsan",
        aboutDesc: "Waxaan nahay hay’ad samafal oo fadhigeedu yahay Milwaukee oo u heellan taageerada bulshada Soomaali Bantu anagoo bixinna caawimo wax ku ool ah, ilaalinta xuquuqda, iyo barnaamijyo bulsho hoggaaminayaan.",
        missionTitle: "Himiladeenna",
        missionDesc: "Inaan xoojino oo awood-siino bulshada Soomaali Bantu ee Milwaukee annagoo u marayna u-doodista xuquuqda aadanaha, adeegyada bulshada, iyo barnaamijyo fura fursado.",
        visionTitle: "Aragtideenna",
        visionDesc: "Bulsho ammaan ah, kobcaysa, oo la ixtiraamo—qoysaskuna helaan adeeg, karaamo, iyo cod xooggan.",
        valuesTitle: "Qiyamkeenna",
        valuesDesc: "Daacadnimo, adeeg, midnimo, isla-xisaabtan, iyo ixtiraam qof walba.",

        programsTitle: "Barnaamijyada & Adeegyada",
        programsDesc: "Waxaan bixinnaa taageero dhinacyo badan. Haddii aad u baahan tahay caawimo, nala soo xiriir—waan ku hagaynaa adeegga ku habboon.",
        prog1Title: "U-doodista Xuquuqda Aadanaha",
        prog1Desc: "Taageero, caawin warbixin, gudbin, iyo wacyigelin si loo ilaaliyo xuquuqda iyo karaamada.",
        prog2Title: "Taageerada Dib-u-dejinta",
        prog2Desc: "Hagid kheyraad, turjumaad/taageero luqadeed, gudbin, iyo hagitaan deegaanka.",
        prog3Title: "Adeegyada Bulshada",
        prog3Desc: "Taageero kiis, hagid gaadiid/kheyraad, caawin foomam, iyo isku-xir adeegyo.",
        prog4Title: "Ciyaaraha Dhalinyarada",
        prog4Desc: "Barnaamijyo ciyaareed iyo hagid dhalinyaro si loo dhiso caafimaad, hoggaan, iyo kalsooni.",
        prog5Title: "Taageerada Qoyska & Carruurta",
        prog5Desc: "Taageero qoys, gudbin carruurta, iyo caawin daryeelka dhalinyarada.",
        prog6Title: "Ka-Qaybgalka Bulshada",
        prog6Desc: "Kulan, aqoon-is-weydaarsi, wacyigelin, iyo iskaashi lagu xoojinayo codka bulshada.",

        boardTitle: "Hoggaanka & Guddiga",
        boardDesc: "Hoggaankeenna wuxuu u adeegaa bulshada si daahfurnaan, adeeg, iyo isla-xisaabtan leh.",
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
        contactNote: "Beddel iimaylka/telefoonka si ay u noqdaan kuwa rasmiga ah ee hay’adda.",
        formName: "Magaca",
        formEmail: "Iimayl",
        formMessage: "Fariin",
        formBtn: "Dir Fariinta",
        formHint: "Foomkan demo ma dirayo hadda. Haddii aad rabto, waan ku xirin karaa Formspree ama iimaylkaaga.",
        footerSub: "Hay’ad Samafal • Milwaukee, Wisconsin"
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
      document.documentElement.lang = lang === "so" ? "so" : "en";
    }

    document.getElementById("year").textContent = new Date().getFullYear();

    document.getElementById("lang-en").addEventListener("click", ()=>setLang("en"));
    document.getElementById("lang-so").addEventListener("click", ()=>setLang("so"));

    setLang(localStorage.getItem("msbc_lang") || "en");
  </script>
</body>
</html>

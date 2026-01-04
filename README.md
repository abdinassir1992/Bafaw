<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>BAFAW — Somali Bantu Advocacy & Community Services</title>
  <meta name="description" content="BAFAW supports the Somali Bantu community in Milwaukee through human rights advocacy, youth & sports, resettlement support, and community services." />
  <style>
    :root{
      --bg:#0b1220;
      --panel:#0f1a33;
      --card:#0f1a33;
      --text:#eaf0ff;
      --muted:#b9c4e6;
      --line:rgba(255,255,255,.10);
      --brand:#5aa2ff;
      --brand2:#7cf3c7;
      --shadow:0 12px 30px rgba(0,0,0,.35);
      --radius:18px;
      --max:1120px;
    }
    *{box-sizing:border-box}
    html{scroll-behavior:smooth}
    body{
      margin:0;
      font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Arial, "Apple Color Emoji","Segoe UI Emoji";
      background: radial-gradient(1200px 700px at 20% 0%, rgba(90,162,255,.22), transparent 60%),
                  radial-gradient(900px 600px at 90% 10%, rgba(124,243,199,.16), transparent 55%),
                  linear-gradient(180deg, #070b14, var(--bg));
      color:var(--text);
    }
    a{color:inherit}
    .wrap{max-width:var(--max); margin:0 auto; padding:0 18px}
    /* NAV */
    .nav{
      position:sticky; top:0; z-index:50;
      backdrop-filter:saturate(140%) blur(12px);
      background:rgba(7,11,20,.72);
      border-bottom:1px solid var(--line);
    }
    .nav-inner{
      display:flex; align-items:center; justify-content:space-between;
      padding:14px 0;
      gap:14px;
    }
    .brand{
      display:flex; align-items:center; gap:10px; text-decoration:none;
    }
    .logo{
      width:38px; height:38px; border-radius:12px;
      background:linear-gradient(135deg, var(--brand), var(--brand2));
      box-shadow:0 10px 22px rgba(90,162,255,.18);
    }
    .brand b{letter-spacing:.2px}
    .brand small{display:block; color:var(--muted); font-weight:600; margin-top:2px}
    .menu{display:flex; gap:16px; align-items:center}
    .menu a{
      text-decoration:none;
      color:var(--muted);
      font-weight:700;
      font-size:14px;
      padding:8px 10px;
      border-radius:12px;
    }
    .menu a:hover{color:var(--text); background:rgba(255,255,255,.06)}
    .cta{
      display:flex; gap:10px; align-items:center;
    }
    .btn{
      display:inline-flex; align-items:center; justify-content:center;
      gap:8px;
      padding:10px 14px;
      border-radius:14px;
      border:1px solid var(--line);
      background:rgba(255,255,255,.04);
      color:var(--text);
      text-decoration:none;
      font-weight:800;
      font-size:14px;
      box-shadow:0 10px 22px rgba(0,0,0,.18);
    }
    .btn:hover{background:rgba(255,255,255,.07)}
    .btn.primary{
      border:none;
      background:linear-gradient(135deg, var(--brand), #3f7dff 55%, var(--brand2));
      color:#061022;
    }
    .hamb{
      display:none;
      width:44px; height:44px;
      border-radius:14px;
      border:1px solid var(--line);
      background:rgba(255,255,255,.04);
      color:var(--text);
      font-weight:900;
      font-size:18px;
    }
    /* HERO */
    .hero{
      padding:64px 0 26px;
    }
    .tagline{
      display:flex; flex-wrap:wrap; gap:10px; align-items:center;
      color:var(--muted);
      font-weight:900;
      letter-spacing:.6px;
      text-transform:uppercase;
      font-size:12px;
    }
    .pill{
      border:1px solid var(--line);
      background:rgba(255,255,255,.04);
      padding:8px 12px;
      border-radius:999px;
    }
    .hero-grid{
      display:grid;
      grid-template-columns: 1.2fr .8fr;
      gap:26px;
      margin-top:18px;
      align-items:stretch;
    }
    h1{
      margin:14px 0 10px;
      font-size:46px;
      line-height:1.05;
      letter-spacing:-.8px;
    }
    .lead{
      color:var(--muted);
      font-size:16px;
      line-height:1.65;
      max-width:62ch;
    }
    .hero-actions{display:flex; gap:12px; flex-wrap:wrap; margin-top:18px}
    .panel{
      background:linear-gradient(180deg, rgba(15,26,51,.92), rgba(10,16,34,.92));
      border:1px solid var(--line);
      border-radius:var(--radius);
      box-shadow:var(--shadow);
      overflow:hidden;
    }
    .panel-head{
      padding:16px 16px 0;
      display:flex; align-items:center; justify-content:space-between; gap:12px;
    }
    .panel-head .mini{
      color:var(--muted);
      font-weight:900;
      font-size:12px;
      letter-spacing:.7px;
      text-transform:uppercase;
    }
    .flagbar{
      display:flex; gap:8px; align-items:center;
      border:1px solid var(--line);
      background:rgba(255,255,255,.04);
      padding:8px 10px;
      border-radius:999px;
      color:var(--muted);
      font-weight:800;
      font-size:12px;
      white-space:nowrap;
    }
    .panel-body{padding:16px}
    .statgrid{
      display:grid;
      grid-template-columns: repeat(3, 1fr);
      gap:12px;
      margin-top:10px;
    }
    .stat{
      border:1px solid var(--line);
      border-radius:16px;
      background:rgba(255,255,255,.03);
      padding:14px 12px;
    }
    .stat b{display:block; font-size:22px; letter-spacing:-.3px}
    .stat span{display:block; color:var(--muted); margin-top:6px; font-weight:700; font-size:12px}
    /* SECTIONS */
    section{padding:56px 0}
    .section-title{
      display:flex; align-items:flex-end; justify-content:space-between; gap:16px;
      margin-bottom:18px;
    }
    .section-title h2{
      margin:0;
      font-size:28px;
      letter-spacing:-.4px;
    }
    .section-title p{margin:0; color:var(--muted); max-width:60ch; line-height:1.6}
    .grid-2{
      display:grid;
      grid-template-columns: 1fr 1fr;
      gap:18px;
    }
    .card{
      border:1px solid var(--line);
      background:rgba(255,255,255,.03);
      border-radius:var(--radius);
      padding:18px;
      box-shadow:0 10px 24px rgba(0,0,0,.20);
    }
    .card h3{margin:0 0 8px; font-size:18px}
    .card p{margin:0; color:var(--muted); line-height:1.65}
    .list{
      margin:12px 0 0; padding:0 0 0 18px; color:var(--muted); line-height:1.7;
      font-weight:650;
    }
    .pillrow{display:flex; flex-wrap:wrap; gap:10px; margin-top:12px}
    .pillrow .pill{font-weight:800; color:var(--muted)}
    /* PROGRAMS */
    .programs{
      display:grid;
      grid-template-columns: repeat(4, 1fr);
      gap:14px;
    }
    .program{
      padding:16px;
      border-radius:18px;
      border:1px solid var(--line);
      background:rgba(255,255,255,.03);
    }
    .program b{display:block; margin-bottom:8px}
    .program p{margin:0; color:var(--muted); line-height:1.6; font-size:14px}
    /* LEADERSHIP */
    .people{
      display:grid;
      grid-template-columns: repeat(3, 1fr);
      gap:14px;
    }
    .person{
      display:flex; gap:12px; align-items:flex-start;
      border:1px solid var(--line);
      background:rgba(255,255,255,.03);
      border-radius:18px;
      padding:14px;
    }
    .avatar{
      width:44px; height:44px; border-radius:16px;
      background:linear-gradient(135deg, rgba(90,162,255,.8), rgba(124,243,199,.7));
      flex:0 0 auto;
    }
    .person b{display:block}
    .person span{display:block; color:var(--muted); font-weight:750; margin-top:4px; font-size:13px}
    /* CONTACT */
    form{display:grid; gap:12px}
    input, textarea{
      width:100%;
      padding:12px 12px;
      border-radius:14px;
      border:1px solid var(--line);
      background:rgba(255,255,255,.03);
      color:var(--text);
      outline:none;
      font-weight:650;
    }
    textarea{min-height:120px; resize:vertical}
    .foot{
      padding:22px 0;
      border-top:1px solid var(--line);
      color:var(--muted);
      font-weight:700;
      font-size:13px;
    }
    /* MOBILE */
    @media (max-width: 980px){
      h1{font-size:38px}
      .hero-grid{grid-template-columns: 1fr}
      .programs{grid-template-columns: repeat(2, 1fr)}
      .people{grid-template-columns: repeat(2, 1fr)}
      .grid-2{grid-template-columns:1fr}
    }
    @media (max-width: 720px){
      .menu{display:none}
      .hamb{display:inline-flex; align-items:center; justify-content:center}
      .statgrid{grid-template-columns:1fr}
      .programs{grid-template-columns:1fr}
      .people{grid-template-columns:1fr}
    }
    .mobile-menu{
      display:none;
      padding:0 0 14px;
    }
    .mobile-menu a{
      display:block;
      padding:10px 12px;
      margin-top:8px;
      border:1px solid var(--line);
      border-radius:14px;
      text-decoration:none;
      color:var(--muted);
      font-weight:900;
      background:rgba(255,255,255,.03);
    }
    .mobile-menu a:hover{color:var(--text); background:rgba(255,255,255,.06)}
  </style>
</head>

<body>
  <!-- NAV -->
  <header class="nav">
    <div class="wrap">
      <div class="nav-inner">
        <a class="brand" href="#top">
          <div class="logo" aria-hidden="true"></div>
          <div>
            <b>BAFAW</b>
            <small>Milwaukee Somali Bantu Community</small>
          </div>
        </a>

        <nav class="menu" aria-label="Primary">
          <a href="#about">About</a>
          <a href="#mission">Mission</a>
          <a href="#programs">Programs</a>
          <a href="#leadership">Leadership</a>
          <a href="#getinvolved">Get Involved</a>
          <a href="#contact">Contact</a>
        </nav>

        <div class="cta">
          <a class="btn" href="#contact">Volunteer</a>
          <a class="btn primary" href="#getinvolved">Join / Register</a>
          <button class="hamb" id="hamb" aria-label="Open menu">☰</button>
        </div>
      </div>

      <div class="mobile-menu" id="mobileMenu">
        <a href="#about">About</a>
        <a href="#mission">Mission</a>
        <a href="#programs">Programs</a>
        <a href="#leadership">Leadership</a>
        <a href="#getinvolved">Get Involved</a>
        <a href="#contact">Contact</a>
      </div>
    </div>
  </header>

  <!-- HERO -->
  <main id="top" class="hero">
    <div class="wrap">
      <div class="tagline">
        <span class="pill">Unity</span>
        <span class="pill">Justice</span>
        <span class="pill">Service</span>
        <span class="pill">Dignity</span>
      </div>

      <div class="hero-grid">
        <div>
          <h1>BAFAW — Advocacy & Community Services in Milwaukee</h1>
          <p class="lead">
            BAFAW supports the Somali Bantu community through human rights advocacy and community services including
            youth & sports, family support, resettlement assistance, and programs that strengthen dignity and opportunity.
          </p>

          <div class="hero-actions">
            <a class="btn primary" href="#getinvolved">Join / Become a Member</a>
            <a class="btn" href="#leadership">View Leadership</a>
            <a class="btn" href="#programs">Explore Programs</a>
          </div>

          <div class="pillrow">
            <span class="pill">Community-driven</span>
            <span class="pill">Non-partisan</span>
            <span class="pill">Milwaukee, Wisconsin</span>
          </div>
        </div>

        <aside class="panel" aria-label="Highlights">
          <div class="panel-head">
            <div class="mini">BAFAW at a glance</div>
            <div class="flagbar">Milwaukee • Wisconsin • USA</div>
          </div>
          <div class="panel-body">
            <div class="statgrid">
              <div class="stat">
                <b>Human Rights</b>
                <span>Advocacy & protection support</span>
              </div>
              <div class="stat">
                <b>Social Services</b>
                <span>Resettlement & family support</span>
              </div>
              <div class="stat">
                <b>Youth & Sports</b>
                <span>Safe spaces & leadership</span>
              </div>
            </div>
            <p class="lead" style="margin-top:14px">
              Our work is rooted in community needs — building partnerships, supporting families, and ensuring Somali Bantu
              voices are respected in every space where decisions are made.
            </p>
          </div>
        </aside>
      </div>
    </div>
  </main>

  <!-- ABOUT -->
  <section id="about">
    <div class="wrap">
      <div class="section-title">
        <div>
          <h2>Who We Are</h2>
          <p>BAFAW is a community-rooted initiative serving Somali Bantu families in Milwaukee through advocacy, services, and strong local partnerships.</p>
        </div>
      </div>

      <div class="grid-2">
        <div class="card">
          <h3>Our Story</h3>
          <p>
            Somali Bantu communities have a long history of resilience. BAFAW exists to strengthen dignity, safety, and opportunity
            for families in Milwaukee through practical services and trusted community leadership.
          </p>
        </div>
        <div class="card">
          <h3>How We Work</h3>
          <p>We collaborate with local partners to deliver community support and connect families to resources.</p>
          <ul class="list">
            <li>Community advocacy and referrals</li>
            <li>Support for resettlement and navigation</li>
            <li>Youth, sports, and leadership development</li>
            <li>Family & children support services</li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <!-- MISSION -->
  <section id="mission">
    <div class="wrap">
      <div class="section-title">
        <div>
          <h2>Mission, Vision & Values</h2>
          <p>Our direction is clear: serve the community, protect rights, and build pathways to stability and success.</p>
        </div>
      </div>

      <div class="grid-2">
        <div class="card">
          <h3>Our Mission</h3>
          <p>
            To support the Somali Bantu community in Milwaukee through human rights advocacy, social services, youth programs,
            and partnerships that improve wellbeing and opportunity.
          </p>
        </div>
        <div class="card">
          <h3>Our Vision</h3>
          <p>
            A stronger, safer, and thriving Somali Bantu community — fully included, respected, and equipped with the tools to succeed,
            while preserving culture and identity.
          </p>
        </div>
      </div>

      <div class="grid-2" style="margin-top:18px">
        <div class="card">
          <h3>Core Values</h3>
          <ul class="list">
            <li><b>Unity</b> — building together across families and generations</li>
            <li><b>Justice</b> — standing against discrimination and harm</li>
            <li><b>Service</b> — leadership means humility and action</li>
            <li><b>Accountability</b> — transparency, responsibility, and trust</li>
          </ul>
        </div>
        <div class="card">
          <h3>Focus Areas</h3>
          <p>BAFAW’s work aligns to these pillars:</p>
          <div class="pillrow">
            <span class="pill">Advocacy</span>
            <span class="pill">Community Services</span>
            <span class="pill">Youth & Sports</span>
            <span class="pill">Family & Children</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- PROGRAMS -->
  <section id="programs">
    <div class="wrap">
      <div class="section-title">
        <div>
          <h2>Programs & Departments</h2>
          <p>BAFAW organizes its work around real needs identified by families and community leaders in Milwaukee.</p>
        </div>
      </div>

      <div class="programs">
        <div class="program">
          <b>Human Rights & Advocacy</b>
          <p>Support, referrals, documentation, and engagement with local institutions to protect community rights.</p>
        </div>
        <div class="program">
          <b>Resettlement & Navigation</b>
          <p>Helping families access resources, services, interpretation support, and local systems.</p>
        </div>
        <div class="program">
          <b>Youth & Sports</b>
          <p>Safe activities, leadership development, mentorship, and community-building through sports.</p>
        </div>
        <div class="program">
          <b>Family & Children</b>
          <p>Family support, community education, and child/youth wellbeing programs with trusted partners.</p>
        </div>
        <div class="program">
          <b>Community Services</b>
          <p>Coordination of community assistance, events, and local support efforts.</p>
        </div>
        <div class="program">
          <b>Education & Training</b>
          <p>Guidance, workshops, and connections to educational opportunities and workforce resources.</p>
        </div>
        <div class="program">
          <b>Public Relations</b>
          <p>Community communication, announcements, and representation to media and partners.</p>
        </div>
        <div class="program">
          <b>Finance & Development</b>
          <p>Transparent operations, fundraising coordination, and program support planning.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- LEADERSHIP -->
  <section id="leadership">
    <div class="wrap">
      <div class="section-title">
        <div>
          <h2>Board & Leadership</h2>
          <p>BAFAW’s leadership team coordinates programs and community support across Milwaukee.</p>
        </div>
      </div>

      <div class="people">
        <div class="person"><div class="avatar"></div><div><b>Mohamed Sidi</b><span>President</span></div></div>
        <div class="person"><div class="avatar"></div><div><b>Sheikh Abdishakur Ali</b><span>Vice President</span></div></div>
        <div class="person"><div class="avatar"></div><div><b>Engineer Abdinasser Omar</b><span>Secretary</span></div></div>

        <div class="person"><div class="avatar"></div><div><b>Sheiknoor Adan</b><span>Executive Director</span></div></div>
        <div class="person"><div class="avatar"></div><div><b>Nuurto Jeylani</b><span>Assistant Executive Director</span></div></div>
        <div class="person"><div class="avatar"></div><div><b>Anab Aden</b><span>Treasury</span></div></div>

        <div class="person"><div class="avatar"></div><div><b>Jafar Hussien</b><span>Program Coordinator</span></div></div>
        <div class="person"><div class="avatar"></div><div><b>Mohamed Omar</b><span>Assistant Program Coordinator</span></div></div>
        <div class="person"><div class="avatar"></div><div><b>Fatuma Sharif</b><span>Family & Children Coordinator</span></div></div>

        <div class="person"><div class="avatar"></div><div><b>Muktarhussin</b><span>Spokesperson</span></div></div>
      </div>

      <div class="card" style="margin-top:16px">
        <h3>Visual Organizational Structure</h3>
        <p>
          You can add your official org chart image here (PNG/JPG). If you upload it to your site, replace the placeholder below.
        </p>
        <div style="margin-top:12px; border:1px dashed var(--line); border-radius:18px; padding:18px; color:var(--muted); font-weight:800;">
          Placeholder: BAFAW_OrgChart.png
        </div>
      </div>
    </div>
  </section>

  <!-- GET INVOLVED -->
  <section id="getinvolved">
    <div class="wrap">
      <div class="section-title">
        <div>
          <h2>Get Involved</h2>
          <p>Somali Bantu progress is a shared responsibility. There is a place for you in this work.</p>
        </div>
      </div>

      <div class="grid-2">
        <div class="card">
          <h3>Become a Member, Volunteer, or Partner</h3>
          <ul class="list">
            <li>Join as a member and support community programs</li>
            <li>Volunteer skills: interpretation, tutoring, youth coaching, media, organizing</li>
            <li>Partner with BAFAW on services and community initiatives</li>
            <li>Support programs through donations or in-kind contributions</li>
          </ul>
        </div>
        <div class="card">
          <h3>What We Need Right Now</h3>
          <p>Examples (edit these):</p>
          <div class="pillrow">
            <span class="pill">Volunteer Coaches</span>
            <span class="pill">Interpreters</span>
            <span class="pill">Youth Mentors</span>
            <span class="pill">Community Drivers</span>
            <span class="pill">School Support</span>
          </div>
          <p style="margin-top:12px" class="lead">Use the contact form below to sign up.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact">
    <div class="wrap">
      <div class="section-title">
        <div>
          <h2>Contact</h2>
          <p>Send a message to BAFAW. You can connect the form to email later (Formspree, Netlify Forms, or a backend).</p>
        </div>
      </div>

      <div class="grid-2">
        <div class="card">
          <h3>Send a message</h3>
          <form onsubmit="event.preventDefault(); alert('Thanks! This demo form is not connected yet.');">
            <input type="text" name="name" placeholder="Full name" required />
            <input type="email" name="email" placeholder="Email" required />
            <input type="text" name="subject" placeholder="Subject" required />
            <textarea name="message" placeholder="Message" required></textarea>
            <button class="btn primary" type="submit">Send</button>
          </form>
          <p style="margin-top:10px" class="lead">Tip: When you’re ready, I can wire this to email with Formspree in 2 minutes.</p>
        </div>

        <div class="card">
          <h3>BAFAW — Milwaukee Office</h3>
          <p class="lead">
            <b>Location:</b> Milwaukee, Wisconsin, USA<br/>
            <b>Email:</b> (add your official email)<br/>
            <b>Phone/WhatsApp:</b> (add your official phone)
          </p>
          <ul class="list">
            <li>For partnerships, include your organization name and contact details.</li>
            <li>For services, tell us what help you need and the best time to reach you.</li>
          </ul>
        </div>
      </div>

      <div class="foot">
        © <span id="year"></span> BAFAW. All rights reserved.
      </div>
    </div>
  </section>

  <script>
    // Year
    document.getElementById("year").textContent = new Date().getFullYear();

    // Mobile menu toggle
    const hamb = document.getElementById("hamb");
    const mm = document.getElementById("mobileMenu");
    hamb?.addEventListener("click", () => {
      const open = mm.style.display === "block";
      mm.style.display = open ? "none" : "block";
      hamb.textContent = open ? "☰" : "✕";
    });

    // Auto-close mobile menu on click
    mm?.querySelectorAll("a").forEach(a => {
      a.addEventListener("click", () => {
        mm.style.display = "none";
        hamb.textContent = "☰";
      });
    });
  </script>
</body>
</html>

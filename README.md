<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Milwaukee Somali Bantu Community | Advocacy & Services</title>
  <meta name="description" content="Milwaukee Somali Bantu Community: human rights advocacy and social services including sports, resettlement, and community programs." />
  <style>
    :root{
      --bg:#0b1220;
      --card:#0f1a33;
      --text:#eaf0ff;
      --muted:#b9c6e6;
      --accent:#55d6ff;
      --accent2:#86efac;
      --line:rgba(255,255,255,.10);
      --shadow: 0 20px 60px rgba(0,0,0,.35);
      --radius:18px;
      --max:1120px;
      --font: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, "Apple Color Emoji","Segoe UI Emoji";
    }
    *{box-sizing:border-box}
    html,body{margin:0;padding:0;background:radial-gradient(1200px 900px at 15% 10%, rgba(85,214,255,.20), transparent 55%),
                                   radial-gradient(1000px 700px at 90% 20%, rgba(134,239,172,.14), transparent 50%),
                                   var(--bg);
              color:var(--text); font-family:var(--font); line-height:1.55;}
    a{color:inherit}
    .wrap{max-width:var(--max); margin:0 auto; padding:24px;}
    .topbar{
      display:flex; align-items:center; justify-content:space-between;
      gap:16px; padding:10px 0;
    }
    .brand{display:flex; align-items:center; gap:12px; text-decoration:none}
    .logo{
      width:42px; height:42px; border-radius:14px;
      background:linear-gradient(135deg, rgba(85,214,255,.9), rgba(134,239,172,.85));
      box-shadow:0 12px 30px rgba(85,214,255,.18);
    }
    .brand h1{font-size:16px; margin:0; letter-spacing:.2px}
    .brand small{display:block; color:var(--muted); margin-top:2px; font-size:12px}
    nav{display:flex; flex-wrap:wrap; gap:10px; align-items:center}
    nav a{
      padding:10px 12px; border:1px solid var(--line); border-radius:999px;
      text-decoration:none; color:var(--muted);
      transition:.15s ease;
    }
    nav a:hover{border-color:rgba(85,214,255,.45); color:var(--text)}
    .btn{
      background:linear-gradient(135deg, rgba(85,214,255,.95), rgba(134,239,172,.88));
      color:#071018; border:none; padding:10px 14px; border-radius:999px;
      text-decoration:none; font-weight:700; box-shadow:0 14px 40px rgba(85,214,255,.16);
      display:inline-flex; gap:8px; align-items:center;
    }
    .hero{
      margin-top:16px;
      border:1px solid var(--line);
      background:linear-gradient(180deg, rgba(255,255,255,.05), rgba(255,255,255,.02));
      border-radius:var(--radius);
      padding:34px;
      box-shadow:var(--shadow);
      position:relative;
      overflow:hidden;
    }
    .hero:before{
      content:""; position:absolute; inset:-120px -80px auto auto; width:360px; height:360px;
      background:radial-gradient(circle at 30% 30%, rgba(85,214,255,.35), transparent 60%);
      filter:blur(2px);
    }
    .hero-grid{display:grid; grid-template-columns: 1.2fr .8fr; gap:24px}
    @media (max-width: 900px){ .hero-grid{grid-template-columns:1fr} }
    .kicker{color:var(--accent); font-weight:700; letter-spacing:.14em; text-transform:uppercase; font-size:12px}
    .hero h2{font-size:40px; line-height:1.1; margin:10px 0 10px}
    @media (max-width: 520px){ .hero h2{font-size:32px} }
    .hero p{color:var(--muted); margin:0 0 16px; font-size:16px}
    .cta-row{display:flex; flex-wrap:wrap; gap:12px; align-items:center; margin-top:18px}
    .ghost{
      border:1px solid var(--line); color:var(--text); background:transparent;
      padding:10px 14px; border-radius:999px; text-decoration:none; font-weight:650;
    }
    .stats{
      display:grid; gap:12px;
      grid-template-columns: repeat(2, minmax(0,1fr));
    }
    .stat{
      border:1px solid var(--line);
      background:rgba(15,26,51,.55);
      border-radius:16px;
      padding:14px;
    }
    .stat b{display:block; font-size:18px}
    .stat span{color:var(--muted); font-size:12px}
    section{margin-top:22px}
    .section-card{
      border:1px solid var(--line);
      background:rgba(15,26,51,.55);
      border-radius:var(--radius);
      padding:24px;
      box-shadow:0 18px 50px rgba(0,0,0,.20);
    }
    .section-title{display:flex; align-items:flex-end; justify-content:space-between; gap:14px; margin-bottom:14px}
    .section-title h3{margin:0; font-size:22px}
    .section-title p{margin:0; color:var(--muted); font-size:14px}
    .grid3{display:grid; grid-template-columns:repeat(3, minmax(0,1fr)); gap:12px}
    @media (max-width: 900px){ .grid3{grid-template-columns:1fr} }
    .pill{
      display:inline-flex; align-items:center; gap:8px;
      padding:8px 10px; border-radius:999px; border:1px solid var(--line);
      color:var(--muted); font-size:13px; margin:6px 8px 0 0;
    }
    .card{
      border:1px solid var(--line);
      border-radius:16px;
      padding:16px;
      background:rgba(11,18,32,.35);
    }
    .card h4{margin:0 0 6px; font-size:16px}
    .card p{margin:0; color:var(--muted); font-size:14px}
    .people{display:grid; grid-template-columns:repeat(2, minmax(0,1fr)); gap:12px}
    @media (max-width: 900px){ .people{grid-template-columns:1fr} }
    .person{
      display:flex; gap:12px; align-items:flex-start;
      border:1px solid var(--line);
      border-radius:16px;
      padding:14px;
      background:rgba(11,18,32,.35);
    }
    .avatar{
      width:42px; height:42px; border-radius:14px;
      background:linear-gradient(135deg, rgba(85,214,255,.25), rgba(134,239,172,.22));
      border:1px solid rgba(255,255,255,.10);
      flex:0 0 auto;
    }
    .person b{display:block}
    .person small{color:var(--muted)}
    .footer{
      margin:24px 0 10px;
      color:var(--muted);
      font-size:13px;
      display:flex; flex-wrap:wrap; justify-content:space-between; gap:10px;
      border-top:1px solid var(--line);
      padding-top:16px;
    }
    .form{
      display:grid; grid-template-columns:1fr 1fr; gap:12px; margin-top:10px;
    }
    @media (max-width: 900px){ .form{grid-template-columns:1fr} }
    input, textarea{
      width:100%; padding:12px 12px; border-radius:14px;
      border:1px solid var(--line); background:rgba(11,18,32,.55); color:var(--text);
      outline:none;
    }
    textarea{min-height:120px; resize:vertical}
    .note{color:var(--muted); font-size:12px; margin-top:10px}
  </style>
</head>

<body>
  <div class="wrap">
    <header class="topbar">
      <a class="brand" href="#top">
        <div class="logo" aria-hidden="true"></div>
        <div>
          <h1>Milwaukee Somali Bantu Community</h1>
          <small>Human rights advocacy • Social services • Community programs</small>
        </div>
      </a>

      <nav aria-label="Primary">
        <a href="#about">About</a>
        <a href="#services">Programs</a>
        <a href="#leadership">Leadership</a>
        <a href="#get-involved">Get involved</a>
        <a href="#contact">Contact</a>
        <a class="btn" href="#donate">Donate</a>
      </nav>
    </header>

    <main id="top" class="hero">
      <div class="hero-grid">
        <div>
          <div class="kicker">Milwaukee, Wisconsin</div>
          <h2>Supporting the Somali Bantu community with dignity, justice, and opportunity.</h2>
          <p>
            We provide trusted community support and services—from resettlement and family resources to youth sports and human rights advocacy.
            Our mission is to strengthen families, protect rights, and build a safer, healthier future for all.
          </p>

          <div>
            <span class="pill">Human Rights Advocacy</span>
            <span class="pill">Resettlement Support</span>
            <span class="pill">Youth & Sports</span>
            <span class="pill">Family & Children Services</span>
          </div>

          <div class="cta-row">
            <a class="btn" href="#get-involved">Volunteer / Partner</a>
            <a class="ghost" href="#services">See our programs</a>
          </div>
        </div>

        <div class="stats" aria-label="Quick highlights">
          <div class="stat">
            <b>Community Services</b>
            <span>Support for families, youth, and newcomers</span>
          </div>
          <div class="stat">
            <b>Advocacy</b>
            <span>Human rights, community protection, and voice</span>
          </div>
          <div class="stat">
            <b>Sports Programs</b>
            <span>Youth development through teamwork</span>
          </div>
          <div class="stat">
            <b>Resettlement Help</b>
            <span>Guidance navigating schools, jobs, resources</span>
          </div>
        </div>
      </div>
    </main>

    <section id="about" class="section-card">
      <div class="section-title">
        <h3>About us</h3>
        <p>Rooted in community. Focused on solutions.</p>
      </div>
      <p style="color:var(--muted); margin:0;">
        The Milwaukee Somali Bantu Community organization is committed to empowering Somali Bantu families and individuals through
        advocacy, social services, and community programming. We collaborate with local partners to connect residents to resources,
        strengthen youth opportunities, and protect the rights and well-being of our community.
      </p>
    </section>

    <section id="services" class="section-card">
      <div class="section-title">
        <h3>Programs & services</h3>
        <p>What we do</p>
      </div>

      <div class="grid3">
        <div class="card">
          <h4>Human Rights Advocacy</h4>
          <p>Support, awareness, and community representation to protect dignity and rights.</p>
        </div>
        <div class="card">
          <h4>Resettlement & Navigation</h4>
          <p>Help connecting to housing resources, school systems, health services, and employment pathways.</p>
        </div>
        <div class="card">
          <h4>Youth Sports & Development</h4>
          <p>Sports programs that build leadership, confidence, and healthy routines for youth.</p>
        </div>
        <div class="card">
          <h4>Family & Children Support</h4>
          <p>Family guidance, children services coordination, and support for parents and caregivers.</p>
        </div>
        <div class="card">
          <h4>Community Services</h4>
          <p>Community support, referrals, translation support (if available), and local resource connection.</p>
        </div>
        <div class="card">
          <h4>Programs & Events</h4>
          <p>Workshops, community meetings, and partnerships that strengthen community unity.</p>
        </div>
      </div>
    </section>

    <section id="leadership" class="section-card">
      <div class="section-title">
        <h3>Leadership & board</h3>
        <p>Serving Milwaukee with accountability and transparency</p>
      </div>

      <div class="people">
        <div class="person"><div class="avatar"></div><div><b>Mohamed Sidi</b><small>President</small></div></div>
        <div class="person"><div class="avatar"></div><div><b>Sheikh Abdishakur Ali</b><small>Vice President</small></div></div>

        <div class="person"><div class="avatar"></div><div><b>Engineer Abdinasser Omar</b><small>Secretary</small></div></div>
        <div class="person"><div class="avatar"></div><div><b>Sheiknoor Adan</b><small>Executive Director</small></div></div>

        <div class="person"><div class="avatar"></div><div><b>Nuurto Jeylani</b><small>Assistant Executive Director</small></div></div>
        <div class="person"><div class="avatar"></div><div><b>Anab Aden</b><small>Treasury</small></div></div>

        <div class="person"><div class="avatar"></div><div><b>Jafar Hussien</b><small>Program Coordinator</small></div></div>
        <div class="person"><div class="avatar"></div><div><b>Mohamed Omar</b><small>Assistant Program Coordinator</small></div></div>

        <div class="person"><div class="avatar"></div><div><b>Fatuma Sharif</b><small>Family & Children Coordinator</small></div></div>
        <div class="person"><div class="avatar"></div><div><b>Muktarhussin</b><small>Spokesperson</small></div></div>
      </div>
    </section>

    <section id="get-involved" class="section-card">
      <div class="section-title">
        <h3>Get involved</h3>
        <p>Volunteer • Partner • Sponsor</p>
      </div>

      <div class="grid3">
        <div class="card">
          <h4>Volunteer</h4>
          <p>Help with events, youth activities, community outreach, and support services.</p>
        </div>
        <div class="card">
          <h4>Partner</h4>
          <p>We welcome partnerships with schools, nonprofits, clinics, and local organizations.</p>
        </div>
        <div class="card">
          <h4>Sponsor</h4>
          <p>Support programs like youth sports, community workshops, and resettlement assistance.</p>
        </div>
      </div>

      <p class="note">Tip: Add your EIN/501(c)(3) info here later if you want donations to be tax-deductible.</p>
    </section>

    <section id="donate" class="section-card">
      <div class="section-title">
        <h3>Donate</h3>
        <p>Support programs and services</p>
      </div>
      <p style="color:var(--muted); margin:0 0 12px;">
        Donations help us deliver advocacy and community services. Add your payment link (PayPal, Stripe, Cash App, etc.) when ready.
      </p>
      <a class="btn" href="#contact">Request donation info</a>
    </section>

    <section id="contact" class="section-card">
      <div class="section-title">
        <h3>Contact</h3>
        <p>We’ll respond as soon as possible</p>
      </div>

      <p style="color:var(--muted); margin:0 0 8px;">
        Add your official email/phone/address here when ready.
      </p>

      <!-- Simple mailto form (works without a server) -->
      <form action="mailto:YOUR_EMAIL_HERE@example.com" method="post" enctype="text/plain">
        <div class="form">
          <input name="name" placeholder="Your name" required />
          <input name="email" type="email" placeholder="Your email" required />
        </div>
        <div style="margin-top:12px;">
          <textarea name="message" placeholder="How can we help?" required></textarea>
        </div>
        <div class="cta-row" style="margin-top:12px;">
          <button class="btn" type="submit">Send message</button>
          <span class="note">Replace <b>YOUR_EMAIL_HERE@example.com</b> in the code with your organization email.</span>
        </div>
      </form>
    </section>

    <footer class="footer">
      <div>© <span id="year"></span> Milwaukee Somali Bantu Community. All rights reserved.</div>
      <div>
        <a href="#top" style="text-decoration:none; border-bottom:1px dotted var(--line);">Back to top</a>
      </div>
    </footer>
  </div>

  <script>
    document.getElementById("year").textContent = new Date().getFullYear();
  </script>
</body>
</html>


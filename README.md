<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>BAFAW Milwaukee Somali Bantu Community</title>
<meta name="description" content="BAFAW is a Milwaukee-based nonprofit supporting the Somali Bantu community through advocacy and community services." />

<style>
:root{
  --c1:#2563eb;
  --c2:#22c55e;
  --c3:#a855f7;
  --c4:#f97316;
  --dark:#0f172a;
  --muted:#475569;
  --radius:22px;
  --shadow:0 20px 45px rgba(2,6,23,.18);
  --line:rgba(15,23,42,.10);
}

*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{
  margin:0;
  font-family:system-ui,-apple-system,Segoe UI,Roboto,Arial;
  color:var(--dark);
  background:
    radial-gradient(900px 500px at 10% 10%, rgba(37,99,235,.28), transparent 60%),
    radial-gradient(800px 500px at 90% 20%, rgba(168,85,247,.25), transparent 60%),
    radial-gradient(800px 600px at 20% 90%, rgba(34,197,94,.25), transparent 60%),
    radial-gradient(700px 500px at 90% 85%, rgba(249,115,22,.20), transparent 60%),
    linear-gradient(180deg,#f8fafc,#eef2ff);
}

a{text-decoration:none;color:inherit}
.container{max-width:1200px;margin:auto;padding:0 18px}

/* TOP STRIP */
.top-strip{
  height:10px;
  background:linear-gradient(90deg,var(--c1),var(--c3),var(--c2),var(--c4));
}

/* HEADER */
header{
  position:sticky;
  top:0;
  z-index:50;
  backdrop-filter:blur(10px);
  background:rgba(255,255,255,.86);
  border-bottom:1px solid var(--line);
}
.header-inner{
  display:flex;
  align-items:center;
  justify-content:space-between;
  padding:14px 0;
  gap:12px;
}

/* Logo text */
.brand{
  display:flex;
  flex-direction:column;
  min-width: 0;
}
.logo-text{
  font-size:26px;
  font-weight:1000;
  letter-spacing:1px;
  line-height:1;
  background:linear-gradient(90deg,var(--c1),var(--c3),var(--c2));
  -webkit-background-clip:text;
  background-clip:text;
  color:transparent;
  white-space:nowrap;
}
.brand-sub{
  font-size:13px;
  color:var(--muted);
  font-weight:650;
  margin-top:4px;
  white-space:nowrap;
  overflow:hidden;
  text-overflow:ellipsis;
}

/* Desktop nav */
nav.nav{
  display:none;
  gap:18px;
  font-weight:850;
  align-items:center;
}
nav.nav a{color:var(--muted)}
nav.nav a:hover{color:var(--c1)}
.nav-btn{
  padding:10px 14px;
  border-radius:16px;
  background:#fff;
  border:1px solid rgba(37,99,235,.25);
  box-shadow:0 12px 25px rgba(2,6,23,.08);
  color:var(--dark) !important;
}

/* Hamburger */
.menu-btn{
  display:inline-flex;
  align-items:center;
  justify-content:center;
  width:44px;height:44px;
  border-radius:14px;
  border:1px solid var(--line);
  background:rgba(255,255,255,.92);
  box-shadow:0 12px 25px rgba(2,6,23,.08);
  cursor:pointer;
}
.menu-icon{
  width:20px;height:14px; position:relative;
}
.menu-icon span{
  position:absolute; left:0; right:0;
  height:2px; border-radius:2px;
  background:rgba(15,23,42,.8);
  transition:transform .2s ease, top .2s ease, opacity .2s ease;
}
.menu-icon span:nth-child(1){top:0}
.menu-icon span:nth-child(2){top:6px}
.menu-icon span:nth-child(3){top:12px}

/* Mobile drawer */
.drawer{
  display:none;
  border-top:1px solid var(--line);
  background:rgba(255,255,255,.92);
}
.drawer.open{display:block}
.drawer a{
  display:block;
  padding:14px 18px;
  font-weight:850;
  color:rgba(15,23,42,.78);
  border-bottom:1px solid rgba(15,23,42,.06);
}
.drawer a:last-child{border-bottom:none}
.drawer .drawer-cta{
  background:linear-gradient(135deg, rgba(37,99,235,.10), rgba(168,85,247,.10));
}

/* HERO */
.hero{padding:52px 0 26px}
.hero-grid{
  display:grid;
  grid-template-columns:1fr;
  gap:22px;
  align-items:start;
}
.badge{
  display:inline-block;
  padding:8px 14px;
  border-radius:999px;
  font-weight:850;
  font-size:13px;
  background:rgba(255,255,255,.86);
  border:1px solid var(--line);
}
.hero h1{
  font-size:clamp(28px,5vw,46px);
  line-height:1.1;
  margin:14px 0 10px;
  letter-spacing:-.6px;
}
.hero p{
  color:var(--muted);
  font-size:16px;
  line-height:1.7;
  margin:0;
}
.hero-actions{
  display:flex;
  gap:12px;
  margin:18px 0 0;
  flex-wrap:wrap;
}
.btn{
  padding:14px 18px;
  border-radius:18px;
  font-weight:950;
  border:none;
  cursor:pointer;
  width:100%;
}
.btn-primary{
  color:#fff;
  background:linear-gradient(135deg,var(--c1),var(--c3));
  box-shadow:0 18px 40px rgba(37,99,235,.28);
}
.btn-light{
  background:rgba(255,255,255,.92);
  border:1px solid var(--line);
}

/* Side card */
.side-card{
  background:rgba(255,255,255,.90);
  border-radius:28px;
  padding:20px;
  box-shadow:var(--shadow);
  border:1px solid rgba(15,23,42,.06);
}
.side-card h3{margin:0 0 12px}
.pill-grid{
  display:grid;
  grid-template-columns:1fr;
  gap:10px;
}
.pill{
  padding:10px 12px;
  border-radius:14px;
  background:#fff;
  border:1px solid rgba(15,23,42,.10);
  font-weight:800;
  color:rgba(15,23,42,.82);
}

/* SECTIONS */
section{padding:54px 0}
.alt{
  background:rgba(255,255,255,.65);
  border-top:1px solid rgba(15,23,42,.08);
  border-bottom:1px solid rgba(15,23,42,.08);
}
.section-title{
  font-size:28px;
  letter-spacing:-.4px;
  margin:0 0 10px;
}
.section-desc{
  color:var(--muted);
  line-height:1.7;
  margin:0;
  max-width: 85ch;
}

.grid-3{
  display:grid;
  grid-template-columns:1fr;
  gap:14px;
  margin-top:18px;
}
.card{
  background:#fff;
  padding:18px;
  border-radius:var(--radius);
  border:1px solid rgba(15,23,42,.10);
  box-shadow:0 16px 36px rgba(2,6,23,.10);
}
.card h3{margin:0 0 8px}
.card p{margin:0;color:var(--muted);line-height:1.65}

/* Board */
.board{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:14px;
  margin-top:18px;
}
.board-card{
  background:#fff;
  padding:14px;
  border-radius:18px;
  border:1px solid rgba(15,23,42,.10);
  box-shadow:0 14px 30px rgba(2,6,23,.10);
}
.role{
  font-size:12px;
  font-weight:950;
  text-transform:uppercase;
  color:var(--muted);
  letter-spacing:.7px;
}
.name{font-weight:950;margin-top:6px}

/* Contact */
.contact-grid{
  display:grid;
  grid-template-columns:1fr;
  gap:14px;
  margin-top:18px;
}
label{font-weight:850}
input,textarea{
  width:100%;
  padding:12px 12px;
  border-radius:14px;
  border:1px solid rgba(15,23,42,.15);
  margin-top:6px;
  font:inherit;
  outline:none;
  background:rgba(255,255,255,.96);
}
input:focus, textarea:focus{
  border-color: rgba(37,99,235,.40);
  box-shadow: 0 0 0 4px rgba(37,99,235,.12);
}
.small{font-size:13px;color:var(--muted);line-height:1.6;margin-top:10px}

/* Footer */
footer{
  padding:28px 0;
  background:rgba(255,255,255,.84);
  border-top:1px solid rgba(15,23,42,.10);
}

/* Tablet */
@media (min-width:768px){
  .hero-grid{grid-template-columns:1.1fr .9fr}
  .pill-grid{grid-template-columns:1fr 1fr}
  .grid-3{grid-template-columns:repeat(3,1fr)}
  .board{grid-template-columns:repeat(3,1fr)}
  .btn{width:auto}
}

/* Desktop */
@media (min-width:1024px){
  nav.nav{display:flex}
  .menu-btn{display:none}
  .drawer{display:none !important}
  .board{grid-template-columns:repeat(5,1fr)}
  .contact-grid{grid-template-columns:1fr 1fr}
}
</style>
</head>

<body>
<div class="top-strip"></div>

<header>
  <div class="container header-inner">
    <div class="brand">
      <div class="logo-text">BAFAW</div>
      <div class="brand-sub">Milwaukee Somali Bantu Community</div>
    </div>

    <!-- Desktop nav -->
    <nav class="nav" aria-label="Primary">
      <a href="#about">About</a>
      <a href="#programs">Programs</a>
      <a href="#board">Board</a>
      <a class="nav-btn" href="#contact">Contact</a>
    </nav>

    <!-- Mobile menu button -->
    <button class="menu-btn" id="menuBtn" aria-label="Open menu" aria-expanded="false" aria-controls="drawer">
      <div class="menu-icon" aria-hidden="true">
        <span></span><span></span><span></span>
      </div>
    </button>
  </div>

  <!-- Mobile drawer -->
  <div class="drawer" id="drawer">
    <a href="#about" class="drawer-link">About</a>
    <a href="#programs" class="drawer-link">Programs</a>
    <a href="#board" class="drawer-link">Board</a>
    <a href="#contact" class="drawer-link drawer-cta">Contact</a>
  </div>
</header>

<main class="hero container" id="home">
  <div class="hero-grid">
    <div>
      <div class="badge">Serving the Somali Bantu community in Milwaukee</div>
      <h1>Community advocacy and social services that support families.</h1>
      <p>
        BAFAW provides human rights advocacy and essential community services including resettlement assistance,
        youth sports, family support, and referrals.
      </p>

      <div class="hero-actions">
        <a class="btn btn-primary" href="#contact">Get Support</a>
        <a class="btn btn-light" href="#programs">View Programs</a>
      </div>
    </div>

    <aside class="side-card">
      <h3>What we do</h3>
      <div class="pill-grid">
        <div class="pill">Human Rights Advocacy</div>
        <div class="pill">Resettlement Support</div>
        <div class="pill">Youth Sports</div>
        <div class="pill">Family & Children Services</div>
        <div class="pill">Community Referrals</div>
        <div class="pill">Workshops & Outreach</div>
      </div>
      <p class="small">Need help today? Contact us and we’ll guide you to the right service.</p>
    </aside>
  </div>
</main>

<section id="about" class="container">
  <h2 class="section-title">About BAFAW</h2>
  <p class="section-desc">
    BAFAW is a Milwaukee-based nonprofit organization dedicated to supporting the Somali Bantu community through
    advocacy, services, and community-led initiatives.
  </p>

  <div class="grid-3">
    <div class="card">
      <h3>Mission</h3>
      <p>Support and empower Somali Bantu families through advocacy and community services.</p>
    </div>
    <div class="card">
      <h3>Vision</h3>
      <p>A connected community with access to opportunity, resources, and fair treatment.</p>
    </div>
    <div class="card">
      <h3>Values</h3>
      <p>Service, unity, accountability, transparency, and respect.</p>
    </div>
  </div>
</section>

<section id="programs" class="alt">
  <div class="container">
    <h2 class="section-title">Programs & Services</h2>
    <p class="section-desc">We provide support across multiple areas. If you need help, contact us and we will guide you to the right service.</p>

    <div class="grid-3">
      <div class="card">
        <h3>Human Rights Advocacy</h3>
        <p>Support, reporting help, referrals, and community education to protect rights and fair access.</p>
      </div>
      <div class="card">
        <h3>Resettlement Support</h3>
        <p>Guidance with resources, local referrals, interpretation support, and community navigation.</p>
      </div>
      <div class="card">
        <h3>Community Services</h3>
        <p>Case support, forms help, referrals, and connections to local services.</p>
      </div>
      <div class="card">
        <h3>Youth Sports</h3>
        <p>Sports programs and mentorship that promote health, teamwork, and leadership.</p>
      </div>
      <div class="card">
        <h3>Family & Children Support</h3>
        <p>Family-focused support, children referrals, and youth wellbeing assistance.</p>
      </div>
      <div class="card">
        <h3>Community Engagement</h3>
        <p>Meetings, workshops, outreach, and partnerships that strengthen community voice.</p>
      </div>
    </div>
  </div>
</section>

<section id="board" class="container">
  <h2 class="section-title">Board & Leadership</h2>
  <p class="section-desc">Our leadership team serves the community with responsibility and transparency.</p>

  <div class="board">
    <div class="board-card"><div class="role">President</div><div class="name">Mohamed Sidi</div></div>
    <div class="board-card"><div class="role">Vice President</div><div class="name">Sheikh Abdishakur Ali</div></div>
    <div class="board-card"><div class="role">Secretary</div><div class="name">Abdinasser Omar</div></div>
    <div class="board-card"><div class="role">Executive Director</div><div class="name">Sheiknoor Adan</div></div>
    <div class="board-card"><div class="role">Assistant Executive Director</div><div class="name">Nuurto Jeylani</div></div>
    <div class="board-card"><div class="role">Treasury</div><div class="name">Anab Aden</div></div>
    <div class="board-card"><div class="role">Program Coordinator</div><div class="name">Jafar Hussien</div></div>
    <div class="board-card"><div class="role">Assistant Program Coordinator</div><div class="name">Mohamed Omar</div></div>
    <div class="board-card"><div class="role">Family & Children Coordinator</div><div class="name">Fatuma Sharif</div></div>
    <div class="board-card"><div class="role">Spokesperson</div><div class="name">Muktar Hussien</div></div>
  </div>
</section>

<section id="contact" class="alt">
  <div class="container">
    <h2 class="section-title">Contact</h2>
    <p class="section-desc">Tell us what you need help with. We will respond as soon as possible.</p>

    <div class="contact-grid">
      <div class="card">
        <h3>Organization Info</h3>
        <p><strong>Location:</strong> Milwaukee, Wisconsin</p>
        <p><strong>Email:</strong> yourname@example.org</p>
        <p><strong>Phone:</strong> (414) 000-0000</p>
        <p class="small">Replace email/phone with your real nonprofit contact info.</p>
      </div>

      <div class="card">
        <h3>Send a message</h3>
        <form onsubmit="return false;">
          <label>Name
            <input type="text" placeholder="Your name" />
          </label>
          <label>Email
            <input type="email" placeholder="you@email.com" />
          </label>
          <label>Message
            <textarea rows="4" placeholder="How can we help?"></textarea>
          </label>
          <button class="btn btn-primary" style="width:100%" type="submit">Send Message</button>
          <p class="small">This form is a demo. If you want, I’ll connect it to a real form that sends to your email.</p>
        </form>
      </div>
    </div>
  </div>
</section>

<footer>
  <div class="container" style="display:flex;flex-direction:column;gap:8px;padding:18px 0;">
    <strong>BAFAW – Milwaukee Somali Bantu Community</strong>
    <div class="small">© <span id="y"></span></div>
  </div>
</footer>

<script>
  // Year
  document.getElementById("y").textContent = new Date().getFullYear();

  // Mobile menu toggle
  const btn = document.getElementById("menuBtn");
  const drawer = document.getElementById("drawer");

  function setOpen(isOpen){
    drawer.classList.toggle("open", isOpen);
    btn.setAttribute("aria-expanded", String(isOpen));
  }

  btn.addEventListener("click", () => {
    setOpen(!drawer.classList.contains("open"));
  });

  // Close menu when clicking a link
  document.querySelectorAll(".drawer-link").forEach(a=>{
    a.addEventListener("click", ()=>setOpen(false));
  });

  // Close drawer if resizing to desktop
  window.addEventListener("resize", ()=>{
    if (window.innerWidth >= 1024) setOpen(false);
  });
</script>
</body>
</html>

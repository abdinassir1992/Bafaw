<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Milwaukee Somali Bantu Community BAFAW</title>

<style>
:root{
  --c1:#2563eb;
  --c2:#22c55e;
  --c3:#a855f7;
  --c4:#f97316;
  --dark:#0f172a;
  --muted:#475569;
  --white:#ffffff;
  --radius:22px;
  --shadow:0 20px 45px rgba(2,6,23,.18);
}

*{box-sizing:border-box}
body{
  margin:0;
  font-family:system-ui,-apple-system,Segoe UI,Roboto,Arial;
  color:var(--dark);
  background:
    radial-gradient(900px 500px at 10% 10%, rgba(37,99,235,.30), transparent 60%),
    radial-gradient(800px 500px at 90% 20%, rgba(168,85,247,.25), transparent 60%),
    radial-gradient(800px 600px at 20% 90%, rgba(34,197,94,.25), transparent 60%),
    radial-gradient(700px 500px at 90% 85%, rgba(249,115,22,.20), transparent 60%),
    linear-gradient(180deg,#f8fafc,#eef2ff);
}

a{text-decoration:none;color:inherit}
.container{max-width:1200px;margin:auto;padding:0 20px}

/* TOP STRIP */
.top-strip{
  height:10px;
  background:linear-gradient(90deg,var(--c1),var(--c3),var(--c2),var(--c4));
}

/* HEADER */
header{
  position:sticky;
  top:0;
  z-index:20;
  backdrop-filter:blur(10px);
  background:rgba(255,255,255,.75);
  border-bottom:1px solid rgba(15,23,42,.1);
}
.header-inner{
  display:flex;
  align-items:center;
  justify-content:space-between;
  padding:16px 0;
}
.brand{
  display:flex;
  align-items:center;
  gap:14px;
}
.logo{
  width:48px;height:48px;
  border-radius:16px;
  display:grid;
  place-items:center;
  font-weight:900;
  color:#fff;
  background:linear-gradient(135deg,var(--c1),var(--c3));
  box-shadow:0 15px 35px rgba(37,99,235,.35);
}
.brand-title{
  font-weight:900;
  letter-spacing:-.4px;
}
.brand-title span{
  background:linear-gradient(90deg,var(--c1),var(--c3));
  -webkit-background-clip:text;
  color:transparent;
}
.brand-sub{
  font-size:13px;
  color:var(--muted);
  margin-top:3px;
}
nav{
  display:flex;
  gap:20px;
  font-weight:700;
}
nav a:hover{color:var(--c1)}
.nav-btn{
  padding:10px 16px;
  border-radius:16px;
  background:#fff;
  border:1px solid rgba(37,99,235,.25);
  box-shadow:0 12px 25px rgba(2,6,23,.1);
}

/* HERO */
.hero{padding:60px 0 30px}
.hero-grid{
  display:grid;
  grid-template-columns:1.2fr .8fr;
  gap:22px;
}
.badge{
  display:inline-block;
  padding:8px 14px;
  border-radius:999px;
  font-weight:800;
  font-size:13px;
  background:rgba(255,255,255,.85);
  border:1px solid rgba(15,23,42,.1);
}
.hero h1{
  font-size:clamp(32px,4.5vw,54px);
  line-height:1.05;
  margin:16px 0 10px;
  letter-spacing:-.8px;
}
.hero p{
  color:var(--muted);
  font-size:16px;
  line-height:1.7;
  max-width:65ch;
}
.hero-actions{
  display:flex;
  gap:14px;
  margin:20px 0;
}
.btn{
  padding:14px 20px;
  border-radius:18px;
  font-weight:900;
  border:none;
  cursor:pointer;
}
.btn-primary{
  color:#fff;
  background:linear-gradient(135deg,var(--c1),var(--c3));
  box-shadow:0 18px 40px rgba(37,99,235,.35);
}
.btn-light{
  background:rgba(255,255,255,.9);
  border:1px solid rgba(15,23,42,.1);
}

/* SIDE CARD */
.side-card{
  background:rgba(255,255,255,.85);
  border-radius:28px;
  padding:22px;
  box-shadow:var(--shadow);
}
.side-card h3{margin-top:0}
.pill-grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:10px;
}
.pill{
  padding:10px 12px;
  border-radius:14px;
  background:rgba(255,255,255,.9);
  border:1px solid rgba(15,23,42,.1);
  font-weight:700;
  font-size:14px;
}

/* SECTIONS */
section{padding:60px 0}
.alt{
  background:rgba(255,255,255,.65);
  border-top:1px solid rgba(15,23,42,.08);
  border-bottom:1px solid rgba(15,23,42,.08);
}
.section-title{
  font-size:30px;
  letter-spacing:-.4px;
}
.section-desc{
  color:var(--muted);
  max-width:80ch;
  line-height:1.7;
}

.grid-3{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:18px;
  margin-top:22px;
}
.card{
  background:rgba(255,255,255,.9);
  padding:20px;
  border-radius:var(--radius);
  border:1px solid rgba(15,23,42,.1);
  box-shadow:0 18px 40px rgba(2,6,23,.1);
}

/* BOARD */
.board{
  display:grid;
  grid-template-columns:repeat(5,1fr);
  gap:14px;
  margin-top:22px;
}
.board-card{
  background:#fff;
  padding:14px;
  border-radius:18px;
  border:1px solid rgba(15,23,42,.1);
  box-shadow:0 14px 30px rgba(2,6,23,.1);
}
.role{
  font-size:12px;
  font-weight:900;
  text-transform:uppercase;
  color:var(--muted);
}
.name{font-weight:900;margin-top:6px}

/* CONTACT */
.contact-grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:18px;
  margin-top:22px;
}
input,textarea{
  width:100%;
  padding:12px;
  border-radius:14px;
  border:1px solid rgba(15,23,42,.15);
  margin-top:6px;
}
label{font-weight:700}

/* FOOTER */
footer{
  padding:30px 0;
  background:rgba(255,255,255,.75);
  border-top:1px solid rgba(15,23,42,.1);
}
.footer-inner{
  display:flex;
  justify-content:space-between;
  flex-wrap:wrap;
  gap:14px;
}
.small{font-size:13px;color:var(--muted)}

@media(max-width:900px){
  .hero-grid{grid-template-columns:1fr}
  .grid-3{grid-template-columns:1fr}
  .board{grid-template-columns:repeat(2,1fr)}
  .contact-grid{grid-template-columns:1fr}
  nav{display:none}
}
</style>
</head>

<body>

<div class="top-strip"></div>

<header>
  <div class="container header-inner">
    <div class="brand">
      <div class="logo">B</div>
      <div>
        <div class="brand-title">Milwaukee Somali Bantu Community <span>BAFAW</span></div>
        <div class="brand-sub">Nonprofit • Milwaukee, Wisconsin</div>
      </div>
    </div>
    <nav>
      <a href="#about">About</a>
      <a href="#programs">Programs</a>
      <a href="#board">Board</a>
      <a href="#contact" class="nav-btn">Contact</a>
    </nav>
  </div>
</header>

<section class="hero container">
  <div class="hero-grid">
    <div>
      <div class="badge">Serving the Somali Bantu community in Milwaukee</div>
      <h1>Community advocacy and social services that support families.</h1>
      <p>
        Milwaukee Somali Bantu Community BAFAW provides human rights advocacy and
        essential community services including resettlement assistance, youth sports,
        family support, and referrals.
      </p>
      <div class="hero-actions">
        <button class="btn btn-primary">Get Support</button>
        <button class="btn btn-light">View Programs</button>
      </div>
    </div>

    <div class="side-card">
      <h3>What we do</h3>
      <div class="pill-grid">
        <div class="pill">Human Rights Advocacy</div>
        <div class="pill">Resettlement Support</div>
        <div class="pill">Youth Sports</div>
        <div class="pill">Family & Children Services</div>
        <div class="pill">Community Referrals</div>
        <div class="pill">Workshops & Outreach</div>
      </div>
    </div>
  </div>
</section>

<section id="about" class="container">
  <h2 class="section-title">About BAFAW</h2>
  <p class="section-desc">
    BAFAW is a Milwaukee-based nonprofit organization dedicated to supporting
    the Somali Bantu community through advocacy, services, and community-led initiatives.
  </p>

  <div class="grid-3">
    <div class="card"><h3>Mission</h3><p>Support and empower Somali Bantu families through advocacy and services.</p></div>
    <div class="card"><h3>Vision</h3><p>A connected community with access to opportunity and fair treatment.</p></div>
    <div class="card"><h3>Values</h3><p>Service, unity, accountability, and transparency.</p></div>
  </div>
</section>

<section id="programs" class="alt">
  <div class="container">
    <h2 class="section-title">Programs & Services</h2>
    <div class="grid-3">
      <div class="card">Human Rights Advocacy</div>
      <div class="card">Resettlement Support</div>
      <div class="card">Community Services</div>
      <div class="card">Youth Sports</div>
      <div class="card">Family & Children Support</div>
      <div class="card">Community Engagement</div>
    </div>
  </div>
</section>

<section id="board" class="container">
  <h2 class="section-title">Board & Leadership</h2>
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
    <div class="contact-grid">
      <div class="card">
        <p><strong>Location:</strong> Milwaukee, Wisconsin</p>
        <p><strong>Email:</strong> yourname@example.org</p>
        <p><strong>Phone:</strong> (414) 000-0000</p>
      </div>
      <div class="card">
        <label>Name<input></label>
        <label>Email<input></label>
        <label>Message<textarea rows="4"></textarea></label>
        <button class="btn btn-primary" style="width:100%">Send Message</button>
      </div>
    </div>
  </div>
</section>

<footer>
  <div class="container footer-inner">
    <div>
      <strong>Milwaukee Somali Bantu Community BAFAW</strong>
      <div class="small">Nonprofit • Milwaukee, Wisconsin</div>
    </div>
    <div class="small">© <span id="y"></span></div>
  </div>
</footer>

<script>
document.getElementById("y").textContent=new Date().getFullYear();
</script>

</body>
</html>

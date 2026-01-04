<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>BAFAW Milwaukee Somali Bantu Community</title>

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
}

*{box-sizing:border-box}
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
  z-index:20;
  backdrop-filter:blur(10px);
  background:rgba(255,255,255,.8);
  border-bottom:1px solid rgba(15,23,42,.1);
}
.header-inner{
  display:flex;
  align-items:center;
  justify-content:space-between;
  padding:14px 0;
  gap:14px;
}

/* LOGO TEXT */
.brand{
  display:flex;
  flex-direction:column;
}
.logo-text{
  font-size:26px;
  font-weight:1000;
  letter-spacing:1px;
  background:linear-gradient(90deg,var(--c1),var(--c3),var(--c2));
  -webkit-background-clip:text;
  background-clip:text;
  color:transparent;
}
.brand-sub{
  font-size:13px;
  color:var(--muted);
  font-weight:600;
}

nav{
  display:flex;
  gap:18px;
  font-weight:800;
}
nav a:hover{color:var(--c1)}
.nav-btn{
  padding:10px 14px;
  border-radius:16px;
  background:#fff;
  border:1px solid rgba(37,99,235,.25);
  box-shadow:0 12px 25px rgba(2,6,23,.1);
}

/* HERO */
.hero{padding:52px 0 30px}
.hero-grid{
  display:grid;
  grid-template-columns:1fr;
  gap:26px;
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
  font-size:clamp(28px,5vw,46px);
  line-height:1.1;
  margin:14px 0 10px;
  letter-spacing:-.6px;
}
.hero p{
  color:var(--muted);
  font-size:16px;
  line-height:1.7;
}

.hero-actions{
  display:flex;
  gap:14px;
  margin:20px 0;
  flex-wrap:wrap;
}
.btn{
  padding:14px 18px;
  border-radius:18px;
  font-weight:900;
  border:none;
  cursor:pointer;
  width:100%;
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
  background:rgba(255,255,255,.88);
  border-radius:28px;
  padding:22px;
  box-shadow:var(--shadow);
}
.pill-grid{
  display:grid;
  grid-template-columns:1fr;
  gap:10px;
}
.pill{
  padding:10px 12px;
  border-radius:14px;
  background:#fff;
  border:1px solid rgba(15,23,42,.1);
  font-weight:700;
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
}
.section-desc{
  color:var(--muted);
  line-height:1.7;
}

.grid-3{
  display:grid;
  grid-template-columns:1fr;
  gap:18px;
  margin-top:22px;
}
.card{
  background:#fff;
  padding:20px;
  border-radius:var(--radius);
  border:1px solid rgba(15,23,42,.1);
  box-shadow:0 18px 40px rgba(2,6,23,.1);
}

/* BOARD */
.board{
  display:grid;
  grid-template-columns:1fr 1fr;
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
  grid-template-columns:1fr;
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

/* FOOTER */
footer{
  padding:28px 0;
  background:rgba(255,255,255,.8);
  border-top:1px solid rgba(15,23,42,.1);
}
.footer-inner{
  display:flex;
  flex-direction:column;
  gap:10px;
}
.small{font-size:13px;color:var(--muted)}

/* TABLET & DESKTOP */
@media(min-width:768px){
  .hero-grid{grid-template-columns:1.1fr .9fr}
  .pill-grid{grid-template-columns:1fr 1fr}
  .grid-3{grid-template-columns:repeat(3,1fr)}
  .board{grid-template-columns:repeat(3,1fr)}
  .btn{width:auto}
}

@media(min-width:1024px){
  nav{display:flex}
  .board{grid-template-columns:repeat(5,1fr)}
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
        BAFAW provides human rights advocacy and essential community services
        including resettlement assistance, youth sports, family support, and referrals.
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
</section>

<section id="board" class="alt">
  <div class="container">
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
  </div>
</section>

<footer>
  <div class="container footer-inner">
    <strong>BAFAW – Milwaukee Somali Bantu Community</strong>
    <div class="small">© <span id="y"></span></div>
  </div>
</footer>

<script>
document.getElementById("y").textContent=new Date().getFullYear();
</script>

</body>
</html>

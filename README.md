# GALAXY-STAR-PRIVATE-LIMITED-
Galaxy Star Private Limited - AC &amp; HVAC Repairing, Service &amp; Installation
from pathlib import Path
import shutil, zipfile, textwrap

base = Path("/mnt/data/galaxy_star_website")
if base.exists():
    shutil.rmtree(base)
(base / "assets").mkdir(parents=True)

# Copy uploaded logo into the website package.
shutil.copy2("/mnt/data/1000312088.png", base / "assets" / "galaxy-star-logo.png")

html = """<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Galaxy Star Private Limited - AC Repairing, Service, Installation, HVAC and AMC solutions.">
  <title>Galaxy Star Private Limited | AC & HVAC Solutions</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
<header class="navbar">
  <a class="brand" href="#home"><img src="assets/galaxy-star-logo.png" alt="Galaxy Star Logo"></a>
  <nav>
    <a href="#services">Services</a>
    <a href="#packages">Packages</a>
    <a href="#booking">Booking</a>
    <a href="#contact">Contact</a>
  </nav>
  <a class="btn small" href="tel:+917481904976">Call 7481904976</a>
</header>

<main>
<section id="home" class="hero">h
  <div class="hero-content">
    <span class="eyebrow">GALAXY STAR PRIVATE LIMITED</span>
    <h1>Professional <span>AC & HVAC</span> Solutions</h1>
    <p>Repairing • Servicing • Installation • Maintenance • AMC</p>
    <div class="actions">
      <a class="btn" href="#booking">Book a Technician</a>
      <a class="btn secondary" href="https://wa.me/917481904976" target="_blank">WhatsApp</a>
    </div>
  </div>
  <div class="hero-orb"><img src="assets/galaxy-star-logo.png" alt="Galaxy Star"></div>
</section>

<section class="stats">
  <div><b>AC</b><small>Repair & Service</small></div>
  <div><b>HVAC</b><small>Technical Solutions</small></div>
  <div><b>AMC</b><small>Maintenance Plans</small></div>
  <div><b>24/7</b><small>Enquiry Support</small></div>
</section>

<section id="services">
  <div class="heading"><span>WHAT WE DO</span><h2>Our Services</h2></div>
  <div class="grid">
    <article class="card"><i>❄️</i><h3>Split AC</h3><p>Repair, installation, cleaning and preventive maintenance.</p></article>
    <article class="card"><i>🏠</i><h3>Window AC</h3><p>Inspection, servicing, troubleshooting and installation.</p></article>
    <article class="card"><i>🏢</i><h3>Cassette AC</h3><p>Professional commercial AC service and maintenance.</p></article>
    <article class="card"><i>⚙️</i><h3>HVAC Solutions</h3><p>Technical support and planned maintenance for HVAC systems.</p></article>
    <article class="card"><i>🧰</i><h3>Installation</h3><p>Careful installation with system performance checks.</p></article>
    <article class="card"><i>🔧</i><h3>AMC & Maintenance</h3><p>Scheduled service plans for long-term reliability.</p></article>
  </div>
</section>

<section id="packages" class="dark-section">
  <div class="heading"><span>POPULAR OPTIONS</span><h2>Service Packages</h2></div>
  <div class="grid">
    <article class="card price-card"><h3>Basic Service</h3><strong>₹499*</strong><p>General inspection and standard cleaning.</p><a class="btn" href="#booking">Book</a></article>
    <article class="card price-card featured"><label>POPULAR</label><h3>Deep Service</h3><strong>₹899*</strong><p>Detailed cleaning and performance check.</p><a class="btn" href="#booking">Book</a></article>
    <article class="card price-card"><h3>AMC</h3><strong>Custom</strong><p>Maintenance package based on system and site.</p><a class="btn" href="#booking">Get Quote</a></article>
  </div>
  <p class="note">*Sample prices. Confirm your final rates before publishing.</p>
</section>

<section id="booking">
  <div class="booking-layout">
    <div>
      <div class="heading"><span>ONLINE BOOKING</span><h2>Book a Technician</h2></div>
      <p class="muted">Fill in the details and receive a booking ID. This front-end demo stores the booking in your browser.</p>
      <div class="contact-box"><b>Need urgent help?</b><br>Call <a href="tel:+917481904976">7481904976</a></div>
    </div>
    <form id="bookingForm" class="form-card">
      <input id="name" required placeholder="Customer name">
      <input id="phone" required inputmode="tel" placeholder="Mobile number">
      <select id="service" required>
        <option value="">Select service</option>
        <option>Split AC</option><option>Window AC</option><option>Cassette AC</option>
        <option>HVAC</option><option>Installation</option><option>AMC / Maintenance</option>
      </select>
      <input id="date" required type="date">
      <textarea id="problem" placeholder="Describe the problem"></textarea>
      <button class="btn" type="submit">Create Booking</button>
    </form>
  </div>
</section>

<section id="contact" class="contact-section">
  <div class="heading"><span>GET IN TOUCH</span><h2>Contact Galaxy Star</h2></div>
  <div class="contact-grid">
    <div class="card"><h3>📞 Phone</h3><a href="tel:+917481904976">7481904976</a></div>
    <div class="card"><h3>📍 Address</h3><p>Main Road, Sitamarhi, Bihar</p></div>
    <div class="card"><h3>💬 WhatsApp</h3><a href="https://wa.me/917481904976" target="_blank">Start Enquiry</a></div>
  </div>
</section>
</main>

<footer>
  <img src="assets/galaxy-star-logo.png" alt="Galaxy Star">
  <p>© 2026 Galaxy Star Private Limited • AC & HVAC Solutions</p>
</footer>

<div id="toast" class="toast"></div>
<script src="script.js"></script>
</body>
</html>
"""

css = """*{box-sizing:border-box}html{scroll-behavior:smooth}body{margin:0;background:#050914;color:#f6f9ff;font-family:Inter,Arial,sans-serif;line-height:1.5}
:root{--cyan:#42d9ff;--blue:#1677ff;--purple:#8b5cf6;--card:#0d1728;--line:#223451;--muted:#9baac2}
.navbar{position:sticky;top:0;z-index:50;height:76px;padding:8px 6%;display:flex;align-items:center;justify-content:space-between;background:#050914dd;backdrop-filter:blur(18px);border-bottom:1px solid #ffffff12}
.brand img{width:60px;height:60px;object-fit:contain}.navbar nav{display:flex;gap:25px}.navbar nav a{color:#dce8fb;text-decoration:none;font-size:14px}.btn{display:inline-block;border:0;border-radius:13px;padding:13px 19px;color:white;text-decoration:none;font-weight:800;background:linear-gradient(135deg,var(--cyan),var(--purple));cursor:pointer;box-shadow:0 12px 30px #168cff22}.btn.small{padding:10px 14px;font-size:13px}.btn.secondary{background:#15243b}
.hero{min-height:78vh;padding:80px 7%;display:flex;align-items:center;justify-content:space-between;gap:40px;background:radial-gradient(circle at 75% 45%,#173a72 0,transparent 30%),radial-gradient(circle at 20% 20%,#1a1745 0,transparent 32%)}
.hero-content{max-width:720px}.eyebrow,.heading span{font-size:12px;font-weight:900;letter-spacing:2px;color:var(--cyan)}h1{font-size:clamp(46px,7vw,82px);line-height:1.02;letter-spacing:-3px;margin:15px 0}h1 span{background:linear-gradient(90deg,#fff,var(--cyan),#b794ff);-webkit-background-clip:text;color:transparent}.hero p{color:var(--muted);font-size:19px}.actions{display:flex;gap:12px;flex-wrap:wrap;margin-top:28px}.hero-orb{width:min(360px,38vw);aspect-ratio:1;border-radius:50%;display:grid;place-items:center;background:radial-gradient(circle,#193b76,#071023 65%);box-shadow:0 0 100px #1677ff33}.hero-orb img{width:82%;filter:drop-shadow(0 0 28px #2bd7ff55)}
.stats{max-width:1100px;margin:-30px auto 0;padding:24px;display:grid;grid-template-columns:repeat(4,1fr);gap:12px;background:#0c1626dd;border:1px solid var(--line);border-radius:22px;position:relative}.stats div{padding:14px;text-align:center}.stats b{display:block;font-size:27px;color:var(--cyan)}.stats small,.muted,.note{color:var(--muted)}
section{max-width:1200px;margin:auto;padding:90px 6%}.heading h2{font-size:42px;margin:8px 0 30px}.grid{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}.card,.form-card{background:linear-gradient(145deg,#101d31,#09111e);border:1px solid var(--line);border-radius:20px;padding:24px}.card i{font-style:normal;font-size:34px}.card h3{margin:12px 0 8px}.card p{color:var(--muted)}.dark-section{max-width:none;background:#080f1c}.dark-section>*{max-width:1080px;margin-left:auto;margin-right:auto}.price-card{position:relative}.price-card strong{font-size:30px;color:var(--cyan);display:block;margin:10px 0}.featured{border-color:#4ad9ff88;box-shadow:0 0 40px #1677ff18}.price-card label{position:absolute;right:18px;top:18px;background:#55d6ff18;color:var(--cyan);padding:5px 8px;border-radius:8px;font-size:10px;font-weight:900}.note{font-size:12px;margin-top:18px}.booking-layout{display:grid;grid-template-columns:1fr 1fr;gap:30px;align-items:start}.form-card{display:grid;gap:13px}input,select,textarea{width:100%;border:1px solid var(--line);background:#07101d;color:#fff;border-radius:12px;padding:14px;font:inherit}textarea{min-height:110px;resize:vertical}.contact-box{margin-top:25px;padding:18px;border-left:3px solid var(--cyan);background:#0b1728}.contact-box a,.contact-grid a{color:var(--cyan);text-decoration:none}.contact-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}.contact-section{padding-top:40px}.toast{position:fixed;right:18px;bottom:18px;background:#15243a;border:1px solid #55d6ff66;padding:15px 18px;border-radius:12px;display:none;z-index:100}footer{padding:30px 6%;border-top:1px solid var(--line);display:flex;align-items:center;gap:15px;color:var(--muted)}footer img{width:45px;height:45px;object-fit:contain}
@media(max-width:800px){.navbar nav{display:none}.navbar{padding:8px 4%}.hero{padding:65px 6%;text-align:center;flex-direction:column}.hero-orb{width:250px}.actions{justify-content:center}.stats{margin:0 5%;grid-template-columns:repeat(2,1fr)}.grid,.contact-grid,.booking-layout{grid-template-columns:1fr}.heading h2{font-size:34px}section{padding:65px 6%}.navbar .btn{display:none}}
"""

js = """const form=document.getElementById('bookingForm');
const toast=document.getElementById('toast');
form.addEventListener('submit',e=>{
  e.preventDefault();
  const bookingId='GS-'+Math.random().toString(36).slice(2,8).toUpperCase();
  const booking={
    id:bookingId,name:document.getElementById('name').value,
    phone:document.getElementById('phone').value,
    service:document.getElementById('service').value,
    date:document.getElementById('date').value,
    problem:document.getElementById('problem').value,
    createdAt:new Date().toISOString()
  };
  const list=JSON.parse(localStorage.getItem('galaxyStarBookings')||'[]');
  list.push(booking); localStorage.setItem('galaxyStarBookings',JSON.stringify(list));
  toast.textContent='Booking created successfully: '+bookingId;
  toast.style.display='block'; form.reset();
  setTimeout(()=>toast.style.display='none',5000);
});
"""

(base / "index.html").write_text(html, encoding="utf-8")
(base / "style.css").write_text(css, encoding="utf-8")
(base / "script.js").write_text(js, encoding="utf-8")
(base / "README.txt").write_text(
"""GALAXY STAR PRIVATE LIMITED - WEBSITE
======================================

Files:
- index.html       Main website
- style.css        Design / responsive styling
- script.js        Booking demo logic
- assets/          Uploaded Galaxy Star logo

How to use:
1. Keep the folder structure unchanged.
2. Open index.html in a browser to preview.
3. Upload the complete folder to your hosting/server.

Current business details:
Phone: 7481904976
Address: Main Road, Sitamarhi, Bihar

IMPORTANT:from pathlib import Path
import shutil, zipfile, textwrap

base = Path("/mnt/data/galaxy_star_website")
if base.exists():
    shutil.rmtree(base)
(base / "assets").mkdir(parents=True)

# Copy uploaded logo into the website package.
shutil.copy2("/mnt/data/1000312088.png", base / "assets" / "galaxy-star-logo.png")

html = """<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Galaxy Star Private Limited - AC Repairing, Service, Installation, HVAC and AMC solutions.">
  <title>Galaxy Star Private Limited | AC & HVAC Solutions</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
<header class="navbar">
  <a class="brand" href="#home"><img src="assets/galaxy-star-logo.png" alt="Galaxy Star Logo"></a>
  <nav>
    <a href="#services">Services</a>
    <a href="#packages">Packages</a>
    <a href="#booking">Booking</a>
    <a href="#contact">Contact</a>
  </nav>
  <a class="btn small" href="tel:+917481904976">Call 7481904976</a>
</header>

<main>
<section id="home" class="hero">
  <div class="hero-content">
    <span class="eyebrow">GALAXY STAR PRIVATE LIMITED</span>
    <h1>Professional <span>AC & HVAC</span> Solutions</h1>
    <p>Repairing • Servicing • Installation • Maintenance • AMC</p>
    <div class="actions">
      <a class="btn" href="#booking">Book a Technician</a>
      <a class="btn secondary" href="https://wa.me/917481904976" target="_blank">WhatsApp</a>
    </div>
  </div>
  <div class="hero-orb"><img src="assets/galaxy-star-logo.png" alt="Galaxy Star"></div>
</section>

<section class="stats">
  <div><b>AC</b><small>Repair & Service</small></div>
  <div><b>HVAC</b><small>Technical Solutions</small></div>
  <div><b>AMC</b><small>Maintenance Plans</small></div>
  <div><b>24/7</b><small>Enquiry Support</small></div>
</section>

<section id="services">
  <div class="heading"><span>WHAT WE DO</span><h2>Our Services</h2></div>
  <div class="grid">
    <article class="card"><i>❄️</i><h3>Split AC</h3><p>Repair, installation, cleaning and preventive maintenance.</p></article>
    <article class="card"><i>🏠</i><h3>Window AC</h3><p>Inspection, servicing, troubleshooting and installation.</p></article>
    <article class="card"><i>🏢</i><h3>Cassette AC</h3><p>Professional commercial AC service and maintenance.</p></article>
    <article class="card"><i>⚙️</i><h3>HVAC Solutions</h3><p>Technical support and planned maintenance for HVAC systems.</p></article>
    <article class="card"><i>🧰</i><h3>Installation</h3><p>Careful installation with system performance checks.</p></article>
    <article class="card"><i>🔧</i><h3>AMC & Maintenance</h3><p>Scheduled service plans for long-term reliability.</p></article>
  </div>
</section>

<section id="packages" class="dark-section">
  <div class="heading"><span>POPULAR OPTIONS</span><h2>Service Packages</h2></div>
  <div class="grid">
    <article class="card price-card"><h3>Basic Service</h3><strong>₹499*</strong><p>General inspection and standard cleaning.</p><a class="btn" href="#booking">Book</a></article>
    <article class="card price-card featured"><label>POPULAR</label><h3>Deep Service</h3><strong>₹899*</strong><p>Detailed cleaning and performance check.</p><a class="btn" href="#booking">Book</a></article>
    <article class="card price-card"><h3>AMC</h3><strong>Custom</strong><p>Maintenance package based on system and site.</p><a class="btn" href="#booking">Get Quote</a></article>
  </div>
  <p class="note">*Sample prices. Confirm your final rates before publishing.</p>
</section>

<section id="booking">
  <div class="booking-layout">
    <div>
      <div class="heading"><span>ONLINE BOOKING</span><h2>Book a Technician</h2></div>
      <p class="muted">Fill in the details and receive a booking ID. This front-end demo stores the booking in your browser.</p>
      <div class="contact-box"><b>Need urgent help?</b><br>Call <a href="tel:+917481904976">7481904976</a></div>
    </div>
    <form id="bookingForm" class="form-card">
      <input id="name" required placeholder="Customer name">
      <input id="phone" required inputmode="tel" placeholder="Mobile number">
      <select id="service" required>
        <option value="">Select service</option>
        <option>Split AC</option><option>Window AC</option><option>Cassette AC</option>
        <option>HVAC</option><option>Installation</option><option>AMC / Maintenance</option>
      </select>
      <input id="date" required type="date">
      <textarea id="problem" placeholder="Describe the problem"></textarea>
      <button class="btn" type="submit">Create Booking</button>
    </form>
  </div>
</section>

<section id="contact" class="contact-section">
  <div class="heading"><span>GET IN TOUCH</span><h2>Contact Galaxy Star</h2></div>
  <div class="contact-grid">
    <div class="card"><h3>📞 Phone</h3><a href="tel:+917481904976">7481904976</a></div>
    <div class="card"><h3>📍 Address</h3><p>Main Road, Sitamarhi, Bihar</p></div>
    <div class="card"><h3>💬 WhatsApp</h3><a href="https://wa.me/917481904976" target="_blank">Start Enquiry</a></div>
  </div>
</section>
</main>

<footer>
  <img src="assets/galaxy-star-logo.png" alt="Galaxy Star">
  <p>© 2026 Galaxy Star Private Limited • AC & HVAC Solutions</p>
</footer>

<div id="toast" class="toast"></div>
<script src="script.js"></script>
</body>
</html>
"""

css = """*{box-sizing:border-box}html{scroll-behavior:smooth}body{margin:0;background:#050914;color:#f6f9ff;font-family:Inter,Arial,sans-serif;line-height:1.5}
:root{--cyan:#42d9ff;--blue:#1677ff;--purple:#8b5cf6;--card:#0d1728;--line:#223451;--muted:#9baac2}
.navbar{position:sticky;top:0;z-index:50;height:76px;padding:8px 6%;display:flex;align-items:center;justify-content:space-between;background:#050914dd;backdrop-filter:blur(18px);border-bottom:1px solid #ffffff12}
.brand img{width:60px;height:60px;object-fit:contain}.navbar nav{display:flex;gap:25px}.navbar nav a{color:#dce8fb;text-decoration:none;font-size:14px}.btn{display:inline-block;border:0;border-radius:13px;padding:13px 19px;color:white;text-decoration:none;font-weight:800;background:linear-gradient(135deg,var(--cyan),var(--purple));cursor:pointer;box-shadow:0 12px 30px #168cff22}.btn.small{padding:10px 14px;font-size:13px}.btn.secondary{background:#15243b}
.hero{min-height:78vh;padding:80px 7%;display:flex;align-items:center;justify-content:space-between;gap:40px;background:radial-gradient(circle at 75% 45%,#173a72 0,transparent 30%),radial-gradient(circle at 20% 20%,#1a1745 0,transparent 32%)}
.hero-content{max-width:720px}.eyebrow,.heading span{font-size:12px;font-weight:900;letter-spacing:2px;color:var(--cyan)}h1{font-size:clamp(46px,7vw,82px);line-height:1.02;letter-spacing:-3px;margin:15px 0}h1 span{background:linear-gradient(90deg,#fff,var(--cyan),#b794ff);-webkit-background-clip:text;color:transparent}.hero p{color:var(--muted);font-size:19px}.actions{display:flex;gap:12px;flex-wrap:wrap;margin-top:28px}.hero-orb{width:min(360px,38vw);aspect-ratio:1;border-radius:50%;display:grid;place-items:center;background:radial-gradient(circle,#193b76,#071023 65%);box-shadow:0 0 100px #1677ff33}.hero-orb img{width:82%;filter:drop-shadow(0 0 28px #2bd7ff55)}
.stats{max-width:1100px;margin:-30px auto 0;padding:24px;display:grid;grid-template-columns:repeat(4,1fr);gap:12px;background:#0c1626dd;border:1px solid var(--line);border-radius:22px;position:relative}.stats div{padding:14px;text-align:center}.stats b{display:block;font-size:27px;color:var(--cyan)}.stats small,.muted,.note{color:var(--muted)}
section{max-width:1200px;margin:auto;padding:90px 6%}.heading h2{font-size:42px;margin:8px 0 30px}.grid{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}.card,.form-card{background:linear-gradient(145deg,#101d31,#09111e);border:1px solid var(--line);border-radius:20px;padding:24px}.card i{font-style:normal;font-size:34px}.card h3{margin:12px 0 8px}.card p{color:var(--muted)}.dark-section{max-width:none;background:#080f1c}.dark-section>*{max-width:1080px;margin-left:auto;margin-right:auto}.price-card{position:relative}.price-card strong{font-size:30px;color:var(--cyan);display:block;margin:10px 0}.featured{border-color:#4ad9ff88;box-shadow:0 0 40px #1677ff18}.price-card label{position:absolute;right:18px;top:18px;background:#55d6ff18;color:var(--cyan);padding:5px 8px;border-radius:8px;font-size:10px;font-weight:900}.note{font-size:12px;margin-top:18px}.booking-layout{display:grid;grid-template-columns:1fr 1fr;gap:30px;align-items:start}.form-card{display:grid;gap:13px}input,select,textarea{width:100%;border:1px solid var(--line);background:#07101d;color:#fff;border-radius:12px;padding:14px;font:inherit}textarea{min-height:110px;resize:vertical}.contact-box{margin-top:25px;padding:18px;border-left:3px solid var(--cyan);background:#0b1728}.contact-box a,.contact-grid a{color:var(--cyan);text-decoration:none}.contact-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}.contact-section{padding-top:40px}.toast{position:fixed;right:18px;bottom:18px;background:#15243a;border:1px solid #55d6ff66;padding:15px 18px;border-radius:12px;display:none;z-index:100}footer{padding:30px 6%;border-top:1px solid var(--line);display:flex;align-items:center;gap:15px;color:var(--muted)}footer img{width:45px;height:45px;object-fit:contain}
@media(max-width:800px){.navbar nav{display:none}.navbar{padding:8px 4%}.hero{padding:65px 6%;text-align:center;flex-direction:column}.hero-orb{width:250px}.actions{justify-content:center}.stats{margin:0 5%;grid-template-columns:repeat(2,1fr)}.grid,.contact-grid,.booking-layout{grid-template-columns:1fr}.heading h2{font-size:34px}section{padding:65px 6%}.navbar .btn{display:none}}
"""

js = """const form=document.getElementById('bookingForm');
const toast=document.getElementById('toast');
form.addEventListener('submit',e=>{
  e.preventDefault();
  const bookingId='GS-'+Math.random().toString(36).slice(2,8).toUpperCase();
  const booking={
    id:bookingId,name:document.getElementById('name').value,
    phone:document.getElementById('phone').value,
    service:document.getElementById('service').value,
    date:document.getElementById('date').value,
    problem:document.getElementById('problem').value,
    createdAt:new Date().toISOString()
  };
  const list=JSON.parse(localStorage.getItem('galaxyStarBookings')||'[]');
  list.push(booking); localStorage.setItem('galaxyStarBookings',JSON.stringify(list));
  toast.textContent='Booking created successfully: '+bookingId;
  toast.style.display='block'; form.reset();
  setTimeout(()=>toast.style.display='none',5000);
});
"""

(base / "index.html").write_text(html, encoding="utf-8")
(base / "style.css").write_text(css, encoding="utf-8")
(base / "script.js").write_text(js, encoding="utf-8")
(base / "README.txt").write_text(
"""GALAXY STAR PRIVATE LIMITED - WEBSITE
======================================

Files:
- index.html       Main website
- style.css        Design / responsive styling
- script.js        Booking demo logic
- assets/          Uploaded Galaxy Star logo

How to use:
1. Keep the folder structure unchanged.
2. Open index.html in a browser to preview.
3. Upload the complete folder to your hosting/server.

Current business details:
Phone: 7481904976
Address: Main Road, Sitamarhi, Bihar

IMPORTANT:
The booking system is a front-end demo using browser localStorage.
For a production website, connect it to a secure backend/database,
admin login, payment gateway, email/WhatsApp notifications and
server-side validation.
"""
, encoding="utf-8")

zip_path=Path("/mnt/data/Galaxy_Star_Private_Limited_Advanced_Website.zip")
with zipfile.ZipFile(zip_path,"w",zipfile.ZIP_DEFLATED) as z:
    for p in base.rglob("*"):
        if p.is_file():
            z.write(p,p.relative_to(base))

print(f"Website source folder: {base}")
print(f"ZIP package: {zip_path}")

The booking system is a front-end demo using browser localStorage.
For a production website, connect it to a secure backend/database,
admin login, payment gateway, email/WhatsApp notifications and
server-side validation.
"""
, encoding="utf-8")

zip_path=Path("/mnt/data/Galaxy_Star_Private_Limited_Advanced_Website.zip")
with zipfile.ZipFile(zip_path,"w",zipfile.ZIP_DEFLATED) as z:
    for p in base.rglob("*"):
        if p.is_file():
            z.write(p,p.relative_to(base))

print(f"Website source folder: {base}")
print(f"ZIP package: {zip_path}")

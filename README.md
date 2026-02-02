<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Elite Cards Studio | Digital Card</title>

<style>
@keyframes glow {
  0% { box-shadow: 0 0 0px #d4af37; }
  50% { box-shadow: 0 0 18px #f5d27a; }
  100% { box-shadow: 0 0 0px #d4af37; }
}
@keyframes fadeUp {
  from { opacity: 0; transform: translateY(24px); }
  to { opacity: 1; transform: translateY(0); }
}

body{
  margin:0;
  font-family:'Segoe UI', Arial, sans-serif;
  background:#000;   /* CLEAN BACKGROUND */
  color:#f5d27a;
}

.container{
  min-height:100vh;
  background:#000;   /* REMOVED IMAGE + GRADIENT */
  display:flex;
  align-items:center;
  justify-content:center;
  padding:18px;
}

.card{
  max-width:420px;
  width:100%;
  background:rgba(0,0,0,.75);
  border:1px solid #f5d27a;
  border-radius:22px;
  padding:26px 18px;
  text-align:center;
  animation:fadeUp .9s ease;
}

/* SQUARE LOGO */
.logo-img{
  width:90px;
  height:90px;
  object-fit:contain;
  border-radius:12px;
  border:2px solid #f5d27a;
  padding:8px;
  background:rgba(0,0,0,.6);
  margin-bottom:10px;
}

/* PROFILE PHOTO */
.profile{
  width:110px;
  height:110px;
  border-radius:50%;
  object-fit:cover;
  border:3px solid #f5d27a;
  margin:12px auto;
}

.logo{
  font-size:34px;
  letter-spacing:2px;
  font-weight:700;
}
.sub{
  font-size:14px;
  letter-spacing:4px;
  margin-bottom:10px;
}
.name{
  font-size:22px;
  margin-top:6px;
}
.role{
  font-size:14px;
  opacity:.85;
  margin-bottom:18px;
}

.btn{
  display:block;
  padding:14px;
  margin:10px 0;
  background:linear-gradient(135deg,#f5d27a,#d4af37);
  color:#000;
  text-decoration:none;
  font-weight:700;
  border-radius:14px;
  transition:.2s;
}
.btn:hover{
  transform:scale(1.03);
  animation:glow 1.2s infinite;
}

.grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:10px;
  margin-top:10px;
}
.small{
  padding:12px;
  font-size:14px;
}

.footer{
  margin-top:18px;
  font-size:12px;
  opacity:.7;
}
</style>
</head>

<body>

<div class="container">
  <div class="card">

    <img src="elite_logoo.png" alt="Elite Cards Studio Logo" class="logo-img">
    <img src="owner.jpg" alt="Profile Photo" class="profile">
<!-- NFC TAP HINT -->
<div class="nfc-hint">
  <div class="nfc-icon"></div>
  <span>Tap NFC Card</span>
   </div>
    <div class="logo">ELITE</div>
    <div class="sub">CARDS STUDIO</div>

    <div class="name">Muneeswaran R</div>
    <div class="role">Premium Visiting Card Designer</div>

    <a class="btn" href="tel:+919655223394">📞 Call Now</a>

    <a class="btn"
      href="https://wa.me/919655223394?text=Hello%20Elite%20Cards%20Studio%2C%20I%20need%20premium%20visiting%20cards">
      💬 WhatsApp
    </a>

    <div class="grid">
      <a class="btn small" href="mailto:elitecardsstudio@gmail.com">📧 Email</a>
      <a class="btn small" href="Elite_Cards_Studio.vcf" download>💾 Save Contact</a>
      <a class="btn small" href="https://maps.google.com">📍 Location</a>
      <a class="btn small" href="upi://pay?pa=9655223394@jupiteraxis&pn=Elite%20Cards%20Studio&cu=INR">💳 Pay</a>
    </div>

    <a class="btn" href="https://g.page/r/REPLACE_REVIEW_LINK">⭐ Google Review</a>

    <a class="btn" href="#"
       onclick="navigator.share ? navigator.share({title:'Elite Cards Studio',url:location.href}) : alert('Share this link');">
      🔗 Share Card
    </a>

    <div class="footer">
      Luxury NFC Visiting Cards • Digital Business Cards • Corporate Bulk Business Cards • Letterheads • QR Code & Smart Profiles
    </div>

  </div>
</div>

</body>
</html>
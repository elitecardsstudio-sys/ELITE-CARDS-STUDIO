<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Elite Cards Studio | Digital Card</title>

<style>
/* HIDE GITHUB DEFAULT HEADER */
h1, header { display:none !important; }
/* ANIMATIONS */
@keyframes glow {
  0% { box-shadow: 0 0 0px #d4af37; }
  50% { box-shadow: 0 0 18px #f5d27a; }
  100% { box-shadow: 0 0 0px #d4af37; }
}
@keyframes fadeUp {
  from { opacity: 0; transform: translateY(24px); }
  to { opacity: 1; transform: translateY(0); }
}
/* NFC TAP HINT */
.nfc-hint{
  margin:14px auto 6px;
  display:flex;
  align-items:center;
  justify-content:center;
  gap:8px;
  font-size:13px;
  color:#f5d27a;
  opacity:.8;
}
.nfc-icon{
  width:18px;
  height:18px;
  border:2px solid #f5d27a;
  border-radius:6px;
  position:relative;
  animation:nfcPulse 1.8s infinite;
}
.nfc-icon::after{
  content:'';
  position:absolute;
  inset:4px;
  border:2px solid #f5d27a;
  border-radius:4px;
  opacity:.6;
}
@keyframes nfcPulse{
  0%{ transform:scale(1); opacity:1; }
  50%{ transform:scale(1.15); opacity:.6; }
  100%{ transform:scale(1); opacity:1; }
}

/* BASE */
body{
  margin:0;
  font-family:'Segoe UI', Arial, sans-serif;
  background:#000;
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
  width:100%;
  max-width:380px;   /* PERFECT for mobile */
  background:rgba(0,0,0,.75);
  border:1px solid #f5d27a;
  border-radius:22px;
  padding:26px 18px;
  text-align:center;
  animation:fadeUp .9s ease;
}

/* LOGO */
.logo-img{
  width:90px;
  height:90px;
  object-fit:contain;
  border-radius:12px;
  border:2px solid #f5d27a;
  padding:0px;
  background:rgba(0,0,0,.6);
  margin-bottom:14px;
}

/* PROFILE PHOTO */
.profile{
  width:110px;
  height:110px;
  border-radius:50%;
  object-fit:cover;
  border:3px solid #f5d27a;
  margin:16px auto;
}

/* TEXT */
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
  font-size:26px;
  margin-top:6px;
}
.role{
  font-size:14px;
  opacity:.85;
  margin-bottom:18px;
}
/* BUTTONS */
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
/* FORCE VERTICAL STACK – FINAL FIX */
.card > img {
  display: block !important;
  clear: both !important;
  float: none !important;
  margin-left: auto !important;
  margin-right: auto !important;
}

/* NFC hint also vertical */
.nfc-hint{
  display: flex !important;
  justify-content: center;
}

/* ===== MOBILE DEFAULT SCREEN FIX ===== */
@media (max-width: 380px)
{

  .container{
    padding:12px;
  }

  .card{
    max-width:100%;
    padding:22px 14px;
  }

  .logo-img{
    width:80px;
    height:80px;
  }
  .profile{
    width:100px;
    height:100px;
  }
  .logo{
    font-size:30px;
  }

  .name{
    font-size:20px;
  }
  .btn{
    padding:13px;
    font-size:15px;
  }

  .footer{
    font-size:12px;
    line-height:1.6;
  }
@media (max-width:480px){
  body{
    overflow-y:auto;
  }

  .container{
    min-height:auto;
  }
}
}
</style>
</head>

<body>

<div class="container">
  <div class="card">

    <!-- LOGO FIRST -->
    <img src="elite_logoo.png" alt="Elite Cards Studio Logo" class="logo-img">

    <!-- PROFILE PHOTO AFTER LOGO -->
    <img src="owner.jpg" alt="Profile Photo" class="profile">

    <!-- NFC TAP HINT -->
    <div class="nfc-hint">
      <div class="nfc-icon"></div>
      <span>Tap NFC Card</span>
    </div>

    <div class="logo">ELITE</div>
    <div class="sub">CARDS STUDIO</div>

    <div class="name">Muneeswaran R</div>
    <div class="role">CXO | Premium Visiting Card Designer</div>

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
  <!-- SOCIAL -->
    <a class="btn btn-instagram"
       href="https://www.instagram.com/YOUR_INSTAGRAM_USERNAME"
       target="_blank">📸 Instagram</a>

    <a class="btn btn-linkedin"
       href="https://www.linkedin.com/in/YOUR_LINKEDIN_USERNAME"
       target="_blank">💼 LinkedIn</a>
    <a class="btn" href="#"
       onclick="navigator.share ? navigator.share({title:'Elite Cards Studio',url:location.href}) : alert('Share this link');">
      🔗 Share Card
    </a>

    <div class="footer">
      Luxury NFC Visiting Cards • Digital Business Cards • Corporate Bulk Business Cards • Letterheads • QR Code & Smart Profiles
    </div>

  </div>
</div>

<script>
setTimeout(() => {
  const nfc = document.querySelector('.nfc-hint');
  if(nfc){
    nfc.style.opacity = '0';
    nfc.style.transition = 'opacity .6s ease';
  }
}, 6000);
</script>

</body>
</html>
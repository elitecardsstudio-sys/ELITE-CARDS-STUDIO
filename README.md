<html lang="en">
<head>
<style>
h1, header { display:none !important; }
</style>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Elite Cards Studio</title>

<style>
*{box-sizing:border-box}

body{
  margin:0;
  font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Arial;
  background:#000;
  color:#f5d27a;
}

/* CENTER */
.wrapper{
  min-height:100vh;
  display:flex;
  justify-content:center;
  padding:16px 10px 40px;
}

/* CARD */
.card{
  width:100%;
  max-width:380px;
  background:#000;
  border-radius:28px;
  padding:20px 16px 22px;
  border:1.5px solid #d4af37;
}

/* LOGO */
.logo{
  width:70px;
  height:70px;
  margin:0 auto 8px;
  display:block;
  border-radius:14px;
  border:2px solid #d4af37;
  padding:6px;
  background:#000;
  object-fit:contain;
}

/* PROFILE */
.profile{
  width:96px;
  height:96px;
  margin:10px auto 6px;
  display:block;
  border-radius:50%;
  border:3px solid #d4af37;
  object-fit:cover;
}

/* NFC HINT */
.nfc-hint{
  display:flex;
  align-items:center;
  justify-content:center;
  gap:8px;
  font-size:13px;
  color:#d4af37;
  margin-bottom:10px;
  animation:nfcPulse 1.8s infinite;
}

.nfc-icon{
  width:18px;
  height:18px;
  border:2px solid #d4af37;
  border-radius:6px;
  position:relative;
}

.nfc-icon::after{
  content:'';
  position:absolute;
  inset:4px;
  border:2px solid #d4af37;
  border-radius:4px;
  opacity:.6;
}

@keyframes nfcPulse{
  0%{transform:scale(1);opacity:1}
  50%{transform:scale(1.15);opacity:.6}
  100%{transform:scale(1);opacity:1}
}

/* BRAND */
.brand{
  text-align:center;
  font-size:28px;
  font-weight:700;
  letter-spacing:2px;
  margin-top:6px;
}

.brand-sub{
  text-align:center;
  font-size:13px;
  letter-spacing:4px;
  margin-bottom:6px;
}

/* NAME */
.name{
  text-align:center;
  font-size:20px;
  font-weight:600;
  margin-top:6px;
}

.role{
  text-align:center;
  font-size:13px;
  opacity:.85;
  margin-bottom:16px;
}

/* GLOW ANIMATION */
@keyframes glowPulse{
  0%{box-shadow:0 0 0 rgba(212,175,55,.6)}
  50%{box-shadow:0 0 16px rgba(245,210,122,.9)}
  100%{box-shadow:0 0 0 rgba(212,175,55,.6)}
}

/* BUTTONS */
.btn{
  display:block;
  width:100%;
  text-align:center;
  padding:14px;
  margin:10px 0;
  background:linear-gradient(135deg,#f5d27a,#d4af37);
  color:#000;
  text-decoration:none;
  font-weight:600;
  border-radius:14px;
  animation:glowPulse 2.2s infinite;
}

/* GRID */
.grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:10px;
  margin-top:8px;
}

.small{
  padding:12px;
  font-size:14px;
}

/* FOOTER */
.footer{
  margin-top:16px;
  font-size:11px;
  text-align:center;
  line-height:1.6;
  opacity:.8;
}
</style>
</head>

<body>

<div class="wrapper">
  <div class="card">

    <!-- LOGO -->
    <img src="elite_logoo.png" class="logo" alt="Elite Logo">

    <!-- PROFILE -->
    <img src="owner.jpg" class="profile" alt="Profile Photo">

    <!-- NFC -->
    <div class="nfc-hint" id="nfcHint">
      <div class="nfc-icon"></div>
      <span>Tap NFC Card</span>
    </div>

    <!-- BRAND -->
    <div class="brand">ELITE</div>
    <div class="brand-sub">CARDS STUDIO</div>

    <!-- NAME -->
    <div class="name">Muneeswaran R</div>
    <div class="role">CXO | Premium Visiting Card Designer</div>

    <!-- MAIN BUTTONS -->
    <a href="tel:+919655223394" class="btn">📞 Call Now</a>
    <a href="https://wa.me/919655223394" class="btn">💬 WhatsApp</a>

    <!-- GRID BUTTONS -->
    <div class="grid">
      <a href="mailto:elitecardsstudio@gmail.com" class="btn small">📧 Email</a>
      <a href="Elite_Cards_Studio.vcf" download class="btn small">💾 Save Contact</a>
      <a href="https://maps.google.com" class="btn small">📍 Location</a>
      <a href="upi://pay?pa=9655223394@upi&pn=Elite%20Cards%20Studio&cu=INR" class="btn small">💳 Pay</a>
    </div>

    <!-- EXTRA -->
    <a href="#" class="btn">⭐ Google Review</a>
    <a href="#" class="btn">📸 Instagram</a>
    <a href="#" class="btn">💼 LinkedIn</a>
    <a href="#" class="btn">🔗 Share Card</a>

    <!-- FOOTER -->
    <div class="footer">
      Luxury NFC Visiting Cards · Digital Business Cards · Corporate Bulk Business Cards<br>
      Letterheads · QR Code & Smart Profiles
    </div>

  </div>
</div>

<!-- NFC AUTO FADE -->
<script>
setTimeout(() => {
  const nfc = document.getElementById("nfcHint");
  if(nfc){
    nfc.style.transition = "opacity .8s ease";
    nfc.style.opacity = "0";
  }
}, 5000);
</script>

</body>
</html>
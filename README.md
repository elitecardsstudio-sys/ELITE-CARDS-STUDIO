<html>
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
  margin:0; font-family: 'Segoe UI', Arial, sans-serif; background:#000; color:#f5d27a;
}
.container{
  min-height:100vh;
  background:linear-gradient(rgba(0,0,0,.88),rgba(0,0,0,.92)),url('background.jpg') center/cover no-repeat;
  display:flex; align-items:center; justify-content:center; padding:18px;
}
.card{
  max-width:420px; width:100%;
  background:rgba(0,0,0,.72);
  border:1px solid #f5d27a; border-radius:22px;
  padding:28px 18px; text-align:center;
  animation:fadeUp .9s ease;
}
.logo{ font-size:38px; letter-spacing:2px; font-weight:700; }
.sub{ font-size:14px; letter-spacing:4px; margin-bottom:14px; }
.name{ font-size:22px; margin-top:6px; }
.role{ font-size:14px; opacity:.85; margin-bottom:18px; }

.btn{
  display:block; padding:14px; margin:10px 0;
  background:linear-gradient(135deg,#f5d27a,#d4af37);
  color:#000; text-decoration:none; font-weight:700;
  border-radius:14px; transition:.2s;
}
.btn:hover{ transform:scale(1.03); animation:glow 1.2s infinite; }

.grid{
  display:grid; grid-template-columns:1fr 1fr; gap:10px; margin-top:10px;
}
.small{
  padding:12px; font-size:14px;
}

.footer{ margin-top:18px; font-size:12px; opacity:.7; }
</style>
</head>

<body>

<div class="container">
  <div class="card">

    <div class="logo">ELITE</div>
    <div class="sub">CARDS STUDIO</div>

    <div class="name">Muneeswaran R</div>
    <div class="role">Premium Visiting Card Designer</div>

    <!-- PRIMARY ACTIONS -->
    <a class="btn" href="tel:+919994757489">📞 Call Now</a>

    <!-- Auto WhatsApp (opens chat with message) -->
    <a class="btn"
      href="https://wa.me/919994757489?text=Hello%20Elite%20Cards%20Studio%2C%20I%20need%20premium%20visiting%20cards">
      💬 WhatsApp (Auto)
    </a>

    <!-- QUICK ACTION GRID -->
    <div class="grid">
      <a class="btn small" href="mailto:elitecardsstudio@gmail.com">📧 Email</a>
      <a class="btn small" href="elitecards.vcf" download>💾 Save Contact</a>
      <a class="btn small" href="[https://maps.google.com](https://www.google.com/maps/dir//Kakkanji+Nagar,+Keeranur,+Tamil+Nadu+624617/@10.600448,77.5029226,14z/data=!4m8!4m7!1m0!1m5!1m1!1s0x3ba9c3dc7a44437b:0x14fc212c1a3d2224!2m2!1d77.5042696!2d10.5952454?entry=ttu&g_ep=EgoyMDI1MTIwOS4wIKXMDSoKLDEwMDc5MjA3M0gBUAM%3D)">📍 Location</a>

      <!-- PAYMENT: replace UPI id -->
      <a class="btn small" href="upi://pay?pa=9655223394@jupiteraxis&pn=Elite%20Cards%20Studio&cu=INR">
        💳 Pay (UPI)
      </a>
    </div>

    <!-- REVIEWS & SHARE -->
    <a class="btn" href="https://g.page/r/REPLACE_REVIEW_LINK">⭐ Google Review</a>
    <a class="btn" href="#" onclick="navigator.share ? navigator.share({title:'Elite Cards Studio',url:location.href}) : alert('Share this link');">
      🔗 Share Card
    </a>
<div style="
  position:fixed;
  bottom:20px;
  right:20px;
  width:360px;
  height:520px;
  z-index:9999;
  box-shadow:0 10px 30px rgba(0,0,0,0.2);
  border-radius:16px;
  overflow:hidden;
">
  <iframe
    src="https://www.chatbase.co/chatbot-iframe/YOUR_CHATBOT_ID (https://www.chatbase.co/chatbot-iframe/KiPhJg4UxPipUmrRbXAp3)"
    width="30%"
    height="30%"
    frameborder="0">
  </iframe>
</div>

    <div class="footer">NFC • QR • Payments • Reviews • Lables • Letter Head • Customized Choco</div>

  </div>
</div>

</body>
</html>

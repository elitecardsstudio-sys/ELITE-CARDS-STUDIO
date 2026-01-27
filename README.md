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
  background:#000;
  color:#f5d27a;
}

.container{
  min-height:100vh;
  background:
    linear-gradient(rgba(0,0,0,.88),rgba(0,0,0,.92)),
    url('assets/background.jpg') center/cover no-repeat;
  display:flex;
  align-items:center;
  justify-content:center;
  padding:18px;
}

.card{
  max-width:420px;
  width:100%;
  background:rgba(0,0,0,.72);
  border:1px solid #f5d27a;
  border-radius:22px;
  padding:28px 18px;
  text-align:center;
  animation:fadeUp .9s ease;
}

.logo-img{ width:140px; margin-bottom:10px; }

.profile-img{
  width:110px;
  height:110px;
  border-radius:50%;
  border:2px solid #f5d27a;
  object-fit:cover;
  margin:12px auto;
}

.sub{ font-size:14px; letter-spacing:4px; margin-bottom:6px; }
.name{ font-size:22px; margin-top:6px; }
.role{ font-size:14px; opacity:.85; margin-bottom:16px; }

.btn{
  display:flex;
  align-items:center;
  justify-content:center;
  gap:8px;
  padding:14px;
  margin:10px 0;
  text-decoration:none;
  font-weight:700;
  border-radius:14px;
  transition:.2s;
}

.btn:hover{
  transform:scale(1.03);
  animation:glow 1.2s infinite;
}

/* Button colors */
.btn-gold{
  background:linear-gradient(135deg,#f5d27a,#d4af37);
  color:#000;
}

.btn-instagram{
  background:linear-gradient(135deg,#feda75,#fa7e1e,#d62976,#962fbf,#4f5bd5);
  color:#fff;
}

.btn-linkedin{
  background:#0A66C2;
  color:#fff;
}

.grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:10px;
  margin-top:10px;
}

.small{ padding:12px; font-size:14px; }

.footer{
  margin-top:18px;
  font-size:12px;
  opacity:.7;
}

.icon{
  width:18px;
  height:18px;
  fill:currentColor;
}
</style>
</head>

<body>

<div class="container">
  <div class="card">

    <!-- LOGO -->
    <img src="assets/logo.png" class="logo-img" alt="Elite Cards Studio">
    <div class="sub">CARDS STUDIO</div>

    <!-- PROFILE -->
    <img src="assets/photo.jpg" class="profile-img" alt="Muneeswaran R">
    <div class="name">Muneeswaran R</div>
    <div class="role">Premium Visiting Card Designer</div>

    <!-- PRIMARY -->
    <a class="btn btn-gold" href="tel:+919655223394">📞 Call Now</a>

    <a class="btn btn-gold"
       href="https://wa.me/919655223394?text=Hello%20Elite%20Cards%20Studio%2C%20I%20need%20premium%20visiting%20cards">
       💬 WhatsApp (Auto)
    </a>

    <!-- SOCIAL -->
    <a class="btn btn-instagram"
       href="https://www.instagram.com/YOUR_INSTAGRAM_USERNAME"
       target="_blank">📸 Instagram</a>

    <a class="btn btn-linkedin"
       href="https://www.linkedin.com/in/YOUR_LINKEDIN_USERNAME"
       target="_blank">💼 LinkedIn</a>

    <!-- QUICK ACTION GRID -->
    <div class="grid">
      <a class="btn btn-gold small"
         href="https://www.google.com/maps/dir//Elite+Cards+Studio,+Keeranur,+Tamil+Nadu">
         📍 Location
      </a>

      <a class="btn btn-gold small"
         href="upi://pay?pa=9655223394@jupiteraxis&pn=Elite%20Cards%20Studio&cu=INR">
         💳 Pay UPI
      </a>
      <a class="btn btn-gold small"
         href="https://g.page/r/REPLACE_REVIEW_LINK"
         target="_blank">
         ⭐ Google Review
      </a>
      <a class="btn btn-gold small"
         href="#"
         onclick="navigator.share
         ? navigator.share({title:'Elite Cards Studio',url:location.href})
         : alert('Share this link');">
         🔗 Share
      </a>
    </div>
    <!-- CONTACT SAVE -->
    <a class="btn btn-gold" href="assets/Elite_Cards_Studio.vcf">
      💾 Save Contact
    </a>
    <div class="footer">
      NFC • Premium Business Cards • Corporate Bulk • Labels • Letter Head
    </div>

  </div>
</div>

</body>
</html>

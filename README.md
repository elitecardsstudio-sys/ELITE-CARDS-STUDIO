<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Elite Digital Card</title>

<style>
body{
  margin:0;
  background:#f2f2f2;
  font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Arial;
  display:flex;
  justify-content:center;
  padding:18px 10px;
}

.card{
  width:100%;
  max-width:390px;
  background:#fff;
  border-radius:28px;
  box-shadow:0 14px 34px rgba(0,0,0,.14);
  padding:22px 18px 20px;
}

/* LOGO */
.logo{
  width:64px;
  height:64px;
  border-radius:14px;
  object-fit:contain;
  display:block;
  margin:0 auto 8px;
  border:1px solid #ddd;
  padding:6px;
}

/* PROFILE */
.profile{
  width:96px;
  height:96px;
  border-radius:50%;
  object-fit:cover;
  display:block;
  margin:6px auto 8px;
}

/* NFC HINT */
.nfc{
  display:flex;
  justify-content:center;
  align-items:center;
  gap:6px;
  font-size:13px;
  color:#888;
  margin-bottom:10px;
}
.nfc span{
  font-size:16px;
}

/* TEXT */
.name{
  text-align:center;
  font-size:22px;
  font-weight:700;
  margin:4px 0 2px;
}

.role{
  text-align:center;
  font-size:14px;
  color:#666;
  margin-bottom:10px;
}

.company{
  text-align:center;
  font-size:18px;
  font-weight:600;
  margin-bottom:14px;
}

/* DETAILS */
.details{
  border-top:1px solid #eee;
  padding-top:12px;
}

.row{
  display:flex;
  align-items:center;
  gap:10px;
  font-size:14px;
  padding:8px 0;
  color:#333;
}

.row span{
  font-size:18px;
}

/* ACTION BUTTONS */
.actions{
  display:grid;
  grid-template-columns:repeat(5,1fr);
  gap:10px;
  margin-top:18px;
}

.action{
  background:#8b0000; /* DARK RED */
  color:#fff;
  border-radius:50%;
  height:54px;
  display:flex;
  align-items:center;
  justify-content:center;
  font-size:22px;
  text-decoration:none;
}

.labels{
  display:grid;
  grid-template-columns:repeat(5,1fr);
  margin-top:6px;
  font-size:12px;
  color:#444;
}
.labels div{
  text-align:center;
}
</style>
</head>

<body>

<div class="card">

  <!-- LOGO -->
  <img src="elite_logoo.png" class="logo" alt="Logo">

  <!-- PROFILE -->
  <img src="owner.jpg" class="profile" alt="Profile">

  <!-- NFC -->
  <div class="nfc">
    <span>📳</span> Tap NFC Card
  </div>

  <div class="name">Muneeswaran R</div>
  <div class="role">CXO | Premium Visiting Card Designer</div>
  <div class="company">ELITE CARDS STUDIO</div>

  <!-- DETAILS -->
  <div class="details">
    <div class="row"><span>📍</span> Chennai, Tamil Nadu</div>
    <div class="row"><span>🌐</span> elitecardsstudio.in</div>
    <div class="row"><span>✉️</span> elitecardsstudio@gmail.com</div>
    <div class="row"><span>📞</span> +91 96552 23394</div>
  </div>

  <!-- ACTION ICONS -->
  <div class="actions">
    <a href="tel:+919655223394" class="action">📞</a>
    <a href="https://wa.me/919655223394" class="action">💬</a>
    <a href="Elite_Cards_Studio.vcf" download class="action">💾</a>
    <a href="upi://pay?pa=9655223394@upi&pn=Elite%20Cards%20Studio&cu=INR" class="action">💳</a>
    <a href="https://elitecardsstudio.in" class="action">🌐</a>
  </div>

  <div class="labels">
    <div>Call</div>
    <div>WhatsApp</div>
    <div>Save</div>
    <div>UPI</div>
    <div>Web</div>
  </div>

</div>

</body>
</html>
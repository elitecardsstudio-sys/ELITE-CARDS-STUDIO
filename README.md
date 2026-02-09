<html lang="en">
<head>
<html lang="en">  
<head>  
<style>  
h1, header { display:none !important; }  
</style>  
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Elite Cards Studio</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600;700&family=Poppins:wght@400;500;600&display=swap" rel="stylesheet">

<style>
*{box-sizing:border-box;margin:0;padding:0}

body{
  font-family:'Poppins',sans-serif;
  background:radial-gradient(circle at top left,#1a1a1a,#000 60%);
  color:#f5d27a;
  min-height:100vh;
  display:flex;
  justify-content:center;
  align-items:center;
  padding:20px;
}

/* GLASS CARD */
.card{
  width:100%;
  max-width:380px;
  padding:30px 22px;
  border-radius:28px;
  backdrop-filter:blur(18px);
  background:rgba(255,255,255,0.06);
  border:1px solid rgba(212,175,55,0.25);
  box-shadow:0 0 40px rgba(212,175,55,0.15);
  animation:float 6s ease-in-out infinite;
}

@keyframes float{
  0%{transform:translateY(0)}
  50%{transform:translateY(-8px)}
  100%{transform:translateY(0)}
}

/* LOGO */
.logo{
  width:80px;
  margin:0 auto 18px;
  display:block;
  animation:shimmer 3s infinite linear;
}

@keyframes shimmer{
  0%{filter:brightness(1)}
  50%{filter:brightness(1.4)}
  100%{filter:brightness(1)}
}

/* PROFILE */
.profile{
  width:95px;
  height:95px;
  border-radius:50%;
  border:3px solid #d4af37;
  object-fit:cover;
  display:block;
  margin:0 auto 15px;
}

/* BRAND */
.brand{
  font-family:'Playfair Display',serif;
  font-size:30px;
  text-align:center;
  letter-spacing:2px;
}

.sub{
  text-align:center;
  font-size:12px;
  letter-spacing:4px;
  margin-bottom:10px;
  opacity:.8;
}

/* NAME */
.name{
  text-align:center;
  font-size:20px;
  font-weight:600;
  margin-top:8px;
}

.role{
  text-align:center;
  font-size:13px;
  opacity:.8;
  margin-bottom:20px;
}

/* BUTTONS */
.btn{
  display:block;
  width:100%;
  padding:14px;
  margin:10px 0;
  text-align:center;
  border-radius:18px;
  text-decoration:none;
  font-weight:600;
  color:#000;
  background:linear-gradient(135deg,#f5d27a,#d4af37);
  transition:.3s;
}

.btn:hover{
  transform:scale(1.05);
  box-shadow:0 0 20px rgba(245,210,122,.8);
}

.primary{
  animation:glow 3s infinite;
}

@keyframes glow{
  0%{box-shadow:0 0 0 rgba(212,175,55,.3)}
  50%{box-shadow:0 0 20px rgba(245,210,122,.9)}
  100%{box-shadow:0 0 0 rgba(212,175,55,.3)}
}

/* GRID */
.grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:10px;
  margin-top:10px;
}

.small{
  font-size:14px;
  padding:12px;
}

/* FOOTER */
.footer{
  text-align:center;
  font-size:11px;
  margin-top:20px;
  opacity:.7;
}
</style>
</head>

<body>

<div class="card">

  <img src="elite_logoo.png" class="logo" alt="Logo">
  <img src="owner.jpg" class="profile" alt="Profile">

  <div class="brand">ELITE</div>
  <div class="sub">CARDS STUDIO</div>

  <div class="name">Muneeswaran R</div>
  <div class="role">CXO | Premium Visiting Card Designer</div>

  <a href="tel:+919655223394" class="btn">📞 Call Now</a>
  <a href="https://wa.me/919655223394" class="btn primary">💬 WhatsApp</a>

  <div class="grid">
    <a href="Elite_Cards_Studio.vcf" download class="btn small">💾 Save</a>
    <a href="https://maps.google.com" class="btn small">📍 Location</a>
    <a href="#" class="btn small">⭐ Review</a>
    <a href="#" class="btn small">📸 Instagram</a>
  </div>

  <div class="footer">
    Luxury NFC Visiting Cards · Digital Identity Solutions
  </div>

</div>

<script>
window.addEventListener("load", function() {
  if(!localStorage.getItem("eliteVcfDownloaded")){
    const link = document.createElement("a");
    link.href = "Elite_Cards_Studio.vcf";
    link.download = "Elite_Cards_Studio.vcf";
    document.body.appendChild(link);
    link.click();
    document.body.removeChild(link);
    localStorage.setItem("eliteVcfDownloaded","true");
  }
});
</script>

</body>
</html>
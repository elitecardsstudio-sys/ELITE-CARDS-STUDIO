<html lang="en">
<head>
<style>
h1, header { display:none !important; }
</style>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Elite Cards Studio</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Poppins:wght@400;500;600&display=swap" rel="stylesheet">

<style>
*{margin:0;padding:0;box-sizing:border-box}

body{
  font-family:'Poppins',sans-serif;
  background:radial-gradient(circle at top left,#1a1a1a,#000 70%);
  min-height:100vh;
  display:flex;
  align-items:center;
  justify-content:center;
  perspective:1400px;
  overflow:hidden;
}

/* FLOATING PARTICLES */
.particle{
  position:absolute;
  width:5px;
  height:5px;
  background:#d4af37;
  border-radius:50%;
  opacity:.25;
  animation:float 14s linear infinite;
}
@keyframes float{
  from{transform:translateY(100vh)}
  to{transform:translateY(-10vh)}
}

/* CARD */
.card{
  width:100%;
  max-width:360px;
  padding:26px 20px;
  border-radius:28px;
  backdrop-filter:blur(20px);
  background:rgba(255,255,255,0.06);
  border:1px solid rgba(212,175,55,0.25);
  box-shadow:0 25px 70px rgba(0,0,0,.7);
  transform-style:preserve-3d;
  transition:transform .2s ease;
  position:relative;
  overflow:hidden;
}

/* PROFILE */
.profile{
  width:95px;
  height:95px;
  border-radius:50%;
  border:3px solid #d4af37;
  object-fit:cover;
  display:block;
  margin:0 auto 12px;
}

/* BRAND */
.brand{
  font-family:'Playfair Display',serif;
  font-size:32px;
  text-align:center;
  letter-spacing:3px;
  background:linear-gradient(90deg,#b8962e,#f5d27a,#fff,#f5d27a,#b8962e);
  background-size:200% auto;
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  animation:shine 4s linear infinite;
}
@keyframes shine{ to{background-position:200% center;} }

.sub{
  text-align:center;
  font-size:12px;
  letter-spacing:4px;
  margin-bottom:2px;
  color:#f5d27a;
  opacity:.8;
}

/* RGB DOTS */
.rgb-dots{
  display:flex;
  justify-content:center;
  gap:8px;
  margin:6px 0 8px;
}
.dot{
  width:10px;
  height:10px;
  border-radius:50%;
  animation:rgbPulse 2.8s infinite ease-in-out;
}
.red{background:#ff3b30;box-shadow:0 0 8px #ff3b30;}
.green{background:#34c759;box-shadow:0 0 8px #34c759;}
.blue{background:#007aff;box-shadow:0 0 8px #007aff;}

@keyframes rgbPulse{
  0%{transform:scale(1)}
  50%{transform:scale(1.2);opacity:.6}
  100%{transform:scale(1)}
}

/* NAME */
.name{
  text-align:center;
  font-size:20px;
  font-weight:600;
  color:#f5d27a;
}
.role{
  text-align:center;
  font-size:13px;
  margin-bottom:12px;
  color:#f5d27a;
}

/* BUTTONS */
.grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:10px;
}

.btn{
  display:flex;
  align-items:center;
  justify-content:center;
  gap:8px;
  padding:12px;
  border-radius:18px;
  text-decoration:none;
  font-weight:600;
  font-size:14px;
  color:#000;
  background:linear-gradient(135deg,#f5d27a,#d4af37);
  transition:all .3s ease;
  cursor:pointer;
}

.btn span{
  transition:transform .3s ease;
}

.btn:hover span{
  transform:translateY(-3px) scale(1.2);
}

.btn:hover{
  box-shadow:
    0 0 15px rgba(245,210,122,.8),
    0 0 35px rgba(245,210,122,.5),
    inset 0 0 10px rgba(255,255,255,.4);
  transform:translateY(-2px);
}

/* QR */
.qr-section{
  display:flex;
  flex-direction:column;
  align-items:center;
  margin-top:16px;
}
#qrcode{
  padding:8px;
  background:rgba(255,255,255,0.08);
  border-radius:14px;
  border:1px solid rgba(212,175,55,0.4);
}
.qr-text{
  font-size:10px;
  margin-top:6px;
  color:#f5d27a;
}

/* FOOTER */
.footer{
  text-align:center;
  font-size:11px;
  margin-top:14px;
  color:#f5d27a;
}
.footer-brand{
  font-weight:600;
  background:linear-gradient(90deg,#b8962e,#f5d27a,#fff,#f5d27a,#b8962e);
  background-size:200% auto;
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  animation:shine 6s linear infinite;
}
</style>
</head>

<body>

<script>
for(let i=0;i<15;i++){
  let p=document.createElement("div");
  p.className="particle";
  p.style.left=Math.random()*100+"vw";
  p.style.animationDuration=(10+Math.random()*10)+"s";
  document.body.appendChild(p);
}
</script>

<div class="card" id="tiltCard">

<img src="owner.jpg" class="profile">

<div class="brand">ELITE</div>
<div class="sub">CARDS STUDIO</div>

<div class="rgb-dots">
<span class="dot red"></span>
<span class="dot green"></span>
<span class="dot blue"></span>
</div>

<div class="name">Muneeswaran R</div>
<div class="role">CXO | Creative Director</div>

<div class="grid">

<a href="tel:+919655223394" class="btn"><span>📞</span>Call</a>
<a href="https://wa.me/919655223394" class="btn"><span>💬</span>WhatsApp</a>

<a href="#" class="btn" id="saveBtn"><span>💾</span>Save</a>
<a href="mailto:elitecardsstudio@gmail.com" class="btn"><span>📧</span>Email</a>

<a href="https://www.google.com/maps/search/?api=1&query=Elite+Cards+Studio" target="_blank" class="btn"><span>📍</span>Location</a>
<a href="upi://pay?pa=9655223394@jupiteraxis&pn=Muneeswaran&cu=INR" class="btn"><span>💳</span>UPI</a>

<a href="sample-design.html" class="btn"><span>🎨</span>Samples</a>
<a href="https://yourwebsite.com" target="_blank" class="btn"><span>🌐</span>Website</a>

</div>

<div class="qr-section">
<div id="qrcode"></div>
<p class="qr-text">Scan to Open Digital Card</p>
</div>

<div class="footer">
Luxury NFC Identity Solutions for Modern Professionals <br>
<span class="footer-brand">Powered by Elite Cards Studio</span>
</div>

</div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>

<script>
// QR GENERATOR
new QRCode(document.getElementById("qrcode"), {
text: window.location.href,
width: 100,
height: 100,
colorDark : "#d4af37",
colorLight : "#000000",
correctLevel : QRCode.CorrectLevel.H
});

// SAVE CONTACT DOWNLOAD
document.getElementById("saveBtn").addEventListener("click", function(e){
e.preventDefault();
const link = document.createElement("a");
link.href = "Elite_Cards_Studio.vcf";
link.download = "Elite_Cards_Studio.vcf";
document.body.appendChild(link);
link.click();
document.body.removeChild(link);
});

// 3D TILT
const card=document.getElementById("tiltCard");
card.addEventListener("mousemove",(e)=>{
const r=card.getBoundingClientRect();
const x=e.clientX-r.left;
const y=e.clientY-r.top;
const centerX=r.width/2;
const centerY=r.height/2;
card.style.transform=`rotateX(${((y-centerY)/centerY)*6}deg) rotateY(${((x-centerX)/centerX)*-6}deg)`;
});
card.addEventListener("mouseleave",()=>card.style.transform="rotateX(0deg) rotateY(0deg)");
</script>

</body>
</html>
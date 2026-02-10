
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

/* GLASS CARD */
.card{
  width:100%;
  max-width:380px;
  padding:32px 24px;
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
  margin:0 auto 18px;
}

/* GOLD SHINE ELITE */
.brand{
  font-family:'Playfair Display',serif;
  font-size:32px;
  text-align:center;
  letter-spacing:3px;
  background:linear-gradient(
    90deg,
    #b8962e 0%,
    #f5d27a 40%,
    #ffffff 50%,
    #f5d27a 60%,
    #b8962e 100%
  );
  background-size:200% auto;
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  animation:shine 4s linear infinite;
}
@keyframes shine{
  to{background-position:200% center;}
}

.sub{
  text-align:center;
  font-size:12px;
  letter-spacing:4px;
  margin-bottom:6px;
  color:#f5d27a;
  opacity:.8;
}

/* RGB DOTS */
.rgb-dots{
  display:flex;
  justify-content:center;
  gap:8px;
  margin:8px 0 12px;
}
.dot{
  width:10px;
  height:10px;
  border-radius:50%;
  animation:rgbPulse 2.8s infinite ease-in-out;
}
.red{background:#ff3b30;box-shadow:0 0 8px #ff3b30;animation-delay:0s;}
.green{background:#34c759;box-shadow:0 0 8px #34c759;animation-delay:.4s;}
.blue{background:#007aff;box-shadow:0 0 8px #007aff;animation-delay:.8s;}

@keyframes rgbPulse{
  0%{transform:scale(1);opacity:1}
  50%{transform:scale(1.2);opacity:.6}
  100%{transform:scale(1);opacity:1}
}

/* NAME */
.name{
  text-align:center;
  font-size:20px;
  font-weight:600;
  color:#f5d27a;
  margin-top:6px;
}
.role{
  text-align:center;
  font-size:13px;
  opacity:.85;
  margin-bottom:20px;
  color:#f5d27a;
}

/* BUTTONS */
.btn{
  display:block;
  width:100%;
  padding:14px;
  margin:10px 0;
  text-align:center;
  border-radius:20px;
  text-decoration:none;
  font-weight:600;
  color:#000;
  background:linear-gradient(135deg,#f5d27a,#d4af37);
  transition:.3s;
}
.btn:hover{
  transform:translateZ(12px);
  box-shadow:0 0 25px rgba(245,210,122,.9);
}

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

.footer{
  text-align:center;
  font-size:11px;
  margin-top:20px;
  opacity:.7;
  color:#f5d27a;
}
</style>
</head>

<body>

<script>
for(let i=0;i<20;i++){
  let p=document.createElement("div");
  p.className="particle";
  p.style.left=Math.random()*100+"vw";
  p.style.animationDuration=(10+Math.random()*10)+"s";
  document.body.appendChild(p);
}
</script>

<div class="card" id="tiltCard">

  <img src="owner.jpg" class="profile" alt="Profile">

  <div class="brand">ELITE</div>
  <div class="sub">CARDS STUDIO</div>

  <div class="rgb-dots">
    <span class="dot red"></span>
    <span class="dot green"></span>
    <span class="dot blue"></span>
  </div>

  <div class="name">Muneeswaran R</div>
  <div class="role">CXO | Premium Visiting Card Designer</div>

  <a href="tel:+919655223394" class="btn">📞 Call</a>
  <a href="https://wa.me/919655223394" class="btn">💬 WhatsApp</a>

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
const card=document.getElementById("tiltCard");

/* MOUSE TILT */
card.addEventListener("mousemove",(e)=>{
  const r=card.getBoundingClientRect();
  const x=e.clientX-r.left;
  const y=e.clientY-r.top;
  const centerX=r.width/2;
  const centerY=r.height/2;
  card.style.transform=`rotateX(${((y-centerY)/centerY)*6}deg) rotateY(${((x-centerX)/centerX)*-6}deg)`;
});
card.addEventListener("mouseleave",()=>card.style.transform="rotateX(0deg) rotateY(0deg)");

/* TRUE GYROSCOPE */
if(window.DeviceOrientationEvent){
  window.addEventListener("deviceorientation",(e)=>{
    let x=e.beta/25;
    let y=e.gamma/25;
    card.style.transform=`rotateX(${x}deg) rotateY(${y}deg)`;
  });
}

/* AUTO VCF DOWNLOAD (SAFE) */
window.addEventListener("load",()=>{
  if(!localStorage.getItem("eliteDownloaded")){
    setTimeout(()=>{
      const link=document.createElement("a");
      link.href="Elite_Cards_Studio.vcf";
      link.download="Elite_Cards_Studio.vcf";
      document.body.appendChild(link);
      link.click();
      document.body.removeChild(link);
      localStorage.setItem("eliteDownloaded","true");
    },1500);
  }
});
</script>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Elite Cards Studio</title>

<style>
*{box-sizing:border-box;margin:0;padding:0}

body{
  font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Arial;
  background:radial-gradient(circle at top left,#1a1a1a,#000 70%);
  color:#f5d27a;
  min-height:100vh;
  display:flex;
  justify-content:center;
  align-items:center;
  perspective:1400px;
  overflow:hidden;
}

/* FLOATING PARTICLES */
.particle{
  position:absolute;
  width:4px;
  height:4px;
  background:#d4af37;
  border-radius:50%;
  opacity:.25;
  animation:float 14s linear infinite;
}
@keyframes float{
  from{transform:translateY(100vh)}
  to{transform:translateY(-10vh)}
}

/* CENTER */
.wrapper{
  width:100%;
  display:flex;
  justify-content:center;
  padding:20px;
}

/* CARD */
.card{
  width:100%;
  max-width:380px;
  border-radius:28px;
  padding:22px 18px 26px;
  backdrop-filter:blur(18px);
  background:rgba(255,255,255,0.06);
  border:1px solid rgba(212,175,55,.25);
  box-shadow:0 25px 60px rgba(0,0,0,.7);
  transform-style:preserve-3d;
  transition:transform .2s ease;
}

/* LOGO */
.logo{
  width:70px;
  margin:0 auto 10px;
  display:block;
}

/* PROFILE */
.profile{
  width:96px;
  height:96px;
  margin:10px auto 6px;
  border-radius:50%;
  border:3px solid #d4af37;
  object-fit:cover;
  display:block;
}

/* NFC */
.nfc-hint{
  display:flex;
  justify-content:center;
  gap:8px;
  font-size:13px;
  margin-bottom:10px;
  animation:nfcPulse 2.5s infinite;
}
@keyframes nfcPulse{
  0%{transform:scale(1)}
  50%{transform:scale(1.1);opacity:.6}
  100%{transform:scale(1)}
}

/* GOLD SHINE TEXT */
.brand{
  text-align:center;
  font-size:30px;
  font-weight:700;
  letter-spacing:2px;
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
}
.role{
  text-align:center;
  font-size:13px;
  opacity:.85;
  margin-bottom:16px;
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
  border-radius:18px;
  transition:.3s;
}
.btn:hover{
  transform:translateZ(12px);
  box-shadow:0 0 25px rgba(245,210,122,.9);
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
  opacity:.7;
}
</style>
</head>

<body>

<script>
for(let i=0;i<18;i++){
  let p=document.createElement("div");
  p.className="particle";
  p.style.left=Math.random()*100+"vw";
  p.style.animationDuration=(10+Math.random()*8)+"s";
  document.body.appendChild(p);
}
</script>

<div class="wrapper">
  <div class="card" id="tiltCard">

    <img src="elite_logoo.png" class="logo" alt="Elite Logo">
    <img src="owner.jpg" class="profile" alt="Profile">

    <div class="nfc-hint">Tap NFC Card</div>

    <div class="brand">ELITE</div>
    <div class="brand-sub">CARDS STUDIO</div>

    <div class="name">Muneeswaran R</div>
    <div class="role">CXO | Premium Visiting Card Designer</div>

    <a href="tel:+919655223394" class="btn">📞 Call Now</a>
    <a href="https://wa.me/919655223394" class="btn">💬 WhatsApp</a>

    <div class="grid">
      <a href="mailto:elitecardsstudio@gmail.com" class="btn small">📧 Email</a>
      <a href="Elite_Cards_Studio.vcf" download class="btn small">💾 Save</a>
      <a href="https://maps.google.com" class="btn small">📍 Location</a>
      <a href="upi://pay?pa=9655223394@upi&pn=Elite%20Cards%20Studio&cu=INR" class="btn small">💳 Pay</a>
    </div>

    <div class="footer">
      Luxury NFC Visiting Cards · Digital Business Cards
    </div>

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

/* GYROSCOPE TILT */
if(window.DeviceOrientationEvent){
  window.addEventListener("deviceorientation",(e)=>{
    let x=e.beta/25;
    let y=e.gamma/25;
    card.style.transform=`rotateX(${x}deg) rotateY(${y}deg)`;
  });
}

/* AUTO VCF DOWNLOAD */
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
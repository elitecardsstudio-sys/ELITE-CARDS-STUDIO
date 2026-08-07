<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Elite Cards Studio | Digital Identity</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Poppins',sans-serif;
scroll-behavior:smooth;
}

body{
background:#050505;
overflow-x:hidden;
color:#fff;
}

/* Animated Luxury Background */

body::before{
content:"";
position:fixed;
top:0;
left:0;
width:100%;
height:100%;
background:
radial-gradient(circle at 20% 20%,rgba(255,215,0,.15),transparent 20%),
radial-gradient(circle at 80% 10%,rgba(255,215,0,.08),transparent 18%),
radial-gradient(circle at 50% 90%,rgba(255,215,0,.10),transparent 25%);
animation:bgMove 18s linear infinite;
z-index:-2;
}

@keyframes bgMove{

0%{
transform:scale(1) rotate(0deg);
}

100%{
transform:scale(1.2) rotate(360deg);
}

}

/* Sparkles */

.sparkles{
position:fixed;
width:100%;
height:100%;
top:0;
left:0;
pointer-events:none;
background-image:
radial-gradient(#FFD700 1px,transparent 1px),
radial-gradient(#ffffff 1px,transparent 1px),
radial-gradient(#ffe9a8 2px,transparent 2px);

background-size:80px 80px,140px 140px,180px 180px;

opacity:.35;

animation:spark 25s linear infinite;

z-index:-1;

}

@keyframes spark{

from{

transform:translateY(0);

}

to{

transform:translateY(-500px);

}

}

.container{

max-width:460px;

margin:auto;

padding:20px;

}

/* Main Card */

.card{

margin-top:25px;

background:rgba(15,15,15,.75);

backdrop-filter:blur(18px);

border:1px solid rgba(255,215,0,.35);

border-radius:28px;

padding:28px 22px;

text-align:center;

box-shadow:

0 0 30px rgba(255,215,0,.18);

}

/* Logo */

.logo{

font-size:36px;

font-weight:800;

letter-spacing:3px;

background:linear-gradient(90deg,#FFD700,#FFF8DC,#C9A227,#FFD700);

-webkit-background-clip:text;

-webkit-text-fill-color:transparent;

}

.subtitle{

letter-spacing:5px;

font-size:13px;

margin-top:4px;

color:#FFD700;

}

/* Profile */

.profile-box{

width:160px;

height:160px;

margin:30px auto;

border-radius:50%;

padding:5px;

background:linear-gradient(45deg,#FFD700,#FFF,#C9A227,#FFD700);

animation:borderRotate 6s linear infinite;

position:relative;

}

.profile{

width:100%;

height:100%;

border-radius:50%;

object-fit:cover;

border:4px solid #000;

}

.profile-box::before{

content:"";

position:absolute;

inset:-12px;

border-radius:50%;

background:conic-gradient(transparent,#FFD700,transparent,#FFF);

filter:blur(14px);

z-index:-1;

animation:halo 3s linear infinite;

}

@keyframes borderRotate{

100%{

transform:rotate(360deg);

}

}

@keyframes halo{

100%{

transform:rotate(-360deg);

}

}

/* Name */

.name{

font-size:28px;

font-weight:700;

margin-top:10px;

}

.role{

font-size:15px;

color:#FFD700;

margin-top:6px;

margin-bottom:30px;

}

/* Buttons */

.btn{

display:block;

margin:12px 0;

padding:16px;

border-radius:18px;

text-decoration:none;

font-weight:700;

font-size:16px;

color:#111;

background:linear-gradient(135deg,#FFF8DC,#FFD700,#C9A227);

transition:.35s;

position:relative;

overflow:hidden;

box-shadow:0 0 18px rgba(255,215,0,.30);

}

.btn::before{

content:"";

position:absolute;

top:-100%;

left:-100%;

width:300%;

height:300%;

background:linear-gradient(120deg,

transparent,

rgba(255,255,255,.8),

transparent);

transform:rotate(25deg);

transition:.6s;

}

.btn:hover::before{

left:100%;

}

.btn:hover{

transform:translateY(-4px) scale(1.03);

box-shadow:

0 0 12px #FFD700,

0 0 35px #FFD700,

0 0 70px rgba(255,215,0,.5);

}

/* Grid */

.grid{

display:grid;

grid-template-columns:1fr 1fr;

gap:12px;

margin-top:10px;

}

.small{

font-size:14px;

padding:14px;

}

.section-title{

font-size:22px;

margin:35px 0 20px;

font-weight:700;

color:#FFD700;

text-align:center;

}

</style>
</head>

<body>

<div class="sparkles"></div>

<div class="container">

<div class="card">

<div class="logo">ELITE</div>

<div class="subtitle">CARDS STUDIO</div>

<div class="profile-box">

<img src="owner.jpg" class="profile" alt="Owner Photo">

</div>

<div class="name">MUNEESWARAN R</div>

<div class="role">Digital Designer | Founder</div>

<a class="btn" href="tel:+919655223394">📞 Call Now</a>

<a class="btn" href="https://wa.me/919655223394?text=Hello%20Elite%20Cards%20Studio">💬 WhatsApp</a>

<div class="grid">

<a class="btn small" href="mailto:elitecardsstudio@gmail.com">📧 Email</a>

<a class="btn small" href="https://maps.app.goo.gl/UYX1TGwYeXoGQxQH9?g_st=ac">📍 Location</a>

<a class="btn small" href="#">💳 Payment</a>

<a class="btn small" href="elitecards.vcf" download>💾 Save Contact</a>

</div>
<!-- ========================= -->
<!-- SERVICES -->
<!-- ========================= -->

<div class="section-title">✨ Our Services</div>

<div class="grid">

<a class="btn small" href="#">
💼 Visiting Cards
</a>

<a class="btn small" href="#">
🎨 Logo Design
</a>

<a class="btn small" href="#">
🖨 Letter Head
</a>

<a class="btn small" href="#">
📦 Product Labels
</a>

<a class="btn small" href="#">
📢 Flex Banner
</a>

<a class="btn small" href="#">
💍 Wedding Cards
</a>

<a class="btn small" href="#">
🆔 ID Cards
</a>

<a class="btn small" href="#">
📱 Digital Cards
</a>

</div>

<!-- ========================= -->
<!-- SAMPLE DESIGNS -->
<!-- ========================= -->

<div class="section-title">
🎨 Sample Designs
</div>

<div style="display:grid;
grid-template-columns:1fr 1fr;
gap:12px;">

<img src="sample1.jpg"
style="width:100%;
border-radius:16px;
border:2px solid gold;
box-shadow:0 0 20px rgba(255,215,0,.25);">

<img src="sample2.jpg"
style="width:100%;
border-radius:16px;
border:2px solid gold;
box-shadow:0 0 20px rgba(255,215,0,.25);">

<img src="sample3.jpg"
style="width:100%;
border-radius:16px;
border:2px solid gold;
box-shadow:0 0 20px rgba(255,215,0,.25);">

<img src="sample4.jpg"
style="width:100%;
border-radius:16px;
border:2px solid gold;
box-shadow:0 0 20px rgba(255,215,0,.25);">

</div>

<br>

<a class="btn"
href="https://your-gallery-link.com">

🖼 View Complete Portfolio

</a>

<!-- ========================= -->
<!-- DESIGN UPLOAD -->
<!-- ========================= -->

<div class="section-title">

📤 Design Upload

</div>

<form>

<input type="text"
placeholder="Your Name"

style="width:100%;
padding:15px;
margin-bottom:12px;
border-radius:12px;
border:none;
font-size:15px;">

<input type="tel"
placeholder="Mobile Number"

style="width:100%;
padding:15px;
margin-bottom:12px;
border-radius:12px;
border:none;
font-size:15px;">

<input type="file"

style="width:100%;
padding:15px;
margin-bottom:12px;
background:white;
border-radius:12px;">

<textarea
placeholder="Design Instructions"

style="width:100%;
height:120px;
padding:15px;
border-radius:12px;
border:none;
margin-bottom:15px;
font-size:15px;"></textarea>

<button class="btn"
type="submit">

📤 Submit Design

</button>

</form>

<!-- ========================= -->
<!-- ONLINE PAYMENT -->
<!-- ========================= -->

<div class="section-title">

💳 Online Payment

</div>

<a class="btn"
href="upi://pay?pa=YOURUPI@upi&pn=Elite%20Cards%20Studio&cu=INR">

💰 Pay Using UPI

</a>

<img src="upi-qr.png"

style="width:220px;
display:block;
margin:auto;
border-radius:18px;
border:3px solid gold;
box-shadow:0 0 25px rgba(255,215,0,.4);">

<br>

<!-- ========================= -->
<!-- GOOGLE REVIEW -->
<!-- ========================= -->

<a class="btn"

href="https://g.page/r/REPLACE_REVIEW_LINK">

⭐⭐⭐⭐⭐

Leave Google Review

</a>

<a class="btn"

href="#">

📲 Share Digital Card

</a>
<!-- ========================= -->
<!-- FLOATING BUTTONS -->
<!-- ========================= -->

<a href="https://wa.me/919655223394"
class="float-whatsapp">
💬
</a>

<a href="tel:+919655223394"
class="float-call">
📞
</a>

<style>

.float-whatsapp,
.float-call{

position:fixed;

right:18px;

width:60px;

height:60px;

border-radius:50%;

display:flex;

justify-content:center;

align-items:center;

font-size:30px;

text-decoration:none;

color:#fff;

z-index:9999;

box-shadow:0 0 25px rgba(255,215,0,.45);

animation:pulse 2s infinite;

}

.float-whatsapp{

bottom:90px;

background:#25D366;

}

.float-call{

bottom:18px;

background:#FFD700;

color:#000;

}

@keyframes pulse{

0%{

transform:scale(1);

}

50%{

transform:scale(1.08);

}

100%{

transform:scale(1);

}

}

.footer{

margin-top:40px;

padding:25px 10px;

text-align:center;

border-top:1px solid rgba(255,215,0,.25);

color:#FFD700;

font-size:14px;

line-height:28px;

}

.footer h3{

font-size:24px;

margin-bottom:8px;

letter-spacing:2px;

}

</style>

<div class="footer">

<h3>ELITE CARDS STUDIO</h3>

Creative Design • Premium Printing • Digital Identity

<br><br>

© 2026 Elite Cards Studio

</div>

</div>

</div>

<script>

/* ===========================
GLITTER EFFECT
=========================== */

document.querySelectorAll(".btn").forEach(button=>{

button.addEventListener("click",function(e){

for(let i=0;i<35;i++){

const sparkle=document.createElement("span");

sparkle.innerHTML=["✨","⭐","💛"][Math.floor(Math.random()*3)];

sparkle.style.position="fixed";

sparkle.style.left=e.clientX+"px";

sparkle.style.top=e.clientY+"px";

sparkle.style.fontSize=(12+Math.random()*20)+"px";

sparkle.style.pointerEvents="none";

sparkle.style.transition="all 1s ease";

sparkle.style.zIndex="99999";

document.body.appendChild(sparkle);

setTimeout(()=>{

sparkle.style.transform=

`translate(${(Math.random()-0.5)*280}px,

${(Math.random()-0.5)*280}px)

rotate(720deg)

scale(0)`;

sparkle.style.opacity="0";

},20);

setTimeout(()=>{

sparkle.remove();

},1000);

}

});

});

/* ===========================
MOUSE GLOW
=========================== */

const glow=document.createElement("div");

glow.style.position="fixed";

glow.style.width="20px";

glow.style.height="20px";

glow.style.borderRadius="50%";

glow.style.background="gold";

glow.style.filter="blur(18px)";

glow.style.pointerEvents="none";

glow.style.zIndex="99999";

document.body.appendChild(glow);

document.addEventListener("mousemove",e=>{

glow.style.left=(e.clientX-10)+"px";

glow.style.top=(e.clientY-10)+"px";

});

/* ===========================
BUTTON SHIMMER
=========================== */

setInterval(()=>{

document.querySelectorAll(".btn").forEach(btn=>{

btn.animate([

{

boxShadow:"0 0 10px gold"

},

{

boxShadow:"0 0 45px white"

},

{

boxShadow:"0 0 10px gold"

}

],{

duration:1500

});

});

},2500);

</script>

</body>

</html>
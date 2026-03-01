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

*{
margin:0;
padding:0;
box-sizing:border-box
}

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


/* PARTICLES */

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

@keyframes shine{

to{background-position:200% center;}

}


.sub{

text-align:center;

font-size:12px;

letter-spacing:4px;

margin-bottom:2px;

color:#f5d27a;

opacity:.8;

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


/* BUTTON GRID */

.grid{

display:grid;

grid-template-columns:1fr 1fr;

gap:10px;

}


/* LUXURY BUTTON */

.btn{

display:flex;

align-items:center;

justify-content:center;

padding:13px;

border-radius:16px;

text-decoration:none;

font-weight:600;

font-size:14px;

color:#f5d27a;

background:rgba(255,255,255,0.05);

border:1px solid rgba(212,175,55,0.5);

backdrop-filter:blur(10px);

box-shadow:

0 0 10px rgba(212,175,55,0.2),

inset 0 0 8px rgba(212,175,55,0.1);

transition:all .3s ease;

}


/* HOVER */

.btn:hover{

color:#000;

background:linear-gradient(135deg,#f5d27a,#d4af37);

box-shadow:

0 0 20px rgba(212,175,55,0.8),

0 0 40px rgba(212,175,55,0.4);

transform:translateY(-3px) scale(1.03);

}


/* CLICK */

.btn:active{

transform:scale(.95);

}


/* FOOTER */

.footer{

text-align:center;

font-size:11px;

margin-top:14px;

color:#f5d27a;

}

</style>

</head>

<body>



<script>

/* PARTICLES */

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


<div class="name">Muneeswaran R</div>

<div class="role">CXO | Creative Director</div>



<div class="grid">


<a href="tel:+919655223394" class="btn">📞 Call</a>

<a href="https://wa.me/919655223394" class="btn">💬 WhatsApp</a>


<a href="#" class="btn" id="saveBtn">💾 Save</a>

<a href="mailto:elitecardsstudio@gmail.com" class="btn">📧 Email</a>


<a href="https://www.google.com/maps/search/?api=1&query=Elite+Cards+Studio" class="btn">📍 Location</a>

<a href="upi://pay?pa=9655223394@jupiteraxis&pn=Muneeswaran&cu=INR" class="btn">💳 UPI</a>


<a href="sample-design.html" class="btn">🎨 Designs</a>
<img src="images/design1.jpg">
<a href="https://yourwebsite.com" class="btn">🌐 Website</a>


</div>



<div class="footer">

“Crafting Premium Identity for Modern Professionals”

</div>


</div>



<script>


/* DOWNLOAD FUNCTION */

function downloadContact(){

if(window.saved) return;

window.saved=true;

const link=document.createElement("a");

link.href="Elite_Cards_Studio.vcf";

link.download="Elite_Cards_Studio.vcf";

document.body.appendChild(link);

link.click();

document.body.removeChild(link);

}


/* AUTO DOWNLOAD */

window.onload=function(){

setTimeout(downloadContact,1000);

}


/* SAVE BUTTON */

document.getElementById("saveBtn").onclick=function(e){

e.preventDefault();

downloadContact();

}


/* 3D TILT */

const card=document.getElementById("tiltCard");

card.onmousemove=function(e){

const r=card.getBoundingClientRect();

const x=e.clientX-r.left;

const y=e.clientY-r.top;

const cx=r.width/2;

const cy=r.height/2;

card.style.transform=

`rotateX(${((y-cy)/cy)*6}deg)

 rotateY(${((x-cx)/cx)*-6}deg)`;

}


card.onmouseleave=function(){

card.style.transform="rotateX(0) rotateY(0)";

}


</script>


</body>

</html>

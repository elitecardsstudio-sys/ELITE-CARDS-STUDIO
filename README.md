
<html lang="en">
<head>

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

overflow:hidden;

}


/* GOLD PARTICLES */

.particle{

position:absolute;
width:5px;
height:5px;
background:#d4af37;
border-radius:50%;
opacity:.3;
animation:float linear infinite;

}

@keyframes float{

from{transform:translateY(100vh);}
to{transform:translateY(-10vh);}

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

}


/* PROFILE */

.profile{

width:95px;
height:95px;
border-radius:50%;
border:3px solid #d4af37;
display:block;
margin:0 auto 12px;

}


/* BRAND */

.brand{

font-family:'Playfair Display',serif;
font-size:32px;
text-align:center;
color:#f5d27a;

}

.sub{

text-align:center;
font-size:12px;
color:#f5d27a;

}

.name{

text-align:center;
font-size:20px;
color:#f5d27a;

}


/* TRUE RGB DOTS */

.rgbDots{

display:flex;
justify-content:center;
gap:10px;
margin:6px 0;

}

.rgbDots span{

width:10px;
height:10px;
border-radius:50%;

animation:pulse 2s infinite alternate;

}

/* RED */

.rgbDots span:nth-child(1){

background:#ff0000;

box-shadow:
0 0 10px #ff0000,
0 0 20px #ff0000,
0 0 30px #ff0000;

}

/* GREEN */

.rgbDots span:nth-child(2){

background:#00ff00;

box-shadow:
0 0 10px #00ff00,
0 0 20px #00ff00,
0 0 30px #00ff00;

animation-delay:.4s;

}

/* TRUE BLUE */

.rgbDots span:nth-child(3){

background:#0080ff;

box-shadow:
0 0 10px #0080ff,
0 0 20px #0080ff,
0 0 30px #0080ff;

animation-delay:.8s;

}


@keyframes pulse{

from{

transform:scale(1);

opacity:.7;

}

to{

transform:scale(1.6);

opacity:1;

}

}


/* ROLE */

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


/* GLOW BUTTON */

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

transition:.25s;

}

.btn:active{

color:#000;

background:linear-gradient(135deg,#f5d27a,#d4af37);

box-shadow:
0 0 20px gold,
0 0 40px gold;

transform:scale(.95);

}


/* FOOTER */

.footer{

text-align:center;
font-size:11px;
margin-top:14px;
color:#f5d27a;

}


/* POPUP */

.designPopup{

position:fixed;
top:0;
left:0;

width:100%;
height:100%;

background:rgba(0,0,0,.95);

display:none;

align-items:center;
justify-content:center;
flex-direction:column;

z-index:999;

}

.designGallery{

display:grid;
grid-template-columns:repeat(2,1fr);
gap:15px;

}

.designGallery img{

width:150px;
border:2px solid gold;
border-radius:10px;

}

.closeBtn{

position:absolute;
top:20px;
right:20px;
font-size:30px;
color:white;
cursor:pointer;

}

</style>

</head>

<body>



<!-- PARTICLES -->

<script>

for(let i=0;i<20;i++){

let p=document.createElement("div");

p.className="particle";

p.style.left=Math.random()*100+"vw";

p.style.animationDuration=(10+Math.random()*10)+"s";

document.body.appendChild(p);

}

</script>



<div class="card">

<img src="owner.jpg" class="profile">

<div class="brand">ELITE</div>

<div class="sub">CARDS STUDIO</div>

<div class="name">Muneeswaran R</div>


<div class="rgbDots">

<span></span>
<span></span>
<span></span>

</div>


<div class="role">CXO | Creative Director</div>


<div class="grid">

<a href="tel:+919655223394" class="btn">📞 Call</a>

<a href="https://wa.me/919655223394" class="btn">💬 WhatsApp</a>

<a href="#" onclick="downloadContact()" class="btn">💾 Save</a>

<a href="mailto:elitecardsstudio@gmail.com" class="btn">📧 Email</a>

<a href="https://maps.google.com/?q=Elite+Cards+Studio" class="btn">📍 Location</a>

<a href="upi://pay?pa=9655223394@axisbank&pn=Muneeswaran&cu=INR" class="btn">💳 UPI</a>

<a href="#" onclick="openDesign()" class="btn">🎨 Designs</a>

<a href="https://yourwebsite.com" class="btn">🌐 Website</a>

</div>


<div class="footer">

Crafting Premium Identity for Modern Professionals

</div>

</div>



<!-- POPUP -->

<div class="designPopup" id="designPopup">

<span class="closeBtn" onclick="closeDesign()">✖</span>

<div class="designGallery">

<img src="design1.jpg">
<img src="design2.jpg">
<img src="design3.jpg">
<img src="design4.jpg">
<img src="design5.jpg">

</div>

</div>



<script>


/* CONTACT DOWNLOAD */

function downloadContact(){

const link=document.createElement("a");

link.href="Elite_Cards_Studio.vcf";

link.download="Elite_Cards_Studio.vcf";

link.click();

}


/* AUTO DOWNLOAD */

window.onload=function(){

setTimeout(downloadContact,1500);

}


/* POPUP */

function openDesign(){

document.getElementById("designPopup").style.display="flex";

}

function closeDesign(){

document.getElementById("designPopup").style.display="none";

}

</script>


</body>
</html>
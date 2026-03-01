
<html lang="en">

<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Elite Cards Studio</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Poppins:wght@400;500;600&display=swap" rel="stylesheet">

<style>

/* YOUR ORIGINAL STYLE — unchanged */

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
object-fit:cover;
display:block;
margin:0 auto 12px;

}

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
font-weight:600;
color:#f5d27a;

}

.role{

text-align:center;
font-size:13px;
margin-bottom:12px;
color:#f5d27a;

}

.grid{

display:grid;
grid-template-columns:1fr 1fr;
gap:10px;

}

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

}

.footer{

text-align:center;
font-size:11px;
margin-top:14px;
color:#f5d27a;

}


/* ✅ POPUP CSS ONLY ADDED */

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



<div class="card">

<img src="owner.jpg" class="profile">

<div class="brand">ELITE</div>

<div class="sub">CARDS STUDIO</div>

<div class="name">Muneeswaran R</div>

<div class="role">CXO | Creative Director</div>


<div class="grid">

<a href="tel:+919655223394" class="btn">📞 Call</a>

<a href="https://wa.me/919655223394" class="btn">💬 WhatsApp</a>

<a href="#" onclick="downloadContact()" class="btn">💾 Save</a>

<a href="mailto:elitecardsstudio@gmail.com" class="btn">📧 Email</a>

<a href="#" onclick="openDesign()" class="btn">🎨 Designs</a>

<a href="https://yourwebsite.com" class="btn">🌐 Website</a>

</div>


<div class="footer">

Crafting Premium Identity for Modern Professionals

</div>

</div>



<!-- ✅ POPUP OUTSIDE CARD -->

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

/* popup */

function openDesign(){

document.getElementById("designPopup").style.display="flex";

}

function closeDesign(){

document.getElementById("designPopup").style.display="none";

}


/* save contact */

function downloadContact(){

const link=document.createElement("a");

link.href="Elite_Cards_Studio.vcf";

link.download="Elite_Cards_Studio.vcf";

link.click();

}

</script>


</body>
</html>
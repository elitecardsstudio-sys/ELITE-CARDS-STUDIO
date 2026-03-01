
<html lang="en">
<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Elite Cards Studio</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
}

body{
font-family:Poppins;
background:#000;
display:flex;
justify-content:center;
align-items:center;
min-height:100vh;
}

/* CARD */

.card{

width:360px;
padding:20px;
border-radius:20px;
background:#111;
border:1px solid gold;
text-align:center;
color:gold;

}

.profile{

width:90px;
height:90px;
border-radius:50%;
border:3px solid gold;
margin-bottom:10px;

}

.grid{

display:grid;
grid-template-columns:1fr 1fr;
gap:10px;
margin-top:15px;

}

.btn{

padding:12px;
border-radius:10px;
border:1px solid gold;
color:gold;
text-decoration:none;
display:block;

}

.footer{

margin-top:15px;
font-size:12px;

}


/* ✅ DESIGN POPUP CSS */

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
gap:10px;

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

<h2>ELITE</h2>

<p>Muneeswaran R</p>

<div class="grid">

<a href="#" class="btn">Call</a>

<a href="#" class="btn">WhatsApp</a>

<a href="#" class="btn">Save</a>

<a href="#" class="btn">Email</a>

<a href="#" onclick="openDesign()" class="btn">🎨 Designs</a>

<a href="#" class="btn">Website</a>

</div>

<div class="footer">

Crafting Premium Identity

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

function openDesign(){

document.getElementById("designPopup").style.display="flex";

}

function closeDesign(){

document.getElementById("designPopup").style.display="none";

}

</script>


</body>
</html>
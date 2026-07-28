<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Elite Cards Studio</title>

<style>
body{
    margin:0;
    background:#000;
    display:flex;
    justify-content:center;
    align-items:center;
    min-height:100vh;
    font-family:Arial,sans-serif;
}
.card{
    width:360px;
    background:#171717;
    border:1px solid #c8a64a;
    border-radius:30px;
    padding:25px;
    text-align:center;
    color:#e7c86d;
}
.profile{
    width:110px;
    height:110px;
    border-radius:50%;
    border:4px solid #d4af37;
    object-fit:cover;
}
.brand{
    font-size:52px;
    font-weight:bold;
    margin-top:15px;
}
.sub{
    font-size:22px;
    margin-bottom:15px;
}
.name{
    font-size:24px;
}
.role{
    margin:15px 0;
}
.grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:12px;
}
.btn{
    padding:15px;
    border:1px solid #c8a64a;
    border-radius:15px;
    color:#e7c86d;
    text-decoration:none;
    display:block;
}
.order{
    margin-top:18px;
    background:#d4af37;
    color:#000;
    padding:16px;
    border-radius:15px;
    text-decoration:none;
    display:block;
    font-weight:bold;
}
</style>
</head>

<body>

<div class="card">

<img src="owner.png" class="profile">

<div class="brand">ELITE</div>
<div class="sub">CARDS STUDIO</div>

<div class="name">Muneeswaran R</div>
<div class="role">CXO | Creative Director</div>

<div class="grid">
<a href="tel:+919655223394" class="btn">📞 Call</a>
<a href="https://wa.me/919655223394" class="btn">💬 WhatsApp</a>
<a href="Elite_Cards_Studio.vcf" class="btn">💾 Save</a>
<a href="mailto:elitecardsstudio@gmail.com" class="btn">📧 Email</a>
<a href="https://maps.google.com/?q=Elite+Cards+Studio" class="btn">📍 Location</a>
<a href="upi://pay?pa=9655223394@axisbank&pn=Muneeswaran&cu=INR" class="btn">💳 UPI</a>
<a href="#" class="btn">🎨 Designs</a>
</div>

<a href="#" class="order">✍️ Order Here</a>

</div>

</body>
</html>
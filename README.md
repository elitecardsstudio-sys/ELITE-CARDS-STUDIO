<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Elite Cards Studio</title>

<style>
body{
  margin:0;
  font-family:"Poppins",Arial,sans-serif;
  background:#0a0a0a;
  color:#d4af37;
}

.container{
  max-width:420px;
  margin:auto;
  padding:18px;
}

/* Card */
.card{
  background:linear-gradient(145deg,#111,#000);
  border-radius:22px;
  padding:24px;
  border:1px solid #2a2200;
  box-shadow:0 0 30px rgba(212,175,55,0.25);
}

/* Logo */
.logo{
  width:90px;
  display:block;
  margin:auto;
}

/* Owner Photo */
.owner{
  width:120px;
  height:120px;
  border-radius:50%;
  border:3px solid #d4af37;
  margin:16px auto;
  display:block;
  object-fit:cover;
}

h2{
  text-align:center;
  margin:10px 0 4px;
}

.role{
  text-align:center;
  color:#c9b15f;
  font-weight:600;
}

.brand{
  text-align:center;
  font-size:14px;
  color:#aaa;
  margin-bottom:18px;
}

/* Buttons */
.btn{
  display:block;
  text-align:center;
  padding:13px;
  margin:10px 0;
  border-radius:14px;
  text-decoration:none;
  font-weight:600;
  letter-spacing:.5px;
}

.call{ background:#d4af37; color:#000; }
.whatsapp{ background:#128c7e; color:#fff; }
.map{
  background:#0f0f0f;
  border:1px solid #d4af37;
  color:#d4af37;
}

/* Services */
.services{
  margin-top:20px;
  background:#0f0f0f;
  padding:18px;
  border-radius:18px;
  border:1px solid #2a2200;
}

.services ul{
  padding-left:18px;
  margin:0;
}

.services li{
  margin:8px 0;
}

/* Enquiry */
.form{
  margin-top:20px;
  background:#0f0f0f;
  padding:18px;
  border-radius:18px;
  border:1px solid #2a2200;
}

input, textarea{
  width:100%;
  margin-top:10px;
  padding:12px;
  background:#000;
  border:1px solid #333;
  border-radius:12px;
  color:#fff;
}

button{
  width:100%;
  margin-top:15px;
  padding:13px;
  background:#d4af37;
  color:#000;
  border:none;
  border-radius:14px;
  font-size:16px;
  font-weight:bold;
}

/* Footer */
.footer{
  text-align:center;
  font-size:12px;
  margin-top:16px;
  color:#777;
}
</style>
</head>

<body>
<div class="container">

<div class="card">

  <!-- Logo -->
  <img src="elite_logo.png" class="logo" alt="Elite Cards Studio">

  <!-- Owner -->
  <img src="owner.jpg" class="owner" alt="Founder">

  <h2>Elite Cards Studio</h2>
  <div class="role">Luxury NFC & Digital Card Agency</div>
  <div class="brand">Premium Business Cards</div>

  <a href="tel:+919655223394" class="btn call">📞 Call Us</a>

  <a href="https://wa.me/919655223394?text=Hello%20Elite%20Cards%20Studio,%20I%20need%20a%20luxury%20digital%20card"
     class="btn whatsapp">💬 WhatsApp Enquiry</a>

  <a href="https://www.google.com/maps?q=Elite+Cards+Studio"
     target="_blank" class="btn map">📍 Studio Location</a>

  <!-- Services -->
  <div class="services">
    <h3>Our Services</h3>
    <ul>
      <li>Luxury NFC Visiting Cards</li>
      <li>Digital Business Cards</li>
      <li>Doctor & Business Branding</li>
      <li>QR Code & Smart Profiles</li>
      <li>Corporate Bulk Business Cards</li>
      <li>Letterheads</li>
    </ul>
  </div>

  <!-- Enquiry Form -->
  <div class="form">
    <h3>Quick Enquiry</h3>
    <input type="text" id="name" placeholder="Your Name" required>
    <input type="tel" id="phone" placeholder="Mobile Number" required>
    <textarea id="message" placeholder="Your Requirement"></textarea>
    <button onclick="sendWhatsApp()">Send Enquiry</button>
  </div>

</div>

<div class="footer">
  © Elite Cards Studio • Luxury Digital Identity
</div>

</div>

<script>
function sendWhatsApp(){
  var name = document.getElementById("name").value;
  var phone = document.getElementById("phone").value;
  var message = document.getElementById("message").value;

  if(name==="" || phone===""){
    alert("Please fill required fields");
    return;
  }

  var text =
    "Hello Elite Cards Studio,%0A%0A" +
    "👤 Name: " + name + "%0A" +
    "📞 Mobile: " + phone + "%0A" +
    "📌 Requirement: " + message;

  window.open(
    "https://wa.me/919655223394?text=" + text,
    "_blank"
  );
}
</script>

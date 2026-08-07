
<html lang="en">
<head>

<style>
header{
    display:none !important;
}
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Elite Cards Studio</title>

<style>
*{box-sizing:border-box}

body{
  margin:0;
  font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Arial;
  background:#000;
  color:#f5d27a;
}

/* CENTER */
.wrapper{
  min-height:100vh;
  display:flex;
  justify-content:center;
  padding:16px 10px 40px;
}

/* CARD */
.card{
  width:100%;
  max-width:380px;
  background:#000;
  border-radius:28px;
  padding:20px 16px 22px;
  border:1.5px solid #d4af37;
  position:relative;
  overflow:hidden;
}

.card-content{
  position:relative;
  z-index:2;
}
.glitter-layer{
  position:absolute;
  inset:0;
  pointer-events:none;
  z-index:1;
}

.spark{
  position:absolute;
  bottom:-10px;
  border-radius:50%;
  background:radial-gradient(circle,#fff8e1 0%,#f5d27a 45%,rgba(212,175,55,0) 75%);
  opacity:0;
  animation-name:sparkRise;
  animation-timing-function:ease-in;
  animation-iteration-count:infinite;
}

@keyframes sparkRise{
  0%{
    transform:translateY(0) translateX(0) scale(.4);
    opacity:0;
  }
  15%{
    opacity:1;
  }
  50%{
    opacity:.9;
  }
  100%{
    transform:translateY(var(--rise)) translateX(var(--drift)) scale(1);
    opacity:0;
  }
}

/* PROFILE */
.profile{
  width:96px;
  height:96px;
  margin:10px auto 6px;
  display:block;
  border-radius:50%;
  border:3px solid #d4af37;
  object-fit:cover;
}

/* BRAND */
.brand{
  text-align:center;
  font-size:28px;
  font-weight:700;
  letter-spacing:2px;
  margin-top:6px;
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
  margin-top:6px;
}

.role{
  text-align:center;
  font-size:13px;
  opacity:.85;
  margin-bottom:16px;
}

/* TOUCH FLASH */
@keyframes touchFlash{
  0%{box-shadow:0 0 0 rgba(212,175,55,0)}
  40%{box-shadow:0 0 18px rgba(245,210,122,.95)}
  100%{box-shadow:0 0 0 rgba(212,175,55,0)}
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
  border-radius:14px;
  transition:transform .15s ease;
}

.btn:active{
  transform:scale(.97);
  animation:touchFlash .5s ease;
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
  margin:0;
}

/* FOOTER */
.footer{
  margin-top:16px;
  font-size:11px;
  text-align:center;
  line-height:1.6;
  opacity:.8;
}

/* SAMPLE DESIGNS MODAL */
.modal-overlay{
  display:none;
  position:fixed;
  inset:0;
  background:rgba(0,0,0,.85);
  z-index:100;
  padding:20px 12px;
  overflow-y:auto;
}

.modal-overlay.open{
  display:block;
}

.modal-box{
  max-width:400px;
  margin:0 auto;
  background:#000;
  border:1.5px solid #d4af37;
  border-radius:20px;
  padding:16px;
}

.modal-header{
  display:flex;
  justify-content:space-between;
  align-items:center;
  margin-bottom:12px;
}

.modal-title{
  font-size:17px;
  font-weight:700;
  color:#f5d27a;
}

.modal-close{
  background:none;
  border:1px solid #d4af37;
  color:#f5d27a;
  border-radius:8px;
  width:30px;
  height:30px;
  font-size:16px;
  cursor:pointer;
}

.sample-grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:10px;
}

.sample-grid img{
  width:100%;
  aspect-ratio:1/1;
  object-fit:cover;
  border-radius:10px;
  border:1px solid #d4af37;
}
</style>
</head>

<body>

<div class="wrapper">
  <div class="card">

    <div class="glitter-layer" id="glitterLayer"></div>

    <div class="card-content">

    <!-- PROFILE -->
    <img src="owner.png" class="profile" alt="Profile Photo">

    <!-- BRAND -->
    <div class="brand">ELITE</div>
    <div class="brand-sub">CARDS STUDIO</div>

    <!-- NAME -->
    <div class="name">Muneeswaran R</div>
    <div class="role">  Premium Visiting Card Designer</div>

    <!-- MAIN BUTTONS -->
    <a href="tel:+919655223394" class="btn">📞 Call Now</a>
    <a href="https://wa.me/919655223394" class="btn">💬 WhatsApp</a>

    <!-- GRID BUTTONS -->
    <div class="grid">
      <a href="mailto:elitecardsstudio@gmail.com" class="btn small">📧 Email</a>
      <a href="#" class="btn small" onclick="downloadContact();return false;">💾 Save Contact</a>
      <a href="https://maps.google.com" class="btn small">📍 Location</a>
      <a href="upi://pay?pa=9655223394@upi&pn=Elite%20Cards%20Studio&cu=INR" class="btn small">💳 Pay</a>
    </div>

    <!-- EXTRA -->
    <a href="#" class="btn">⭐ Google Review</a>
    <a href="#" class="btn" onclick="openSamples();return false;">🎨 Sample Designs</a>

    <!-- FOOTER -->
    <div class="footer">
      Luxury NFC Visiting Cards · Digital Business Cards · Corporate Bulk Business Cards<br>
      Letterheads · QR Code & Smart Profiles
    </div>

    </div>

  </div>
</div>

<!-- SAMPLE DESIGNS MODAL -->
<div class="modal-overlay" id="samplesModal">
  <div class="modal-box">
    <div class="modal-header">
      <div class="modal-title">Sample Designs</div>
      <button class="modal-close" onclick="closeSamples()">✕</button>
    </div>
    <div class="sample-grid">
      <img src="sample1.jpg" alt="Sample Design 1">
      <img src="sample2.jpg" alt="Sample Design 2">
      <img src="sample3.jpg" alt="Sample Design 3">
      <img src="sample4.jpg" alt="Sample Design 4">
    </div>
  </div>
</div>

<!-- AUTO DOWNLOAD CONTACT -->
<script>
function downloadContact(){
  const vcard =
    "BEGIN:VCARD\n" +
    "VERSION:3.0\n" +
    "N:R;Muneeswaran;;;\n" +
    "FN:Muneeswaran R\n" +
    "ORG:Elite Cards Studio\n" +
    "TITLE: Premium Visiting Card Designer\n" +
    "TEL;TYPE=CELL:+919655223394\n" +
    "EMAIL:elitecardsstudio@gmail.com\n" +
    "END:VCARD";

  const blob = new Blob([vcard], { type: "text/vcard" });
  const url = URL.createObjectURL(blob);
  const link = document.createElement("a");
  link.href = url;
  link.download = "Elite_Cards_Studio.vcf";
  document.body.appendChild(link);
  link.click();
  document.body.removeChild(link);
  URL.revokeObjectURL(url);
}

// Auto-trigger contact download shortly after the page loads
window.addEventListener("load", () => {
  setTimeout(downloadContact, 1500);
});

function openSamples(){
  document.getElementById("samplesModal").classList.add("open");
}
function closeSamples(){
  document.getElementById("samplesModal").classList.remove("open");
}

// GLITTER PARTICLES rising from the bottom of the card
function createGlitter(){
  const layer = document.getElementById("glitterLayer");
  const cardHeight = layer.parentElement.offsetHeight;
  const count = 22;

  for(let i = 0; i < count; i++){
    const spark = document.createElement("div");
    spark.className = "spark";

    const size = 2 + Math.random() * 3;
    const left = Math.random() * 100;
    const rise = cardHeight * (0.5 + Math.random() * 0.55);
    const drift = (Math.random() * 40) - 20;
    const duration = 3 + Math.random() * 3.5;
    const delay = Math.random() * 6;

    spark.style.width = size + "px";
    spark.style.height = size + "px";
    spark.style.left = left + "%";
    spark.style.setProperty("--rise", -rise + "px");
    spark.style.setProperty("--drift", drift + "px");
    spark.style.animationDuration = duration + "s";
    spark.style.animationDelay = delay + "s";

    layer.appendChild(spark);
  }
}

window.addEventListener("load", createGlitter);
</script>

</body>
</html>
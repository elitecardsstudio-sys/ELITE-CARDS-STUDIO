<html lang="en" style="scroll-behavior:smooth;">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Elite Cards Studio</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Poppins:wght@400;500;600&family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600;9..144,700&family=Space+Grotesk:wght@400;500;600;700&family=IBM+Plex+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
*{margin:0;padding:0;box-sizing:border-box;}
body{min-height:100vh;}

/* =========================================================
   SECTION 1 -- PROFILE / DIGITAL CARD
========================================================= */
.profile-hero{
  position:relative;
  min-height:100vh;
  background:radial-gradient(circle at top left,#1a1a1a,#000 70%);
  display:flex;align-items:center;justify-content:center;
  padding:50px 20px;overflow:hidden;
  font-family:'Poppins',sans-serif;
}

/* GOLD PARTICLES */
.particle{
  position:absolute;width:5px;height:5px;background:#d4af37;
  border-radius:50%;opacity:.3;animation:float linear infinite;
}
@keyframes float{ from{transform:translateY(100vh);} to{transform:translateY(-10vh);} }

/* CARD */
.card{
  width:100%;max-width:360px;padding:26px 20px;border-radius:28px;
  backdrop-filter:blur(20px);background:rgba(255,255,255,0.06);
  border:1px solid rgba(212,175,55,0.25);box-shadow:0 25px 70px rgba(0,0,0,.7);
  position:relative;z-index:2;
}
.profile{width:95px;height:95px;border-radius:50%;border:3px solid #d4af37;display:block;margin:0 auto 12px;}
.brand{font-family:'Playfair Display',serif;font-size:32px;text-align:center;color:#f5d27a;}
.sub{text-align:center;font-size:12px;color:#f5d27a;}
.name{text-align:center;font-size:20px;color:#f5d27a;}

.rgbDots{display:flex;justify-content:center;gap:10px;margin:6px 0;}
.rgbDots span{width:10px;height:10px;border-radius:50%;animation:pulse 2s infinite alternate;}
.rgbDots span:nth-child(1){background:#ff0000;box-shadow:0 0 10px #ff0000,0 0 20px #ff0000,0 0 30px #ff0000;}
.rgbDots span:nth-child(2){background:#00ff00;box-shadow:0 0 10px #00ff00,0 0 20px #00ff00,0 0 30px #00ff00;animation-delay:.4s;}
.rgbDots span:nth-child(3){background:#0080ff;box-shadow:0 0 10px #0080ff,0 0 20px #0080ff,0 0 30px #0080ff;animation-delay:.8s;}
@keyframes pulse{ from{transform:scale(1);opacity:.7;} to{transform:scale(1.6);opacity:1;} }

.role{text-align:center;font-size:13px;margin-bottom:12px;color:#f5d27a;}
.grid{display:grid;grid-template-columns:1fr 1fr;gap:10px;}
.btn{
  display:flex;align-items:center;justify-content:center;padding:13px;border-radius:16px;
  text-decoration:none;font-weight:600;font-size:14px;color:#f5d27a;
  background:rgba(255,255,255,0.05);border:1px solid rgba(212,175,55,0.5);
  transition:.25s;cursor:pointer;
}
.btn:active{color:#000;background:linear-gradient(135deg,#f5d27a,#d4af37);box-shadow:0 0 20px gold,0 0 40px gold;transform:scale(.95);}
.btn.order-cta{grid-column:1 / -1;background:linear-gradient(135deg,#f5d27a,#d4af37);color:#141105;}

.footer{text-align:center;font-size:11px;margin-top:14px;color:#f5d27a;}

.designPopup{
  position:fixed;inset:0;background:rgba(0,0,0,.95);display:none;
  align-items:center;justify-content:center;flex-direction:column;z-index:999;
}
.designGallery{display:grid;grid-template-columns:repeat(2,1fr);gap:15px;}
.designGallery img{width:150px;border:2px solid gold;border-radius:10px;}
.closeBtn{position:absolute;top:20px;right:20px;font-size:30px;color:white;cursor:pointer;}

/* scroll cue */
.scrollCue{
  position:absolute;bottom:22px;left:50%;transform:translateX(-50%);
  color:#f5d27a;font-size:11px;letter-spacing:.14em;text-transform:uppercase;
  display:flex;flex-direction:column;align-items:center;gap:6px;opacity:.8;z-index:2;
}
.scrollCue span{display:block;width:1px;height:22px;background:#f5d27a;animation:pulse 1.6s infinite alternate;}

/* =========================================================
   SECTION 2 -- ORDER FORM
========================================================= */
:root{
  --ink:#201d1a; --ink-soft:#4a443e;
  --card:#f3ecdf; --card-2:#eae1cd; --card-3:#e0d4b8;
  --gold:#b8935b; --gold-deep:#8f7040; --maroon:#7c2d2d; --sage:#5c6e4f;
  --line:rgba(32,29,26,.16); --line-strong:rgba(32,29,26,.32); --radius:2px;
}
#orderSection{
  display:none;
  position:fixed;inset:0;z-index:1000;overflow-y:auto;
  background:var(--card);
  background-image:radial-gradient(circle at 1px 1px, rgba(32,29,26,.05) 1px, transparent 0);
  background-size:22px 22px;
  color:var(--ink);font-family:'Space Grotesk', sans-serif;
  padding:44px 20px 80px;
}
#orderSection.show{display:block;}
body.modal-open{overflow:hidden;}
.back-to-profile{
  display:inline-flex;align-items:center;gap:6px;margin-bottom:18px;
  font-family:'Space Grotesk',sans-serif;font-size:12.5px;letter-spacing:.06em;text-transform:uppercase;
  color:var(--ink-soft);background:none;border:none;cursor:pointer;padding:0;
}
.back-to-profile:hover{color:var(--maroon);}
.modal-close{
  position:fixed;top:18px;right:22px;z-index:1001;
  width:38px;height:38px;border-radius:50%;
  background:var(--ink);color:var(--card);border:none;cursor:pointer;
  font-size:18px;line-height:1;display:flex;align-items:center;justify-content:center;
  box-shadow:0 6px 16px -6px rgba(32,29,26,.5);
}
.modal-close:hover{background:var(--maroon);}
#orderSection .wrap{max-width:1180px;margin:0 auto;}

#orderSection header{
  display:flex;justify-content:space-between;align-items:flex-end;
  border-bottom:2px solid var(--ink);padding-bottom:18px;margin-bottom:8px;flex-wrap:wrap;gap:14px;
}
.oc-brand{display:flex;align-items:center;gap:14px;}
.oc-brand-mark{
  width:46px;height:46px;border:2px solid var(--ink);border-radius:50%;
  display:flex;align-items:center;justify-content:center;
  font-family:'Fraunces',serif;font-weight:600;font-size:19px;
  background:var(--gold);color:var(--ink);flex-shrink:0;
}
#orderSection h1{font-family:'Fraunces',serif;font-weight:600;font-size:clamp(26px,4vw,36px);margin:0;line-height:1;letter-spacing:.2px;}
.oc-brand p{margin:4px 0 0;font-size:12.5px;letter-spacing:.14em;text-transform:uppercase;color:var(--ink-soft);}
.docket-id{font-family:'IBM Plex Mono',monospace;font-size:12px;color:var(--ink-soft);text-align:right;line-height:1.6;}
.docket-id b{color:var(--maroon);}

.subhead{display:flex;justify-content:space-between;color:var(--ink-soft);font-size:13px;margin-bottom:34px;flex-wrap:wrap;gap:8px;}
.subhead span:first-child{max-width:520px;}

.layout{display:grid;grid-template-columns:390px 1fr;gap:36px;align-items:start;}
@media (max-width:920px){.layout{grid-template-columns:1fr;}}

.proof{position:sticky;top:24px;}
@media (max-width:920px){.proof{position:static;}}
.proof-label{font-family:'IBM Plex Mono',monospace;font-size:11px;letter-spacing:.14em;text-transform:uppercase;color:var(--ink-soft);margin-bottom:10px;display:flex;justify-content:space-between;}
.stage{perspective:1600px;width:100%;aspect-ratio:1.75/1;margin-bottom:14px;}
.card3d{position:relative;width:100%;height:100%;transform-style:preserve-3d;transition:transform .7s cubic-bezier(.6,.2,.1,1);cursor:pointer;}
.card3d.flipped{transform:rotateY(180deg);}
.face{
  position:absolute;inset:0;backface-visibility:hidden;border-radius:10px;
  border:1px solid var(--line-strong);box-shadow:0 18px 34px -14px rgba(32,29,26,.4);
  display:flex;align-items:center;justify-content:center;
  background:linear-gradient(155deg,#fffdf8,#efe6d3);overflow:hidden;
}
.face.back{transform:rotateY(180deg);}
.face img{width:100%;height:100%;object-fit:cover;}
.face .placeholder{text-align:center;color:var(--ink-soft);font-size:11.5px;font-family:'IBM Plex Mono',monospace;letter-spacing:.08em;padding:0 20px;}
.face .placeholder .glyph{font-family:'Fraunces',serif;font-size:30px;color:var(--gold-deep);display:block;margin-bottom:6px;}
.stage-hint{text-align:center;font-size:11px;color:var(--ink-soft);margin-bottom:22px;font-family:'IBM Plex Mono',monospace;}

.quote{background:var(--card-2);border:1px solid var(--line-strong);border-radius:var(--radius);padding:18px 20px;}
.quote-row{display:flex;justify-content:space-between;font-size:13.5px;padding:6px 0;border-bottom:1px dashed var(--line);}
.quote-row:last-of-type{border-bottom:none;}
.quote-row span:first-child{color:var(--ink-soft);}
.quote-total{display:flex;justify-content:space-between;align-items:baseline;margin-top:12px;padding-top:12px;border-top:2px solid var(--ink);}
.quote-total span:first-child{font-family:'Fraunces',serif;font-size:15px;}
.quote-total b{font-family:'Fraunces',serif;font-size:26px;color:var(--maroon);}
.quote-note{font-size:11px;color:var(--ink-soft);margin-top:10px;line-height:1.5;}

#orderForm{display:flex;flex-direction:column;}
.section{padding:26px 0;border-bottom:1px dashed var(--line-strong);}
.section:first-child{padding-top:0;}
.section-head{display:flex;align-items:baseline;gap:10px;margin-bottom:18px;}
.section-num{
  font-family:'IBM Plex Mono',monospace;font-size:12px;color:var(--gold-deep);
  border:1px solid var(--gold-deep);border-radius:50%;width:22px;height:22px;
  display:flex;align-items:center;justify-content:center;flex-shrink:0;
}
.section-head h2{font-family:'Fraunces',serif;font-weight:600;font-size:19px;margin:0;}

.grid2{display:grid;grid-template-columns:1fr 1fr;gap:16px;}
.grid3{display:grid;grid-template-columns:1fr 1fr 1fr;gap:16px;}
@media (max-width:600px){.grid2,.grid3{grid-template-columns:1fr;}}

#orderSection label{display:block;font-size:11px;letter-spacing:.08em;text-transform:uppercase;color:var(--ink-soft);margin-bottom:6px;}
.field{margin-bottom:16px;}
#orderSection input[type=text],#orderSection input[type=tel],#orderSection input[type=email],#orderSection select,#orderSection textarea{
  width:100%;padding:11px 12px;background:#fffdf9;border:1px solid var(--line-strong);border-radius:var(--radius);
  font-family:'Space Grotesk',sans-serif;font-size:14.5px;color:var(--ink);
}
#orderSection input:focus,#orderSection select:focus,#orderSection textarea:focus{outline:2px solid var(--gold-deep);outline-offset:1px;border-color:var(--gold-deep);}
#orderSection textarea{resize:vertical;min-height:78px;}
.required::after{content:' *';color:var(--maroon);}

.uploads{display:grid;grid-template-columns:1fr 1fr;gap:16px;}
@media (max-width:600px){.uploads{grid-template-columns:1fr;}}
.dropzone{
  border:1.5px dashed var(--line-strong);border-radius:var(--radius);padding:18px;text-align:center;
  background:#fffdf9;cursor:pointer;transition:border-color .2s, background .2s;position:relative;min-height:150px;
  display:flex;flex-direction:column;align-items:center;justify-content:center;
}
.dropzone:hover{border-color:var(--gold-deep);background:#fbf6ea;}
.dropzone input{position:absolute;inset:0;opacity:0;cursor:pointer;}
.dropzone .dz-icon{font-family:'Fraunces',serif;font-size:22px;color:var(--gold-deep);margin-bottom:6px;}
.dropzone .dz-title{font-size:13px;font-weight:600;margin-bottom:2px;}
.dropzone .dz-sub{font-size:11px;color:var(--ink-soft);}
.dropzone .dz-file{font-size:11.5px;font-family:'IBM Plex Mono',monospace;color:var(--sage);margin-top:8px;word-break:break-all;padding:0 6px;}
.dropzone img.thumb{position:absolute;inset:0;width:100%;height:100%;object-fit:cover;border-radius:var(--radius);}
.dropzone .thumb-label{position:absolute;bottom:6px;right:8px;background:rgba(32,29,26,.75);color:#f3ecdf;font-family:'IBM Plex Mono',monospace;font-size:10px;padding:2px 6px;border-radius:2px;}

.checkline{display:flex;align-items:flex-start;gap:9px;font-size:13px;color:var(--ink-soft);margin-top:6px;}
.checkline input{margin-top:3px;}

.submit-row{padding-top:26px;display:flex;flex-wrap:wrap;gap:12px;align-items:center;}
#orderSection button{
  font-family:'Space Grotesk',sans-serif;font-weight:600;font-size:14.5px;padding:14px 28px;
  border-radius:var(--radius);border:none;cursor:pointer;letter-spacing:.02em;
  transition:transform .12s ease, box-shadow .12s ease;
}
#orderSection button:active{transform:translateY(1px);}
.btn-primary{background:var(--ink);color:var(--card);}
.btn-primary:hover{box-shadow:0 6px 16px -6px rgba(32,29,26,.5);}
.btn-ghost{background:transparent;color:var(--ink);border:1.5px solid var(--ink);}
.btn-gold{background:var(--gold);color:var(--ink);}
.form-msg{font-size:12.5px;color:var(--maroon);width:100%;min-height:16px;}

.confirm{display:none;}
.confirm.show{display:block;}
.confirm-card{
  border:2px solid var(--ink);border-radius:var(--radius);padding:28px 26px;
  background:repeating-linear-gradient(180deg,#fffdf9,#fffdf9 27px,#f4ecda 28px);position:relative;
}
.confirm-card::before{
  content:'';position:absolute;left:-9px;top:0;bottom:0;width:18px;
  background-image:radial-gradient(circle,var(--card) 4px,transparent 4.2px);background-size:18px 18px;
}
.confirm-stamp{
  display:inline-block;border:2px solid var(--sage);color:var(--sage);font-family:'IBM Plex Mono',monospace;
  font-size:12px;letter-spacing:.12em;padding:4px 10px;border-radius:3px;transform:rotate(-3deg);margin-bottom:14px;
}
.confirm-card h3{font-family:'Fraunces',serif;font-size:22px;margin:0 0 4px;}
.confirm-card .cid{font-family:'IBM Plex Mono',monospace;font-size:12.5px;color:var(--ink-soft);margin-bottom:18px;}
.confirm-grid{display:grid;grid-template-columns:1fr 1fr;gap:4px 24px;font-size:13.5px;margin-bottom:8px;}
.confirm-grid div b{display:block;font-size:10.5px;text-transform:uppercase;letter-spacing:.08em;color:var(--ink-soft);font-weight:500;margin-bottom:2px;}
@media (max-width:600px){.confirm-grid{grid-template-columns:1fr;}}
.confirm-actions{display:flex;gap:12px;margin-top:20px;flex-wrap:wrap;}

#orderSection footer{margin-top:40px;text-align:center;font-size:11.5px;color:var(--ink-soft);}
</style>
</head>
<body>
<!-- =========================================================
     SECTION 1 -- PROFILE / DIGITAL CARD
========================================================= -->
<div class="profile-hero" id="profileHero">
  <div class="card">
    <img src="owner.png" class="profile">
    <div class="brand">ELITE</div>
    <div class="sub">CARDS STUDIO</div>
    <div class="name">Muneeswaran R</div>
    <div class="rgbDots"><span></span><span></span><span></span></div>

    <div class="role">CXO | Creative Director</div>

    <div class="grid">
      <a href="tel:+919655223394" class="btn">📞 Call</a>
      <a href="https://wa.me/919655223394" class="btn">💬 WhatsApp</a>
      <a href="#" onclick="downloadContact()" class="btn">💾 Save</a>
      <a href="mailto:elitecardsstudio@gmail.com" class="btn">📧 Email</a>
      <a href="https://maps.google.com/?q=Elite+Cards+Studio" class="btn">📍 Location</a>
      <a href="upi://pay?pa=9655223394@axisbank&pn=Muneeswaran&cu=INR" class="btn">💳 UPI</a>
      <a href="#" onclick="openDesign()" class="btn">🎨 Designs</a>
      <a href="#" onclick="openOrder();return false;" class="btn order-cta">✍️ Order Here</a>
    </div>

    <div class="footer">
      Luxury Business Cards | Digital Cards | QR Virtual Card | Premium Texture Cards | Spot UV Cards
    </div>
  </div>

  <div class="scrollCue"><span></span>Order form below</div>
</div>

<!-- POPUP -->
<div class="designPopup" id="designPopup">
  <span class="closeBtn" onclick="closeDesign()">✖</span>
  <div class="designGallery">
    <img src="design1.jpg"><img src="design2.jpg"><img src="design3.jpg"><img src="design4.jpg">
    <img src="design5.jpg"><img src="design6.jpg"><img src="design7.jpg"><img src="design8.jpg">
    <img src="design9.jpg"><img src="design10.jpg"><img src="design11.png">
  </div>
</div>

<!-- =========================================================
     SECTION 2 -- ORDER FORM
========================================================= -->
<div id="orderSection">
  <button type="button" class="modal-close" onclick="closeOrder()" aria-label="Close order form">✕</button>
  <div class="wrap">
    <header>
      <div class="oc-brand">
        <div class="oc-brand-mark">EC</div>
        <div>
          <h1>Elite Cards Studio</h1>
          <p>Business Card Print Order</p>
        </div>
      </div>
      <div class="docket-id">
        Docket No. <b id="docketPreview">ECS-000000</b><br>
        <span id="dateStamp"></span>
      </div>
    </header>

    <div class="subhead">
      <span>Fill in your details, upload your front and back artwork, and confirm your specification. We print gloss, matt, synthetic, metallic and textured finishes, single or double sided.</span>
      <span>Front &amp; back artwork required</span>
    </div>

    <div class="layout">

      <div class="proof">
        <div class="proof-label"><span>Proof preview</span><span id="sideTag">SINGLE SIDE</span></div>
        <div class="stage">
          <div class="card3d" id="card3d">
            <div class="face front">
              <div class="placeholder" id="frontPlaceholder"><span class="glyph">A</span>Front artwork<br>appears here</div>
              <img id="frontImg" style="display:none">
            </div>
            <div class="face back">
              <div class="placeholder" id="backPlaceholder"><span class="glyph">B</span>Back artwork<br>appears here</div>
              <img id="backImg" style="display:none">
            </div>
          </div>
        </div>
        <div class="stage-hint">tap the card to flip · front / back</div>

        <div class="quote">
          <div class="quote-row"><span>Finish</span><span id="qFinish">Gloss Cards</span></div>
          <div class="quote-row"><span>Sides</span><span id="qSide">Single side</span></div>
          <div class="quote-row"><span>Quantity</span><span id="qQty">500 pcs</span></div>
          <div class="quote-row"><span>Design service</span><span id="qDesign">Not needed</span></div>
          <div class="quote-total"><span>Estimated total</span><b id="qTotal">₹599</b></div>
          <div class="quote-note">Estimate from our current rate card. Final price is confirmed on the phone once artwork is reviewed. Prices in INR.</div>
        </div>
      </div>

      <div>
        <form id="orderForm">

          <div class="section">
            <div class="section-head"><span class="section-num">1</span><h2>Contact details</h2></div>
            <div class="grid2">
              <div class="field"><label class="required" for="fullName">Full name</label><input type="text" id="fullName" required placeholder="e.g. Arun Kumar"></div>
              <div class="field"><label class="required" for="phone">Phone / WhatsApp number</label><input type="tel" id="phone" required placeholder="e.g. 98765 43210"></div>
            </div>
            <div class="grid2">
              <div class="field"><label for="email">Email</label><input type="email" id="email" placeholder="e.g. arun@email.com"></div>
              <div class="field"><label for="company">Company / title on card</label><input type="text" id="company" placeholder="e.g. Arun Kumar, Interior Designer"></div>
            </div>
          </div>

          <div class="section">
            <div class="section-head"><span class="section-num">2</span><h2>Delivery address</h2></div>
            <div class="field"><label class="required" for="addr1">Address line</label><input type="text" id="addr1" required placeholder="Flat / building, street, area"></div>
            <div class="grid3">
              <div class="field"><label class="required" for="city">City</label><input type="text" id="city" required></div>
              <div class="field"><label class="required" for="state">State</label><input type="text" id="state" required></div>
              <div class="field"><label class="required" for="pin">PIN code</label><input type="text" id="pin" required inputmode="numeric"></div>
            </div>
            <div class="field"><label for="landmark">Landmark (optional)</label><input type="text" id="landmark" placeholder="Nearby landmark for the courier"></div>
          </div>

          <div class="section">
            <div class="section-head"><span class="section-num">3</span><h2>Card specification</h2></div>
            <div class="grid3">
              <div class="field"><label class="required" for="finish">Finish / type</label><select id="finish"></select></div>
              <div class="field"><label class="required" for="sides">Sides</label>
                <select id="sides"><option value="single">Single side</option><option value="double">Double side</option></select>
              </div>
              <div class="field"><label class="required" for="qty">Quantity</label><select id="qty"></select></div>
            </div>
            <label class="checkline"><input type="checkbox" id="needDesign"> I need the studio's designer to create my artwork (+ ₹350 design charge, where applicable)</label>
          </div>

          <div class="section">
            <div class="section-head"><span class="section-num">4</span><h2>Upload artwork</h2></div>
            <div class="uploads">
              <label class="dropzone" id="dzFront">
                <input type="file" id="fileFront" accept="image/*,.pdf,.ai,.psd">
                <div class="dz-icon">⤒</div><div class="dz-title">Front side</div><div class="dz-sub">Image or PDF, print-ready</div>
                <div class="dz-file" id="fileFrontName"></div>
              </label>
              <label class="dropzone" id="dzBack">
                <input type="file" id="fileBack" accept="image/*,.pdf,.ai,.psd">
                <div class="dz-icon">⤓</div><div class="dz-title">Back side</div><div class="dz-sub">Image or PDF, print-ready</div>
                <div class="dz-file" id="fileBackName"></div>
              </label>
            </div>
          </div>

          <div class="section">
            <div class="section-head"><span class="section-num">5</span><h2>Special instructions</h2></div>
            <div class="field"><label for="notes">Anything we should know -- colours, urgency, reference card, etc.</label><textarea id="notes" placeholder="Optional"></textarea></div>
          </div>

          <div class="submit-row">
            <button type="submit" class="btn-primary">Submit order</button>
            <span class="form-msg" id="formMsg"></span>
          </div>
        </form>

        <div class="confirm" id="confirmBlock">
          <div class="confirm-card">
            <span class="confirm-stamp">✓ RECEIVED</span>
            <h3>Order docket ready</h3>
            <div class="cid">Docket No. <span id="confirmId"></span> · <span id="confirmDate"></span></div>
            <div class="confirm-grid" id="confirmGrid"></div>
            <div class="confirm-actions">
              <button type="button" class="btn-primary" id="waBtn">Send to studio on WhatsApp</button>
              <button type="button" class="btn-gold" id="emailBtn">Send to studio by Email</button>
              <button type="button" class="btn-ghost" id="editBtn">Edit this order</button>
              <button type="button" class="btn-ghost" id="newOrderBtn">＋ Create new order</button>
            </div>
          </div>
        </div>

      </div>
    </div>

    <footer>Elite Cards Studio -- this form prepares your order docket in your browser. Attach the front/back artwork files manually when you send it over WhatsApp or email, as browsers can't attach files automatically.</footer>

  </div>
</div>

<script>
/* ---------- Profile card scripts ---------- */
for(let i=0;i<20;i++){
  let p=document.createElement("div");
  p.className="particle";
  p.style.left=Math.random()*100+"vw";
  p.style.animationDuration=(10+Math.random()*10)+"s";
  document.getElementById('profileHero').appendChild(p);
}
function downloadContact(){
  const link=document.createElement("a");
  link.href="Elite_Cards_Studio.vcf";
  link.download="Elite_Cards_Studio.vcf";
  link.click();
}
window.addEventListener('load', function(){ setTimeout(downloadContact,1500); });
function openDesign(){ document.getElementById("designPopup").style.display="flex"; }
function closeDesign(){ document.getElementById("designPopup").style.display="none"; }

/* ---------- Show / hide order form (modal) ---------- */
function openOrder(){
  document.getElementById('orderSection').classList.add('show');
  document.body.classList.add('modal-open');
  document.getElementById('orderSection').scrollTop = 0;
}
function closeOrder(){
  document.getElementById('orderSection').classList.remove('show');
  document.body.classList.remove('modal-open');
}

/* ---------- Order form: rate data ---------- */
const RATES = {
  "Gloss Cards":            { single:{500:599,1000:999},            double:{500:999,1000:1299},  design:350 },
  "Matt Card":               { single:{500:799,1000:1199},           double:{500:1299,1000:1699}, design:350 },
  "Synthetic Cards":         { single:{500:1199,1000:1599},          double:{500:1599,1000:1999}, design:350 },
  "Nature Visiting Card (Spcl)": { single:{500:1099,1000:2099},      double:{},                    design:0   },
  "Metallic Gold (300 GSM)": { single:{100:999,500:2999,1000:3999},  double:{100:999,500:3999,1000:4999}, design:350 },
  "Metallic Silver (300 GSM)":{ single:{100:999,500:2999,1000:3999}, double:{100:999,500:3999,1000:4999}, design:350 },
  "Texture -- Linen White":   { single:{100:999,500:2999,1000:3999},  double:{100:999,500:3999,1000:4999}, design:350 },
  "Texture -- Linen Yellow":  { single:{100:999,500:2999,1000:3999},  double:{100:999,500:3999,1000:4999}, design:350 },
  "Texture -- Kriss Cross":   { single:{100:999,500:2999,1000:3999},  double:{100:999,500:3999,1000:4999}, design:350 },
  "Texture -- Leather":       { single:{100:999,500:2999,1000:3999},  double:{100:999,500:3999,1000:4999}, design:350 },
};

const finishSel = document.getElementById('finish');
const sidesSel  = document.getElementById('sides');
const qtySel    = document.getElementById('qty');
const needDesign = document.getElementById('needDesign');

Object.keys(RATES).forEach(name=>{
  const o = document.createElement('option');
  o.value = name; o.textContent = name;
  finishSel.appendChild(o);
});

function availableQtys(){
  const finish = RATES[finishSel.value];
  const side = sidesSel.value;
  return Object.keys(finish[side] || {}).map(Number).sort((a,b)=>a-b);
}
function refreshQtyOptions(){
  const qtys = availableQtys();
  const prev = qtySel.value;
  qtySel.innerHTML = '';
  if(qtys.length === 0){
    const o = document.createElement('option');
    o.textContent = 'Not available for this side -- call studio';
    o.value = '';
    qtySel.appendChild(o);
  } else {
    qtys.forEach(q=>{
      const o = document.createElement('option');
      o.value = q; o.textContent = q + ' pcs';
      qtySel.appendChild(o);
    });
    if(qtys.includes(Number(prev))) qtySel.value = prev;
  }
  updateQuote();
}
function updateQuote(){
  const finishName = finishSel.value;
  const finish = RATES[finishName];
  const side = sidesSel.value;
  const qty = qtySel.value;
  const base = (finish[side] && qty) ? finish[side][qty] : null;
  const design = needDesign.checked ? (finish.design || 0) : 0;
  const total = base ? base + design : null;

  document.getElementById('qFinish').textContent = finishName;
  document.getElementById('qSide').textContent = side === 'single' ? 'Single side' : 'Double side';
  document.getElementById('qQty').textContent = qty ? (qty + ' pcs') : '--';
  document.getElementById('qDesign').textContent = needDesign.checked ? ('+ ₹' + (finish.design || 0)) : 'Not needed';
  document.getElementById('qTotal').textContent = total !== null ? ('₹' + total.toLocaleString('en-IN')) : 'Call for quote';
  document.getElementById('sideTag').textContent = side === 'single' ? 'SINGLE SIDE' : 'DOUBLE SIDE';
}
finishSel.addEventListener('change', refreshQtyOptions);
sidesSel.addEventListener('change', refreshQtyOptions);
qtySel.addEventListener('change', updateQuote);
needDesign.addEventListener('change', updateQuote);
refreshQtyOptions();

/* ---------- Card flip ---------- */
const card3d = document.getElementById('card3d');
card3d.addEventListener('click', ()=> card3d.classList.toggle('flipped'));

/* ---------- File uploads + live preview ---------- */
function wireUpload(inputId, nameId, imgId, placeholderId){
  const input = document.getElementById(inputId);
  const nameEl = document.getElementById(nameId);
  const img = document.getElementById(imgId);
  const placeholder = document.getElementById(placeholderId);
  input.addEventListener('change', ()=>{
    const f = input.files[0];
    if(!f) return;
    nameEl.textContent = f.name;
    if(f.type.startsWith('image/')){
      const reader = new FileReader();
      reader.onload = e=>{
        img.src = e.target.result;
        img.style.display = 'block';
        placeholder.style.display = 'none';
        const dz = input.closest('.dropzone');
        let thumb = dz.querySelector('img.thumb');
        if(!thumb){
          thumb = document.createElement('img');
          thumb.className = 'thumb';
          dz.insertBefore(thumb, dz.firstChild);
          const lbl = document.createElement('div');
          lbl.className = 'thumb-label';
          lbl.textContent = f.name.length > 22 ? f.name.slice(0,19)+'…' : f.name;
          dz.appendChild(lbl);
        }
        thumb.src = e.target.result;
      };
      reader.readAsDataURL(f);
    } else {
      placeholder.innerHTML = '<span class="glyph">✓</span>' + f.name + '<br>ready for print';
    }
  });
}
wireUpload('fileFront','fileFrontName','frontImg','frontPlaceholder');
wireUpload('fileBack','fileBackName','backImg','backPlaceholder');

/* ---------- Docket id / date ---------- */
function makeDocketId(){
  const d = new Date();
  const yy = String(d.getFullYear()).slice(2);
  const mm = String(d.getMonth()+1).padStart(2,'0');
  const dd = String(d.getDate()).padStart(2,'0');
  const rand = Math.floor(1000 + Math.random()*9000);
  return `ECS-${yy}${mm}${dd}-${rand}`;
}
let docketId = makeDocketId();
document.getElementById('docketPreview').textContent = docketId;
document.getElementById('dateStamp').textContent = new Date().toLocaleDateString('en-IN', {day:'numeric',month:'short',year:'numeric'});

/* ---------- Submit ---------- */
const form = document.getElementById('orderForm');
const confirmBlock = document.getElementById('confirmBlock');
const formMsg = document.getElementById('formMsg');

/* studio's own address used for the email send button */
const STUDIO_EMAIL = 'elitecardsstudio@gmail.com';

function buildOrderData(){
  return {
    name: document.getElementById('fullName').value,
    phone: document.getElementById('phone').value,
    email: document.getElementById('email').value,
    company: document.getElementById('company').value,
    addr1: document.getElementById('addr1').value,
    city: document.getElementById('city').value,
    state: document.getElementById('state').value,
    pin: document.getElementById('pin').value,
    landmark: document.getElementById('landmark').value,
    finish: finishSel.value,
    sides: sidesSel.options[sidesSel.selectedIndex].textContent,
    qty: qtySel.value ? qtySel.value + ' pcs' : '--',
    design: needDesign.checked ? 'Yes (+₹' + (RATES[finishSel.value].design||0) + ')' : 'No',
    total: document.getElementById('qTotal').textContent,
    notes: document.getElementById('notes').value,
    frontFile: document.getElementById('fileFrontName').textContent || 'not attached',
    backFile: document.getElementById('fileBackName').textContent || 'not attached',
  };
}

form.addEventListener('submit', e=>{
  e.preventDefault();
  if(!form.checkValidity()){
    formMsg.textContent = 'Please fill in all required fields marked with *.';
    form.reportValidity();
    return;
  }
  formMsg.textContent = '';
  const data = buildOrderData();

  docketId = makeDocketId();
  document.getElementById('confirmId').textContent = docketId;
  document.getElementById('confirmDate').textContent = new Date().toLocaleDateString('en-IN', {day:'numeric',month:'short',year:'numeric', hour:'2-digit', minute:'2-digit'});

  const grid = document.getElementById('confirmGrid');
  const rows = [
    ['Name', data.name], ['Phone', data.phone], ['Email', data.email || '--'],
    ['Company / title', data.company || '--'],
    ['Address', `${data.addr1}, ${data.city}, ${data.state} - ${data.pin}` + (data.landmark ? ` (near ${data.landmark})` : '')],
    ['Finish', data.finish], ['Sides', data.sides], ['Quantity', data.qty],
    ['Design service', data.design], ['Estimated total', data.total],
    ['Front artwork', data.frontFile], ['Back artwork', data.backFile],
    ['Notes', data.notes || '--'],
  ];
  grid.innerHTML = rows.map(([k,v])=>`<div><b>${k}</b>${v}</div>`).join('');

  form.style.display = 'none';
  confirmBlock.classList.add('show');
  confirmBlock.scrollIntoView({behavior:'smooth', block:'start'});

  document.getElementById('waBtn').onclick = ()=>{
    const msg =
`New order -- Elite Cards Studio
Docket: ${docketId}
Name: ${data.name}
Phone: ${data.phone}
Address: ${data.addr1}, ${data.city}, ${data.state} - ${data.pin}
Finish: ${data.finish}
Sides: ${data.sides}
Qty: ${data.qty}
Design service: ${data.design}
Estimated total: ${data.total}
Notes: ${data.notes || '--'}
(Front: ${data.frontFile} / Back: ${data.backFile} -- please attach these files in chat)`;
    window.open('https://wa.me/919655223394?text=' + encodeURIComponent(msg), '_blank');
  };

  document.getElementById('emailBtn').onclick = ()=>{
    const subject = `New order ${docketId} -- Elite Cards Studio`;
    const body =
`New order -- Elite Cards Studio
Docket: ${docketId}

Name: ${data.name}
Phone: ${data.phone}
Email: ${data.email || '--'}
Company / title: ${data.company || '--'}

Delivery address: ${data.addr1}, ${data.city}, ${data.state} - ${data.pin}${data.landmark ? ' (near ' + data.landmark + ')' : ''}

Finish: ${data.finish}
Sides: ${data.sides}
Quantity: ${data.qty}
Design service: ${data.design}
Estimated total: ${data.total}

Notes: ${data.notes || '--'}

Front artwork file: ${data.frontFile}
Back artwork file: ${data.backFile}
(Please attach these files to this email manually before sending)`;
    window.location.href = 'mailto:' + STUDIO_EMAIL
      + '?subject=' + encodeURIComponent(subject)
      + '&body=' + encodeURIComponent(body);
  };
});

/* Edit this order -- go back to the form, keep everything filled in */
document.getElementById('editBtn').addEventListener('click', ()=>{
  confirmBlock.classList.remove('show');
  form.style.display = 'flex';
  form.scrollIntoView({behavior:'smooth', block:'start'});
});

/* Create new order -- full reset, ready for the next customer */
function resetOrderForm(){
  form.reset();

  ['fileFront','fileBack'].forEach(id=>{ document.getElementById(id).value = ''; });
  document.getElementById('fileFrontName').textContent = '';
  document.getElementById('fileBackName').textContent = '';

  const frontImg = document.getElementById('frontImg');
  const backImg = document.getElementById('backImg');
  frontImg.style.display = 'none'; frontImg.src = '';
  backImg.style.display = 'none'; backImg.src = '';

  const frontPlaceholder = document.getElementById('frontPlaceholder');
  const backPlaceholder = document.getElementById('backPlaceholder');
  frontPlaceholder.style.display = 'flex';
  backPlaceholder.style.display = 'flex';
  frontPlaceholder.innerHTML = '<span class="glyph">A</span>Front artwork<br>appears here';
  backPlaceholder.innerHTML = '<span class="glyph">B</span>Back artwork<br>appears here';

  document.querySelectorAll('.dropzone img.thumb, .dropzone .thumb-label').forEach(el=>el.remove());

  card3d.classList.remove('flipped');

  finishSel.selectedIndex = 0;
  sidesSel.selectedIndex = 0;
  refreshQtyOptions();

  docketId = makeDocketId();
  document.getElementById('docketPreview').textContent = docketId;
  document.getElementById('dateStamp').textContent = new Date().toLocaleDateString('en-IN', {day:'numeric',month:'short',year:'numeric'});

  formMsg.textContent = '';
  confirmBlock.classList.remove('show');
  form.style.display = 'flex';
  document.getElementById('orderSection').scrollTop = 0;
}
document.getElementById('newOrderBtn').addEventListener('click', resetOrderForm);
</script>
</body>
</html>
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Happy Birthday KK Dika 💖</title>

<style>
/* ================= GLOBAL ================= */
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  min-height: 100vh;
  background: linear-gradient(135deg, #ffb6c1, #ffe4e1);
  display: flex;
  flex-direction: column;
  align-items: center;
  font-family: "Comic Sans MS", cursive;
  overflow-y: auto;
  animation: bgMove 6s ease-in-out infinite alternate;
}

/* ================= TEXT ================= */
h1 {
  color: white;
  font-size: clamp(2rem, 4vw, 3rem);
  margin: 20px 0;
  text-shadow: 0 0 15px pink;
  text-align: center;
  z-index: 10;
}

/* ================= CAKE ================= */
.cake {
  position: relative;
  width: 220px;
  margin-top: 10px;
  z-index: 10;
}

.layer {
  height: 60px;
  border-radius: 18px;
  margin: auto;
  position: relative;
}

.layer1 { background: #ff9aa2; width: 220px; }
.layer2 { background: #ffb7b2; width: 180px; margin-top: -12px; }
.layer3 { background: #ffdac1; width: 140px; margin-top: -12px; }

.drip {
  position: absolute;
  width: 18px;
  height: 26px;
  background: #6b3e26;
  border-radius: 0 0 12px 12px;
  top: 0;
}

.drip:nth-child(1) { left: 35px; }
.drip:nth-child(2) { left: 95px; }
.drip:nth-child(3) { left: 155px; }

/* ================= CANDLE ================= */
.candle {
  width: 14px;
  height: 45px;
  background: #fff;
  margin: auto;
  position: relative;
  top: -18px;
  border-radius: 4px;
}

.flame {
  width: 18px;
  height: 18px;
  background: radial-gradient(circle, #ffd700, orange, red);
  border-radius: 50%;
  position: absolute;
  top: -18px;
  left: -2px;
  animation: flame 0.25s infinite alternate;
  filter: blur(0.5px);
}

/* ================= HEARTS ================= */
.heart {
  position: fixed;
  font-size: 20px;
  animation: fall linear forwards;
  pointer-events: none;
  opacity: 0.9;
}

/* ================= SPOTIFY ================= */
.spotify {
  margin-top: 25px;
  z-index: 10;
}

/* ================= SECRET TEXT ================= */
.secret {
  max-width: 330px;
  margin: 30px auto 60px;
  text-align: center;
  font-size: 15.5px;
  line-height: 1.7;
  color: white;
  opacity: 0;
  transform: translateY(20px);
  transition: 1.5s ease;
  text-shadow: 0 0 10px rgba(255,255,255,0.4);
  z-index: 10;
}

/* ================= ANIMATIONS ================= */
@keyframes flame {
  0% { transform: scale(1) rotate(-2deg); }
  100% { transform: scale(1.3) rotate(2deg); }
}

@keyframes fall {
  0% {
    transform: translateY(-10vh) scale(1);
    opacity: 1;
  }
  100% {
    transform: translateY(110vh) scale(0.6);
    opacity: 0;
  }
}

@keyframes bgMove {
  0% { background-position: left; }
  100% { background-position: right; }
}
</style>
</head>

<body>

<h1>💖 Happy Birthday KK Dika 💖</h1>

<div class="cake">
  <div class="candle">
    <div class="flame"></div>
  </div>

  <div class="layer layer3"></div>
  <div class="layer layer2"></div>
  <div class="layer layer1">
    <div class="drip"></div>
    <div class="drip"></div>
    <div class="drip"></div>
  </div>
</div>

<!-- SPOTIFY -->
<div class="spotify">
  <iframe 
    id="spotifyPlayer"
    style="border-radius:12px"
    src="https://open.spotify.com/embed/track/38Z9ira4cManq7mw70Px81"
    width="300"
    height="80"
    frameborder="0"
    allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture">
  </iframe>
</div>

<!-- PESAN RAHASIA -->
<div id="secretMessage" class="secret">
  💖 <b>Selamat ulang tahun ya, kk…</b><br><br>

  Hari ini mungkin cuma satu hari biasa,<br>
  tapi buat Put, hari ini spesial karena kk lahir ke dunia 🤍<br><br>

  Makasih ya, kk…  
  udah bertahan sejauh ini,  
  udah kuat walau kadang capek,  
  dan tetap jalan meski nggak selalu mudah.<br><br>

  Put cuma mau bilang,<br>
  kk itu berarti…  
  lebih dari yang kk kira 💫<br><br>

  Semoga langkah kk ke depan lebih ringan,  
  hatinya lebih tenang,  
  dan hidupnya penuh hal baik 🤍
</div>

<script>
function createHeart() {
  const heart = document.createElement("div");
  heart.className = "heart";
  heart.innerHTML = ["💖","💗","💕","💞"][Math.floor(Math.random() * 4)];
  heart.style.left = Math.random() * 100 + "vw";
  heart.style.animationDuration = (3 + Math.random() * 3) + "s";
  heart.style.fontSize = (18 + Math.random() * 15) + "px";
  document.body.appendChild(heart);

  setTimeout(() => heart.remove(), 6000);
}

setInterval(createHeart, 350);

setTimeout(() => {
  document.getElementById("secretMessage").style.opacity = "1";
  document.getElementById("secretMessage").style.transform = "translateY(0)";
}, 1200);
</script>

</body>
</html>


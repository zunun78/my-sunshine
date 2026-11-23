<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Untuk Clarissa ❤️</title>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  min-height: 100vh;
  font-family: 'Segoe UI', sans-serif;
  background: linear-gradient(135deg,#130b2c,#39204e,#743b67);
  color: white;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow-x: hidden;
  text-align: center;
  padding: 20px;
}

.container {
  max-width: 500px;
  width: 100%;
  padding: 35px 25px;
  background: rgba(255,255,255,.10);
  border: 1px solid rgba(255,255,255,.2);
  border-radius: 25px;
  backdrop-filter: blur(12px);
  box-shadow: 0 10px 40px #0005;
  animation: muncul 2s ease;
  z-index: 2;
}

h1 {
  color: #ffd4ed;
  font-size: 32px;
  margin-bottom: 15px;
}

.heart {
  font-size: 55px;
  animation: detak 1.3s infinite;
  margin: 15px;
}

p {
  font-size: 16px;
  line-height: 1.9;
  margin: 15px 0;
}

.highlight {
  color: #ffb8dc;
  font-weight: bold;
}

button {
  border: none;
  padding: 13px 25px;
  border-radius: 30px;
  background: linear-gradient(90deg,#ff76b7,#c77dff);
  color: white;
  font-size: 15px;
  font-weight: bold;
  cursor: pointer;
  margin-top: 15px;
  box-shadow: 0 5px 20px #0004;
}

button:hover {
  transform: scale(1.05);
}

.signature {
  margin-top: 25px;
  color: #ffd0e9;
  font-style: italic;
  font-size: 20px;
}

.floating {
  position: fixed;
  bottom: -30px;
  animation: naik 8s linear infinite;
  opacity: .7;
  z-index: 1;
}

@keyframes detak {
  50% { transform: scale(1.25); }
}

@keyframes muncul {
  from {opacity:0; transform:translateY(30px);}
  to {opacity:1; transform:translateY(0);}
}

@keyframes naik {
  to {transform:translateY(-110vh) rotate(360deg); opacity:0;}
}
</style>
</head>

<body>

<div class="container">
  <div class="heart">❤️</div>

  <h1>Untuk Clarissa</h1>

  <p>
    Selamat melepas lelah, Clarissa sayang...
  </p>

  <p>
    Hari ini mungkin tidak mudah untukmu.
    Ada banyak hal yang sudah kamu lalui,
    banyak pikiran yang mungkin kamu simpan,
    dan banyak lelah yang tidak semua orang tahu.
  </p>

  <p class="highlight">
    Sekarang waktunya kamu beristirahat.
    Jangan terlalu keras pada dirimu sendiri.
  </p>

  <p>
    Kamu tidak harus selalu kuat setiap saat.
    Tidak apa-apa jika hari ini kamu merasa lelah.
    Tidak apa-apa jika kamu ingin diam sejenak.
    Ingat, istirahat bukan berarti menyerah.
  </p>

  <p>
    Aku berharap esok kamu bangun dengan hati
    yang lebih tenang, senyum yang lebih indah,
    dan semangat baru untuk menjalani hari.
  </p>

  <p class="highlight">
    Jangan pernah meragukan dirimu sendiri.
    Kamu jauh lebih kuat dan berharga
    daripada yang kamu bayangkan.
  </p>

  <div class="heart">💗</div>

  <p>
    Terima kasih sudah bertahan sampai hari ini.
    Semoga semua lelahmu berubah menjadi kebahagiaan
    dan setiap langkahmu membawa kebaikan.
  </p>

  <p class="signature">
    Dengan penuh perhatian,<br>
    Zunun ❤️
  </p>

  <button onclick="playMusic()" id="musicBtn">
    ▶ Putar Musik Pengantar Istirahat
  </button>

  <p style="font-size:12px;color:#f6c9e4;">
    Sebuah melodi lembut untuk menemani istirahatmu.
  </p>
</div>

<script>
let audioContext;
let playing = false;
let timer;
let noteIndex = 0;

const notes = [
  261.63, 329.63, 392.00, 329.63,
  293.66, 349.23, 440.00, 349.23,
  261.63, 329.63, 392.00, 523.25
];

function playNote(freq) {
  const osc = audioContext.createOscillator();
  const gain = audioContext.createGain();

  osc.type = "sine";
  osc.frequency.value = freq;

  gain.gain.setValueAtTime(0.0001,
    audioContext.currentTime);
  gain.gain.exponentialRampToValueAtTime(
    0.12, audioContext.currentTime + 0.15);
  gain.gain.exponentialRampToValueAtTime(
    0.0001, audioContext.currentTime + 1.8);

  osc.connect(gain);
  gain.connect(audioContext.destination);

  osc.start();
  osc.stop(audioContext.currentTime + 2);
}

function playMusic() {
  const btn = document.getElementById("musicBtn");

  if (!playing) {
    if (!audioContext) {
      audioContext = new (window.AudioContext ||
        window.webkitAudioContext)();
    }

    audioContext.resume();
    playing = true;
    btn.innerHTML = "⏸ Jeda Musik";

    timer = setInterval(() => {
      playNote(notes[noteIndex % notes.length]);
      noteIndex++;
    }, 700);

  } else {
    clearInterval(timer);
    audioContext.suspend();
    playing = false;
    btn.innerHTML = "▶ Lanjutkan Musik";
  }
}

// Animasi hati melayang
function createHeart() {
  const heart = document.createElement("div");
  heart.className = "floating";
  heart.innerHTML = Math.random() > 0.5 ? "❤️" : "💕";
  heart.style.left = Math.random() * 100 + "vw";
  heart.style.fontSize = (15 + Math.random()*20) + "px";
  heart.style.animationDuration = (5 + Math.random()*6) + "s";

  document.body.appendChild(heart);

  setTimeout(() => heart.remove(), 11000);
}

setInterval(createHeart, 600);
</script>

</body>
</html>

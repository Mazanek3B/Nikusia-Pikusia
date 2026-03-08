<!DOCTYPE html>
<html lang="pl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no"/>
  <title>Dla Nikusi Pikusi ♡ Najsłodszej na świecie</title>
  
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&family=Dancing+Script:wght@600;700&family=Baloo+2:wght@500;700&display=swap" rel="stylesheet">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      min-height: 100dvh;
      background: linear-gradient(135deg, #ffe6f2 0%, #ffd1e0 50%, #ffc2d9 100%);
      font-family: 'Poppins', system-ui, sans-serif;
      color: #4a1e2f;
      overflow-x: hidden;
      position: relative;
      touch-action: manipulation;
    }

    .hearts-container {
      position: fixed;
      inset: 0;
      pointer-events: none;
      z-index: 1;
    }

    .heart {
      position: absolute;
      font-size: clamp(16px, 5.5vw, 24px);
      color: white;
      animation: floatUp linear forwards;
      text-shadow: 0 0 14px #ff85c0, 0 0 28px #ff4d94;
      will-change: transform, opacity;
    }

    @keyframes floatUp {
      0%   { transform: translateY(110dvh) scale(0.4) rotate(0deg); opacity: 0.85; }
      100% { transform: translateY(-25dvh) scale(1.25) rotate(1080deg); opacity: 0; }
    }

    main {
      position: relative;
      z-index: 10;
      min-height: 100dvh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 5vh 5vw;
      text-align: center;
      gap: 3vh;
    }

    h1 {
      font-family: 'Dancing Script', cursive;
      font-size: clamp(4.2rem, 15vw, 8.5rem);
      color: #ff4d94;
      line-height: 0.9;
      text-shadow: 0 0 35px #ff85c0, 0 0 70px #ff1493;
      margin-bottom: 0.15em;
      animation: sweet-glow 3.2s ease-in-out infinite alternate;
    }

    @keyframes sweet-glow {
      from { text-shadow: 0 0 25px #ffb3d9, 0 0 55px #ff85c0; }
      to   { text-shadow: 0 0 55px #ff4d94, 0 0 110px #ff1493; }
    }

    .love-msg {
      font-family: 'Baloo 2', cursive;
      font-size: clamp(1.35rem, 5.8vw, 2.25rem);
      color: #5c1f38;
      line-height: 1.48;
      max-width: 92vw;
      font-weight: 600;
      text-shadow: 0 2px 12px rgba(255,105,180,0.4);
    }

    .highlight {
      color: #fff;
      font-weight: 700;
      background: linear-gradient(90deg, #ff85c0, #ff4d94, #ff1493);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    .kitty-big {
      font-size: clamp(4.5rem, 20vw, 9rem);
      margin: 1.5vh 0 2.5vh;
      animation: happy-bounce 2.8s infinite ease-in-out;
      filter: drop-shadow(0 12px 24px rgba(255,77,148,0.45));
    }

    @keyframes happy-bounce {
      0%,100% { transform: translateY(0) rotate(0deg); }
      50%     { transform: translateY(-14px) rotate(3deg); }
    }

    .kitty-small {
      font-size: clamp(2.4rem, 10vw, 4.2rem);
      margin: 1vh 0 2vh;
      color: #ff85c0;
    }

    .signature {
      margin-top: 6vh;
      font-size: clamp(1.15rem, 4.5vw, 1.5rem);
      color: #6b2d47;
      font-style: italic;
      opacity: 0.95;
      text-shadow: 0 1px 10px rgba(0,0,0,0.3);
    }

    @media (orientation: landscape) and (max-height: 520px) {
      main { padding: 3vh 6vw; gap: 2vh; }
      h1 { font-size: clamp(3.5rem, 13vw, 6.5rem); }
      .kitty-big { font-size: clamp(3.8rem, 18vw, 7rem); }
    }
  </style>
</head>
<body>

<div class="hearts-container" id="hearts"></div>

<main>
  <h1>Nikusia Pikusia ♡</h1>

  <div class="love-msg">
    Jesteś moim <span class="highlight">najmilszym puchatkiem</span> na całym wszechświecie 🌸
  </div>

  <div class="kitty-big">ฅ^•ﻌ•^ฅ 💕</div>

  <div class="love-msg">
    Kiedy się uśmiechasz to mi się robi <span class="highlight">tęcza w sercu</span><br>
    a jak mruczysz to cały świat robi się różowy i mięciutki 🐾✨
  </div>

  <div class="kitty-small">^•ﻌ•^  ♡  ^•ﻌ•^  ♡  ^•ﻌ•^</div>

  <div class="love-msg">
    Kocham Cię najmocniej na świecie,<br>
    bardziej niż wszystkie puszyste ogonki i różowe poduszeczki razem wzięte 💗🐱
  </div>

  <div class="signature">
    8 marca 2026<br>
    Twój największy wielbiciel i osobisty dostawca głasków ♡
  </div>
</main>

<script>
  function createPuffyHeart() {
    const heart = document.createElement('div');
    heart.className = 'heart';
    heart.innerHTML = ['💗','💖','🌸','🐾','♡','💞','🌷','✿','🐱','🫶','🍓','🎀'][Math.floor(Math.random()*12)];
    
    heart.style.left = Math.random() * 100 + 'vw';
    heart.style.animationDuration = (Math.random() * 4 + 5.5) + 's';
    heart.style.fontSize = (Math.random() * 18 + 16) + 'px';
    
    document.getElementById('hearts').appendChild(heart);
    
    setTimeout(() => heart.remove(), 11000);
  }

  setInterval(createPuffyHeart, 280);

  // od razu dużo słodyczy na wejściu
  for(let i = 0; i < 20; i++) {
    setTimeout(createPuffyHeart, i * 140);
  }
</script>
</body>
</html>

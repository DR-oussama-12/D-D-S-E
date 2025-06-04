
<html lang="ar">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>D-D-S-E</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body, html {
      height: 100%;
      overflow: hidden;
      font-family: Arial, sans-serif;
    }

    .video-background {
      position: fixed;
      top: 0;
      left: 0;
      min-width: 100%;
      min-height: 100%;
      z-index: -1;
      object-fit: cover;
    }

    .glow-button {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      padding: 20px 40px;
      font-size: 2rem;
      color: #00ff00;
      text-decoration: none;
      border: 2px solid #00ff00;
      border-radius: 10px;
      text-align: center;
      background: transparent;
      box-shadow: 0 0 10px #00ff00, 0 0 20px #00ff00, 0 0 30px #00ff00;
      animation: pulse 2s infinite ease-in-out;
      transition: background 0.3s, color 0.3s;
      cursor: pointer;
    }

    .glow-button:hover {
      background: #00ff00;
      color: black;
      box-shadow: 0 0 20px #00ff00, 0 0 40px #00ff00, 0 0 60px #00ff00;
    }

    @keyframes pulse {
      0%, 100% {
        box-shadow: 0 0 10px #00ff00, 0 0 20px #00ff00;
      }
      50% {
        box-shadow: 0 0 20px #00ff00, 0 0 40px #00ff00;
      }
    }
  </style>
</head>
<body>
  <!-- خلفية الفيديو -->
  <video autoplay muted loop class="video-background">
    <source src="cyber security stock footage - free video cyber security background.mp4" type="video/mp4">
    متصفحك لا يدعم تشغيل الفيديو.
  </video>

  <!-- زر الترحيب -->
  <a href="page 1.html" class="glow-button" id="glowBtn">Welcome to my world</a>

  <!-- الصوت -->
  <audio id="hoverSound" src="Binary Code - Interface Sound Effects  Sci-Fi Computer Beeps & Data Processing Sounds.mp3" preload="auto"></audio>

  <!-- البرمجة -->
  <script>
    const btn = document.getElementById('glowBtn');
    const sound = document.getElementById('hoverSound');

    // شغّل الصوت عند التحريك أو الضغط
    btn.addEventListener('mouseover', () => {
      sound.currentTime = 0;
      sound.play();
    });

    btn.addEventListener('click', () => {
      sound.currentTime = 0;
      sound.play();
    });
  </script>
</body>
</html>

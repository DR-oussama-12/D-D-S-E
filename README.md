<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>     D     -     D     -     S     -     E     </title>
  <script src="https://cdn.emailjs.com/dist/email.min.js"></script>
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

    .contact-form {
      position: absolute;
      bottom: 30px;
      right: 30px;
      background-color: rgba(0, 0, 0, 0.7);
      padding: 20px;
      border: 2px solid #00ff00;
      border-radius: 10px;
      color: #00ff00;
      width: 300px;
    }

    .contact-form input,
    .contact-form textarea,
    .contact-form button {
      width: 100%;
      margin-top: 10px;
      padding: 10px;
      background-color: black;
      color: #00ff00;
      border: 1px solid #00ff00;
      border-radius: 5px;
    }

    .contact-form button:hover {
      background-color: #00ff00;
      color: black;
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

  <!-- نموذج خدمة العملاء -->
  <div class="contact-form">
    <h3>خدمة العملاء</h3>
    <form id="contactForm">
      <input type="text" name="from_name" placeholder="الاسم" required>
      <input type="email" name="reply_to" placeholder="البريد الإلكتروني" required>
      <textarea name="message" rows="4" placeholder="رسالتك..." required></textarea>
      <button type="submit">إرسال</button>
    </form>
  </div>

  <!-- الصوت -->
  <audio id="hoverSound" src="Binary Code - Interface Sound Effects  Sci-Fi Computer Beeps & Data Processing Sounds.mp3" preload="auto"></audio>

  <script>
    // صوت التفاعل
    const btn = document.getElementById('glowBtn');
    const sound = document.getElementById('hoverSound');

    btn.addEventListener('mouseover', () => {
      sound.currentTime = 0;
      sound.play();
    });

    btn.addEventListener('click', () => {
      sound.currentTime = 0;
      sound.play();
    });

    // إعداد EmailJS
    (function(){
      emailjs.init("YOUR_USER_ID"); // ← ضعه من EmailJS
    })();

    // إرسال النموذج
    document.getElementById('contactForm').addEventListener('submit', function(e) {
      e.preventDefault();
      emailjs.sendForm('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', this)
        .then(() => {
          alert("تم الإرسال بنجاح!");
          this.reset();
        }, (error) => {
          alert("حدث خطأ: " + JSON.stringify(error));
        });
    });
  </script>
</body>
</html>

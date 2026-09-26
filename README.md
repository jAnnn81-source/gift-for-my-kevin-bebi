# gift-for-my-kevin-bebi
happy anniversary 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>A Special Surprise For You, My Love! 💕</title>
  <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
  <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }
    body {
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(135deg, #ffe6eb 0%, #ffd1dc 100%);
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 20px;
      overflow-x: hidden;
      position: relative;
    }
    /* Floating Hearts Background */
    .heart {
      position: absolute;
      color: rgba(255, 105, 180, 0.3);
      font-size: 20px;
      animation: float 6s linear infinite;
      user-select: none;
    }
    @keyframes float {
      0% { transform: translateY(100vh) rotate(0deg); opacity: 1; }
      100% { transform: translateY(-10vh) rotate(360deg); opacity: 0; }
    }
    /* Main Container */
    .card-container {
      background: #ffffff;
      border-radius: 24px;
      box-shadow: 0 15px 35px rgba(230, 80, 115, 0.2);
      max-width: 480px;
      width: 100%;
      padding: 40px 30px;
      text-align: center;
      position: relative;
      z-index: 10;
      transition: transform 0.3s ease;
    }
    .card-container:hover {
      transform: translateY(-5px);
    }
    h1 {
      font-family: 'Dancing Script', cursive;
      font-size: 2.8rem;
      color: #e63946;
      margin-bottom: 10px;
    }
    p.subtitle {
      color: #6c757d;
      font-size: 1rem;
      margin-bottom: 25px;
    }
    /* Gift Box Icon / Initial State */
    .gift-box {
      font-size: 80px;
      cursor: pointer;
      margin: 20px 0;
      display: inline-block;
      animation: pulse 2s infinite;
      transition: transform 0.2s ease;
    }
    .gift-box:hover {
      transform: scale(1.1) rotate(5deg);
    }
    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.08); }
      100% { transform: scale(1); }
    }
    /* Reveal Button */
    .btn-reveal {
      background: linear-gradient(135deg, #ff4b2b, #ff416c);
      color: white;
      border: none;
      padding: 14px 32px;
      font-size: 1.1rem;
      font-weight: 600;
      border-radius: 50px;
      cursor: pointer;
      box-shadow: 0 8px 20px rgba(255, 65, 108, 0.4);
      transition: all 0.3s ease;
    }
    .btn-reveal:hover {
      background: linear-gradient(135deg, #ff416c, #ff4b2b);
      box-shadow: 0 12px 25px rgba(255, 65, 108, 0.6);
      transform: translateY(-2px);
    }
    /* Hidden Reveal Content */
    #reveal-content {
      display: none;
      animation: fadeIn 0.8s ease forwards;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(15px); }
      to { opacity: 1; transform: translateY(0); }
    }
    .voucher-card {
      background: #fff8f9;
      border: 2px dashed #ffb6c1;
      border-radius: 16px;
      padding: 25px;
      margin: 20px 0;
    }
    .voucher-title {
      font-size: 1.3rem;
      font-weight: 600;
      color: #333;
      margin-bottom: 8px;
    }
    .voucher-desc {
      font-size: 0.95rem;
      color: #555;
      margin-bottom: 20px;
      line-height: 1.5;
    }
    /* Groupon Redirect Button */
    .btn-claim {
      display: inline-block;
      background-color: #53a318; /* Groupon Green */
      color: #ffffff;
      text-decoration: none;
      padding: 14px 28px;
      font-size: 1.05rem;
      font-weight: 600;
      border-radius: 50px;
      box-shadow: 0 6px 18px rgba(83, 163, 24, 0.35);
      transition: all 0.3s ease;
    }
    .btn-claim:hover {
      background-color: #448813;
      box-shadow: 0 10px 22px rgba(83, 163, 24, 0.5);
      transform: translateY(-2px);
    }
    .love-note {
      font-family: 'Dancing Script', cursive;
      font-size: 1.5rem;
      color: #e63946;
      margin-top: 15px;
    }
  </style>
</head>
<body>

  <!-- Floating Hearts Animation -->
  <div id="hearts-container"></div>

  <div class="card-container">
    <!-- Initial Cover View -->
    <div id="cover-content">
      <h1>For My Wonderful Husband ❤️</h1>
      <p class="subtitle">I made a little surprise just for you. Ready to open it?</p>
      <div class="gift-box" onclick="revealGift()">🎁</div>
      <br>
      <button class="btn-reveal" onclick="revealGift()">Open Your Gift 💕</button>
    </div>

    <!-- Revealed Gift View -->
    <div id="reveal-content">
      <h1>Surprise, Babe! 🎉</h1>
      <p class="subtitle">Because you deserve something special!</p>
      
      <div class="voucher-card">
        <div class="voucher-title">🎟️ Your Gift Voucher</div>
        <p class="voucher-desc">
          I got us a little experience to enjoy together! Click the button below to claim and view your gift voucher.
        </p>
        <a href="https://www.groupon.com/gifts/VS-1b5b8bdfb64e5388d341d22390c9949e5ddc9ed6" target="_blank" class="btn-claim">
          🎁 Claim Your Groupon Gift
        </a>
      </div>

      <p class="love-note">I love you so much! xoxo</p>
    </div>
  </div>

  <script>
    // Create floating background hearts
    const heartsContainer = document.getElementById('hearts-container');
    for (let i = 0; i < 15; i++) {
      const heart = document.createElement('div');
      heart.classList.add('heart');
      heart.innerHTML = '❤️';
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.animationDuration = (Math.random() * 3 + 4) + 's';
      heart.style.animationDelay = (Math.random() * 5) + 's';
      heartsContainer.appendChild(heart);
    }

    // Reveal function with Confetti
    function revealGift() {
      document.getElementById('cover-content').style.display = 'none';
      document.getElementById('reveal-content').style.display = 'block';

      // Confetti burst
      confetti({
        particleCount: 100,
        spread: 70,
        origin: { y: 0.6 }
      });
    }
  </script>
</body>
</html>

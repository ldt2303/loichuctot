<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <title>Lời chúc THPTQG</title>
  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(120deg, #ffe6f0, #e0f7ff, #fff7e6);
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: 'Comic Sans MS', cursive;
      overflow: hidden;
    }

    .container {
      text-align: center;
      padding: 30px;
    }

    .open-btn {
      padding: 15px 30px;
      font-size: 1.5rem;
      border: none;
      border-radius: 20px;
      background: linear-gradient(to right, #ff9a9e, #fad0c4);
      color: white;
      cursor: pointer;
      box-shadow: 0 0 20px #ff69b4;
      transition: transform 0.2s;
    }

    .open-btn:hover {
      transform: scale(1.05);
    }

    .message {
      margin-top: 40px;
      font-size: 2rem;
      font-weight: bold;
      display: none;
      animation: typing 4s steps(40, end), blink-caret 0.75s step-end infinite;
      white-space: nowrap;
      overflow: hidden;
      border-right: 3px solid pink;
      max-width: 100%;
    }

    @keyframes typing {
      from { width: 0 }
      to { width: 100% }
    }

    @keyframes blink-caret {
      from, to { border-color: transparent }
      50% { border-color: pink; }
    }

    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background-color: pink;
      transform: rotate(45deg);
      animation: float 6s linear infinite;
    }

    .heart::before,
    .heart::after {
      content: '';
      position: absolute;
      width: 20px;
      height: 20px;
      background-color: pink;
      border-radius: 50%;
    }

    .heart::before {
      top: -10px;
      left: 0;
    }

    .heart::after {
      left: -10px;
      top: 0;
    }

    @keyframes float {
      0% {
        transform: translateY(0) rotate(45deg);
        opacity: 1;
      }
      100% {
        transform: translateY(-100vh) rotate(45deg);
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <button class="open-btn" onclick="showMessage()">🎁 Mở lời chúc</button>
    <div id="message" class="message">💖 Chúc em vượt qua kỳ thi THPTQG thật tự tin, bình tĩnh và đạt kết quả như mong đợi nhé! 💖</div>
  </div>

  <script>
    function showMessage() {
      const message = document.getElementById("message");
      message.style.display = "inline-block";

      const btn = document.querySelector(".open-btn");
      btn.disabled = true;
      btn.style.display = "none";

      // Tạo hiệu ứng trái tim bay
      setInterval(() => {
        const heart = document.createElement("div");
        heart.classList.add("heart");
        heart.style.left = Math.random() * window.innerWidth + "px";
        heart.style.animationDuration = 3 + Math.random() * 3 + "s";
        document.body.appendChild(heart);
        setTimeout(() => heart.remove(), 6000);
      }, 300);
    }
  </script>
</body>
</html>

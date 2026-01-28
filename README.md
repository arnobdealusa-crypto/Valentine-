# Valentine
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Will You Be My Valentine?</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #ff758c, #ff7eb3);
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      color: #fff;
      text-align: center;
    }
    .card {
      background: rgba(255, 255, 255, 0.15);
      backdrop-filter: blur(10px);
      border-radius: 20px;
      padding: 40px 30px;
      max-width: 420px;
      box-shadow: 0 20px 40px rgba(0,0,0,0.2);
    }
    h1 {
      font-size: 2.2rem;
      margin-bottom: 10px;
    }
    p {
      font-size: 1.1rem;
      margin-bottom: 25px;
    }
    .heart {
      font-size: 3rem;
      animation: pulse 1.5s infinite;
      margin-bottom: 15px;
    }
    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.2); }
      100% { transform: scale(1); }
    }
    button {
      border: none;
      padding: 12px 22px;
      font-size: 1rem;
      border-radius: 30px;
      cursor: pointer;
      margin: 10px;
    }
    .yes {
      background: #fff;
      color: #ff4f7a;
      font-weight: bold;
    }
    .no {
      background: transparent;
      color: #fff;
      border: 2px solid #fff;
      position: relative;
    }
    .message {
      margin-top: 20px;
      font-size: 1.2rem;
      display: none;
    }
  </style>
</head>
<body>
  <div class="card">
    <div class="heart">❤️</div>
    <h1>Hey, my love</h1>
    <p>
      Every day with you means more to me than words can say.<br />
      So I just have one important question…
    </p>
    <h2>Will you be my Valentine? 💘</h2>

    <div>
      <button class="yes" onclick="sayYes()">Yes 💕</button>
      <button class="no" onmouseover="moveButton(this)">No 🙈</button>
    </div>

    <div class="message" id="message">
      You just made me the happiest person ever 😭❤️<br />
      I love you so much.
    </div>
  </div>

  <script>
    function sayYes() {
      document.getElementById('message').style.display = 'block';
    }

    function moveButton(btn) {
      const x = Math.random() * 200 - 100;
      const y = Math.random() * 200 - 100;
      btn.style.transform = `translate(${x}px, ${y}px)`;
    }
  </

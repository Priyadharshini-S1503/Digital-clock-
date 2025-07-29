<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Digital Clock</title>
  <style>
    body {
      background: #1a1a1a;
      color: #00ffcc;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      font-family: "Courier New", Courier, monospace;
      margin: 0;
    }

    .clock {
      font-size: 60px;
      padding: 20px 40px;
      background: #000;
      border: 3px solid #00ffcc;
      border-radius: 15px;
      box-shadow: 0 0 20px #00ffcc;
    }
  </style>
</head>
<body>
  <div class="clock" id="clock">00:00:00</div>

  <script>
    function updateClock() {
      const now = new Date();
      let hours = now.getHours().toString().padStart(2, "0");
      let minutes = now.getMinutes().toString().padStart(2, "0");
      let seconds = now.getSeconds().toString().padStart(2, "0");
      document.getElementById("clock").textContent = `${hours}:${minutes}:${seconds}`;
    }

    setInterval(updateClock, 1000);
    updateClock(); // initial call
  </script>
</body>
</html># Digital-clock-

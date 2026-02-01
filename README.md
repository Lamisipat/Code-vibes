# Code-vibes
#Just texting out

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Be My Valentine 💘</title>

  <style>
    body {
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      overflow: hidden;
    }

    .card {
      background: white;
      padding: 30px 40px;
      border-radius: 20px;
      text-align: center;
      box-shadow: 0 10px 30px rgba(0,0,0,0.25);
    }

    h1 {
      color: #e63946;
    }

    .buttons {
      margin-top: 30px;
      position: relative;
      height: 100px;
    }

    button {
      padding: 12px 28px;
      font-size: 18px;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      position: absolute;
      transition: transform 0.2s;
    }

    #yes {
      background: #38b000;
      color: white;
      left: 42%;
    }

    #no {
      background: #e63946;
      color: white;
      left: 10%;
    }

    #celebration {
      display: none;
      margin-top: 20px;
    }

    img {
      width: 220px;
    }
  </style>
</head>

<body>

  <div class="card">
    <h1>Will you be my Valentine? 💖</h1>

    <div class="buttons">
      <button id="yes">Yes 💘</button>
      <button id="no">No 💔</button>
    </div>

    <div id="celebration">
      <h2>MISSION SUCCESS 🎉😎</h2>
      <img src="https://media.giphy.com/media/26BRv0ThflsHCqDrG/giphy.gif" alt="Celebration">
    </div>
  </div>

  <script>
    const noBtn = document.getElementById("no");
    const yesBtn = document.getElementById("yes");
    const celebration = document.getElementById("celebration");

    // NO button repels like positive magnets
    noBtn.addEventListener("mouseover", () => {
      const x = Math.random() * 300;
      const y = Math.random() * 80;
      noBtn.style.transform = `translate(${x}px, ${y}px)`;
    });

    // YES button logic
    yesBtn.addEventListener("click", () => {
      celebration.style.display = "block";

      const message = encodeURIComponent(
        "MISSION SUCCESS 😎💘 — They said YES!"
      );

      // 🔴 CHANGE THIS NUMBER TO YOUR WHATSAPP
      window.open(
        `https://wa.me/233592031964?text=${message}`,
        "_blank"
      );
    });
  </script>

</body>
</html>

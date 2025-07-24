<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Jawab Jujur Ya 😁</title>
  <style>
    body {
      text-align: center;
      margin-top: 100px;
      font-family: 'Comic Sans MS', cursive;
      background-color: #e0ffff;
    }
    h1 {
      color: #ff4500;
    }
    #yesBtn, #noBtn {
      padding: 10px 20px;
      font-size: 18px;
      border: none;
      cursor: pointer;
      border-radius: 10px;
      margin: 10px;
    }
    #yesBtn {
      background-color: #90ee90;
    }
    #noBtn {
      background-color: #add8e6;
      position: absolute;
    }
  </style>
</head>
<body>

  <h1>Apakah kamu pendek? 🤭</h1>
  <button id="yesBtn" onclick="playYes()">Iya 😅</button>
  <button id="noBtn" onclick="playNo()">Tidak 😤</button>

  <!-- Audio -->
  <audio id="audioYes" src="https://www.myinstants.com/media/sounds/kids-cheering.mp3"></audio>
  <audio id="audioNo" src="https://www.myinstants.com/media/sounds/anime-laugh.mp3"></audio>

  <script>
    const noBtn = document.getElementById('noBtn');

    function moveButton() {
      const x = Math.random() * (window.innerWidth - noBtn.offsetWidth);
      const y = Math.random() * (window.innerHeight - noBtn.offsetHeight);
      noBtn.style.left = x + 'px';
      noBtn.style.top = y + 'px';
    }

    function playYes() {
      document.getElementById('audioYes').play();
      alert('Hehehe ngakuu 😆');
    }

    function playNo() {
      document.getElementById('audioNo').play();
      alert('Yahh ngga bisa ngeles 😝');
    }

    noBtn.addEventListener('mouseover', moveButton);
  </script>

</body>
</html>

<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Proposta de Casamento</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
    }
    .container {
      margin-top: 100px;
    }
    .btn {
      display: inline-block;
      padding: 10px 20px;
      margin: 10px;
      border: 2px solid #000;
      border-radius: 5px;
      text-decoration: none;
      color: #000;
      font-weight: bold;
      cursor: pointer;
    }
    .btn:hover {
      background-color: #000;
      color: #fff;
    }
    .hearts {
      position: absolute;
      display: none;
      pointer-events: none;
    }
    .heart {
      width: 20px;
      height: 20px;
      position: absolute;
      background: url('https://emojicdn.elk.sh/❤️');
      background-size: cover;
      animation: heart-animation 1s ease-out;
    }
    @keyframes heart-animation {
      0% {
        transform: scale(1);
        opacity: 1;
      }
      100% {
        transform: scale(1.5);
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Quer casar comigo?</h1>
    <a href="#" onclick="showHearts()" class="btn">Sim</a>
    <a href="#" onclick="alert('Que pena! Mas obrigado por considerar.')" class="btn">Não</a>
  </div>
  <div class="hearts"></div>

  <script>
    function showHearts() {
      var container = document.querySelector('.hearts');
      for (var i = 0; i < 10; i++) {
        var heart = document.createElement('div');
        heart.className = 'heart';
        heart.style.left = Math.random() * 90 + '%';
        heart.style.animationDuration = Math.random() * 2 + 1 + 's';
        container.appendChild(heart);
      }
      container.style.display = 'block';
      setTimeout(function() {
        container.style.display = 'none';
      }, 2000);
    }
  </script>
</body>
</html>

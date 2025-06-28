<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Page protégée</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f4f4;
      text-align: center;
      padding-top: 100px;
    }
    input, button {
      padding: 10px;
      font-size: 18px;
      margin: 5px;
    }
    #secretContent {
      display: none;
      margin-top: 40px;
      padding: 20px;
      background-color: #e1ffe1;
      border-radius: 10px;
      width: 80%;
      margin-left: auto;
      margin-right: auto;
    }
  </style>
</head>
<body>

  <h1>🔐 Accès réservé</h1>
  <p>Veuillez entrer le code d'accès :</p>

  <input type="text" id="codeInput" placeholder="Code d'accès">
  <button onclick="checkCode()">Valider</button>

  <div id="secretContent">
    <h2>✅ Bienvenue !</h2>
    <p>Voici votre contenu protégé :</p>
    <a href="https://www.google.com" target="_blank">Lien secret</a>
  </div>

  <script>
    function checkCode() {
      const input = document.getElementById("codeInput").value.trim();
      const validCode = "1234VIP";

      if (input === validCode) {
        document.getElementById("secretContent").style.display = "block";
      } else {
        alert("❌ Code incorrect");
      }
    }
  </script>

</body>
</html>

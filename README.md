<!DOCTYPE html>
<html lang="fi">
<head>
  <meta charset="UTF-8">
  <title>Super Analyysi 3000</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(120deg, #f093fb, #f5576c);
      color: white;
      text-align: center;
      padding-top: 100px;
    }
    input, button {
      padding: 10px;
      font-size: 16px;
      border-radius: 8px;
      border: none;
      margin: 5px;
    }
    button {
      background: #333;
      color: white;
      cursor: pointer;
    }
    #result {
      margin-top: 30px;
      font-size: 22px;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <h1>🤖 Super Analyysi 3000</h1>
  <p>Syötä nimesi ja anna tekoälyn kertoa totuus!</p>
  <input type="text" id="name" placeholder="Kirjoita nimesi">
  <button onclick="analysoi()">Analysoi</button>
  <div id="result"></div>

  <script>
    const tulokset = [
      "Sinun älykkyystasosi vastaa saunavihdan tasoa.",
      "Olet virallisesti maailman huonoin piilottelija.",
      "Analyysi: 99% todennäköisyydellä syöt viimeisen nakin.",
      "Tietokanta kertoo: sinulla on +10 karisma, -50 onni.",
      "Olet testin mukaan täydellinen... jos olet peruna.",
      "Arvostelumme: 2/10, söisit uudestaan.",
      "Sinulla on salainen kyky kadottaa kaikki kuulokkeet.",
      "Olet niin erityinen, että jopa Excel kaatuu sinua ajatellessa."
    ];

    function analysoi() {
      const nimi = document.getElementById("name").value;
      if (nimi.trim() === "") {
        document.getElementById("result").innerText = "Syötä ensin nimi, muuten tekoäly ei toimi! 🤔";
        return;
      }
      const satunnainen = tulokset[Math.floor(Math.random() * tulokset.length)];
      document.getElementById("result").innerText = nimi + ", " + satunnainen;
    }
  </script>
</body>
</html>

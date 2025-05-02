# Ascii-kodlay-c-
Bu depo metinleri ASCII rakamları ile kodlar.
<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ASCII Kodlayıcı</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      padding: 20px;
      background: #f0f0f0;
    }
    textarea, input {
      width: 100%;
      padding: 10px;
      margin-top: 10px;
      font-size: 16px;
    }
    button {
      padding: 10px 20px;
      margin-top: 10px;
      font-size: 16px;
      cursor: pointer;
    }
    .output {
      margin-top: 20px;
      padding: 10px;
      background: #fff;
      border: 1px solid #ccc;
      white-space: pre-wrap;
    }
  </style>
</head>
<body>
  <h2>ASCII Kodlayıcı / Çözücü</h2>

  <label for="inputText">Mesajınızı yazın:</label>
  <textarea id="inputText" rows="3" placeholder="Örn: Merhaba Dünya!"></textarea>
  <button onclick="encodeASCII()">ASCII Kodla</button>
  <button onclick="decodeASCII()">ASCII Çöz</button>

  <div class="output" id="output"></div>

  <script>
    function encodeASCII() {
      const text = document.getElementById("inputText").value;
      const encoded = text.split('').map(c => c.charCodeAt(0)).join(' ');
      document.getElementById("output").textContent = encoded;
    }

    function decodeASCII() {
      const text = document.getElementById("inputText").value;
      const decoded = text.split(' ').map(code => String.fromCharCode(code)).join('');
      document.getElementById("output").textContent = decoded;
    }
  </script>
</body>
</html>

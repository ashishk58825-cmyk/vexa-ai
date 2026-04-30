<!DOCTYPE html>
<html lang="hi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Vexa AI</title>
  <style>
    body{
      margin:0;
      background:#111827;
      color:white;
      font-family:Arial,sans-serif;
      display:flex;
      justify-content:center;
      align-items:center;
      height:100vh;
    }
    .card{
      text-align:center;
      background:#1f2937;
      padding:30px;
      border-radius:20px;
      box-shadow:0 0 20px rgba(0,0,0,.4);
      width:320px;
    }
    .avatar{
      width:140px;
      height:140px;
      border-radius:50%;
      background:#374151;
      margin:0 auto 20px;
      display:flex;
      justify-content:center;
      align-items:center;
      font-size:50px;
      font-weight:bold;
    }
    button{
      margin-top:20px;
      padding:12px 20px;
      border:none;
      border-radius:12px;
      background:#7c3aed;
      color:white;
      font-size:16px;
      cursor:pointer;
    }
  </style>
</head>
<body>

  <div class="card">
    <div class="avatar">V</div>
    <h1>Vexa AI</h1>
    <p id="text">नमस्ते आशिष, मैं Vexa हूँ।</p>
    <button id="btn">Hey Vexa</button>
  </div>

  <script>
    document.getElementById("btn").addEventListener("click", function () {
      const text = "हाँ आशिष, बताओ।";
      document.getElementById("text").innerText = text;

      const speech = new SpeechSynthesisUtterance(text);
      speech.lang = "hi-IN";
      window.speechSynthesis.speak(speech);
    });
  </script>

</body>
</html>

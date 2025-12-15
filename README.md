<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Buat Kamu</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #ffdde1, #ee9ca7);
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .card {
      background: white;
      padding: 30px;
      border-radius: 20px;
      width: 90%;
      max-width: 400px;
      text-align: center;
      box-shadow: 0 10px 30px rgba(0,0,0,0.15);
      animation: fadeIn 1.5s ease;
    }
    h1 {
      color: #ee5a7a;
      font-size: 26px;
    }
    p {
      color: #444;
      font-size: 16px;
      line-height: 1.6;
    }
    button {
      margin: 10px;
      padding: 10px 20px;
      border: none;
      border-radius: 30px;
      font-size: 16px;
      cursor: pointer;
      transition: 0.3s;
    }
    .yes {
      background: #ee5a7a;
      color: white;
    }
    .yes:hover {
      background: #d94c6a;
    }
    .no {
      background: #ddd;
    }
    .no:hover {
      background: #bbb;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body>
  <div class="card">
    <h1>Hai Kamu 🌷</h1>
    <p>
      Kita satu kelas, sudah cukup lama saling kenal.
      Jujur saja, perasaan ini baru aku sadari di semester 7 ini.
      Bukan karena tiba-tiba, tapi karena makin lama aku makin nyaman
      setiap ngobrol dan satu ruang sama kamu.
    </p>
    <p><strong>Aku cuma mau jujur. Kalau suatu hari kamu mau melihat aku lebih dari sekadar teman, aku akan senang. Kalau tidak pun, aku tetap menghargai kamu dan pertemanan kita.</strong></p>
    <button class="yes" onclick="yesAnswer()">Iya 😳💖</button>
    <button class="no" id="noBtn">Tidak 🙃</button>
  </div>

  <script>
    function yesAnswer() {
      document.body.innerHTML = `
        <div style=\"text-align:center; color:white;\">
          <h1>YES! 🎉✨</h1>
          <p>Plot twist terbaik semester ini.</p>
          <p>Makasih sudah berani bilang iya. Aku bakal jaga ini pelan-pelan.</p>
        </div>`;
    }

    const noBtn = document.getElementById('noBtn');
    let moveCount = 0;
    noBtn.addEventListener('mouseover', () => {
      moveCount++;
      const x = Math.random() * 200 - 100;
      const y = Math.random() * 200 - 100;
      noBtn.style.transform = `translate(${x}px, ${y}px)`;
      if (moveCount > 5) {
        noBtn.innerText = 'Yakin? 😅';
      }
    });
  </script>
</body>
</html>

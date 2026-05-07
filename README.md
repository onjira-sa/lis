<!DOCTYPE html>
<html lang="th">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>เว็บใบ้หวย</title>

  <style>
    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      font-family:sans-serif;
    }

    body{
      background:#0f0f0f;
      color:white;
      display:flex;
      justify-content:center;
      align-items:center;
      min-height:100vh;
      padding:20px;
    }

    .card{
      background:#1a1a1a;
      width:100%;
      max-width:500px;
      border-radius:25px;
      padding:30px;
      text-align:center;
      box-shadow:0 0 20px rgba(0,0,0,0.5);
    }

    h1{
      margin-bottom:10px;
      font-size:40px;
    }

    p{
      color:#aaa;
      margin-bottom:25px;
    }

    .box{
      background:#262626;
      border-radius:20px;
      padding:20px;
      margin-bottom:15px;
    }

    .label{
      color:#bbb;
      margin-bottom:10px;
      font-size:18px;
    }

    .number{
      font-size:42px;
      font-weight:bold;
    }

    .two{
      color:#ffd700;
    }

    .three{
      color:#ff69b4;
    }

    .main{
      color:#00e5ff;
    }

    button{
      width:100%;
      padding:15px;
      border:none;
      border-radius:15px;
      background:white;
      color:black;
      font-size:18px;
      font-weight:bold;
      cursor:pointer;
      transition:0.3s;
      margin-top:10px;
    }

    button:hover{
      transform:scale(1.03);
    }

    .footer{
      margin-top:20px;
      color:#666;
      font-size:12px;
    }
  </style>
</head>

<body>

  <div class="card">
    <h1>✨ เว็บใบ้หวย ✨</h1>
    <p>สุ่มเลขเพื่อความบันเทิง</p>

    <div class="box">
      <div class="label">เลข 2 ตัว</div>
      <div class="number two" id="twoDigit">00</div>
    </div>

    <div class="box">
      <div class="label">เลข 3 ตัว</div>
      <div class="number three" id="threeDigit">000</div>
    </div>

    <div class="box">
      <div class="label">เลขเด่น</div>
      <div class="number main" id="mainNumber">0 - 0 - 0</div>
    </div>

    <button onclick="generateNumbers()">
      🎲 สุ่มเลขใหม่
    </button>

    <div class="footer">
      เว็บไซต์นี้จัดทำขึ้นเพื่อความบันเทิงเท่านั้น
    </div>
  </div>

  <script>
    function generateNumbers() {

      let two = Math.floor(Math.random() * 90) + 10;
      let three = Math.floor(Math.random() * 900) + 100;

      let a = Math.floor(Math.random() * 10);
      let b = Math.floor(Math.random() * 10);
      let c = Math.floor(Math.random() * 10);

      document.getElementById("twoDigit").innerText = two;
      document.getElementById("threeDigit").innerText = three;
      document.getElementById("mainNumber").innerText = a + " - " + b + " - " + c;
    }

    generateNumbers();
  </script>

</body>
</html>

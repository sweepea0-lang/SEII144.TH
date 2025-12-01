<!DOCTYPE html>
<html lang="th">
<head>
  <meta charset="UTF-8">
  <title>หน้าโปร / เซลเพจ</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
</head>
<body style="background:#020617;margin:0;font-family:system-ui,sans-serif;">

  <!-- กล่องแจ็คพอต --------------------------------------------------- -->
  <div id="jackpot-box"></div>

  <script>
    // ฟังก์ชันสุ่มตัวเลขใช้งานร่วมกันทุกส่วน
    function rand(min, max) {
      return Math.floor(Math.random() * (max - min + 1)) + min;
    }

    // แจ็คพอต
    var lastJackpot = null;

    function getNewJackpot() {
      var num = rand(10000, 300000);
      while (num === lastJackpot) {
        num = rand(10000, 300000);
      }
      lastJackpot = num;
      return num;
    }

    function formatNumber(num) {
      return num.toLocaleString("th-TH");
    }

    function formatDate() {
      var d = new Date();
      var thMonths = ["ม.ค.","ก.พ.","มี.ค.","เม.ย.","พ.ค.","มิ.ย.","ก.ค.","ส.ค.","ก.ย.","ต.ค.","พ.ย.","ธ.ค."];

      var day = d.getDate();
      var month = thMonths[d.getMonth()];
      var year = d.getFullYear() + 543;
      var time =
        d.getHours().toString().padStart(2, "0") + ":" +
        d.getMinutes().toString().padStart(2, "0") + ":" +
        d.getSeconds().toString().padStart(2, "0");

      return day + " " + month + " " + year + " " + time;
    }

    var jackpotBox = document.getElementById("jackpot-box");

    function renderJackpot() {
      var jackpotAmount = getNewJackpot();

      var html =
        '<div style="max-width:700px;margin:15px auto;padding:25px 20px;background:#0f3d31;color:#fff;border-radius:20px;text-align:center;box-shadow:0 8px 20px rgba(0,0,0,0.25);">' +
          '<div style="font-size:20px;font-weight:700;color:#facc15;">🏆 แจ็คพอตล่าสุด 🏆</div>' +
          '<div style="font-size:44px;font-weight:900;margin:10px 0;color:#ffffff;text-shadow:0 0 10px rgba(255,255,255,0.7);">' +
            formatNumber(jackpotAmount) + ' บาท</div>' +
          '<div style="font-size:14px;color:#cbd5e1;">อัปเดตล่าสุดเมื่อ ' + formatDate() + '</div>' +
        '</div>';

      jackpotBox.innerHTML = html;
    }

    renderJackpot();
    setInterval(renderJackpot, 5000);
  </script>

  <!-- SLIDER โลโก้ค่ายเกม --------------------------------------------------- -->
  <div id="provider-slider" style="
    max-width:900px;
    margin:15px auto;
    padding:10px;
    background:#0d3b31;
    border-radius:22px;
    overflow:hidden;
    box-shadow:0 8px 20px rgba(0,0,0,0.35);
    position:relative;
    white-space:nowrap;
  ">
    <div id="provider-track" style="
      display:inline-flex;
      align-items:center;
      white-space:nowrap;
    ">

      <!-- dreamgame -->
      <div style="min-width:180px;margin:0 8px;padding:10px 18px;border-radius:18px;
        background:rgba(0,0,0,0.25);display:flex;align-items:center;justify-content:center;">
        <img src="https://img2.pic.in.th/pic/dream6e317e1af3ae9e20.png"
             style="max-width:160px;max-height:60px;object-fit:contain;">
      </div>

      <!-- nolimit -->
      <div style="min-width:180px;margin:0 8px;padding:10px 18px;border-radius:18px;
        background:rgba(0,0,0,0.25);display:flex;align-items:center;justify-content:center;">
        <img src="https://img2.pic.in.th/pic/nolimit206913862165258a.png"
             style="max-width:160px;max-height:60px;object-fit:contain;">
      </div>

      <!-- joker -->
      <div style="min-width:180px;margin:0 8px;padding:10px 18px;border-radius:18px;
        background:rgba(0,0,0,0.25);display:flex;align-items:center;justify-content:center;">
        <img src="https://img5.pic.in.th/file/secure-sv1/jokerd99eb847c4171248.png"
             style="max-width:160px;max-height:60px;object-fit:contain;">
      </div>

      <!-- jili -->
      <div style="min-width:180px;margin:0 8px;padding:10px 18px;border-radius:18px;
        background:rgba(0,0,0,0.25);display:flex;align-items:center;justify-content:center;">
        <img src="https://img5.pic.in.th/file/secure-sv1/jili752a3c379bf8df1f.png"
             style="max-width:160px;max-height:60px;object-fit:contain;">
      </div>

      <!-- sexy -->
      <div style="min-width:180px;margin:0 8px;padding:10px 18px;border-radius:18px;
        background:rgba(0,0,0,0.25);display:flex;align-items:center;justify-content:center;">
        <img src="https://img2.pic.in.th/pic/sexyfceecb5e13b29644.png"
             style="max-width:160px;max-height:60px;object-fit:contain;">
      </div>

      <!-- sa -->
      <div style="min-width:180px;margin:0 8px;padding:10px 18px;border-radius:18px;
        background:rgba(0,0,0,0.25);display:flex;align-items:center;justify-content:center;">
        <img src="https://img2.pic.in.th/pic/sad80f0f406967d5c7.png"
             style="max-width:160px;max-height:60px;object-fit:contain;">
      </div>

      <!-- pg -->
      <div style="min-width:180px;margin:0 8px;padding:10px 18px;border-radius:18px;
        background:rgba(0,0,0,0.25);display:flex;align-items:center;justify-content:center;">
        <img src="https://img5.pic.in.th/file/secure-sv1/pg4aa31cb2a8fe009f.png"
             style="max-width:160px;max-height:60px;object-fit:contain;">
      </div>

      <!-- wm -->
      <div style="min-width:180px;margin:0 8px;padding:10px 18px;border-radius:18px;
        background:rgba(0,0,0,0.25);display:flex;align-items:center;justify-content:center;">
        <img src="https://img5.pic.in.th/file/secure-sv1/wm0c0e1b5ec6db6f54.png"
             style="max-width:160px;max-height:60px;object-fit:contain;">
      </div>

    </div>
  </div>

  <script>
    (function() {
      var slider = document.getElementById("provider-slider");
      var track = document.getElementById("provider-track");

      // ทำซ้ำโลโก้ 2 รอบ (เพื่อทำ infinite loop)
      track.innerHTML = track.innerHTML + track.innerHTML

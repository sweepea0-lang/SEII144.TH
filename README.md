<div id="jackpot-box"></div>

<script>
  // สุ่มตัวเลขช่วง และไม่ให้ซ้ำกับค่าก่อนหน้า
  var lastJackpot = null;

  function rand(min, max) {
    return Math.floor(Math.random() * (max - min + 1)) + min;
  }

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

  var box = document.getElementById("jackpot-box");

  function renderJackpot() {
    var jackpotAmount = getNewJackpot();

    var html =
      '<div style="max-width:700px;margin:15px auto;padding:25px 20px;background:#0f3d31;color:#fff;border-radius:20px;text-align:center;box-shadow:0 8px 20px rgba(0,0,0,0.25);">' +
        '<div style="font-size:20px;font-weight:700;color:#facc15;">🏆 แจ็คพอตล่าสุด 🏆</div>' +
        '<div style="font-size:44px;font-weight:900;margin:10px 0;color:#ffffff;text-shadow:0 0 10px rgba(255,255,255,0.7);">' +
          formatNumber(jackpotAmount) + ' บาท</div>' +
        '<div style="font-size:14px;color:#cbd5e1;">อัปเดตล่าสุดเมื่อ ' + formatDate() + '</div>' +
      '</div>';

    box.innerHTML = html;
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
  track.innerHTML = track.innerHTML + track.innerHTML;

  var speed = 1; // ความเร็วเลื่อน (px ต่อ tick)
  
  setInterval(function() {
    slider.scrollLeft += speed;

    if (slider.scrollLeft >= track.scrollWidth / 2) {
      slider.scrollLeft = 0; // reset เพื่อให้วนลูป
    }
  }, 15); // 15ms → ลื่นมาก
})();
</script>



<div id="withdraw-box"></div>

<script>
  function rand(min, max) {
    return Math.floor(Math.random() * (max - min + 1)) + min;
  }

  function formatDateTime(offsetSec) {
    var d = new Date();
    d.setSeconds(d.getSeconds() - offsetSec);

    var thMonths = ["ม.ค.","ก.พ.","มี.ค.","เม.ย.","พ.ค.","มิ.ย.",
                    "ก.ค.","ส.ค.","ก.ย.","ต.ค.","พ.ย.","ธ.ค."];

    var day = d.getDate();
    var month = thMonths[d.getMonth()];
    var year = d.getFullYear() + 543;

    var time =
      ("0" + d.getHours()).slice(-2) + ":" +
      ("0" + d.getMinutes()).slice(-2) + ":" +
      ("0" + d.getSeconds()).slice(-2);

    return day + " " + month + " " + year + " " + time;
  }

  function generateUniqueUsers(n) {
    var set = {};
    var arr = [];

    while (arr.length < n) {
      var nums = rand(10000, 99999);
      var id = "ztip10" + nums + "xx";
      if (!set[id]) {
        set[id] = true;
        arr.push(id);
      }
    }
    return arr;
  }

  // โลโก้ธนาคาร + วอเลท
  var bankLogos = [
    { name: "BBL",    type: "bank",   url: "https://img5.pic.in.th/file/secure-sv1/bblf40c39ca40eed0ba.png" },
    { name: "SCB",    type: "bank",   url: "https://img2.pic.in.th/pic/scb019a059f73100475.png" },
    { name: "KBANK",  type: "bank",   url: "https://img2.pic.in.th/pic/kbank7742b78e974ad389.png" },
    { name: "KTB",    type: "bank",   url: "https://img2.pic.in.th/pic/ktbd955d7cfe24294c4.png" },
    { name: "WALLET", type: "wallet", url: "https://img2.pic.in.th/pic/16e821711eaeac85e1fd523d38a57f75.png" }
  ];

  var statusList = [
    { text: "✔ โอนแล้ว", bg: "#022c22", border: "#22c55e", color: "#bbf7d0" },
    { text: "⏳ กำลังโอน", bg: "#422006", border: "#fbbf24", color: "#fef9c3" }
  ];

  var container = document.getElementById("withdraw-box");

  function renderCards() {
    var users = generateUniqueUsers(3);

    // เวลาแต่ละช่องไม่เท่ากัน และไม่เกินเวลาจริง
    var offsets = [
      rand(1, 7),
      rand(8, 14),
      rand(15, 20)
    ];

    var usedAmounts = {}; // กันยอดไม่ให้ซ้ำ
    var html = "";

    for (var i = 0; i < 3; i++) {

      var user = users[i];

      // เลือกธนาคาร/วอเลทแบบสุ่ม
      var bank = bankLogos[rand(0, bankLogos.length - 1)];

      // สุ่มยอดถอนตามประเภทธนาคาร
      var amountVal;
      do {
        if (bank.type === "wallet") {
          // วอเลท: ไม่เกิน 3,000
          amountVal = rand(200, 3000);
        } else {
          // ธนาคารปกติ: 200–100,000
          amountVal = rand(200, 100000);
        }
      } while (usedAmounts[amountVal]);
      usedAmounts[amountVal] = true;

      var amount = amountVal.toLocaleString("th-TH");
      var status = statusList[rand(0, statusList.length - 1)];
      var timeStamp = formatDateTime(offsets[i]);

      html +=
        '<div style="max-width:480px;margin:10px auto;padding:12px 16px;border-radius:14px;border:1px solid #d1a43a;background:#0b2a26;color:#f9fafb;font-family:system-ui, sans-serif;display:flex;align-items:center;gap:14px;box-shadow:0 4px 10px rgba(0,0,0,0.3);">' +

          '<div style="width:48px;height:48px;border-radius:12px;background:white;display:flex;align-items:center;justify-content:center;overflow:hidden;">' +
            '<img src="' + bank.url + '" style="width:40px;height:40px;object-fit:contain;">' +
          '</div>' +

          '<div style="flex:1;">' +
            '<div style="font-size:12px;color:#cbd5e1;">ยูส: <span style="font-weight:600;">' + user + '</span></div>' +
            '<div style="font-size:14px;margin:3px 0;">ยอดถอน: <span style="font-weight:700;color:#fbbf24;">' + amount + '</span> บาท</div>' +
            '<div style="font-size:11px;color:#94a3b8;">อัปเดตล่าสุด: ' + timeStamp + '</div>' +
          '</div>' +

          '<div style="padding:4px 10px;border-radius:999px;background:' + status.bg + ';border:1px solid ' + status.border + ';color:' + status.color + ';font-size:12px;display:flex;align-items:center;gap:5px;white-space:nowrap;">' +
            status.text +
          '</div>' +

        '</div>';
    }

    container.innerHTML = html;
  }

  renderCards();
  setInterval(renderCards, 4000);
</script>


<!-- กล่องแสดงจำนวนคนออนไลน์ (เวอร์ชันใหญ่) -->
<div style="
  max-width:380px;
  margin:20px auto;
  padding:18px 26px;
  background:#0b0b0b;
  border-radius:20px;
  border:2px solid #22c55e;
  box-shadow:0 0 12px rgba(34,197,94,0.45);
  color:#ffffff;
  font-family:system-ui,sans-serif;
  display:flex;
  align-items:center;
  justify-content:center;
  gap:14px;
">
  <span style="
    width:14px;
    height:14px;
    background:#22c55e;
    border-radius:50%;
    box-shadow:0 0 8px #22c55e;
  "></span>

  <span style="font-size:18px;font-weight:500;">ออนไลน์</span>

  <!-- ตัวเลขออนไลน์ -->
  <span id="online-number" style="
    font-size:26px;
    font-weight:800;
    color:#4ade80;
  ">
    180,000
  </span>

  <span style="font-size:18px;">คน</span>
</div>

<script>
  function rand(min, max) {
    return Math.floor(Math.random() * (max - min + 1)) + min;
  }

  var numberEl = document.getElementById("online-number");

  function updateOnline() {
    var amount = rand(180000, 180999);
    numberEl.innerHTML = amount.toLocaleString("th-TH");
  }

  updateOnline();
  setInterval(updateOnline, 4000);
</script>


<script src="//code.jivosite.com/widget/fmEuwcaXgH" async></script>

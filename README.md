

    header {
      text-align: center;
      margin-bottom: 30px;
    }

    header h1 {<form onsubmit="submitForm(event)">
  <div class="product">
    <input type="checkbox" name="product" value="ไอดี #1 - 4,600 บาท">
    <h3>🎮 ไอดี #1</h3>
    <div class="price">ราคา: 4,600 บาท</div>
    <a href="https://www.facebook.com/share/p/1HTcMRxooD/" target="_blank">ดูรายละเอียด</a>
  </div>

  <div class="product">
    <input type="checkbox" name="product" value="ไอดี #2 - 3,200 บาท">
    <h3>🎮 ไอดี #2</h3>
    <div class="price">ราคา: 3,200 บาท</div>
    <a href="#">ดูรายละเอียด</a>
  </div>

  <div class="product">
    <input type="checkbox" name="product" value="ไอดี #3 - 5,500 บาท">
    <h3>🎮 ไอดี #3</h3>
    <div class="price">ราคา: 5,500 บาท</div>
    <a href="#">ดูรายละเอียด</a>
  </div>

  <button type="submit" style="padding:10px 20px; margin-top:20px;">📤 ส่งรายการที่เลือก</button>
</form>

<script>
  function submitForm(event) {
    event.preventDefault();
    const selected = Array.from(document.querySelectorAll('input[name=\"product\"]:checked'))
      .map(cb => cb.value);

    if (selected.length === 0) {
      alert(\"กรุณาเลือกสินค้าที่ต้องการก่อนส่งค่ะ\");
      return;
    }

    const message = encodeURIComponent(\"ฉันต้องการซื้อ:\\n\" + selected.join(\"\\n\"));
    window.open(https://www.facebook.com/share/1AeBmdfGfA/?message=${message}, \"_blank\");
  }
</script>
      color: #5c6bc0;
      font-size: 36px;
    }

    .id-card {
      background-color: #ffffff;
      padding: 20px;
      border-radius: 16px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      max-width: 500px;
      margin: auto;
    }

    .id-card img {
      width: 100%;
      border-radius: 12px;
      margin-bottom: 15px;
    }

    .price {
      font-size: 24px;
      color: #e53935;
      margin: 10px 0;
    }

    .details {
      font-size: 16px;
      line-height: 1.6;
    }

    .contact {
      text-align: center;
      margin-top: 30px;
    }

    .contact a {
      background-color: #4267B2;
      color: white;
      text-decoration: none;
      padding: 10px 20px;
      border-radius: 8px;
      display: inline-block;
      font-size: 18px;
    }

    footer {
      text-align: center;
      margin-top: 40px;
      font-size: 14px;
      color: #888;
    }
  </style>
</head>
<body>

  <header>
    <h1>ร้านสายลม</h1>
    <p>ขายไอดีเกม Identity V</p>
  </header>

  <div class="id-card">
    <img src="https://via.placeholder.com/500x300.png?text=รูปสกิน+ไอดี" alt="สกินไอดี">
    <div class="price">ราคา: 2,200 บาท</div>
    <div class="details">
      <strong>สกิน:</strong> มีสกิน https://www.facebook.com/share/p/1HTcMRxooD/<br>
      <strong>ตัวละคร:</strong> ครบตัวหลัก พร้อมอัปเกรด<br>
      <strong>อื่น ๆ:</strong> ผูกเมลแล้ว พร้อมเปลี่ยนเมลได้<br>
    </div>
  </div>

  <div class="contact">
    <a href="https://www.facebook.com/share/1AeBmdfGfA/" target="_blank">ทักแชททาง Facebook</a>
  </div>

  <footer>
    © 2025 ร้านสายลม | จำหน่ายไอดีเกม Identity V
  </footer>

</body>
</html>
  <footer>
    © 2025 ร้านสายลม | จำหน่ายไอดีเกม Identity V
  </footer>

</body>
</html>

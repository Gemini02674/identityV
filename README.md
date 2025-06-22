<form onsubmit="submitForm(event)">
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

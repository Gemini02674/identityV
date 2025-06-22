<!DOCTYPE html>
<html lang="th">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>ร้านสายลม - ขายไอดี Identity V</title>
  <style>
    body {
      font-family: sans-serif;
      background: #f9f9f9;
      margin: 0;
      padding: 20px;
    }
    header {
      background: #cceeff;
      padding: 20px;
      text-align: center;
      border-radius: 10px;
    }
    .product {
      background: #fff;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      padding: 15px;
      margin: 20px 0;
    }
    .product img {
      max-width: 100%;
      border-radius: 10px;
    }
    .cart-button {
      background: #22c55e;
      color: white;
      border: none;
      padding: 10px 15px;
      margin-top: 10px;
      border-radius: 5px;
      cursor: pointer;
    }
    .contact {
      margin-top: 30px;
      text-align: center;
    }
    input, textarea {
      width: 100%;
      padding: 8px;
      margin-top: 5px;
      border-radius: 5px;
      border: 1px solid #ccc;
    }
  </style>
</head>
<body>

<header>
  <h1>ร้านสายลม</h1>
  <p>ขายไอดีเกม Identity V</p>
</header>

<h2>เพิ่มไอดีใหม่</h2>
<form id="addProductForm">
  <label>ชื่อไอดี:</label>
  <input type="text" id="name" required>

  <label>รายละเอียด:</label>
  <textarea id="description" required></textarea>

  <label>ราคา (บาท):</label>
  <input type="number" id="price" required>

  <label>อัปโหลดรูปสกิน:</label>
  <input type="file" id="image" accept="image/*" required>

  <button type="submit" class="cart-button">เพิ่มไอดี</button>
</form>

<h2>สินค้าในร้าน</h2>
<div id="productList"></div>

<div class="contact">
  <p>📞 ช่องทางติดต่อ: <a href="https://www.facebook.com/share/1AeBmdfGfA/" target="_blank">Facebook ร้านสายลม</a></p>
</div>

<script>
  const productList = document.getElementById('productList');
  const form = document.getElementById('addProductForm');

  form.addEventListener('submit', function(e) {
    e.preventDefault();

    const name = document.getElementById('name').value;
    const desc = document.getElementById('description').value;
    const price = document.getElementById('price').value;
    const imageFile = document.getElementById('image').files[0];

    const reader = new FileReader();
    reader.onload = function(event) {
      const newProduct = document.createElement('div');
      newProduct.classList.add('product');
      newProduct.innerHTML = `
        <img src="${event.target.result}" alt="skin">
        <h3>${name}</h3>
        <p>${desc}</p>
        <p><strong>ราคา:</strong> ${price} บาท</p>
        <button class="cart-button">เพิ่มในตะกร้า</button>
      `;
      productList.appendChild(newProduct);
      form.reset();
    };
    reader.readAsDataURL(imageFile);
  });
</script>

</body>
</html>

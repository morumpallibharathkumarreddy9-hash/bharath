<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>MiniShop</title>
  <style>
    * { box-sizing: border-box; }
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f5f5f5;
      color: #222;
    }
    header {
      background: #111;
      color: white;
      padding: 20px;
      display: flex;
      justify-content: space-between;
    }
    .products {
      max-width: 1000px;
      margin: 30px auto;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 20px;
      padding: 20px;
    }
    .product {
      background: white;
      padding: 15px;
      border-radius: 10px;
      text-align: center;
    }
    .product img {
      width: 100%;
      height: 180px;
      object-fit: cover;
      border-radius: 8px;
    }
    button {
      background: #111;
      color: white;
      border: 0;
      padding: 10px 15px;
      border-radius: 5px;
      cursor: pointer;
    }
    button:hover { background: #444; }
  </style>
</head>

<body>

<header>
  <strong>MiniShop</strong>
  <span>Cart: <b id="cart">0</b></span>
</header>

<main class="products">

  <div class="product">
    <img src="https://via.placeholder.com/300" alt="T-Shirt">
    <h3>T-Shirt</h3>
    <p>₹499</p>
    <button onclick="addToCart()">Add to Cart</button>
  </div>

  <div class="product">
    <img src="https://via.placeholder.com/300" alt="Shoes">
    <h3>Shoes</h3>
    <p>₹1,499</p>
    <button onclick="addToCart()">Add to Cart</button>
  </div>

  <div class="product">
    <img src="https://via.placeholder.com/300" alt="Watch">
    <h3>Watch</h3>
    <p>₹999</p>
    <button onclick="addToCart()">Add to Cart</button>
  </div>

</main>

<script>
  let cart = 0;

  function addToCart() {
    cart++;
    document.getElementById("cart").textContent = cart;
  }
</script>

</body>
</html>

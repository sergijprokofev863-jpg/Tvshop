Копіювати код
<!DOCTYPE html>
<html lang="uk">
<head>
  <meta charset="UTF-8">
  <title>Все для дому та сім'ї — Інтернет-магазин</title>
  <meta name="description" content="Інтернет-магазин товарів для дому та сім'ї. Зручно, швидко, доступно.">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f5f5f5;
    }
    header {
      background: #2c3e50;
      color: #fff;
      padding: 15px;
      text-align: center;
    }
    nav {
      display: flex;
      justify-content: center;
      gap: 15px;
      background: #34495e;
      padding: 10px;
      flex-wrap: wrap;
    }
    nav a {
      color: white;
      text-decoration: none;
      font-weight: bold;
    }
    section {
      padding: 20px;
      background: white;
      margin: 10px;
      border-radius: 8px;
    }
    .products {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 15px;
    }
    .product {
      background: #ecf0f1;
      padding: 15px;
      border-radius: 8px;
      text-align: center;
    }
    button {
      background: #27ae60;
      color: white;
      border: none;
      padding: 10px;
      cursor: pointer;
      border-radius: 5px;
    }
    button:hover {
      background: #219150;
    }
    footer {
      text-align: center;
      padding: 15px;
      background: #2c3e50;
      color: white;
    }
  </style>
</head>

<body>

<header>
  <h1>Все для дому та сім'ї</h1>
  <p>Інтернет-магазин</p>
</header>

<nav>
  <a href="#home">Головна</a>
  <a href="#shop">Магазин</a>
  <a href="#cart">Кошик</a>
  <a href="#about">Про нас</a>
  <a href="#contacts">Контакти</a>
</nav>

<section id="home">
  <h2>Ласкаво просимо!</h2>
  <p>У нас ви знайдете все необхідне для дому, кухні та сім'ї.</p>
</section>

<section id="shop">
  <h2>Товари</h2>
  <div class="products">
    <div class="product">
      <h3>Набір для кухні</h3>
      <p>Ціна: 500 грн</p>
      <button onclick="addToCart('Набір для кухні', 500)">Додати в кошик</button>
    </div>
    <div class="product">
      <h3>Господарські товари</h3>
      <p>Ціна: 300 грн</p>
      <button onclick="addToCart('Господарські товари', 300)">Додати в кошик</button>
    </div>
    <div class="product">
      <h3>Товари для дому</h3>
      <p>Ціна: 700 грн</p>
      <button onclick="addToCart('Товари для дому', 700)">Додати в кошик</button>
    </div>
  </div>
</section>

<section id="cart">
  <h2>Кошик</h2>
  <ul id="cartItems"></ul>
  <p><strong>Разом: <span id="total">0</span> грн</strong></p>
</section>

<section id="about">
  <h2>Про нас</h2>
  <p>Ми — український інтернет-магазин, який пропонує якісні товари для кожної родини.</p>
</section>

<section id="contacts">
  <h2>Контакти</h2>
  <p>Телефон: 098 947 7418</p>
  <p>Telegram: Прокофьев</p>
</section>

<footer>
  © 2026 Все для дому та сім'ї
</footer>

<script>
  let total = 0;
  const cartItems = document.getElementById('cartItems');
  const totalEl = document.getElementById('total');

  function addToCart(name, price) {
    const li = document.createElement('li');
    li.textContent = name + ' — ' + price + ' грн';
    cartItems.appendChild(li);
    total += price;
    totalEl.textContent = total;
  }
</script>

</body>
</html# Tvshop
Магазин для всіх потреб

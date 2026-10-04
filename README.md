# daogiaminh
Website chính thức của Đào Gia Minh 
<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>ĐÀO GIA MINH | Fashion Store</title>

  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: Arial, sans-serif;
      background: #080808;
      color: white;
    }

    /* HEADER */
    header {
      height: 75px;
      padding: 0 7%;
      display: flex;
      align-items: center;
      justify-content: space-between;
      border-bottom: 1px solid #333;
      position: sticky;
      top: 0;
      background: rgba(8,8,8,0.95);
      z-index: 100;
    }

    .logo {
      font-size: 24px;
      font-weight: bold;
      letter-spacing: 3px;
      color: #d8d8d8;
    }

    nav a {
      color: #aaa;
      text-decoration: none;
      margin-left: 30px;
      transition: 0.3s;
    }

    nav a:hover {
      color: white;
    }

    /* HERO */
    .hero {
      min-height: 520px;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 50px 20px;
      background:
        radial-gradient(circle at center, #303030 0%, #111 35%, #050505 75%);
    }

    .hero h1 {
      font-size: clamp(45px, 8vw, 90px);
      letter-spacing: 8px;
      background: linear-gradient(
        120deg,
        #666,
        #fff,
        #999,
        #fff,
        #555
      );
      background-size: 300%;
      -webkit-background-clip: text;
      color: transparent;
      animation: shine 5s infinite linear;
    }

    @keyframes shine {
      0% {
        background-position: 0%;
      }

      100% {
        background-position: 300%;
      }
    }

    .hero p {
      margin-top: 20px;
      color: #aaa;
      font-size: 18px;
    }

    .btn {
      display: inline-block;
      margin-top: 30px;
      padding: 14px 30px;
      border: 1px solid #aaa;
      color: white;
      text-decoration: none;
      transition: 0.3s;
    }

    .btn:hover {
      background: white;
      color: black;
    }

    /* PRODUCTS */
    .section {
      padding: 80px 7%;
    }

    .section-title {
      text-align: center;
      margin-bottom: 45px;
    }

    .section-title h2 {
      font-size: 38px;
      letter-spacing: 3px;
    }

    .section-title p {
      color: #777;
      margin-top: 10px;
    }

    .products {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
      gap: 25px;
    }

    .product {
      background: #111;
      border: 1px solid #292929;
      overflow: hidden;
      transition: 0.3s;
    }

    .product:hover {
      transform: translateY(-8px);
      border-color: #777;
    }

    .product-image {
      height: 280px;
      display: flex;
      align-items: center;
      justify-content: center;
      background: linear-gradient(135deg, #222, #080808);
      color: #555;
      font-size: 70px;
    }

    .product-info {
      padding: 22px;
    }

    .product-info h3 {
      font-size: 20px;
      margin-bottom: 10px;
    }

    .product-info p {
      color: #888;
      font-size: 14px;
      margin-bottom: 15px;
    }

    .price {
      color: #ddd;
      font-size: 20px;
      font-weight: bold;
      margin-bottom: 15px;
    }

    .buy {
      width: 100%;
      padding: 12px;
      background: transparent;
      color: white;
      border: 1px solid #555;
      cursor: pointer;
      transition: 0.3s;
    }

    .buy:hover {
      background: white;
      color: black;
    }

    /* ABOUT */
    .about {
      background: #101010;
      text-align: center;
    }

    .about p {
      max-width: 750px;
      margin: auto;
      line-height: 1.8;
      color: #999;
    }

    /* CONTACT */
    .contact {
      text-align: center;
    }

    .contact p {
      color: #999;
      margin: 10px;
    }

    /* FOOTER */
    footer {
      padding: 30px;
      text-align: center;
      border-top: 1px solid #222;
      color: #666;
    }

    /* MOBILE */
    @media(max-width: 700px) {

      header {
        padding: 0 20px;
      }

      nav {
        display: none;
      }

      .hero {
        min-height: 450px;
      }

      .section {
        padding: 60px 20px;
      }
    }
  </style>
</head>

<body>

  <!-- HEADER -->

  <header>

    <div class="logo">
      ĐÀO GIA MINH
    </div>

    <nav>
      <a href="#home">Trang chủ</a>
      <a href="#products">Sản phẩm</a>
      <a href="#about">Về chúng tôi</a>
      <a href="#contact">Liên hệ</a>
    </nav>

  </header>


  <!-- HERO -->

  <section class="hero" id="home">

    <div>

      <h1>ĐÀO GIA MINH</h1>

      <p>
        PREMIUM FASHION COLLECTION
      </p>

      <a href="#products" class="btn">
        KHÁM PHÁ BỘ SƯU TẬP
      </a>

    </div>

  </section>


  <!-- PRODUCTS -->

  <section class="section" id="products">

    <div class="section-title">

      <h2>SẢN PHẨM NỔI BẬT</h2>

      <p>
        Những thiết kế được tuyển chọn dành cho bạn
      </p>

    </div>


    <div class="products">


      <!-- PRODUCT 1 -->

      <div class="product">

        <div class="product-image">
          👕
        </div>

        <div class="product-info">

          <h3>Áo Thun Premium</h3>

          <p>
            Thiết kế tối giản, chất liệu cao cấp.
          </p>

          <div class="price">
            299.000₫
          </div>

          <button class="buy"
            onclick="addToCart('Áo Thun Premium', 299000)">
            THÊM VÀO GIỎ
          </button>

        </div>

      </div>


      <!-- PRODUCT 2 -->

      <div class="product">

        <div class="product-image">
          👔
        </div>

        <div class="product-info">

          <h3>Áo Polo Luxury</h3>

          <p>
            Phong cách lịch lãm, hiện đại.
          </p>

          <div class="price">
            399.000₫
          </div>

          <button class="buy"
            onclick="addToCart('Áo Polo Luxury', 399000)">
            THÊM VÀO GIỎ
          </button>

        </div>

      </div>


      <!-- PRODUCT 3 -->

      <div class="product">

        <div class="product-image">
          👖
        </div>

        <div class="product-info">

          <h3>Quần Jeans Premium</h3>

          <p>
            Form hiện đại, dễ phối đồ.
          </p>

          <div class="price">
            499.000₫
          </div>

          <button class="buy"
            onclick="addToCart('Quần Jeans Premium', 499000)">
            THÊM VÀO GIỎ
          </button>

        </div>

      </div>


      <!-- PRODUCT 4 -->

      <div class="product">

        <div class="product-image">
          🧥
        </div>

        <div class="product-info">

          <h3>Áo Khoác Signature</h3>

          <p>
            Phong cách mạnh mẽ, sang trọng.
          </p>

          <div class="price">
            699.000₫
          </div>

          <button class="buy"
            onclick="addToCart('Áo Khoác Signature', 699000)">
            THÊM VÀO GIỎ
          </button>

        </div>

      </div>

    </div>

  </section>


  <!-- ABOUT -->

  <section class="section about" id="about">

    <div class="section-title">

      <h2>VỀ ĐÀO GIA MINH</h2>

    </div>

    <p>

      Đào Gia Minh hướng tới những sản phẩm có thiết kế
      hiện đại, tinh tế và chất lượng. Chúng tôi tập trung
      vào trải nghiệm khách hàng và xây dựng một thương hiệu
      có phong cách riêng.

    </p>

  </section>


  <!-- CONTACT -->

  <section class="section contact" id="contact">

    <div class="section-title">

      <h2>LIÊN HỆ</h2>

    </div>

    <p>📞 Điện thoại: 0123 456 789</p>

    <p>📧 Email: contact@daogiaminh.com</p>

    <p>📍 Việt Nam</p>

  </section>


  <!-- FOOTER -->

  <footer>

    © 2026 ĐÀO GIA MINH — ALL RIGHTS RESERVED

  </footer>


  <!-- SHOPPING CART DEMO -->

  <script>

    let cart = [];

    function addToCart(name, price) {

      cart.push({
        name: name,
        price: price
      });

      alert(
        name +
        " đã được thêm vào giỏ hàng!"
      );

      console.log(cart);

    }

  </script>

</body>
</html>

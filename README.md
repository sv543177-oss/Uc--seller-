<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>UC Seller - In Minimum Amount</title>
  <link rel="icon" href="https://img.icons8.com/emoji/48/money-bag.png" type="image/png">
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #0d0d0d, #1a1a1a);
      color: #fff;
    }

    header {
      background: rgba(0,0,0,0.85);
      padding: 20px;
      text-align: center;
      border-bottom: 2px solid gold;
      box-shadow: 0 4px 10px rgba(255,215,0,0.2);
    }

    header h1 {
      margin: 0;
      font-size: 2.4rem;
      color: gold;
      text-shadow: 0 0 12px #ff9900;
    }

    .hero {
      background: url("https://w0.peakpx.com/wallpaper/820/835/HD-wallpaper-bgmi-battlegrounds-mobile-india.jpg") no-repeat center/cover;
      text-align: center;
      padding: 110px 20px;
      color: white;
      box-shadow: inset 0 0 80px rgba(0,0,0,0.7);
    }

    .hero h2 {
      font-size: 2.6rem;
      margin-bottom: 15px;
      text-shadow: 0 0 12px black;
    }

    .section {
      padding: 40px 20px;
      max-width: 1000px;
      margin: auto;
    }

    .section h2 {
      text-align: center;
      margin-bottom: 20px;
      color: gold;
      text-shadow: 0 0 8px #ff9900;
      font-size: 1.8rem;
    }

    .qr-box {
      text-align: center;
      margin-bottom: 30px;
      background: rgba(0,0,0,0.7);
      padding: 25px;
      border-radius: 14px;
      box-shadow: 0 4px 15px rgba(255,215,0,0.4);
    }

    .qr-box img {
      width: 230px;
      border: 4px solid gold;
      border-radius: 14px;
      box-shadow: 0 0 20px gold;
    }

    .qr-box p {
      margin-top: 12px;
      font-size: 1.1rem;
    }

    .products {
      background: rgba(0,0,0,0.75);
      border-radius: 14px;
      padding: 25px;
      box-shadow: 0 4px 12px rgba(255,215,0,0.3);
    }

    .product {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 14px;
      margin: 10px 0;
      background: #1a1a1a;
      border-radius: 10px;
      flex-wrap: wrap;
      transition: transform 0.2s;
    }

    .product:hover {
      transform: scale(1.02);
      box-shadow: 0 0 10px rgba(255,215,0,0.3);
    }

    .product span {
      font-size: 1.2rem;
      margin-bottom: 8px;
      font-weight: bold;
    }

    label {
      display: none;
    }

    input {
      padding: 8px;
      border-radius: 6px;
      border: none;
      outline: none;
      margin-right: 10px;
      flex: 1;
      font-size: 1rem;
    }

    .buy-btn {
      background: gold;
      color: black;
      border: none;
      padding: 10px 18px;
      border-radius: 8px;
      cursor: pointer;
      font-weight: bold;
      text-decoration: none;
      transition: background 0.3s, transform 0.2s;
    }

    .buy-btn:hover {
      background: orange;
      transform: scale(1.05);
    }

    footer {
      background: black;
      color: #aaa;
      text-align: center;
      padding: 18px;
      border-top: 2px solid gold;
      font-size: 0.9rem;
    }

    /* Responsive fixes */
    @media (max-width: 600px) {
      .product {
        flex-direction: column;
        align-items: flex-start;
      }
      input {
        width: 100%;
        margin: 10px 0;
      }
      .buy-btn {
        width: 100%;
        text-align: center;
      }
    }
  </style>
</head>
<body>

  <header>
    <h1>UC Seller</h1>
    <p>In Minimum Amount 💰</p>
  </header>

  <section class="hero">
    <h2>Welcome to UC Seller 🔥</h2>
    <p>Get UC, Gun Skins, X-suits & More at the Lowest Rates!</p>
  </section>

  <section class="section">
    <h2>Scan & Pay First</h2>
    <div class="qr-box">
      <img src="https://i.ibb.co/5nDkwqn/qr-ravi-verma.png" alt="Scan to pay UPI QR for UC purchase">
      <p>UPI ID: <b>rv2803033@okicici</b></p>
      <p><b>Enter UTR Number After Payment ✅</b></p>
      <input type="text" id="utr" placeholder="Enter UTR / Transaction ID">
    </div>

    <h2>Our UC Offers</h2>
    <div class="products">
      <div class="product">
        <span>50 Rs - 60 UC</span>
        <input type="text" id="id1" placeholder="Enter BGMI ID">
        <button class="buy-btn" onclick="sendWhatsApp('50 Rs - 60 UC','id1')">Buy</button>
      </div>
      <div class="product">
        <span>300 Rs - 2700 UC</span>
        <input type="text" id="id2" placeholder="Enter BGMI ID">
        <button class="buy-btn" onclick="sendWhatsApp('300 Rs - 2700 UC','id2')">Buy</button>
      </div>
      <div class="product">
        <span>500 Rs - 5400 UC</span>
        <input type="text" id="id3" placeholder="Enter BGMI ID">
        <button class="buy-btn" onclick="sendWhatsApp('500 Rs - 5400 UC','id3')">Buy</button>
      </div>
      <div class="product">
        <span>1000 Rs - 15000 UC</span>
        <input type="text" id="id4" placeholder="Enter BGMI ID">
        <button class="buy-btn" onclick="sendWhatsApp('1000 Rs - 15000 UC','id4')">Buy</button>
      </div>
      <div class="product">
        <span>1999 Rs - 25000 UC + Glacier Max</span>
        <input type="text" id="id5" placeholder="Enter BGMI ID">
        <button class="buy-btn" onclick="sendWhatsApp('1999 Rs - 25000 UC + Glacier Max','id5')">Buy</button>
      </div>
    </div>
  </section>

  <footer>
    <p>&copy; 2025 UC Seller | All Rights Reserved</p>
  </footer>

  <script>
    function sendWhatsApp(offer, inputId) {
      const input = document.getElementById(inputId);
      const bgmiId = input.value;
      const utr = document.getElementById("utr").value;

      if(bgmiId.trim() === "") {
        alert("Please enter your BGMI ID!");
        return;
      }
      if(utr.trim() === "") {
        alert("Please enter your UTR / Transaction ID after payment!");
        return;
      }

      const phone = "919636739186"; // your WhatsApp number
      const upi = "rv2803033@okicici"; // your UPI ID
      const message = `Hello, I want to buy:\n${offer}\nMy BGMI ID: ${bgmiId}\nTransaction UTR: ${utr}\nI have paid via UPI: ${upi}`;
      const url = `https://wa.me/${phone}?text=${encodeURIComponent(message)}`;
      window.open(url, "_blank");
    }
  </script>

</body>
</html>
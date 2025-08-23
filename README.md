<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>UC Seller - In Minimum Amount</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #0d0d0d;
      color: #fff;
    }

    header {
      background: rgba(0,0,0,0.8);
      padding: 20px;
      text-align: center;
      border-bottom: 2px solid gold;
    }

    header h1 {
      margin: 0;
      font-size: 2.2rem;
      color: gold;
      text-shadow: 0 0 10px #ff9900;
    }

    .hero {
      background: url("https://w0.peakpx.com/wallpaper/820/835/HD-wallpaper-bgmi-battlegrounds-mobile-india.jpg") no-repeat center/cover;
      text-align: center;
      padding: 100px 20px;
      color: white;
    }

    .hero h2 {
      font-size: 2.5rem;
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
    }

    .products {
      background: rgba(0,0,0,0.7);
      border-radius: 12px;
      padding: 20px;
      box-shadow: 0 4px 10px rgba(255,215,0,0.3);
    }

    .product {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 12px;
      margin: 8px 0;
      background: #1a1a1a;
      border-radius: 8px;
    }

    .product span {
      font-size: 1.1rem;
    }

    .buy-btn {
      background: gold;
      color: black;
      border: none;
      padding: 8px 15px;
      border-radius: 6px;
      cursor: pointer;
      font-weight: bold;
    }

    .buy-btn:hover {
      background: orange;
    }

    /* Modal */
    .modal {
      display: none;
      position: fixed;
      z-index: 1000;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      background: rgba(0,0,0,0.8);
      justify-content: center;
      align-items: center;
    }

    .modal-content {
      background: #222;
      padding: 25px;
      border-radius: 12px;
      width: 90%;
      max-width: 400px;
      text-align: center;
      color: white;
    }

    .modal-content h3 {
      color: gold;
      margin-bottom: 15px;
    }

    input {
      width: 90%;
      padding: 10px;
      margin: 10px 0;
      border-radius: 6px;
      border: none;
    }

    .next-btn {
      background: gold;
      color: black;
      border: none;
      padding: 10px 20px;
      border-radius: 6px;
      cursor: pointer;
      margin-top: 10px;
      font-weight: bold;
    }

    .qr-code {
      margin-top: 15px;
    }

    .qr-code img {
      width: 200px;
      border: 4px solid gold;
      border-radius: 12px;
      box-shadow: 0 0 15px gold;
    }

    footer {
      background: black;
      color: #aaa;
      text-align: center;
      padding: 15px;
      border-top: 2px solid gold;
      font-size: 0.9rem;
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
    <h2>Our UC Offers</h2>
    <div class="products">
      <div class="product">
        <span>50 Rs - 60 UC</span>
        <button class="buy-btn" onclick="openModal('50 Rs - 60 UC')">Buy</button>
      </div>
      <div class="product">
        <span>300 Rs - 2700 UC</span>
        <button class="buy-btn" onclick="openModal('300 Rs - 2700 UC')">Buy</button>
      </div>
      <div class="product">
        <span>500 Rs - 5400 UC</span>
        <button class="buy-btn" onclick="openModal('500 Rs - 5400 UC')">Buy</button>
      </div>
      <div class="product">
        <span>1000 Rs - 15000 UC</span>
        <button class="buy-btn" onclick="openModal('1000 Rs - 15000 UC')">Buy</button>
      </div>
      <div class="product">
        <span>1999 Rs - 25000 UC + Glacier Max</span>
        <button class="buy-btn" onclick="openModal('1999 Rs - 25000 UC + Glacier Max')">Buy</button>
      </div>
    </div>
  </section>

  <!-- Modal -->
  <div id="buyModal" class="modal">
    <div class="modal-content" id="modalStep1">
      <h3>Enter Your BGMI ID</h3>
      <p id="chosenOffer"></p>
      <input type="text" id="bgmiId" placeholder="Enter BGMI ID">
      <button class="next-btn" onclick="goToStep2()">Next</button>
    </div>

    <div class="modal-content" id="modalStep2" style="display:none;">
      <h3>Scan & Pay</h3>
      <p>Please scan the QR code below to complete payment:</p>
      <div class="qr-code">
        <!-- ✅ Your real QR code -->
        <img src="https://i.ibb.co/5nDkwqn/qr-ravi-verma.png" alt="Payment QR Code">
      </div>
      <p style="margin-top:10px; font-size:0.9rem;">UPI ID: <b>rv2803033@okicici</b></p>
      <br>
      <button class="next-btn" onclick="sendWhatsApp()">Send Details on WhatsApp</button>
      <button class="next-btn" onclick="closeModal()">Done</button>
    </div>
  </div>

  <footer>
    <p>&copy; 2025 UC Seller | All Rights Reserved</p>
  </footer>

  <script>
    let offerSelected = "";

    function openModal(offer) {
      offerSelected = offer;
      document.getElementById("chosenOffer").innerText = "Offer: " + offer;
      document.getElementById("buyModal").style.display = "flex";
      document.getElementById("modalStep1").style.display = "block";
      document.getElementById("modalStep2").style.display = "none";
    }

    function goToStep2() {
      const bgmiId = document.getElementById("bgmiId").value;
      if(bgmiId.trim() === "") {
        alert("Please enter your BGMI ID!");
        return;
      }
      document.getElementById("modalStep1").style.display = "none";
      document.getElementById("modalStep2").style.display = "block";
    }

    function sendWhatsApp() {
      const bgmiId = document.getElementById("bgmiId").value;
      const message = `Hello, I want to buy:\n${offerSelected}\nMy BGMI ID: ${bgmiId}\nI have paid via UPI (rv2803033@okicici).`;
      const phone = "919251041235"; // your WhatsApp number with country code
      const url = `https://wa.me/${phone}?text=${encodeURIComponent(message)}`;
      window.open(url, "_blank");
    }

    function closeModal() {
      document.getElementById("buyModal").style.display = "none";
      document.getElementById("bgmiId").value = "";
    }
  </script>

</body>
</html>

# Freshfoods
Doorstep freshfoods
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JKS Grocery & Food Delivery</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 0; background: #f5faff; color: #1a4249; }
        header { background: #30b6e4; color: #fff; padding: 20px; text-align: center; }
        h1 { margin: 0; }
        .products { display: flex; flex-wrap: wrap; justify-content: center; margin: 30px 0; }
        .product { background: #fff; border-radius: 10px; box-shadow: 0 2px 6px #9edbf3; margin: 15px; width: 270px; padding: 20px; text-align: center; }
        .product img { width: 80%; border-radius: 8px; }
        .product-title { font-size: 1.2em; margin: 10px 0; }
        .product-price { font-weight: bold; color: #128c7e; }
        .order-btn { background: #20b476; color: #fff; border: none; border-radius: 5px; padding: 10px 20px; font-size: 1em; cursor: pointer; margin-top: 12px; }
        .order-btn:hover { background: #128c7e; }
        footer { background: #30b6e4; color: #fff; text-align: center; padding: 18px; margin-top: 40px; }
    </style>
    <script>
        function orderOnWhatsApp(product) {
            const phone = "919999999999"; // Replace with your WhatsApp number (country code)
            const message = encodeURIComponent(`Hello! I want to order: ${product}. Please provide details.`);
            window.open(`https://wa.me/${phone}?text=${message}`, '_blank');
        }
    </script>
</head>
<body>
    <header>
        <h1>JKS Grocery & Food Delivery</h1>
        <p>Fresh groceries, food & more delivered to your door. Order via WhatsApp!</p>
    </header>
    <div class="products">
        <div class="product">
            <img src="https://images.unsplash.com/photo-1504674900247-0877df9cc836" alt="Fresh Vegetables">
            <div class="product-title">Fresh Vegetables Box</div>
            <div class="product-price">₹299</div>
            <button class="order-btn" onclick="orderOnWhatsApp('Fresh Vegetables Box (₹299)')">Order via WhatsApp</button>
        </div>
        <div class="product">
            <img src="https://images.unsplash.com/photo-1519864600265-abb23847ef2c" alt="Dairy Milk">
            <div class="product-title">Dairy Milk (1 Ltr)</div>
            <div class="product-price">₹55</div>
            <button class="order-btn" onclick="orderOnWhatsApp('Dairy Milk 1 Ltr (₹55)')">Order via WhatsApp</button><!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Home Website</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f5f9ff;
      text-align: center;
    }

    header {
      background: #0077b6;
      color: white;
      padding: 15px;
    }

    nav {
      display: flex;
      justify-content: space-around;
      background: #023e8a;
      padding: 10px 0;
    }

    nav a {
      color: white;
      text-decoration: none;
      font-weight: bold;
      padding: 8px 12px;
      border-radius: 5px;
    }

    nav a:hover {
      background: #0077b6;
    }

    section {
      padding: 30px;
    }

    form {
      background: white;
      max-width: 400px;
      margin: auto;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0px 2px 6px rgba(0,0,0,0.2);
    }

    input, textarea, button {
      width: 100%;
      padding: 10px;
      margin: 8px 0;
      border-radius: 5px;
      border: 1px solid #ccc;
      font-size: 16px;
    }

    button {
      background: #0077b6;
      color: white;
      border: none;
      cursor: pointer;
    }

    button:hover {
      background: #023e8a;
    }
  </style>
</head>
<body>
  <header>
    <h1>My Home Website</h1>
  </header>

  <nav>
    <a href="#">Home Page</a>
    <a href="#">Contact Us</a>
    <a href="#">Camera</a>
    <a href="#">Orders</a>
    <a href="#">Profile</a>
  </nav>

  <section>
    <h2>Place Your Order</h2>
    <form id="orderForm">
      <input type="text" id="name" placeholder="Enter your name" required>
      <input type="tel" id="phone" placeholder="Enter your phone number" required>
      <textarea id="order" rows="3" placeholder="Enter your order details" required></textarea>
      <button type="submit">Send via WhatsApp</button>
    </form>
  </section>

  <script>
    document.getElementById("orderForm").addEventListener("submit", function(e){
      e.preventDefault();
      
      let name = document.getElementById("name").value;
      let phone = document.getElementById("phone").value;
      let order = document.getElementById("order").value;

      let message = `Hello, my name is ${name}. My phone number is ${phone}. I want to order: ${order}`;
      let whatsappURL = `https://wa.me/91XXXXXXXXXX?text=${encodeURIComponent(message)}`;
      
      window.open(whatsappURL, "_blank");
    });
  </script>

</body>
</html>
        </div>
        <div class="product">
            <img src="https://images.unsplash.com/photo-1502741338009-cac2772e18bc" alt="Organic Rice">
            <div class="product-title">Organic Rice (5 Kg)</div>
            <div class="product-price">₹349</div><!DOCTYPE html>
<html>
<head>
    <title>Delivery Place Selection</title>
    <style>
        #map {
            height: 400px;
            width: 100%;
            margin-top: 10px;
        }
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        input, button {
            font-size: 16px;
            padding: 8px;
        }
    </style>
</head>
<body>
    <h2>Select Delivery Place</h2>
    <input id="address" type="text" placeholder="Enter your delivery address" style="width: 300px;">
    <button onclick="codeAddress()">Show on Map</button>

    <div id="map"></div>

    <script>
        let map;
        let geocoder;
        let marker;

        function initMap() {
            const defaultLocation = { lat: 40.7128, lng: -74.0060 }; // Default: New York City

            map = new google.maps.Map(document.getElementById('map'), {
                zoom: 12,
                center: defaultLocation
            });

            geocoder = new google.maps.Geocoder();
        }

        function codeAddress() {
            const address = document.getElementById('address').value;
            geocoder.geocode({ 'address': address }, function(results, status) {
                if (status === 'OK') {
                    map.setCenter(results[0].geometry.location);

                    if (marker) {
                        marker.setMap(null);
                    }

                    marker = new google.maps.Marker({
                        map: map,
                        position: results[0].geometry.location
                    });
                } else {
                    alert('Geocode was not successful for the following reason: ' + status);
                }
            });
        }
    </script>

    <script async defer 
      src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initMap">
    </script>
</body>
</html>
            <button class="order-btn" onclick="orderOnWhatsApp('Organic Rice 5 Kg (₹349)')">Order via WhatsApp</button>
        </div>
        <div class="product">
            <img src="https://images.unsplash.com/photo-1470337458703-46ad1756a187" alt="Chicken Curry Cut">
            <div class="product-title">Chicken Curry Cut (1 Kg)</div>
            <div class="product-price">₹239</div>
            <button class="order-btn" onclick="orderOnWhatsApp('Chicken Curry Cut 1 Kg (₹239)')">Order via WhatsApp</button>
        </div>
        <div class="product">
            <img src="https://images.unsplash.com/photo-1464306076886-debca5e8a6b0" alt="Bread">
            <div class="product-title">Fresh Bread (400g)</div>
            <div class="product-price">₹45</div>
            <button class="order-btn" onclick="orderOnWhatsApp('Fresh Bread 400g (₹45)')">Order via WhatsApp</button>
        </div>
    </div>
    <footer>
        &copy; 2025 JKS Grocery & Food Delivery. All rights reserved.
    </footer>
</body>
</html>

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
            <button class="order-btn" onclick="orderOnWhatsApp('Dairy Milk 1 Ltr (₹55)')">Order via WhatsApp</button>
        </div>
        <div class="product">
            <img src="https://images.unsplash.com/photo-1502741338009-cac2772e18bc" alt="Organic Rice">
            <div class="product-title">Organic Rice (5 Kg)</div>
            <div class="product-price">₹349</div>
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

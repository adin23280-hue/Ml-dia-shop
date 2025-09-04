<!DOCTYPE html>
<html lang="my">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mobile Legends Diamonds အွန်လိုင်း</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 0; padding: 0; background-color: #f0f0f0; }
        header { background-color: #ff4757; color: white; padding: 20px; text-align: center; }
        nav a { color: white; margin: 0 15px; text-decoration: none; font-weight: bold; }
        section { padding: 40px 20px; text-align: center; }
        .products-container { display: flex; justify-content: center; flex-wrap: wrap; gap: 20px; }
        .product { background-color: white; padding: 20px; border-radius: 10px; box-shadow: 0 0 10px rgba(0,0,0,0.1); width: 220px; }
        button { background-color: #ff6b81; color: white; border: none; padding: 10px 15px; border-radius: 5px; cursor: pointer; margin-top: 10px; }
        button:hover { background-color: #ff4757; }
        footer { background-color: #2f3542; color: white; padding: 20px; text-align: center; }
        .qr { margin-top: 15px; width: 150px; height: 150px; cursor: pointer; }
    </style>
</head>
<body>
    <header>
        <h1>Mobile Legends Diamonds အွန်လိုင်း</h1>
        <nav>
            <a href="#home">မူလစာမျက်နှာ</a>
            <a href="#products">Diamonds</a>
            <a href="#contact">ဆက်သွယ်ရန်</a>
        </nav>
    </header>

    <section id="home">
        <h2>မင်္ဂလာပါ!</h2>
        <p>Mobile Legends အတွက် Diamond များကို အလွယ်တကူ ဝယ်ယူနိုင်ပါတယ်။</p>
    </section>

    <section id="products">
        <h2>Diamonds Package များ</h2>
        <div class="products-container" id="productsContainer"></div>
    </section>

    <section id="contact">
        <h2>ဆက်သွယ်ရန်</h2>
        <p>📲 Order Now: @A_ddin</p>
        <p>💳 KPay / Wave – 09799742510</p>
        <p>👤 Ko Pyae Sone Aung</p>
        <!-- Replace the src below with your personal KPay/Wave QR code link -->
        <img src="https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=https://kpay.com/pay/09799742510" 
             alt="KPay QR" class="qr" 
             onclick="window.open('https://kpay.com/pay/09799742510','_blank')" 
             title="Click to Pay">
    </section>

    <footer>
        <p>&copy; 2025 Mobile Legends Diamonds အွန်လိုင်း</p>
    </footer>

    <script>
        const products = [
            { name: "86 💎", price: 5500 },
            { name: "172 💎", price: 10800 },
            { name: "257 💎", price: 15800 },
            { name: "344 💎", price: 21200 },
            { name: "429 💎", price: 26500 },
            { name: "514 💎", price: 32700 },
            { name: "600 💎", price: 37850 },
            { name: "706 💎", price: 43750 },
            { name: "878 💎", price: 54750 },
            { name: "963 💎", price: 59950 },
            { name: "1049 💎", price: 65450 },
            { name: "1135 💎", price: 70950 },
            { name: "1412 💎", price: 87550 },
            { name: "2195 💎", price: 132650 },
            { name: "3688 💎", price: 221000 },
            { name: "5532 💎", price: 333000 },
            { name: "9288 💎", price: 555000 },
            { name: "Weekly Pass (1 Week 💎220 + ⭐️70)", price: 6800 }
        ];

        const kpayLink = "https://kpay.com/pay/09799742510"; // Replace with your own payment link

        const container = document.getElementById('productsContainer');

        products.forEach(product => {
            const div = document.createElement('div');
            div.className = "product";
            div.innerHTML = `
                <h3>${product.name}</h3>
                <p>₭ ${product.price.toLocaleString()}</p>
                <button onclick="buyNow('${product.name}', ${product.price})">ဝယ်ရန်</button>
            `;
            container.appendChild(div);
        });

        function buyNow(packageName, price) {
            const confirmMsg = `${packageName} ကို ₭${price.toLocaleString()} ဖြင့် ဝယ်ချင်သလား?`;
            if(confirm(confirmMsg)) {
                window.open(kpayLink, "_blank");
            }
        }
    </script>
</body>
</html>

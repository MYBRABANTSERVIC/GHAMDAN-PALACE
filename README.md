# GHAMDAN-PALACEbody {
    <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ghamdan Palace</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Ghamdan Palace</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="services.html">Services</a>
            <a href="store.html">Store</a>
            <a href="contact.html">Contact</a>
        </nav>
    </header>

    <section class="hero">
        <h2>Your Partner in Services and Import/Export</h2>
        <p>Professional services: Supervisor, Security, Delivery, Construction Cleaning, Cleaning, Export Support</p>
    </section>

    <section class="overview">
        <h3>What We Offer</h3>
        <ul>
            <li>Supervisor & Security</li>
            <li>Delivery & Construction Cleaning</li>
            <li>Cleaning & Export Support</li>
        </ul>
    </section>

    <footer>
        <p>© 2025 Ghamdan Palace</p>
    </footer>
</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Our Services - Ghamdan Palace</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
<header>
    <h1>Ghamdan Palace</h1>
    <nav>
        <a href="index.html">Home</a>
        <a href="services.html">Services</a>
        <a href="store.html">Store</a>
        <a href="contact.html">Contact</a>
    </nav>
</header>

<section class="services">
    <h2>Our Services</h2>
    <div class="service-card">
        <h3>Security</h3>
        <p>Professional security for your company and events.</p>
    </div>
    <div class="service-card">
        <h3>Delivery</h3>
        <p>Reliable delivery of packages and goods.</p>
    </div>
    <div class="service-card">
        <h3>Construction Cleaning</h3>
        <p>Efficient cleaning of construction sites.</p>
    </div>
    <div class="service-card">
        <h3>Cleaning</h3>
        <p>Thorough cleaning services for any property.</p>
    </div>
    <div class="service-card">
        <h3>Export Support</h3>
        <p>Assistance with export and import processes.</p>
    </div>
</section>

<footer>
    <p>© 2025 Ghamdan Palace</p>
</footer>
</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Store - Ghamdan Palace</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
<header>
    <h1>Ghamdan Palace</h1>
    <nav>
        <a href="index.html">Home</a>
        <a href="services.html">Services</a>
        <a href="store.html">Store</a>
        <a href="contact.html">Contact</a>
    </nav>
</header>

<section class="store">
    <h2>Import / Export Products</h2>

    <div class="product-card">
        <h3>Product 1: Coffee</h3>
        <p>Price: €10</p>
        <label>Quantity:
            <input type="number" value="1" min="1" class="quantity">
        </label>
        <label>Destination:
            <select class="destination">
                <option value="NL_to_Yemen">Netherlands → Yemen</option>
                <option value="NL_to_Gulf">Netherlands → Gulf</option>
                <option value="Yemen_to_NL">Yemen → Netherlands</option>
                <option value="Gulf_to_NL">Gulf → Netherlands</option>
            </select>
        </label>
        <button onclick="addToCart(this)">Add to Cart</button>
    </div>

    <h3>Cart:</h3>
    <ul id="cart"></ul>
</section>

<script src="script.js"></script>

<footer>
    <p>© 2025 Ghamdan Palace</p>
</footer>
</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contact - Ghamdan Palace</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
<header>
    <h1>Ghamdan Palace</h1>
    <nav>
        <a href="index.html">Home</a>
        <a href="services.html">Services</a>
        <a href="store.html">Store</a>
        <a href="contact.html">Contact</a>
    </nav>
</header>

<section class="contact">
    <h2>Contact Us</h2>
    <form>
        <label>Name: <input type="text" required></label>
        <label>Email: <input type="email" required></label>
        <label>Message: <textarea required></textarea></label>
        <button type="submit">Send</button>
    </form>
    <p>WhatsApp: +31 6 12345678</p>
    <p>Email: info@ghamdanpalace.com</p>
</section>

<footer>
    <p>© 2025 Ghamdan Palace</p>
</footer>
</body>
</html>function addToCart(button){
    const card = button.parentElement;
    const productName = card.querySelector('h3').innerText;
    const quantity = card.querySelector('.quantity').value;
    const destination = card.querySelector('.destination').value;

    const cart = document.getElementById('cart');
    const li = document.createElement('li');
    li.textContent = `${productName} - Quantity: ${quantity} - Destination: ${destination}`;
    cart.appendChild(li);
}body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    line-height: 1.6;
}
header {
    background: #0a74da;
    color: white;
    padding: 10px 20px;
}
header h1 {
    margin: 0;
}
nav a {
    color: white;
    margin-right: 15px;
    text-decoration: none;
}
.hero {
    background: #f4f4f4;
    padding: 30px;
    text-align: center;
}
.services, .store, .contact {
    padding: 20px;
}
.service-card, .product-card {
    border: 1px solid #ccc;
    padding: 10px;
    margin-bottom: 10px;
}
footer {
    text-align: center;
    padding: 10px;
    background: #333;
    color: white;
}

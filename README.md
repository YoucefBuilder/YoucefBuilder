<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Rahim's Auto</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <!-- Header Section -->
  <header class="header">
    <div class="hero-content">
      <h1>Rahim's Auto</h1>
      <p>Your Trusted Source for French and German Auto Parts</p>
      <a href="#products" class="cta-button">Explore Products</a>
    </div>
  </header>

  <!-- Navigation Bar -->
  <nav class="navbar">
    <a href="#home">Home</a>
    <a href="#products">Products</a>
    <a href="#contact">Contact</a>
  </nav>

  <!-- About Us Section -->
  <section id="home" class="section">
    <h2>About Us</h2>
    <p>Rahim's Auto specializes in premium auto parts for top French and German car brands, ensuring quality and performance for Peugeot, Renault, DS Auto, and Volkswagen.</p>
  </section>

  <!-- Products Section -->
  <section id="products" class="section">
    <h2>Our Products</h2>
    <div class="product-slider">
      <div class="slide">
        <img src="https://via.placeholder.com/400x200" alt="Peugeot Brake Pads">
        <h3>Peugeot Brake Pads</h3>
        <p>High-quality brake pads for smooth performance.</p>
      </div>
      <div class="slide">
        <img src="https://via.placeholder.com/400x200" alt="Volkswagen Oil Filters">
        <h3>Volkswagen Oil Filters</h3>
        <p>Reliable filters for peak engine performance.</p>
      </div>
      <div class="slide">
        <img src="https://via.placeholder.com/400x200" alt="Renault Spark Plugs">
        <h3>Renault Spark Plugs</h3>
        <p>Efficient spark plugs for enhanced ignition.</p>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact" class="section">
    <h2>Contact Us</h2>
    <p>Email: support@rahimsauto.com</p>
    <p>Phone: +123 456 7890</p>
    <form class="contact-form">
      <input type="text" placeholder="Your Name" required>
      <input type="email" placeholder="Your Email" required>
      <textarea placeholder="Your Message" rows="5" required></textarea>
      <button type="submit">Send Message</button>
    </form>
  </section>

  <!-- Footer -->
  <footer class="footer">
    <p>&copy; 2024 Rahim's Auto. All Rights Reserved.</p>
  </footer>

  <!-- Link to JavaScript -->
  <script src="script.js"></script>
</body>
</html>
/* General Styles */
body {
  font-family: 'Arial', sans-serif;
  margin: 0;
  padding: 0;
  background: #f5f5f5;
  color: #333;
  line-height: 1.6;
  overflow-x: hidden;
}

header {
  background: linear-gradient(to right, #35424a, #64707d);
  color: #fff;
  text-align: center;
  padding: 3rem 1rem;
}

.hero-content {
  max-width: 800px;
  margin: auto;
}

.cta-button {
  display: inline-block;
  padding: 10px 20px;
  background: #ff9900;
  color: #fff;
  text-decoration: none;
  border-radius: 5px;
  margin-top: 20px;
  transition: background 0.3s;
}

.cta-button:hover {
  background: #cc7a00;
}

.navbar {
  background: #35424a;
  padding: 0.5rem;
  text-align: center;
}

.navbar a {
  color: #fff;
  text-decoration: none;
  margin: 0 1rem;
  transition: color 0.3s;
}

.navbar a:hover {
  color: #ff9900;
}

.section {
  padding: 2rem;
  text-align: center;
  background: #fff;
  margin: 20px 0;
  border-radius: 10px;
}

.product-slider {
  display: flex;
  overflow: hidden;
  gap: 1rem;
  margin-top: 1rem;
  padding: 1rem;
}

.slide {
  min-width: 300px;
  background: #f9f9f9;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  padding: 1rem;
  text-align: center;
  transition: transform 0.5s ease;
}

.slide img {
  width: 100%;
  border-radius: 10px;
}

footer {
  background: #35424a;
  color: #fff;
  text-align: center;
  padding: 1rem 0;
}

/* Contact Form */
.contact-form input,
.contact-form textarea {
  width: 100%;
  padding: 10px;
  margin: 10px 0;
  border: 1px solid #ccc;
  border-radius: 5px;
}

.contact-form button {
  background: #ff9900;
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 5px;
  cursor: pointer;
}

.contact-form button:hover {
  background: #cc7a00;
}
// Smooth Scroll for Navbar Links
document.querySelectorAll('.navbar a').forEach(link => {
  link.addEventListener('click', function (e) {
    e.preventDefault();
    document.querySelector(this.getAttribute('href')).scrollIntoView({
      behavior: 'smooth'
    });
  });
});

// Automatic Slider for Product Section
const slides = document.querySelectorAll('.slide');
let index = 0;

function showSlide() {
  slides.forEach((slide, i) => {
    slide.style.transform = translateX(${(i - index) * 100}%);
  });
}

setInterval(() => {
  index = (index + 1) % slides.length;
  showSlide();
}, 3000);

showSlide();

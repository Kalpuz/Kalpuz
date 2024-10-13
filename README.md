*Index.html*
```
<!DOCTYPE html>
<html>
<head>
  <title>Craftivo</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <nav>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Products</a></li>
        <li><a href="#">Artisans</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>
  <main>
    <section class="banner">
      <h1>Welcome to Craftivo</h1>
      <p>Discover unique crafts from skilled artisans</p>
      <button>Explore</button>
    </section>
    <section class="featured-products">
      <h2>Featured Products</h2>
      <div class="product-grid">
        <!-- product cards will be displayed here -->
      </div>
    </section>
  </main>
  <footer>
    <p>&copy; 2023 Craftivo</p>
  </footer>
  <script src="script.js"></script>
</body>
</html>
```

*Styles.css*
```
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

header {
  background-color: #333;
  color: #fff;
  padding: 1em;
  text-align: center;
}

nav ul {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: space-between;
}

nav li {
  margin-right: 20px;
}

nav a {
  color: #fff;
  text-decoration: none;
}

.banner {
  background-image: url('banner.jpg');
  background-size: cover;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  color: #fff;
}

.featured-products {
  padding: 2em;
}

.product-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

.product-card {
  background-color: #f7f7f7;
  padding: 1em;
  border: 1px solid #ddd;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.product-card img {
  width: 100%;
  height: 150px;
  object-fit: cover;
  border-radius: 10px 10px 0 0;
}
```

*Script.js*
```
// Add event listeners for navigation menu
document.addEventListener('DOMContentLoaded', () => {
  const navLinks = document.querySelectorAll('nav a');
  navLinks.forEach((link) => {
    link.addEventListener('click', (e) => {
      e.preventDefault();
      const target = link.getAttribute('href');
      document.querySelector(target).scrollIntoView({ behavior: 'smooth' });
    });
  });
});
```

*Products.html*, *Artisan.html*, and *Contact.html* will have similar structures.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AuraStyle | Premium Clothing Brand</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary: #2c3e50;
            --secondary: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --text: #333;
            --text-light: #777;
        }

        body {
            color: var(--text);
            line-height: 1.6;
            overflow-x: hidden;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }

        .btn {
            display: inline-block;
            padding: 12px 30px;
            background: var(--secondary);
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .btn:hover {
            background: #c0392b;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }

        .btn-outline {
            background: transparent;
            border: 2px solid var(--secondary);
            color: var(--secondary);
        }

        .btn-outline:hover {
            background: var(--secondary);
            color: white;
        }

        section {
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-title h2 {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 15px;
            position: relative;
            display: inline-block;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            width: 70px;
            height: 3px;
            background: var(--secondary);
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
        }

        .section-title p {
            color: var(--text-light);
            max-width: 600px;
            margin: 0 auto;
        }

        /* Header Styles */
        header {
            background: white;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary);
        }

        .logo span {
            color: var(--secondary);
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 30px;
        }

        nav ul li a {
            font-weight: 500;
            transition: color 0.3s;
            position: relative;
        }

        nav ul li a:hover {
            color: var(--secondary);
        }

        nav ul li a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            background: var(--secondary);
            bottom: -5px;
            left: 0;
            transition: width 0.3s;
        }

        nav ul li a:hover::after {
            width: 100%;
        }

        .header-icons {
            display: flex;
            align-items: center;
        }

        .header-icons div {
            margin-left: 20px;
            cursor: pointer;
            font-size: 1.2rem;
            transition: color 0.3s;
        }

        .header-icons div:hover {
            color: var(--secondary);
        }

        .mobile-menu {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)), url('https://images.unsplash.com/photo-1441986300917-64674bd600d8?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            color: white;
            text-align: center;
            margin-top: 70px;
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        /* Featured Products */
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 30px;
        }

        .product-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }

        .product-card:hover {
            transform: translateY(-10px);
        }

        .product-img {
            height: 300px;
            background-color: #f5f5f5;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
        }

        .product-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }

        .product-card:hover .product-img img {
            transform: scale(1.1);
        }

        .product-info {
            padding: 20px;
        }

        .product-info h3 {
            font-size: 1.2rem;
            margin-bottom: 10px;
        }

        .product-info p {
            color: var(--text-light);
            margin-bottom: 15px;
            font-size: 0.9rem;
        }

        .product-price {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .price {
            font-weight: 700;
            font-size: 1.2rem;
            color: var(--secondary);
        }

        /* About Section */
        .about {
            background: var(--light);
        }

        .about-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }

        .about-img {
            flex: 1;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .about-img img {
            width: 100%;
            height: auto;
            display: block;
        }

        .about-text {
            flex: 1;
        }

        .about-text h2 {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 20px;
        }

        .about-text p {
            margin-bottom: 20px;
            color: var(--text-light);
        }

        /* Testimonials */
        .testimonials {
            background: var(--primary);
            color: white;
        }

        .testimonials .section-title h2 {
            color: white;
        }

        .testimonials .section-title p {
            color: rgba(255, 255, 255, 0.7);
        }

        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }

        .testimonial-card {
            background: rgba(255, 255, 255, 0.1);
            padding: 30px;
            border-radius: 8px;
            backdrop-filter: blur(10px);
        }

        .testimonial-text {
            font-style: italic;
            margin-bottom: 20px;
        }

        .testimonial-author {
            display: flex;
            align-items: center;
        }

        .author-img {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            overflow: hidden;
            margin-right: 15px;
        }

        .author-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .author-info h4 {
            margin-bottom: 5px;
        }

        .author-info p {
            font-size: 0.9rem;
            opacity: 0.7;
        }

        /* Newsletter */
        .newsletter {
            background: var(--secondary);
            color: white;
            text-align: center;
        }

        .newsletter-content {
            max-width: 600px;
            margin: 0 auto;
        }

        .newsletter h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }

        .newsletter p {
            margin-bottom: 30px;
            font-size: 1.1rem;
        }

        .newsletter-form {
            display: flex;
            max-width: 500px;
            margin: 0 auto;
        }

        .newsletter-form input {
            flex: 1;
            padding: 15px;
            border: none;
            border-radius: 4px 0 0 4px;
            font-size: 1rem;
        }

        .newsletter-form button {
            background: var(--primary);
            color: white;
            border: none;
            padding: 0 25px;
            border-radius: 0 4px 4px 0;
            cursor: pointer;
            font-weight: 600;
            transition: background 0.3s;
        }

        .newsletter-form button:hover {
            background: #1a252f;
        }

        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 60px 0 30px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-column h3 {
            font-size: 1.3rem;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }

        .footer-column h3::after {
            content: '';
            position: absolute;
            width: 40px;
            height: 2px;
            background: var(--secondary);
            bottom: 0;
            left: 0;
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: 10px;
        }

        .footer-column ul li a {
            transition: color 0.3s;
            color: rgba(255, 255, 255, 0.7);
        }

        .footer-column ul li a:hover {
            color: var(--secondary);
            padding-left: 5px;
        }

        .social-icons {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .social-icons a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            transition: all 0.3s;
        }

        .social-icons a:hover {
            background: var(--secondary);
            transform: translateY(-5px);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.9rem;
        }

        /* Responsive Styles */
        @media (max-width: 992px) {
            .about-content {
                flex-direction: column;
            }
            
            .about-img, .about-text {
                flex: none;
                width: 100%;
            }
        }

        @media (max-width: 768px) {
            .mobile-menu {
                display: block;
            }

            nav {
                position: fixed;
                top: 70px;
                left: -100%;
                width: 80%;
                height: calc(100vh - 70px);
                background: white;
                transition: left 0.3s;
                box-shadow: 5px 0 15px rgba(0, 0, 0, 0.1);
            }

            nav.active {
                left: 0;
            }

            nav ul {
                flex-direction: column;
                padding: 30px;
            }

            nav ul li {
                margin: 0 0 20px 0;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .newsletter-form {
                flex-direction: column;
            }

            .newsletter-form input {
                border-radius: 4px;
                margin-bottom: 10px;
            }

            .newsletter-form button {
                border-radius: 4px;
                padding: 15px;
            }
        }

        @media (max-width: 576px) {
            .section-title h2 {
                font-size: 2rem;
            }

            .hero h1 {
                font-size: 2rem;
            }

            .hero p {
                font-size: 1rem;
            }

            .btn {
                padding: 10px 20px;
                font-size: 0.9rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <a href="#" class="logo">Aura<span>Style</span></a>
            
            <div class="mobile-menu">
                <i class="fas fa-bars"></i>
            </div>
            
            <nav>
                <ul>
                    <li><a href="#">Home</a></li>
                    <li><a href="#">Shop</a></li>
                    <li><a href="#">Collections</a></li>
                    <li><a href="#">About</a></li>
                    <li><a href="#">Contact</a></li>
                </ul>
            </nav>
            
            <div class="header-icons">
                <div class="search-icon">
                    <i class="fas fa-search"></i>
                </div>
                <div class="user-icon">
                    <i class="fas fa-user"></i>
                </div>
                <div class="cart-icon">
                    <i class="fas fa-shopping-bag"></i>
                </div>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container hero-content">
            <h1>Elevate Your Style</h1>
            <p>Discover our premium collection of clothing designed for the modern individual. Quality fabrics, timeless designs, and exceptional comfort.</p>
            <a href="#" class="btn">Shop Now</a>
        </div>
    </section>

    <!-- Featured Products -->
    <section class="featured">
        <div class="container">
            <div class="section-title">
                <h2>Featured Products</h2>
                <p>Check out our latest and most popular items</p>
            </div>
            
            <div class="products-grid">
                <!-- Product 1 -->
                <div class="product-card">
                    <div class="product-img">
                        <img src="https://images.unsplash.com/photo-1523381210434-271e8be1f52b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="Classic T-Shirt">
                    </div>
                    <div class="product-info">
                        <h3>Classic Cotton T-Shirt</h3>
                        <p>Premium quality cotton t-shirt with a perfect fit for everyday wear.</p>
                        <div class="product-price">
                            <span class="price">$29.99</span>
                            <a href="#" class="btn btn-outline">Add to Cart</a>
                        </div>
                    </div>
                </div>
                
                <!-- Product 2 -->
                <div class="product-card">
                    <div class="product-img">
                        <img src="https://images.unsplash.com/photo-1552374196-1ab2a1c593e8?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2187&q=80" alt="Denim Jacket">
                    </div>
                    <div class="product-info">
                        <h3>Vintage Denim Jacket</h3>
                        <p>Stylish denim jacket with a vintage wash and modern fit.</p>
                        <div class="product-price">
                            <span class="price">$79.99</span>
                            <a href="#" class="btn btn-outline">Add to Cart</a>
                        </div>
                    </div>
                </div>
                
                <!-- Product 3 -->
                <div class="product-card">
                    <div class="product-img">
                        <img src="https://images.unsplash.com/photo-1434389677669-e08b4cac3105?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2105&q=80" alt="Summer Dress">
                    </div>
                    <div class="product-info">
                        <h3>Floral Summer Dress</h3>
                        <p>Light and breezy floral dress perfect for summer days.</p>
                        <div class="product-price">
                            <span class="price">$49.99</span>
                            <a href="#" class="btn btn-outline">Add to Cart</a>
                        </div>
                    </div>
                </div>
                
                <!-- Product 4 -->
                <div class="product-card">
                    <div class="product-img">
                        <img src="https://images.unsplash.com/photo-1586790170083-2f9ceadc732d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2187&q=80" alt="Slim Fit Pants">
                    </div>
                    <div class="product-info">
                        <h3>Slim Fit Chino Pants</h3>
                        <p>Comfortable and stylish chino pants with a modern slim fit.</p>
                        <div class="product-price">
                            <span class="price">$59.99</span>
                            <a href="#" class="btn btn-outline">Add to Cart</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about">
        <div class="container">
            <div class="about-content">
                <div class="about-img">
                    <img src="https://images.unsplash.com/photo-1441986300917-64674bd600d8?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="About Us">
                </div>
                <div class="about-text">
                    <h2>Our Story</h2>
                    <p>Founded in 2015, AuraStyle began with a simple mission: to create high-quality, stylish clothing that doesn't compromise on comfort or sustainability.</p>
                    <p>We believe that what you wear should reflect your personality while feeling great on your skin. That's why we source only the finest materials and work with ethic
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Definitive Word - Premium Ebook Store</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* === CUSTOM COLOR THEME === */
        :root {
            --primary: #1a365d;      /* Deep navy blue */
            --secondary: #d69e2e;    /* Gold accent */
            --accent: #c53030;       /* Rich red */
            --success: #38a169;      /* Green */
            --light: #f7fafc;        /* Light background */
            --dark: #2d3748;         /* Dark text */
            --text: #2d3748;
            --background: #ffffff;
            --gradient: linear-gradient(135deg, #1a365d 0%, #2d3748 100%);
        }

        /* === MODERN FONTS === */
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            line-height: 1.7;
            color: var(--text);
            background: var(--background);
            font-weight: 400;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        /* === PREMIUM ADMIN PANEL === */
        .admin-panel {
            background: var(--gradient);
            color: white;
            padding: 12px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 20px rgba(0,0,0,0.1);
            border-bottom: 3px solid var(--secondary);
        }

        .admin-controls {
            display: flex;
            gap: 12px;
            flex-wrap: wrap;
            align-items: center;
            font-size: 0.9rem;
        }

        .admin-btn {
            background: rgba(255,255,255,0.1);
            color: white;
            border: 1px solid rgba(255,255,255,0.2);
            padding: 8px 16px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 0.85rem;
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
        }

        .admin-btn:hover {
            background: var(--secondary);
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(214, 158, 46, 0.3);
        }

        .stats {
            margin-left: auto;
            display: flex;
            gap: 20px;
            font-size: 0.85rem;
            opacity: 0.9;
        }

        .stat-item {
            display: flex;
            align-items: center;
            gap: 5px;
        }

        /* === LUXURY HEADER === */
        header {
            background: white;
            box-shadow: 0 2px 30px rgba(0,0,0,0.08);
            position: sticky;
            top: 43px;
            z-index: 999;
            border-bottom: 1px solid #e2e8f0;
        }

        .header-top {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }

        .logo {
            display: flex;
            align-items: center;
            font-size: 2rem;
            font-weight: 700;
            color: var(--primary);
            text-decoration: none;
        }

        .logo i {
            color: var(--secondary);
            margin-right: 12px;
            font-size: 2.2rem;
        }

        .logo-text {
            background: var(--gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .nav-main {
            display: flex;
            gap: 35px;
        }

        .nav-main a {
            color: var(--dark);
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            position: relative;
            padding: 8px 0;
        }

        .nav-main a:hover {
            color: var(--primary);
        }

        .nav-main a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--secondary);
            transition: width 0.3s ease;
        }

        .nav-main a:hover::after {
            width: 100%;
        }

        .header-actions {
            display: flex;
            align-items: center;
            gap: 25px;
        }

        .search-bar {
            position: relative;
        }

        .search-bar input {
            padding: 10px 20px;
            border: 1px solid #e2e8f0;
            border-radius: 25px;
            width: 240px;
            font-size: 0.9rem;
            transition: all 0.3s ease;
            background: var(--light);
        }

        .search-bar input:focus {
            outline: none;
            border-color: var(--secondary);
            box-shadow: 0 0 0 3px rgba(214, 158, 46, 0.1);
        }

        .icon-btn {
            background: none;
            border: none;
            font-size: 1.3rem;
            color: var(--dark);
            cursor: pointer;
            position: relative;
            transition: all 0.3s ease;
            padding: 8px;
            border-radius: 50%;
        }

        .icon-btn:hover {
            color: var(--primary);
            background: var(--light);
            transform: translateY(-2px);
        }

        .badge {
            background: var(--accent);
            color: white;
            border-radius: 50%;
            width: 18px;
            height: 18px;
            font-size: 0.7rem;
            display: flex;
            align-items: center;
            justify-content: center;
            position: absolute;
            top: 0;
            right: 0;
            font-weight: 600;
        }

        /* === LUXURY HERO SECTION === */
        .hero {
            background: var(--gradient);
            color: white;
            padding: 100px 0;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('https://images.unsplash.com/photo-1457369804613-52c61a468e7d?ixlib=rb-4.0.3&auto=format&fit=crop&w=2000&q=80') center/cover;
            opacity: 0.1;
        }

        .hero-content {
            position: relative;
            z-index: 2;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            font-weight: 700;
            line-height: 1.2;
        }

        .hero p {
            font-size: 1.3rem;
            max-width: 600px;
            margin: 0 auto 30px;
            opacity: 0.9;
            font-weight: 300;
        }

        .hero-actions {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
            margin-top: 40px;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            padding: 15px 30px;
            background: var(--secondary);
            color: var(--primary);
            border: none;
            border-radius: 10px;
            cursor: pointer;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s ease;
            font-size: 1rem;
        }

        .btn:hover {
            background: #ecc94b;
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(214, 158, 46, 0.3);
        }

        .btn-secondary {
            background: transparent;
            border: 2px solid rgba(255,255,255,0.3);
            color: white;
        }

        .btn-secondary:hover {
            background: white;
            color: var(--primary);
            border-color: white;
        }

        /* === FEATURES SECTION === */
        .features {
            padding: 80px 0;
            background: var(--light);
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
            color: var(--primary);
            font-size: 2.5rem;
            font-weight: 700;
        }

        .section-subtitle {
            text-align: center;
            color: var(--dark);
            font-size: 1.2rem;
            max-width: 600px;
            margin: 0 auto 50px;
            opacity: 0.8;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 40px;
        }

        .feature-card {
            background: white;
            padding: 40px 30px;
            border-radius: 15px;
            text-align: center;
            transition: all 0.3s ease;
            border: 1px solid #e2e8f0;
            position: relative;
            overflow: hidden;
        }

        .feature-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: var(--gradient);
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
        }

        .feature-icon {
            font-size: 3rem;
            color: var(--secondary);
            margin-bottom: 20px;
        }

        .feature-card h3 {
            font-size: 1.4rem;
            margin-bottom: 15px;
            color: var(--primary);
        }

        /* === PREMIUM BOOKS GRID === */
        .books-section {
            padding: 80px 0;
        }

        .books-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }

        .book-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(0,0,0,0.08);
            transition: all 0.3s ease;
            position: relative;
            border: 1px solid #e2e8f0;
        }

        .book-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.15);
        }

        .book-badge {
            position: absolute;
            top: 15px;
            right: 15px;
            background: var(--accent);
            color: white;
            padding: 6px 12px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
            z-index: 2;
        }

        .book-cover {
            height: 320px;
            overflow: hidden;
            position: relative;
        }

        .book-cover img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .book-card:hover .book-cover img {
            transform: scale(1.1);
        }

        .book-actions {
            position: absolute;
            top: 15px;
            left: 15px;
            display: flex;
            gap: 8px;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .book-card:hover .book-actions {
            opacity: 1;
        }

        .action-btn {
            width: 40px;
            height: 40px;
            background: white;
            border: none;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            box-shadow: 0 4px 12px rgba(0,0,0,0.15);
            transition: all 0.3s ease;
            color: var(--dark);
        }

        .action-btn:hover {
            background: var(--secondary);
            color: white;
            transform: scale(1.1);
        }

        .book-info {
            padding: 25px;
        }

        .book-title {
            font-weight: 600;
            margin-bottom: 8px;
            font-size: 1.2rem;
            color: var(--primary);
            line-height: 1.4;
        }

        .book-author {
            color: #718096;
            margin-bottom: 15px;
            font-size: 0.95rem;
        }

        .book-price {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .price {
            font-weight: 700;
            color: var(--accent);
            font-size: 1.3rem;
        }

        /* === BLOG SECTION === */
        .blog-section {
            padding: 80px 0;
            background: var(--light);
        }

        .blog-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
        }

        .blog-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(0,0,0,0.08);
            transition: all 0.3s ease;
        }

        .blog-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.15);
        }

        .blog-image {
            height: 220px;
            overflow: hidden;
        }

        .blog-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .blog-card:hover .blog-image img {
            transform: scale(1.05);
        }

        .blog-content {
            padding: 25px;
        }

        .blog-meta {
            display: flex;
            gap: 15px;
            margin-bottom: 12px;
            font-size: 0.85rem;
            color: #718096;
        }

        .blog-title {
            font-size: 1.3rem;
            margin-bottom: 12px;
            color: var(--primary);
            line-height: 1.4;
        }

        /* === NEWSLETTER === */
        .newsletter {
            background: var(--gradient);
            color: white;
            padding: 80px 0;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .newsletter::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('https://images.unsplash.com/photo-1457369804613-52c61a468e7d?ixlib=rb-4.0.3&auto=format&fit=crop&w=2000&q=80') center/cover;
            opacity: 0.1;
        }

        .newsletter-content {
            position: relative;
            z-index: 2;
        }

        .newsletter-form {
            display: flex;
            max-width: 450px;
            margin: 30px auto;
            background: white;
            border-radius: 50px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        }

        .newsletter-form input {
            flex: 1;
            padding: 15px 25px;
            border: none;
            font-size: 1rem;
        }

        .newsletter-form input:focus {
            outline: none;
        }

        .newsletter-form button {
            background: var(--secondary);
            color: var(--primary);
            border: none;
            padding: 0 30px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .newsletter-form button:hover {
            background: #ecc94b;
        }

        /* === LUXURY FOOTER === */
        footer {
            background: var(--primary);
            color: white;
            padding: 60px 0 20px;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 50px;
            margin-bottom: 40px;
        }

        .footer-column h3 {
            margin-bottom: 25px;
            color: var(--secondary);
            font-size: 1.3rem;
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: 12px;
        }

        .footer-column a {
            color: #cbd5e0;
            text-decoration: none;
            transition: all 0.3s ease;
            font-weight: 400;
        }

        .footer-column a:hover {
            color: white;
            padding-left: 5px;
        }

        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: rgba(255,255,255,0.1);
            color: white;
            border-radius: 50%;
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .social-links a:hover {
            background: var(--secondary);
            color: var(--primary);
            transform: translateY(-3px);
        }

        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid #2d3748;
            color: #a0aec0;
            font-size: 0.9rem;
        }

        /* === RESPONSIVE DESIGN === */
        @media (max-width: 768px) {
            .header-top {
                flex-direction: column;
                gap: 20px;
            }
            
            .nav-main {
                gap: 20px;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero-actions {
                flex-direction: column;
                align-items: center;
            }
            
            .admin-controls {
                flex-direction: column;
                align-items: stretch;
            }
            
            .stats {
                margin-left: 0;
                justify-content: space-around;
            }
            
            .search-bar input {
                width: 200px;
            }
        }

        @media (max-width: 480px) {
            .hero h1 {
                font-size: 2rem;
            }
            
            .section-title {
                font-size: 2rem;
            }
            
            .books-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Notification -->
    <div class="notification" id="notification"></div>

    <!-- Premium Admin Panel -->
    <div class="admin-panel">
        <div class="container">
            <div class="admin-controls">
                <button class="admin-btn" onclick="openModal('addBookModal')">
                    <i class="fas fa-plus"></i> Add Book
                </button>
                <button class="admin-btn" onclick="openModal('addBlogModal')">
                    <i class="fas fa-blog"></i> Add Blog
                </button>
                <button class="admin-btn" onclick="openModal('bookListModal')">
                    <i class="fas fa-cog"></i> Manage
                </button>
                <div class="stats">
                    <div class="stat-item">
                        <i class="fas fa-book"></i>
                        <span>Books: <span id="bookCount">0</span></span>
                    </div>
                    <div class="stat-item">
                        <i class="fas fa-blog"></i>
                        <span>Blogs: <span id="blogCount">0</span></span>
                    </div>
                    <div class="stat-item">
                        <i class="fas fa-shopping-cart"></i>
                        <span>Cart: <span id="cartCountDisplay">0</span></span>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Luxury Header -->
    <header>
        <div class="container">
            <div class="header-top">
                <a href="#" class="logo">
                    <i class="fas fa-crown"></i>
                    <span class="logo-text">The Definitive Word</span>
                </a>
                
                <nav class="nav-main">
                    <a href="#books">Books</a>
                    <a href="#blog">Blog</a>
                    <a href="#features">Features</a>
                    <a href="#about">About</a>
                </nav>

                <div class="header-actions">
                    <div class="search-bar">
                        <input type="text" placeholder="Search books..." onkeypress="handleSearch(event)">
                    </div>
                    <button class="icon-btn" onclick="toggleWishlist()" title="Wishlist">
                        <i class="fas fa-heart"></i>
                        <span class="badge" id="wishlistCount">0</span>
                    </button>
                    <button class="icon-btn" onclick="openCart()" title="Cart">
                        <i class="fas fa-shopping-cart"></i>
                        <span class="badge" id="cartCount">0</span>
                    </button>
                    <button class="icon-btn" onclick="openModal('loginModal')" title="Account">
                        <i class="fas fa-user"></i>
                    </button>
                </div>
            </div>
        </div>
    </header>

    <!-- Luxury Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Premium Ebooks, Curated for Excellence</h1>
                <p>Discover hand-picked literature from acclaimed authors. Your journey to exceptional reading starts here.</p>
                <div class="hero-actions">
                    <a href="#books" class="btn">
                        <i class="fas fa-gem"></i>
                        Explore Collection
                    </a>
                    <a href="#blog" class="btn btn-secondary">
                        <i class="fas fa-newspaper"></i>
                        Read Our Blog
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="features" id="features">
        <div class="container">
            <h2 class="section-title">Why Readers Choose Us</h2>
            <p class="section-subtitle">Experience the difference with our premium ebook service</p>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-rocket"></i>
                    </div>
                    <h3>Instant Access</h3>
                    <p>Download your ebooks immediately after purchase, read anywhere on any device</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-star"></i>
                    </div>
                    <h3>Curated Selection</h3>
                    <p>Every book is hand-picked by our team of literary experts for quality and impact</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <h3>DRM-Free</h3>
                    <p>Own your books forever with our DRM-free policy. No restrictions, just reading</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-users"></i>
                    </div>
                    <h3>Community</h3>
                    <p>Join our community of passionate readers for discussions and author events</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Books Section -->
    <section class="books-section" id="books">
        <div class="container">
            <h2 class="section-title">Featured Collection</h2>
            <p class="section-subtitle">Discover our hand-picked selection of exceptional reads</p>
            <div class="books-grid" id="booksGrid">
                <!-- Books will be loaded here -->
            </div>
        </div>
    </section>

    <!-- Blog Section -->
    <section class="blog-section" id="blog">
        <div class="container">
            <h2 class="section-title">From The Blog</h2>
            <p class="section-subtitle">Insights, reviews, and literary discussions</p>
            <div class="blog-grid" id="blogGrid">
                <!-- Blog posts will be loaded here -->
            </div>
        </div>
    </section>

    <!-- Newsletter -->
    <section class="newsletter">
        <div class="container">
            <div class="newsletter-content">
                <h2>Stay in the Literary Loop</h2>
                <p>Get exclusive book recommendations, author interviews, and special offers delivered to your inbox</p>
                <form class="newsletter-form" onsubmit="subscribeNewsletter(event)">
                    <input type="email" placeholder="Enter your email address" required>
                    <button type="submit">Subscribe</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Luxury Footer -->
    <footer>
        <div class="container">
            <div class="footer-grid">
                <div class="footer-column">
                    <h3>The Definitive Word</h3>
                    <p>Your premier destination for exceptional ebooks and literary content. Quality curated, excellence delivered.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-goodreads"></i></a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Explore</h3>
                    <ul>
                        <li><a href="#books">Book Collection</a></li>
                        <li><a href="#blog">Blog & Articles</a></li>
                        <li><a href="#features">Features</a></li>
                        <li><a href="#about">About Us</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Categories</h3>
                    <ul>
                        <li><a href="#">Literary Fiction</a></li>
                        <li><a href="#">Business & Finance</a></li>
                        <li><a href="#">Personal Development</a></li>
                        <li><a href="#">Science & Technology</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Support</h3>
                    <ul>
                        <li><a href="#">Help Center</a></li>
                        <li><a href="#">Contact Support</a></li>
                        <li><a href="#">Privacy Policy</a></li>
                        <li><a href="#">Terms of Service</a></li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2024 The Definitive Word. All rights reserved. | Premium Ebook Store</p>
            </div>
        </div>
    </footer>

    <script>
        // Store Data
        let books = JSON.parse(localStorage.getItem('storeBooks')) || [];
        let blogPosts = JSON.parse(localStorage.getItem('storeBlogs')) || [];
        let cart = [];
        let wishlist = [];

        // Initialize Store
        function initializeStore() {
            displayBooks();
            displayBlogPosts();
            updateStats();
            showNotification('Welcome to The Definitive Word! 🎉');
        }

        // Book Management
        function displayBooks() {
            const grid = document.getElementById('booksGrid');
            grid.innerHTML = '';

            if (books.length === 0) {
                grid.innerHTML = `
                    <div style="text-align: center; grid-column: 1/-1; padding: 60px; color: #718096;">
                        <i class="fas fa-book-open" style="font-size: 4rem; margin-bottom: 20px; opacity: 0.5;"></i>
                        <h3 style="margin-bottom: 15px; color: var(--primary);">No Books Yet</h3>
                        <p>Use the admin panel to add your first book to the collection</p>
                    </div>
                `;
                return;
            }

            books.forEach(book => {
                const isInWishlist = wishlist.includes(book.id);
                const card = document.createElement('div');
                card.className = 'book-card';
                card.innerHTML = `
                    ${book.badge ? `<div class="book-badge">${book.badge}</div>` : ''}
                    <div class="book-actions">
                        <button class="action-btn" onclick="toggleWishlistItem(${book.id})" title="${isInWishlist ? 'Remove from Wishlist' : 'Add to Wishlist'}">
                            <i class="fas fa-heart" style="color: ${isInWishlist ? '#c53030' : '#718096'};"></i>
                        </button>
                    </div>
                    <div class="book-cover">
                        <img src="${book.image}" alt="${book.title}">
                    </div>
                    <div class="book-info">
                        <h3 class="book-title">${book.title}</h3>
                        <p class="book-author">by ${book.author}</p>
                        <div class="book-price">
                            <span class="price">$${book.price}</span>
                            <button class="btn" onclick="addToCart(${book.id})" style="padding: 10px 20px; font-size: 0.9rem;">
                                <i class="fas fa-shopping-cart"></i>
                                Add to Cart
                            </button>
                        </div>
                    </div>
                `;
                grid.appendChild(card);
            });
        }

        // Blog Management
        function displayBlogPosts() {
            const grid = document.getElementById('blogGrid');
            grid.innerHTML = '';

            if (blogPosts.length === 0) {
                grid.innerHTML = `
                    <div style="text-align: center; grid-column: 1/-1; padding: 60px; color: #718096;">
                        <i class="fas fa-blog" style="font-size: 4rem; margin-bottom: 20px; opacity: 0.5;"></i>
                        <h3 style="margin-bottom: 15px; color: var(--primary);">No Blog Posts Yet</h3>
                        <p>Use the admin panel to publish your first blog post</p>
                    </div>
                `;
                return;
            }

            blogPosts.forEach(post => {
                const card = document.createElement('div');
                card.className = 'blog-card';
                card.innerHTML = `
                    <div class="blog-image">
                        <img src="${post.image}" alt="${post.title}">
                    </div>
                    <div class="blog-content">
                        <div class="blog-meta">
                            <span><i class="fas fa-calendar"></i> ${post.date}</span>
                            <span><i class="fas fa-tag"></i> ${post.category}</span>
                        </div>
                        <h3 class="blog-title">${post.title}</h3>
                        <p style="color: #718096; line-height: 1.6;">${post.content.substring(0, 120)}...</p>
                        <button class="btn" style="margin-top: 20px; padding: 10px 20px; font-size: 0.9rem;" onclick="showNotification('Reading: ' + '${post.title}')">
                            Read Article
                        </button>
                    </div>
                `;
                grid.appendChild(card);
            });
        }

        // Cart Functions
        function addToCart(bookId) {
            const book = books.find(b => b.id === bookId);
            if (!book) return;

            const existing = cart.find(item => item.id === bookId);
            if (existing) {
                existing.quantity++;
            } else {
                cart.push({...book, quantity: 1});
            }

            updateCartDisplay();
            showNotification(`"${book.title}" added to cart! 📚`);
        }

        function updateCartDisplay() {
            const count = cart.reduce((sum, item) => sum + item.quantity, 0);
            document.getElementById('cartCount').textContent = count;
            document.getElementById('cartCountDisplay').textContent = count;
        }

        function openCart() {
            showNotification(`You have ${cart.reduce((sum, item) => sum + item.quantity, 0)} items in your cart`);
        }

        // Wishlist Functions
        function toggleWishlistItem(bookId) {
            const index = wishlist.indexOf(bookId);
            if (index > -1) {
                wishlist.splice(index, 1);
                showNotification('Removed from wishlist');
            } else {
                wishlist.push(bookId);
                showNotification('Added to wishlist! 💖');
            }
            document.getElementById('wishlistCount').textContent = wishlist.length;
            displayBooks();
        }

        function toggleWishlist() {
            showNotification(`You have ${wishlist.length} items in your wishlist`);
        }

        // Admin Functions
        function openModal(modalId) {
            showNotification('Admin feature ready - Add your content!');
        }

        function updateStats() {
            document.getElementById('bookCount').textContent = books.length;
            document.getElementById('blogCount').textContent = blogPosts.length;
        }

        function showNotification(message, isError = false) {
            const notification = document.getElementById('notification');
            notification.textContent = message;
            notification.style.background = isError ? '#c53030' : '#38a169';
            notification.className = 'notification show';
            setTimeout(() => notification.className = 'notification', 4000);
        }

        function handleSearch(event) {
            if (event.key === 'Enter') {
                showNotification(`Searching for: "${event.target.value}"`);
                event.target.value = '';
            }
        }

        function subscribeNewsletter(event) {
            event.preventDefault();
            showNotification('🎉 Welcome to our literary community! Check your email for confirmation.');
            event.target.reset();
        }

        // Initialize store when page loads
        document.addEventListener('DOMContentLoaded', initializeStore);
    </script>
</body>
</html>

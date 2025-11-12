<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Definitive Word - Premium Ebook Store</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #1a365d;
            --secondary: #d69e2e;
            --accent: #c53030;
            --light: #f7fafc;
            --success: #38a169;
            --dark: #2d3748;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background: #f9f9f9;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        /* === COMPACT EDIT MODE === */
        .edit-mode {
            background: linear-gradient(135deg, #1a365d, #c53030);
            color: white;
            padding: 8px 0;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 10000;
            text-align: center;
            box-shadow: 0 2px 10px rgba(0,0,0,0.3);
            border-bottom: 2px solid #d69e2e;
            font-size: 0.9rem;
        }

        .edit-btn {
            background: #d69e2e;
            color: #1a365d;
            border: none;
            padding: 6px 12px;
            border-radius: 6px;
            cursor: pointer;
            font-weight: bold;
            margin: 0 5px;
            font-size: 0.85rem;
            transition: all 0.3s ease;
        }

        .edit-btn:hover {
            background: #ecc94b;
            transform: translateY(-1px);
        }

        .edit-btn.large {
            padding: 7px 15px;
            font-size: 0.9rem;
        }

        /* === EDITABLE ELEMENTS === */
        .editable {
            position: relative;
            border: 2px dashed transparent;
            transition: all 0.3s ease;
            padding: 5px;
            border-radius: 6px;
            margin: 1px;
        }

        .edit-mode-on .editable {
            border-color: #d69e2e !important;
            background: rgba(214, 158, 46, 0.15) !important;
        }

        .editable:hover {
            background: rgba(214, 158, 46, 0.25) !important;
        }

        .edit-icon {
            position: absolute;
            top: -6px;
            right: -6px;
            background: #d69e2e;
            color: #1a365d;
            border-radius: 50%;
            width: 22px;
            height: 22px;
            display: none;
            align-items: center;
            justify-content: center;
            font-size: 12px;
            cursor: pointer;
            z-index: 1000;
            font-weight: bold;
            box-shadow: 0 2px 6px rgba(0,0,0,0.3);
        }

        .edit-mode-on .edit-icon {
            display: flex;
        }

        /* === HEADER - ADJUSTED FOR SMALLER EDIT BAR === */
        header {
            background: white;
            box-shadow: 0 2px 20px rgba(0,0,0,0.1);
            position: sticky;
            top: 40px;
            z-index: 999;
        }

        .header-top {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 12px 0;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: #1a365d;
        }

        .nav-main {
            display: flex;
            gap: 30px;
        }

        .nav-main a {
            color: #333;
            text-decoration: none;
            font-weight: 600;
            padding: 10px 0;
            position: relative;
            transition: all 0.3s ease;
            font-size: 0.95rem;
        }

        .nav-main a:hover,
        .nav-main a.active {
            color: #d69e2e;
        }

        .nav-main a.active::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 2px;
            background: #d69e2e;
        }

        .header-actions {
            display: flex;
            gap: 15px;
            align-items: center;
        }

        .cart-icon {
            position: relative;
            cursor: pointer;
        }

        .cart-count {
            position: absolute;
            top: -8px;
            right: -8px;
            background: #c53030;
            color: white;
            border-radius: 50%;
            width: 20px;
            height: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.7rem;
            font-weight: bold;
        }

        /* === SECTIONS === */
        .section {
            padding: 70px 0;
            min-height: 65vh;
        }

        .section-title {
            text-align: center;
            margin-bottom: 40px;
            color: #1a365d;
            font-size: 2.5rem;
            font-weight: 700;
        }

        .section-subtitle {
            text-align: center;
            max-width: 700px;
            margin: 0 auto 50px;
            font-size: 1.1rem;
            color: #666;
        }

        /* === HERO SECTION === */
        .hero {
            background: linear-gradient(135deg, #1a365d 0%, #2d3748 100%);
            color: white;
            padding: 100px 0;
            text-align: center;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            font-weight: 700;
        }

        .hero p {
            font-size: 1.2rem;
            max-width: 600px;
            margin: 0 auto 30px;
            opacity: 0.9;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            padding: 12px 25px;
            background: #d69e2e;
            color: #1a365d;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-weight: 700;
            text-decoration: none;
            transition: all 0.3s ease;
            font-size: 1rem;
        }

        .btn:hover {
            background: #ecc94b;
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(0,0,0,0.15);
        }

        .btn-secondary {
            background: transparent;
            color: white;
            border: 2px solid #d69e2e;
        }

        .btn-secondary:hover {
            background: rgba(214, 158, 46, 0.1);
        }

        /* === BLOG SECTION === */
        .blog-section {
            background: #f7fafc;
        }

        .blog-container {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 40px;
        }

        .blog-posts {
            display: grid;
            gap: 30px;
        }

        .blog-post {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
        }

        .blog-post:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }

        .blog-post-image {
            height: 200px;
            overflow: hidden;
        }

        .blog-post-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .blog-post:hover .blog-post-image img {
            transform: scale(1.05);
        }

        .blog-post-content {
            padding: 25px;
        }

        .blog-post-meta {
            display: flex;
            gap: 15px;
            margin-bottom: 15px;
            font-size: 0.85rem;
            color: #666;
        }

        .blog-post-category {
            background: #d69e2e;
            color: white;
            padding: 4px 10px;
            border-radius: 20px;
            font-size: 0.75rem;
            font-weight: 600;
        }

        .blog-post-title {
            font-size: 1.4rem;
            margin-bottom: 15px;
            color: #1a365d;
        }

        .blog-post-excerpt {
            color: #666;
            margin-bottom: 20px;
        }

        .blog-post-footer {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding-top: 15px;
            border-top: 1px solid #e2e8f0;
        }

        .blog-post-actions {
            display: flex;
            gap: 15px;
        }

        .blog-post-actions button {
            background: none;
            border: none;
            color: #666;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 5px;
            transition: color 0.3s ease;
        }

        .blog-post-actions button:hover {
            color: #d69e2e;
        }

        /* Blog Sidebar */
        .blog-sidebar {
            display: flex;
            flex-direction: column;
            gap: 30px;
        }

        .sidebar-widget {
            background: white;
            padding: 25px;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }

        .widget-title {
            font-size: 1.2rem;
            margin-bottom: 20px;
            color: #1a365d;
            padding-bottom: 10px;
            border-bottom: 2px solid #d69e2e;
        }

        .categories-list {
            list-style: none;
        }

        .categories-list li {
            margin-bottom: 10px;
            padding-bottom: 10px;
            border-bottom: 1px solid #e2e8f0;
        }

        .categories-list a {
            color: #4a5568;
            text-decoration: none;
            transition: color 0.3s ease;
            display: flex;
            justify-content: space-between;
        }

        .categories-list a:hover {
            color: #d69e2e;
        }

        .categories-list span {
            background: #e2e8f0;
            padding: 2px 8px;
            border-radius: 10px;
            font-size: 0.8rem;
        }

        .recent-posts-list {
            list-style: none;
        }

        .recent-posts-list li {
            margin-bottom: 15px;
            padding-bottom: 15px;
            border-bottom: 1px solid #e2e8f0;
        }

        .recent-post {
            display: flex;
            gap: 15px;
        }

        .recent-post-image {
            width: 70px;
            height: 70px;
            border-radius: 8px;
            overflow: hidden;
            flex-shrink: 0;
        }

        .recent-post-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .recent-post-content h4 {
            font-size: 0.95rem;
            margin-bottom: 5px;
            color: #1a365d;
        }

        .recent-post-content .post-date {
            font-size: 0.8rem;
            color: #666;
        }

        .tags-cloud {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .tag {
            background: #e2e8f0;
            color: #4a5568;
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 0.85rem;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .tag:hover {
            background: #d69e2e;
            color: white;
        }

        /* Blog Create Post */
        .blog-create-post {
            background: white;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            margin-top: 40px;
        }

        .create-post-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 25px;
        }

        .create-post-title {
            font-size: 1.5rem;
            color: #1a365d;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: #1a365d;
        }

        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 1rem;
            transition: all 0.3s ease;
        }

        .form-control:focus {
            border-color: #d69e2e;
            outline: none;
            box-shadow: 0 0 0 3px rgba(214, 158, 46, 0.2);
        }

        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
        }

        /* === BOOKS SECTION === */
        .books-section {
            background: white;
        }

        .books-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .book-card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
            transition: all 0.3s ease;
            position: relative;
        }

        .book-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
        }

        .book-cover {
            height: 250px;
            overflow: hidden;
        }

        .book-cover img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .book-card:hover .book-cover img {
            transform: scale(1.05);
        }

        .book-info {
            padding: 20px;
        }

        .book-title {
            font-size: 1.3rem;
            font-weight: 700;
            margin-bottom: 8px;
            color: #1a365d;
        }

        .book-author {
            color: #666;
            margin-bottom: 15px;
            font-size: 0.95rem;
        }

        .book-price {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .price {
            font-size: 1.5rem;
            font-weight: 700;
            color: #1a365d;
        }

        /* === COMMUNITY SECTION === */
        .community-section {
            background: white;
        }

        .community-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
        }

        .discussion-forum {
            background: #f7fafc;
            padding: 30px;
            border-radius: 12px;
        }

        .discussion-list {
            margin-top: 20px;
        }

        .discussion-item {
            background: white;
            padding: 20px;
            border-radius: 8px;
            margin-bottom: 15px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.05);
        }

        .discussion-meta {
            display: flex;
            justify-content: space-between;
            font-size: 0.85rem;
            color: #666;
            margin-top: 10px;
        }

        .user-reviews {
            background: #f7fafc;
            padding: 30px;
            border-radius: 12px;
        }

        .review-item {
            background: white;
            padding: 20px;
            border-radius: 8px;
            margin-bottom: 15px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.05);
        }

        .review-header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
        }

        .review-rating {
            color: #d69e2e;
        }

        /* === PAYMENT SECTION === */
        .payment-section {
            background: #f7fafc;
        }

        .payment-container {
            max-width: 800px;
            margin: 0 auto;
            background: white;
            padding: 40px;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }

        .payment-methods {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }

        .payment-method {
            border: 2px solid #e2e8f0;
            border-radius: 8px;
            padding: 20px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .payment-method:hover, .payment-method.active {
            border-color: #d69e2e;
            background: rgba(214, 158, 46, 0.05);
        }

        .payment-method i {
            font-size: 2rem;
            margin-bottom: 10px;
            color: #4a5568;
        }

        .payment-form {
            margin-top: 30px;
        }

        /* === CART MODAL === */
        .cart-modal {
            position: fixed;
            top: 0;
            right: -400px;
            width: 380px;
            height: 100%;
            background: white;
            box-shadow: -5px 0 15px rgba(0,0,0,0.1);
            z-index: 10001;
            transition: right 0.3s ease;
            padding: 20px;
            overflow-y: auto;
        }

        .cart-modal.active {
            right: 0;
        }

        .cart-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 1px solid #e2e8f0;
        }

        .cart-items {
            margin-bottom: 20px;
        }

        .cart-item {
            display: flex;
            gap: 15px;
            padding: 15px 0;
            border-bottom: 1px solid #e2e8f0;
        }

        .cart-item img {
            width: 60px;
            height: 80px;
            object-fit: cover;
            border-radius: 4px;
        }

        .cart-item-details {
            flex: 1;
        }

        .cart-item-title {
            font-weight: 600;
            margin-bottom: 5px;
        }

        .cart-item-price {
            color: #1a365d;
            font-weight: 600;
        }

        .cart-item-remove {
            color: #c53030;
            background: none;
            border: none;
            cursor: pointer;
        }

        .cart-total {
            display: flex;
            justify-content: space-between;
            font-size: 1.2rem;
            font-weight: 700;
            margin: 20px 0;
            padding-top: 15px;
            border-top: 1px solid #e2e8f0;
        }

        /* === MODAL === */
        .edit-modal {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.7);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 10001;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s ease;
        }

        .edit-modal.active {
            opacity: 1;
            visibility: visible;
        }

        .modal-content {
            background: white;
            width: 90%;
            max-width: 600px;
            border-radius: 12px;
            padding: 30px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        }

        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
        }

        .modal-header h2 {
            color: #1a365d;
        }

        .close-modal {
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: #666;
            transition: color 0.3s ease;
        }

        .close-modal:hover {
            color: #c53030;
        }

        .modal-body textarea {
            width: 100%;
            min-height: 150px;
            padding: 15px;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 1rem;
            font-family: inherit;
            resize: vertical;
        }

        .modal-footer {
            display: flex;
            justify-content: flex-end;
            gap: 15px;
            margin-top: 20px;
        }

        /* === NOTIFICATION === */
        .notification {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: #d69e2e;
            color: white;
            padding: 15px 25px;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            z-index: 10002;
            transform: translateY(100px);
            opacity: 0;
            transition: all 0.3s ease;
        }

        .notification.show {
            transform: translateY(0);
            opacity: 1;
        }

        /* === FOOTER === */
        footer {
            background: #1a365d;
            color: white;
            padding: 50px 0 20px;
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
            color: #d69e2e;
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: 10px;
        }

        .footer-column a {
            color: #cbd5e0;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-column a:hover {
            color: #d69e2e;
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
            border-radius: 50%;
            color: white;
            transition: all 0.3s ease;
        }

        .social-links a:hover {
            background: #d69e2e;
            transform: translateY(-3px);
        }

        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.1);
            color: #cbd5e0;
            font-size: 0.9rem;
        }

        /* === RESPONSIVE === */
        @media (max-width: 768px) {
            .edit-mode {
                padding: 6px 0;
                font-size: 0.8rem;
            }
            
            .edit-btn {
                padding: 5px 10px;
                font-size: 0.8rem;
                margin: 0 3px;
            }
            
            .header-top {
                flex-direction: column;
                gap: 15px;
            }
            
            .nav-main {
                gap: 20px;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .section-title {
                font-size: 2rem;
            }
            
            .blog-container {
                grid-template-columns: 1fr;
            }
            
            .community-container {
                grid-template-columns: 1fr;
            }
            
            .books-grid {
                grid-template-columns: 1fr;
            }
            
            .cart-modal {
                width: 100%;
                right: -100%;
            }
        }

        @media (max-width: 480px) {
            .edit-mode {
                font-size: 0.75rem;
            }
            
            .edit-btn {
                padding: 4px 8px;
                font-size: 0.75rem;
                margin: 0 2px;
            }
            
            .edit-btn.large {
                padding: 5px 10px;
                font-size: 0.8rem;
            }
            
            .hero h1 {
                font-size: 1.8rem;
            }
            
            .section-title {
                font-size: 1.7rem;
            }
            
            .form-row {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- COMPACT EDIT MODE -->
    <div class="edit-mode">
        <div class="container">
            <strong>🎨 EDIT MODE:</strong>
            <button class="edit-btn large" onclick="toggleEditMode()" id="editToggle">
                <i class="fas fa-edit"></i> TURN ON EDITING
            </button>
            <button class="edit-btn" onclick="saveAllContent()">
                <i class="fas fa-save"></i> SAVE
            </button>
            <button class="edit-btn" onclick="resetToDefault()">
                <i class="fas fa-undo"></i> RESET
            </button>
            <span style="margin-left: 15px; font-size: 0.85em;">Click ✏️ icons to edit</span>
        </div>
    </div>

    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-top">
                <div class="logo editable" data-id="logo">
                    <span class="edit-icon">✏️</span>
                    The Definitive Word
                </div>
                
                <nav class="nav-main">
                    <a href="#home" class="active nav-link">Home</a>
                    <a href="#books" class="nav-link">Books</a>
                    <a href="#blog" class="nav-link">Blog</a>
                    <a href="#community" class="nav-link">Community</a>
                    <a href="#payment" class="nav-link">Payment</a>
                    <a href="#about" class="nav-link">About Us</a>
                </nav>
                
                <div class="header-actions">
                    <div class="cart-icon" onclick="toggleCart()">
                        <i class="fas fa-shopping-cart fa-lg"></i>
                        <div class="cart-count" id="cartCount">0</div>
                    </div>
                    <button class="btn" onclick="toggleLogin()" id="loginBtn">
                        <i class="fas fa-user"></i> Login
                    </button>
                </div>
            </div>
        </div>
    </header>

    <!-- Home Section -->
    <section id="home" class="hero">
        <div class="container">
            <h1 class="editable" data-id="hero-title">
                <span class="edit-icon">✏️</span>
                Welcome to The Definitive Word
            </h1>
            <p class="editable" data-id="hero-subtitle">
                <span class="edit-icon">✏️</span>
                South Africa's premier destination for quality ebooks and exceptional reading experiences
            </p>
            <div style="margin-top: 35px;">
                <a href="#books" class="btn">
                    <i class="fas fa-gem"></i>
                    Browse Books
                </a>
                <a href="#blog" class="btn btn-secondary">
                    <i class="fas fa-blog"></i>
                    Read Our Blog
                </a>
            </div>
        </div>
    </section>

    <!-- Books Section -->
    <section id="books" class="section books-section">
        <div class="container">
            <h2 class="section-title editable" data-id="books-title">
                <span class="edit-icon">✏️</span>
                Featured Ebooks
            </h2>
            <p class="section-subtitle editable" data-id="books-subtitle">
                <span class="edit-icon">✏️</span>
                Discover our curated collection of exceptional reads from South African and international authors
            </p>
            
            <div class="books-grid" id="booksGrid">
                <!-- Books will be loaded here -->
            </div>
        </div>
    </section>

    <!-- Blog Section -->
    <section id="blog" class="section blog-section">
        <div class="container">
            <h2 class="section-title editable" data-id="blog-title">
                <span class="edit-icon">✏️</span>
                Our Blog
            </h2>
            <p class="section-subtitle editable" data-id="blog-subtitle">
                <span class="edit-icon">✏️</span>
                Insights, author interviews, reading recommendations, and literary discussions
            </p>
            
            <div class="blog-container">
                <div class="blog-posts" id="blogPosts">
                    <!-- Blog posts will be loaded here -->
                </div>
                
                <div class="blog-sidebar">
                    <div class="sidebar-widget">
                        <h3 class="widget-title editable" data-id="categories-title">
                            <span class="edit-icon">✏️</span>
                            Categories
                        </h3>
                        <ul class="categories-list" id="categoriesList">
                            <!-- Categories will be loaded here -->
                        </ul>
                    </div>
                    
                    <div class="sidebar-widget">
                        <h3 class="widget-title editable" data-id="recent-posts-title">
                            <span class="edit-icon">✏️</span>
                            Recent Posts
                        </h3>
                        <ul class="recent-posts-list" id="recentPostsList">
                            <!-- Recent posts will be loaded here -->
                        </ul>
                    </div>
                    
                    <div class="sidebar-widget">
                        <h3 class="widget-title editable" data-id="tags-title">
                            <span class="edit-icon">✏️</span>
                            Popular Tags
                        </h3>
                        <div class="tags-cloud" id="tagsCloud">
                            <!-- Tags will be loaded here -->
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Blog Post Creation (for logged in users) -->
            <div class="blog-create-post" id="blogCreatePost" style="display: none;">
                <div class="create-post-header">
                    <h3 class="create-post-title">Create New Blog Post</h3>
                    <button class="btn" onclick="toggleCreatePost()">
                        <i class="fas fa-times"></i> Cancel
                    </button>
                </div>
                
                <form id="createPostForm" onsubmit="createNewPost(event)">
                    <div class="form-group">
                        <label for="postTitle">Post Title</label>
                        <input type="text" id="postTitle" class="form-control" required>
                    </div>
                    
                    <div class="form-row">
                        <div class="form-group">
                            <label for="postCategory">Category</label>
                            <select id="postCategory" class="form-control" required>
                                <!-- Categories will be loaded here -->
                            </select>
                        </div>
                        
                        <div class="form-group">
                            <label for="postImage">Featured Image URL</label>
                            <input type="text" id="postImage" class="form-control" placeholder="https://example.com/image.jpg">
                        </div>
                    </div>
                    
                    <div class="form-group">
                        <label for="postContent">Content</label>
                        <textarea id="postContent" class="form-control" required></textarea>
                    </div>
                    
                    <div class="form-group">
                        <label for="postTags">Tags (comma separated)</label>
                        <input type="text" id="postTags" class="form-control" placeholder="fiction, literature, south africa">
                    </div>
                    
                    <button type="submit" class="btn" style="width: 100%;">
                        <i class="fas fa-paper-plane"></i> Publish Post
                    </button>
                </form>
            </div>
            
            <!-- Create Post Button (for logged in users) -->
            <div style="text-align: center; margin-top: 40px;" id="createPostBtnContainer">
                <button class="btn" onclick="toggleCreatePost()" id="createPostBtn" style="display: none;">
                    <i class="fas fa-plus"></i> Create New Post
                </button>
            </div>
        </div>
    </section>

    <!-- Community Section -->
    <section id="community" class="section community-section">
        <div class="container">
            <h2 class="section-title editable" data-id="community-title">
                <span class="edit-icon">✏️</span>
                Join Our Reading Community
            </h2>
            <p class="section-subtitle editable" data-id="community-subtitle">
                <span class="edit-icon">✏️</span>
                Connect with fellow readers, share reviews, and discuss your favorite books
            </p>
            
            <div class="community-container">
                <div class="discussion-forum">
                    <h3 class="editable" data-id="forum-title">
                        <span class="edit-icon">✏️</span>
                        Discussion Forum
                    </h3>
                    <div class="discussion-list" id="discussionList">
                        <!-- Discussions will be loaded here -->
                    </div>
                    <div class="form-group" style="margin-top: 20px;">
                        <input type="text" class="form-control" id="newDiscussion" placeholder="Start a new discussion...">
                        <button class="btn" style="width: 100%; margin-top: 10px;" onclick="addDiscussion()">
                            <i class="fas fa-plus"></i> Post Discussion
                        </button>
                    </div>
                </div>
                
                <div class="user-reviews">
                    <h3 class="editable" data-id="reviews-title">
                        <span class="edit-icon">✏️</span>
                        Recent Reviews
                    </h3>
                    <div class="reviews-list" id="reviewsList">
                        <!-- Reviews will be loaded here -->
                    </div>
                    <div class="form-group" style="margin-top: 20px;">
                        <select class="form-control" id="reviewBook">
                            <!-- Book options will be loaded here -->
                        </select>
                        <input type="text" class="form-control" id="newReview" placeholder="Write a review..." style="margin-top: 10px;">
                        <div style="display: flex; justify-content: space-between; margin-top: 10px;">
                            <div>
                                <span>Rating: </span>
                                <span class="review-rating" id="reviewStars">
                                    <i class="far fa-star" onclick="setRating(1)"></i>
                                    <i class="far fa-star" onclick="setRating(2)"></i>
                                    <i class="far fa-star" onclick="setRating(3)"></i>
                                    <i class="far fa-star" onclick="setRating(4)"></i>
                                    <i class="far fa-star" onclick="setRating(5)"></i>
                                </span>
                            </div>
                            <button class="btn" onclick="addReview()">
                                <i class="fas fa-pen"></i> Post Review
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Payment Section -->
    <section id="payment" class="section payment-section">
        <div class="container">
            <h2 class="section-title editable" data-id="payment-title">
                <span class="edit-icon">✏️</span>
                Secure Payment
            </h2>
            <p class="section-subtitle editable" data-id="payment-subtitle">
                <span class="edit-icon">✏️</span>
                Complete your purchase with our secure payment system
            </p>
            
            <div class="payment-container">
                <h3 class="editable" data-id="checkout-title">
                    <span class="edit-icon">✏️</span>
                    Checkout
                </h3>
                
                <div class="payment-methods">
                    <div class="payment-method active" onclick="selectPaymentMethod('credit')">
                        <i class="far fa-credit-card"></i>
                        <p>Credit Card</p>
                    </div>
                    <div class="payment-method" onclick="selectPaymentMethod('paypal')">
                        <i class="fab fa-paypal"></i>
                        <p>PayPal</p>
                    </div>
                    <div class="payment-method" onclick="selectPaymentMethod('bank')">
                        <i class="fas fa-university"></i>
                        <p>Bank Transfer</p>
                    </div>
                </div>
                
                <div class="payment-form" id="creditCardForm">
                    <div class="form-group">
                        <label for="cardNumber" class="editable" data-id="card-number">
                            <span class="edit-icon">✏️</span>
                            Card Number
                        </label>
                        <input type="text" id="cardNumber" class="form-control" placeholder="1234 5678 9012 3456">
                    </div>
                    
                    <div class="form-row">
                        <div class="form-group">
                            <label for="expiryDate" class="editable" data-id="expiry-date">
                                <span class="edit-icon">✏️</span>
                                Expiry Date
                            </label>
                            <input type="text" id="expiryDate" class="form-control" placeholder="MM/YY">
                        </div>
                        
                        <div class="form-group">
                            <label for="cvv" class="editable" data-id="cvv">
                                <span class="edit-icon">✏️</span>
                                CVV
                            </label>
                            <input type="text" id="cvv" class="form-control" placeholder="123">
                        </div>
                    </div>
                    
                    <div class="form-group">
                        <label for="cardName" class="editable" data-id="card-name">
                            <span class="edit-icon">✏️</span>
                            Name on Card
                        </label>
                        <input type="text" id="cardName" class="form-control" placeholder="John Doe">
                    </div>
                    
                    <button class="btn" style="width: 100%; margin-top: 20px;" onclick="processPayment()">
                        <i class="fas fa-lock"></i>
                        <span class="editable" data-id="pay-now">
                            <span class="edit-icon">✏️</span>
                            Pay Now
                        </span>
                    </button>
                </div>
                
                <div class="payment-form" id="paypalForm" style="display: none;">
                    <p class="editable" data-id="paypal-desc">
                        <span class="edit-icon">✏️</span>
                        You will be redirected to PayPal to complete your payment securely.
                    </p>
                    <button class="btn" style="width: 100%; margin-top: 20px;" onclick="processPayPal()">
                        <i class="fab fa-paypal"></i>
                        <span class="editable" data-id="paypal-btn">
                            <span class="edit-icon">✏️</span>
                            Pay with PayPal
                        </span>
                    </button>
                </div>
                
                <div class="payment-form" id="bankForm" style="display: none;">
                    <p class="editable" data-id="bank-desc">
                        <span class="edit-icon">✏️</span>
                        Please use the following bank details to complete your transfer:
                    </p>
                    <div style="background: #f7fafc; padding: 20px; border-radius: 8px; margin-top: 15px;">
                        <p><strong>Bank:</strong> <span class="editable" data-id="bank-name">
                            <span class="edit-icon">✏️</span>
                            Standard Bank
                        </span></p>
                        <p><strong>Account Name:</strong> <span class="editable" data-id="account-name">
                            <span class="edit-icon">✏️</span>
                            The Definitive Word
                        </span></p>
                        <p><strong>Account Number:</strong> <span class="editable" data-id="account-number">
                            <span class="edit-icon">✏️</span>
                            0123456789
                        </span></p>
                        <p><strong>Reference:</strong> Your Email Address</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Us Section -->
    <section id="about" class="section about-section">
        <div class="container">
            <h2 class="section-title editable" data-id="about-title">
                <span class="edit-icon">✏️</span>
                Our Story
            </h2>
            
            <div class="about-content">
                <div class="about-text editable" data-id="about-text-1">
                    <span class="edit-icon">✏️</span>
                    The Definitive Word was born in South Africa with a passion for connecting readers with transformative literature. We believe that every great book has the power to change perspectives and inspire growth.
                </div>
                
                <div class="about-text editable" data-id="about-text-2">
                    <span class="edit-icon">✏️</span>
                    Our team carefully selects each title, focusing on quality writing, compelling storytelling, and meaningful impact. We're proud to support both local South African authors and international literary excellence.
                </div>

                <h3 style="text-align: center; margin: 50px 0 35px; color: #1a365d; font-size: 1.8rem;" class="editable" data-id="team-title">
                    <span class="edit-icon">✏️</span>
                    Meet Our Team
                </h3>
                
                <div class="team-grid">
                    <div class="team-member">
                        <img src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-4.0.3&auto=format&fit=crop&w=400&q=80" alt="Team Member">
                        <h4 class="editable" data-id="team1-name">
                            <span class="edit-icon">✏️</span>
                            Sipho Mbeki
                        </h4>
                        <p class="editable" data-id="team1-role">
                            <span class="edit-icon">✏️</span>
                            Founder & CEO
                        </p>
                        <p class="editable" data-id="team1-desc">
                            <span class="edit-icon">✏️</span>
                            Passionate about bringing African literature to the world stage
                        </p>
                    </div>
                    
                    <div class="team-member">
                        <img src="https://images.unsplash.com/photo-1494790108755-2616b612b786?ixlib=rb-4.0.3&auto=format&fit=crop&w=400&q=80" alt="Team Member">
                        <h4 class="editable" data-id="team2-name">
                            <span class="edit-icon">✏️</span>
                            Nomvula Kalenga
                        </h4>
                        <p class="editable" data-id="team2-role">
                            <span class="edit-icon">✏️</span>
                            Head of Content
                        </p>
                        <p class="editable" data-id="team2-desc">
                            <span class="edit-icon">✏️</span>
                            Curating exceptional books for our growing community
                        </p>
                    </div>
                    
                    <div class="team-member">
                        <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3&auto=format&fit=crop&w=400&q=80" alt="Team Member">
                        <h4 class="editable" data-id="team3-name">
                            <span class="edit-icon">✏️</span>
                            Thabo van der Merwe
                        </h4>
                        <p class="editable" data-id="team3-role">
                            <span class="edit-icon">✏️</span>
                            Customer Support
                        </p>
                        <p class="editable" data-id="team3-desc">
                            <span class="edit-icon">✏️</span>
                            Dedicated to providing exceptional service to our readers
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3 class="editable" data-id="footer-about">
                        <span class="edit-icon">✏️</span>
                        About Us
                    </h3>
                    <p class="editable" data-id="footer-about-desc">
                        <span class="edit-icon">✏️</span>
                        South Africa's premier destination for quality ebooks and exceptional reading experiences.
                    </p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    </div>
                </div>
                
                <div class="footer-column">
                    <h3 class="editable" data-id="footer-links">
                        <span class="edit-icon">✏️</span>
                        Quick Links
                    </h3>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#books">Books</a></li>
                        <li><a href="#blog">Blog</a></li>
                        <li><a href="#community">Community</a></li>
                        <li><a href="#payment">Payment</a></li>
                        <li><a href="#about">About Us</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3 class="editable" data-id="footer-contact">
                        <span class="edit-icon">✏️</span>
                        Contact Info
                    </h3>
                    <ul>
                        <li><i class="fas fa-map-marker-alt"></i> <span class="editable" data-id="footer-address">
                            <span class="edit-icon">✏️</span>
                            123 Book Street, Johannesburg
                        </span></li>
                        <li><i class="fas fa-phone"></i> <span class="editable" data-id="footer-phone">
                            <span class="edit-icon">✏️</span>
                            +27 11 123 4567
                        </span></li>
                        <li><i class="fas fa-envelope"></i> <span class="editable" data-id="footer-email">
                            <span class="edit-icon">✏️</span>
                            info@definitiveword.co.za
                        </span></li>
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                <p class="editable" data-id="copyright">
                    <span class="edit-icon">✏️</span>
                    &copy; 2023 The Definitive Word. All rights reserved.
                </p>
            </div>
        </div>
    </footer>

    <!-- Cart Modal -->
    <div class="cart-modal" id="cartModal">
        <div class="cart-header">
            <h3>Your Cart</h3>
            <button class="close-modal" onclick="toggleCart()">&times;</button>
        </div>
        <div class="cart-items" id="cartItems">
            <!-- Cart items will be loaded here -->
        </div>
        <div class="cart-total">
            <span>Total:</span>
            <span id="cartTotal">R0.00</span>
        </div>
        <button class="btn" style="width: 100%;" onclick="proceedToCheckout()">
            <i class="fas fa-credit-card"></i> Proceed to Checkout
        </button>
    </div>

    <!-- Edit Modal -->
    <div class="edit-modal" id="editModal">
        <div class="modal-content">
            <div class="modal-header">
                <h2 id="editModalTitle">Edit Content</h2>
                <button class="close-modal" onclick="closeEditModal()">&times;</button>
            </div>
            <div class="modal-body">
                <textarea id="editModalTextarea"></textarea>
            </div>
            <div class="modal-footer">
                <button class="edit-btn" onclick="closeEditModal()">Cancel</button>
                <button class="edit-btn" onclick="saveEdit()">Save Changes</button>
            </div>
        </div>
    </div>

    <!-- Login Modal -->
    <div class="edit-modal" id="loginModal">
        <div class="modal-content">
            <div class="modal-header">
                <h2>Login to Your Account</h2>
                <button class="close-modal" onclick="toggleLogin()">&times;</button>
            </div>
            <div class="modal-body">
                <div class="form-group">
                    <label for="loginEmail">Email Address</label>
                    <input type="email" id="loginEmail" class="form-control" placeholder="your@email.com">
                </div>
                <div class="form-group">
                    <label for="loginPassword">Password</label>
                    <input type="password" id="loginPassword" class="form-control" placeholder="Your password">
                </div>
                <div style="text-align: center; margin-top: 20px;">
                    <p>Don't have an account? <a href="#" style="color: #d69e2e;">Sign up here</a></p>
                </div>
            </div>
            <div class="modal-footer">
                <button class="edit-btn" onclick="toggleLogin()">Cancel</button>
                <button class="edit-btn" onclick="performLogin()">Login</button>
            </div>
        </div>
    </div>

    <!-- Notification -->
    <div class="notification" id="notification"></div>

    <script>
        // Global variables
        let currentEditingElement = null;
        let editMode = false;
        let cart = [];
        let currentUser = null;
        let currentRating = 0;
        let discussions = [];
        let reviews = [];
        let blogPosts = [];
        let categories = [];
        let tags = [];

        // Sample data
        const sampleBooks = [
            {
                id: 1,
                title: "The Silent Observer",
                author: "Megan Foster", 
                price: 249.99,
                image: "https://images.unsplash.com/photo-1544947950-fa07a98d237f?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                badge: "Bestseller",
                description: "A psychological thriller that explores the depths of human consciousness."
            },
            {
                id: 2,
                title: "Digital Revolution",
                author: "Alex Chen",
                price: 299.99,
                image: "https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                badge: "New",
                description: "How technology is reshaping our world and what it means for the future."
            },
            {
                id: 3,
                title: "Business Mastery",
                author: "Sarah Johnson", 
                price: 349.99,
                image: "https://images.unsplash.com/photo-1512820790803-83ca734da794?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                badge: "Popular",
                description: "Essential strategies for entrepreneurial success in the modern economy."
            },
            {
                id: 4,
                title: "African Skies",
                author: "Tendai Moyo", 
                price: 279.99,
                image: "https://images.unsplash.com/photo-1481627834876-b7833e8f5570?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                badge: "Local Author",
                description: "A captivating novel set against the backdrop of contemporary South Africa."
            },
            {
                id: 5,
                title: "Mindful Living",
                author: "James Wilson", 
                price: 229.99,
                image: "https://images.unsplash.com/photo-1506880018603-83d5b814b5a6?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                badge: "",
                description: "Practical techniques for finding peace and purpose in a busy world."
            },
            {
                id: 6,
                title: "Culinary Journey",
                author: "Maria Rodriguez", 
                price: 319.99,
                image: "https://images.unsplash.com/photo-1544716278-ca5e3f4abd8c?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                badge: "Featured",
                description: "Explore world cuisines with these delicious and accessible recipes."
            }
        ];

        // Sample blog data
        const sampleBlogPosts = [
            {
                id: 1,
                title: "The Rise of African Literature in the Global Market",
                excerpt: "Exploring how African authors are making their mark on the international literary scene and what it means for the future of publishing.",
                content: "Full content would go here...",
                author: "Nomvula Kalenga",
                date: "2023-07-15",
                category: "Literature",
                image: "https://images.unsplash.com/photo-1481627834876-b7833e8f5570?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                tags: ["african literature", "publishing", "global market"],
                likes: 24,
                comments: 8
            },
            {
                id: 2,
                title: "5 Must-Read Books by South African Authors",
                excerpt: "A curated list of exceptional books from South African writers that deserve a spot on your reading list.",
                content: "Full content would go here...",
                author: "Sipho Mbeki",
                date: "2023-07-10",
                category: "Recommendations",
                image: "https://images.unsplash.com/photo-1544716278-ca5e3f4abd8c?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                tags: ["south africa", "recommendations", "must-read"],
                likes: 42,
                comments: 15
            },
            {
                id: 3,
                title: "How Reading Fiction Improves Empathy and Understanding",
                excerpt: "Scientific research shows that immersing yourself in fictional worlds can have real benefits for your emotional intelligence.",
                content: "Full content would go here...",
                author: "Thabo van der Merwe",
                date: "2023-07-05",
                category: "Psychology",
                image: "https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                tags: ["psychology", "fiction", "empathy"],
                likes: 31,
                comments: 12
            }
        ];

        const sampleCategories = [
            { name: "Literature", count: 12 },
            { name: "Recommendations", count: 8 },
            { name: "Author Interviews", count: 5 },
            { name: "Writing Tips", count: 7 },
            { name: "Book Reviews", count: 15 },
            { name: "Psychology", count: 4 },
            { name: "Industry News", count: 6 }
        ];

        const sampleTags = [
            "fiction", "non-fiction", "south africa", "african literature", 
            "bestseller", "new release", "author interview", "writing tips",
            "book review", "reading list", "literary awards", "publishing"
        ];

        // Sample discussions and reviews
        const sampleDiscussions = [
            {
                id: 1,
                title: "What's your favorite book of 2023 so far?",
                author: "BookLover42",
                date: "2023-07-15",
                replies: 12
            },
            {
                id: 2,
                title: "Recommendations for historical fiction?",
                author: "HistoryBuff",
                date: "2023-07-14",
                replies: 7
            },
            {
                id: 3,
                title: "Book club starting next month - join us!",
                author: "ReadingEnthusiast",
                date: "2023-07-10",
                replies: 23
            }
        ];

        const sampleReviews = [
            {
                id: 1,
                bookTitle: "The Silent Observer",
                author: "CriticalReader",
                rating: 5,
                text: "Absolutely gripping from start to finish! The character development was exceptional.",
                date: "2023-07-12"
            },
            {
                id: 2,
                bookTitle: "Digital Revolution",
                author: "TechGuru",
                rating: 4,
                text: "Well-researched and thought-provoking, though a bit technical in places.",
                date: "2023-07-08"
            },
            {
                id: 3,
                bookTitle: "Business Mastery",
                author: "Entrepreneur2023",
                rating: 5,
                text: "Practical advice that I've already implemented in my startup. Highly recommended!",
                date: "2023-07-05"
            }
        ];

        // Initialize the application
        function initApp() {
            loadAllContent();
            displayBooks();
            setupNavigation();
            setupEditing();
            loadCart();
            loadCommunityData();
            loadBlogData();
            updateCartDisplay();
            showNotification('Welcome to The Definitive Word! Click the EDIT button above to customize your site.');
        }

        // Toggle edit mode
        function toggleEditMode() {
            editMode = !editMode;
            document.body.classList.toggle('edit-mode-on', editMode);
            const toggleBtn = document.getElementById('editToggle');
            toggleBtn.innerHTML = editMode ? 
                '<i class="fas fa-times"></i> TURN OFF EDITING' : 
                '<i class="fas fa-edit"></i> TURN ON EDITING';
            toggleBtn.style.background = editMode ? '#c53030' : '#d69e2e';
            
            showNotification(editMode ? 
                '✏️ EDIT MODE ON: Click any yellow ✏️ icon to edit content!' : 
                '✅ Edit mode turned off');
        }

        // Display books in the grid
        function displayBooks() {
            const grid = document.getElementById('booksGrid');
            grid.innerHTML = '';

            sampleBooks.forEach(book => {
                const card = document.createElement('div');
                card.className = 'book-card';
                card.innerHTML = `
                    ${book.badge ? `<div style="position: absolute; top: 15px; right: 15px; background: #c53030; color: white; padding: 6px 12px; border-radius: 20px; font-size: 0.8rem; font-weight: 600; z-index: 2;">${book.badge}</div>` : ''}
                    <div class="book-cover">
                        <img src="${book.image}" alt="${book.title}">
                    </div>
                    <div class="book-info">
                        <h3 class="book-title">${book.title}</h3>
                        <p class="book-author">by ${book.author}</p>
                        <p style="font-size: 0.9rem; color: #666; margin-bottom: 15px;">${book.description}</p>
                        <div class="book-price">
                            <span class="price">R${book.price.toFixed(2)}</span>
                            <button class="btn" onclick="addToCart(${book.id})" style="padding: 10px 20px; font-size: 0.9rem;">
                                <i class="fas fa-cart-plus"></i>
                                Add to Cart
                            </button>
                        </div>
                    </div>
                `;
                grid.appendChild(card);
            });

            // Populate book options for reviews
            const bookSelect = document.getElementById('reviewBook');
            bookSelect.innerHTML = '<option value="">Select a book</option>';
            sampleBooks.forEach(book => {
                const option = document.createElement('option');
                option.value = book.id;
                option.textContent = book.title;
                bookSelect.appendChild(option);
            });
        }

        // Blog functionality
        function loadBlogData() {
            // Load blog posts
            const savedPosts = localStorage.getItem('blogPosts');
            if (savedPosts) {
                blogPosts = JSON.parse(savedPosts);
            } else {
                blogPosts = [...sampleBlogPosts];
            }
            
            // Load categories
            const savedCategories = localStorage.getItem('blogCategories');
            if (savedCategories) {
                categories = JSON.parse(savedCategories);
            } else {
                categories = [...sampleCategories];
            }
            
            // Load tags
            const savedTags = localStorage.getItem('blogTags');
            if (savedTags) {
                tags = JSON.parse(savedTags);
            } else {
                tags = [...sampleTags];
            }
            
            displayBlogPosts();
            displayCategories();
            displayRecentPosts();
            displayTags();
            
            // Populate category dropdown for post creation
            const categorySelect = document.getElementById('postCategory');
            categorySelect.innerHTML = '<option value="">Select a category</option>';
            categories.forEach(category => {
                const option = document.createElement('option');
                option.value = category.name;
                option.textContent = category.name;
                categorySelect.appendChild(option);
            });
        }

        function displayBlogPosts() {
            const postsContainer = document.getElementById('blogPosts');
            postsContainer.innerHTML = '';
            
            blogPosts.forEach(post => {
                const postElement = document.createElement('div');
                postElement.className = 'blog-post';
                postElement.innerHTML = `
                    <div class="blog-post-image">
                        <img src="${post.image}" alt="${post.title}">
                    </div>
                    <div class="blog-post-content">
                        <div class="blog-post-meta">
                            <span class="blog-post-category">${post.category}</span>
                            <span>${formatDate(post.date)}</span>
                            <span>by ${post.author}</span>
                        </div>
                        <h3 class="blog-post-title">${post.title}</h3>
                        <p class="blog-post-excerpt">${post.excerpt}</p>
                        <div class="blog-post-footer">
                            <div class="blog-post-actions">
                                <button onclick="likePost(${post.id})">
                                    <i class="far fa-heart"></i> ${post.likes}
                                </button>
                                <button onclick="commentOnPost(${post.id})">
                                    <i class="far fa-comment"></i> ${post.comments}
                                </button>
                            </div>
                            <a href="#" class="btn" style="padding: 8px 15px; font-size: 0.9rem;">Read More</a>
                        </div>
                    </div>
                `;
                postsContainer.appendChild(postElement);
            });
        }

        function displayCategories() {
            const categoriesList = document.getElementById('categoriesList');
            categoriesList.innerHTML = '';
            
            categories.forEach(category => {
                const listItem = document.createElement('li');
                listItem.innerHTML = `
                    <a href="#">
                        ${category.name}
                        <span>${category.count}</span>
                    </a>
                `;
                categoriesList.appendChild(listItem);
            });
        }

        function displayRecentPosts() {
            const recentPostsList = document.getElementById('recentPostsList');
            recentPostsList.innerHTML = '';
            
            // Show only the 3 most recent posts
            const recentPosts = [...blogPosts].sort((a, b) => new Date(b.date) - new Date(a.date)).slice(0, 3);
            
            recentPosts.forEach(post => {
                const listItem = document.createElement('li');
                listItem.innerHTML = `
                    <div class="recent-post">
                        <div class="recent-post-image">
                            <img src="${post.image}" alt="${post.title}">
                        </div>
                        <div class="recent-post-content">
                            <h4>${post.title}</h4>
                            <div class="post-date">${formatDate(post.date)}</div>
                        </div>
                    </div>
                `;
                recentPostsList.appendChild(listItem);
            });
        }

        function displayTags() {
            const tagsCloud = document.getElementById('tagsCloud');
            tagsCloud.innerHTML = '';
            
            tags.forEach(tag => {
                const tagElement = document.createElement('span');
                tagElement.className = 'tag';
                tagElement.textContent = tag;
                tagElement.onclick = () => filterByTag(tag);
                tagsCloud.appendChild(tagElement);
            });
        }

        function formatDate(dateString) {
            const options = { year: 'numeric', month: 'long', day: 'numeric' };
            return new Date(dateString).toLocaleDateString('en-US', options);
        }

        function likePost(postId) {
            if (!currentUser) {
                showNotification('Please log in to like posts');
                toggleLogin();
                return;
            }
            
            const post = blogPosts.find(p => p.id === postId);
            if (post) {
                post.likes += 1;
                localStorage.setItem('blogPosts', JSON.stringify(blogPosts));
                displayBlogPosts();
                showNotification('Post liked!');
            }
        }

        function commentOnPost(postId) {
            if (!currentUser) {
                showNotification('Please log in to comment on posts');
                toggleLogin();
                return;
            }
            
            const comment = prompt('Enter your comment:');
            if (comment) {
                const post = blogPosts.find(p => p.id === postId);
                if (post) {
                    post.comments += 1;
                    localStorage.setItem('blogPosts', JSON.stringify(blogPosts));
                    displayBlogPosts();
                    showNotification('Comment added!');
                }
            }
        }

        function filterByTag(tag) {
            showNotification(`Filtering by tag: ${tag}`);
            // In a real application, you would filter the blog posts by this tag
        }

        function toggleCreatePost() {
            if (!currentUser) {
                showNotification('Please log in to create blog posts');
                toggleLogin();
                return;
            }
            
            const createPostSection = document.getElementById('blogCreatePost');
            const createPostBtn = document.getElementById('createPostBtn');
            
            if (createPostSection.style.display === 'none') {
                createPostSection.style.display = 'block';
                createPostBtn.textContent = 'Cancel Post Creation';
            } else {
                createPostSection.style.display = 'none';
                createPostBtn.textContent = 'Create New Post';
                document.getElementById('createPostForm').reset();
            }
        }

        function createNewPost(event) {
            event.preventDefault();
            
            const title = document.getElementById('postTitle').value;
            const category = document.getElementById('postCategory').value;
            const image = document.getElementById('postImage').value || 'https://images.unsplash.com/photo-1481627834876-b7833e8f5570?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80';
            const content = document.getElementById('postContent').value;
            const tagsInput = document.getElementById('postTags').value;
            
            // Create excerpt from first 150 characters of content
            const excerpt = content.length > 150 ? content.substring(0, 150) + '...' : content;
            
            // Process tags
            const postTags = tagsInput.split(',').map(tag => tag.trim()).filter(tag => tag);
            
            // Add new tags to global tags list
            postTags.forEach(tag => {
                if (!tags.includes(tag)) {
                    tags.push(tag);
                }
            });
            
            // Create new post
            const newPost = {
                id: blogPosts.length + 1,
                title: title,
                excerpt: excerpt,
                content: content,
                author: currentUser,
                date: new Date().toISOString().split('T')[0],
                category: category,
                image: image,
                tags: postTags,
                likes: 0,
                comments: 0
            };
            
            blogPosts.unshift(newPost);
            localStorage.setItem('blogPosts', JSON.stringify(blogPosts));
            localStorage.setItem('blogTags', JSON.stringify(tags));
            
            // Update category count
            const categoryIndex = categories.findIndex(c => c.name === category);
            if (categoryIndex !== -1) {
                categories[categoryIndex].count += 1;
            } else {
                categories.push({ name: category, count: 1 });
            }
            localStorage.setItem('blogCategories', JSON.stringify(categories));
            
            // Refresh displays
            displayBlogPosts();
            displayCategories();
            displayRecentPosts();
            displayTags();
            
            // Reset form and hide creation section
            document.getElementById('createPostForm').reset();
            document.getElementById('blogCreatePost').style.display = 'none';
            document.getElementById('createPostBtn').textContent = 'Create New Post';
            
            showNotification('Blog post published successfully!');
        }

        // Setup navigation
        function setupNavigation() {
            document.querySelectorAll('.nav-link').forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    document.querySelectorAll('.nav-link').forEach(l => l.classList.remove('active'));
                    this.classList.add('active');
                    
                    const targetId = this.getAttribute('href').substring(1);
                    const targetSection = document.getElementById(targetId);
                    
                    if (targetSection) {
                        window.scrollTo({
                            top: targetSection.offsetTop - 80,
                            behavior: 'smooth'
                        });
                    }
                });
            });

            window.addEventListener('scroll', function() {
                const sections = document.querySelectorAll('.section, .hero');
                const navLinks = document.querySelectorAll('.nav-link');
                
                let current = '';
                sections.forEach(section => {
                    const sectionTop = section.offsetTop;
                    if (scrollY >= (sectionTop - 120)) {
                        current = section.getAttribute('id');
                    }
                });

                navLinks.forEach(link => {
                    link.classList.remove('active');
                    if (link.getAttribute('href').substring(1) === current) {
                        link.classList.add('active');
                    }
                });
            });
        }

        // Setup editing functionality
        function setupEditing() {
            document.querySelectorAll('.editable').forEach(element => {
                element.addEventListener('click', function(e) {
                    if (editMode) {
                        openEditModal(this);
                    }
                });
            });
        }

        // Open edit modal
        function openEditModal(element) {
            currentEditingElement = element;
            const currentText = element.textContent.replace('✏️', '').trim();
            document.getElementById('editModalTitle').textContent = 'Edit Content';
            document.getElementById('editModalTextarea').value = currentText;
            document.getElementById('editModal').classList.add('active');
            document.getElementById('editModalTextarea').focus();
        }

        // Save edit
        function saveEdit() {
            if (currentEditingElement) {
                const newText = document.getElementById('editModalTextarea').value;
                currentEditingElement.innerHTML = '<span class="edit-icon">✏️</span> ' + newText;
                saveAllContent();
                closeEditModal();
                showNotification('✅ Changes saved successfully!');
            }
        }

        // Close edit modal
        function closeEditModal() {
            document.getElementById('editModal').classList.remove('active');
            currentEditingElement = null;
        }

        // Save all content to localStorage
        function saveAllContent() {
            const content = {};
            document.querySelectorAll('.editable').forEach(element => {
                const id = element.getAttribute('data-id');
                const text = element.textContent.replace('✏️', '').trim();
                content[id] = text;
            });
            localStorage.setItem('websiteContent', JSON.stringify(content));
        }

        // Load all content from localStorage
        function loadAllContent() {
            const saved = localStorage.getItem('websiteContent');
            if (saved) {
                const content = JSON.parse(saved);
                document.querySelectorAll('.editable').forEach(element => {
                    const id = element.getAttribute('data-id');
                    if (content[id]) {
                        element.innerHTML = '<span class="edit-icon">✏️</span> ' + content[id];
                    }
                });
            }
        }

        // Reset to default content
        function resetToDefault() {
            if (confirm('Are you sure you want to reset all content to original? This cannot be undone.')) {
                localStorage.removeItem('websiteContent');
                localStorage.removeItem('cart');
                localStorage.removeItem('discussions');
                localStorage.removeItem('reviews');
                localStorage.removeItem('blogPosts');
                localStorage.removeItem('blogCategories');
                localStorage.removeItem('blogTags');
                location.reload();
            }
        }

        // Cart functionality
        function addToCart(bookId) {
            const book = sampleBooks.find(b => b.id === bookId);
            if (book) {
                const existingItem = cart.find(item => item.id === bookId);
                if (existingItem) {
                    existingItem.quantity += 1;
                } else {
                    cart.push({
                        id: book.id,
                        title: book.title,
                        price: book.price,
                        image: book.image,
                        quantity: 1
                    });
                }
                saveCart();
                updateCartDisplay();
                showNotification(`🛒 Added "${book.title}" to cart!`);
            }
        }

        function removeFromCart(bookId) {
            cart = cart.filter(item => item.id !== bookId);
            saveCart();
            updateCartDisplay();
            showNotification('Item removed from cart');
        }

        function updateCartDisplay() {
            const cartCount = document.getElementById('cartCount');
            const cartItems = document.getElementById('cartItems');
            const cartTotal = document.getElementById('cartTotal');
            
            // Update cart count
            const totalItems = cart.reduce((sum, item) => sum + item.quantity, 0);
            cartCount.textContent = totalItems;
            
            // Update cart items
            cartItems.innerHTML = '';
            if (cart.length === 0) {
                cartItems.innerHTML = '<p style="text-align: center; color: #666;">Your cart is empty</p>';
            } else {
                cart.forEach(item => {
                    const cartItem = document.createElement('div');
                    cartItem.className = 'cart-item';
                    cartItem.innerHTML = `
                        <img src="${item.image}" alt="${item.title}">
                        <div class="cart-item-details">
                            <div class="cart-item-title">${item.title}</div>
                            <div class="cart-item-price">R${item.price.toFixed(2)} x ${item.quantity}</div>
                        </div>
                        <button class="cart-item-remove" onclick="removeFromCart(${item.id})">
                            <i class="fas fa-times"></i>
                        </button>
                    `;
                    cartItems.appendChild(cartItem);
                });
            }
            
            // Update total
            const total = cart.reduce((sum, item) => sum + (item.price * item.quantity), 0);
            cartTotal.textContent = `R${total.toFixed(2)}`;
        }

        function saveCart() {
            localStorage.setItem('cart', JSON.stringify(cart));
        }

        function loadCart() {
            const savedCart = localStorage.getItem('cart');
            if (savedCart) {
                cart = JSON.parse(savedCart);
            }
        }

        function toggleCart() {
            document.getElementById('cartModal').classList.toggle('active');
        }

        function proceedToCheckout() {
            if (cart.length === 0) {
                showNotification('Your cart is empty');
                return;
            }
            
            toggleCart();
            // Scroll to payment section
            const paymentSection = document.getElementById('payment');
            window.scrollTo({
                top: paymentSection.offsetTop - 80,
                behavior: 'smooth'
            });
            showNotification('Proceeding to checkout');
        }

        // Community functionality
        function loadCommunityData() {
            // Load discussions
            const savedDiscussions = localStorage.getItem('discussions');
            if (savedDiscussions) {
                discussions = JSON.parse(savedDiscussions);
            } else {
                discussions = [...sampleDiscussions];
            }
            
            // Load reviews
            const savedReviews = localStorage.getItem('reviews');
            if (savedReviews) {
                reviews = JSON.parse(savedReviews);
            } else {
                reviews = [...sampleReviews];
            }
            
            displayDiscussions();
            displayReviews();
        }

        function displayDiscussions() {
            const discussionList = document.getElementById('discussionList');
            discussionList.innerHTML = '';
            
            discussions.forEach(discussion => {
                const discussionItem = document.createElement('div');
                discussionItem.className = 'discussion-item';
                discussionItem.innerHTML = `
                    <h4>${discussion.title}</h4>
                    <div class="discussion-meta">
                        <span>by ${discussion.author}</span>
                        <span>${discussion.replies} replies</span>
                    </div>
                `;
                discussionList.appendChild(discussionItem);
            });
        }

        function displayReviews() {
            const reviewsList = document.getElementById('reviewsList');
            reviewsList.innerHTML = '';
            
            reviews.forEach(review => {
                const reviewItem = document.createElement('div');
                reviewItem.className = 'review-item';
                
                // Create star rating
                let stars = '';
                for (let i = 1; i <= 5; i++) {
                    if (i <= review.rating) {
                        stars += '<i class="fas fa-star"></i>';
                    } else {
                        stars += '<i class="far fa-star"></i>';
                    }
                }
                
                reviewItem.innerHTML = `
                    <div class="review-header">
                        <strong>${review.bookTitle}</strong>
                        <div class="review-rating">${stars}</div>
                    </div>
                    <p>${review.text}</p>
                    <div class="discussion-meta">
                        <span>by ${review.author}</span>
                    </div>
                `;
                reviewsList.appendChild(reviewItem);
            });
        }

        function addDiscussion() {
            const newDiscussionInput = document.getElementById('newDiscussion');
            const title = newDiscussionInput.value.trim();
            
            if (!title) {
                showNotification('Please enter a discussion title');
                return;
            }
            
            if (!currentUser) {
                showNotification('Please log in to post a discussion');
                toggleLogin();
                return;
            }
            
            const newDiscussion = {
                id: discussions.length + 1,
                title: title,
                author: currentUser,
                date: new Date().toISOString().split('T')[0],
                replies: 0
            };
            
            discussions.unshift(newDiscussion);
            localStorage.setItem('discussions', JSON.stringify(discussions));
            displayDiscussions();
            newDiscussionInput.value = '';
            showNotification('Discussion posted successfully!');
        }

        function setRating(rating) {
            currentRating = rating;
            const stars = document.getElementById('reviewStars');
            stars.innerHTML = '';
            
            for (let i = 1; i <= 5; i++) {
                const star = document.createElement('i');
                if (i <= rating) {
                    star.className = 'fas fa-star';
                } else {
                    star.className = 'far fa-star';
                }
                star.onclick = () => setRating(i);
                stars.appendChild(star);
            }
        }

        function addReview() {
            const bookSelect = document.getElementById('reviewBook');
            const reviewInput = document.getElementById('newReview');
            const bookId = bookSelect.value;
            const text = reviewInput.value.trim();
            
            if (!bookId) {
                showNotification('Please select a book');
                return;
            }
            
            if (!text) {
                showNotification('Please enter your review');
                return;
            }
            
            if (currentRating === 0) {
                showNotification('Please set a rating');
                return;
            }
            
            if (!currentUser) {
                showNotification('Please log in to post a review');
                toggleLogin();
                return;
            }
            
            const book = sampleBooks.find(b => b.id === parseInt(bookId));
            const newReview = {
                id: reviews.length + 1,
                bookTitle: book.title,
                author: currentUser,
                rating: currentRating,
                text: text,
                date: new Date().toISOString().split('T')[0]
            };
            
            reviews.unshift(newReview);
            localStorage.setItem('reviews', JSON.stringify(reviews));
            displayReviews();
            
            // Reset form
            bookSelect.value = '';
            reviewInput.value = '';
            setRating(0);
            
            showNotification('Review posted successfully!');
        }

        // Payment functionality
        function selectPaymentMethod(method) {
            // Update active state
            document.querySelectorAll('.payment-method').forEach(el => {
                el.classList.remove('active');
            });
            event.target.closest('.payment-method').classList.add('active');
            
            // Show appropriate form
            document.getElementById('creditCardForm').style.display = 'none';
            document.getElementById('paypalForm').style.display = 'none';
            document.getElementById('bankForm').style.display = 'none';
            
            if (method === 'credit') {
                document.getElementById('creditCardForm').style.display = 'block';
            } else if (method === 'paypal') {
                document.getElementById('paypalForm').style.display = 'block';
            } else if (method === 'bank') {
                document.getElementById('bankForm').style.display = 'block';
            }
        }

        function processPayment() {
            if (cart.length === 0) {
                showNotification('Your cart is empty');
                return;
            }
            
            // In a real application, you would process the payment here
            // For this demo, we'll just simulate a successful payment
            
            const total = cart.reduce((sum, item) => sum + (item.price * item.quantity), 0);
            
            // Clear cart
            cart = [];
            saveCart();
            updateCartDisplay();
            
            showNotification(`✅ Payment successful! Thank you for your purchase of R${total.toFixed(2)}. Your ebooks will be delivered to your email.`);
            
            // Scroll to top
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        }

        function processPayPal() {
            // In a real application, you would redirect to PayPal
            showNotification('Redirecting to PayPal...');
            
            // Simulate PayPal processing
            setTimeout(() => {
                processPayment();
            }, 2000);
        }

        // User authentication
        function toggleLogin() {
            document.getElementById('loginModal').classList.toggle('active');
        }

        function performLogin() {
            const email = document.getElementById('loginEmail').value;
            const password = document.getElementById('loginPassword').value;
            
            if (!email || !password) {
                showNotification('Please enter both email and password');
                return;
            }
            
            // In a real application, you would validate credentials with a server
            // For this demo, we'll just simulate a successful login
            currentUser = email.split('@')[0]; // Use the part before @ as username
            document.getElementById('loginBtn').innerHTML = `<i class="fas fa-user"></i> ${currentUser}`;
            
            // Show create post button for logged in users
            document.getElementById('createPostBtn').style.display = 'inline-flex';
            
            toggleLogin();
            showNotification(`Welcome back, ${currentUser}!`);
        }

        // Utility functions
        function showNotification(message) {
            const notification = document.getElementById('notification');
            notification.textContent = message;
            
            // Set color based on message type
            if (message.includes('✅') || message.includes('successful') || message.includes('Welcome')) {
                notification.style.background = '#38a169';
            } else if (message.includes('🛒')) {
                notification.style.background = '#d69e2e';
            } else if (message.includes('error') || message.includes('Please')) {
                notification.style.background = '#c53030';
            } else {
                notification.style.background = '#d69e2e';
            }
            
            notification.className = 'notification show';
            setTimeout(() => {
                notification.className = 'notification';
            }, 5000);
        }

        // Event listeners
        window.addEventListener('click', function(event) {
            if (event.target.classList.contains('edit-modal')) {
                closeEditModal();
                document.getElementById('loginModal').classList.remove('active');
            }
        });

        document.addEventListener('keydown', function(event) {
            if (event.key === 'Escape') {
                closeEditModal();
                document.getElementById('loginModal').classList.remove('active');
                document.getElementById('cartModal').classList.remove('active');
            }
        });

        // Initialize the app when DOM is loaded
        document.addEventListener('DOMContentLoaded', initApp);
    </script>
</body>
</html>

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

        .edit-indicator {
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

        .edit-mode-on .edit-indicator {
            display: flex;
        }

        /* === HEADER === */
        header {
            background: white;
            box-shadow: 0 2px 20px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
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
            cursor: pointer;
            user-select: none;
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

        /* Double-click indicator for tabs */
        .nav-main a::before {
            content: '✏️';
            position: absolute;
            top: -5px;
            right: -5px;
            font-size: 0.7rem;
            opacity: 0;
            transition: opacity 0.3s ease;
            pointer-events: none;
        }

        .edit-mode-on .nav-main a::before {
            opacity: 1;
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

        /* === CONTEXT MENU === */
        .context-menu {
            position: fixed;
            background: white;
            border-radius: 8px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.15);
            z-index: 10001;
            min-width: 180px;
            opacity: 0;
            transform: scale(0.95);
            transition: all 0.2s ease;
            pointer-events: none;
        }

        .context-menu.active {
            opacity: 1;
            transform: scale(1);
            pointer-events: all;
        }

        .context-menu-item {
            padding: 12px 16px;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 10px;
            transition: background 0.2s ease;
            border-bottom: 1px solid #f1f1f1;
        }

        .context-menu-item:last-child {
            border-bottom: none;
        }

        .context-menu-item:hover {
            background: #f7fafc;
        }

        .context-menu-item i {
            width: 16px;
            text-align: center;
            color: #d69e2e;
        }

        /* === EDIT MODE INDICATOR === */
        .edit-mode-indicator {
            position: fixed;
            top: 20px;
            right: 20px;
            background: #d69e2e;
            color: #1a365d;
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 600;
            box-shadow: 0 4px 12px rgba(0,0,0,0.15);
            z-index: 10000;
            display: none;
            align-items: center;
            gap: 8px;
            animation: slideIn 0.3s ease;
        }

        .edit-mode-indicator.active {
            display: flex;
        }

        @keyframes slideIn {
            from {
                transform: translateX(100px);
                opacity: 0;
            }
            to {
                transform: translateX(0);
                opacity: 1;
            }
        }

        /* === QUICK EDIT TOOLTIP === */
        .quick-edit-tooltip {
            position: fixed;
            background: #1a365d;
            color: white;
            padding: 8px 12px;
            border-radius: 6px;
            font-size: 0.8rem;
            z-index: 10003;
            pointer-events: none;
            opacity: 0;
            transform: translateY(10px);
            transition: all 0.3s ease;
            box-shadow: 0 4px 12px rgba(0,0,0,0.2);
        }

        .quick-edit-tooltip.show {
            opacity: 1;
            transform: translateY(0);
        }

        .quick-edit-tooltip::after {
            content: '';
            position: absolute;
            top: -5px;
            left: 50%;
            transform: translateX(-50%);
            border-width: 0 5px 5px 5px;
            border-style: solid;
            border-color: transparent transparent #1a365d transparent;
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

        .modal-btn {
            padding: 10px 20px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .modal-btn.primary {
            background: #d69e2e;
            color: #1a365d;
        }

        .modal-btn.secondary {
            background: #e2e8f0;
            color: #4a5568;
        }

        .modal-btn:hover {
            transform: translateY(-1px);
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
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

        /* === RESPONSIVE === */
        @media (max-width: 768px) {
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
            
            .books-grid {
                grid-template-columns: 1fr;
            }
            
            .nav-main a::before {
                display: none;
            }
            
            .edit-mode-indicator {
                top: 10px;
                right: 10px;
                font-size: 0.75rem;
            }
        }

        @media (max-width: 480px) {
            .hero h1 {
                font-size: 1.8rem;
            }
            
            .section-title {
                font-size: 1.7rem;
            }
            
            .context-menu {
                min-width: 160px;
            }
        }
    </style>
</head>
<body>
    <!-- Edit Mode Indicator -->
    <div class="edit-mode-indicator" id="editModeIndicator">
        <i class="fas fa-edit"></i>
        <span>Edit Mode Active</span>
        <button onclick="toggleEditMode()" style="background: none; border: none; color: #1a365d; cursor: pointer; margin-left: 10px;">
            <i class="fas fa-times"></i>
        </button>
    </div>

    <!-- Quick Edit Tooltip -->
    <div class="quick-edit-tooltip" id="quickEditTooltip">Double-click to edit • Right-click for options</div>

    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-top">
                <div class="logo editable" data-id="logo">
                    <span class="edit-indicator">✏️</span>
                    The Definitive Word
                </div>
                
                <nav class="nav-main">
                    <a href="#home" class="active nav-link" data-tab="home">Home</a>
                    <a href="#books" class="nav-link" data-tab="books">Books</a>
                    <a href="#blog" class="nav-link" data-tab="blog">Blog</a>
                    <a href="#community" class="nav-link" data-tab="community">Community</a>
                    <a href="#payment" class="nav-link" data-tab="payment">Payment</a>
                    <a href="#about" class="nav-link" data-tab="about">About Us</a>
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
                <span class="edit-indicator">✏️</span>
                Welcome to The Definitive Word
            </h1>
            <p class="editable" data-id="hero-subtitle">
                <span class="edit-indicator">✏️</span>
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
                <span class="edit-indicator">✏️</span>
                Featured Ebooks
            </h2>
            <p class="section-subtitle editable" data-id="books-subtitle">
                <span class="edit-indicator">✏️</span>
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
                <span class="edit-indicator">✏️</span>
                Our Blog
            </h2>
            <p class="section-subtitle editable" data-id="blog-subtitle">
                <span class="edit-indicator">✏️</span>
                Insights, author interviews, reading recommendations, and literary discussions
            </p>
            
            <div class="blog-container">
                <div class="blog-posts" id="blogPosts">
                    <!-- Blog posts will be loaded here -->
                </div>
                
                <div class="blog-sidebar">
                    <div class="sidebar-widget">
                        <h3 class="widget-title editable" data-id="categories-title">
                            <span class="edit-indicator">✏️</span>
                            Categories
                        </h3>
                        <ul class="categories-list" id="categoriesList">
                            <!-- Categories will be loaded here -->
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Context Menu -->
    <div class="context-menu" id="contextMenu">
        <div class="context-menu-item" onclick="editElement()">
            <i class="fas fa-edit"></i>
            <span>Edit Content</span>
        </div>
        <div class="context-menu-item" onclick="toggleEditMode()">
            <i class="fas fa-magic"></i>
            <span id="toggleEditText">Enable Edit Mode</span>
        </div>
        <div class="context-menu-item" onclick="saveAllContent()">
            <i class="fas fa-save"></i>
            <span>Save Changes</span>
        </div>
        <div class="context-menu-item" onclick="resetToDefault()">
            <i class="fas fa-undo"></i>
            <span>Reset to Default</span>
        </div>
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
                <button class="modal-btn secondary" onclick="closeEditModal()">Cancel</button>
                <button class="modal-btn primary" onclick="saveEdit()">Save Changes</button>
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
        let clickTimer = null;
        let contextMenuElement = null;

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
            }
        ];

        // Initialize the application
        function initApp() {
            loadAllContent();
            displayBooks();
            setupNavigation();
            setupEditInteractions();
            loadCart();
            updateCartDisplay();
            showNotification('💡 Pro Tip: Double-click any text to edit, or right-click for editing options');
        }

        // Setup edit interactions (double-click and right-click)
        function setupEditInteractions() {
            // Setup for all editable elements
            document.querySelectorAll('.editable').forEach(element => {
                // Double-click to edit
                element.addEventListener('dblclick', function(e) {
                    e.preventDefault();
                    e.stopPropagation();
                    
                    if (editMode) {
                        openEditModal(this);
                    } else {
                        toggleEditMode();
                        openEditModal(this);
                    }
                });
                
                // Right-click for context menu
                element.addEventListener('contextmenu', function(e) {
                    e.preventDefault();
                    e.stopPropagation();
                    
                    contextMenuElement = this;
                    showContextMenu(e);
                });
                
                // Show tooltip on hover
                element.addEventListener('mouseenter', function(e) {
                    showQuickEditTooltip(e, this);
                });
                
                element.addEventListener('mouseleave', function() {
                    hideQuickEditTooltip();
                });
            });
            
            // Setup for navigation tabs
            document.querySelectorAll('.nav-link').forEach(tab => {
                // Double-click to edit tab name
                tab.addEventListener('dblclick', function(e) {
                    e.preventDefault();
                    e.stopPropagation();
                    
                    if (editMode) {
                        editTabName(this);
                    } else {
                        toggleEditMode();
                        editTabName(this);
                    }
                });
                
                // Right-click for context menu
                tab.addEventListener('contextmenu', function(e) {
                    e.preventDefault();
                    e.stopPropagation();
                    
                    contextMenuElement = this;
                    showContextMenu(e);
                });
                
                // Show tooltip on hover
                tab.addEventListener('mouseenter', function(e) {
                    showQuickEditTooltip(e, this);
                });
                
                tab.addEventListener('mouseleave', function() {
                    hideQuickEditTooltip();
                });
            });
            
            // Close context menu when clicking elsewhere
            document.addEventListener('click', function() {
                hideContextMenu();
            });
            
            // Handle escape key
            document.addEventListener('keydown', function(e) {
                if (e.key === 'Escape') {
                    hideContextMenu();
                    closeEditModal();
                }
            });
        }

        // Show context menu
        function showContextMenu(event) {
            const contextMenu = document.getElementById('contextMenu');
            const toggleEditText = document.getElementById('toggleEditText');
            
            // Update context menu text based on current mode
            toggleEditText.textContent = editMode ? 'Disable Edit Mode' : 'Enable Edit Mode';
            
            // Position context menu
            contextMenu.style.left = event.pageX + 'px';
            contextMenu.style.top = event.pageY + 'px';
            contextMenu.classList.add('active');
        }

        // Hide context menu
        function hideContextMenu() {
            const contextMenu = document.getElementById('contextMenu');
            contextMenu.classList.remove('active');
            contextMenuElement = null;
        }

        // Edit current element (from context menu)
        function editElement() {
            if (contextMenuElement) {
                if (contextMenuElement.classList.contains('nav-link')) {
                    editTabName(contextMenuElement);
                } else {
                    openEditModal(contextMenuElement);
                }
            }
            hideContextMenu();
        }

        // Toggle edit mode
        function toggleEditMode() {
            editMode = !editMode;
            document.body.classList.toggle('edit-mode-on', editMode);
            
            const indicator = document.getElementById('editModeIndicator');
            if (editMode) {
                indicator.classList.add('active');
                showNotification('✏️ Edit Mode Enabled: Double-click any text to edit, right-click for options');
            } else {
                indicator.classList.remove('active');
                showNotification('✅ Edit Mode Disabled');
            }
            
            hideContextMenu();
        }

        // Edit tab name
        function editTabName(tabElement) {
            const currentText = tabElement.textContent;
            const tabType = tabElement.getAttribute('data-tab');
            
            const newName = prompt(`Edit "${tabType}" tab name:`, currentText);
            if (newName && newName.trim() !== '') {
                tabElement.textContent = newName;
                saveTabContent(tabType, newName);
                showNotification(`✅ "${tabType}" tab renamed to "${newName}"`);
            }
        }

        // Save tab content
        function saveTabContent(tabId, content) {
            const savedTabs = JSON.parse(localStorage.getItem('websiteTabs')) || {};
            savedTabs[tabId] = content;
            localStorage.setItem('websiteTabs', JSON.stringify(savedTabs));
        }

        // Load tab content
        function loadTabContent() {
            const savedTabs = JSON.parse(localStorage.getItem('websiteTabs')) || {};
            document.querySelectorAll('.nav-link').forEach(tab => {
                const tabId = tab.getAttribute('data-tab');
                if (savedTabs[tabId]) {
                    tab.textContent = savedTabs[tabId];
                }
            });
        }

        // Show quick edit tooltip
        function showQuickEditTooltip(event, element) {
            if (editMode) {
                const tooltip = document.getElementById('quickEditTooltip');
                const rect = element.getBoundingClientRect();
                
                tooltip.style.left = (rect.left + rect.width / 2) + 'px';
                tooltip.style.top = (rect.top - 40) + 'px';
                tooltip.classList.add('show');
            }
        }

        // Hide quick edit tooltip
        function hideQuickEditTooltip() {
            const tooltip = document.getElementById('quickEditTooltip');
            tooltip.classList.remove('show');
        }

        // Setup navigation
        function setupNavigation() {
            document.querySelectorAll('.nav-link').forEach(link => {
                link.addEventListener('click', function(e) {
                    if (!editMode) {
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
                    }
                });
            });

            window.addEventListener('scroll', function() {
                if (!editMode) {
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
                }
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
                currentEditingElement.innerHTML = '<span class="edit-indicator">✏️</span> ' + newText;
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

        // Save all content
        function saveAllContent() {
            const content = {};
            document.querySelectorAll('.editable').forEach(element => {
                const id = element.getAttribute('data-id');
                const text = element.textContent.replace('✏️', '').trim();
                content[id] = text;
            });
            localStorage.setItem('websiteContent', JSON.stringify(content));
            showNotification('💾 All changes saved successfully!');
        }

        // Load all content
        function loadAllContent() {
            const saved = localStorage.getItem('websiteContent');
            if (saved) {
                const content = JSON.parse(saved);
                document.querySelectorAll('.editable').forEach(element => {
                    const id = element.getAttribute('data-id');
                    if (content[id]) {
                        element.innerHTML = '<span class="edit-indicator">✏️</span> ' + content[id];
                    }
                });
            }
            
            loadTabContent();
        }

        // Reset to default
        function resetToDefault() {
            if (confirm('Are you sure you want to reset all content to original? This cannot be undone.')) {
                localStorage.removeItem('websiteContent');
                localStorage.removeItem('websiteTabs');
                localStorage.removeItem('cart');
                location.reload();
            }
            hideContextMenu();
        }

        // Display books
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

        function updateCartDisplay() {
            const cartCount = document.getElementById('cartCount');
            const totalItems = cart.reduce((sum, item) => sum + item.quantity, 0);
            cartCount.textContent = totalItems;
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

        // Utility functions
        function showNotification(message) {
            const notification = document.getElementById('notification');
            notification.textContent = message;
            
            if (message.includes('✅') || message.includes('saved') || message.includes('Enabled')) {
                notification.style.background = '#38a169';
            } else if (message.includes('🛒')) {
                notification.style.background = '#d69e2e';
            } else {
                notification.style.background = '#d69e2e';
            }
            
            notification.className = 'notification show';
            setTimeout(() => {
                notification.className = 'notification';
            }, 4000);
        }

        // Placeholder functions for other features
        function toggleCart() {
            showNotification('Cart functionality would open here');
        }

        function toggleLogin() {
            showNotification('Login modal would open here');
        }

        // Initialize the app
        document.addEventListener('DOMContentLoaded', initApp);
    </script>
</body>
</html>

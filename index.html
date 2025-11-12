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

        /* Double-click indicator */
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

        /* Quick Edit Tooltip */
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

        /* ... rest of the CSS remains the same ... */

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
            
            .nav-main a::before {
                display: none; /* Hide double-click indicator on mobile */
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
            <span style="margin-left: 15px; font-size: 0.85em;">Click ✏️ icons to edit | Double-click tabs for quick edit</span>
        </div>
    </div>

    <!-- Quick Edit Tooltip -->
    <div class="quick-edit-tooltip" id="quickEditTooltip">Double-click to edit tab name</div>

    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-top">
                <div class="logo editable" data-id="logo">
                    <span class="edit-icon">✏️</span>
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

    <!-- ... Rest of the HTML remains the same ... -->

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
        let clickTimer = null;
        let lastClickedTab = null;

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
            setupEditing();
            setupDoubleClickTabs();
            loadCart();
            loadCommunityData();
            loadBlogData();
            updateCartDisplay();
            showNotification('Welcome to The Definitive Word! Click the EDIT button above to customize your site. Double-click any tab to quickly edit its name.');
        }

        // Setup double-click functionality for tabs
        function setupDoubleClickTabs() {
            document.querySelectorAll('.nav-link').forEach(tab => {
                // Single click - normal navigation
                tab.addEventListener('click', function(e) {
                    // Clear any existing timer
                    if (clickTimer) {
                        clearTimeout(clickTimer);
                        clickTimer = null;
                    }
                    
                    // Set timer to detect double click
                    clickTimer = setTimeout(() => {
                        // Single click behavior - normal navigation
                        if (!editMode) {
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
                        clickTimer = null;
                    }, 300);
                });
                
                // Double click - edit mode
                tab.addEventListener('dblclick', function(e) {
                    e.preventDefault();
                    
                    // Clear single click timer
                    if (clickTimer) {
                        clearTimeout(clickTimer);
                        clickTimer = null;
                    }
                    
                    // Enable edit mode if not already enabled
                    if (!editMode) {
                        toggleEditMode();
                    }
                    
                    // Edit the tab text
                    editTabName(this);
                });
                
                // Show tooltip on hover when in edit mode
                tab.addEventListener('mouseenter', function(e) {
                    if (editMode) {
                        showQuickEditTooltip(e, this);
                    }
                });
                
                tab.addEventListener('mouseleave', function() {
                    hideQuickEditTooltip();
                });
            });
        }

        // Edit tab name function
        function editTabName(tabElement) {
            if (!editMode) return;
            
            const currentText = tabElement.textContent;
            const tabType = tabElement.getAttribute('data-tab');
            
            const newName = prompt(`Edit ${tabType} tab name:`, currentText);
            if (newName && newName.trim() !== '') {
                tabElement.textContent = newName;
                
                // Save to localStorage
                saveTabContent(tabType, newName);
                showNotification(`✅ "${tabType}" tab renamed to "${newName}"`);
            }
        }

        // Save tab content to localStorage
        function saveTabContent(tabId, content) {
            const savedTabs = JSON.parse(localStorage.getItem('websiteTabs')) || {};
            savedTabs[tabId] = content;
            localStorage.setItem('websiteTabs', JSON.stringify(savedTabs));
        }

        // Load tab content from localStorage
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
            const tooltip = document.getElementById('quickEditTooltip');
            const rect = element.getBoundingClientRect();
            
            tooltip.style.left = (rect.left + rect.width / 2) + 'px';
            tooltip.style.top = (rect.top - 40) + 'px';
            tooltip.classList.add('show');
        }

        // Hide quick edit tooltip
        function hideQuickEditTooltip() {
            const tooltip = document.getElementById('quickEditTooltip');
            tooltip.classList.remove('show');
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
            
            // Show/hide quick edit tooltip
            if (!editMode) {
                hideQuickEditTooltip();
            }
            
            showNotification(editMode ? 
                '✏️ EDIT MODE ON: Click any yellow ✏️ icon to edit content! Double-click tabs to rename them.' : 
                '✅ Edit mode turned off');
        }

        // Setup navigation (updated for double-click compatibility)
        function setupNavigation() {
            // We're handling single clicks in setupDoubleClickTabs now
            // This function is kept for scroll-based active tab highlighting
            
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
                    if (editMode && !e.target.classList.contains('nav-link')) {
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
            
            // Load tab content
            loadTabContent();
        }

        // Reset to default content
        function resetToDefault() {
            if (confirm('Are you sure you want to reset all content to original? This cannot be undone.')) {
                localStorage.removeItem('websiteContent');
                localStorage.removeItem('websiteTabs');
                localStorage.removeItem('cart');
                localStorage.removeItem('discussions');
                localStorage.removeItem('reviews');
                localStorage.removeItem('blogPosts');
                localStorage.removeItem('blogCategories');
                localStorage.removeItem('blogTags');
                location.reload();
            }
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

        // ... Rest of the JavaScript functions remain the same ...

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

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Definitive Word - AI-Powered Ebook Store</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #1a365d;
            --secondary: #d69e2e;
            --accent: #c53030;
            --light: #f7fafc;
            --success: #38a169;
            --dark: #2d3748;
            --ai-blue: #4f46e5;
            --ai-purple: #7c3aed;
            --ai-gradient: linear-gradient(135deg, #4f46e5 0%, #7c3aed 100%);
            --ai-glow: 0 0 20px rgba(79, 70, 229, 0.3);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background: #0f172a;
            color: #e2e8f0;
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            width: 90%;
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header Styles */
        header {
            background: rgba(15, 23, 42, 0.95);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 1000;
            padding: 15px 0;
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 1.8rem;
            font-weight: 700;
            background: var(--ai-gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .logo i {
            font-size: 2rem;
        }

        .nav-main {
            display: flex;
            gap: 30px;
        }

        .nav-main a {
            color: #cbd5e1;
            text-decoration: none;
            font-weight: 600;
            padding: 8px 16px;
            border-radius: 8px;
            transition: all 0.3s ease;
            position: relative;
        }

        .nav-main a:hover, .nav-main a.active {
            color: white;
            background: rgba(79, 70, 229, 0.1);
        }

        .nav-main a.active::after {
            content: '';
            position: absolute;
            bottom: -2px;
            left: 16px;
            right: 16px;
            height: 2px;
            background: var(--ai-gradient);
            border-radius: 2px;
        }

        .header-actions {
            display: flex;
            gap: 15px;
            align-items: center;
        }

        .ai-assistant-btn {
            background: var(--ai-gradient);
            color: white;
            border: none;
            border-radius: 8px;
            padding: 10px 20px;
            font-weight: 600;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 8px;
            transition: all 0.3s ease;
            box-shadow: var(--ai-glow);
        }

        .ai-assistant-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(79, 70, 229, 0.4);
        }

        .cart-icon {
            position: relative;
            cursor: pointer;
            padding: 10px;
            border-radius: 8px;
            transition: background 0.3s ease;
        }

        .cart-icon:hover {
            background: rgba(255, 255, 255, 0.1);
        }

        .cart-count {
            position: absolute;
            top: 5px;
            right: 5px;
            background: var(--accent);
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

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #0f172a 0%, #1e293b 100%);
            padding: 150px 0 100px;
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
            background: 
                radial-gradient(circle at 20% 80%, rgba(79, 70, 229, 0.15) 0%, transparent 50%),
                radial-gradient(circle at 80% 20%, rgba(124, 58, 237, 0.15) 0%, transparent 50%),
                radial-gradient(circle at 40% 40%, rgba(214, 158, 46, 0.1) 0%, transparent 50%);
            z-index: 1;
        }

        .hero-content {
            position: relative;
            z-index: 2;
            text-align: center;
            max-width: 900px;
            margin: 0 auto;
        }

        .hero h1 {
            font-size: 4rem;
            font-weight: 800;
            margin-bottom: 20px;
            background: linear-gradient(to right, #e2e8f0, #94a3b8);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            line-height: 1.1;
        }

        .hero p {
            font-size: 1.3rem;
            color: #94a3b8;
            margin-bottom: 40px;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }

        .hero-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 15px 30px;
            border-radius: 10px;
            font-weight: 600;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            transition: all 0.3s ease;
            cursor: pointer;
            border: none;
            font-size: 1rem;
        }

        .btn-primary {
            background: var(--ai-gradient);
            color: white;
            box-shadow: var(--ai-glow);
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(79, 70, 229, 0.4);
        }

        .btn-secondary {
            background: rgba(255, 255, 255, 0.1);
            color: white;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .btn-secondary:hover {
            background: rgba(255, 255, 255, 0.2);
            transform: translateY(-3px);
        }

        /* AI Features Section */
        .ai-features {
            padding: 100px 0;
            background: #1e293b;
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-title h2 {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 15px;
            background: linear-gradient(to right, #e2e8f0, #94a3b8);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .section-title p {
            color: #94a3b8;
            font-size: 1.2rem;
            max-width: 600px;
            margin: 0 auto;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .feature-card {
            background: rgba(30, 41, 59, 0.7);
            border-radius: 15px;
            padding: 30px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
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
            background: var(--ai-gradient);
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
            border-color: rgba(79, 70, 229, 0.3);
        }

        .feature-icon {
            width: 70px;
            height: 70px;
            background: var(--ai-gradient);
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 20px;
            font-size: 1.8rem;
            color: white;
        }

        .feature-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: #e2e8f0;
        }

        .feature-card p {
            color: #94a3b8;
            margin-bottom: 20px;
        }

        /* Books Section */
        .books-section {
            padding: 100px 0;
            background: #0f172a;
        }

        .books-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 40px;
        }

        .books-filter {
            display: flex;
            gap: 15px;
        }

        .filter-btn {
            background: rgba(255, 255, 255, 0.05);
            color: #cbd5e1;
            border: 1px solid rgba(255, 255, 255, 0.1);
            padding: 10px 20px;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .filter-btn.active, .filter-btn:hover {
            background: var(--ai-gradient);
            color: white;
            border-color: transparent;
        }

        .books-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 30px;
        }

        .book-card {
            background: rgba(30, 41, 59, 0.7);
            border-radius: 15px;
            overflow: hidden;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
            position: relative;
        }

        .book-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
            border-color: rgba(79, 70, 229, 0.3);
        }

        .book-badge {
            position: absolute;
            top: 15px;
            right: 15px;
            background: var(--ai-gradient);
            color: white;
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 0.7rem;
            font-weight: 600;
            z-index: 2;
        }

        .book-cover {
            height: 250px;
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
            transform: scale(1.05);
        }

        .book-info {
            padding: 20px;
        }

        .book-title {
            font-size: 1.2rem;
            font-weight: 600;
            margin-bottom: 8px;
            color: #e2e8f0;
        }

        .book-author {
            color: #94a3b8;
            margin-bottom: 15px;
            font-size: 0.9rem;
        }

        .book-description {
            color: #cbd5e1;
            font-size: 0.9rem;
            margin-bottom: 20px;
            line-height: 1.5;
        }

        .book-footer {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .book-price {
            font-size: 1.3rem;
            font-weight: 700;
            color: #e2e8f0;
        }

        .add-to-cart {
            background: var(--ai-gradient);
            color: white;
            border: none;
            border-radius: 8px;
            padding: 10px 15px;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 8px;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .add-to-cart:hover {
            transform: scale(1.05);
            box-shadow: 0 5px 15px rgba(79, 70, 229, 0.4);
        }

        /* AI Assistant */
        .ai-assistant {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 400px;
            height: 600px;
            background: rgba(30, 41, 59, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
            z-index: 1000;
            display: flex;
            flex-direction: column;
            overflow: hidden;
            transform: translateY(100px);
            opacity: 0;
            transition: all 0.3s ease;
        }

        .ai-assistant.active {
            transform: translateY(0);
            opacity: 1;
        }

        .ai-header {
            background: var(--ai-gradient);
            padding: 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .ai-header h3 {
            color: white;
            font-size: 1.2rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .ai-close {
            background: none;
            border: none;
            color: white;
            font-size: 1.2rem;
            cursor: pointer;
        }

        .ai-messages {
            flex: 1;
            padding: 20px;
            overflow-y: auto;
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .ai-message {
            padding: 15px;
            border-radius: 15px;
            max-width: 85%;
            font-size: 0.9rem;
            line-height: 1.5;
        }

        .ai-message.user {
            background: var(--ai-gradient);
            color: white;
            align-self: flex-end;
            border-bottom-right-radius: 5px;
        }

        .ai-message.bot {
            background: rgba(255, 255, 255, 0.1);
            color: #e2e8f0;
            align-self: flex-start;
            border-bottom-left-radius: 5px;
        }

        .ai-input {
            padding: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            display: flex;
            gap: 10px;
        }

        .ai-input input {
            flex: 1;
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            padding: 12px 15px;
            color: white;
            outline: none;
        }

        .ai-input input:focus {
            border-color: rgba(79, 70, 229, 0.5);
        }

        .ai-send {
            background: var(--ai-gradient);
            color: white;
            border: none;
            border-radius: 10px;
            width: 45px;
            height: 45px;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .ai-send:hover {
            transform: scale(1.05);
        }

        /* Dashboard */
        .dashboard {
            padding: 100px 0;
            background: #1e293b;
        }

        .dashboard-tabs {
            display: flex;
            gap: 10px;
            margin-bottom: 30px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            padding-bottom: 10px;
        }

        .dashboard-tab {
            background: none;
            border: none;
            color: #94a3b8;
            padding: 10px 20px;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 600;
        }

        .dashboard-tab.active {
            color: white;
            background: rgba(79, 70, 229, 0.2);
        }

        .dashboard-content {
            background: rgba(30, 41, 59, 0.7);
            border-radius: 15px;
            padding: 30px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .stat-card {
            background: rgba(15, 23, 42, 0.5);
            border-radius: 10px;
            padding: 20px;
            text-align: center;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .stat-value {
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 5px;
            background: var(--ai-gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .stat-label {
            color: #94a3b8;
            font-size: 0.9rem;
        }

        /* Footer */
        footer {
            background: #0f172a;
            padding: 60px 0 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-column h3 {
            font-size: 1.2rem;
            margin-bottom: 20px;
            color: #e2e8f0;
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: 10px;
        }

        .footer-column a {
            color: #94a3b8;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-column a:hover {
            color: #e2e8f0;
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
            background: rgba(255, 255, 255, 0.05);
            border-radius: 50%;
            color: #94a3b8;
            transition: all 0.3s ease;
        }

        .social-links a:hover {
            background: var(--ai-gradient);
            color: white;
            transform: translateY(-3px);
        }

        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #94a3b8;
            font-size: 0.9rem;
        }

        /* Responsive Design */
        @media (max-width: 1024px) {
            .hero h1 {
                font-size: 3rem;
            }
            
            .nav-main {
                gap: 15px;
            }
            
            .ai-assistant {
                width: 350px;
                height: 500px;
            }
        }

        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 20px;
            }
            
            .nav-main {
                gap: 10px;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .btn {
                width: 100%;
                max-width: 300px;
                justify-content: center;
            }
            
            .ai-assistant {
                width: calc(100vw - 40px);
                right: 20px;
                bottom: 20px;
            }
            
            .books-header {
                flex-direction: column;
                gap: 20px;
                align-items: flex-start;
            }
            
            .books-filter {
                width: 100%;
                overflow-x: auto;
                padding-bottom: 10px;
            }
        }

        @media (max-width: 480px) {
            .hero h1 {
                font-size: 2rem;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
            
            .feature-card, .book-card {
                padding: 20px;
            }
            
            .books-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <i class="fas fa-book-open"></i>
                    <span>The Definitive Word</span>
                </div>
                
                <nav class="nav-main">
                    <a href="#home" class="active">Home</a>
                    <a href="#features">AI Features</a>
                    <a href="#books">Books</a>
                    <a href="#dashboard">Dashboard</a>
                    <a href="#ministry">Ministry</a>
                    <a href="#community">Community</a>
                </nav>
                
                <div class="header-actions">
                    <button class="ai-assistant-btn" id="aiAssistantBtn">
                        <i class="fas fa-robot"></i>
                        AI Assistant
                    </button>
                    <div class="cart-icon" id="cartIcon">
                        <i class="fas fa-shopping-cart"></i>
                        <div class="cart-count" id="cartCount">0</div>
                    </div>
                    <button class="btn btn-secondary" id="loginBtn">
                        <i class="fas fa-user"></i>
                        Login
                    </button>
                </div>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <h1>AI-Powered Ebook Store & Ministry Platform</h1>
                <p>Discover, read, and grow with our intelligent ebook platform. Personalized recommendations, AI-powered insights, and a thriving community await you.</p>
                <div class="hero-buttons">
                    <a href="#books" class="btn btn-primary">
                        <i class="fas fa-book"></i>
                        Browse Books
                    </a>
                    <a href="#features" class="btn btn-secondary">
                        <i class="fas fa-robot"></i>
                        Explore AI Features
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- AI Features Section -->
    <section class="ai-features" id="features">
        <div class="container">
            <div class="section-title">
                <h2>AI-Powered Features</h2>
                <p>Experience the future of reading with our intelligent platform</p>
            </div>
            
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-brain"></i>
                    </div>
                    <h3>Smart Recommendations</h3>
                    <p>Our AI analyzes your reading patterns to suggest books you'll love based on your interests and reading history.</p>
                    <a href="#" class="btn btn-secondary">Try It</a>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-comments"></i>
                    </div>
                    <h3>AI Reading Assistant</h3>
                    <p>Get instant summaries, vocabulary help, and contextual insights as you read with our intelligent assistant.</p>
                    <a href="#" class="btn btn-secondary">Learn More</a>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <h3>Reading Analytics</h3>
                    <p>Track your reading progress, set goals, and get insights into your reading habits with detailed analytics.</p>
                    <a href="#" class="btn btn-secondary">View Dashboard</a>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-pen-nib"></i>
                    </div>
                    <h3>AI Writing Assistant</h3>
                    <p>Get help with your writing projects, from generating ideas to refining your manuscript with AI-powered tools.</p>
                    <a href="#" class="btn btn-secondary">Start Writing</a>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-users"></i>
                    </div>
                    <h3>Community Insights</h3>
                    <p>Connect with like-minded readers, join discussions, and discover books popular in your community.</p>
                    <a href="#" class="btn btn-secondary">Join Community</a>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-hands-helping"></i>
                    </div>
                    <h3>Ministry Resources</h3>
                    <p>Access curated spiritual content, Bible studies, and ministry tools tailored to your spiritual journey.</p>
                    <a href="#" class="btn btn-secondary">Explore Ministry</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Books Section -->
    <section class="books-section" id="books">
        <div class="container">
            <div class="section-title">
                <h2>Featured Ebooks</h2>
                <p>Discover our curated collection of transformative reads</p>
            </div>
            
            <div class="books-header">
                <h3>AI-Curated Selection</h3>
                <div class="books-filter">
                    <button class="filter-btn active">All</button>
                    <button class="filter-btn">Spiritual</button>
                    <button class="filter-btn">Fiction</button>
                    <button class="filter-btn">Non-Fiction</button>
                    <button class="filter-btn">Business</button>
                </div>
            </div>
            
            <div class="books-grid" id="booksGrid">
                <!-- Books will be dynamically loaded here -->
            </div>
        </div>
    </section>

    <!-- Dashboard Section -->
    <section class="dashboard" id="dashboard">
        <div class="container">
            <div class="section-title">
                <h2>Your Reading Dashboard</h2>
                <p>Track your progress and discover new insights</p>
            </div>
            
            <div class="dashboard-tabs">
                <button class="dashboard-tab active">Overview</button>
                <button class="dashboard-tab">Reading Stats</button>
                <button class="dashboard-tab">My Library</button>
                <button class="dashboard-tab">Community</button>
                <button class="dashboard-tab">Ministry</button>
            </div>
            
            <div class="dashboard-content">
                <div class="stats-grid">
                    <div class="stat-card">
                        <div class="stat-value">12</div>
                        <div class="stat-label">Books Read</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-value">36</div>
                        <div class="stat-label">Reading Hours</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-value">4.8</div>
                        <div class="stat-label">Avg. Rating</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-value">78%</div>
                        <div class="stat-label">AI Match Score</div>
                    </div>
                </div>
                
                <h3>Recommended For You</h3>
                <p>Based on your reading history and preferences, we think you'll love these books:</p>
                
                <div class="books-grid" style="grid-template-columns: repeat(auto-fill, minmax(200px, 1fr)); margin-top: 20px;">
                    <!-- Recommended books will be loaded here -->
                </div>
            </div>
        </div>
    </section>

    <!-- AI Assistant -->
    <div class="ai-assistant" id="aiAssistant">
        <div class="ai-header">
            <h3><i class="fas fa-robot"></i> AI Book Assistant</h3>
            <button class="ai-close" id="aiClose">
                <i class="fas fa-times"></i>
            </button>
        </div>
        <div class="ai-messages" id="aiMessages">
            <div class="ai-message bot">
                Hi! I'm your AI book assistant. How can I help you today? I can recommend books, help with reading, or answer questions about our platform.
            </div>
        </div>
        <div class="ai-input">
            <input type="text" id="aiInput" placeholder="Ask me about books, recommendations...">
            <button class="ai-send" id="aiSend">
                <i class="fas fa-paper-plane"></i>
            </button>
        </div>
    </div>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>The Definitive Word</h3>
                    <p>South Africa's premier AI-powered ebook store and ministry platform, offering personalized reading experiences and spiritual growth resources.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    </div>
                </div>
                
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#features">AI Features</a></li>
                        <li><a href="#books">Books</a></li>
                        <li><a href="#dashboard">Dashboard</a></li>
                        <li><a href="#ministry">Ministry</a></li>
                        <li><a href="#community">Community</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>AI Services</h3>
                    <ul>
                        <li><a href="#">Book Recommendations</a></li>
                        <li><a href="#">Reading Assistant</a></li>
                        <li><a href="#">Writing Assistant</a></li>
                        <li><a href="#">Reading Analytics</a></li>
                        <li><a href="#">Community Insights</a></li>
                        <li><a href="#">Ministry Tools</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>Contact Us</h3>
                    <ul>
                        <li><i class="fas fa-map-marker-alt"></i> 123 Book Street, Johannesburg</li>
                        <li><i class="fas fa-phone"></i> +27 11 123 4567</li>
                        <li><i class="fas fa-envelope"></i> info@definitiveword.co.za</li>
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 The Definitive Word. All rights reserved. | AI-Powered Ebook Store</p>
            </div>
        </div>
    </footer>

    <script>
        // Sample data for books
        const sampleBooks = [
            {
                id: 1,
                title: "The Path to Spiritual Maturity",
                author: "Dr. Michael Johnson",
                price: 249.99,
                image: "https://images.unsplash.com/photo-1544947950-fa07a98d237f?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                badge: "Bestseller",
                description: "A comprehensive guide to deepening your spiritual walk and understanding biblical principles.",
                category: "spiritual"
            },
            {
                id: 2,
                title: "Digital Revolution",
                author: "Alex Chen",
                price: 299.99,
                image: "https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                badge: "New",
                description: "How technology is reshaping our world and what it means for the future of business and society.",
                category: "business"
            },
            {
                id: 3,
                title: "The Silent Observer",
                author: "Megan Foster",
                price: 279.99,
                image: "https://images.unsplash.com/photo-1512820790803-83ca734da794?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                badge: "Popular",
                description: "A psychological thriller that explores the depths of human consciousness and perception.",
                category: "fiction"
            },
            {
                id: 4,
                title: "Business Mastery",
                author: "Sarah Johnson",
                price: 349.99,
                image: "https://images.unsplash.com/photo-1481627834876-b7833e8f5570?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                badge: "",
                description: "Essential strategies for entrepreneurial success in the modern economy and digital landscape.",
                category: "business"
            },
            {
                id: 5,
                title: "African Skies",
                author: "Tendai Moyo",
                price: 229.99,
                image: "https://images.unsplash.com/photo-1506880018603-83d5b814b5a6?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                badge: "Local Author",
                description: "A captivating novel set against the backdrop of contemporary South Africa and its diverse cultures.",
                category: "fiction"
            },
            {
                id: 6,
                title: "Prayer That Changes Everything",
                author: "Sarah Williams",
                price: 199.99,
                image: "https://images.unsplash.com/photo-1544716278-ca5e3f4abd8c?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                badge: "Featured",
                description: "Discover the power of prayer and how to develop a consistent prayer life that transforms your circumstances.",
                category: "spiritual"
            }
        ];

        // Global variables
        let cart = [];
        let currentUser = null;
        let aiChatHistory = [];

        // Initialize the application
        document.addEventListener('DOMContentLoaded', function() {
            initApp();
        });

        function initApp() {
            // Load books
            displayBooks();
            
            // Setup event listeners
            setupEventListeners();
            
            // Load user data from localStorage
            loadUserData();
            
            // Update UI
            updateCartDisplay();
            
            // Show welcome message
            setTimeout(() => {
                showNotification('Welcome to The Definitive Word! Explore our AI-powered features.');
            }, 1000);
        }

        function setupEventListeners() {
            // AI Assistant
            document.getElementById('aiAssistantBtn').addEventListener('click', toggleAIAssistant);
            document.getElementById('aiClose').addEventListener('click', toggleAIAssistant);
            document.getElementById('aiSend').addEventListener('click', sendAIMessage);
            document.getElementById('aiInput').addEventListener('keypress', function(e) {
                if (e.key === 'Enter') sendAIMessage();
            });
            
            // Cart
            document.getElementById('cartIcon').addEventListener('click', toggleCart);
            
            // Login
            document.getElementById('loginBtn').addEventListener('click', toggleLogin);
            
            // Filter buttons
            document.querySelectorAll('.filter-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
                    this.classList.add('active');
                    filterBooks(this.textContent);
                });
            });
            
            // Dashboard tabs
            document.querySelectorAll('.dashboard-tab').forEach(tab => {
                tab.addEventListener('click', function() {
                    document.querySelectorAll('.dashboard-tab').forEach(t => t.classList.remove('active'));
                    this.classList.add('active');
                    // In a real app, this would load different dashboard content
                });
            });
            
            // Smooth scrolling for navigation links
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function(e) {
                    e.preventDefault();
                    const target = document.querySelector(this.getAttribute('href'));
                    if (target) {
                        target.scrollIntoView({
                            behavior: 'smooth',
                            block: 'start'
                        });
                    }
                });
            });
        }

        function displayBooks() {
            const booksGrid = document.getElementById('booksGrid');
            booksGrid.innerHTML = '';
            
            sampleBooks.forEach(book => {
                const bookCard = document.createElement('div');
                bookCard.className = 'book-card';
                bookCard.innerHTML = `
                    ${book.badge ? `<div class="book-badge">${book.badge}</div>` : ''}
                    <div class="book-cover">
                        <img src="${book.image}" alt="${book.title}">
                    </div>
                    <div class="book-info">
                        <h3 class="book-title">${book.title}</h3>
                        <p class="book-author">by ${book.author}</p>
                        <p class="book-description">${book.description}</p>
                        <div class="book-footer">
                            <div class="book-price">R${book.price.toFixed(2)}</div>
                            <button class="add-to-cart" data-id="${book.id}">
                                <i class="fas fa-cart-plus"></i>
                                Add to Cart
                            </button>
                        </div>
                    </div>
                `;
                booksGrid.appendChild(bookCard);
            });
            
            // Add event listeners to Add to Cart buttons
            document.querySelectorAll('.add-to-cart').forEach(btn => {
                btn.addEventListener('click', function() {
                    const bookId = parseInt(this.getAttribute('data-id'));
                    addToCart(bookId);
                });
            });
        }

        function filterBooks(category) {
            const booksGrid = document.getElementById('booksGrid');
            booksGrid.innerHTML = '';
            
            let filteredBooks = sampleBooks;
            if (category !== 'All') {
                filteredBooks = sampleBooks.filter(book => {
                    return book.category === category.toLowerCase();
                });
            }
            
            filteredBooks.forEach(book => {
                const bookCard = document.createElement('div');
                bookCard.className = 'book-card';
                bookCard.innerHTML = `
                    ${book.badge ? `<div class="book-badge">${book.badge}</div>` : ''}
                    <div class="book-cover">
                        <img src="${book.image}" alt="${book.title}">
                    </div>
                    <div class="book-info">
                        <h3 class="book-title">${book.title}</h3>
                        <p class="book-author">by ${book.author}</p>
                        <p class="book-description">${book.description}</p>
                        <div class="book-footer">
                            <div class="book-price">R${book.price.toFixed(2)}</div>
                            <button class="add-to-cart" data-id="${book.id}">
                                <i class="fas fa-cart-plus"></i>
                                Add to Cart
                            </button>
                        </div>
                    </div>
                `;
                booksGrid.appendChild(bookCard);
            });
            
            // Re-add event listeners to Add to Cart buttons
            document.querySelectorAll('.add-to-cart').forEach(btn => {
                btn.addEventListener('click', function() {
                    const bookId = parseInt(this.getAttribute('data-id'));
                    addToCart(bookId);
                });
            });
        }

        function addToCart(bookId) {
            const book = sampleBooks.find(b => b.id === bookId);
            if (book) {
                const existingItem = cart.find(item => item.id === bookId);
                
                if (existingItem) {
                    existingItem.quantity += 1;
                } else {
                    cart.push({
                        ...book,
                        quantity: 1
                    });
                }
                
                updateCartDisplay();
                showNotification(`"${book.title}" added to cart!`);
                
                // Save to localStorage
                localStorage.setItem('cart', JSON.stringify(cart));
            }
        }

        function updateCartDisplay() {
            const cartCount = document.getElementById('cartCount');
            const totalItems = cart.reduce((sum, item) => sum + item.quantity, 0);
            cartCount.textContent = totalItems;
        }

        function toggleAIAssistant() {
            const assistant = document.getElementById('aiAssistant');
            assistant.classList.toggle('active');
        }

        function sendAIMessage() {
            const input = document.getElementById('aiInput');
            const message = input.value.trim();
            
            if (!message) return;
            
            // Add user message to chat
            addAIMessage(message, 'user');
            input.value = '';
            
            // Simulate AI response
            setTimeout(() => {
                const response = generateAIResponse(message);
                addAIMessage(response, 'bot');
            }, 1000);
        }

        function addAIMessage(message, sender) {
            const messagesContainer = document.getElementById('aiMessages');
            const messageElement = document.createElement('div');
            messageElement.className = `ai-message ${sender}`;
            messageElement.textContent = message;
            messagesContainer.appendChild(messageElement);
            
            // Scroll to bottom
            messagesContainer.scrollTop = messagesContainer.scrollHeight;
            
            // Save to history
            aiChatHistory.push({ sender, message });
            localStorage.setItem('aiChatHistory', JSON.stringify(aiChatHistory));
        }

        function generateAIResponse(userMessage) {
            const lowerMessage = userMessage.toLowerCase();
            
            if (lowerMessage.includes('recommend') || lowerMessage.includes('suggest')) {
                return "Based on your reading history, I'd recommend 'The Path to Spiritual Maturity' and 'Prayer That Changes Everything'. Would you like more specific recommendations?";
            } else if (lowerMessage.includes('help') || lowerMessage.includes('assistant')) {
                return "I can help you find books, provide reading assistance, generate writing ideas, and analyze your reading habits. What would you like help with?";
            } else if (lowerMessage.includes('spiritual') || lowerMessage.includes('faith')) {
                return "We have a great selection of spiritual books. 'The Path to Spiritual Maturity' is our most popular, and 'Prayer That Changes Everything' has excellent reviews. Would you like to explore our ministry section?";
            } else if (lowerMessage.includes('price') || lowerMessage.includes('cost')) {
                return "Our ebook prices range from R199 to R349. We also have frequent promotions and bundle deals. Is there a specific book you're interested in?";
            } else {
                return "I'm here to help with all things related to books and reading. You can ask me for recommendations, writing help, or book summaries. What would you like to know?";
            }
        }

        function toggleCart() {
            // In a full implementation, this would open a cart modal
            showNotification(`You have ${cart.reduce((sum, item) => sum + item.quantity, 0)} items in your cart.`);
        }

        function toggleLogin() {
            if (currentUser) {
                // Logout
                currentUser = null;
                document.getElementById('loginBtn').innerHTML = '<i class="fas fa-user"></i> Login';
                showNotification('You have been logged out.');
            } else {
                // Simulate login
                currentUser = {
                    name: 'John Doe',
                    email: 'john@example.com'
                };
                document.getElementById('loginBtn').innerHTML = '<i class="fas fa-user-check"></i> John';
                showNotification('Welcome back, John!');
            }
        }

        function loadUserData() {
            // Load cart from localStorage
            const savedCart = localStorage.getItem('cart');
            if (savedCart) {
                cart = JSON.parse(savedCart);
            }
            
            // Load AI chat history
            const savedChat = localStorage.getItem('aiChatHistory');
            if (savedChat) {
                aiChatHistory = JSON.parse(savedChat);
                displayAIChatHistory();
            }
        }

        function displayAIChatHistory() {
            const messagesContainer = document.getElementById('aiMessages');
            messagesContainer.innerHTML = '';
            
            aiChatHistory.forEach(msg => {
                const messageElement = document.createElement('div');
                messageElement.className = `ai-message ${msg.sender}`;
                messageElement.textContent = msg.message;
                messagesContainer.appendChild(messageElement);
            });
            
            // Scroll to bottom
            messagesContainer.scrollTop = messagesContainer.scrollHeight;
        }

        function showNotification(message) {
            // Create notification element
            const notification = document.createElement('div');
            notification.style.cssText = `
                position: fixed;
                top: 100px;
                right: 30px;
                background: var(--ai-gradient);
                color: white;
                padding: 15px 25px;
                border-radius: 10px;
                box-shadow: 0 5px 15px rgba(0,0,0,0.3);
                z-index: 1001;
                max-width: 300px;
                animation: slideInRight 0.3s ease;
            `;
            notification.textContent = message;
            
            document.body.appendChild(notification);
            
            // Remove after 3 seconds
            setTimeout(() => {
                notification.style.animation = 'slideOutRight 0.3s ease';
                setTimeout(() => {
                    document.body.removeChild(notification);
                }, 300);
            }, 3000);
        }

        // Add CSS for notification animations
        const style = document.createElement('style');
        style.textContent = `
            @keyframes slideInRight {
                from { transform: translateX(100%); opacity: 0; }
                to { transform: translateX(0); opacity: 1; }
            }
            @keyframes slideOutRight {
                from { transform: translateX(0); opacity: 1; }
                to { transform: translateX(100%); opacity: 0; }
            }
        `;
        document.head.appendChild(style);
    </script>
</body>
</html>

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
            scroll-behavior: smooth;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        /* === AI ENHANCEMENTS === */
        .ai-badge {
            background: var(--ai-gradient);
            color: white;
            padding: 4px 10px;
            border-radius: 20px;
            font-size: 0.7rem;
            font-weight: 600;
            display: inline-flex;
            align-items: center;
            gap: 5px;
            margin-left: 8px;
            animation: pulse 2s infinite;
        }

        .ai-feature {
            border-left: 4px solid var(--ai-blue);
            background: rgba(79, 70, 229, 0.05);
            padding: 15px;
            margin: 15px 0;
            border-radius: 0 8px 8px 0;
        }

        .ai-chat-container {
            position: fixed;
            bottom: 20px;
            right: 20px;
            width: 350px;
            height: 500px;
            background: white;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            z-index: 10000;
            display: flex;
            flex-direction: column;
            overflow: hidden;
            transform: translateY(100px);
            opacity: 0;
            transition: all 0.3s ease;
        }

        .ai-chat-container.active {
            transform: translateY(0);
            opacity: 1;
        }

        .ai-chat-header {
            background: var(--ai-gradient);
            color: white;
            padding: 15px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .ai-chat-messages {
            flex: 1;
            padding: 15px;
            overflow-y: auto;
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .ai-message {
            padding: 10px 15px;
            border-radius: 18px;
            max-width: 80%;
            font-size: 0.9rem;
        }

        .ai-message.user {
            background: var(--ai-blue);
            color: white;
            align-self: flex-end;
            border-bottom-right-radius: 4px;
        }

        .ai-message.bot {
            background: #f1f5f9;
            color: #334155;
            align-self: flex-start;
            border-bottom-left-radius: 4px;
        }

        .ai-chat-input {
            padding: 15px;
            border-top: 1px solid #e2e8f0;
            display: flex;
            gap: 10px;
        }

        .ai-chat-input input {
            flex: 1;
            padding: 10px 15px;
            border: 1px solid #ddd;
            border-radius: 20px;
            outline: none;
        }

        .ai-chat-input button {
            background: var(--ai-blue);
            color: white;
            border: none;
            border-radius: 50%;
            width: 40px;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
        }

        .ai-recommendations {
            background: white;
            border-radius: 12px;
            padding: 25px;
            margin: 30px 0;
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
            border: 1px solid #e2e8f0;
        }

        .ai-recommendation-item {
            display: flex;
            gap: 15px;
            padding: 15px;
            border-radius: 8px;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .ai-recommendation-item:hover {
            background: #f8fafc;
        }

        .ai-recommendation-cover {
            width: 60px;
            height: 80px;
            border-radius: 6px;
            overflow: hidden;
        }

        .ai-recommendation-cover img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .ai-recommendation-details {
            flex: 1;
        }

        .ai-recommendation-title {
            font-weight: 600;
            margin-bottom: 5px;
        }

        .ai-recommendation-reason {
            font-size: 0.85rem;
            color: #64748b;
        }

        .ai-personalization-panel {
            background: white;
            border-radius: 12px;
            padding: 25px;
            margin: 30px 0;
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
        }

        .ai-personalization-options {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }

        .ai-option {
            background: #f8fafc;
            border: 2px solid #e2e8f0;
            border-radius: 8px;
            padding: 15px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .ai-option:hover, .ai-option.active {
            border-color: var(--ai-blue);
            background: rgba(79, 70, 229, 0.05);
        }

        .ai-option i {
            font-size: 1.5rem;
            color: var(--ai-blue);
            margin-bottom: 10px;
        }

        .ai-content-generator {
            background: white;
            border-radius: 12px;
            padding: 25px;
            margin: 30px 0;
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
        }

        .ai-generator-input {
            display: flex;
            gap: 10px;
            margin-bottom: 15px;
        }

        .ai-generator-input input {
            flex: 1;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 8px;
            outline: none;
        }

        .ai-generator-output {
            background: #f8fafc;
            border-radius: 8px;
            padding: 15px;
            min-height: 100px;
            border: 1px dashed #cbd5e1;
        }

        .ai-reading-assistant {
            position: fixed;
            top: 50%;
            right: 20px;
            transform: translateY(-50%);
            background: white;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            z-index: 9999;
            width: 300px;
            overflow: hidden;
            display: none;
        }

        .ai-reading-assistant.active {
            display: block;
        }

        .ai-assistant-header {
            background: var(--ai-gradient);
            color: white;
            padding: 15px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .ai-assistant-content {
            padding: 15px;
            max-height: 400px;
            overflow-y: auto;
        }

        .ai-summary {
            background: #f1f5f9;
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 15px;
        }

        .ai-vocabulary {
            margin-top: 15px;
        }

        .ai-vocabulary-item {
            display: flex;
            justify-content: space-between;
            padding: 8px 0;
            border-bottom: 1px solid #e2e8f0;
        }

        .ai-vocabulary-item:last-child {
            border-bottom: none;
        }

        /* === EXISTING STYLES (with AI enhancements) === */
        /* ... (all your existing CSS styles remain the same) ... */
        
        /* Adding AI-specific animations */
        @keyframes aiGlow {
            0% { box-shadow: 0 0 5px rgba(79, 70, 229, 0.5); }
            50% { box-shadow: 0 0 20px rgba(79, 70, 229, 0.8); }
            100% { box-shadow: 0 0 5px rgba(79, 70, 229, 0.5); }
        }

        .ai-glow {
            animation: aiGlow 2s infinite;
        }

        /* Responsive adjustments for AI elements */
        @media (max-width: 768px) {
            .ai-chat-container {
                width: calc(100vw - 40px);
                height: 60vh;
                bottom: 10px;
                right: 10px;
            }
            
            .ai-reading-assistant {
                width: calc(100vw - 40px);
                right: 10px;
                left: 10px;
            }
            
            .ai-personalization-options {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- AI Chat Assistant -->
    <div class="ai-chat-container" id="aiChatContainer">
        <div class="ai-chat-header">
            <div>
                <h3>AI Book Assistant</h3>
                <p>Ask me about books, recommendations, or writing help</p>
            </div>
            <button onclick="toggleAIChat()" style="background: none; border: none; color: white; cursor: pointer;">
                <i class="fas fa-times"></i>
            </button>
        </div>
        <div class="ai-chat-messages" id="aiChatMessages">
            <div class="ai-message bot">
                Hi! I'm your AI book assistant. How can I help you today?
            </div>
        </div>
        <div class="ai-chat-input">
            <input type="text" id="aiChatInput" placeholder="Ask about books, recommendations...">
            <button onclick="sendAIMessage()">
                <i class="fas fa-paper-plane"></i>
            </button>
        </div>
    </div>

    <!-- AI Reading Assistant -->
    <div class="ai-reading-assistant" id="aiReadingAssistant">
        <div class="ai-assistant-header">
            <h3>AI Reading Assistant</h3>
            <button onclick="toggleReadingAssistant()" style="background: none; border: none; color: white; cursor: pointer;">
                <i class="fas fa-times"></i>
            </button>
        </div>
        <div class="ai-assistant-content" id="aiAssistantContent">
            <p>Select a book to get AI-powered insights, summaries, and vocabulary help.</p>
        </div>
    </div>

    <!-- Edit Mode Indicator -->
    <div class="edit-mode-indicator" id="editModeIndicator">
        <i class="fas fa-edit"></i>
        <span>Edit Mode Active</span>
        <button onclick="toggleEditMode()" style="background: none; border: none; color: #1a365d; cursor: pointer; margin-left: 10px;">
            <i class="fas fa-times"></i>
        </button>
    </div>

    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-top">
                <div class="logo editable" data-id="logo">
                    <span class="edit-indicator">✏️</span>
                    The Definitive Word <span class="ai-badge">AI-Powered</span>
                </div>
                
                <nav class="nav-main">
                    <a href="#home" class="active nav-link" data-tab="home">Home</a>
                    <a href="#books" class="nav-link" data-tab="books">Books</a>
                    <a href="#ai-features" class="nav-link" data-tab="ai-features">AI Features</a>
                    <a href="#ministry" class="nav-link" data-tab="ministry">Ministry</a>
                    <a href="#community" class="nav-link" data-tab="community">Community</a>
                    <a href="#payment" class="nav-link" data-tab="payment">Payment</a>
                </nav>
                
                <div class="header-actions">
                    <button class="btn" onclick="toggleAIChat()" style="background: var(--ai-gradient);">
                        <i class="fas fa-robot"></i> AI Assistant
                    </button>
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
                South Africa's first AI-powered ebook store with personalized recommendations and intelligent features
            </p>
            <div style="margin-top: 35px;">
                <a href="#books" class="btn">
                    <i class="fas fa-gem"></i>
                    Browse Books
                </a>
                <a href="#ai-features" class="btn" style="background: var(--ai-gradient);">
                    <i class="fas fa-robot"></i>
                    Explore AI Features
                </a>
            </div>
        </div>
    </section>

    <!-- Books Section -->
    <section id="books" class="section books-section">
        <div class="container">
            <h2 class="section-title editable" data-id="books-title">
                <span class="edit-indicator">✏️</span>
                AI-Curated Ebooks
            </h2>
            <p class="section-subtitle editable" data-id="books-subtitle">
                <span class="edit-indicator">✏️</span>
                Discover books selected by our AI based on your reading preferences and behavior
            </p>
            
            <!-- AI Personalization Panel -->
            <div class="ai-personalization-panel">
                <h3>Personalize Your Experience</h3>
                <p>Tell us what you're interested in for better recommendations</p>
                
                <div class="ai-personalization-options">
                    <div class="ai-option" onclick="togglePreference('fiction')">
                        <i class="fas fa-book-open"></i>
                        <p>Fiction</p>
                    </div>
                    <div class="ai-option" onclick="togglePreference('nonfiction')">
                        <i class="fas fa-chart-bar"></i>
                        <p>Non-Fiction</p>
                    </div>
                    <div class="ai-option" onclick="togglePreference('spiritual')">
                        <i class="fas fa-pray"></i>
                        <p>Spiritual</p>
                    </div>
                    <div class="ai-option" onclick="togglePreference('business')">
                        <i class="fas fa-briefcase"></i>
                        <p>Business</p>
                    </div>
                    <div class="ai-option" onclick="togglePreference('selfhelp')">
                        <i class="fas fa-hands-helping"></i>
                        <p>Self-Help</p>
                    </div>
                    <div class="ai-option" onclick="togglePreference('biography')">
                        <i class="fas fa-user"></i>
                        <p>Biography</p>
                    </div>
                </div>
                
                <button class="btn" style="width: 100%; margin-top: 20px; background: var(--ai-gradient);" onclick="generatePersonalizedRecommendations()">
                    <i class="fas fa-magic"></i> Generate Personalized Recommendations
                </button>
            </div>
            
            <!-- AI Recommendations -->
            <div class="ai-recommendations" id="aiRecommendations">
                <h3>AI Recommendations For You</h3>
                <p>Based on your reading history and preferences</p>
                
                <div id="aiRecommendationsList">
                    <!-- AI recommendations will be populated here -->
                </div>
            </div>
            
            <div class="books-grid" id="booksGrid">
                <!-- Books will be loaded here -->
            </div>
        </div>
    </section>

    <!-- AI Features Section -->
    <section id="ai-features" class="section" style="background: #f8fafc;">
        <div class="container">
            <h2 class="section-title editable" data-id="ai-features-title">
                <span class="edit-indicator">✏️</span>
                AI-Powered Features
            </h2>
            <p class="section-subtitle editable" data-id="ai-features-subtitle">
                <span class="edit-indicator">✏️</span>
                Experience the future of reading with our intelligent AI features
            </p>
            
            <div class="ministry-features">
                <div class="ministry-feature">
                    <i class="fas fa-robot icon-editable" style="color: var(--ai-blue);"></i>
                    <h3 class="editable" data-id="ai-feature1-title">
                        <span class="edit-indicator">✏️</span>
                        Smart Recommendations
                    </h3>
                    <p class="editable" data-id="ai-feature1-desc">
                        <span class="edit-indicator">✏️</span>
                        Our AI analyzes your reading patterns to suggest books you'll love
                    </p>
                </div>
                <div class="ministry-feature">
                    <i class="fas fa-comment-alt icon-editable" style="color: var(--ai-blue);"></i>
                    <h3 class="editable" data-id="ai-feature2-title">
                        <span class="edit-indicator">✏️</span>
                        AI Reading Assistant
                    </h3>
                    <p class="editable" data-id="ai-feature2-desc">
                        <span class="edit-indicator">✏️</span>
                        Get summaries, vocabulary help, and insights as you read
                    </p>
                </div>
                <div class="ministry-feature">
                    <i class="fas fa-pen-nib icon-editable" style="color: var(--ai-blue);"></i>
                    <h3 class="editable" data-id="ai-feature3-title">
                        <span class="edit-indicator">✏️</span>
                        AI Writing Assistant
                    </h3>
                    <p class="editable" data-id="ai-feature3-desc">
                        <span class="edit-indicator">✏️</span>
                        Get help with your own writing projects and book ideas
                    </p>
                </div>
            </div>
            
            <!-- AI Content Generator -->
            <div class="ai-content-generator">
                <h3>AI Writing Assistant</h3>
                <p>Need help with your writing? Our AI can assist with book ideas, outlines, and more.</p>
                
                <div class="ai-generator-input">
                    <input type="text" id="aiWritingPrompt" placeholder="e.g., 'Help me outline a book about spiritual growth'">
                    <button class="btn" style="background: var(--ai-gradient);" onclick="generateContent()">
                        <i class="fas fa-magic"></i> Generate
                    </button>
                </div>
                
                <div class="ai-generator-output" id="aiWritingOutput">
                    Your AI-generated content will appear here...
                </div>
            </div>
            
            <!-- AI Reading Stats -->
            <div class="ai-personalization-panel">
                <h3>Your Reading Analytics</h3>
                <p>AI-powered insights into your reading habits</p>
                
                <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 20px; margin-top: 20px;">
                    <div style="text-align: center; padding: 20px; background: #f1f5f9; border-radius: 8px;">
                        <h4 style="color: var(--ai-blue); font-size: 2rem;">12</h4>
                        <p>Books Read This Year</p>
                    </div>
                    <div style="text-align: center; padding: 20px; background: #f1f5f9; border-radius: 8px;">
                        <h4 style="color: var(--ai-blue); font-size: 2rem;">36</h4>
                        <p>Hours of Reading</p>
                    </div>
                    <div style="text-align: center; padding: 20px; background: #f1f5f9; border-radius: 8px;">
                        <h4 style="color: var(--ai-blue); font-size: 2rem;">4.2</h4>
                        <p>Average Rating Given</p>
                    </div>
                    <div style="text-align: center; padding: 20px; background: #f1f5f9; border-radius: 8px;">
                        <h4 style="color: var(--ai-blue); font-size: 2rem;">78%</h4>
                        <p>Match With AI Recommendations</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- The rest of your existing sections (Ministry, Community, Payment) remain the same -->
    <!-- ... -->

    <!-- AI-enhanced Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3 class="editable" data-id="footer-about">
                        <span class="edit-indicator">✏️</span>
                        About Us
                    </h3>
                    <p class="editable" data-id="footer-about-desc">
                        <span class="edit-indicator">✏️</span>
                        South Africa's first AI-powered ebook store with personalized recommendations and intelligent features.
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
                        <span class="edit-indicator">✏️</span>
                        AI Features
                    </h3>
                    <ul>
                        <li><a href="#ai-features">Smart Recommendations</a></li>
                        <li><a href="#ai-features">Reading Assistant</a></li>
                        <li><a href="#ai-features">Writing Assistant</a></li>
                        <li><a href="#ai-features">Reading Analytics</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3 class="editable" data-id="footer-contact">
                        <span class="edit-indicator">✏️</span>
                        Contact Info
                    </h3>
                    <ul>
                        <li><i class="fas fa-map-marker-alt"></i> <span class="editable" data-id="footer-address">
                            <span class="edit-indicator">✏️</span>
                            123 Book Street, Johannesburg
                        </span></li>
                        <li><i class="fas fa-phone"></i> <span class="editable" data-id="footer-phone">
                            <span class="edit-indicator">✏️</span>
                            +27 11 123 4567
                        </span></li>
                        <li><i class="fas fa-envelope"></i> <span class="editable" data-id="footer-email">
                            <span class="edit-indicator">✏️</span>
                            info@definitiveword.co.za
                        </span></li>
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                <p class="editable" data-id="copyright">
                    <span class="edit-indicator">✏️</span>
                    &copy; 2023 The Definitive Word. Powered by AI. All rights reserved.
                </p>
            </div>
        </div>
    </footer>

    <!-- All your existing modals and context menus remain the same -->
    <!-- ... -->

    <script>
        // AI-specific variables
        let userPreferences = [];
        let aiChatHistory = [];
        let readingAssistantActive = false;

        // Enhanced initialization with AI features
        function initApp() {
            loadAllContent();
            displayBooks();
            setupNavigation();
            setupEditInteractions();
            loadCart();
            loadCommunityData();
            initMinistrySection();
            updateCartDisplay();
            setupInteractiveElements();
            initAIFeatures();
            showNotification('🤖 Welcome to our AI-powered bookstore! Try our intelligent features.');
        }

        // Initialize AI features
        function initAIFeatures() {
            // Load user preferences from localStorage
            const savedPreferences = localStorage.getItem('userPreferences');
            if (savedPreferences) {
                userPreferences = JSON.parse(savedPreferences);
                updatePreferenceUI();
            }
            
            // Load AI chat history
            const savedChat = localStorage.getItem('aiChatHistory');
            if (savedChat) {
                aiChatHistory = JSON.parse(savedChat);
                displayAIChatHistory();
            }
            
            // Generate initial recommendations
            generatePersonalizedRecommendations();
        }

        // Toggle AI chat
        function toggleAIChat() {
            const chatContainer = document.getElementById('aiChatContainer');
            chatContainer.classList.toggle('active');
            
            if (chatContainer.classList.contains('active')) {
                document.getElementById('aiChatInput').focus();
            }
        }

        // Send AI message
        function sendAIMessage() {
            const input = document.getElementById('aiChatInput');
            const message = input.value.trim();
            
            if (!message) return;
            
            // Add user message to chat
            addAIMessage(message, 'user');
            input.value = '';
            
            // Simulate AI response (in a real app, this would call an API)
            setTimeout(() => {
                const response = generateAIResponse(message);
                addAIMessage(response, 'bot');
            }, 1000);
        }

        // Add message to AI chat
        function addAIMessage(message, sender) {
            const chatMessages = document.getElementById('aiChatMessages');
            const messageElement = document.createElement('div');
            messageElement.className = `ai-message ${sender}`;
            messageElement.textContent = message;
            chatMessages.appendChild(messageElement);
            
            // Scroll to bottom
            chatMessages.scrollTop = chatMessages.scrollHeight;
            
            // Save to history
            aiChatHistory.push({ sender, message });
            localStorage.setItem('aiChatHistory', JSON.stringify(aiChatHistory));
        }

        // Display AI chat history
        function displayAIChatHistory() {
            const chatMessages = document.getElementById('aiChatMessages');
            chatMessages.innerHTML = '';
            
            aiChatHistory.forEach(msg => {
                const messageElement = document.createElement('div');
                messageElement.className = `ai-message ${msg.sender}`;
                messageElement.textContent = msg.message;
                chatMessages.appendChild(messageElement);
            });
            
            // Scroll to bottom
            chatMessages.scrollTop = chatMessages.scrollHeight;
        }

        // Generate AI response (simulated)
        function generateAIResponse(userMessage) {
            const lowerMessage = userMessage.toLowerCase();
            
            if (lowerMessage.includes('recommend') || lowerMessage.includes('suggest')) {
                return "Based on your reading history, I'd recommend 'The Path to Spiritual Maturity' and 'Digital Revolution'. Would you like more specific recommendations?";
            } else if (lowerMessage.includes('help') || lowerMessage.includes('assistant')) {
                return "I can help you find books, provide reading assistance, generate writing ideas, and analyze your reading habits. What would you like help with?";
            } else if (lowerMessage.includes('summary') || lowerMessage.includes('summarize')) {
                return "I can provide summaries for any book in our collection. Which book would you like me to summarize?";
            } else if (lowerMessage.includes('writing') || lowerMessage.includes('write')) {
                return "I'd be happy to help with your writing! I can generate ideas, outlines, or even help with specific passages. What are you working on?";
            } else {
                return "I'm here to help with all things related to books and reading. You can ask me for recommendations, writing help, or book summaries. What would you like to know?";
            }
        }

        // Toggle user preference
        function togglePreference(preference) {
            const index = userPreferences.indexOf(preference);
            
            if (index === -1) {
                userPreferences.push(preference);
            } else {
                userPreferences.splice(index, 1);
            }
            
            updatePreferenceUI();
            localStorage.setItem('userPreferences', JSON.stringify(userPreferences));
            
            // Regenerate recommendations if we have preferences
            if (userPreferences.length > 0) {
                generatePersonalizedRecommendations();
            }
        }

        // Update preference UI
        function updatePreferenceUI() {
            document.querySelectorAll('.ai-option').forEach(option => {
                const preference = option.querySelector('p').textContent.toLowerCase().replace('-', '');
                if (userPreferences.includes(preference)) {
                    option.classList.add('active');
                } else {
                    option.classList.remove('active');
                }
            });
        }

        // Generate personalized recommendations
        function generatePersonalizedRecommendations() {
            const recommendationsList = document.getElementById('aiRecommendationsList');
            
            if (userPreferences.length === 0) {
                recommendationsList.innerHTML = '<p>Select your preferences above to get personalized recommendations.</p>';
                return;
            }
            
            // Filter books based on preferences (simulated)
            const allBooks = [...sampleBooks, ...ministryBooks];
            let filteredBooks = allBooks;
            
            // In a real app, this would use more sophisticated matching
            if (userPreferences.includes('spiritual')) {
                filteredBooks = ministryBooks;
            } else if (userPreferences.includes('fiction')) {
                filteredBooks = sampleBooks.filter(book => 
                    book.title === 'The Silent Observer' || 
                    book.title === 'African Skies'
                );
            }
            
            // Limit to 3 recommendations
            const recommendations = filteredBooks.slice(0, 3);
            
            // Display recommendations
            recommendationsList.innerHTML = '';
            recommendations.forEach(book => {
                const recommendationItem = document.createElement('div');
                recommendationItem.className = 'ai-recommendation-item';
                recommendationItem.innerHTML = `
                    <div class="ai-recommendation-cover">
                        <img src="${book.image}" alt="${book.title}">
                    </div>
                    <div class="ai-recommendation-details">
                        <div class="ai-recommendation-title">${book.title}</div>
                        <div class="ai-recommendation-author">by ${book.author}</div>
                        <div class="ai-recommendation-reason">Recommended based on your interest in ${userPreferences.join(', ')}</div>
                    </div>
                `;
                recommendationItem.addEventListener('click', () => {
                    showBookDetails(book);
                });
                recommendationsList.appendChild(recommendationItem);
            });
            
            showNotification('✨ New personalized recommendations generated!');
        }

        // Show book details with AI assistant
        function showBookDetails(book) {
            // In a real app, this would open a detailed view
            // For now, we'll just activate the reading assistant
            activateReadingAssistant(book);
        }

        // Activate reading assistant for a book
        function activateReadingAssistant(book) {
            const assistant = document.getElementById('aiReadingAssistant');
            const content = document.getElementById('aiAssistantContent');
            
            // Generate AI content for the book
            content.innerHTML = `
                <h4>${book.title}</h4>
                <p>by ${book.author}</p>
                
                <div class="ai-summary">
                    <h5>AI Summary</h5>
                    <p>${generateBookSummary(book)}</p>
                </div>
                
                <div class="ai-vocabulary">
                    <h5>Key Concepts</h5>
                    <div class="ai-vocabulary-item">
                        <span>Spiritual Growth</span>
                        <span>⭐️⭐️⭐️⭐️</span>
                    </div>
                    <div class="ai-vocabulary-item">
                        <span>Biblical Principles</span>
                        <span>⭐️⭐️⭐️⭐️⭐️</span>
                    </div>
                    <div class="ai-vocabulary-item">
                        <span>Practical Application</span>
                        <span>⭐️⭐️⭐️⭐️</span>
                    </div>
                </div>
                
                <button class="btn" style="width: 100%; margin-top: 15px; background: var(--ai-gradient);" onclick="addToCart(${book.id})">
                    <i class="fas fa-cart-plus"></i> Add to Cart - R${book.price.toFixed(2)}
                </button>
            `;
            
            assistant.classList.add('active');
            readingAssistantActive = true;
        }

        // Toggle reading assistant
        function toggleReadingAssistant() {
            const assistant = document.getElementById('aiReadingAssistant');
            assistant.classList.remove('active');
            readingAssistantActive = false;
        }

        // Generate book summary (simulated)
        function generateBookSummary(book) {
            if (book.title.includes('Spiritual') || book.title.includes('Prayer') || book.title.includes('Biblical')) {
                return "This book provides a comprehensive exploration of spiritual principles and their practical application in daily life. It offers guidance for those seeking to deepen their faith and understanding of biblical teachings.";
            } else if (book.title.includes('Digital') || book.title.includes('Business')) {
                return "An insightful examination of modern technology trends and their impact on business and society. The author provides practical strategies for navigating the digital landscape successfully.";
            } else {
                return "A compelling narrative that explores complex themes through rich character development and engaging storytelling. This book offers both entertainment and thoughtful reflection.";
            }
        }

        // Generate content with AI
        function generateContent() {
            const prompt = document.getElementById('aiWritingPrompt').value;
            const output = document.getElementById('aiWritingOutput');
            
            if (!prompt) {
                showNotification('Please enter a writing prompt');
                return;
            }
            
            // Show loading state
            output.innerHTML = '<i class="fas fa-spinner fa-spin"></i> AI is generating content...';
            
            // Simulate AI generation
            setTimeout(() => {
                let generatedContent = '';
                
                if (prompt.toLowerCase().includes('outline')) {
                    generatedContent = `
                        <h4>Book Outline: ${prompt}</h4>
                        <ol>
                            <li><strong>Introduction</strong> - Setting the stage and stating the core message</li>
                            <li><strong>Foundation Principles</strong> - Establishing the fundamental concepts</li>
                            <li><strong>Practical Application</strong> - How to implement these principles in daily life</li>
                            <li><strong>Overcoming Challenges</strong> - Addressing common obstacles and solutions</li>
                            <li><strong>Sustaining Growth</strong> - Strategies for long-term development</li>
                            <li><strong>Conclusion</strong> - Final thoughts and next steps</li>
                        </ol>
                        <p>This structure provides a logical flow from theory to practice, helping readers not just understand but implement the concepts.</p>
                    `;
                } else if (prompt.toLowerCase().includes('idea')) {
                    generatedContent = `
                        <h4>Book Ideas Based on Your Interest</h4>
                        <ul>
                            <li><strong>"The Daily Practice"</strong> - A 30-day guide to developing consistent spiritual habits</li>
                            <li><strong>"Faith in Action"</strong> - Stories of people who transformed their communities through faith-based initiatives</li>
                            <li><strong>"The Modern Disciple"</strong> - Navigating faith in a digital, fast-paced world</li>
                            <li><strong>"Questions of Faith"</strong> - Addressing common doubts and strengthening belief through inquiry</li>
                        </ul>
                        <p>These ideas combine timeless spiritual principles with contemporary relevance.</p>
                    `;
                } else {
                    generatedContent = `
                        <h4>AI-Generated Content</h4>
                        <p>Based on your request about "${prompt}", here are some thoughts:</p>
                        <p>The journey of spiritual growth is both personal and universal. While each person's path is unique, there are common principles that guide all seekers toward deeper understanding and connection.</p>
                        <p>Consider exploring the tension between tradition and innovation, or the balance between faith and reason. These themes resonate with contemporary audiences while remaining grounded in timeless wisdom.</p>
                        <p>Remember that the most powerful writing comes from authentic experience paired with thoughtful reflection.</p>
                    `;
                }
                
                output.innerHTML = generatedContent;
                showNotification('✅ AI content generated successfully!');
            }, 2000);
        }

        // Enhanced book display with AI features
        function displayBooks() {
            const booksGrid = document.getElementById('booksGrid');
            booksGrid.innerHTML = '';
            
            sampleBooks.forEach(book => {
                const bookCard = document.createElement('div');
                bookCard.className = 'book-card';
                bookCard.innerHTML = `
                    <div class="book-cover">
                        <img src="${book.image}" alt="${book.title}">
                        ${book.badge ? `<div class="ai-badge" style="position: absolute; top: 10px; right: 10px;">${book.badge}</div>` : ''}
                    </div>
                    <div class="book-info">
                        <h3 class="book-title">${book.title}</h3>
                        <p class="book-author">by ${book.author}</p>
                        <p class="book-description">${book.description}</p>
                        <div class="book-price">
                            <span class="price price-editable">R${book.price.toFixed(2)}</span>
                            <button class="btn" onclick="addToCart(${book.id})">
                                <i class="fas fa-cart-plus"></i> Add to Cart
                            </button>
                        </div>
                        <div class="reading-progress">
                            <div class="reading-progress-bar" style="width: 0%"></div>
                        </div>
                        <button class="btn" style="width: 100%; margin-top: 10px; background: var(--ai-gradient);" onclick="activateReadingAssistant(${JSON.stringify(book).replace(/"/g, '&quot;')})">
                            <i class="fas fa-robot"></i> AI Reading Assistant
                        </button>
                    </div>
                `;
                booksGrid.appendChild(bookCard);
                
                // Add reading simulation
                bookCard.addEventListener('click', function(e) {
                    if (!e.target.closest('.btn')) {
                        simulateReading(this);
                    }
                });
            });
        }

        // The rest of your existing functions remain the same
        // ...
    </script>
</body>
</html>

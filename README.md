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

        /* === SUPER SIMPLE EDIT MODE === */
        .edit-mode {
            background: #1a365d;
            color: white;
            padding: 10px 0;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 10000;
            text-align: center;
        }

        .edit-btn {
            background: #d69e2e;
            color: #1a365d;
            border: none;
            padding: 8px 15px;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            margin: 0 5px;
        }

        .editable {
            position: relative;
            border: 2px dashed transparent;
            transition: all 0.3s ease;
            padding: 5px;
            border-radius: 5px;
        }

        .edit-mode-on .editable {
            border-color: #d69e2e;
            background: rgba(214, 158, 46, 0.1);
        }

        .editable:hover {
            background: rgba(214, 158, 46, 0.2);
        }

        .edit-icon {
            position: absolute;
            top: -10px;
            right: -10px;
            background: #d69e2e;
            color: #1a365d;
            border-radius: 50%;
            width: 25px;
            height: 25px;
            display: none;
            align-items: center;
            justify-content: center;
            font-size: 12px;
            cursor: pointer;
            z-index: 1000;
        }

        .edit-mode-on .edit-icon {
            display: flex;
        }

        /* === HEADER === */
        header {
            background: white;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 45px;
            z-index: 999;
        }

        .header-top {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
        }

        .logo {
            font-size: 2rem;
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
            font-weight: 500;
            padding: 10px 0;
        }

        .nav-main a.active {
            color: #d69e2e;
            border-bottom: 2px solid #d69e2e;
        }

        /* === SECTIONS === */
        .section {
            padding: 60px 0;
            min-height: 60vh;
        }

        .section-title {
            text-align: center;
            margin-bottom: 40px;
            color: #1a365d;
            font-size: 2.5rem;
        }

        /* === HERO === */
        .hero {
            background: linear-gradient(135deg, #1a365d 0%, #2d3748 100%);
            color: white;
            padding: 100px 0;
            text-align: center;
        }

        .btn {
            display: inline-block;
            padding: 12px 25px;
            background: #d69e2e;
            color: #1a365d;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            text-decoration: none;
            margin: 10px;
        }

        /* === ABOUT SECTION === */
        .about-section {
            background: white;
        }

        .about-content {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
        }

        .about-text {
            font-size: 1.1rem;
            line-height: 1.8;
            margin-bottom: 30px;
        }

        .team-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }

        .team-member {
            background: #f7fafc;
            padding: 30px;
            border-radius: 10px;
            text-align: center;
        }

        .team-member img {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            margin-bottom: 20px;
            object-fit: cover;
        }

        /* === SUPPORT SECTION === */
        .support-section {
            background: #f7fafc;
        }

        .support-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .support-category {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .support-category h3 {
            color: #1a365d;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .support-category ul {
            list-style: none;
        }

        .support-category li {
            margin-bottom: 10px;
            padding: 8px 0;
            border-bottom: 1px solid #eee;
        }

        /* === CONTACT === */
        .contact-section {
            background: white;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 50px;
        }

        .contact-info {
            background: #f7fafc;
            padding: 30px;
            border-radius: 10px;
        }

        .contact-item {
            margin-bottom: 20px;
            padding: 15px;
            background: white;
            border-radius: 5px;
        }

        .contact-form {
            background: #f7fafc;
            padding: 30px;
            border-radius: 10px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }

        .form-group input, .form-group textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }

        /* === EDIT MODAL === */
        .edit-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.5);
            z-index: 20000;
            align-items: center;
            justify-content: center;
        }

        .edit-modal.active {
            display: flex;
        }

        .edit-content {
            background: white;
            padding: 30px;
            border-radius: 10px;
            max-width: 500px;
            width: 90%;
        }

        .edit-content h3 {
            margin-bottom: 20px;
            color: #1a365d;
        }

        .edit-content textarea {
            width: 100%;
            height: 150px;
            padding: 15px;
            border: 2px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            margin-bottom: 20px;
        }

        /* === RESPONSIVE === */
        @media (max-width: 768px) {
            .header-top {
                flex-direction: column;
                gap: 15px;
            }
            
            .nav-main {
                gap: 15px;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .section {
                padding: 40px 0;
            }
            
            .section-title {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- SUPER SIMPLE EDIT MODE -->
    <div class="edit-mode">
        <div class="container">
            <strong>🚀 EASY EDIT MODE:</strong>
            <button class="edit-btn" onclick="toggleEditMode()" id="editToggle">
                <i class="fas fa-edit"></i> TURN ON EDITING
            </button>
            <button class="edit-btn" onclick="saveAllContent()">
                <i class="fas fa-save"></i> SAVE EVERYTHING
            </button>
            <button class="edit-btn" onclick="resetToDefault()">
                <i class="fas fa-undo"></i> RESET
            </button>
            <span style="margin-left: 20px; font-size: 0.9em;">Click the ✏️ icons to edit anything!</span>
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
                    <a href="#home" class="active">Home</a>
                    <a href="#about">About Us</a>
                    <a href="#support">Support Center</a>
                    <a href="#contact">Contact</a>
                </nav>
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
                Your premier destination for quality ebooks and exceptional reading experiences
            </p>
            <div>
                <a href="#about" class="btn">Learn About Us</a>
                <a href="#support" class="btn" style="background: transparent; border: 2px solid white; color: white;">Get Support</a>
            </div>
        </div>
    </section>

    <!-- About Us Section -->
    <section id="about" class="section about-section">
        <div class="container">
            <h2 class="section-title editable" data-id="about-title">
                <span class="edit-icon">✏️</span>
                About The Definitive Word
            </h2>
            
            <div class="about-content">
                <div class="about-text editable" data-id="about-text-1">
                    <span class="edit-icon">✏️</span>
                    <p>The Definitive Word was founded with a simple mission: to bring exceptional literature to discerning readers. We believe that great books have the power to transform lives, spark conversations, and shape perspectives.</p>
                </div>
                
                <div class="about-text editable" data-id="about-text-2">
                    <span class="edit-icon">✏️</span>
                    <p>Our team of literary experts carefully curates each title in our collection, ensuring that every book meets our standards for quality writing, compelling storytelling, and lasting impact.</p>
                </div>

                <h3 style="margin: 50px 0 30px; color: #1a365d;" class="editable" data-id="team-title">
                    <span class="edit-icon">✏️</span>
                    Meet Our Team
                </h3>
                
                <div class="team-grid">
                    <div class="team-member">
                        <img src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-4.0.3&auto=format&fit=crop&w=400&q=80" alt="Team Member">
                        <h4 class="editable" data-id="team1-name">
                            <span class="edit-icon">✏️</span>
                            Alex Johnson
                        </h4>
                        <p class="editable" data-id="team1-role">
                            <span class="edit-icon">✏️</span>
                            Founder & CEO
                        </p>
                        <p class="editable" data-id="team1-desc">
                            <span class="edit-icon">✏️</span>
                            Passionate about connecting readers with transformative literature
                        </p>
                    </div>
                    
                    <div class="team-member">
                        <img src="https://images.unsplash.com/photo-1494790108755-2616b612b786?ixlib=rb-4.0.3&auto=format&fit=crop&w=400&q=80" alt="Team Member">
                        <h4 class="editable" data-id="team2-name">
                            <span class="edit-icon">✏️</span>
                            Sarah Chen
                        </h4>
                        <p class="editable" data-id="team2-role">
                            <span class="edit-icon">✏️</span>
                            Head of Content
                        </p>
                        <p class="editable" data-id="team2-desc">
                            <span class="edit-icon">✏️</span>
                            Curating exceptional books for our community
                        </p>
                    </div>
                    
                    <div class="team-member">
                        <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3&auto=format&fit=crop&w=400&q=80" alt="Team Member">
                        <h4 class="editable" data-id="team3-name">
                            <span class="edit-icon">✏️</span>
                            Marcus Rodriguez
                        </h4>
                        <p class="editable" data-id="team3-role">
                            <span class="edit-icon">✏️</span>
                            Customer Support
                        </p>
                        <p class="editable" data-id="team3-desc">
                            <span class="edit-icon">✏️</span>
                            Here to help with any questions or issues
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Support Center Section -->
    <section id="support" class="section support-section">
        <div class="container">
            <h2 class="section-title editable" data-id="support-title">
                <span class="edit-icon">✏️</span>
                Support Center
            </h2>
            <p class="section-subtitle editable" data-id="support-subtitle">
                <span class="edit-icon">✏️</span>
                We're here to help! Find answers to common questions and get support
            </p>
            
            <div class="support-grid">
                <div class="support-category">
                    <h3 class="editable" data-id="support1-title">
                        <span class="edit-icon">✏️</span>
                        <i class="fas fa-shopping-cart"></i> Order Help
                    </h3>
                    <ul>
                        <li class="editable" data-id="support1-item1">
                            <span class="edit-icon">✏️</span>
                            How to purchase ebooks
                        </li>
                        <li class="editable" data-id="support1-item2">
                            <span class="edit-icon">✏️</span>
                            Downloading your books
                        </li>
                        <li class="editable" data-id="support1-item3">
                            <span class="edit-icon">✏️</span>
                            Payment issues
                        </li>
                        <li class="editable" data-id="support1-item4">
                            <span class="edit-icon">✏️</span>
                            Order confirmation
                        </li>
                    </ul>
                </div>
                
                <div class="support-category">
                    <h3 class="editable" data-id="support2-title">
                        <span class="edit-icon">✏️</span>
                        <i class="fas fa-book"></i> Reading Help
                    </h3>
                    <ul>
                        <li class="editable" data-id="support2-item1">
                            <span class="edit-icon">✏️</span>
                            Supported devices
                        </li>
                        <li class="editable" data-id="support2-item2">
                            <span class="edit-icon">✏️</span>
                            Reading app recommendations
                        </li>
                        <li class="editable" data-id="support2-item3">
                            <span class="edit-icon">✏️</span>
                            Format compatibility
                        </li>
                        <li class="editable" data-id="support2-item4">
                            <span class="edit-icon">✏️</span>
                            Transferring between devices
                        </li>
                    </ul>
                </div>
                
                <div class="support-category">
                    <h3 class="editable" data-id="support3-title">
                        <span class="edit-icon">✏️</span>
                        <i class="fas fa-user"></i> Account Help
                    </h3>
                    <ul>
                        <li class="editable" data-id="support3-item1">
                            <span class="edit-icon">✏️</span>
                            Creating an account
                        </li>
                        <li class="editable" data-id="support3-item2">
                            <span class="edit-icon">✏️</span>
                            Password reset
                        </li>
                        <li class="editable" data-id="support3-item3">
                            <span class="edit-icon">✏️</span>
                            Managing your library
                        </li>
                        <li class="editable" data-id="support3-item4">
                            <span class="edit-icon">✏️</span>
                            Privacy and security
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section contact-section">
        <div class="container">
            <h2 class="section-title editable" data-id="contact-title">
                <span class="edit-icon">✏️</span>
                Contact Us
            </h2>
            
            <div class="contact-grid">
                <div class="contact-info">
                    <h3 class="editable" data-id="contact-info-title">
                        <span class="edit-icon">✏️</span>
                        Get In Touch
                    </h3>
                    
                    <div class="contact-item editable" data-id="contact-email">
                        <span class="edit-icon">✏️</span>
                        <strong>Email:</strong> support@thedefinitiveword.com
                    </div>
                    
                    <div class="contact-item editable" data-id="contact-phone">
                        <span class="edit-icon">✏️</span>
                        <strong>Phone:</strong> +1 (555) 123-4567
                    </div>
                    
                    <div class="contact-item editable" data-id="contact-address">
                        <span class="edit-icon">✏️</span>
                        <strong>Address:</strong> 123 Book Street, Literary City, LC 12345
                    </div>
                    
                    <div class="contact-item editable" data-id="contact-hours">
                        <span class="edit-icon">✏️</span>
                        <strong>Hours:</strong> Mon-Fri 9AM-6PM EST
                    </div>
                </div>
                
                <div class="contact-form">
                    <h3 class="editable" data-id="contact-form-title">
                        <span class="edit-icon">✏️</span>
                        Send us a Message
                    </h3>
                    <form onsubmit="handleContactForm(event)">
                        <div class="form-group">
                            <label>Your Name</label>
                            <input type="text" required>
                        </div>
                        <div class="form-group">
                            <label>Email Address</label>
                            <input type="email" required>
                        </div>
                        <div class="form-group">
                            <label>Subject</label>
                            <input type="text" required>
                        </div>
                        <div class="form-group">
                            <label>Message</label>
                            <textarea rows="5" required></textarea>
                        </div>
                        <button type="submit" class="btn" style="width: 100%;">
                            Send Message
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Edit Modal -->
    <div class="edit-modal" id="editModal">
        <div class="edit-content">
            <h3 id="editModalTitle">Edit Content</h3>
            <textarea id="editModalTextarea"></textarea>
            <div style="display: flex; gap: 10px;">
                <button class="btn" onclick="saveEdit()" style="flex: 1;">Save Changes</button>
                <button class="btn" onclick="closeEditModal()" style="flex: 1; background: #666;">Cancel</button>
            </div>
        </div>
    </div>

    <script>
        let currentEditingElement = null;
        let editMode = false;

        // Toggle edit mode on/off
        function toggleEditMode() {
            editMode = !editMode;
            document.body.classList.toggle('edit-mode-on', editMode);
            document.getElementById('editToggle').innerHTML = editMode ? 
                '<i class="fas fa-times"></i> TURN OFF EDITING' : 
                '<i class="fas fa-edit"></i> TURN ON EDITING';
        }

        // Set up click handlers for all editable elements
        document.addEventListener('DOMContentLoaded', function() {
            // Load saved content
            loadAllContent();
            
            // Add click handlers to all edit icons
            document.querySelectorAll('.edit-icon').forEach(icon => {
                icon.addEventListener('click', function(e) {
                    e.stopPropagation();
                    if (editMode) {
                        const editableElement = this.parentElement;
                        openEditModal(editableElement);
                    }
                });
            });

            // Add click handlers to editable areas (for larger click targets)
            document.querySelectorAll('.editable').forEach(element => {
                element.addEventListener('click', function(e) {
                    if (editMode && !e.target.classList.contains('edit-icon')) {
                        openEditModal(this);
                    }
                });
            });

            // Navigation
            document.querySelectorAll('.nav-main a').forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    document.querySelectorAll('.nav-main a').forEach(l => l.classList.remove('active'));
                    this.classList.add('active');
                    
                    const targetId = this.getAttribute('href').substring(1);
                    const targetSection = document.getElementById(targetId);
                    if (targetSection) {
                        window.scrollTo({
                            top: targetSection.offsetTop - 100,
                            behavior: 'smooth'
                        });
                    }
                });
            });
        });

        // Open edit modal
        function openEditModal(element) {
            currentEditingElement = element;
            const currentText = element.textContent.replace('✏️', '').trim();
            document.getElementById('editModalTitle').textContent = 'Edit: ' + element.getAttribute('data-id');
            document.getElementById('editModalTextarea').value = currentText;
            document.getElementById('editModal').classList.add('active');
        }

        // Save edit
        function saveEdit() {
            if (currentEditingElement) {
                const newText = document.getElementById('editModalTextarea').value;
                currentEditingElement.innerHTML = '<span class="edit-icon">✏️</span> ' + newText;
                saveAllContent();
                closeEditModal();
                showNotification('Changes saved!');
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
            if (confirm('Reset all content to original? This cannot be undone.')) {
                localStorage.removeItem('websiteContent');
                location.reload();
            }
        }

        // Handle contact form
        function handleContactForm(event) {
            event.preventDefault();
            showNotification('Thank you! Your message has been sent. We\'ll respond within 24 hours.');
            event.target.reset();
        }

        // Show notification
        function showNotification(message) {
            alert('✅ ' + message); // Simple alert for now
        }

        // Close modal when clicking outside
        window.addEventListener('click', function(event) {
            if (event.target.classList.contains('edit-modal')) {
                closeEditModal();
            }
        });
    </script>
</body>
</html>

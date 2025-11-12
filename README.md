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
            --success: #38a169;
            --light: #f7fafc;
            --dark: #2d3748;
            --text: #2d3748;
            --background: #ffffff;
            --gradient: linear-gradient(135deg, #1a365d 0%, #2d3748 100%);
        }

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
            scroll-behavior: smooth;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        /* === ADMIN PANEL === */
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

        /* === HEADER === */
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

        .nav-main a.active {
            color: var(--secondary);
        }

        .nav-main a.active::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 2px;
            background: var(--secondary);
        }

        /* === SECTIONS === */
        .section {
            padding: 80px 0;
            min-height: 60vh;
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

        /* === HERO SECTION === */
        .hero {
            background: var(--gradient);
            color: white;
            padding: 100px 0;
            text-align: center;
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

        /* === ABOUT SECTION === */
        .about-section {
            background: var(--light);
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
            color: var(--dark);
        }

        .team-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }

        .team-member {
            background: white;
            padding: 30px;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 5px 20px rgba(0,0,0,0.08);
        }

        .team-member img {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            margin-bottom: 20px;
            object-fit: cover;
        }

        /* === CONTACT SECTION === */
        .contact-section {
            background: white;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 50px;
            max-width: 1000px;
            margin: 0 auto;
        }

        .contact-info {
            text-align: center;
        }

        .contact-item {
            margin-bottom: 25px;
            padding: 20px;
            background: var(--light);
            border-radius: 10px;
        }

        .contact-item i {
            font-size: 2rem;
            color: var(--secondary);
            margin-bottom: 15px;
        }

        .contact-form {
            background: var(--light);
            padding: 40px;
            border-radius: 15px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--primary);
        }

        .form-group input, .form-group textarea {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #e2e8f0;
            border-radius: 8px;
            font-size: 1rem;
            transition: all 0.3s ease;
        }

        .form-group input:focus, .form-group textarea:focus {
            outline: none;
            border-color: var(--secondary);
            box-shadow: 0 0 0 3px rgba(214, 158, 46, 0.1);
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
            z-index: 2000;
            align-items: center;
            justify-content: center;
        }

        .edit-modal.active {
            display: flex;
        }

        .edit-content {
            background: white;
            padding: 30px;
            border-radius: 15px;
            max-width: 600px;
            width: 90%;
            max-height: 80vh;
            overflow-y: auto;
        }

        .edit-section {
            margin-bottom: 25px;
            padding: 20px;
            border: 2px dashed #e2e8f0;
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .edit-section:hover {
            border-color: var(--secondary);
            background: rgba(214, 158, 46, 0.05);
        }

        /* === RESPONSIVE === */
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
            
            .section {
                padding: 60px 0;
            }
            
            .section-title {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Notification -->
    <div class="notification" id="notification"></div>

    <!-- Admin Panel -->
    <div class="admin-panel">
        <div class="container">
            <div class="admin-controls">
                <button class="admin-btn" onclick="openEditModal()">
                    <i class="fas fa-edit"></i> Edit Website Content
                </button>
                <button class="admin-btn" onclick="openModal('addBookModal')">
                    <i class="fas fa-plus"></i> Add Book
                </button>
                <button class="admin-btn" onclick="openModal('addBlogModal')">
                    <i class="fas fa-blog"></i> Add Blog
                </button>
            </div>
        </div>
    </div>

    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-top">
                <a href="#" class="logo">
                    <i class="fas fa-crown"></i>
                    The Definitive Word
                </a>
                
                <nav class="nav-main">
                    <a href="#home" class="nav-link active">Home</a>
                    <a href="#books" class="nav-link">Books</a>
                    <a href="#blog" class="nav-link">Blog</a>
                    <a href="#about" class="nav-link">About Us</a>
                    <a href="#contact" class="nav-link">Contact</a>
                </nav>
            </div>
        </div>
    </header>

    <!-- Home Section -->
    <section id="home" class="hero">
        <div class="container">
            <h1 id="hero-title">Premium Ebooks, Curated for Excellence</h1>
            <p id="hero-subtitle">Discover hand-picked literature from acclaimed authors. Your journey to exceptional reading starts here.</p>
            <div class="hero-actions">
                <a href="#books" class="btn">
                    <i class="fas fa-gem"></i>
                    Explore Collection
                </a>
                <a href="#about" class="btn" style="background: transparent; border: 2px solid white; color: white;">
                    <i class="fas fa-users"></i>
                    Learn About Us
                </a>
            </div>
        </div>
    </section>

    <!-- Books Section -->
    <section id="books" class="section">
        <div class="container">
            <h2 class="section-title" id="books-title">Featured Collection</h2>
            <p class="section-subtitle" id="books-subtitle">Discover our hand-picked selection of exceptional reads</p>
            <div class="books-grid" id="booksGrid">
                <!-- Books will be loaded here -->
            </div>
        </div>
    </section>

    <!-- About Us Section -->
    <section id="about" class="section about-section">
        <div class="container">
            <h2 class="section-title" id="about-title">About The Definitive Word</h2>
            <div class="about-content">
                <div class="about-text" id="about-text">
                    <p>The Definitive Word was founded with a simple mission: to bring exceptional literature to discerning readers. We believe that great books have the power to transform lives, spark conversations, and shape perspectives.</p>
                    
                    <p>Our team of literary experts carefully curates each title in our collection, ensuring that every book meets our standards for quality writing, compelling storytelling, and lasting impact. We're passionate about connecting readers with works that inspire, challenge, and entertain.</p>
                    
                    <p>Beyond just selling books, we're building a community of passionate readers who appreciate the art of great writing. Join us on this journey of literary discovery.</p>
                </div>

                <h3 style="margin: 50px 0 30px; color: var(--primary);">Our Team</h3>
                <div class="team-grid">
                    <div class="team-member">
                        <img src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-4.0.3&auto=format&fit=crop&w=400&q=80" alt="Founder">
                        <h4 id="team-member-1-name">Alex Johnson</h4>
                        <p id="team-member-1-role">Founder & Chief Curator</p>
                        <p id="team-member-1-desc">Former publishing executive with 15+ years in the literary world</p>
                    </div>
                    <div class="team-member">
                        <img src="https://images.unsplash.com/photo-1494790108755-2616b612b786?ixlib=rb-4.0.3&auto=format&fit=crop&w=400&q=80" alt="Editor">
                        <h4 id="team-member-2-name">Sarah Chen</h4>
                        <p id="team-member-2-role">Senior Editor</p>
                        <p id="team-member-2-desc">Award-winning editor with a passion for discovering new voices</p>
                    </div>
                    <div class="team-member">
                        <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3&auto=format&fit=crop&w=400&q=80" alt="Community Manager">
                        <h4 id="team-member-3-name">Marcus Rodriguez</h4>
                        <p id="team-member-3-role">Community Manager</p>
                        <p id="team-member-3-desc">Building connections between readers and authors worldwide</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section contact-section">
        <div class="container">
            <h2 class="section-title" id="contact-title">Get In Touch</h2>
            <p class="section-subtitle" id="contact-subtitle">We'd love to hear from you. Reach out with any questions or feedback.</p>
            
            <div class="contact-grid">
                <div class="contact-info">
                    <div class="contact-item">
                        <i class="fas fa-envelope"></i>
                        <h4 id="contact-email-title">Email Us</h4>
                        <p id="contact-email">hello@thedefinitiveword.com</p>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-phone"></i>
                        <h4 id="contact-phone-title">Call Us</h4>
                        <p id="contact-phone">+1 (555) 123-4567</p>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-map-marker-alt"></i>
                        <h4 id="contact-address-title">Visit Us</h4>
                        <p id="contact-address">123 Literary Lane<br>Bookville, BK 12345</p>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-clock"></i>
                        <h4 id="contact-hours-title">Business Hours</h4>
                        <p id="contact-hours">Mon-Fri: 9AM-6PM EST<br>Sat: 10AM-4PM EST</p>
                    </div>
                </div>
                
                <div class="contact-form">
                    <h3 style="margin-bottom: 20px; color: var(--primary);">Send us a Message</h3>
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
                            <i class="fas fa-paper-plane"></i>
                            Send Message
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Edit Content Modal -->
    <div class="edit-modal" id="editModal">
        <div class="edit-content">
            <h2 style="margin-bottom: 30px; color: var(--primary);">Edit Website Content</h2>
            
            <div class="edit-section" onclick="editSection('hero-title', 'Hero Title')">
                <h4>Hero Section Title</h4>
                <p id="hero-title-preview">Premium Ebooks, Curated for Excellence</p>
            </div>
            
            <div class="edit-section" onclick="editSection('hero-subtitle', 'Hero Subtitle')">
                <h4>Hero Section Subtitle</h4>
                <p id="hero-subtitle-preview">Discover hand-picked literature from acclaimed authors...</p>
            </div>
            
            <div class="edit-section" onclick="editSection('about-title', 'About Us Title')">
                <h4>About Us Title</h4>
                <p id="about-title-preview">About The Definitive Word</p>
            </div>
            
            <div class="edit-section" onclick="editSection('about-text', 'About Us Text')">
                <h4>About Us Content</h4>
                <p id="about-text-preview">The Definitive Word was founded with a simple mission...</p>
            </div>
            
            <div class="edit-section" onclick="editTeamMember(1)">
                <h4>Team Member 1</h4>
                <p id="team-1-preview">Alex Johnson - Founder & Chief Curator</p>
            </div>
            
            <div class="edit-section" onclick="editTeamMember(2)">
                <h4>Team Member 2</h4>
                <p id="team-2-preview">Sarah Chen - Senior Editor</p>
            </div>
            
            <div class="edit-section" onclick="editTeamMember(3)">
                <h4>Team Member 3</h4>
                <p id="team-3-preview">Marcus Rodriguez - Community Manager</p>
            </div>
            
            <div class="edit-section" onclick="editContactInfo()">
                <h4>Contact Information</h4>
                <p>Email, Phone, Address, and Business Hours</p>
            </div>
            
            <button class="btn" onclick="closeEditModal()" style="width: 100%; margin-top: 20px; background: #666;">
                Close Editor
            </button>
        </div>
    </div>

    <script>
        // Navigation functionality
        document.querySelectorAll('.nav-link').forEach(link => {
            link.addEventListener('click', function(e) {
                e.preventDefault();
                
                // Remove active class from all links
                document.querySelectorAll('.nav-link').forEach(l => l.classList.remove('active'));
                
                // Add active class to clicked link
                this.classList.add('active');
                
                // Scroll to section
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

        // Update active nav link on scroll
        window.addEventListener('scroll', function() {
            const sections = document.querySelectorAll('.section, .hero');
            const navLinks = document.querySelectorAll('.nav-link');
            
            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                if (scrollY >= (sectionTop - 150)) {
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

        // Edit Modal Functions
        function openEditModal() {
            document.getElementById('editModal').classList.add('active');
            updateEditPreview();
        }

        function closeEditModal() {
            document.getElementById('editModal').classList.remove('active');
        }

        function updateEditPreview() {
            // Update preview text in edit modal
            document.getElementById('hero-title-preview').textContent = document.getElementById('hero-title').textContent;
            document.getElementById('hero-subtitle-preview').textContent = document.getElementById('hero-subtitle').textContent.substring(0, 50) + '...';
            document.getElementById('about-title-preview').textContent = document.getElementById('about-title').textContent;
            document.getElementById('about-text-preview').textContent = document.getElementById('about-text').textContent.substring(0, 50) + '...';
            document.getElementById('team-1-preview').textContent = document.getElementById('team-member-1-name').textContent + ' - ' + document.getElementById('team-member-1-role').textContent;
            document.getElementById('team-2-preview').textContent = document.getElementById('team-member-2-name').textContent + ' - ' + document.getElementById('team-member-2-role').textContent;
            document.getElementById('team-3-preview').textContent = document.getElementById('team-member-3-name').textContent + ' - ' + document.getElementById('team-member-3-role').textContent;
        }

        function editSection(elementId, label) {
            const currentText = document.getElementById(elementId).textContent;
            const newText = prompt(`${label}:\n\nEdit the text below:`, currentText);
            
            if (newText !== null && newText.trim() !== '') {
                document.getElementById(elementId).textContent = newText;
                updateEditPreview();
                showNotification(`${label} updated successfully!`);
                saveContentToStorage();
            }
        }

        function editTeamMember(memberNumber) {
            const name = prompt(`Team Member ${memberNumber} Name:`, document.getElementById(`team-member-${memberNumber}-name`).textContent);
            const role = prompt(`Team Member ${memberNumber} Role:`, document.getElementById(`team-member-${memberNumber}-role`).textContent);
            const desc = prompt(`Team Member ${memberNumber} Description:`, document.getElementById(`team-member-${memberNumber}-desc`).textContent);
            
            if (name && role && desc) {
                document.getElementById(`team-member-${memberNumber}-name`).textContent = name;
                document.getElementById(`team-member-${memberNumber}-role`).textContent = role;
                document.getElementById(`team-member-${memberNumber}-desc`).textContent = desc;
                updateEditPreview();
                showNotification(`Team member ${memberNumber} updated!`);
                saveContentToStorage();
            }
        }

        function editContactInfo() {
            const email = prompt('Contact Email:', document.getElementById('contact-email').textContent);
            const phone = prompt('Contact Phone:', document.getElementById('contact-phone').textContent);
            const address = prompt('Contact Address (use \\n for line breaks):', document.getElementById('contact-address').textContent.replace(/<br>/g, '\n'));
            const hours = prompt('Business Hours (use \\n for line breaks):', document.getElementById('contact-hours').textContent.replace(/<br>/g, '\n'));
            
            if (email) document.getElementById('contact-email').textContent = email;
            if (phone) document.getElementById('contact-phone').textContent = phone;
            if (address) document.getElementById('contact-address').innerHTML = address.replace(/\n/g, '<br>');
            if (hours) document.getElementById('contact-hours').innerHTML = hours.replace(/\n/g, '<br>');
            
            showNotification('Contact information updated!');
            saveContentToStorage();
        }

        function handleContactForm(event) {
            event.preventDefault();
            showNotification('Thank you for your message! We\'ll get back to you within 24 hours.');
            event.target.reset();
        }

        function showNotification(message) {
            const notification = document.getElementById('notification');
            notification.textContent = message;
            notification.style.background = '#38a169';
            notification.className = 'notification show';
            setTimeout(() => notification.className = 'notification', 4000);
        }

        // Save content to localStorage
        function saveContentToStorage() {
            const content = {
                heroTitle: document.getElementById('hero-title').textContent,
                heroSubtitle: document.getElementById('hero-subtitle').textContent,
                aboutTitle: document.getElementById('about-title').textContent,
                aboutText: document.getElementById('about-text').innerHTML,
                teamMembers: {
                    1: {
                        name: document.getElementById('team-member-1-name').textContent,
                        role: document.getElementById('team-member-1-role').textContent,
                        desc: document.getElementById('team-member-1-desc').textContent
                    },
                    2: {
                        name: document.getElementById('team-member-2-name').textContent,
                        role: document.getElementById('team-member-2-role').textContent,
                        desc: document.getElementById('team-member-2-desc').textContent
                    },
                    3: {
                        name: document.getElementById('team-member-3-name').textContent,
                        role: document.getElementById('team-member-3-role').textContent,
                        desc: document.getElementById('team-member-3-desc').textContent
                    }
                },
                contact: {
                    email: document.getElementById('contact-email').textContent,
                    phone: document.getElementById('contact-phone').textContent,
                    address: document.getElementById('contact-address').innerHTML,
                    hours: document.getElementById('contact-hours').innerHTML
                }
            };
            localStorage.setItem('websiteContent', JSON.stringify(content));
        }

        // Load content from localStorage
        function loadContentFromStorage() {
            const saved = localStorage.getItem('websiteContent');
            if (saved) {
                const content = JSON.parse(saved);
                
                document.getElementById('hero-title').textContent = content.heroTitle;
                document.getElementById('hero-subtitle').textContent = content.heroSubtitle;
                document.getElementById('about-title').textContent = content.aboutTitle;
                document.getElementById('about-text').innerHTML = content.aboutText;
                
                // Team members
                for (let i = 1; i <= 3; i++) {
                    if (content.teamMembers[i]) {
                        document.getElementById(`team-member-${i}-name`).textContent = content.teamMembers[i].name;
                        document.getElementById(`team-member-${i}-role`).textContent = content.teamMembers[i].role;
                        document.getElementById(`team-member-${i}-desc`).textContent = content.teamMembers[i].desc;
                    }
                }
                
                // Contact info
                if (content.contact) {
                    document.getElementById('contact-email').textContent = content.contact.email;
                    document.getElementById('contact-phone').textContent = content.contact.phone;
                    document.getElementById('contact-address').innerHTML = content.contact.address;
                    document.getElementById('contact-hours').innerHTML = content.contact.hours;
                }
            }
        }

        // Initialize
        document.addEventListener('DOMContentLoaded', function() {
            loadContentFromStorage();
            showNotification('Welcome! Click "Edit Website Content" to customize your site.');
        });

        // Close edit modal when clicking outside
        window.addEventListener('click', function(event) {
            if (event.target.classList.contains('edit-modal')) {
                closeEditModal();
            }
        });
    </script>
</body>
</html>

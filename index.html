<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Definitive Word - Ebook Store</title>
    <script src="https://unpkg.com/react@18/umd/react.development.js"></script>
    <script src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f9fafb;
            line-height: 1.6;
        }

        .app {
            min-height: 100vh;
        }

        /* Navigation */
        nav {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .nav-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 80px;
        }

        .logo {
            display: flex;
            align-items: center;
            cursor: pointer;
        }

        .logo-icon {
            font-size: 2rem;
            margin-right: 12px;
        }

        .logo-text h1 {
            font-size: 1.5rem;
            font-weight: bold;
            color: #1f2937;
        }

        .logo-text .tagline {
            font-size: 0.8rem;
            color: #dc2626;
            font-style: italic;
        }

        .nav-links {
            display: none;
            gap: 2rem;
        }

        @media (min-width: 768px) {
            .nav-links {
                display: flex;
            }
        }

        .nav-link {
            color: #374151;
            font-weight: 500;
            background: none;
            border: none;
            cursor: pointer;
            font-size: 1rem;
            transition: color 0.3s;
        }

        .nav-link:hover {
            color: #1d4ed8;
        }

        .nav-actions {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .cart-button {
            position: relative;
            background: none;
            border: none;
            cursor: pointer;
            font-size: 1.5rem;
        }

        .cart-count {
            position: absolute;
            top: -8px;
            right: -8px;
            background-color: #dc2626;
            color: white;
            font-size: 0.8rem;
            border-radius: 50%;
            width: 20px;
            height: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .user-section {
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .mobile-menu-button {
            background: none;
            border: none;
            cursor: pointer;
            font-size: 1.5rem;
        }

        @media (min-width: 768px) {
            .mobile-menu-button {
                display: none;
            }
        }

        .mobile-menu {
            background-color: white;
            border-top: 1px solid #e5e7eb;
            padding: 1rem;
        }

        .mobile-menu-link {
            display: block;
            width: 100%;
            text-align: left;
            color: #374151;
            background: none;
            border: none;
            cursor: pointer;
            padding: 0.5rem 0;
            font-size: 1rem;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #1d4ed8, #1e40af);
            color: white;
            padding: 6rem 1rem;
            text-align: center;
        }

        .hero h1 {
            font-size: 3rem;
            font-weight: bold;
            margin-bottom: 1rem;
        }

        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
        }

        .hero-tagline {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
            color: #fecaca;
            font-style: italic;
            font-weight: 600;
        }

        .hero-subtitle {
            font-size: 1.25rem;
            margin-bottom: 2rem;
        }

        .hero-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 0.75rem 2rem;
            border-radius: 8px;
            font-weight: bold;
            border: none;
            cursor: pointer;
            font-size: 1rem;
            transition: all 0.3s;
        }

        .btn-primary {
            background-color: #dc2626;
            color: white;
        }

        .btn-primary:hover {
            background-color: #b91c1c;
        }

        .btn-secondary {
            background-color: white;
            color: #1d4ed8;
        }

        .btn-secondary:hover {
            background-color: #f3f4f6;
        }

        /* Features Grid */
        .features {
            max-width: 1200px;
            margin: 0 auto;
            padding: 4rem 1rem;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 4rem;
        }

        .feature-card {
            text-align: center;
            padding: 2rem;
            border: 2px solid;
            border-radius: 8px;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }

        .feature-card.blue {
            border-color: #1d4ed8;
        }

        .feature-card.red {
            border-color: #dc2626;
        }

        .feature-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .feature-title {
            font-size: 1.25rem;
            font-weight: bold;
            margin-bottom: 0.5rem;
            color: #1f2937;
        }

        .feature-desc {
            color: #6b7280;
        }

        /* Featured Books */
        .featured-books {
            background: linear-gradient(to right, #dbeafe, #fecaca);
            padding: 3rem 1rem;
            border-radius: 12px;
        }

        .section-title {
            font-size: 2rem;
            font-weight: bold;
            text-align: center;
            margin-bottom: 2rem;
            color: #1f2937;
        }

        .books-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.5rem;
        }

        .book-card {
            background-color: white;
            padding: 1.5rem;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .book-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
        }

        .book-icon {
            font-size: 4rem;
            text-align: center;
            margin-bottom: 1rem;
        }

        .book-title {
            font-weight: bold;
            font-size: 1.125rem;
            margin-bottom: 0.5rem;
            color: #1f2937;
        }

        .book-desc {
            color: #6b7280;
            font-size: 0.875rem;
            margin-bottom: 1rem;
        }

        .book-price {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .price {
            font-size: 1.5rem;
            font-weight: bold;
            color: #1d4ed8;
        }

        /* Store Page */
        .store-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem 1rem;
        }

        .page-title {
            font-size: 2.5rem;
            font-weight: bold;
            margin-bottom: 0.5rem;
            color: #1f2937;
        }

        .page-subtitle {
            color: #6b7280;
            margin-bottom: 2rem;
        }

        .search-container {
            position: relative;
            margin-bottom: 2rem;
        }

        .search-icon {
            position: absolute;
            left: 12px;
            top: 50%;
            transform: translateY(-50%);
            font-size: 1.2rem;
            color: #6b7280;
        }

        .search-input {
            width: 100%;
            padding: 12px 12px 12px 40px;
            border: 2px solid #d1d5db;
            border-radius: 8px;
            font-size: 1rem;
            outline: none;
            transition: border-color 0.3s;
        }

        .search-input:focus {
            border-color: #1d4ed8;
        }

        /* Workshop Cards */
        .workshops-list {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }

        .workshop-card {
            background-color: white;
            border: 2px solid #1d4ed8;
            border-radius: 8px;
            padding: 1.5rem;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .workshop-card:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.1);
        }

        .workshop-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 1rem;
        }

        .workshop-info {
            flex: 1;
        }

        .workshop-title {
            font-size: 1.5rem;
            font-weight: bold;
            margin-bottom: 0.5rem;
            color: #1f2937;
        }

        .workshop-meta {
            color: #6b7280;
            margin-bottom: 1rem;
        }

        .workshop-price {
            text-align: right;
            margin-left: 1.5rem;
        }

        .price-large {
            font-size: 1.875rem;
            font-weight: bold;
            color: #1d4ed8;
            margin-bottom: 1rem;
        }

        /* Blog Cards */
        .blog-container {
            max-width: 800px;
            margin: 0 auto;
            padding: 2rem 1rem;
        }

        .blog-list {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }

        .blog-card {
            background-color: white;
            border-left: 4px solid #1d4ed8;
            padding: 1.5rem;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            cursor: pointer;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .blog-card:hover {
            transform: translateX(5px);
            box-shadow: 0 6px 15px rgba(0,0,0,0.15);
        }

        .blog-title {
            font-size: 1.5rem;
            font-weight: bold;
            margin-bottom: 0.5rem;
            color: #1f2937;
        }

        .blog-meta {
            font-size: 0.875rem;
            color: #6b7280;
            margin-bottom: 0.5rem;
        }

        .blog-excerpt {
            color: #374151;
            margin-bottom: 1rem;
        }

        .read-more {
            color: #dc2626;
            font-weight: 600;
            background: none;
            border: none;
            cursor: pointer;
        }

        /* Modal */
        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: rgba(0,0,0,0.5);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 1000;
            padding: 1rem;
        }

        .modal {
            background-color: white;
            padding: 2rem;
            border-radius: 8px;
            width: 90%;
            max-width: 400px;
            position: relative;
            max-height: 80vh;
            overflow: auto;
        }

        .modal-close {
            position: absolute;
            top: 1rem;
            right: 1rem;
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: #6b7280;
        }

        .modal-title {
            font-size: 1.5rem;
            font-weight: bold;
            margin-bottom: 1rem;
        }

        .error-message {
            background-color: #fee2e2;
            border: 1px solid #ef4444;
            color: #dc2626;
            padding: 0.75rem;
            border-radius: 4px;
            margin-bottom: 1rem;
        }

        .form-group {
            margin-bottom: 1rem;
        }

        .form-label {
            display: block;
            font-weight: bold;
            margin-bottom: 0.5rem;
            color: #1f2937;
        }

        .form-input {
            width: 100%;
            padding: 0.5rem;
            border: 1px solid #d1d5db;
            border-radius: 4px;
            font-size: 1rem;
        }

        .form-input:focus {
            outline: none;
            border-color: #1d4ed8;
        }

        .form-footer {
            text-align: center;
            margin-top: 1rem;
        }

        .form-link {
            background: none;
            border: none;
            color: #1d4ed8;
            cursor: pointer;
            text-decoration: underline;
        }

        /* Cart */
        .cart-container {
            max-width: 800px;
            margin: 0 auto;
            padding: 2rem 1rem;
        }

        .cart-empty {
            text-align: center;
            padding: 4rem;
        }

        .cart-empty-icon {
            font-size: 4rem;
            margin-bottom: 1rem;
        }

        .cart-items {
            display: flex;
            flex-direction: column;
            gap: 1rem;
            margin-bottom: 2rem;
        }

        .cart-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background-color: white;
            padding: 1rem;
            border-radius: 8px;
            border: 2px solid #e5e7eb;
        }

        .cart-item-info {
            display: flex;
            align-items: center;
        }

        .cart-item-icon {
            font-size: 2.5rem;
            margin-right: 1rem;
        }

        .cart-item-details h3 {
            font-weight: bold;
            color: #1f2937;
        }

        .cart-item-details p {
            font-size: 0.875rem;
            color: #6b7280;
        }

        .cart-item-actions {
            display: flex;
            align-items: center;
            gap: 1.5rem;
        }

        .cart-total {
            background: linear-gradient(to right, #dbeafe, #fecaca);
            padding: 1.5rem;
            border-radius: 8px;
        }

        .total-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.5rem;
        }

        .total-label {
            font-size: 1.5rem;
            font-weight: bold;
            color: #1f2937;
        }

        .total-amount {
            font-size: 2rem;
            font-weight: bold;
            color: #1d4ed8;
        }

        .checkout-btn {
            width: 100%;
            background-color: #dc2626;
            color: white;
            font-weight: bold;
            padding: 1rem;
            border-radius: 8px;
            border: none;
            cursor: pointer;
            font-size: 1.125rem;
            transition: background-color 0.3s;
        }

        .checkout-btn:hover:not(:disabled) {
            background-color: #b91c1c;
        }

        .checkout-btn:disabled {
            background-color: #9ca3af;
            cursor: not-allowed;
        }

        .secure-text {
            text-align: center;
            font-size: 0.875rem;
            color: #6b7280;
            margin-top: 0.5rem;
        }

        /* Footer */
        footer {
            background: linear-gradient(135deg, #1e40af, #1d4ed8);
            color: white;
            padding: 2rem 1rem;
            margin-top: 4rem;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            text-align: center;
        }

        .footer-title {
            font-size: 1.5rem;
            font-weight: bold;
            margin-bottom: 0.5rem;
        }

        .footer-tagline {
            color: #fecaca;
            font-style: italic;
            margin-bottom: 1rem;
        }

        .footer-copyright {
            font-size: 0.875rem;
        }

        /* Utility Classes */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1rem;
        }

        .text-center {
            text-align: center;
        }

        .hidden {
            display: none;
        }

        @media (min-width: 768px) {
            .md\\:flex {
                display: flex;
            }
        }
    </style>
</head>
<body>
    <div id="root"></div>

    <script type="text/babel">
        const { useState, useEffect } = React;

        // Mock backend data
        const mockBackend = {
            users: [
                { id: 1, name: 'John Doe', email: 'john@example.com', password: 'password123' }
            ],
            ebooks: [
                { 
                    id: 1, 
                    title: "Walking in Divine Purpose", 
                    price: 19.99, 
                    category: "Ministry", 
                    image: "📖", 
                    description: "Discover your calling and walk in your God-given destiny.",
                    author: "Dr. Michael Johnson",
                    isFeatured: true
                },
                { 
                    id: 2, 
                    title: "Prophetic Insights Vol 1", 
                    price: 24.99, 
                    category: "Prophecy", 
                    image: "✨", 
                    description: "Unlock the mysteries of prophetic revelation.",
                    author: "Sarah Williams",
                    isFeatured: true
                },
                { 
                    id: 3, 
                    title: "Leadership in the Kingdom", 
                    price: 29.99, 
                    category: "Training", 
                    image: "👑", 
                    description: "Biblical principles for effective spiritual leadership.",
                    author: "Pastor James Miller",
                    isFeatured: true
                },
                { 
                    id: 4, 
                    title: "Prayer Warrior's Guide", 
                    price: 14.99, 
                    category: "Ministry", 
                    image: "🙏", 
                    description: "Transform your prayer life and see breakthrough.",
                    author: "Rebecca Thompson",
                    isFeatured: false
                }
            ],
            workshops: [
                { 
                    id: 1, 
                    title: "Prophetic Activation Workshop", 
                    date: "Dec 5, 2025", 
                    price: 49.99,
                    description: "Learn to hear God's voice and operate in prophetic gifts.",
                    instructor: "Sarah Williams",
                    duration: "3 hours"
                }
            ],
            blogs: [
                { 
                    id: 1,
                    title: "5 Keys to Hearing God's Voice", 
                    date: "Nov 20, 2025", 
                    excerpt: "Learn practical steps to discern divine direction in your daily life...",
                    content: "In this comprehensive guide, we explore five essential keys to developing your ability to hear God's voice clearly...",
                    author: "Sarah Williams",
                    category: "Spiritual Growth",
                    readTime: "5 min read"
                }
            ]
        };

        function EbookStore() {
            const [cart, setCart] = useState([]);
            const [currentPage, setCurrentPage] = useState('home');
            const [mobileMenuOpen, setMobileMenuOpen] = useState(false);
            const [user, setUser] = useState(null);
            const [loginModalOpen, setLoginModalOpen] = useState(false);
            const [isLogin, setIsLogin] = useState(true);
            const [loading, setLoading] = useState(false);
            const [searchQuery, setSearchQuery] = useState('');
            const [activeBlog, setActiveBlog] = useState(null);
            const [formData, setFormData] = useState({ name: '', email: '', password: '' });
            const [loginError, setLoginError] = useState('');

            // Load user from localStorage
            useEffect(() => {
                const savedUser = localStorage.getItem('ebookStoreUser');
                if (savedUser) {
                    setUser(JSON.parse(savedUser));
                }
            }, []);

            const handleLogin = async (e) => {
                if (e) e.preventDefault();
                setLoading(true);
                setLoginError('');

                // Simulate API call
                setTimeout(() => {
                    if (isLogin) {
                        const user = mockBackend.users.find(u => u.email === formData.email && u.password === formData.password);
                        if (user) {
                            const { password, ...userWithoutPassword } = user;
                            setUser(userWithoutPassword);
                            localStorage.setItem('ebookStoreUser', JSON.stringify(userWithoutPassword));
                            setLoginModalOpen(false);
                            setFormData({ name: '', email: '', password: '' });
                        } else {
                            setLoginError('Invalid email or password');
                        }
                    } else {
                        // Registration
                        const newUser = { 
                            id: mockBackend.users.length + 1, 
                            name: formData.name, 
                            email: formData.email, 
                            password: formData.password 
                        };
                        mockBackend.users.push(newUser);
                        const { password, ...userWithoutPassword } = newUser;
                        setUser(userWithoutPassword);
                        localStorage.setItem('ebookStoreUser', JSON.stringify(userWithoutPassword));
                        setLoginModalOpen(false);
                        setFormData({ name: '', email: '', password: '' });
                    }
                    setLoading(false);
                }, 1000);
            };

            const handleLogout = () => {
                setUser(null);
                localStorage.removeItem('ebookStoreUser');
                setCart([]);
            };

            const addToCart = (product) => {
                setCart([...cart, { ...product, cartId: Date.now() }]);
            };

            const removeFromCart = (cartId) => {
                setCart(cart.filter(item => item.cartId !== cartId));
            };

            const getTotal = () => {
                return cart.reduce((sum, item) => sum + item.price, 0).toFixed(2);
            };

            const handleCheckout = async () => {
                if (!user) {
                    setLoginModalOpen(true);
                    return;
                }

                setLoading(true);
                setTimeout(() => {
                    alert(`Payment successful! Thank you for your purchase.`);
                    setCart([]);
                    setCurrentPage('home');
                    setLoading(false);
                }, 2000);
            };

            const filteredEbooks = mockBackend.ebooks.filter(ebook =>
                ebook.title.toLowerCase().includes(searchQuery.toLowerCase()) ||
                ebook.author.toLowerCase().includes(searchQuery.toLowerCase()) ||
                ebook.description.toLowerCase().includes(searchQuery.toLowerCase())
            );

            const featuredEbooks = mockBackend.ebooks.filter(ebook => ebook.isFeatured);

            // Login Modal Component
            const LoginModal = () => {
                if (!loginModalOpen) return null;

                return React.createElement('div', { className: 'modal-overlay' },
                    React.createElement('div', { className: 'modal' },
                        React.createElement('button', {
                            className: 'modal-close',
                            onClick: () => setLoginModalOpen(false)
                        }, '×'),
                        React.createElement('h2', { className: 'modal-title' }, isLogin ? 'Login' : 'Register'),
                        
                        loginError && React.createElement('div', { className: 'error-message' }, loginError),
                        
                        React.createElement('form', { onSubmit: handleLogin },
                            !isLogin && React.createElement('div', { className: 'form-group' },
                                React.createElement('label', { className: 'form-label' }, 'Name'),
                                React.createElement('input', {
                                    type: 'text',
                                    className: 'form-input',
                                    value: formData.name,
                                    onChange: (e) => setFormData({...formData, name: e.target.value}),
                                    required: true
                                })
                            ),
                            
                            React.createElement('div', { className: 'form-group' },
                                React.createElement('label', { className: 'form-label' }, 'Email'),
                                React.createElement('input', {
                                    type: 'email',
                                    className: 'form-input',
                                    value: formData.email,
                                    onChange: (e) => setFormData({...formData, email: e.target.value}),
                                    required: true
                                })
                            ),
                            
                            React.createElement('div', { className: 'form-group' },
                                React.createElement('label', { className: 'form-label' }, 'Password'),
                                React.createElement('input', {
                                    type: 'password',
                                    className: 'form-input',
                                    value: formData.password,
                                    onChange: (e) => setFormData({...formData, password: e.target.value}),
                                    required: true
                                })
                            ),
                            
                            React.createElement('button', {
                                type: 'submit',
                                className: 'checkout-btn',
                                disabled: loading
                            }, loading ? 'Processing...' : (isLogin ? 'Login' : 'Register'))
                        ),
                        
                        React.createElement('div', { className: 'form-footer' },
                            React.createElement('button', {
                                className: 'form-link',
                                onClick: () => {
                                    setIsLogin(!isLogin);
                                    setLoginError('');
                                    setFormData({ name: '', email: '', password: '' });
                                }
                            }, isLogin ? 'Need an account? Register' : 'Have an account? Login')
                        )
                    )
                );
            };

            // Navigation Component
            const NavBar = () => {
                return React.createElement('nav', null,
                    React.createElement('div', { className: 'nav-container' },
                        React.createElement('div', { className: 'nav-content' },
                            React.createElement('div', {
                                className: 'logo',
                                onClick: () => setCurrentPage('home')
                            },
                                React.createElement('div', { className: 'logo-icon' }, '📚'),
                                React.createElement('div', { className: 'logo-text' },
                                    React.createElement('h1', null, 'The Definitive Word'),
                                    React.createElement('div', { className: 'tagline' }, 'Your Destiny Has Been Written')
                                )
                            ),
                            
                            React.createElement('div', { className: 'nav-links' },
                                ['home', 'store', 'workshops', 'blog', 'about'].map((page) =>
                                    React.createElement('button', {
                                        key: page,
                                        className: 'nav-link',
                                        onClick: () => setCurrentPage(page)
                                    }, page.charAt(0).toUpperCase() + page.slice(1))
                                )
                            ),
                            
                            React.createElement('div', { className: 'nav-actions' },
                                React.createElement('button', {
                                    className: 'cart-button',
                                    onClick: () => setCurrentPage('cart')
                                },
                                    '🛒',
                                    cart.length > 0 && React.createElement('span', { className: 'cart-count' }, cart.length)
                                ),
                                
                                user ? React.createElement('div', { className: 'user-section' },
                                    React.createElement('span', null, `Hello, ${user.name}`),
                                    React.createElement('button', {
                                        className: 'nav-link',
                                        onClick: handleLogout
                                    }, 'Logout')
                                ) : React.createElement('button', {
                                    className: 'nav-link',
                                    onClick: () => setLoginModalOpen(true)
                                }, 'Login'),
                                
                                React.createElement('button', {
                                    className: 'mobile-menu-button',
                                    onClick: () => setMobileMenuOpen(!mobileMenuOpen)
                                }, mobileMenuOpen ? '✕' : '☰')
                            )
                        ),
                        
                        mobileMenuOpen && React.createElement('div', { className: 'mobile-menu' },
                            ['home', 'store', 'workshops', 'blog', 'about'].map((page) =>
                                React.createElement('button', {
                                    key: page,
                                    className: 'mobile-menu-link',
                                    onClick: () => {
                                        setCurrentPage(page);
                                        setMobileMenuOpen(false);
                                    }
                                }, page.charAt(0).toUpperCase() + page.slice(1))
                            )
                        )
                    )
                );
            };

            // Page Components
            const HomePage = () => {
                return React.createElement('div', null,
                    React.createElement('section', { className: 'hero' },
                        React.createElement('h1', null, 'The Definitive Word'),
                        React.createElement('div', { className: 'hero-tagline' }, 'Your Destiny Has Been Written'),
                        React.createElement('p', { className: 'hero-subtitle' }, 'Empowering believers through prophetic wisdom and biblical teaching'),
                        React.createElement('div', { className: 'hero-buttons' },
                            React.createElement('button', {
                                className: 'btn btn-primary',
                                onClick: () => setCurrentPage('store')
                            }, 'Browse Store'),
                            React.createElement('button', {
                                className: 'btn btn-secondary',
                                onClick: () => setCurrentPage('workshops')
                            }, 'View Workshops')
                        )
                    ),
                    
                    React.createElement('section', { className: 'features' },
                        React.createElement('div', { className: 'features-grid' },
                            React.createElement('div', { className: 'feature-card blue' },
                                React.createElement('div', { className: 'feature-icon' }, '📖'),
                                React.createElement('h3', { className: 'feature-title' }, 'Digital Books'),
                                React.createElement('p', { className: 'feature-desc' }, 'Access transformative teaching instantly')
                            ),
                            React.createElement('div', { className: 'feature-card red' },
                                React.createElement('div', { className: 'feature-icon' }, '🏆'),
                                React.createElement('h3', { className: 'feature-title' }, 'Training & Workshops'),
                                React.createElement('p', { className: 'feature-desc' }, 'Equip yourself for ministry excellence')
                            ),
                            React.createElement('div', { className: 'feature-card blue' },
                                React.createElement('div', { className: 'feature-icon' }, '📅'),
                                React.createElement('h3', { className: 'feature-title' }, 'Ministry Resources'),
                                React.createElement('p', { className: 'feature-desc' }, 'Tools to strengthen your calling')
                            )
                        ),
                        
                        React.createElement('div', { className: 'featured-books' },
                            React.createElement('h2', { className: 'section-title' }, 'Featured Books'),
                            React.createElement('div', { className: 'books-grid' },
                                featuredEbooks.map(book =>
                                    React.createElement('div', { key: book.id, className: 'book-card' },
                                        React.createElement('div', { className: 'book-icon' }, book.image),
                                        React.createElement('h3', { className: 'book-title' }, book.title),
                                        React.createElement('p', { className: 'book-desc' }, book.description),
                                        React.createElement('div', { className: 'book-price' },
                                            React.createElement('span', { className: 'price' }, `$${book.price}`),
                                            React.createElement('button', {
                                                className: 'btn btn-primary',
                                                onClick: () => addToCart(book)
                                            }, 'Add to Cart')
                                        )
                                    )
                                )
                            )
                        )
                    )
                );
            };

            const StorePage = () => {
                return React.createElement('div', { className: 'store-container' },
                    React.createElement('div', null,
                        React.createElement('h1', { className: 'page-title' }, 'Ebook Store'),
                        React.createElement('p', { className: 'page-subtitle' }, 'Transform your life with prophetic wisdom and biblical teaching')
                    ),
                    
                    React.createElement('div', { className: 'search-container' },
                        React.createElement('div', { className: 'search-icon' }, '🔍'),
                        React.createElement('input', {
                            type: 'text',
                            className: 'search-input',
                            placeholder: 'Search books...',
                            value: searchQuery,
                            onChange: (e) => setSearchQuery(e.target.value)
                        })
                    ),
                    
                    React.createElement('div', { className: 'books-grid' },
                        filteredEbooks.map(book =>
                            React.createElement('div', { key: book.id, className: 'book-card' },
                                React.createElement('div', { className: 'book-icon' }, book.image),
                                React.createElement('div', { style: {color: '#dc2626', fontSize: '0.8rem', fontWeight: '600', marginBottom: '0.5rem'} }, book.category),
                                React.createElement('h3', { className: 'book-title' }, book.title),
                                React.createElement('p', { className: 'book-desc' }, book.description),
                                React.createElement('div', { className: 'book-price' },
                                    React.createElement('span', { className: 'price' }, `$${book.price}`),
                                    React.createElement('button', {
                                        className: 'btn btn-primary',
                                        onClick: () => addToCart(book)
                                    }, 'Add to Cart')
                                )
                            )
                        )
                    ),
                    
                    filteredEbooks.length === 0 && React.createElement('div', { className: 'text-center', style: {padding: '3rem'} },
                        React.createElement('p', { style: {color: '#6b7280', fontSize: '1.125rem'} }, 'No books found matching your search.')
                    )
                );
            };

            const WorkshopsPage = () => {
                return React.createElement('div', { className: 'store-container' },
                    React.createElement('h1', { className: 'page-title' }, 'Workshops & Training'),
                    React.createElement('div', { className: 'workshops-list' },
                        mockBackend.workshops.map(workshop =>
                            React.createElement('div', { key: workshop.id, className: 'workshop-card' },
                                React.createElement('div', { className: 'workshop-header' },
                                    React.createElement('div', { className: 'workshop-info' },
                                        React.createElement('h3', { className: 'workshop-title' }, workshop.title),
                                        React.createElement('p', { className: 'workshop-meta' },
                                            `📅 ${workshop.date} • ⏰ ${workshop.duration} • Instructor: ${workshop.instructor}`
                                        ),
                                        React.createElement('p', { style: {color: '#374151'} }, workshop.description)
                                    ),
                                    React.createElement('div', { className: 'workshop-price' },
                                        React.createElement('div', { className: 'price-large' }, `$${workshop.price}`),
                                        React.createElement('button', {
                                            className: 'btn btn-primary',
                                            onClick: () => addToCart(workshop)
                                        }, 'Register Now')
                                    )
                                )
                            )
                        )
                    )
                );
            };

            const BlogPage = () => {
                return React.createElement('div', { className: 'blog-container' },
                    React.createElement('h1', { className: 'page-title' }, 'Ministry Blog'),
                    React.createElement('div', { className: 'blog-list' },
                        mockBackend.blogs.map(blog =>
                            React.createElement('div', {
                                key: blog.id,
                                className: 'blog-card',
                                onClick: () => setActiveBlog(blog)
                            },
                                React.createElement('h3', { className: 'blog-title' }, blog.title),
                                React.createElement('p', { className: 'blog-meta' },
                                    `${blog.date} • ${blog.category} • ${blog.readTime}`
                                ),
                                React.createElement('p', { className: 'blog-excerpt' }, blog.excerpt),
                                React.createElement('button', { className: 'read-more' }, 'Read More →')
                            )
                        )
                    ),
                    
                    activeBlog && React.createElement('div', { className: 'modal-overlay' },
                        React.createElement('div', { className: 'modal', style: {maxWidth: '600px'} },
                            React.createElement('button', {
                                className: 'modal-close',
                                onClick: () => setActiveBlog(null)
                            }, '×'),
                            React.createElement('h2', { className: 'modal-title' }, activeBlog.title),
                            React.createElement('p', { className: 'blog-meta' },
                                `By ${activeBlog.author} • ${activeBlog.date} • ${activeBlog.readTime}`
                            ),
                            React.createElement('div', { style: {lineHeight: '1.6', marginTop: '1rem'} },
                                React.createElement('p', { style: {marginBottom: '1rem'} }, activeBlog.content),
                                React.createElement('p', null, 'Continue reading for more insights and practical applications...')
                            )
                        )
                    )
                );
            };

            const CartPage = () => {
                return React.createElement('div', { className: 'cart-container' },
                    React.createElement('h1', { className: 'page-title' }, 'Shopping Cart'),
                    
                    cart.length === 0 ? React.createElement('div', { className: 'cart-empty' },
                        React.createElement('div', { className: 'cart-empty-icon' }, '🛒'),
                        React.createElement('p', { style: {fontSize: '1.25rem', color: '#6b7280', margin: '1rem 0'} }, 'Your cart is empty'),
                        React.createElement('button', {
                            className: 'btn btn-primary',
                            onClick: () => setCurrentPage('store')
                        }, 'Continue Shopping')
                    ) : React.createElement('div', null,
                        React.createElement('div', { className: 'cart-items' },
                            cart.map((item) =>
                                React.createElement('div', { key: item.cartId, className: 'cart-item' },
                                    React.createElement('div', { className: 'cart-item-info' },
                                        React.createElement('div', { className: 'cart-item-icon' }, item.image),
                                        React.createElement('div', { className: 'cart-item-details' },
                                            React.createElement('h3', null, item.title),
                                            React.createElement('p', null, item.category)
                                        )
                                    ),
                                    React.createElement('div', { className: 'cart-item-actions' },
                                        React.createElement('span', { className: 'price' }, `$${item.price}`),
                                        React.createElement('button', {
                                            style: {color: '#dc2626', background: 'none', border: 'none', cursor: 'pointer', fontSize: '1.2rem'},
                                            onClick: () => removeFromCart(item.cartId)
                                        }, '✕')
                                    )
                                )
                            )
                        ),

                        React.createElement('div', { className: 'cart-total' },
                            React.createElement('div', { className: 'total-row' },
                                React.createElement('span', { className: 'total-label' }, 'Total:'),
                                React.createElement('span', { className: 'total-amount' }, `$${getTotal()}`)
                            ),
                            React.createElement('button', {
                                className: 'checkout-btn',
                                onClick: handleCheckout,
                                disabled: loading
                            }, loading ? 'Processing...' : 'Proceed to Checkout'),
                            React.createElement('p', { className: 'secure-text' }, 'Secure payment processing')
                        )
                    )
                );
            };

            const AboutPage = () => {
                return React.createElement('div', { className: 'blog-container' },
                    React.createElement('h1', { className: 'page-title' }, 'About The Definitive Word'),
                    React.createElement('div', {
                        style: {
                            background: 'linear-gradient(to right, #dbeafe, #fecaca)',
                            padding: '2rem',
                            borderRadius: '8px',
                            marginBottom: '2rem'
                        }
                    },
                        React.createElement('p', { style: {fontSize: '1.125rem', color: '#374151', marginBottom: '1rem'} },
                            'The Definitive Word is a prophetic ministry dedicated to empowering believers through biblical teaching, prophetic insights, and practical training. Our mission is to help you discover and walk in your God-given destiny.'
                        ),
                        React.createElement('p', { style: {fontSize: '1.125rem', color: '#374151'} },
                            'Through our ebooks, workshops, and training materials, we provide tools and resources that transform lives and activate callings.'
                        )
                    ),
                    
                    React.createElement('div', { style: {display: 'flex', flexDirection: 'column', gap: '1rem'} },
                        React.createElement('div', { style: {display: 'flex', alignItems: 'center'} },
                            React.createElement('span', { style: {fontSize: '1.2rem', marginRight: '0.75rem'} }, '✉️'),
                            React.createElement('span', { style: {color: '#374151'} }, 'contact@thedefinitiveword.com')
                        ),
                        React.createElement('div', { style: {display: 'flex', alignItems: 'center'} },
                            React.createElement('span', { style: {fontSize: '1.2rem', marginRight: '0.75rem'} }, '📞'),
                            React.createElement('span', { style: {color: '#374151'} }, '+1 (555) 123-4567')
                        ),
                        React.createElement('div', { style: {display: 'flex', alignItems: 'center'} },
                            React.createElement('span', { style: {fontSize: '1.2rem', marginRight: '0.75rem'} }, '📍'),
                            React.createElement('span', { style: {color: '#374151'} }, 'Your Ministry Location')
                        )
                    )
                );
            };

            // Main App Render
            return React.createElement('div', { className: 'app' },
                React.createElement(NavBar),
                
                currentPage === 'home' && React.createElement(HomePage),
                currentPage === 'store' && React.createElement(StorePage),
                currentPage === 'workshops' && React.createElement(WorkshopsPage),
                currentPage === 'blog' && React.createElement(BlogPage),
                currentPage === 'cart' && React.createElement(CartPage),
                currentPage === 'about' && React.createElement(AboutPage),
                
                React.createElement(LoginModal),
                
                React.createElement('footer', null,
                    React.createElement('div', { className: 'footer-content' },
                        React.createElement('h3', { className: 'footer-title' }, 'The Definitive Word'),
                        React.createElement('p', { className: 'footer-tagline' }, 'Your Destiny Has Been Written'),
                        React.createElement('p', { className: 'footer-copyright' }, '© 2025 The Definitive Word. All rights reserved.')
                    )
                )
            );
        }

        // Render the app
        const root = ReactDOM.createRoot(document.getElementById('root'));
        root.render(React.createElement(EbookStore));
    </script>
</body>
</html>

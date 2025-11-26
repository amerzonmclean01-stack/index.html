const { useState, useEffect } = React;

// Currency conversion rates (simplified)
const exchangeRates = {
    USD: 1,
    EUR: 0.85,
    GBP: 0.73,
    NGN: 410,
    CAD: 1.25,
    AUD: 1.35,
    JPY: 110,
    ZAR: 18.50
};

const currencySymbols = {
    USD: '$',
    EUR: '€',
    GBP: '£',
    NGN: '₦',
    CAD: 'C$',
    AUD: 'A$',
    JPY: '¥',
    ZAR: 'R'
};

const currencyFlags = {
    USD: '🇺🇸',
    EUR: '🇪🇺',
    GBP: '🇬🇧',
    NGN: '🇳🇬',
    CAD: '🇨🇦',
    AUD: '🇦🇺',
    JPY: '🇯🇵',
    ZAR: '🇿🇦'
};

// Mock backend data
const mockBackend = {
    users: [
        { id: 1, name: 'John Doe', email: 'john@example.com', password: 'password123', role: 'user' },
        { id: 2, name: 'Admin', email: 'admin', password: 'admin', role: 'admin' }
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
    const [currency, setCurrency] = useState('USD');
    const [paymentModalOpen, setPaymentModalOpen] = useState(false);
    const [selectedPaymentMethod, setSelectedPaymentMethod] = useState('');
    const [ebooks, setEbooks] = useState(mockBackend.ebooks);
    const [workshops, setWorkshops] = useState(mockBackend.workshops);
    const [successMessage, setSuccessMessage] = useState('');
    const [showAddForm, setShowAddForm] = useState(false);
    const [itemToDelete, setItemToDelete] = useState(null);
    const [simpleFormData, setSimpleFormData] = useState({
        title: '',
        price: '',
        type: 'ebook'
    });

    // Load user from localStorage
    useEffect(() => {
        const savedUser = localStorage.getItem('ebookStoreUser');
        if (savedUser) {
            setUser(JSON.parse(savedUser));
        }
    }, []);

    // Currency conversion function
    const convertPrice = (price) => {
        return (price * exchangeRates[currency]).toFixed(2);
    };

    // SUPER SIMPLE ADMIN LOGIN
    const quickAdminLogin = () => {
        const adminUser = { id: 2, name: 'Admin', email: 'admin', role: 'admin' };
        setUser(adminUser);
        localStorage.setItem('ebookStoreUser', JSON.stringify(adminUser));
        setSuccessMessage('Welcome Admin! You can now manage the store.');
        setTimeout(() => setSuccessMessage(''), 3000);
    };

    const handleLogin = async (e) => {
        if (e) e.preventDefault();
        setLoading(true);

        // Simple login - just check if email and password match any user
        const user = mockBackend.users.find(u => 
            u.email === e.target.email.value && u.password === e.target.password.value
        );

        setTimeout(() => {
            if (user) {
                const { password, ...userWithoutPassword } = user;
                setUser(userWithoutPassword);
                localStorage.setItem('ebookStoreUser', JSON.stringify(userWithoutPassword));
                setLoginModalOpen(false);
                setSuccessMessage(`Welcome ${user.name}!`);
                setTimeout(() => setSuccessMessage(''), 3000);
            } else {
                setSuccessMessage('Invalid login. Try email: "admin" & password: "admin" for admin access.');
                setTimeout(() => setSuccessMessage(''), 5000);
            }
            setLoading(false);
        }, 500);
    };

    const handleLogout = () => {
        setUser(null);
        localStorage.removeItem('ebookStoreUser');
        setCart([]);
        setSuccessMessage('You have been logged out.');
        setTimeout(() => setSuccessMessage(''), 3000);
    };

    const addToCart = (product) => {
        setCart([...cart, { ...product, cartId: Date.now() }]);
        setSuccessMessage(`${product.title} added to cart!`);
        setTimeout(() => setSuccessMessage(''), 2000);
    };

    const removeFromCart = (cartId) => {
        const item = cart.find(item => item.cartId === cartId);
        setCart(cart.filter(item => item.cartId !== cartId));
        setSuccessMessage(`${item.title} removed from cart.`);
        setTimeout(() => setSuccessMessage(''), 2000);
    };

    const getTotal = () => {
        return cart.reduce((sum, item) => sum + item.price, 0).toFixed(2);
    };

    const handleCheckout = () => {
        if (!user) {
            setLoginModalOpen(true);
            return;
        }
        setPaymentModalOpen(true);
    };

    const processPayment = () => {
        setLoading(true);
        setTimeout(() => {
            setSuccessMessage('Payment successful! Thank you for your order!');
            setCart([]);
            setPaymentModalOpen(false);
            setLoading(false);
            setTimeout(() => setSuccessMessage(''), 5000);
        }, 2000);
    };

    // SUPER SIMPLE ADD ITEM FUNCTION
    const quickAddItem = () => {
        if (!simpleFormData.title || !simpleFormData.price) {
            setSuccessMessage('Please enter both title and price');
            setTimeout(() => setSuccessMessage(''), 3000);
            return;
        }

        const newItem = {
            id: Date.now(),
            title: simpleFormData.title,
            price: parseFloat(simpleFormData.price),
            category: 'Ministry',
            image: simpleFormData.type === 'ebook' ? '📖' : '🎓',
            description: 'New item added by admin',
            author: 'Admin',
            isFeatured: false
        };

        if (simpleFormData.type === 'ebook') {
            setEbooks([...ebooks, newItem]);
            setSuccessMessage('Ebook added successfully!');
        } else {
            setWorkshops([...workshops, { ...newItem, date: 'Soon', duration: '2 hours', instructor: 'Admin' }]);
            setSuccessMessage('Workshop added successfully!');
        }

        setSimpleFormData({ title: '', price: '', type: 'ebook' });
        setShowAddForm(false);
        setTimeout(() => setSuccessMessage(''), 3000);
    };

    // SIMPLE DELETE FUNCTION
    const quickDeleteItem = (id, type) => {
        if (type === 'ebook') {
            setEbooks(ebooks.filter(ebook => ebook.id !== id));
            setSuccessMessage('Item deleted successfully!');
        } else {
            setWorkshops(workshops.filter(workshop => workshop.id !== id));
            setSuccessMessage('Item deleted successfully!');
        }
        setItemToDelete(null);
        setTimeout(() => setSuccessMessage(''), 3000);
    };

    const filteredEbooks = ebooks.filter(ebook =>
        ebook.title.toLowerCase().includes(searchQuery.toLowerCase()) ||
        ebook.author.toLowerCase().includes(searchQuery.toLowerCase()) ||
        ebook.description.toLowerCase().includes(searchQuery.toLowerCase())
    );

    const featuredEbooks = ebooks.filter(ebook => ebook.isFeatured);

    // Currency Selector Component
    const CurrencySelector = () => {
        return React.createElement('div', { className: 'currency-selector' },
            React.createElement('span', { style: {fontSize: '0.9rem', fontWeight: '500'} }, 'Currency:'),
            React.createElement('select', {
                value: currency,
                onChange: (e) => setCurrency(e.target.value),
                style: { 
                    padding: '0.4rem', 
                    border: '1px solid #d1d5db', 
                    borderRadius: '4px',
                    fontSize: '0.9rem'
                }
            },
                Object.entries(currencyFlags).map(([code, flag]) =>
                    React.createElement('option', { key: code, value: code },
                        `${flag} ${code}`
                    )
                )
            )
        );
    };

    // Quick Admin Panel Component
    const QuickAdminPanel = () => {
        if (!user || user.role !== 'admin') return null;

        return React.createElement('div', { className: 'quick-admin' },
            React.createElement('h3', { style: {textAlign: 'center', marginBottom: '1rem', color: 'white'} }, 'Admin Controls'),
            React.createElement('div', { className: 'quick-admin-buttons' },
                React.createElement('button', {
                    className: 'quick-admin-btn',
                    onClick: () => setShowAddForm(!showAddForm)
                }, showAddForm ? 'Cancel Add' : '➕ Add Item'),
                
                React.createElement('button', {
                    className: 'quick-admin-btn',
                    onClick: () => {
                        setEbooks(mockBackend.ebooks);
                        setWorkshops(mockBackend.workshops);
                        setSuccessMessage('Store reset to original items!');
                        setTimeout(() => setSuccessMessage(''), 3000);
                    }
                }, '🔄 Reset Store'),
                
                React.createElement('button', {
                    className: 'quick-admin-btn',
                    onClick: handleLogout
                }, '🚪 Logout')
            ),

            showAddForm && React.createElement('div', { className: 'simple-add-form' },
                React.createElement('h4', { style: {textAlign: 'center', marginBottom: '1rem', color: '#1f2937'} }, 'Add New Item'),
                React.createElement('div', { className: 'simple-form-group' },
                    React.createElement('select', {
                        className: 'simple-form-input',
                        value: simpleFormData.type,
                        onChange: (e) => setSimpleFormData({...simpleFormData, type: e.target.value})
                    },
                        React.createElement('option', { value: 'ebook' }, 'Ebook'),
                        React.createElement('option', { value: 'workshop' }, 'Workshop')
                    )
                ),
                React.createElement('div', { className: 'simple-form-group' },
                    React.createElement('input', {
                        type: 'text',
                        className: 'simple-form-input',
                        placeholder: 'Item Title',
                        value: simpleFormData.title,
                        onChange: (e) => setSimpleFormData({...simpleFormData, title: e.target.value})
                    })
                ),
                React.createElement('div', { className: 'simple-form-group' },
                    React.createElement('input', {
                        type: 'number',
                        className: 'simple-form-input',
                        placeholder: 'Price (USD)',
                        value: simpleFormData.price,
                        onChange: (e) => setSimpleFormData({...simpleFormData, price: e.target.value})
                    })
                ),
                React.createElement('div', { className: 'simple-form-actions' },
                    React.createElement('button', {
                        className: 'btn btn-success',
                        onClick: quickAddItem
                    }, 'Add Item'),
                    React.createElement('button', {
                        className: 'btn btn-secondary',
                        onClick: () => setShowAddForm(false)
                    }, 'Cancel')
                )
            )
        );
    };

    // Delete Confirmation Component
    const DeleteConfirmation = ({ item, type, onConfirm, onCancel }) => {
        if (!item) return null;

        return React.createElement('div', { className: 'delete-confirm' },
            React.createElement('p', { style: {fontWeight: 'bold', marginBottom: '0.5rem'} }, 
                `Delete "${item.title}"?`
            ),
            React.createElement('p', { style: {marginBottom: '1rem', fontSize: '0.9rem', color: '#6b7280'} }, 
                'This action cannot be undone.'
            ),
            React.createElement('div', { style: {display: 'flex', gap: '1rem', justifyContent: 'center'} },
                React.createElement('button', {
                    className: 'btn btn-danger',
                    onClick: () => onConfirm(item.id, type)
                }, 'Yes, Delete'),
                React.createElement('button', {
                    className: 'btn btn-secondary',
                    onClick: onCancel
                }, 'Cancel')
            )
        );
    };

    // Navigation Component
    const NavBar = () => {
        const isActive = (page) => currentPage === page;

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
                            React.createElement('div', { className: 'tagline' }, 'Christian Ebook Store')
                        )
                    ),

                    React.createElement('div', { className: 'nav-links' },
                        React.createElement('button', {
                            className: `nav-link ${isActive('home') ? 'active' : ''}`,
                            onClick: () => setCurrentPage('home')
                        }, 'Home'),
                        React.createElement('button', {
                            className: `nav-link ${isActive('store') ? 'active' : ''}`,
                            onClick: () => setCurrentPage('store')
                        }, 'Ebooks'),
                        React.createElement('button', {
                            className: `nav-link ${isActive('workshops') ? 'active' : ''}`,
                            onClick: () => setCurrentPage('workshops')
                        }, 'Workshops'),
                        React.createElement('button', {
                            className: `nav-link ${isActive('cart') ? 'active' : ''}`,
                            onClick: () => setCurrentPage('cart')
                        }, `Cart (${cart.length})`)
                    ),

                    React.createElement('div', { className: 'nav-actions' },
                        React.createElement(CurrencySelector),
                        
                        React.createElement('button', {
                            className: 'cart-button',
                            onClick: () => setCurrentPage('cart')
                        },
                            React.createElement('span', null, '🛒'),
                            cart.length > 0 && React.createElement('span', { className: 'cart-count' }, cart.length)
                        ),

                        React.createElement('div', { className: 'user-section' },
                            user ? React.createElement('div', { style: {display: 'flex', alignItems: 'center', gap: '0.5rem'} },
                                React.createElement('span', { style: {fontSize: '0.9rem'} }, user.name),
                                user.role === 'admin' && React.createElement('span', { className: 'admin-badge' }, 'Admin'),
                                React.createElement('button', {
                                    className: 'nav-link',
                                    onClick: handleLogout
                                }, 'Logout')
                            ) : React.createElement('button', {
                                className: 'nav-link',
                                onClick: () => setLoginModalOpen(true)
                            }, 'Login')
                        ),

                        React.createElement('button', {
                            className: 'mobile-menu-button',
                            onClick: () => setMobileMenuOpen(!mobileMenuOpen)
                        }, '☰')
                    )
                ),

                mobileMenuOpen && React.createElement('div', { className: 'mobile-menu' },
                    React.createElement('button', {
                        className: `mobile-menu-link ${isActive('home') ? 'active' : ''}`,
                        onClick: () => { setCurrentPage('home'); setMobileMenuOpen(false); }
                    }, 'Home'),
                    React.createElement('button', {
                        className: `mobile-menu-link ${isActive('store') ? 'active' : ''}`,
                        onClick: () => { setCurrentPage('store'); setMobileMenuOpen(false); }
                    }, 'Ebooks'),
                    React.createElement('button', {
                        className: `mobile-menu-link ${isActive('workshops') ? 'active' : ''}`,
                        onClick: () => { setCurrentPage('workshops'); setMobileMenuOpen(false); }
                    }, 'Workshops'),
                    React.createElement('button', {
                        className: `mobile-menu-link ${isActive('cart') ? 'active' : ''}`,
                        onClick: () => { setCurrentPage('cart'); setMobileMenuOpen(false); }
                    }, `Cart (${cart.length})`),
                    !user && React.createElement('button', {
                        className: 'mobile-menu-link',
                        onClick: () => { setLoginModalOpen(true); setMobileMenuOpen(false); }
                    }, 'Login')
                )
            )
        );
    };

    // Login Modal Component
    const LoginModal = () => {
        if (!loginModalOpen) return null;

        return React.createElement('div', { className: 'modal-overlay' },
            React.createElement('div', { className: 'modal' },
                React.createElement('button', {
                    className: 'modal-close',
                    onClick: () => setLoginModalOpen(false)
                }, '×'),

                React.createElement('h2', { className: 'modal-title' }, isLogin ? 'Login' : 'Create Account'),

                React.createElement('div', { className: 'login-tabs' },
                    React.createElement('button', {
                        className: `login-tab ${isLogin ? 'active' : ''}`,
                        onClick: () => setIsLogin(true)
                    }, 'Login'),
                    React.createElement('button', {
                        className: `login-tab ${!isLogin ? 'active' : ''}`,
                        onClick: () => setIsLogin(false)
                    }, 'Sign Up')
                ),

                React.createElement('form', { onSubmit: handleLogin },
                    React.createElement('div', { className: 'simple-form-group' },
                        React.createElement('input', {
                            type: 'email',
                            name: 'email',
                            className: 'simple-form-input',
                            placeholder: 'Email',
                            required: true,
                            defaultValue: isLogin ? 'admin' : ''
                        })
                    ),
                    React.createElement('div', { className: 'simple-form-group' },
                        React.createElement('input', {
                            type: 'password',
                            name: 'password',
                            className: 'simple-form-input',
                            placeholder: 'Password',
                            required: true,
                            defaultValue: isLogin ? 'admin' : ''
                        })
                    ),
                    !isLogin && React.createElement('div', { className: 'simple-form-group' },
                        React.createElement('input', {
                            type: 'text',
                            name: 'name',
                            className: 'simple-form-input',
                            placeholder: 'Full Name',
                            required: true
                        })
                    ),

                    React.createElement('button', {
                        type: 'submit',
                        className: 'btn btn-primary',
                        style: {width: '100%', marginBottom: '1rem'},
                        disabled: loading
                    }, loading ? 'Loading...' : (isLogin ? 'Login' : 'Create Account')),

                    isLogin && React.createElement('div', { className: 'form-footer' },
                        React.createElement('p', { style: {fontSize: '0.9rem', color: '#6b7280'} },
                            'Demo: Use ',
                            React.createElement('button', {
                                type: 'button',
                                className: 'form-link',
                                onClick: quickAdminLogin
                            }, 'Quick Admin Login'),
                            ' for instant admin access'
                        )
                    )
                )
            )
        );
    };

    // Payment Modal Component
    const PaymentModal = () => {
        if (!paymentModalOpen) return null;

        return React.createElement('div', { className: 'modal-overlay' },
            React.createElement('div', { className: 'modal' },
                React.createElement('button', {
                    className: 'modal-close',
                    onClick: () => setPaymentModalOpen(false)
                }, '×'),

                React.createElement('h2', { className: 'modal-title' }, 'Complete Your Purchase'),

                React.createElement('div', { style: {marginBottom: '1.5rem'} },
                    React.createElement('h3', { style: {marginBottom: '1rem', color: '#1f2937'} }, 'Order Summary'),
                    cart.map(item => 
                        React.createElement('div', {
                            key: item.cartId,
                            style: {display: 'flex', justifyContent: 'space-between', marginBottom: '0.5rem'}
                        },
                            React.createElement('span', null, item.title),
                            React.createElement('span', null, `${currencySymbols[currency]}${convertPrice(item.price)}`)
                        )
                    ),
                    React.createElement('div', {
                        style: {display: 'flex', justifyContent: 'space-between', marginTop: '1rem', paddingTop: '1rem', borderTop: '1px solid #e5e7eb', fontWeight: 'bold'}
                    },
                        React.createElement('span', null, 'Total:'),
                        React.createElement('span', null, `${currencySymbols[currency]}${convertPrice(getTotal())}`)
                    )
                ),

                React.createElement('div', { className: 'simple-form-group' },
                    React.createElement('label', { style: {display: 'block', marginBottom: '0.5rem', fontWeight: '500'} }, 'Payment Method'),
                    React.createElement('select', {
                        className: 'simple-form-input',
                        value: selectedPaymentMethod,
                        onChange: (e) => setSelectedPaymentMethod(e.target.value),
                        required: true
                    },
                        React.createElement('option', { value: '' }, 'Select Payment Method'),
                        React.createElement('option', { value: 'card' }, 'Credit/Debit Card'),
                        React.createElement('option', { value: 'paypal' }, 'PayPal'),
                        React.createElement('option', { value: 'transfer' }, 'Bank Transfer')
                    )
                ),

                selectedPaymentMethod && React.createElement('div', { style: {marginTop: '1rem'} },
                    React.createElement('p', { style: {fontSize: '0.9rem', color: '#059669', textAlign: 'center'} },
                        'Demo: No real payment will be processed'
                    )
                ),

                React.createElement('button', {
                    className: 'btn btn-primary',
                    style: {width: '100%', marginTop: '1.5rem'},
                    onClick: processPayment,
                    disabled: !selectedPaymentMethod || loading
                }, loading ? 'Processing...' : 'Complete Purchase')
            )
        );
    };

    // Home Page Component
    const HomePage = () => {
        return React.createElement('div', { className: 'main-content' },
            React.createElement('section', { className: 'hero' },
                React.createElement('h1', null, 'The Definitive Word'),
                React.createElement('div', { className: 'hero-tagline' }, 'Christian Ebook Store'),
                React.createElement('p', { className: 'hero-subtitle' }, 'Discover transformative Christian ebooks and workshops to deepen your faith and ministry'),
                React.createElement('div', { className: 'hero-buttons' },
                    React.createElement('button', {
                        className: 'btn btn-primary',
                        onClick: () => setCurrentPage('store')
                    }, 'Browse Ebooks'),
                    React.createElement('button', {
                        className: 'btn btn-secondary',
                        onClick: () => setCurrentPage('workshops')
                    }, 'View Workshops')
                )
            ),

            React.createElement('div', { className: 'container' },
                React.createElement(QuickAdminPanel),

                successMessage && React.createElement('div', { className: successMessage.includes('error') ? 'error-message' : 'success-message' },
                    successMessage
                ),

                React.createElement('section', { className: 'features' },
                    React.createElement('h2', { className: 'section-title' }, 'Why Choose Our Store?'),
                    React.createElement('div', { className: 'features-grid' },
                        React.createElement('div', { className: 'feature-card blue' },
                            React.createElement('div', { className: 'feature-icon' }, '🙏'),
                            React.createElement('h3', { className: 'feature-title' }, 'Faith-Based Content'),
                            React.createElement('p', { className: 'feature-desc' }, 'Carefully curated Christian resources for spiritual growth')
                        ),
                        React.createElement('div', { className: 'feature-card red' },
                            React.createElement('div', { className: 'feature-icon' }, '📚'),
                            React.createElement('h3', { className: 'feature-title' }, 'Instant Access'),
                            React.createElement('p', { className: 'feature-desc' }, 'Download your ebooks immediately after purchase')
                        ),
                        React.createElement('div', { className: 'feature-card blue' },
                            React.createElement('div', { className: 'feature-icon' }, '💝'),
                            React.createElement('h3', { className: 'feature-title' }, 'Ministry Support'),
                            React.createElement('p', { className: 'feature-desc' }, 'Proceeds support Christian ministry and outreach')
                        )
                    )
                ),

                React.createElement('section', { className: 'featured-books' },
                    React.createElement('h2', { className: 'section-title' }, 'Featured Ebooks'),
                    React.createElement('div', { className: 'books-grid' },
                        featuredEbooks.map(ebook =>
                            React.createElement('div', { key: ebook.id, className: 'book-card' },
                                React.createElement('div', { className: 'book-icon' }, ebook.image),
                                React.createElement('h3', { className: 'book-title' }, ebook.title),
                                React.createElement('p', { className: 'book-desc' }, ebook.description),
                                React.createElement('p', { style: {fontSize: '0.9rem', color: '#6b7280', marginBottom: '1rem'} }, `by ${ebook.author}`),
                                React.createElement('div', { className: 'book-price' },
                                    React.createElement('span', { className: 'price' }, 
                                        `${currencySymbols[currency]}${convertPrice(ebook.price)}`
                                    ),
                                    React.createElement('button', {
                                        className: 'btn btn-primary',
                                        onClick: () => addToCart(ebook)
                                    }, 'Add to Cart')
                                ),
                                user?.role === 'admin' && React.createElement('button', {
                                    className: 'btn btn-danger',
                                    style: {width: '100%', marginTop: '0.5rem', fontSize: '0.8rem', padding: '0.4rem'},
                                    onClick: () => setItemToDelete({...ebook, type: 'ebook'})
                                }, 'Delete')
                            )
                        )
                    )
                )
            )
        );
    };

    // Store Page Component
    const StorePage = () => {
        return React.createElement('div', { className: 'store-container' },
            React.createElement(QuickAdminPanel),

            successMessage && React.createElement('div', { className: successMessage.includes('error') ? 'error-message' : 'success-message' },
                successMessage
            ),

            React.createElement('h1', { className: 'page-title' }, 'Christian Ebooks'),
            React.createElement('p', { className: 'page-subtitle' }, 'Transformative resources for your spiritual journey'),

            React.createElement('div', { className: 'search-container' },
                React.createElement('span', { className: 'search-icon' }, '🔍'),
                React.createElement('input', {
                    type: 'text',
                    className: 'search-input',
                    placeholder: 'Search ebooks by title, author, or description...',
                    value: searchQuery,
                    onChange: (e) => setSearchQuery(e.target.value)
                })
            ),

            itemToDelete && React.createElement(DeleteConfirmation, {
                item: itemToDelete,
                type: itemToDelete.type,
                onConfirm: quickDeleteItem,
                onCancel: () => setItemToDelete(null)
            }),

            React.createElement('div', { className: 'books-grid' },
                filteredEbooks.map(ebook =>
                    React.createElement('div', { key: ebook.id, className: 'book-card' },
                        React.createElement('div', { className: 'book-icon' }, ebook.image),
                        React.createElement('h3', { className: 'book-title' }, ebook.title),
                        React.createElement('p', { className: 'book-desc' }, ebook.description),
                        React.createElement('p', { style: {fontSize: '0.9rem', color: '#6b7280', marginBottom: '0.5rem'} }, `by ${ebook.author}`),
                        React.createElement('p', { style: {fontSize: '0.8rem', color: '#dc2626', marginBottom: '1rem'} }, ebook.category),
                        React.createElement('div', { className: 'book-price' },
                            React.createElement('span', { className: 'price' }, 
                                `${currencySymbols[currency]}${convertPrice(ebook.price)}`
                            ),
                            React.createElement('button', {
                                className: 'btn btn-primary',
                                onClick: () => addToCart(ebook)
                            }, 'Add to Cart')
                        ),
                        user?.role === 'admin' && React.createElement('button', {
                            className: 'btn btn-danger',
                            style: {width: '100%', marginTop: '0.5rem', fontSize: '0.8rem', padding: '0.4rem'},
                            onClick: () => setItemToDelete({...ebook, type: 'ebook'})
                        }, 'Delete')
                    )
                )
            ),

            filteredEbooks.length === 0 && React.createElement('div', { className: 'text-center', style: {padding: '4rem', color: '#6b7280'} },
                React.createElement('div', { style: {fontSize: '4rem', marginBottom: '1rem'} }, '📚'),
                React.createElement('h3', null, 'No ebooks found'),
                React.createElement('p', null, 'Try adjusting your search terms')
            )
        );
    };

    // Workshops Page Component
    const WorkshopsPage = () => {
        return React.createElement('div', { className: 'store-container' },
            React.createElement(QuickAdminPanel),

            successMessage && React.createElement('div', { className: successMessage.includes('error') ? 'error-message' : 'success-message' },
                successMessage
            ),

            React.createElement('h1', { className: 'page-title' }, 'Christian Workshops'),
            React.createElement('p', { className: 'page-subtitle' }, 'Live and recorded workshops for deeper learning'),

            itemToDelete && React.createElement(DeleteConfirmation, {
                item: itemToDelete,
                type: itemToDelete.type,
                onConfirm: quickDeleteItem,
                onCancel: () => setItemToDelete(null)
            }),

            React.createElement('div', { className: 'books-grid' },
                workshops.map(workshop =>
                    React.createElement('div', { key: workshop.id, className: 'book-card' },
                        React.createElement('div', { className: 'book-icon' }, '🎓'),
                        React.createElement('h3', { className: 'book-title' }, workshop.title),
                        React.createElement('p', { className: 'book-desc' }, workshop.description),
                        React.createElement('div', { style: {marginBottom: '1rem'} },
                            React.createElement('p', { style: {fontSize: '0.9rem', color: '#6b7280', marginBottom: '0.25rem'} }, 
                                `Instructor: ${workshop.instructor}`
                            ),
                            React.createElement('p', { style: {fontSize: '0.9rem', color: '#6b7280', marginBottom: '0.25rem'} }, 
                                `Date: ${workshop.date}`
                            ),
                            React.createElement('p', { style: {fontSize: '0.9rem', color: '#6b7280'} }, 
                                `Duration: ${workshop.duration}`
                            )
                        ),
                        React.createElement('div', { className: 'book-price' },
                            React.createElement('span', { className: 'price' }, 
                                `${currencySymbols[currency]}${convertPrice(workshop.price)}`
                            ),
                            React.createElement('button', {
                                className: 'btn btn-primary',
                                onClick: () => addToCart(workshop)
                            }, 'Add to Cart')
                        ),
                        user?.role === 'admin' && React.createElement('button', {
                            className: 'btn btn-danger',
                            style: {width: '100%', marginTop: '0.5rem', fontSize: '0.8rem', padding: '0.4rem'},
                            onClick: () => setItemToDelete({...workshop, type: 'workshop'})
                        }, 'Delete')
                    )
                )
            ),

            workshops.length === 0 && React.createElement('div', { className: 'text-center', style: {padding: '4rem', color: '#6b7280'} },
                React.createElement('div', { style: {fontSize: '4rem', marginBottom: '1rem'} }, '🎓'),
                React.createElement('h3', null, 'No workshops available'),
                React.createElement('p', null, 'Check back later for new workshops')
            )
        );
    };

    // Cart Page Component
    const CartPage = () => {
        if (cart.length === 0) {
            return React.createElement('div', { className: 'cart-container' },
                React.createElement('div', { className: 'cart-empty' },
                    React.createElement('div', { className: 'cart-empty-icon' }, '🛒'),
                    React.createElement('h2', null, 'Your cart is empty'),
                    React.createElement('p', { style: {color: '#6b7280', marginBottom: '2rem'} }, 'Browse our ebooks and workshops to add items to your cart'),
                    React.createElement('div', { style: {display: 'flex', gap: '1rem', justifyContent: 'center', flexWrap: 'wrap'} },
                        React.createElement('button', {
                            className: 'btn btn-primary',
                            onClick: () => setCurrentPage('store')
                        }, 'Browse Ebooks'),
                        React.createElement('button', {
                            className: 'btn btn-secondary',
                            onClick: () => setCurrentPage('workshops')
                        }, 'View Workshops')
                    )
                )
            );
        }

        return React.createElement('div', { className: 'cart-container' },
            React.createElement('h1', { className: 'page-title' }, 'Your Cart'),
            
            React.createElement('div', { className: 'cart-items' },
                cart.map(item =>
                    React.createElement('div', { key: item.cartId, className: 'cart-item' },
                        React.createElement('div', { className: 'cart-item-info' },
                            React.createElement('div', { className: 'cart-item-icon' }, item.image || '📖'),
                            React.createElement('div', { className: 'cart-item-details' },
                                React.createElement('h3', null, item.title),
                                React.createElement('p', null, item.description || `by ${item.author}`)
                            )
                        ),
                        React.createElement('div', { className: 'cart-item-actions' },
                            React.createElement('span', { className: 'price' }, 
                                `${currencySymbols[currency]}${convertPrice(item.price)}`
                            ),
                            React.createElement('button', {
                                className: 'btn btn-danger',
                                onClick: () => removeFromCart(item.cartId)
                            }, 'Remove')
                        )
                    )
                )
            ),

            React.createElement('div', { className: 'cart-total' },
                React.createElement('div', { className: 'total-row' },
                    React.createElement('span', { className: 'total-label' }, 'Total:'),
                    React.createElement('span', { className: 'total-amount' }, 
                        `${currencySymbols[currency]}${convertPrice(getTotal())}`
                    )
                ),
                React.createElement('button', {
                    className: 'checkout-btn',
                    onClick: handleCheckout
                }, 'Proceed to Checkout'),
                React.createElement('p', { className: 'secure-text' }, '🔒 Secure checkout • Your payment is safe with us')
            )
        );
    };

    // Main App Render
    return React.createElement('div', { className: 'app' },
        React.createElement(NavBar),
        
        currentPage === 'home' && React.createElement(HomePage),
        currentPage === 'store' && React.createElement(StorePage),
        currentPage === 'workshops' && React.createElement(WorkshopsPage),
        currentPage === 'cart' && React.createElement(CartPage),

        React.createElement(LoginModal),
        React.createElement(PaymentModal),

        React.createElement('footer', null,
            React.createElement('div', { className: 'footer-content' },
                React.createElement('h2', { className: 'footer-title' }, 'The Definitive Word'),
                React.createElement('p', { className: 'footer-tagline' }, 'Equipping believers through transformative resources'),
                React.createElement('p', { className: 'footer-copyright' }, 
                    `© ${new Date().getFullYear()} The Definitive Word. All rights reserved.`
                )
            )
        )
    );
}

// Render the app
ReactDOM.render(React.createElement(EbookStore), document.getElementById('root'));

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Definitive Word - Premium Ebook Store</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* ... (keep all existing CSS styles exactly as they are) ... */
        
        /* Additional styles for price and icon editing */
        .price-editable {
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .edit-mode-on .price-editable:hover {
            background: rgba(214, 158, 46, 0.25) !important;
            border-radius: 4px;
            padding: 2px 8px;
        }
        
        .icon-editable {
            position: relative;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .edit-mode-on .icon-editable:hover::after {
            content: '✏️';
            position: absolute;
            top: -5px;
            right: -5px;
            background: #d69e2e;
            color: #1a365d;
            border-radius: 50%;
            width: 20px;
            height: 20px;
            font-size: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .icon-selector {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 10px;
            margin-top: 15px;
            max-height: 200px;
            overflow-y: auto;
            padding: 10px;
            background: #f7fafc;
            border-radius: 8px;
        }
        
        .icon-option {
            padding: 10px;
            text-align: center;
            border: 2px solid #e2e8f0;
            border-radius: 6px;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .icon-option:hover {
            border-color: #d69e2e;
            background: rgba(214, 158, 46, 0.1);
        }
        
        .icon-option.selected {
            border-color: #d69e2e;
            background: rgba(214, 158, 46, 0.2);
        }
    </style>
</head>
<body>
    <!-- ... (keep all existing HTML exactly as it is) ... -->

    <script>
        // ... (keep all existing JavaScript code exactly as it is until the sample data section) ...

        // Enhanced sample data with icon support
        const sampleBooks = [
            {
                id: 1,
                title: "The Silent Observer",
                author: "Megan Foster", 
                price: 249.99,
                image: "https://images.unsplash.com/photo-1544947950-fa07a98d237f?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                badge: "Bestseller",
                description: "A psychological thriller that explores the depths of human consciousness.",
                icon: "fas fa-book"
            },
            {
                id: 2,
                title: "Digital Revolution",
                author: "Alex Chen",
                price: 299.99,
                image: "https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                badge: "New",
                description: "How technology is reshaping our world and what it means for the future.",
                icon: "fas fa-laptop"
            },
            {
                id: 3,
                title: "Business Mastery",
                author: "Sarah Johnson", 
                price: 349.99,
                image: "https://images.unsplash.com/photo-1512820790803-83ca734da794?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                badge: "Popular",
                description: "Essential strategies for entrepreneurial success in the modern economy.",
                icon: "fas fa-chart-line"
            },
            {
                id: 4,
                title: "African Skies",
                author: "Tendai Moyo", 
                price: 279.99,
                image: "https://images.unsplash.com/photo-1481627834876-b7833e8f5570?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                badge: "Local Author",
                description: "A captivating novel set against the backdrop of contemporary South Africa.",
                icon: "fas fa-globe-africa"
            },
            {
                id: 5,
                title: "Mindful Living",
                author: "James Wilson", 
                price: 229.99,
                image: "https://images.unsplash.com/photo-1506880018603-83d5b814b5a6?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                badge: "",
                description: "Practical techniques for finding peace and purpose in a busy world.",
                icon: "fas fa-spa"
            },
            {
                id: 6,
                title: "Culinary Journey",
                author: "Maria Rodriguez", 
                price: 319.99,
                image: "https://images.unsplash.com/photo-1544716278-ca5e3f4abd8c?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                badge: "Featured",
                description: "Explore world cuisines with these delicious and accessible recipes.",
                icon: "fas fa-utensils"
            }
        ];

        // Ministry books data with icons
        const ministryBooks = [
            {
                id: 101,
                title: "The Path to Spiritual Maturity",
                author: "Dr. Michael Johnson", 
                price: 299.99,
                image: "https://images.unsplash.com/photo-1544947950-fa07a98d237f?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                description: "A comprehensive guide to deepening your spiritual walk.",
                icon: "fas fa-pray"
            },
            {
                id: 102,
                title: "Prayer That Changes Everything",
                author: "Sarah Williams",
                price: 249.99,
                image: "https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                description: "Discover the power of prayer and how to develop a consistent prayer life.",
                icon: "fas fa-hands-praying"
            },
            {
                id: 103,
                title: "Biblical Leadership Principles",
                author: "Pastor David Chen", 
                price: 349.99,
                image: "https://images.unsplash.com/photo-1512820790803-83ca734da794?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                description: "Learn leadership skills and wisdom from the Bible.",
                icon: "fas fa-user-tie"
            },
            {
                id: 104,
                title: "Healing from Within",
                author: "Dr. Rebecca Martinez", 
                price: 279.99,
                image: "https://images.unsplash.com/photo-1481627834876-b7833e8f5570?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                description: "A Christian approach to emotional healing and overcoming past trauma.",
                icon: "fas fa-heart-circle-plus"
            },
            {
                id: 105,
                title: "The Generous Life",
                author: "Financial Ministry Team", 
                price: 229.99,
                image: "https://images.unsplash.com/photo-1506880018603-83d5b814b5a6?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                description: "Biblical principles for financial stewardship and generosity.",
                icon: "fas fa-hand-holding-heart"
            },
            {
                id: 106,
                title: "Family Foundations",
                author: "The Relationship Coaches", 
                price: 319.99,
                image: "https://images.unsplash.com/photo-1544716278-ca5e3f4abd8c?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                description: "Building strong Christian families through biblical values.",
                icon: "fas fa-house-chimney-heart"
            }
        ];

        // Available icons for easy selection
        const availableIcons = [
            'fas fa-book', 'fas fa-gem', 'fas fa-laptop', 'fas fa-chart-line', 
            'fas fa-globe-africa', 'fas fa-spa', 'fas fa-utensils', 'fas fa-pray',
            'fas fa-hands-praying', 'fas fa-user-tie', 'fas fa-heart-circle-plus',
            'fas fa-hand-holding-heart', 'fas fa-house-chimney-heart', 'fas fa-cross',
            'fas fa-bible', 'fas fa-hands-helping', 'fas fa-users', 'fas fa-seedling',
            'fas fa-graduation-cap', 'fas fa-heart', 'fas fa-star', 'fas fa-award',
            'fas fa-lightbulb', 'fas fa-compass', 'fas fa-shield-heart', 'fas fa-dove'
        ];

        // Enhanced setup edit interactions to include prices and icons
        function setupEditInteractions() {
            // Double-click to edit
            document.addEventListener('dblclick', function(e) {
                if (!editMode) return;
                
                const editable = e.target.closest('.editable');
                if (editable) {
                    e.preventDefault();
                    e.stopPropagation();
                    openEditModal(editable);
                }
                
                // Check if it's a price element
                const priceElement = e.target.closest('.price-editable');
                if (priceElement) {
                    e.preventDefault();
                    e.stopPropagation();
                    editPrice(priceElement);
                }
                
                // Check if it's an icon element
                const iconElement = e.target.closest('.icon-editable');
                if (iconElement) {
                    e.preventDefault();
                    e.stopPropagation();
                    editIcon(iconElement);
                }
            });

            // ... (keep the rest of the existing setupEditInteractions code) ...
        }

        // Function to edit price
        function editPrice(priceElement) {
            const currentPrice = priceElement.textContent.replace('R', '').trim();
            const newPrice = prompt('Enter new price (e.g., 249.99):', currentPrice);
            
            if (newPrice && !isNaN(parseFloat(newPrice))) {
                priceElement.textContent = `R${parseFloat(newPrice).toFixed(2)}`;
                
                // Update the data in our arrays
                updatePriceInData(priceElement.closest('.book-card, .ministry-book-card'), parseFloat(newPrice));
                saveAllContent();
                showNotification('Price updated successfully!');
            } else if (newPrice !== null) {
                showNotification('Please enter a valid price');
            }
        }

        // Function to update price in data arrays
        function updatePriceInData(element, newPrice) {
            const bookTitle = element.querySelector('.book-title, h4').textContent;
            
            // Find book in sampleBooks
            let book = sampleBooks.find(b => b.title === bookTitle);
            if (book) {
                book.price = newPrice;
                return;
            }
            
            // Find book in ministryBooks
            book = ministryBooks.find(b => b.title === bookTitle);
            if (book) {
                book.price = newPrice;
                return;
            }
            
            // Update program prices
            const programTitle = element.querySelector('h3')?.textContent;
            if (programTitle && element.closest('.program-card')) {
                // This would update program prices - you can extend this as needed
                showNotification('Program price updated in display');
            }
        }

        // Function to edit icon
        function editIcon(iconElement) {
            const currentIcon = iconElement.className;
            openIconSelector(iconElement);
        }

        // Function to open icon selector modal
        function openIconSelector(iconElement) {
            // Create icon selector modal
            const modal = document.createElement('div');
            modal.className = 'edit-modal active';
            modal.innerHTML = `
                <div class="modal-content">
                    <div class="modal-header">
                        <h2>Select Icon</h2>
                        <button class="close-modal" onclick="closeIconSelector()">&times;</button>
                    </div>
                    <div class="modal-body">
                        <div class="icon-selector" id="iconSelector">
                            ${availableIcons.map(icon => `
                                <div class="icon-option" data-icon="${icon}">
                                    <i class="${icon} fa-2x"></i>
                                    <div style="font-size: 0.8rem; margin-top: 5px;">${icon.replace('fas fa-', '')}</div>
                                </div>
                            `).join('')}
                        </div>
                    </div>
                    <div class="modal-footer">
                        <button class="modal-btn secondary" onclick="closeIconSelector()">Cancel</button>
                        <button class="modal-btn primary" onclick="saveIcon()">Save Icon</button>
                    </div>
                </div>
            `;
            
            document.body.appendChild(modal);
            
            // Store reference to the icon element being edited
            window.currentIconElement = iconElement;
            
            // Add click handlers for icon options
            document.querySelectorAll('.icon-option').forEach(option => {
                option.addEventListener('click', function() {
                    document.querySelectorAll('.icon-option').forEach(opt => opt.classList.remove('selected'));
                    this.classList.add('selected');
                    window.selectedIcon = this.getAttribute('data-icon');
                });
            });
        }

        // Function to close icon selector
        function closeIconSelector() {
            const modal = document.querySelector('.edit-modal');
            if (modal) {
                modal.remove();
            }
            window.currentIconElement = null;
            window.selectedIcon = null;
        }

        // Function to save selected icon
        function saveIcon() {
            if (window.currentIconElement && window.selectedIcon) {
                // Update the icon class
                window.currentIconElement.className = `icon-editable ${window.selectedIcon}`;
                
                // Update the data in our arrays
                updateIconInData(window.currentIconElement, window.selectedIcon);
                saveAllContent();
                showNotification('Icon updated successfully!');
            }
            closeIconSelector();
        }

        // Function to update icon in data arrays
        function updateIconInData(iconElement, newIcon) {
            const card = iconElement.closest('.book-card, .ministry-book-card, .ministry-feature, .program-card');
            if (!card) return;
            
            const title = card.querySelector('.book-title, h3, h4')?.textContent;
            if (!title) return;
            
            // Find in sampleBooks
            let item = sampleBooks.find(b => b.title === title);
            if (item) {
                item.icon = newIcon;
                return;
            }
            
            // Find in ministryBooks
            item = ministryBooks.find(b => b.title === title);
            if (item) {
                item.icon = newIcon;
                return;
            }
            
            // Find in ministry features
            if (card.classList.contains('ministry-feature')) {
                // Update ministry feature icons
                showNotification('Ministry feature icon updated in display');
            }
            
            // Find in program cards
            if (card.classList.contains('program-card')) {
                // Update program icons
                showNotification('Program icon updated in display');
            }
        }

        // Enhanced display functions with editable prices and icons
        function displayBooks() {
            const booksGrid = document.getElementById('booksGrid');
            booksGrid.innerHTML = '';
            
            sampleBooks.forEach(book => {
                const bookCard = document.createElement('div');
                bookCard.className = 'book-card';
                bookCard.innerHTML = `
                    <div class="book-cover">
                        <img src="${book.image}" alt="${book.title}">
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
                    </div>
                `;
                booksGrid.appendChild(bookCard);
            });
        }

        // Enhanced display ministry books with editable prices
        function displayMinistryBooks() {
            const ministryBooksTrack = document.getElementById('ministryBooksTrack');
            ministryBooksTrack.innerHTML = '';
            
            ministryBooks.forEach(book => {
                const bookCard = document.createElement('div');
                bookCard.className = 'ministry-book-card';
                bookCard.innerHTML = `
                    <div class="book-cover-small">
                        <img src="${book.image}" alt="${book.title}">
                    </div>
                    <h4>${book.title}</h4>
                    <p>by ${book.author}</p>
                    <p class="book-description">${book.description}</p>
                    <div class="book-price-small price-editable">R${book.price.toFixed(2)}</div>
                    <button class="btn" style="width: 100%; padding: 10px;" onclick="addToCart(${book.id})">
                        <i class="fas fa-cart-plus"></i> Add to Cart
                    </button>
                `;
                ministryBooksTrack.appendChild(bookCard);
            });
        }

        // Enhanced ministry features with editable icons
        function initMinistrySection() {
            displayMinistryBooks();
            setupMinistryIcons();
        }

        // Setup ministry section icons to be editable
        function setupMinistryIcons() {
            // Make ministry feature icons editable
            document.querySelectorAll('.ministry-feature i').forEach(icon => {
                icon.classList.add('icon-editable');
            });
            
            // Make program card icons editable
            document.querySelectorAll('.program-header i').forEach(icon => {
                icon.classList.add('icon-editable');
            });
        }

        // Enhanced add to cart to use updated prices
        function addToCart(bookId) {
            const allBooks = [...sampleBooks, ...ministryBooks];
            const book = allBooks.find(b => b.id === bookId);
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
                
                saveCart();
                updateCartDisplay();
                showNotification(`"${book.title}" added to cart!`);
            }
        }

        // Enhanced update cart display to show current prices
        function updateCartDisplay() {
            const cartCount = document.getElementById('cartCount');
            const cartItems = document.getElementById('cartItems');
            const cartTotal = document.getElementById('cartTotal');
            
            // Update cart count
            const totalItems = cart.reduce((sum, item) => sum + item.quantity, 0);
            cartCount.textContent = totalItems;
            
            // Update cart items
            cartItems.innerHTML = '';
            let total = 0;
            
            cart.forEach(item => {
                const itemTotal = item.price * item.quantity;
                total += itemTotal;
                
                const cartItem = document.createElement('div');
                cartItem.className = 'cart-item';
                cartItem.innerHTML = `
                    <img src="${item.image}" alt="${item.title}">
                    <div class="cart-item-details">
                        <div class="cart-item-title">${item.title}</div>
                        <div class="cart-item-author">by ${item.author}</div>
                        <div class="cart-item-price">R${item.price.toFixed(2)} × ${item.quantity}</div>
                    </div>
                    <button class="cart-item-remove" onclick="removeFromCart(${item.id})">
                        <i class="fas fa-trash"></i>
                    </button>
                `;
                cartItems.appendChild(cartItem);
            });
            
            // Update total
            cartTotal.textContent = `R${total.toFixed(2)}`;
        }

        // Enhanced initialization
        function initApp() {
            loadAllContent();
            displayBooks();
            setupNavigation();
            setupEditInteractions();
            loadCart();
            loadCommunityData();
            loadBlogData();
            initMinistrySection();
            updateCartDisplay();
            showNotification('💡 Pro Tip: Double-click any price to edit it, or double-click icons to change them');
        }

        // ... (keep all other existing JavaScript functions exactly as they are) ...
    </script>
</body>
</html>

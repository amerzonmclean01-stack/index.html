// ==================== COMPLETE WEBSITE FUNCTIONALITY ====================
// Add this script section right before the closing </body> tag, or integrate with existing script

// System State Management
const websiteState = {
    // Content management
    editableContent: {
        // Hero section
        hero: {
            title: "Welcome to The Definitive Word",
            subtitle: "Your Destiny Has Been Written",
            description: "Discover God's plan for your life through prophetic teaching, life coaching, and transformative resources",
            buttons: [
                { text: "Explore Our Resources", link: "#ebooks", style: "primary" },
                { text: "Get In Touch", link: "#contact", style: "secondary" }
            ]
        },
        
        // E-books
        ebooks: [
            {
                id: 1,
                title: "Unveiling Your Destiny",
                description: "A comprehensive guide to discovering and walking in your God-given purpose. Learn to recognize divine opportunities and align your life with God's plan.",
                price: 349.99,
                oldPrice: 449.99,
                badge: "Bestseller",
                icon: "fas fa-book-open"
            },
            {
                id: 2,
                title: "Prophetic Insights",
                description: "Understanding the prophetic voice in the modern church and your personal life. Develop discernment and learn to apply prophetic wisdom daily.",
                price: 449.99,
                oldPrice: null,
                badge: "New Release",
                icon: "fas fa-dove"
            },
            {
                id: 3,
                title: "The Written Word",
                description: "Exploring the power of God's promises and declarations over your life. Unlock the transformative power of Scripture in your daily walk.",
                price: 299.99,
                oldPrice: 399.99,
                badge: null,
                icon: "fas fa-bible"
            }
        ],
        
        // Coaching section
        coaching: {
            title: "Transform Your Life Through Prophetic Coaching",
            description: "Our life coaching program combines biblical principles with practical strategies to help you:",
            points: [
                "Discover your divine purpose and calling",
                "Overcome obstacles and limiting beliefs",
                "Develop spiritual disciplines and growth",
                "Create actionable plans for your goals",
                "Walk in the fullness of your destiny"
            ],
            buttonText: "Book a Session"
        },
        
        // Blog posts
        blogPosts: [
            {
                id: 1,
                title: "Walking in Your Prophetic Purpose",
                date: "November 20, 2025",
                description: "Discovering how to align your daily life with the prophetic words spoken over you and recognizing divine appointments."
            },
            {
                id: 2,
                title: "The Power of Declared Destiny",
                date: "November 15, 2025",
                description: "Understanding how God's written word over your life shapes your future and learning to speak life into your circumstances."
            },
            {
                id: 3,
                title: "Breaking Through Limitations",
                date: "November 10, 2025",
                description: "Practical steps to overcome the barriers standing between you and your destiny through faith and strategic action."
            }
        ],
        
        // Workshops
        workshops: [
            {
                id: 4,
                title: "Prophetic Activation Workshop",
                description: "A powerful one-day intensive designed to activate and strengthen your prophetic gifting. Learn to hear God's voice clearly and minister prophetically with confidence.",
                day: "15",
                month: "DEC 2025",
                location: "Virtual (Zoom)",
                time: "9:00 AM - 4:00 PM",
                price: 599.99
            },
            {
                id: 5,
                title: "Destiny Mapping Masterclass",
                description: "Discover God's blueprint for your life and create a practical roadmap to walk in your divine purpose. Limited to 20 participants for personalized attention.",
                day: "22",
                month: "JAN 2026",
                location: "Cape Town, South Africa",
                time: "6:00 PM - 9:00 PM",
                price: 799.99
            }
        ],
        
        // Ministry items
        ministry: [
            { title: "Teaching", description: "Biblical and prophetic instruction for spiritual growth and understanding.", icon: "fas fa-book-open" },
            { title: "Prayer", description: "Intercessory and prophetic prayer for breakthrough and direction.", icon: "fas fa-hands-praying" },
            { title: "Coaching", description: "Personal transformation guidance for walking in divine purpose.", icon: "fas fa-user-graduate" },
            { title: "Community", description: "Building connections with like-minded believers on the same journey.", icon: "fas fa-people-group" }
        ],
        
        // Testimonials
        testimonials: [
            {
                name: "Sarah Mitchell",
                role: "Life Coaching Client",
                text: "\"The Definitive Word Ministry completely transformed my understanding of God's plan for my life. The prophetic insights I received gave me clarity and direction I had been seeking for years.\"",
                initials: "SM"
            },
            {
                name: "Michael Johnson",
                role: "Workshop Attendee",
                text: "\"The e-books and workshops provided practical tools that helped me break through spiritual barriers. I'm now walking confidently in my calling with a clear sense of purpose.\"",
                initials: "MJ"
            },
            {
                name: "Rebecca Davis",
                role: "Ministry Partner",
                text: "\"The prophetic activation workshop was life-changing! I learned to recognize God's voice more clearly and now feel equipped to minister to others with confidence and accuracy.\"",
                initials: "RD"
            }
        ],
        
        // Contact info
        contact: {
            address: "123 Prophetic Way, Divine City, DC 12345",
            phone: "+27 (0)21 123 4567",
            email: "info@definitiveword.org",
            hours: "Monday - Friday: 9am - 5pm"
        },
        
        // Footer
        footer: {
            description: "Your Destiny Has Been Written. We're dedicated to helping you discover and walk in God's perfect plan for your life.",
            copyright: "© 2025 The Definitive Word Ministry. Your Destiny Has Been Written.",
            tagline: "Walking in prophetic purpose since 2025"
        }
    },
    
    // User preferences
    userPreferences: {
        theme: 'light',
        fontSize: 'medium',
        notifications: true
    },
    
    // Editing state
    isEditing: false,
    currentEditSection: null
};

// ==================== EDITING MODE FUNCTIONALITY ====================
function toggleEditMode() {
    websiteState.isEditing = !websiteState.isEditing;
    
    if (websiteState.isEditing) {
        enableEditMode();
        showToast("Edit mode enabled. Click on any text to edit.", "info");
    } else {
        disableEditMode();
        showToast("Edit mode disabled. Changes saved.", "success");
    }
    
    updateEditModeUI();
}

function enableEditMode() {
    // Add edit indicators to editable elements
    document.querySelectorAll('.editable').forEach(element => {
        element.classList.add('editable-active');
        element.setAttribute('contenteditable', 'true');
        element.addEventListener('blur', handleContentEdit);
        element.addEventListener('keydown', handleEditKeydown);
    });
    
    // Show edit controls
    document.getElementById('editControls')?.style.display = 'flex';
    
    // Add save button to header if not exists
    if (!document.getElementById('editModeToggle')) {
        const editButton = document.createElement('button');
        editButton.id = 'editModeToggle';
        editButton.className = 'auth-button';
        editButton.innerHTML = '<i class="fas fa-edit"></i> Edit Mode';
        editButton.onclick = toggleEditMode;
        
        const headerRight = document.querySelector('.header-right');
        headerRight.insertBefore(editButton, headerRight.firstChild);
    }
}

function disableEditMode() {
    // Remove edit indicators
    document.querySelectorAll('.editable').forEach(element => {
        element.classList.remove('editable-active');
        element.removeAttribute('contenteditable');
        element.removeEventListener('blur', handleContentEdit);
        element.removeEventListener('keydown', handleEditKeydown);
    });
    
    // Hide edit controls
    document.getElementById('editControls')?.style.display = 'none';
    
    // Save content to localStorage
    saveContentToStorage();
}

function updateEditModeUI() {
    const editButton = document.getElementById('editModeToggle');
    if (editButton) {
        if (websiteState.isEditing) {
            editButton.innerHTML = '<i class="fas fa-save"></i> Save & Exit';
            editButton.style.background = 'var(--success)';
        } else {
            editButton.innerHTML = '<i class="fas fa-edit"></i> Edit Mode';
            editButton.style.background = '';
        }
    }
}

function handleContentEdit(event) {
    const element = event.target;
    const section = element.closest('section')?.id || element.closest('.editable-section')?.dataset.section;
    const field = element.dataset.field;
    
    if (section && field) {
        // Update the state
        updateContentState(section, field, element.textContent);
    }
}

function handleEditKeydown(event) {
    // Allow Enter to create new line in textareas, but prevent in other elements
    if (event.key === 'Enter' && !event.target.matches('textarea, [contenteditable="true"][data-multiline]')) {
        event.preventDefault();
        event.target.blur();
    }
}

function updateContentState(section, field, value) {
    // Navigate through the state object to update the correct field
    const path = section.split('-');
    let current = websiteState.editableContent;
    
    for (let i = 0; i < path.length - 1; i++) {
        current = current[path[i]];
    }
    
    current[field] = value;
}

function saveContentToStorage() {
    try {
        localStorage.setItem('definitiveWordContent', JSON.stringify(websiteState.editableContent));
        localStorage.setItem('definitiveWordUserPrefs', JSON.stringify(websiteState.userPreferences));
        console.log('Content saved to localStorage');
    } catch (error) {
        console.error('Error saving content:', error);
        showToast('Error saving content. Please try again.', 'error');
    }
}

function loadContentFromStorage() {
    try {
        const savedContent = localStorage.getItem('definitiveWordContent');
        const savedPrefs = localStorage.getItem('definitiveWordUserPrefs');
        
        if (savedContent) {
            websiteState.editableContent = JSON.parse(savedContent);
        }
        
        if (savedPrefs) {
            websiteState.userPreferences = JSON.parse(savedPrefs);
            applyUserPreferences();
        }
    } catch (error) {
        console.error('Error loading content:', error);
    }
}

// ==================== CONTENT MANAGEMENT SYSTEM ====================
class ContentManager {
    constructor() {
        this.initializeEditableElements();
        this.setupDragAndDrop();
        this.setupImageUpload();
    }
    
    initializeEditableElements() {
        // Mark all content areas as editable
        const editableSelectors = [
            'h1', 'h2', 'h3', 'h4', 'p.description', '.blog-post h3',
            '.blog-post p:not(.blog-date)', '.ebook-content h3',
            '.ebook-content p', '.coaching-text h3', '.coaching-text li',
            '.workshop-details h3', '.workshop-details p', '.ministry-item h3',
            '.ministry-item p', '.testimonial-text', '.author-info h4',
            '.contact-info p', '.footer-column p', '.copyright'
        ];
        
        editableSelectors.forEach(selector => {
            document.querySelectorAll(selector).forEach(element => {
                element.classList.add('editable');
                
                // Add data attributes for identification
                const section = element.closest('section')?.id || 'global';
                const field = this.generateFieldName(element);
                element.dataset.section = section;
                element.dataset.field = field;
            });
        });
    }
    
    generateFieldName(element) {
        // Generate a meaningful field name based on element type and context
        const tag = element.tagName.toLowerCase();
        const parentId = element.parentElement.id || element.parentElement.className;
        const text = element.textContent.substring(0, 20).toLowerCase().replace(/\s+/g, '_');
        
        return `${tag}_${parentId}_${text}`;
    }
    
    setupDragAndDrop() {
        // Enable drag and drop for reordering sections
        const draggableSections = document.querySelectorAll('.ebook-card, .blog-post, .ministry-item');
        
        draggableSections.forEach(section => {
            section.draggable = true;
            section.addEventListener('dragstart', this.handleDragStart);
            section.addEventListener('dragover', this.handleDragOver);
            section.addEventListener('drop', this.handleDrop);
            section.addEventListener('dragend', this.handleDragEnd);
        });
    }
    
    handleDragStart(event) {
        event.dataTransfer.setData('text/plain', event.target.id || event.target.dataset.id);
        event.target.classList.add('dragging');
    }
    
    handleDragOver(event) {
        event.preventDefault();
        const draggingElement = document.querySelector('.dragging');
        const afterElement = this.getDragAfterElement(event.currentTarget, event.clientY);
        
        if (afterElement) {
            event.currentTarget.insertBefore(draggingElement, afterElement);
        } else {
            event.currentTarget.appendChild(draggingElement);
        }
    }
    
    getDragAfterElement(container, y) {
        const draggableElements = [...container.querySelectorAll('.draggable:not(.dragging)')];
        
        return draggableElements.reduce((closest, child) => {
            const box = child.getBoundingClientRect();
            const offset = y - box.top - box.height / 2;
            
            if (offset < 0 && offset > closest.offset) {
                return { offset: offset, element: child };
            } else {
                return closest;
            }
        }, { offset: Number.NEGATIVE_INFINITY }).element;
    }
    
    handleDrop(event) {
        event.preventDefault();
        const id = event.dataTransfer.getData('text/plain');
        const draggedElement = document.getElementById(id) || document.querySelector(`[data-id="${id}"]`);
        
        if (draggedElement) {
            event.currentTarget.appendChild(draggedElement);
            showToast('Section reordered successfully', 'success');
        }
    }
    
    handleDragEnd(event) {
        event.target.classList.remove('dragging');
    }
    
    setupImageUpload() {
        // Add image upload functionality to image containers
        const imageContainers = document.querySelectorAll('.ebook-image, .coaching-image, .author-avatar');
        
        imageContainers.forEach(container => {
            container.addEventListener('click', () => {
                if (websiteState.isEditing) {
                    this.uploadImage(container);
                }
            });
            
            // Add upload indicator when in edit mode
            container.classList.add('image-uploadable');
        });
    }
    
    uploadImage(container) {
        const input = document.createElement('input');
        input.type = 'file';
        input.accept = 'image/*';
        
        input.onchange = (event) => {
            const file = event.target.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = (e) => {
                    container.style.backgroundImage = `url(${e.target.result})`;
                    container.innerHTML = ''; // Remove icon
                    showToast('Image uploaded successfully', 'success');
                };
                reader.readAsDataURL(file);
            }
        };
        
        input.click();
    }
    
    // Export content as JSON
    exportContent() {
        const dataStr = JSON.stringify(websiteState.editableContent, null, 2);
        const dataUri = 'data:application/json;charset=utf-8,'+ encodeURIComponent(dataStr);
        
        const exportFileDefaultName = 'definitive-word-content.json';
        
        const linkElement = document.createElement('a');
        linkElement.setAttribute('href', dataUri);
        linkElement.setAttribute('download', exportFileDefaultName);
        linkElement.click();
        
        showToast('Content exported successfully', 'success');
    }
    
    // Import content from JSON
    importContent() {
        const input = document.createElement('input');
        input.type = 'file';
        input.accept = '.json';
        
        input.onchange = (event) => {
            const file = event.target.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = (e) => {
                    try {
                        const importedContent = JSON.parse(e.target.result);
                        Object.assign(websiteState.editableContent, importedContent);
                        this.updateAllContent();
                        showToast('Content imported successfully', 'success');
                    } catch (error) {
                        showToast('Error importing content. Invalid file format.', 'error');
                    }
                };
                reader.readAsText(file);
            }
        };
        
        input.click();
    }
    
    updateAllContent() {
        // This function would update all content on the page from the state
        // Implementation would update each section based on websiteState.editableContent
        console.log('Updating all content from state...');
        // Add your content update logic here
    }
}

// ==================== ENHANCED E-COMMERCE FUNCTIONALITY ====================
class EnhancedECommerce extends ECommerceSystem {
    constructor() {
        super();
        this.initEnhancedFeatures();
    }
    
    initEnhancedFeatures() {
        this.setupWishlist();
        this.setupProductReviews();
        this.setupDiscountCodes();
    }
    
    setupWishlist() {
        this.wishlist = JSON.parse(localStorage.getItem('definitiveWordWishlist')) || [];
        this.updateWishlistUI();
    }
    
    addToWishlist(id, title) {
        if (!this.wishlist.some(item => item.id === id)) {
            this.wishlist.push({ id, title, date: new Date().toISOString() });
            localStorage.setItem('definitiveWordWishlist', JSON.stringify(this.wishlist));
            this.updateWishlistUI();
            this.showToast(`"${title}" added to wishlist`, 'success');
        }
    }
    
    removeFromWishlist(id) {
        this.wishlist = this.wishlist.filter(item => item.id !== id);
        localStorage.setItem('definitiveWordWishlist', JSON.stringify(this.wishlist));
        this.updateWishlistUI();
        this.showToast('Item removed from wishlist', 'info');
    }
    
    updateWishlistUI() {
        const wishlistBtn = document.getElementById('wishlistBtn');
        if (wishlistBtn) {
            const count = this.wishlist.length;
            wishlistBtn.innerHTML = `<i class="fas fa-heart"></i>${count > 0 ? ` ${count}` : ''}`;
        }
    }
    
    setupProductReviews() {
        this.reviews = JSON.parse(localStorage.getItem('definitiveWordReviews')) || {};
    }
    
    addReview(productId, rating, comment) {
        if (!this.reviews[productId]) {
            this.reviews[productId] = [];
        }
        
        this.reviews[productId].push({
            user: this.currentUser?.name || 'Anonymous',
            rating: rating,
            comment: comment,
            date: new Date().toISOString()
        });
        
        localStorage.setItem('definitiveWordReviews', JSON.stringify(this.reviews));
        this.showToast('Review submitted successfully', 'success');
    }
    
    setupDiscountCodes() {
        this.discountCodes = {
            'WELCOME10': 10,
            'DESTINY25': 25,
            'PROPHETIC50': 50
        };
    }
    
    applyDiscount(code) {
        const discount = this.discountCodes[code.toUpperCase()];
        if (discount) {
            const total = this.getCartTotal();
            const discountAmount = (total * discount) / 100;
            const newTotal = total - discountAmount;
            
            this.showToast(`Discount applied! Saved R${discountAmount.toFixed(2)}`, 'success');
            return newTotal;
        } else {
            this.showToast('Invalid discount code', 'error');
            return this.getCartTotal();
        }
    }
}

// ==================== ADMIN DASHBOARD ====================
function openAdminDashboard() {
    if (!ecommerce.currentUser) {
        showToast('Please login to access admin dashboard', 'warning');
        openAuthModal();
        return;
    }
    
    const dashboardHTML = `
        <div class="dashboard-modal">
            <div class="dashboard-content" style="max-width: 800px;">
                <div class="dashboard-header">
                    <h3><i class="fas fa-cogs"></i> Admin Dashboard</h3>
                    <button class="close-dashboard" onclick="closeAdminDashboard()">&times;</button>
                </div>
                <div class="dashboard-body">
                    <div class="modal-tabs" style="margin-bottom: 2rem;">
                        <div class="modal-tab active" onclick="switchAdminTab('content')">Content</div>
                        <div class="modal-tab" onclick="switchAdminTab('products')">Products</div>
                        <div class="modal-tab" onclick="switchAdminTab('analytics')">Analytics</div>
                        <div class="modal-tab" onclick="switchAdminTab('users')">Users</div>
                    </div>
                    
                    <div id="adminContentTab" class="admin-tab active">
                        <h4>Content Management</h4>
                        <div class="admin-actions">
                            <button class="cta-button small" onclick="contentManager.exportContent()">
                                <i class="fas fa-download"></i> Export Content
                            </button>
                            <button class="cta-button small outline" onclick="contentManager.importContent()">
                                <i class="fas fa-upload"></i> Import Content
                            </button>
                            <button class="cta-button small" onclick="toggleEditMode()">
                                <i class="fas fa-edit"></i> ${websiteState.isEditing ? 'Disable' : 'Enable'} Edit Mode
                            </button>
                        </div>
                        
                        <div class="content-stats" style="margin-top: 2rem;">
                            <h5>Content Statistics</h5>
                            <div class="stats-grid">
                                <div class="stat-card">
                                    <div class="stat-value">${websiteState.editableContent.ebooks.length}</div>
                                    <div class="stat-label">E-books</div>
                                </div>
                                <div class="stat-card">
                                    <div class="stat-value">${websiteState.editableContent.blogPosts.length}</div>
                                    <div class="stat-label">Blog Posts</div>
                                </div>
                                <div class="stat-card">
                                    <div class="stat-value">${websiteState.editableContent.testimonials.length}</div>
                                    <div class="stat-label">Testimonials</div>
                                </div>
                                <div class="stat-card">
                                    <div class="stat-value">${websiteState.editableContent.workshops.length}</div>
                                    <div class="stat-label">Workshops</div>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <div id="adminProductsTab" class="admin-tab">
                        <h4>Product Management</h4>
                        <button class="cta-button small" onclick="addNewProduct()">
                            <i class="fas fa-plus"></i> Add New Product
                        </button>
                        
                        <div class="products-list" style="margin-top: 1rem;">
                            ${websiteState.editableContent.ebooks.map(ebook => `
                                <div class="product-item">
                                    <strong>${ebook.title}</strong>
                                    <div>R${ebook.price.toFixed(2)}</div>
                                    <div class="product-actions">
                                        <button class="download-btn small" onclick="editProduct(${ebook.id})">Edit</button>
                                        <button class="download-btn small" onclick="deleteProduct(${ebook.id})" style="background: var(--prophetic-red);">Delete</button>
                                    </div>
                                </div>
                            `).join('')}
                        </div>
                    </div>
                    
                    <div id="adminAnalyticsTab" class="admin-tab">
                        <h4>Website Analytics</h4>
                        <p>Coming soon: Detailed analytics dashboard</p>
                    </div>
                    
                    <div id="adminUsersTab" class="admin-tab">
                        <h4>User Management</h4>
                        <p>Total Registered Users: <strong>${Object.keys(JSON.parse(localStorage.getItem('definitiveWordUsers') || '{}')).length}</strong></p>
                    </div>
                </div>
            </div>
        </div>
    `;
    
    // Create and show admin dashboard
    const existingAdmin = document.getElementById('adminDashboard');
    if (existingAdmin) {
        existingAdmin.remove();
    }
    
    const adminDiv = document.createElement('div');
    adminDiv.id = 'adminDashboard';
    adminDiv.innerHTML = dashboardHTML;
    document.body.appendChild(adminDiv);
    
    // Show the dashboard
    document.querySelector('#adminDashboard .dashboard-modal').style.display = 'block';
}

function closeAdminDashboard() {
    const adminDashboard = document.getElementById('adminDashboard');
    if (adminDashboard) {
        adminDashboard.remove();
    }
}

function switchAdminTab(tabName) {
    // Hide all tabs
    document.querySelectorAll('.admin-tab').forEach(tab => {
        tab.classList.remove('active');
    });
    
    // Remove active class from all tab buttons
    document.querySelectorAll('.modal-tab').forEach(tab => {
        tab.classList.remove('active');
    });
    
    // Show selected tab
    document.getElementById(`admin${tabName.charAt(0).toUpperCase() + tabName.slice(1)}Tab`).classList.add('active');
    
    // Activate tab button
    const tabButtons = document.querySelectorAll('.modal-tab');
    Array.from(tabButtons).find(button => button.textContent.toLowerCase().includes(tabName)).classList.add('active');
}

// ==================== ADDITIONAL STYLES ====================
const additionalStyles = `
    /* Edit Mode Styles */
    .editable {
        position: relative;
        transition: all 0.3s ease;
    }
    
    .editable-active {
        outline: 2px dashed rgba(30, 58, 138, 0.3);
        background-color: rgba(30, 58, 138, 0.05);
        padding: 4px 8px;
        border-radius: 4px;
        cursor: text;
    }
    
    .editable-active:hover {
        background-color: rgba(30, 58, 138, 0.1);
    }
    
    .editable-active:focus {
        outline: 2px solid var(--prophetic-blue);
        background-color: rgba(30, 58, 138, 0.15);
    }
    
    /* Image upload indicators */
    .image-uploadable {
        cursor: pointer;
        position: relative;
    }
    
    .image-uploadable:after {
        content: '📷 Click to change image';
        position: absolute;
        bottom: 10px;
        left: 0;
        right: 0;
        background: rgba(0, 0, 0, 0.7);
        color: white;
        padding: 5px;
        font-size: 0.8rem;
        opacity: 0;
        transition: opacity 0.3s;
    }
    
    .image-uploadable:hover:after {
        opacity: 1;
    }
    
    /* Draggable elements */
    .draggable {
        cursor: move;
        transition: transform 0.3s;
    }
    
    .dragging {
        opacity: 0.5;
        transform: rotate(2deg);
    }
    
    /* Edit Controls */
    #editControls {
        position: fixed;
        bottom: 20px;
        right: 20px;
        background: white;
        padding: 15px;
        border-radius: 10px;
        box-shadow: var(--shadow-lg);
        z-index: 10000;
        display: none;
        flex-direction: column;
        gap: 10px;
        max-width: 300px;
    }
    
    .edit-control-group {
        display: flex;
        gap: 10px;
        flex-wrap: wrap;
    }
    
    /* Admin Dashboard Styles */
    .admin-tab {
        display: none;
    }
    
    .admin-tab.active {
        display: block;
    }
    
    .admin-actions {
        display: flex;
        gap: 10px;
        flex-wrap: wrap;
    }
    
    .stats-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
        gap: 15px;
        margin-top: 15px;
    }
    
    .stat-card {
        background: var(--light-gray);
        padding: 20px;
        border-radius: 8px;
        text-align: center;
        border: 1px solid var(--medium-gray);
    }
    
    .stat-value {
        font-size: 2rem;
        font-weight: bold;
        color: var(--prophetic-blue);
    }
    
    .stat-label {
        color: var(--text-dark);
        font-size: 0.9rem;
        margin-top: 5px;
    }
    
    .product-item {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 10px;
        border-bottom: 1px solid var(--medium-gray);
    }
    
    .product-actions {
        display: flex;
        gap: 5px;
    }
    
    /* Wishlist button */
    #wishlistBtn {
        background: none;
        border: none;
        color: var(--white);
        font-size: 1.3rem;
        cursor: pointer;
        transition: var(--transition);
        position: relative;
    }
    
    #wishlistBtn:hover {
        color: var(--prophetic-red);
    }
    
    .wishlist-count {
        position: absolute;
        top: -8px;
        right: -8px;
        background: var(--prophetic-red);
        color: white;
        font-size: 0.7rem;
        padding: 2px 6px;
        border-radius: 50%;
        min-width: 18px;
        text-align: center;
    }
    
    /* Enhanced cart */
    .cart-actions .discount-section {
        margin-bottom: 1rem;
        padding: 1rem;
        background: var(--light-gray);
        border-radius: 8px;
    }
    
    .discount-input {
        display: flex;
        gap: 0.5rem;
        margin-top: 0.5rem;
    }
    
    .discount-input input {
        flex: 1;
        padding: 0.5rem;
        border: 1px solid var(--medium-gray);
        border-radius: 4px;
    }
    
    .discount-input button {
        background: var(--prophetic-blue);
        color: white;
        border: none;
        padding: 0.5rem 1rem;
        border-radius: 4px;
        cursor: pointer;
    }
    
    /* Review system */
    .review-form {
        margin-top: 2rem;
        padding: 1.5rem;
        background: var(--light-gray);
        border-radius: 8px;
    }
    
    .review-form textarea {
        width: 100%;
        min-height: 100px;
        padding: 0.5rem;
        border: 1px solid var(--medium-gray);
        border-radius: 4px;
        margin-bottom: 1rem;
    }
    
    .star-rating {
        display: flex;
        gap: 0.5rem;
        margin-bottom: 1rem;
    }
    
    .star-rating i {
        font-size: 1.5rem;
        color: var(--medium-gray);
        cursor: pointer;
        transition: color 0.3s;
    }
    
    .star-rating i:hover,
    .star-rating i.active {
        color: var(--gold);
    }
`;

// Add styles to document
const styleSheet = document.createElement("style");
styleSheet.textContent = additionalStyles;
document.head.appendChild(styleSheet);

// ==================== INITIALIZATION ====================
document.addEventListener('DOMContentLoaded', function() {
    // Load saved content
    loadContentFromStorage();
    
    // Initialize content manager
    const contentManager = new ContentManager();
    
    // Initialize enhanced e-commerce
    const enhancedEcommerce = new EnhancedECommerce();
    
    // Add wishlist button to header
    const wishlistBtn = document.createElement('button');
    wishlistBtn.id = 'wishlistBtn';
    wishlistBtn.innerHTML = '<i class="far fa-heart"></i>';
    wishlistBtn.title = 'Wishlist';
    wishlistBtn.onclick = () => {
        if (!enhancedEcommerce.currentUser) {
            showToast('Please login to view wishlist', 'warning');
            openAuthModal();
            return;
        }
        openWishlist();
    };
    
    const headerRight = document.querySelector('.header-right');
    if (headerRight) {
        headerRight.insertBefore(wishlistBtn, headerRight.querySelector('.cart-icon'));
    }
    
    // Add admin button for logged-in users (simulating admin)
    const checkForAdmin = () => {
        if (enhancedEcommerce.currentUser) {
            const adminBtn = document.createElement('button');
            adminBtn.className = 'auth-button';
            adminBtn.innerHTML = '<i class="fas fa-cogs"></i> Admin';
            adminBtn.onclick = openAdminDashboard;
            adminBtn.style.background = 'var(--gold)';
            adminBtn.style.color = 'var(--dark-gray)';
            
            const userInfo = document.getElementById('userInfo');
            if (userInfo && !document.querySelector('.admin-btn')) {
                userInfo.insertBefore(adminBtn, userInfo.querySelector('.auth-button'));
            }
        }
    };
    
    // Check for admin periodically
    setInterval(checkForAdmin, 5000);
    
    // Create edit controls
    const editControls = document.createElement('div');
    editControls.id = 'editControls';
    editControls.innerHTML = `
        <div style="margin-bottom: 10px;">
            <strong><i class="fas fa-edit"></i> Edit Mode Active</strong>
            <p style="font-size: 0.8rem; margin-top: 5px;">Click on any text to edit. Changes are saved automatically.</p>
        </div>
        <div class="edit-control-group">
            <button class="cta-button small" onclick="toggleEditMode()">
                <i class="fas fa-save"></i> Save & Exit
            </button>
            <button class="cta-button small outline" onclick="contentManager.exportContent()">
                <i class="fas fa-download"></i> Export
            </button>
        </div>
    `;
    document.body.appendChild(editControls);
    
    // Add keyboard shortcut for edit mode (Ctrl+E)
    document.addEventListener('keydown', function(event) {
        if (event.ctrlKey && event.key === 'e') {
            event.preventDefault();
            toggleEditMode();
        }
    });
    
    console.log('Enhanced website functionality loaded!');
    console.log('Edit Mode: Press Ctrl+E to toggle');
    console.log('Admin Dashboard: Available for logged-in users');
    console.log('Content Management: Fully operational');
});

// ==================== ADDITIONAL FUNCTIONS ====================
function openWishlist() {
    const wishlistModal = document.createElement('div');
    wishlistModal.className = 'modal';
    wishlistModal.innerHTML = `
        <div class="modal-content">
            <span class="close-modal" onclick="this.closest('.modal').remove()">&times;</span>
            <h3><i class="fas fa-heart"></i> My Wishlist</h3>
            <div id="wishlistItems">
                ${enhancedEcommerce?.wishlist?.map(item => `
                    <div class="cart-item">
                        <div class="cart-item-info">
                            <h4>${item.title}</h4>
                        </div>
                        <div>
                            <button class="download-btn small" onclick="addToCart(${item.id}, '${item.title}', ${websiteState.editableContent.ebooks.find(e => e.id === item.id)?.price || 0})">
                                Add to Cart
                            </button>
                            <button class="download-btn small" onclick="enhancedEcommerce.removeFromWishlist(${item.id})" style="background: var(--prophetic-red);">
                                Remove
                            </button>
                        </div>
                    </div>
                `).join('') || '<p>Your wishlist is empty</p>'}
            </div>
        </div>
    `;
    
    document.body.appendChild(wishlistModal);
    wishlistModal.style.display = 'flex';
}

function addNewProduct() {
    const title = prompt('Enter product title:');
    if (!title) return;
    
    const price = parseFloat(prompt('Enter product price (R):'));
    if (isNaN(price)) return;
    
    const description = prompt('Enter product description:');
    if (!description) return;
    
    const newProduct = {
        id: Date.now(),
        title: title,
        description: description,
        price: price,
        oldPrice: null,
        badge: null,
        icon: 'fas fa-book'
    };
    
    websiteState.editableContent.ebooks.push(newProduct);
    saveContentToStorage();
    showToast('Product added successfully', 'success');
    closeAdminDashboard();
    openAdminDashboard(); // Refresh
}

function editProduct(id) {
    const product = websiteState.editableContent.ebooks.find(e => e.id === id);
    if (!product) return;
    
    product.title = prompt('Edit title:', product.title) || product.title;
    product.description = prompt('Edit description:', product.description) || product.description;
    product.price = parseFloat(prompt('Edit price:', product.price)) || product.price;
    
    saveContentToStorage();
    showToast('Product updated successfully', 'success');
    closeAdminDashboard();
    openAdminDashboard(); // Refresh
}

function deleteProduct(id) {
    if (confirm('Are you sure you want to delete this product?')) {
        websiteState.editableContent.ebooks = websiteState.editableContent.ebooks.filter(e => e.id !== id);
        saveContentToStorage();
        showToast('Product deleted successfully', 'success');
        closeAdminDashboard();
        openAdminDashboard(); // Refresh
    }
}

function applyUserPreferences() {
    const prefs = websiteState.userPreferences;
    
    // Apply theme
    if (prefs.theme === 'dark') {
        document.body.classList.add('dark-theme');
    }
    
    // Apply font size
    document.body.style.fontSize = {
        'small': '14px',
        'medium': '16px',
        'large': '18px'
    }[prefs.fontSize] || '16px';
}

// Global function to show toast (compatible with existing code)
function showToast(message, type = 'success') {
    // Use existing toast system or create new
    if (typeof ecommerce !== 'undefined' && ecommerce.showToast) {
        ecommerce.showToast(message, type);
    } else {
        // Fallback toast
        const toast = document.createElement('div');
        toast.className = `toast ${type}`;
        toast.innerHTML = `
            <i class="fas fa-${type === 'success' ? 'check-circle' : type === 'error' ? 'exclamation-circle' : 'info-circle'}"></i>
            <span>${message}</span>
        `;
        document.body.appendChild(toast);
        
        setTimeout(() => {
            toast.classList.add('show');
            setTimeout(() => {
                toast.classList.remove('show');
                setTimeout(() => toast.remove(), 300);
            }, 3000);
        }, 100);
    }
}

// Make functions globally available
window.toggleEditMode = toggleEditMode;
window.openAdminDashboard = openAdminDashboard;
window.closeAdminDashboard = closeAdminDashboard;
window.switchAdminTab = switchAdminTab;
window.showToast = showToast;

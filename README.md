<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Definitive Word - Premium Ebook Store</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* ... (keep ALL previous CSS styles exactly as they are) ... */
        
        /* Enhanced Enrollment Modal Styles */
        .enrollment-modal {
            max-width: 700px;
            background: linear-gradient(135deg, #1a365d 0%, #2d3748 100%);
            color: white;
        }
        
        .enrollment-modal .modal-content {
            background: transparent;
            box-shadow: 0 20px 60px rgba(0,0,0,0.3);
        }
        
        .enrollment-modal .modal-header {
            border-bottom: 2px solid rgba(214, 158, 46, 0.3);
            padding-bottom: 25px;
        }
        
        .enrollment-modal .modal-header h2 {
            color: #d69e2e;
            font-size: 2rem;
            text-align: center;
            width: 100%;
        }
        
        .enrollment-steps-container {
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 30px;
            margin: 20px 0;
            border: 1px solid rgba(255,255,255,0.2);
        }
        
        .enrollment-steps {
            display: flex;
            justify-content: space-between;
            margin: 30px 0;
            position: relative;
        }
        
        .enrollment-steps::before {
            content: '';
            position: absolute;
            top: 25px;
            left: 10%;
            right: 10%;
            height: 3px;
            background: rgba(255,255,255,0.3);
            z-index: 1;
        }
        
        .enrollment-steps::after {
            content: '';
            position: absolute;
            top: 25px;
            left: 10%;
            width: 0%;
            height: 3px;
            background: #d69e2e;
            z-index: 2;
            transition: width 0.5s ease;
        }
        
        .enrollment-steps.step-1::after { width: 0%; }
        .enrollment-steps.step-2::after { width: 40%; }
        .enrollment-steps.step-3::after { width: 80%; }
        
        .step {
            text-align: center;
            position: relative;
            z-index: 3;
            background: #2d3748;
            padding: 15px;
            border-radius: 50%;
            width: 50px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto;
            border: 3px solid rgba(255,255,255,0.3);
            transition: all 0.3s ease;
        }
        
        .step.active {
            background: #d69e2e;
            color: #1a365d;
            border-color: #d69e2e;
            transform: scale(1.1);
            box-shadow: 0 5px 15px rgba(214, 158, 46, 0.4);
        }
        
        .step.completed {
            background: #38a169;
            color: white;
            border-color: #38a169;
        }
        
        .step i {
            font-size: 1.2rem;
        }
        
        .step-label {
            margin-top: 15px;
            font-size: 0.9rem;
            font-weight: 600;
            color: #d69e2e;
        }
        
        .step-label span {
            display: block;
            font-size: 0.8rem;
            font-weight: normal;
            color: rgba(255,255,255,0.7);
            margin-top: 5px;
        }
        
        .enrollment-form {
            display: none;
            animation: slideInUp 0.5s ease;
        }
        
        .enrollment-form.active {
            display: block;
        }
        
        .program-preview {
            background: rgba(255,255,255,0.05);
            border-radius: 12px;
            padding: 25px;
            margin: 20px 0;
            border-left: 4px solid #d69e2e;
        }
        
        .program-preview-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
        }
        
        .program-preview-title {
            color: #d69e2e;
            font-size: 1.4rem;
            font-weight: 700;
        }
        
        .program-price-tag {
            background: #d69e2e;
            color: #1a365d;
            padding: 8px 16px;
            border-radius: 20px;
            font-weight: 700;
            font-size: 1.3rem;
        }
        
        .program-features-list {
            list-style: none;
            margin: 20px 0;
        }
        
        .program-features-list li {
            padding: 10px 0;
            border-bottom: 1px solid rgba(255,255,255,0.1);
            display: flex;
            align-items: center;
            gap: 12px;
        }
        
        .program-features-list li:last-child {
            border-bottom: none;
        }
        
        .program-features-list i {
            color: #d69e2e;
            width: 20px;
        }
        
        .enrollment-form .form-group {
            margin-bottom: 20px;
        }
        
        .enrollment-form label {
            color: #d69e2e;
            font-weight: 600;
            margin-bottom: 8px;
            display: block;
        }
        
        .enrollment-form .form-control {
            background: rgba(255,255,255,0.1);
            border: 2px solid rgba(255,255,255,0.2);
            color: white;
            border-radius: 8px;
            padding: 12px 15px;
            width: 100%;
            transition: all 0.3s ease;
        }
        
        .enrollment-form .form-control:focus {
            border-color: #d69e2e;
            background: rgba(255,255,255,0.15);
            outline: none;
            box-shadow: 0 0 0 3px rgba(214, 158, 46, 0.2);
        }
        
        .enrollment-form .form-control::placeholder {
            color: rgba(255,255,255,0.5);
        }
        
        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
        }
        
        .success-animation {
            text-align: center;
            padding: 40px 20px;
        }
        
        .success-icon {
            width: 80px;
            height: 80px;
            background: #38a169;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 25px;
            animation: bounceIn 0.6s ease;
        }
        
        .success-icon i {
            font-size: 2.5rem;
            color: white;
        }
        
        .success-title {
            color: #d69e2e;
            font-size: 1.8rem;
            margin-bottom: 15px;
            font-weight: 700;
        }
        
        .success-message {
            color: rgba(255,255,255,0.9);
            line-height: 1.6;
            margin-bottom: 25px;
        }
        
        .welcome-kit {
            background: rgba(255,255,255,0.05);
            border-radius: 10px;
            padding: 20px;
            margin: 25px 0;
            border: 1px solid rgba(214, 158, 46, 0.3);
        }
        
        .welcome-kit h5 {
            color: #d69e2e;
            margin-bottom: 15px;
            text-align: center;
        }
        
        .kit-items {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 15px;
            text-align: center;
        }
        
        .kit-item {
            padding: 15px 10px;
            background: rgba(255,255,255,0.1);
            border-radius: 8px;
            transition: transform 0.3s ease;
        }
        
        .kit-item:hover {
            transform: translateY(-5px);
        }
        
        .kit-item i {
            font-size: 1.5rem;
            color: #d69e2e;
            margin-bottom: 8px;
        }
        
        .kit-item span {
            font-size: 0.8rem;
            color: rgba(255,255,255,0.8);
        }
        
        .enrollment-actions {
            display: flex;
            justify-content: space-between;
            gap: 15px;
            margin-top: 30px;
        }
        
        .enrollment-btn {
            flex: 1;
            padding: 15px 25px;
            border: none;
            border-radius: 8px;
            font-weight: 700;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
        }
        
        .enrollment-btn.primary {
            background: #d69e2e;
            color: #1a365d;
        }
        
        .enrollment-btn.primary:hover {
            background: #ecc94b;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(214, 158, 46, 0.4);
        }
        
        .enrollment-btn.secondary {
            background: rgba(255,255,255,0.1);
            color: white;
            border: 2px solid rgba(255,255,255,0.3);
        }
        
        .enrollment-btn.secondary:hover {
            background: rgba(255,255,255,0.2);
            border-color: #d69e2e;
        }
        
        .enrollment-btn:disabled {
            opacity: 0.6;
            cursor: not-allowed;
            transform: none !important;
        }
        
        .enrollment-progress {
            margin: 20px 0;
        }
        
        .progress-text {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            font-size: 0.9rem;
            color: rgba(255,255,255,0.8);
        }
        
        .progress-bar-container {
            height: 6px;
            background: rgba(255,255,255,0.2);
            border-radius: 3px;
            overflow: hidden;
        }
        
        .progress-bar {
            height: 100%;
            background: linear-gradient(90deg, #d69e2e, #ecc94b);
            border-radius: 3px;
            transition: width 0.5s ease;
            width: 0%;
        }
        
        @keyframes slideInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes bounceIn {
            0% {
                opacity: 0;
                transform: scale(0.3);
            }
            50% {
                opacity: 1;
                transform: scale(1.05);
            }
            70% {
                transform: scale(0.9);
            }
            100% {
                opacity: 1;
                transform: scale(1);
            }
        }
        
        .pulse {
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% {
                box-shadow: 0 0 0 0 rgba(214, 158, 46, 0.4);
            }
            70% {
                box-shadow: 0 0 0 10px rgba(214, 158, 46, 0);
            }
            100% {
                box-shadow: 0 0 0 0 rgba(214, 158, 46, 0);
            }
        }
        
        /* Responsive adjustments */
        @media (max-width: 768px) {
            .enrollment-modal {
                margin: 20px;
                max-width: calc(100vw - 40px);
            }
            
            .enrollment-steps-container {
                padding: 20px;
            }
            
            .step {
                width: 40px;
                height: 40px;
                padding: 10px;
            }
            
            .step i {
                font-size: 1rem;
            }
            
            .form-row {
                grid-template-columns: 1fr;
            }
            
            .enrollment-actions {
                flex-direction: column;
            }
            
            .kit-items {
                grid-template-columns: repeat(2, 1fr);
            }
        }
        
        @media (max-width: 480px) {
            .enrollment-steps::before,
            .enrollment-steps::after {
                left: 15%;
                right: 15%;
            }
            
            .step-label {
                font-size: 0.8rem;
            }
            
            .program-preview-header {
                flex-direction: column;
                gap: 10px;
                text-align: center;
            }
        }
    </style>
</head>
<body>
    <!-- ... (keep ALL previous HTML exactly as it is) ... -->

    <!-- Enhanced Enrollment Modal -->
    <div class="edit-modal" id="enrollmentModal">
        <div class="modal-content enrollment-modal">
            <div class="modal-header">
                <h2 id="enrollmentTitle">Begin Your Transformation</h2>
                <button class="close-modal" onclick="closeEnrollmentModal()">&times;</button>
            </div>
            <div class="modal-body">
                <!-- Progress Bar -->
                <div class="enrollment-progress">
                    <div class="progress-text">
                        <span>Enrollment Progress</span>
                        <span id="progressPercent">0%</span>
                    </div>
                    <div class="progress-bar-container">
                        <div class="progress-bar" id="enrollmentProgressBar"></div>
                    </div>
                </div>
                
                <div class="enrollment-steps-container">
                    <!-- Step Indicators -->
                    <div class="enrollment-steps step-1" id="enrollmentSteps">
                        <div class="step-container">
                            <div class="step active" id="step1">
                                <i class="fas fa-info"></i>
                            </div>
                            <div class="step-label">
                                Program Details
                                <span>Step 1 of 3</span>
                            </div>
                        </div>
                        <div class="step-container">
                            <div class="step" id="step2">
                                <i class="fas fa-user"></i>
                            </div>
                            <div class="step-label">
                                Your Information
                                <span>Step 2 of 3</span>
                            </div>
                        </div>
                        <div class="step-container">
                            <div class="step" id="step3">
                                <i class="fas fa-check"></i>
                            </div>
                            <div class="step-label">
                                Confirmation
                                <span>Step 3 of 3</span>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Step 1: Program Information -->
                    <div class="enrollment-form active" id="enrollmentStep1">
                        <div class="program-preview">
                            <div class="program-preview-header">
                                <h3 class="program-preview-title" id="programName">Program Name</h3>
                                <div class="program-price-tag" id="programPriceDisplay">R0.00</div>
                            </div>
                            <p id="programDescription">Program description will appear here.</p>
                            
                            <div class="program-duration">
                                <strong><i class="fas fa-clock"></i> Duration:</strong> 
                                <span id="programDuration">0 weeks</span>
                            </div>
                            
                            <h4 style="color: #d69e2e; margin: 20px 0 15px;">What's Included:</h4>
                            <ul class="program-features-list" id="programFeaturesList">
                                <!-- Features will be dynamically added -->
                            </ul>
                        </div>
                        
                        <div class="enrollment-actions">
                            <button class="enrollment-btn secondary" onclick="closeEnrollmentModal()">
                                <i class="fas fa-times"></i> Cancel
                            </button>
                            <button class="enrollment-btn primary" onclick="nextEnrollmentStep()">
                                Continue to Enrollment <i class="fas fa-arrow-right"></i>
                            </button>
                        </div>
                    </div>
                    
                    <!-- Step 2: Personal Information -->
                    <div class="enrollment-form" id="enrollmentStep2">
                        <h3 style="color: #d69e2e; margin-bottom: 20px;">Your Information</h3>
                        
                        <form id="enrollmentForm">
                            <div class="form-row">
                                <div class="form-group">
                                    <label for="enrollmentFirstName">First Name *</label>
                                    <input type="text" class="form-control" id="enrollmentFirstName" required placeholder="Enter your first name">
                                </div>
                                <div class="form-group">
                                    <label for="enrollmentLastName">Last Name *</label>
                                    <input type="text" class="form-control" id="enrollmentLastName" required placeholder="Enter your last name">
                                </div>
                            </div>
                            
                            <div class="form-group">
                                <label for="enrollmentEmail">Email Address *</label>
                                <input type="email" class="form-control" id="enrollmentEmail" required placeholder="your.email@example.com">
                            </div>
                            
                            <div class="form-group">
                                <label for="enrollmentPhone">Phone Number *</label>
                                <input type="tel" class="form-control" id="enrollmentPhone" required placeholder="+27 12 345 6789">
                            </div>
                            
                            <div class="form-group">
                                <label for="enrollmentSource">How did you hear about us? *</label>
                                <select class="form-control" id="enrollmentSource" required>
                                    <option value="">Please select...</option>
                                    <option value="friend">Friend or Family Referral</option>
                                    <option value="social">Social Media</option>
                                    <option value="search">Online Search</option>
                                    <option value="event">Live Event or Workshop</option>
                                    <option value="website">Our Website</option>
                                    <option value="other">Other</option>
                                </select>
                            </div>
                            
                            <div class="form-group">
                                <label for="enrollmentGoals">What are your main goals for this program?</label>
                                <textarea class="form-control" id="enrollmentGoals" rows="3" placeholder="Share what you hope to achieve..."></textarea>
                            </div>
                        </form>
                        
                        <div class="enrollment-actions">
                            <button class="enrollment-btn secondary" onclick="prevEnrollmentStep()">
                                <i class="fas fa-arrow-left"></i> Back
                            </button>
                            <button class="enrollment-btn primary" onclick="nextEnrollmentStep()">
                                Continue to Review <i class="fas fa-arrow-right"></i>
                            </button>
                        </div>
                    </div>
                    
                    <!-- Step 3: Confirmation -->
                    <div class="enrollment-form" id="enrollmentStep3">
                        <div class="success-animation">
                            <div class="success-icon">
                                <i class="fas fa-check"></i>
                            </div>
                            <h3 class="success-title">Welcome to the Program!</h3>
                            <p class="success-message">
                                Thank you for enrolling in <strong id="successProgramName">Program Name</strong>. 
                                We're excited to have you join our community of learners and support your 
                                spiritual growth journey.
                            </p>
                            
                            <div class="welcome-kit">
                                <h5>Your Welcome Kit Includes:</h5>
                                <div class="kit-items">
                                    <div class="kit-item">
                                        <i class="fas fa-book-open"></i>
                                        <span>Program Materials</span>
                                    </div>
                                    <div class="kit-item">
                                        <i class="fas fa-users"></i>
                                        <span>Community Access</span>
                                    </div>
                                    <div class="kit-item">
                                        <i class="fas fa-calendar-check"></i>
                                        <span>Session Schedule</span>
                                    </div>
                                    <div class="kit-item">
                                        <i class="fas fa-headset"></i>
                                        <span>Support Resources</span>
                                    </div>
                                </div>
                            </div>
                            
                            <p class="success-message">
                                We've sent a confirmation email with your program details and next steps. 
                                Check your inbox within the next 5 minutes.
                            </p>
                        </div>
                        
                        <div class="enrollment-actions">
                            <button class="enrollment-btn primary pulse" onclick="closeEnrollmentModal()" style="flex: 1;">
                                <i class="fas fa-rocket"></i> Start Your Journey
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // ... (keep ALL previous JavaScript code exactly as it is) ...

        // Enhanced Enrollment Variables
        let currentProgram = null;
        let currentEnrollmentStep = 1;
        const totalEnrollmentSteps = 3;

        // Enhanced Program Data
        const programData = {
            'spiritual-foundations': {
                name: 'Spiritual Foundations',
                description: 'Build a strong spiritual foundation with our comprehensive 12-week program designed for beginners and those seeking to deepen their faith journey.',
                price: 1299,
                duration: '12 weeks',
                features: [
                    'Weekly Bible study materials and workbooks',
                    'Personal prayer journal template',
                    '4 live group coaching sessions',
                    'Access to private online community',
                    'Weekly inspirational video content',
                    'Progress tracking and assessments',
                    'Certificate of completion'
                ]
            },
            'leadership-development': {
                name: 'Leadership Development', 
                description: 'Transform into a confident Christian leader with our intensive 6-month program featuring mentorship, practical training, and theological education.',
                price: 4999,
                duration: '6 months',
                features: [
                    'Advanced theological training modules',
                    'One-on-one mentorship sessions',
                    'Practical ministry experience opportunities',
                    'Leadership certification upon completion',
                    'Networking with Christian leaders',
                    'Personalized growth plan',
                    'Lifetime access to alumni resources'
                ]
            },
            'marriage-family': {
                name: 'Marriage & Family',
                description: 'Strengthen your family relationships through biblical principles and practical tools in this transformative 8-week program for couples and families.',
                price: 2499, 
                duration: '8 weeks',
                features: [
                    'Comprehensive couples workbook',
                    'Weekly interactive video sessions',
                    '2 private counseling sessions included',
                    'Family activity guides and resources',
                    'Communication skills training',
                    'Conflict resolution strategies',
                    'Ongoing support community access'
                ]
            }
        };

        // Enhanced Enrollment Functions
        function enrollProgram(programId) {
            if (!currentUser) {
                showNotification('Please login to enroll in a program');
                toggleLogin(true);
                return;
            }
            
            currentProgram = programData[programId];
            if (!currentProgram) {
                showNotification('Program not found');
                return;
            }
            
            openEnrollmentModal();
        }

        function openEnrollmentModal() {
            const modal = document.getElementById('enrollmentModal');
            const title = document.getElementById('enrollmentTitle');
            const programName = document.getElementById('programName');
            const programDesc = document.getElementById('programDescription');
            const programPrice = document.getElementById('programPriceDisplay');
            const programDuration = document.getElementById('programDuration');
            const programFeatures = document.getElementById('programFeaturesList');
            const successProgram = document.getElementById('successProgramName');
            
            // Set program information
            title.textContent = `Enroll in ${currentProgram.name}`;
            programName.textContent = currentProgram.name;
            programDesc.textContent = currentProgram.description;
            programPrice.textContent = `R${currentProgram.price}`;
            programDuration.textContent = currentProgram.duration;
            successProgram.textContent = currentProgram.name;
            
            // Populate features list
            programFeatures.innerHTML = '';
            currentProgram.features.forEach(feature => {
                const li = document.createElement('li');
                li.innerHTML = `<i class="fas fa-check"></i> ${feature}`;
                programFeatures.appendChild(li);
            });
            
            // Reset to first step
            currentEnrollmentStep = 1;
            updateEnrollmentUI();
            
            modal.classList.add('active');
        }

        function closeEnrollmentModal() {
            document.getElementById('enrollmentModal').classList.remove('active');
            currentProgram = null;
            currentEnrollmentStep = 1;
            updateEnrollmentUI();
        }

        function updateEnrollmentUI() {
            // Update progress bar
            const progressPercent = ((currentEnrollmentStep - 1) / (totalEnrollmentSteps - 1)) * 100;
            document.getElementById('enrollmentProgressBar').style.width = `${progressPercent}%`;
            document.getElementById('progressPercent').textContent = `${Math.round(progressPercent)}%`;
            
            // Update step indicators
            for (let i = 1; i <= totalEnrollmentSteps; i++) {
                const step = document.getElementById(`step${i}`);
                const form = document.getElementById(`enrollmentStep${i}`);
                
                if (i < currentEnrollmentStep) {
                    step.className = 'step completed';
                    step.innerHTML = '<i class="fas fa-check"></i>';
                } else if (i === currentEnrollmentStep) {
                    step.className = 'step active';
                    // Set appropriate icon for current step
                    if (i === 1) step.innerHTML = '<i class="fas fa-info"></i>';
                    else if (i === 2) step.innerHTML = '<i class="fas fa-user"></i>';
                    else if (i === 3) step.innerHTML = '<i class="fas fa-check"></i>';
                } else {
                    step.className = 'step';
                    // Set appropriate icon for future steps
                    if (i === 1) step.innerHTML = '<i class="fas fa-info"></i>';
                    else if (i === 2) step.innerHTML = '<i class="fas fa-user"></i>';
                    else if (i === 3) step.innerHTML = '<i class="fas fa-check"></i>';
                }
                
                // Show/hide forms
                if (i === currentEnrollmentStep) {
                    form.classList.add('active');
                } else {
                    form.classList.remove('active');
                }
            }
            
            // Update steps container class for progress line
            document.getElementById('enrollmentSteps').className = `enrollment-steps step-${currentEnrollmentStep}`;
        }

        function nextEnrollmentStep() {
            if (currentEnrollmentStep === 2) {
                // Validate form
                const firstName = document.getElementById('enrollmentFirstName').value;
                const lastName = document.getElementById('enrollmentLastName').value;
                const email = document.getElementById('enrollmentEmail').value;
                const phone = document.getElementById('enrollmentPhone').value;
                const source = document.getElementById('enrollmentSource').value;
                
                if (!firstName || !lastName || !email || !phone || !source) {
                    showNotification('Please fill in all required fields');
                    document.getElementById('enrollmentForm').classList.add('shake');
                    setTimeout(() => {
                        document.getElementById('enrollmentForm').classList.remove('shake');
                    }, 500);
                    return;
                }
                
                // Validate email format
                const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
                if (!emailRegex.test(email)) {
                    showNotification('Please enter a valid email address');
                    return;
                }
            }
            
            if (currentEnrollmentStep < totalEnrollmentSteps) {
                currentEnrollmentStep++;
                updateEnrollmentUI();
                
                // If moving to final step, simulate processing
                if (currentEnrollmentStep === 3) {
                    simulateEnrollmentProcessing();
                }
            }
        }

        function prevEnrollmentStep() {
            if (currentEnrollmentStep > 1) {
                currentEnrollmentStep--;
                updateEnrollmentUI();
            }
        }

        function simulateEnrollmentProcessing() {
            const button = document.querySelector('#enrollmentStep2 .enrollment-btn.primary');
            const originalText = button.innerHTML;
            
            // Show processing state
            button.innerHTML = '<i class="fas fa-spinner fa-spin"></i> Processing Enrollment...';
            button.disabled = true;
            
            // Simulate API call
            setTimeout(() => {
                button.disabled = false;
                
                // Show success state
                showNotification(`🎉 Successfully enrolled in ${currentProgram.name}!`, 5000);
                
                // Track enrollment in user data
                if (currentUser) {
                    if (!currentUser.enrollments) {
                        currentUser.enrollments = [];
                    }
                    currentUser.enrollments.push({
                        program: currentProgram.name,
                        date: new Date().toLocaleDateString(),
                        status: 'active'
                    });
                }
            }, 2000);
        }

        // ... (keep all other existing JavaScript functions) ...
    </script>
</body>
</html>

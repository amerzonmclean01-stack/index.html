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

        /* === EDITABLE ELEMENTS === */
        .editable {
            position: relative;
            border: 2px dashed transparent;
            transition: all 0.3s ease;
            padding: 5px;
            border-radius: 6px;
            margin: 1px;
            cursor: default;
        }

        .edit-mode-on .editable {
            border-color: #d69e2e !important;
            background: rgba(214, 158, 46, 0.15) !important;
        }

        .editable:hover {
            background: rgba(214, 158, 46, 0.25) !important;
        }

        .edit-indicator {
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

        .edit-mode-on .edit-indicator {
            display: flex;
        }

        /* === HEADER === */
        header {
            background: white;
            box-shadow: 0 2px 20px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
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

        /* === CONTEXT MENU === */
        .context-menu {
            position: fixed;
            background: white;
            border-radius: 8px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.15);
            z-index: 10001;
            min-width: 180px;
            opacity: 0;
            transform: scale(0.95);
            transition: all 0.2s ease;
            pointer-events: none;
        }

        .context-menu.active {
            opacity: 1;
            transform: scale(1);
            pointer-events: all;
        }

        .context-menu-item {
            padding: 12px 16px;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 10px;
            transition: background 0.2s ease;
            border-bottom: 1px solid #f1f1f1;
        }

        .context-menu-item:last-child {
            border-bottom: none;
        }

        .context-menu-item:hover {
            background: #f7fafc;
        }

        .context-menu-item i {
            width: 16px;
            text-align: center;
            color: #d69e2e;
        }

        /* === EDIT MODE INDICATOR === */
        .edit-mode-indicator {
            position: fixed;
            top: 20px;
            right: 20px;
            background: #d69e2e;
            color: #1a365d;
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 600;
            box-shadow: 0 4px 12px rgba(0,0,0,0.15);
            z-index: 10000;
            display: none;
            align-items: center;
            gap: 8px;
            animation: slideIn 0.3s ease;
        }

        .edit-mode-indicator.active {
            display: flex;
        }

        @keyframes slideIn {
            from {
                transform: translateX(100px);
                opacity: 0;
            }
            to {
                transform: translateX(0);
                opacity: 1;
            }
        }

        /* === QUICK EDIT TOOLTIP === */
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

        /* === MODAL === */
        .edit-modal {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.7);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 10001;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s ease;
        }

        .edit-modal.active {
            opacity: 1;
            visibility: visible;
        }

        .modal-content {
            background: white;
            width: 90%;
            max-width: 600px;
            border-radius: 12px;
            padding: 30px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        }

        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
        }

        .modal-header h2 {
            color: #1a365d;
        }

        .close-modal {
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: #666;
            transition: color 0.3s ease;
        }

        .close-modal:hover {
            color: #c53030;
        }

        .modal-body textarea {
            width: 100%;
            min-height: 150px;
            padding: 15px;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 1rem;
            font-family: inherit;
            resize: vertical;
        }

        .modal-footer {
            display: flex;
            justify-content: flex-end;
            gap: 15px;
            margin-top: 20px;
        }

        .modal-btn {
            padding: 10px 20px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .modal-btn.primary {
            background: #d69e2e;
            color: #1a365d;
        }

        .modal-btn.secondary {
            background: #e2e8f0;
            color: #4a5568;
        }

        .modal-btn:hover {
            transform: translateY(-1px);
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }

        /* === NOTIFICATION === */
        .notification {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: #d69e2e;
            color: white;
            padding: 15px 25px;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            z-index: 10002;
            transform: translateY(100px);
            opacity: 0;
            transition: all 0.3s ease;
        }

        .notification.show {
            transform: translateY(0);
            opacity: 1;
        }

        /* === BOOKS SECTION === */
        .books-section {
            background: white;
        }

        .books-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .book-card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
            transition: all 0.3s ease;
            position: relative;
        }

        .book-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
        }

        .book-cover {
            height: 250px;
            overflow: hidden;
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
            font-size: 1.3rem;
            font-weight: 700;
            margin-bottom: 8px;
            color: #1a365d;
        }

        .book-author {
            color: #666;
            margin-bottom: 15px;
            font-size: 0.95rem;
        }

        .book-price {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .price {
            font-size: 1.5rem;
            font-weight: 700;
            color: #1a365d;
        }

        /* === BLOG SECTION === */
        .blog-section {
            background: #f7fafc;
        }

        .blog-container {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 40px;
        }

        .blog-posts {
            display: grid;
            gap: 30px;
        }

        .blog-post {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
        }

        .blog-post:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }

        .blog-post-image {
            height: 200px;
            overflow: hidden;
        }

        .blog-post-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .blog-post:hover .blog-post-image img {
            transform: scale(1.05);
        }

        .blog-post-content {
            padding: 25px;
        }

        .blog-post-meta {
            display: flex;
            gap: 15px;
            margin-bottom: 15px;
            font-size: 0.85rem;
            color: #666;
        }

        .blog-post-category {
            background: #d69e2e;
            color: white;
            padding: 4px 10px;
            border-radius: 20px;
            font-size: 0.75rem;
            font-weight: 600;
        }

        .blog-post-title {
            font-size: 1.4rem;
            margin-bottom: 15px;
            color: #1a365d;
        }

        .blog-post-excerpt {
            color: #666;
            margin-bottom: 20px;
        }

        .blog-post-footer {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding-top: 15px;
            border-top: 1px solid #e2e8f0;
        }

        .blog-post-actions {
            display: flex;
            gap: 15px;
        }

        .blog-post-actions button {
            background: none;
            border: none;
            color: #666;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 5px;
            transition: color 0.3s ease;
        }

        .blog-post-actions button:hover {
            color: #d69e2e;
        }

        /* Blog Sidebar */
        .blog-sidebar {
            display: flex;
            flex-direction: column;
            gap: 30px;
        }

        .sidebar-widget {
            background: white;
            padding: 25px;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }

        .widget-title {
            font-size: 1.2rem;
            margin-bottom: 20px;
            color: #1a365d;
            padding-bottom: 10px;
            border-bottom: 2px solid #d69e2e;
        }

        .categories-list {
            list-style: none;
        }

        .categories-list li {
            margin-bottom: 10px;
            padding-bottom: 10px;
            border-bottom: 1px solid #e2e8f0;
        }

        .categories-list a {
            color: #4a5568;
            text-decoration: none;
            transition: color 0.3s ease;
            display: flex;
            justify-content: space-between;
        }

        .categories-list a:hover {
            color: #d69e2e;
        }

        .categories-list span {
            background: #e2e8f0;
            padding: 2px 8px;
            border-radius: 10px;
            font-size: 0.8rem;
        }

        .recent-posts-list {
            list-style: none;
        }

        .recent-posts-list li {
            margin-bottom: 15px;
            padding-bottom: 15px;
            border-bottom: 1px solid #e2e8f0;
        }

        .recent-post {
            display: flex;
            gap: 15px;
        }

        .recent-post-image {
            width: 70px;
            height: 70px;
            border-radius: 8px;
            overflow: hidden;
            flex-shrink: 0;
        }

        .recent-post-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .recent-post-content h4 {
            font-size: 0.95rem;
            margin-bottom: 5px;
            color: #1a365d;
        }

        .recent-post-content .post-date {
            font-size: 0.8rem;
            color: #666;
        }

        .tags-cloud {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .tag {
            background: #e2e8f0;
            color: #4a5568;
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 0.85rem;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .tag:hover {
            background: #d69e2e;
            color: white;
        }

        /* === MINISTRY SECTION === */
        .ministry-section {
            background: linear-gradient(135deg, #2c5282 0%, #1a365d 100%);
            color: white;
            position: relative;
            overflow: hidden;
        }

        .ministry-section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('https://images.unsplash.com/photo-1532629345422-7515f3d16bb6?ixlib=rb-4.0.3&auto=format&fit=crop&w=2000&q=80') center/cover;
            opacity: 0.1;
            z-index: 1;
        }

        .ministry-section > .container {
            position: relative;
            z-index: 2;
        }

        .ministry-hero {
            text-align: center;
            padding: 80px 0 50px;
        }

        .ministry-hero h2 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            font-weight: 700;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        .ministry-hero p {
            font-size: 1.3rem;
            max-width: 700px;
            margin: 0 auto 40px;
            opacity: 0.9;
        }

        .ministry-features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin: 60px 0;
        }

        .ministry-feature {
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(10px);
            padding: 40px 30px;
            border-radius: 15px;
            text-align: center;
            border: 1px solid rgba(255,255,255,0.2);
            transition: all 0.3s ease;
        }

        .ministry-feature:hover {
            transform: translateY(-10px);
            background: rgba(255,255,255,0.15);
            box-shadow: 0 15px 30px rgba(0,0,0,0.3);
        }

        .ministry-feature i {
            font-size: 3rem;
            margin-bottom: 20px;
            color: #d69e2e;
        }

        .ministry-feature h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: #d69e2e;
        }

        .ministry-feature p {
            opacity: 0.9;
            line-height: 1.6;
        }

        /* Ministry Programs */
        .ministry-programs {
            background: rgba(255,255,255,0.05);
            padding: 60px 0;
            margin: 60px 0;
            border-radius: 20px;
        }

        .programs-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .program-card {
            background: rgba(255,255,255,0.1);
            border-radius: 15px;
            overflow: hidden;
            transition: all 0.3s ease;
            border: 1px solid rgba(255,255,255,0.2);
        }

        .program-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.4);
        }

        .program-header {
            padding: 25px;
            text-align: center;
            border-bottom: 1px solid rgba(255,255,255,0.1);
        }

        .program-header i {
            font-size: 2.5rem;
            color: #d69e2e;
            margin-bottom: 15px;
        }

        .program-header h3 {
            font-size: 1.4rem;
            margin-bottom: 10px;
            color: #d69e2e;
        }

        .program-content {
            padding: 25px;
        }

        .program-features {
            list-style: none;
            margin-bottom: 20px;
        }

        .program-features li {
            padding: 8px 0;
            border-bottom: 1px solid rgba(255,255,255,0.1);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .program-features li:last-child {
            border-bottom: none;
        }

        .program-features i {
            color: #d69e2e;
            font-size: 0.9rem;
        }

        .program-price {
            text-align: center;
            font-size: 1.5rem;
            font-weight: 700;
            color: #d69e2e;
            margin: 20px 0;
        }

        /* Life Coaching */
        .life-coaching {
            background: rgba(255,255,255,0.05);
            padding: 60px 0;
            margin: 60px 0;
            border-radius: 20px;
        }

        .coaching-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .coaching-content h3 {
            font-size: 2rem;
            margin-bottom: 20px;
            color: #d69e2e;
        }

        .coaching-content p {
            margin-bottom: 25px;
            line-height: 1.7;
            opacity: 0.9;
        }

        .coaching-features {
            list-style: none;
            margin: 30px 0;
        }

        .coaching-features li {
            padding: 12px 0;
            border-bottom: 1px solid rgba(255,255,255,0.1);
            display: flex;
            align-items: center;
            gap: 15px;
            font-size: 1.1rem;
        }

        .coaching-features i {
            color: #d69e2e;
            font-size: 1.2rem;
        }

        .coaching-form {
            background: rgba(255,255,255,0.1);
            padding: 40px;
            border-radius: 15px;
            border: 1px solid rgba(255,255,255,0.2);
        }

        .coaching-form h4 {
            font-size: 1.5rem;
            margin-bottom: 25px;
            color: #d69e2e;
            text-align: center;
        }

        /* Ministry Books */
        .ministry-books {
            padding: 60px 0;
        }

        .books-slider {
            position: relative;
            margin: 40px 0;
        }

        .books-track {
            display: flex;
            gap: 25px;
            overflow-x: auto;
            scroll-behavior: smooth;
            padding: 20px 10px;
            scrollbar-width: none;
        }

        .books-track::-webkit-scrollbar {
            display: none;
        }

        .ministry-book-card {
            background: rgba(255,255,255,0.1);
            border-radius: 12px;
            padding: 25px;
            min-width: 280px;
            border: 1px solid rgba(255,255,255,0.2);
            transition: all 0.3s ease;
        }

        .ministry-book-card:hover {
            transform: translateY(-5px);
            background: rgba(255,255,255,0.15);
        }

        .book-cover-small {
            width: 120px;
            height: 160px;
            border-radius: 8px;
            overflow: hidden;
            margin: 0 auto 20px;
        }

        .book-cover-small img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .ministry-book-card h4 {
            font-size: 1.2rem;
            margin-bottom: 10px;
            color: #d69e2e;
            text-align: center;
        }

        .ministry-book-card p {
            font-size: 0.9rem;
            opacity: 0.8;
            text-align: center;
            margin-bottom: 15px;
        }

        .book-price-small {
            text-align: center;
            font-size: 1.3rem;
            font-weight: 700;
            color: #d69e2e;
            margin: 15px 0;
        }

        /* Workshop Calendar */
        .workshop-calendar {
            background: rgba(255,255,255,0.05);
            padding: 60px 0;
            margin: 60px 0;
            border-radius: 20px;
        }

        .calendar-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            margin-top: 40px;
        }

        .calendar-view {
            background: rgba(255,255,255,0.1);
            border-radius: 15px;
            padding: 30px;
            border: 1px solid rgba(255,255,255,0.2);
        }

        .calendar-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 25px;
        }

        .calendar-grid {
            display: grid;
            grid-template-columns: repeat(7, 1fr);
            gap: 8px;
            margin-bottom: 20px;
        }

        .calendar-day {
            text-align: center;
            padding: 10px;
            font-weight: 600;
            color: #d69e2e;
        }

        .calendar-date {
            text-align: center;
            padding: 12px 8px;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .calendar-date:hover {
            background: rgba(214, 158, 46, 0.2);
        }

        .calendar-date.active {
            background: #d69e2e;
            color: #1a365d;
            font-weight: 700;
        }

        .calendar-date.has-event::after {
            content: '';
            display: block;
            width: 6px;
            height: 6px;
            background: #c53030;
            border-radius: 50%;
            margin: 5px auto 0;
        }

        .workshop-list {
            max-height: 400px;
            overflow-y: auto;
        }

        .workshop-item {
            background: rgba(255,255,255,0.1);
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 15px;
            border: 1px solid rgba(255,255,255,0.1);
            transition: all 0.3s ease;
        }

        .workshop-item:hover {
            background: rgba(255,255,255,0.15);
            transform: translateX(5px);
        }

        .workshop-item h4 {
            color: #d69e2e;
            margin-bottom: 8px;
        }

        .workshop-meta {
            display: flex;
            gap: 15px;
            font-size: 0.9rem;
            opacity: 0.8;
            margin-bottom: 10px;
        }

        .workshop-meta i {
            color: #d69e2e;
        }

        /* Testimonials */
        .testimonials {
            padding: 60px 0;
        }

        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .testimonial-card {
            background: rgba(255,255,255,0.1);
            padding: 30px;
            border-radius: 15px;
            border: 1px solid rgba(255,255,255,0.2);
            position: relative;
        }

        .testimonial-card::before {
            content: '"';
            font-size: 4rem;
            color: #d69e2e;
            position: absolute;
            top: 10px;
            left: 20px;
            opacity: 0.3;
            font-family: serif;
        }

        .testimonial-content {
            position: relative;
            z-index: 2;
            margin-bottom: 20px;
            font-style: italic;
            line-height: 1.6;
        }

        .testimonial-author {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .author-avatar {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            overflow: hidden;
            border: 2px solid #d69e2e;
        }

        .author-avatar img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .author-info h5 {
            color: #d69e2e;
            margin-bottom: 5px;
        }

        .author-info p {
            font-size: 0.9rem;
            opacity: 0.8;
        }

        /* CTA Section */
        .ministry-cta {
            text-align: center;
            padding: 80px 0;
            background: rgba(255,255,255,0.05);
            border-radius: 20px;
            margin: 60px 0;
        }

        .ministry-cta h3 {
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: #d69e2e;
        }

        .ministry-cta p {
            font-size: 1.2rem;
            max-width: 600px;
            margin: 0 auto 40px;
            opacity: 0.9;
        }

        .cta-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }

        /* === COMMUNITY SECTION === */
        .community-section {
            background: white;
        }

        .community-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
        }

        .discussion-forum {
            background: #f7fafc;
            padding: 30px;
            border-radius: 12px;
        }

        .discussion-list {
            margin-top: 20px;
        }

        .discussion-item {
            background: white;
            padding: 20px;
            border-radius: 8px;
            margin-bottom: 15px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.05);
        }

        .discussion-meta {
            display: flex;
            justify-content: space-between;
            font-size: 0.85rem;
            color: #666;
            margin-top: 10px;
        }

        .user-reviews {
            background: #f7fafc;
            padding: 30px;
            border-radius: 12px;
        }

        .review-item {
            background: white;
            padding: 20px;
            border-radius: 8px;
            margin-bottom: 15px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.05);
        }

        .review-header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
        }

        .review-rating {
            color: #d69e2e;
        }

        /* === PAYMENT SECTION === */
        .payment-section {
            background: #f7fafc;
        }

        .payment-container {
            max-width: 800px;
            margin: 0 auto;
            background: white;
            padding: 40px;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }

        .payment-methods {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }

        .payment-method {
            border: 2px solid #e2e8f0;
            border-radius: 8px;
            padding: 20px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .payment-method:hover, .payment-method.active {
            border-color: #d69e2e;
            background: rgba(214, 158, 46, 0.05);
        }

        .payment-method i {
            font-size: 2rem;
            margin-bottom: 10px;
            color: #4a5568;
        }

        .payment-form {
            margin-top: 30px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: #1a365d;
        }

        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 1rem;
            transition: all 0.3s ease;
        }

        .form-control:focus {
            border-color: #d69e2e;
            outline: none;
            box-shadow: 0 0 0 3px rgba(214, 158, 46, 0.2);
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
        }

        /* === CART MODAL === */
        .cart-modal {
            position: fixed;
            top: 0;
            right: -400px;
            width: 380px;
            height: 100%;
            background: white;
            box-shadow: -5px 0 15px rgba(0,0,0,0.1);
            z-index: 10001;
            transition: right 0.3s ease;
            padding: 20px;
            overflow-y: auto;
        }

        .cart-modal.active {
            right: 0;
        }

        .cart-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 1px solid #e2e8f0;
        }

        .cart-items {
            margin-bottom: 20px;
        }

        .cart-item {
            display: flex;
            gap: 15px;
            padding: 15px 0;
            border-bottom: 1px solid #e2e8f0;
        }

        .cart-item img {
            width: 60px;
            height: 80px;
            object-fit: cover;
            border-radius: 4px;
        }

        .cart-item-details {
            flex: 1;
        }

        .cart-item-title {
            font-weight: 600;
            margin-bottom: 5px;
        }

        .cart-item-price {
            color: #1a365d;
            font-weight: 600;
        }

        .cart-item-remove {
            color: #c53030;
            background: none;
            border: none;
            cursor: pointer;
        }

        .cart-total {
            display: flex;
            justify-content: space-between;
            font-size: 1.2rem;
            font-weight: 700;
            margin: 20px 0;
            padding-top: 15px;
            border-top: 1px solid #e2e8f0;
        }

        /* === ABOUT SECTION === */
        .about-section {
            background: #f7fafc;
        }

        .about-content {
            max-width: 900px;
            margin: 0 auto;
        }

        .about-text {
            font-size: 1.1rem;
            line-height: 1.8;
            margin-bottom: 30px;
            text-align: center;
        }

        .team-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .team-member {
            text-align: center;
            background: white;
            padding: 30px 20px;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
        }

        .team-member:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }

        .team-member img {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            object-fit: cover;
            margin-bottom: 20px;
            border: 4px solid #d69e2e;
        }

        .team-member h4 {
            font-size: 1.3rem;
            margin-bottom: 8px;
            color: #1a365d;
        }

        .team-member p:first-of-type {
            font-weight: 600;
            color: #d69e2e;
            margin-bottom: 15px;
        }

        /* === FOOTER === */
        footer {
            background: #1a365d;
            color: white;
            padding: 50px 0 20px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-column h3 {
            font-size: 1.3rem;
            margin-bottom: 20px;
            color: #d69e2e;
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: 10px;
        }

        .footer-column a {
            color: #cbd5e0;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-column a:hover {
            color: #d69e2e;
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
            background: rgba(255,255,255,0.1);
            border-radius: 50%;
            color: white;
            transition: all 0.3s ease;
        }

        .social-links a:hover {
            background: #d69e2e;
            transform: translateY(-3px);
        }

        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.1);
            color: #cbd5e0;
            font-size: 0.9rem;
        }

        /* === ENHANCED ENROLLMENT MODAL === */
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

        /* === INTERACTIVE ELEMENTS === */
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

        .reading-progress {
            width: 100%;
            height: 4px;
            background: #e2e8f0;
            border-radius: 2px;
            margin: 10px 0;
            overflow: hidden;
        }
        
        .reading-progress-bar {
            height: 100%;
            background: #d69e2e;
            width: 0%;
            transition: width 0.5s ease;
        }

        .interactive-demo {
            background: rgba(255,255,255,0.1);
            padding: 20px;
            border-radius: 10px;
            margin: 15px 0;
            text-align: center;
        }

        .demo-buttons {
            display: flex;
            gap: 10px;
            justify-content: center;
            margin: 15px 0;
        }

        .shake {
            animation: shake 0.5s ease;
        }

        @keyframes shake {
            0%, 100% { transform: translateX(0); }
            25% { transform: translateX(-5px); }
            75% { transform: translateX(5px); }
        }

        /* === RESPONSIVE === */
        @media (max-width: 768px) {
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
            
            .blog-container {
                grid-template-columns: 1fr;
            }
            
            .community-container {
                grid-template-columns: 1fr;
            }
            
            .books-grid {
                grid-template-columns: 1fr;
            }
            
            .cart-modal {
                width: 100%;
                right: -100%;
            }
            
            .nav-main a::before {
                display: none;
            }
            
            .edit-mode-indicator {
                top: 10px;
                right: 10px;
                font-size: 0.75rem;
            }
            
            .ministry-hero h2 {
                font-size: 2.5rem;
            }
            
            .coaching-container,
            .calendar-container {
                grid-template-columns: 1fr;
            }
            
            .ministry-features {
                grid-template-columns: 1fr;
            }
            
            .programs-grid {
                grid-template-columns: 1fr;
            }
            
            .cta-buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .coaching-form {
                padding: 25px;
            }

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
            .hero h1 {
                font-size: 1.8rem;
            }
            
            .section-title {
                font-size: 1.7rem;
            }
            
            .form-row {
                grid-template-columns: 1fr;
            }
            
            .context-menu {
                min-width: 160px;
            }
            
            .ministry-hero h2 {
                font-size: 2rem;
            }
            
            .ministry-hero p {
                font-size: 1.1rem;
            }
            
            .ministry-feature {
                padding: 30px 20px;
            }

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
    <!-- Edit Mode Indicator -->
    <div class="edit-mode-indicator" id="editModeIndicator">
        <i class="fas fa-edit"></i>
        <span>Edit Mode Active</span>
        <button onclick="toggleEditMode()" style="background: none; border: none; color: #1a365d; cursor: pointer; margin-left: 10px;">
            <i class="fas fa-times"></i>
        </button>
    </div>

    <!-- Quick Edit Tooltip -->
    <div class="quick-edit-tooltip" id="quickEditTooltip">Double-click to edit • Right-click for options</div>

    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-top">
                <div class="logo editable" data-id="logo">
                    <span class="edit-indicator">✏️</span>
                    The Definitive Word
                </div>
                
                <nav class="nav-main">
                    <a href="#home" class="active nav-link" data-tab="home">Home</a>
                    <a href="#books" class="nav-link" data-tab="books">Books</a>
                    <a href="#blog" class="nav-link" data-tab="blog">Blog</a>
                    <a href="#ministry" class="nav-link" data-tab="ministry">Ministry</a>
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
                <span class="edit-indicator">✏️</span>
                Welcome to The Definitive Word
            </h1>
            <p class="editable" data-id="hero-subtitle">
                <span class="edit-indicator">✏️</span>
                South Africa's premier destination for quality ebooks and exceptional reading experiences
            </p>
            <div style="margin-top: 35px;">
                <a href="#books" class="btn">
                    <i class="fas fa-gem"></i>
                    Browse Books
                </a>
                <a href="#ministry" class="btn btn-secondary">
                    <i class="fas fa-hands-helping"></i>
                    Explore Ministry
                </a>
            </div>
        </div>
    </section>

    <!-- Books Section -->
    <section id="books" class="section books-section">
        <div class="container">
            <h2 class="section-title editable" data-id="books-title">
                <span class="edit-indicator">✏️</span>
                Featured Ebooks
            </h2>
            <p class="section-subtitle editable" data-id="books-subtitle">
                <span class="edit-indicator">✏️</span>
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
                <span class="edit-indicator">✏️</span>
                Our Blog
            </h2>
            <p class="section-subtitle editable" data-id="blog-subtitle">
                <span class="edit-indicator">✏️</span>
                Insights, author interviews, reading recommendations, and literary discussions
            </p>
            
            <div class="blog-container">
                <div class="blog-posts" id="blogPosts">
                    <!-- Blog posts will be loaded here -->
                </div>
                
                <div class="blog-sidebar">
                    <div class="sidebar-widget">
                        <h3 class="widget-title editable" data-id="categories-title">
                            <span class="edit-indicator">✏️</span>
                            Categories
                        </h3>
                        <ul class="categories-list" id="categoriesList">
                            <!-- Categories will be loaded here -->
                        </ul>
                    </div>
                    
                    <div class="sidebar-widget">
                        <h3 class="widget-title editable" data-id="recent-posts-title">
                            <span class="edit-indicator">✏️</span>
                            Recent Posts
                        </h3>
                        <ul class="recent-posts-list" id="recentPostsList">
                            <!-- Recent posts will be loaded here -->
                        </ul>
                    </div>
                    
                    <div class="sidebar-widget">
                        <h3 class="widget-title editable" data-id="tags-title">
                            <span class="edit-indicator">✏️</span>
                            Popular Tags
                        </h3>
                        <div class="tags-cloud" id="tagsCloud">
                            <!-- Tags will be loaded here -->
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Ministry & Life Coaching Section -->
    <section id="ministry" class="section ministry-section">
        <div class="container">
            <div class="ministry-hero">
                <h2 class="editable" data-id="ministry-title">
                    <span class="edit-indicator">✏️</span>
                    Ministry & Life Coaching
                </h2>
                <p class="editable" data-id="ministry-subtitle">
                    <span class="edit-indicator">✏️</span>
                    Transform your spiritual journey and personal growth through our comprehensive ministry resources, life coaching programs, and workshops
                </p>
                <div class="cta-buttons">
                    <button class="btn" onclick="scrollToPrograms()">
                        <i class="fas fa-graduation-cap"></i> Explore Programs
                    </button>
                    <button class="btn btn-secondary" onclick="openCoachingModal()">
                        <i class="fas fa-calendar-check"></i> Book Consultation
                    </button>
                </div>
            </div>

            <!-- Ministry Features -->
            <div class="ministry-features">
                <div class="ministry-feature">
                    <i class="fas fa-bible icon-editable"></i>
                    <h3 class="editable" data-id="feature1-title">
                        <span class="edit-indicator">✏️</span>
                        Biblical Teaching
                    </h3>
                    <p class="editable" data-id="feature1-desc">
                        <span class="edit-indicator">✏️</span>
                        Deep dive into scripture with comprehensive study materials and guided lessons
                    </p>
                </div>
                <div class="ministry-feature">
                    <i class="fas fa-hands-helping icon-editable"></i>
                    <h3 class="editable" data-id="feature2-title">
                        <span class="edit-indicator">✏️</span>
                        Personal Coaching
                    </h3>
                    <p class="editable" data-id="feature2-desc">
                        <span class="edit-indicator">✏️</span>
                        One-on-one life coaching sessions tailored to your spiritual and personal goals
                    </p>
                </div>
                <div class="ministry-feature">
                    <i class="fas fa-users icon-editable"></i>
                    <h3 class="editable" data-id="feature3-title">
                        <span class="edit-indicator">✏️</span>
                        Group Workshops
                    </h3>
                    <p class="editable" data-id="feature3-desc">
                        <span class="edit-indicator">✏️</span>
                        Join community workshops and grow together with like-minded individuals
                    </p>
                </div>
            </div>

            <!-- Ministry Programs -->
            <div class="ministry-programs">
                <h2 class="section-title editable" data-id="programs-title">
                    <span class="edit-indicator">✏️</span>
                    Ministry Programs
                </h2>
                <p class="section-subtitle editable" data-id="programs-subtitle">
                    <span class="edit-indicator">✏️</span>
                    Choose from our carefully designed programs to support your spiritual growth journey
                </p>
                
                <div class="programs-grid">
                    <div class="program-card">
                        <div class="program-header">
                            <i class="fas fa-seedling icon-editable"></i>
                            <h3 class="editable" data-id="program1-title">
                                <span class="edit-indicator">✏️</span>
                                Spiritual Foundations
                            </h3>
                            <p class="editable" data-id="program1-desc">
                                <span class="edit-indicator">✏️</span>
                                12-week beginner program
                            </p>
                        </div>
                        <div class="program-content">
                            <ul class="program-features">
                                <li><i class="fas fa-check"></i> <span class="editable" data-id="program1-feature1">Weekly Bible study materials</span></li>
                                <li><i class="fas fa-check"></i> <span class="editable" data-id="program1-feature2">Prayer journal template</span></li>
                                <li><i class="fas fa-check"></i> <span class="editable" data-id="program1-feature3">4 group coaching sessions</span></li>
                                <li><i class="fas fa-check"></i> <span class="editable" data-id="program1-feature4">Access to online community</span></li>
                            </ul>
                            <div class="program-price editable price-editable" data-id="program1-price">
                                <span class="edit-indicator">✏️</span>
                                R1,299
                            </div>
                            <button class="btn" style="width: 100%;" onclick="enrollProgram('spiritual-foundations')">
                                <i class="fas fa-lock"></i> Enroll Now
                            </button>
                        </div>
                    </div>
                    
                    <div class="program-card">
                        <div class="program-header">
                            <i class="fas fa-cross icon-editable"></i>
                            <h3 class="editable" data-id="program2-title">
                                <span class="edit-indicator">✏️</span>
                                Leadership Development
                            </h3>
                            <p class="editable" data-id="program2-desc">
                                <span class="edit-indicator">✏️</span>
                                6-month intensive program
                            </p>
                        </div>
                        <div class="program-content">
                            <ul class="program-features">
                                <li><i class="fas fa-check"></i> <span class="editable" data-id="program2-feature1">Advanced theological training</span></li>
                                <li><i class="fas fa-check"></i> <span class="editable" data-id="program2-feature2">Mentorship from senior leaders</span></li>
                                <li><i class="fas fa-check"></i> <span class="editable" data-id="program2-feature3">Practical ministry experience</span></li>
                                <li><i class="fas fa-check"></i> <span class="editable" data-id="program2-feature4">Leadership certification</span></li>
                            </ul>
                            <div class="program-price editable price-editable" data-id="program2-price">
                                <span class="edit-indicator">✏️</span>
                                R4,999
                            </div>
                            <button class="btn" style="width: 100%;" onclick="enrollProgram('leadership-development')">
                                <i class="fas fa-lock"></i> Enroll Now
                            </button>
                        </div>
                    </div>
                    
                    <div class="program-card">
                        <div class="program-header">
                            <i class="fas fa-heart icon-editable"></i>
                            <h3 class="editable" data-id="program3-title">
                                <span class="edit-indicator">✏️</span>
                                Marriage & Family
                            </h3>
                            <p class="editable" data-id="program3-desc">
                                <span class="edit-indicator">✏️</span>
                                8-week relationship program
                            </p>
                        </div>
                        <div class="program-content">
                            <ul class="program-features">
                                <li><i class="fas fa-check"></i> <span class="editable" data-id="program3-feature1">Couples workbook</span></li>
                                <li><i class="fas fa-check"></i> <span class="editable" data-id="program3-feature2">Weekly video sessions</span></li>
                                <li><i class="fas fa-check"></i> <span class="editable" data-id="program3-feature3">Private counseling sessions</span></li>
                                <li><i class="fas fa-check"></i> <span class="editable" data-id="program3-feature4">Family activity guides</span></li>
                            </ul>
                            <div class="program-price editable price-editable" data-id="program3-price">
                                <span class="edit-indicator">✏️</span>
                                R2,499
                            </div>
                            <button class="btn" style="width: 100%;" onclick="enrollProgram('marriage-family')">
                                <i class="fas fa-lock"></i> Enroll Now
                            </button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Interactive Demo Section -->
            <div class="interactive-demo">
                <h4>Try Our Interactive Features</h4>
                <p>Experience how our programs work with these interactive demos</p>
                <div class="demo-buttons">
                    <button class="btn" onclick="showMinistryTour()">
                        <i class="fas fa-play"></i> Take a Tour
                    </button>
                    <button class="btn btn-secondary" onclick="simulateCoachingSession()">
                        <i class="fas fa-comments"></i> Demo Coaching
                    </button>
                </div>
            </div>

            <!-- Ministry Books -->
            <div class="ministry-books">
                <h2 class="section-title editable" data-id="ministry-books-title">
                    <span class="edit-indicator">✏️</span>
                    Ministry Literature & Resources
                </h2>
                <p class="section-subtitle editable" data-id="ministry-books-subtitle">
                    <span class="edit-indicator">✏️</span>
                    Explore our collection of books, study guides, and resources for spiritual growth
                </p>
                
                <div class="books-slider">
                    <div class="books-track" id="ministryBooksTrack">
                        <!-- Ministry books will be loaded here -->
                    </div>
                </div>
            </div>

            <!-- CTA Section -->
            <div class="ministry-cta">
                <h3 class="editable" data-id="cta-title">
                    <span class="edit-indicator">✏️</span>
                    Ready to Begin Your Transformation?
                </h3>
                <p class="editable" data-id="cta-subtitle">
                    <span class="edit-indicator">✏️</span>
                    Take the first step toward spiritual growth and personal development today. Our team is ready to support you on your journey.
                </p>
                <div class="cta-buttons">
                    <button class="btn" onclick="openCoachingModal()">
                        <i class="fas fa-calendar-alt"></i> Book Free Consultation
                    </button>
                    <button class="btn btn-secondary" onclick="scrollToPrograms()">
                        <i class="fas fa-book-open"></i> Explore All Programs
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Community Section -->
    <section id="community" class="section community-section">
        <div class="container">
            <h2 class="section-title editable" data-id="community-title">
                <span class="edit-indicator">✏️</span>
                Join Our Reading Community
            </h2>
            <p class="section-subtitle editable" data-id="community-subtitle">
                <span class="edit-indicator">✏️</span>
                Connect with fellow readers, share reviews, and discuss your favorite books
            </p>
            
            <div class="community-container">
                <div class="discussion-forum">
                    <h3 class="editable" data-id="forum-title">
                        <span class="edit-indicator">✏️</span>
                        Discussion Forum
                    </h3>
                    <div class="discussion-list" id="discussionList">
                        <!-- Discussions will be loaded here -->
                    </div>
                    <div class="form-group" style="margin-top: 20px;">
                        <input type="text" class="form-control" id="newDiscussion" placeholder="Start a new discussion...">
                        <button class="btn" style="width: 100%; margin-top: 10px;" onclick="addDiscussion()">
                            <i class="fas fa-plus"></i> Post Discussion
                        </button>
                    </div>
                </div>
                
                <div class="user-reviews">
                    <h3 class="editable" data-id="reviews-title">
                        <span class="edit-indicator">✏️</span>
                        Recent Reviews
                    </h3>
                    <div class="reviews-list" id="reviewsList">
                        <!-- Reviews will be loaded here -->
                    </div>
                    <div class="form-group" style="margin-top: 20px;">
                        <select class="form-control" id="reviewBook">
                            <!-- Book options will be loaded here -->
                        </select>
                        <input type="text" class="form-control" id="newReview" placeholder="Write a review..." style="margin-top: 10px;">
                        <div style="display: flex; justify-content: space-between; margin-top: 10px;">
                            <div>
                                <span>Rating: </span>
                                <span class="review-rating" id="reviewStars">
                                    <i class="far fa-star" onclick="setRating(1)"></i>
                                    <i class="far fa-star" onclick="setRating(2)"></i>
                                    <i class="far fa-star" onclick="setRating(3)"></i>
                                    <i class="far fa-star" onclick="setRating(4)"></i>
                                    <i class="far fa-star" onclick="setRating(5)"></i>
                                </span>
                            </div>
                            <button class="btn" onclick="addReview()">
                                <i class="fas fa-pen"></i> Post Review
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Payment Section -->
    <section id="payment" class="section payment-section">
        <div class="container">
            <h2 class="section-title editable" data-id="payment-title">
                <span class="edit-indicator">✏️</span>
                Secure Payment
            </h2>
            <p class="section-subtitle editable" data-id="payment-subtitle">
                <span class="edit-indicator">✏️</span>
                Complete your purchase with our secure payment system
            </p>
            
            <div class="payment-container">
                <h3 class="editable" data-id="checkout-title">
                    <span class="edit-indicator">✏️</span>
                    Checkout
                </h3>
                
                <div class="payment-methods">
                    <div class="payment-method active" onclick="selectPaymentMethod('credit')">
                        <i class="far fa-credit-card"></i>
                        <p>Credit Card</p>
                    </div>
                    <div class="payment-method" onclick="selectPaymentMethod('paypal')">
                        <i class="fab fa-paypal"></i>
                        <p>PayPal</p>
                    </div>
                    <div class="payment-method" onclick="selectPaymentMethod('bank')">
                        <i class="fas fa-university"></i>
                        <p>Bank Transfer</p>
                    </div>
                </div>
                
                <div class="payment-form" id="creditCardForm">
                    <div class="form-group">
                        <label for="cardNumber" class="editable" data-id="card-number">
                            <span class="edit-indicator">✏️</span>
                            Card Number
                        </label>
                        <input type="text" id="cardNumber" class="form-control" placeholder="1234 5678 9012 3456">
                    </div>
                    
                    <div class="form-row">
                        <div class="form-group">
                            <label for="expiryDate" class="editable" data-id="expiry-date">
                                <span class="edit-indicator">✏️</span>
                                Expiry Date
                            </label>
                            <input type="text" id="expiryDate" class="form-control" placeholder="MM/YY">
                        </div>
                        
                        <div class="form-group">
                            <label for="cvv" class="editable" data-id="cvv">
                                <span class="edit-indicator">✏️</span>
                                CVV
                            </label>
                            <input type="text" id="cvv" class="form-control" placeholder="123">
                        </div>
                    </div>
                    
                    <div class="form-group">
                        <label for="cardName" class="editable" data-id="card-name">
                            <span class="edit-indicator">✏️</span>
                            Name on Card
                        </label>
                        <input type="text" id="cardName" class="form-control" placeholder="John Doe">
                    </div>
                    
                    <button class="btn" style="width: 100%; margin-top: 20px;" onclick="processPayment()">
                        <i class="fas fa-lock"></i>
                        <span class="editable" data-id="pay-now">
                            <span class="edit-indicator">✏️</span>
                            Pay Now
                        </span>
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- About Us Section -->
    <section id="about" class="section about-section">
        <div class="container">
            <h2 class="section-title editable" data-id="about-title">
                <span class="edit-indicator">✏️</span>
                Our Story
            </h2>
            
            <div class="about-content">
                <div class="about-text editable" data-id="about-text-1">
                    <span class="edit-indicator">✏️</span>
                    The Definitive Word was born in South Africa with a passion for connecting readers with transformative literature. We believe that every great book has the power to change perspectives and inspire growth.
                </div>
                
                <div class="about-text editable" data-id="about-text-2">
                    <span class="edit-indicator">✏️</span>
                    Our team carefully selects each title, focusing on quality writing, compelling storytelling, and meaningful impact. We're proud to support both local South African authors and international literary excellence.
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
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
                        South Africa's premier destination for quality ebooks and exceptional reading experiences.
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
                        Quick Links
                    </h3>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#books">Books</a></li>
                        <li><a href="#blog">Blog</a></li>
                        <li><a href="#ministry">Ministry</a></li>
                        <li><a href="#community">Community</a></li>
                        <li><a href="#payment">Payment</a></li>
                        <li><a href="#about">About Us</a></li>
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
                    &copy; 2023 The Definitive Word. All rights reserved.
                </p>
            </div>
        </div>
    </footer>

    <!-- Context Menu -->
    <div class="context-menu" id="contextMenu">
        <div class="context-menu-item" onclick="editElement()">
            <i class="fas fa-edit"></i>
            <span>Edit Content</span>
        </div>
        <div class="context-menu-item" onclick="toggleEditMode()">
            <i class="fas fa-magic"></i>
            <span id="toggleEditText">Enable Edit Mode</span>
        </div>
        <div class="context-menu-item" onclick="saveAllContent()">
            <i class="fas fa-save"></i>
            <span>Save Changes</span>
        </div>
        <div class="context-menu-item" onclick="resetToDefault()">
            <i class="fas fa-undo"></i>
            <span>Reset to Default</span>
        </div>
    </div>

    <!-- Edit Modal -->
    <div class="edit-modal" id="editModal">
        <div class="modal-content">
            <div class="modal-header">
                <h2 id="editModalTitle">Edit Content</h2>
                <button class="close-modal" onclick="closeEditModal()">&times;</button>
            </div>
            <div class="modal-body">
                <textarea id="editModalTextarea"></textarea>
            </div>
            <div class="modal-footer">
                <button class="modal-btn secondary" onclick="closeEditModal()">Cancel</button>
                <button class="modal-btn primary" onclick="saveEdit()">Save Changes</button>
            </div>
        </div>
    </div>

    <!-- Cart Modal -->
    <div class="cart-modal" id="cartModal">
        <div class="cart-header">
            <h3>Your Cart</h3>
            <button class="close-modal" onclick="toggleCart()">&times;</button>
        </div>
        <div class="cart-items" id="cartItems">
            <!-- Cart items will be loaded here -->
        </div>
        <div class="cart-total">
            <span>Total:</span>
            <span id="cartTotal">R0.00</span>
        </div>
        <button class="btn" style="width: 100%;" onclick="proceedToCheckout()">
            <i class="fas fa-credit-card"></i> Proceed to Checkout
        </button>
    </div>

    <!-- Login Modal -->
    <div class="edit-modal" id="loginModal">
        <div class="modal-content">
            <div class="modal-header">
                <h2>Login to Your Account</h2>
                <button class="close-modal" onclick="toggleLogin()">&times;</button>
            </div>
            <div class="modal-body">
                <div class="form-group">
                    <label for="loginEmail">Email Address</label>
                    <input type="email" id="loginEmail" class="form-control" placeholder="your@email.com">
                </div>
                <div class="form-group">
                    <label for="loginPassword">Password</label>
                    <input type="password" id="loginPassword" class="form-control" placeholder="Your password">
                </div>
                <div style="text-align: center; margin-top: 20px;">
                    <p>Don't have an account? <a href="#" style="color: #d69e2e;">Sign up here</a></p>
                </div>
            </div>
            <div class="modal-footer">
                <button class="modal-btn secondary" onclick="toggleLogin()">Cancel</button>
                <button class="modal-btn primary" onclick="performLogin()">Login</button>
            </div>
        </div>
    </div>

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

    <!-- Notification -->
    <div class="notification" id="notification"></div>

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
        let contextMenuElement = null;
        let currentProgram = null;
        let currentEnrollmentStep = 1;
        const totalEnrollmentSteps = 3;

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
            },
            {
                id: 4,
                title: "African Skies",
                author: "Tendai Moyo", 
                price: 279.99,
                image: "https://images.unsplash.com/photo-1481627834876-b7833e8f5570?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                badge: "Local Author",
                description: "A captivating novel set against the backdrop of contemporary South Africa."
            },
            {
                id: 5,
                title: "Mindful Living",
                author: "James Wilson", 
                price: 229.99,
                image: "https://images.unsplash.com/photo-1506880018603-83d5b814b5a6?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                badge: "",
                description: "Practical techniques for finding peace and purpose in a busy world."
            },
            {
                id: 6,
                title: "Culinary Journey",
                author: "Maria Rodriguez", 
                price: 319.99,
                image: "https://images.unsplash.com/photo-1544716278-ca5e3f4abd8c?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                badge: "Featured",
                description: "Explore world cuisines with these delicious and accessible recipes."
            }
        ];

        // Ministry books data
        const ministryBooks = [
            {
                id: 101,
                title: "The Path to Spiritual Maturity",
                author: "Dr. Michael Johnson", 
                price: 299.99,
                image: "https://images.unsplash.com/photo-1544947950-fa07a98d237f?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                description: "A comprehensive guide to deepening your spiritual walk and understanding biblical principles for growth."
            },
            {
                id: 102,
                title: "Prayer That Changes Everything",
                author: "Sarah Williams",
                price: 249.99,
                image: "https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                description: "Discover the power of prayer and how to develop a consistent prayer life that transforms your circumstances."
            },
            {
                id: 103,
                title: "Biblical Leadership Principles",
                author: "Pastor David Chen", 
                price: 349.99,
                image: "https://images.unsplash.com/photo-1512820790803-83ca734da794?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                description: "Learn leadership skills and wisdom from the Bible that apply to church, family, and workplace settings."
            },
            {
                id: 104,
                title: "Healing from Within",
                author: "Dr. Rebecca Martinez", 
                price: 279.99,
                image: "https://images.unsplash.com/photo-1481627834876-b7833e8f5570?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                description: "A Christian approach to emotional healing and overcoming past trauma through faith and counseling."
            },
            {
                id: 105,
                title: "The Generous Life",
                author: "Financial Ministry Team", 
                price: 229.99,
                image: "https://images.unsplash.com/photo-1506880018603-83d5b814b5a6?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                description: "Biblical principles for financial stewardship, generosity, and managing resources God's way."
            },
            {
                id: 106,
                title: "Family Foundations",
                author: "The Relationship Coaches", 
                price: 319.99,
                image: "https://images.unsplash.com/photo-1544716278-ca5e3f4abd8c?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80",
                description: "Building strong Christian families through biblical values, communication, and relationship skills."
            }
        ];

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

        // Sample blog data
        const sampleBlogPosts = [
            {
                id: 1,
                title: "The Rise of African Literature in the Global Market",
                excerpt: "Exploring how African authors are making their mark on the international literary scene and what it means for the future of publishing.",
                content: "Full content would go here...",
                author: "Nomvula Kalenga",
                date: "2023-07-15",
                category: "Literature",
                image: "https://images.unsplash.com/photo-1481627834876-b7833e8f5570?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                tags: ["african literature", "publishing", "global market"],
                likes: 24,
                comments: 8
            }
        ];

        const sampleCategories = [
            { name: "Literature", count: 12 },
            { name: "Recommendations", count: 8 }
        ];

        const sampleTags = [
            "fiction", "non-fiction", "south africa", "african literature"
        ];

        // Sample discussions and reviews
        const sampleDiscussions = [
            {
                id: 1,
                title: "What's your favorite book of 2023 so far?",
                author: "BookLover42",
                date: "2023-07-15",
                replies: 12
            }
        ];

        const sampleReviews = [
            {
                id: 1,
                bookTitle: "The Silent Observer",
                author: "CriticalReader",
                rating: 5,
                text: "Absolutely gripping from start to finish! The character development was exceptional.",
                date: "2023-07-12"
            }
        ];

        // Initialize the application
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
            setupInteractiveElements();
            showNotification('🌟 Welcome! Explore our interactive features - click around to see everything in action!');
        }

        // Setup all interactive elements
        function setupInteractiveElements() {
            setupTabNavigation();
            setupReadingProgress();
        }

        // Enhanced tab navigation
        function setupTabNavigation() {
            const navLinks = document.querySelectorAll('.nav-link');
            
            navLinks.forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    const targetId = this.getAttribute('href').substring(1);
                    
                    // Update active state
                    navLinks.forEach(nl => nl.classList.remove('active'));
                    this.classList.add('active');
                    
                    // Scroll to section with smooth animation
                    document.getElementById(targetId).scrollIntoView({
                        behavior: 'smooth'
                    });
                    
                    // Add visual feedback
                    this.style.transform = 'scale(0.95)';
                    setTimeout(() => {
                        this.style.transform = 'scale(1)';
                    }, 150);
                });
            });
        }

        // Setup edit interactions
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
            });

            // Right-click context menu
            document.addEventListener('contextmenu', function(e) {
                const editable = e.target.closest('.editable');
                if (editable) {
                    e.preventDefault();
                    showContextMenu(e, editable);
                }
            });

            // Click to hide context menu
            document.addEventListener('click', function() {
                hideContextMenu();
            });

            // Keyboard shortcuts
            document.addEventListener('keydown', function(e) {
                // Ctrl+E to toggle edit mode
                if (e.ctrlKey && e.key === 'e') {
                    e.preventDefault();
                    toggleEditMode();
                }
                
                // Escape to close modals
                if (e.key === 'Escape') {
                    closeEditModal();
                    hideContextMenu();
                    toggleCart(false);
                    toggleLogin(false);
                    closeEnrollmentModal();
                }
            });
        }

        // Toggle edit mode
        function toggleEditMode() {
            editMode = !editMode;
            document.body.classList.toggle('edit-mode-on', editMode);
            document.getElementById('editModeIndicator').classList.toggle('active', editMode);
            document.getElementById('toggleEditText').textContent = editMode ? 'Disable Edit Mode' : 'Enable Edit Mode';
            
            if (editMode) {
                showNotification('Edit mode activated. Double-click any text to edit.');
            } else {
                showNotification('Edit mode deactivated.');
            }
        }

        // Show context menu
        function showContextMenu(e, element) {
            contextMenuElement = element;
            const contextMenu = document.getElementById('contextMenu');
            contextMenu.style.left = e.pageX + 'px';
            contextMenu.style.top = e.pageY + 'px';
            contextMenu.classList.add('active');
        }

        // Hide context menu
        function hideContextMenu() {
            document.getElementById('contextMenu').classList.remove('active');
        }

        // Open edit modal
        function openEditModal(element) {
            currentEditingElement = element;
            const modal = document.getElementById('editModal');
            const textarea = document.getElementById('editModalTextarea');
            
            // Get the text content (excluding the edit indicator)
            let content = '';
            for (let node of element.childNodes) {
                if (node.nodeType === Node.TEXT_NODE) {
                    content += node.textContent;
                } else if (node.classList && !node.classList.contains('edit-indicator')) {
                    content += node.textContent;
                }
            }
            
            textarea.value = content.trim();
            modal.classList.add('active');
        }

        // Close edit modal
        function closeEditModal() {
            document.getElementById('editModal').classList.remove('active');
            currentEditingElement = null;
        }

        // Save edit
        function saveEdit() {
            if (!currentEditingElement) return;
            
            const textarea = document.getElementById('editModalTextarea');
            const newContent = textarea.value;
            
            // Preserve the edit indicator
            const indicator = currentEditingElement.querySelector('.edit-indicator');
            currentEditingElement.innerHTML = '';
            if (indicator) {
                currentEditingElement.appendChild(indicator);
            }
            currentEditingElement.appendChild(document.createTextNode(newContent));
            
            saveAllContent();
            closeEditModal();
            showNotification('Content updated successfully!');
        }

        // Save all content to localStorage
        function saveAllContent() {
            const editableElements = document.querySelectorAll('.editable');
            const contentData = {};
            
            editableElements.forEach(element => {
                const id = element.getAttribute('data-id');
                if (id) {
                    // Get text content without the edit indicator
                    let content = '';
                    for (let node of element.childNodes) {
                        if (node.nodeType === Node.TEXT_NODE) {
                            content += node.textContent;
                        } else if (node.classList && !node.classList.contains('edit-indicator')) {
                            content += node.textContent;
                        }
                    }
                    contentData[id] = content.trim();
                }
            });
            
            localStorage.setItem('ebookStoreContent', JSON.stringify(contentData));
        }

        // Load all content from localStorage
        function loadAllContent() {
            const savedContent = localStorage.getItem('ebookStoreContent');
            if (savedContent) {
                const contentData = JSON.parse(savedContent);
                
                Object.keys(contentData).forEach(id => {
                    const element = document.querySelector(`[data-id="${id}"]`);
                    if (element) {
                        const indicator = element.querySelector('.edit-indicator');
                        element.innerHTML = '';
                        if (indicator) {
                            element.appendChild(indicator);
                        }
                        element.appendChild(document.createTextNode(contentData[id]));
                    }
                });
            }
        }

        // Reset to default content
        function resetToDefault() {
            if (confirm('Are you sure you want to reset all content to default? This cannot be undone.')) {
                localStorage.removeItem('ebookStoreContent');
                location.reload();
            }
        }

        // Show notification
        function showNotification(message, duration = 3000) {
            const notification = document.getElementById('notification');
            notification.textContent = message;
            notification.classList.add('show');
            
            setTimeout(() => {
                notification.classList.remove('show');
            }, duration);
        }

        // Display books
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
                        <div class="reading-progress">
                            <div class="reading-progress-bar" style="width: 0%"></div>
                        </div>
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

        function simulateReading(bookCard) {
            const progressBar = bookCard.querySelector('.reading-progress-bar');
            if (!progressBar) return;
            
            let progress = parseInt(progressBar.style.width) || 0;
            if (progress < 100) {
                progress += 25;
                if (progress > 100) progress = 100;
                progressBar.style.width = `${progress}%`;
                
                if (progress === 100) {
                    showNotification('🎉 You finished reading this book!', 3000);
                } else {
                    showNotification(`📖 Reading progress: ${progress}%`, 2000);
                }
            }
        }

        // Initialize ministry section
        function initMinistrySection() {
            displayMinistryBooks();
        }

        // Display ministry books
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

        // Enhanced enrollment functionality
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

        // Ministry interactive functions
        function scrollToPrograms() {
            document.querySelector('.ministry-programs').scrollIntoView({ 
                behavior: 'smooth' 
            });
        }

        function openCoachingModal() {
            if (!currentUser) {
                showNotification('Please login to book a consultation');
                toggleLogin(true);
                return;
            }
            showNotification('Consultation booking feature would open here');
        }

        function showMinistryTour() {
            showNotification('🚀 Starting ministry tour...', 2000);
            
            const sections = ['ministry-programs', 'life-coaching', 'ministry-books'];
            let current = 0;
            
            const tourInterval = setInterval(() => {
                if (current < sections.length) {
                    const section = document.querySelector(`.${sections[current]}`);
                    if (section) {
                        section.style.boxShadow = '0 0 0 3px #d69e2e';
                        section.scrollIntoView({ behavior: 'smooth', block: 'center' });
                        
                        setTimeout(() => {
                            section.style.boxShadow = '';
                        }, 2000);
                    }
                    current++;
                } else {
                    clearInterval(tourInterval);
                    showNotification('🎊 Tour completed! Explore each section in detail.', 4000);
                }
            }, 2500);
        }

        function simulateCoachingSession() {
            const questions = [
                "What area of your life would you like to improve?",
                "How can we support your spiritual growth journey?"
            ];
            
            let currentQuestion = 0;
            
            function askNextQuestion() {
                if (currentQuestion < questions.length) {
                    const response = prompt(questions[currentQuestion]);
                    if (response !== null) {
                        showNotification(`✓ Thank you for sharing: "${response.substring(0, 50)}..."`, 3000);
                        currentQuestion++;
                        setTimeout(askNextQuestion, 2000);
                    }
                } else {
                    showNotification('🎯 Based on your responses, we\'ve created a personalized coaching plan for you!', 5000);
                }
            }
            
            askNextQuestion();
        }

        // Cart functionality
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

        function removeFromCart(bookId) {
            cart = cart.filter(item => item.id !== bookId);
            saveCart();
            updateCartDisplay();
            showNotification('Item removed from cart');
        }

        function saveCart() {
            localStorage.setItem('ebookStoreCart', JSON.stringify(cart));
        }

        function loadCart() {
            const savedCart = localStorage.getItem('ebookStoreCart');
            if (savedCart) {
                cart = JSON.parse(savedCart);
            }
        }

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

        function toggleCart(show) {
            const cartModal = document.getElementById('cartModal');
            if (show !== undefined) {
                cartModal.classList.toggle('active', show);
            } else {
                cartModal.classList.toggle('active');
            }
        }

        function proceedToCheckout() {
            if (cart.length === 0) {
                showNotification('Your cart is empty!');
                return;
            }
            
            toggleCart(false);
            document.getElementById('payment').scrollIntoView({ behavior: 'smooth' });
            showNotification('Proceeding to checkout...');
        }

        // Login functionality
        function toggleLogin(show) {
            const loginModal = document.getElementById('loginModal');
            if (show !== undefined) {
                loginModal.classList.toggle('active', show);
            } else {
                loginModal.classList.toggle('active');
            }
        }

        function performLogin() {
            const email = document.getElementById('loginEmail').value;
            const password = document.getElementById('loginPassword').value;
            
            if (email && password) {
                // Show loading state
                const button = document.querySelector('#loginModal .modal-btn.primary');
                const originalText = button.textContent;
                button.innerHTML = '<i class="fas fa-spinner fa-spin"></i> Signing in...';
                
                setTimeout(() => {
                    currentUser = { 
                        email, 
                        name: email.split('@')[0],
                        joined: new Date().toLocaleDateString()
                    };
                    
                    document.getElementById('loginBtn').innerHTML = `<i class="fas fa-user"></i> ${currentUser.name}`;
                    
                    // Update login button in header
                    const loginBtn = document.getElementById('loginBtn');
                    loginBtn.innerHTML = `<i class="fas fa-user-check"></i> ${currentUser.name}`;
                    loginBtn.style.background = '#38a169';
                    
                    toggleLogin(false);
                    showNotification(`🎊 Welcome back, ${currentUser.name}! You now have access to all features.`, 4000);
                    
                    // Reset button
                    button.textContent = originalText;
                }, 1500);
            } else {
                showNotification('Please enter both email and password');
            }
        }

        // Community functionality
        function loadCommunityData() {
            discussions = [...sampleDiscussions];
            reviews = [...sampleReviews];
            displayDiscussions();
            displayReviews();
        }

        function displayDiscussions() {
            const discussionList = document.getElementById('discussionList');
            discussionList.innerHTML = '';
            
            discussions.forEach(discussion => {
                const discussionItem = document.createElement('div');
                discussionItem.className = 'discussion-item';
                discussionItem.innerHTML = `
                    <h4>${discussion.title}</h4>
                    <div class="discussion-meta">
                        <span>by ${discussion.author}</span>
                        <span>${discussion.replies} replies</span>
                    </div>
                `;
                discussionList.appendChild(discussionItem);
            });
        }

        function displayReviews() {
            const reviewsList = document.getElementById('reviewsList');
            reviewsList.innerHTML = '';
            
            reviews.forEach(review => {
                const reviewItem = document.createElement('div');
                reviewItem.className = 'review-item';
                reviewItem.innerHTML = `
                    <div class="review-header">
                        <strong>${review.bookTitle}</strong>
                        <div class="review-rating">
                            ${'★'.repeat(review.rating)}${'☆'.repeat(5 - review.rating)}
                        </div>
                    </div>
                    <p>${review.text}</p>
                    <div class="discussion-meta">
                        <span>by ${review.author}</span>
                    </div>
                `;
                reviewsList.appendChild(reviewItem);
            });
        }

        function addDiscussion() {
            const newDiscussionInput = document.getElementById('newDiscussion');
            const title = newDiscussionInput.value.trim();
            
            if (title && currentUser) {
                discussions.unshift({
                    id: discussions.length + 1,
                    title,
                    author: currentUser.name,
                    date: new Date().toISOString().split('T')[0],
                    replies: 0
                });
                
                newDiscussionInput.value = '';
                displayDiscussions();
                showNotification('Discussion posted!');
            } else if (!currentUser) {
                showNotification('Please login to post a discussion');
                toggleLogin(true);
            } else {
                showNotification('Please enter a discussion topic');
            }
        }

        function setRating(stars) {
            currentRating = stars;
            const starsElements = document.querySelectorAll('#reviewStars i');
            
            starsElements.forEach((star, index) => {
                if (index < stars) {
                    star.className = 'fas fa-star';
                } else {
                    star.className = 'far fa-star';
                }
            });
        }

        function addReview() {
            const newReviewInput = document.getElementById('newReview');
            const text = newReviewInput.value.trim();
            
            if (text && currentRating > 0 && currentUser) {
                reviews.unshift({
                    id: reviews.length + 1,
                    bookTitle: 'Recent Purchase',
                    author: currentUser.name,
                    rating: currentRating,
                    text,
                    date: new Date().toISOString().split('T')[0]
                });
                
                newReviewInput.value = '';
                setRating(0);
                displayReviews();
                showNotification('Review posted!');
            } else if (!currentUser) {
                showNotification('Please login to post a review');
                toggleLogin(true);
            } else if (currentRating === 0) {
                showNotification('Please select a rating');
            } else {
                showNotification('Please enter your review');
            }
        }

        // Blog functionality
        function loadBlogData() {
            blogPosts = [...sampleBlogPosts];
            categories = [...sampleCategories];
            tags = [...sampleTags];
            displayBlogPosts();
            displayCategories();
            displayRecentPosts();
            displayTags();
        }

        function displayBlogPosts() {
            const blogPostsContainer = document.getElementById('blogPosts');
            blogPostsContainer.innerHTML = '';
            
            blogPosts.forEach(post => {
                const postElement = document.createElement('article');
                postElement.className = 'blog-post';
                postElement.innerHTML = `
                    <div class="blog-post-image">
                        <img src="${post.image}" alt="${post.title}">
                    </div>
                    <div class="blog-post-content">
                        <div class="blog-post-meta">
                            <span class="blog-post-category">${post.category}</span>
                            <span><i class="far fa-calendar"></i> ${post.date}</span>
                            <span><i class="far fa-user"></i> ${post.author}</span>
                        </div>
                        <h3 class="blog-post-title">${post.title}</h3>
                        <p class="blog-post-excerpt">${post.excerpt}</p>
                        <div class="blog-post-footer">
                            <div class="blog-post-actions">
                                <button><i class="far fa-heart"></i> ${post.likes}</button>
                                <button><i class="far fa-comment"></i> ${post.comments}</button>
                            </div>
                            <a href="#" class="btn" style="padding: 8px 15px;">Read More</a>
                        </div>
                    </div>
                `;
                blogPostsContainer.appendChild(postElement);
            });
        }

        function displayCategories() {
            const categoriesList = document.getElementById('categoriesList');
            categoriesList.innerHTML = '';
            
            categories.forEach(category => {
                const li = document.createElement('li');
                li.innerHTML = `
                    <a href="#">
                        ${category.name}
                        <span>${category.count}</span>
                    </a>
                `;
                categoriesList.appendChild(li);
            });
        }

        function displayRecentPosts() {
            const recentPostsList = document.getElementById('recentPostsList');
            recentPostsList.innerHTML = '';
            
            blogPosts.slice(0, 3).forEach(post => {
                const li = document.createElement('li');
                li.innerHTML = `
                    <div class="recent-post">
                        <div class="recent-post-image">
                            <img src="${post.image}" alt="${post.title}">
                        </div>
                        <div class="recent-post-content">
                            <h4>${post.title}</h4>
                            <div class="post-date">${post.date}</div>
                        </div>
                    </div>
                `;
                recentPostsList.appendChild(li);
            });
        }

        function displayTags() {
            const tagsCloud = document.getElementById('tagsCloud');
            tagsCloud.innerHTML = '';
            
            tags.forEach(tag => {
                const span = document.createElement('span');
                span.className = 'tag';
                span.textContent = tag;
                tagsCloud.appendChild(span);
            });
        }

        // Payment functionality
        function selectPaymentMethod(method) {
            document.querySelectorAll('.payment-method').forEach(el => {
                el.classList.remove('active');
            });
            
            event.currentTarget.classList.add('active');
        }

        function processPayment() {
            if (cart.length === 0) {
                showNotification('Your cart is empty!');
                return;
            }
            
            // Show processing animation
            const button = document.querySelector('#creditCardForm .btn');
            const originalText = button.innerHTML;
            button.innerHTML = '<i class="fas fa-spinner fa-spin"></i> Processing Payment...';
            button.disabled = true;
            
            // Simulate payment processing
            setTimeout(() => {
                cart = [];
                saveCart();
                updateCartDisplay();
                
                button.innerHTML = '<i class="fas fa-check"></i> Payment Successful!';
                button.style.background = '#38a169';
                
                showNotification('🎉 Payment successful! Thank you for your purchase. Your books are available for download.', 5000);
                
                // Reset button after delay
                setTimeout(() => {
                    button.innerHTML = originalText;
                    button.disabled = false;
                    button.style.background = '';
                }, 3000);
            }, 3000);
        }

        // Price editing functionality
        function editPrice(priceElement) {
            const currentPrice = priceElement.textContent.replace('R', '').replace(',', '').trim();
            const newPrice = prompt('Enter new price (e.g., 249.99):', currentPrice);
            
            if (newPrice && !isNaN(parseFloat(newPrice))) {
                priceElement.textContent = `R${parseFloat(newPrice).toFixed(2)}`;
                showNotification('Price updated successfully!');
            } else if (newPrice !== null) {
                showNotification('Please enter a valid price');
            }
        }

        // Reading progress simulation
        function setupReadingProgress() {
            // Already implemented in displayBooks function
        }

        // Initialize the application when DOM is loaded
        document.addEventListener('DOMContentLoaded', initApp);
    </script>
</body>
</html>

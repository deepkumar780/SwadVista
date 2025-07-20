<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SwadVista | Authentic Indian Cuisine</title>
    <style>
        :root {
            --saffron: #FF9933;
            --green: #138808;
            --white: #FFFFFF;
            --dark-red: #AA3939;
            --gold: #FFD700;
            --spice-brown: #8B4513;
            --dark-gray: #333333;
            --light-gray: #F5F5F5;
            --turmeric-yellow: #FFC324;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', 'Noto Sans Devanagari', sans-serif;
        }

        body {
            background-color: var(--light-gray);
            color: var(--dark-gray);
            line-height: 1.6;
        }

        @font-face {
            font-family: 'Noto Sans Devanagari';
            src: url('https://fonts.googleapis.com/css2?family=Noto+Sans+Devanagari:wght@400;700&display=swap');
        }

        header {
            background: linear-gradient(to right, var(--saffron), var(--white), var(--green));
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            z-index: 1000;
            padding: 0.5rem 2rem;
            border-bottom: 3px solid var(--gold);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--dark-red);
            text-decoration: none;
            display: flex;
            align-items: center;
            font-family: 'Noto Sans Devanagari', 'Poppins', sans-serif;
        }

        .logo img {
            margin-right: 10px;
            height: 50px;
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 1.5rem;
            position: relative;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--dark-gray);
            font-weight: 600;
            transition: all 0.3s ease;
            padding: 0.5rem 0;
            font-family: 'Noto Sans Devanagari', 'Poppins', sans-serif;
        }

        .nav-links a:hover {
            color: var(--dark-red);
        }

        .nav-links a:after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            background: var(--dark-red);
            bottom: 0;
            left: 0;
            transition: all 0.3s ease;
        }

        .nav-links a:hover:after {
            width: 100%;
        }

        .auth-buttons {
            display: flex;
            align-items: center;
        }

        .btn {
            padding: 0.6rem 1.2rem;
            border-radius: 25px;
            border: none;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s ease;
            font-family: 'Noto Sans Devanagari', 'Poppins', sans-serif;
        }

        .btn-primary {
            background-color: var(--dark-red);
            color: white;
            margin-left: 1rem;
            box-shadow: 0 4px 8px rgba(170, 57, 57, 0.2);
        }

        .btn-secondary {
            background-color: transparent;
            color: var(--dark-red);
            border: 2px solid var(--dark-red);
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
        }

        .btn-primary:hover {
            background-color: #8a2a2a;
        }

        .btn-secondary:hover {
            background-color: rgba(170, 57, 57, 0.1);
        }

        main {
            padding-top: 90px;
        }

        section {
            padding: 4rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)), url('https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/8d1c4c16-166a-4561-8df5-d2d3d3d5f370.png');
            background-size: cover;
            background-position: center;
            color: white;
            text-align: center;
            height: 80vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            margin-bottom: 3rem;
            border-radius: 10px;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, var(--saffron), var(--green));
            opacity: 0.3;
            z-index: 0;
        }

        .hero-content {
            position: relative;
            z-index: 1;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
            font-family: 'Noto Sans Devanagari', 'Poppins', sans-serif;
        }

        .hero h1 span {
            color: var(--gold);
        }

        .hero p {
            font-size: 1.3rem;
            max-width: 700px;
            margin-bottom: 2rem;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
            line-height: 1.8;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            font-size: 2.5rem;
            color: var(--dark-red);
            position: relative;
            font-family: 'Noto Sans Devanagari', 'Poppins', sans-serif;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 100px;
            height: 4px;
            background: linear-gradient(to right, var(--saffron), var(--green));
            margin: 0.5rem auto 0;
            border-radius: 2px;
        }

        .menu-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .menu-item {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 153, 51, 0.3);
            position: relative;
        }

        .menu-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
            border-color: var(--saffron);
        }

        .veg-mark {
            position: absolute;
            top: 10px;
            right: 10px;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background-color: var(--green);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 12px;
            font-weight: bold;
        }

        .menu-item img {
            width: 100%;
            height: 220px;
            object-fit: cover;
            border-bottom: 2px solid var(--gold);
        }

        .menu-item-content {
            padding: 1.5rem;
        }

        .menu-item h3 {
            margin-bottom: 0.5rem;
            font-size: 1.4rem;
            color: var(--dark-red);
            font-family: 'Noto Sans Devanagari', 'Poppins', sans-serif;
        }

        .menu-item p {
            color: var(--dark-gray);
            margin-bottom: 1rem;
            font-size: 0.95rem;
        }

        .price {
            font-weight: 700;
            color: var(--saffron);
            font-size: 1.3rem;
        }

        .price span {
            color: var(--dark-gray);
            font-size: 0.9rem;
            text-decoration: line-through;
            margin-left: 5px;
        }

        .about-content {
            display: flex;
            align-items: center;
            gap: 3rem;
            flex-wrap: wrap;
        }

        .about-text {
            flex: 1;
            min-width: 300px;
        }

        .about-text h3 {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            color: var(--dark-red);
            font-family: 'Noto Sans Devanagari', 'Poppins', sans-serif;
        }

        .about-text p {
            margin-bottom: 1.5rem;
            line-height: 1.8;
        }

        .about-image {
            flex: 1;
            min-width: 300px;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
            border: 5px solid var(--gold);
        }

        .about-image img {
            width: 100%;
            height: auto;
            display: block;
        }

        .contact-form {
            max-width: 600px;
            margin: 0 auto;
            background: white;
            padding: 2.5rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            border-top: 5px solid var(--dark-red);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: var(--dark-gray);
            font-family: 'Noto Sans Devanagari', 'Poppins', sans-serif;
        }

        .form-control {
            width: 100%;
            padding: 0.8rem 1rem;
            border: 2px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            transition: all 0.3s ease;
            font-family: 'Noto Sans Devanagari', 'Poppins', sans-serif;
        }

        .form-control:focus {
            outline: none;
            border-color: var(--dark-red);
            box-shadow: 0 0 0 3px rgba(170, 57, 57, 0.2);
        }

        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }

        footer {
            background: linear-gradient(to right, var(--saffron), var(--green));
            color: white;
            padding: 4rem 2rem 2rem;
            text-align: center;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 3rem;
            text-align: left;
            align-items: flex-start;
        }

        .footer-column h3 {
            font-size: 1.4rem;
            margin-bottom: 1.5rem;
            color: white;
            position: relative;
            padding-bottom: 10px;
            font-family: 'Noto Sans Devanagari', 'Poppins', sans-serif;
        }

        .footer-column h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 3px;
            background-color: var(--gold);
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
        }

        .footer-column ul li::before {
            content: '→';
            margin-right: 8px;
            color: var(--gold);
            font-weight: bold;
        }

        .footer-column a {
            color: rgba(255, 255, 255, 0.9);
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .footer-column a:hover {
            color: var(--gold);
            padding-left: 5px;
        }

        .footer-column p {
            margin-bottom: 1.5rem;
            line-height: 1.8;
            opacity: 0.9;
        }

        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1.5rem;
        }

        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: rgba(255, 255, 255, 0.1);
            color: white;
            transition: all 0.3s ease;
            font-size: 1.1rem;
        }

        .social-links a:hover {
            background-color: var(--gold);
            color: var(--dark-gray);
            transform: translateY(-3px) scale(1.1);
        }

        .copyright {
            margin-top: 3rem;
            padding-top: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.2);
            font-size: 0.9rem;
            color: rgba(255, 255, 255, 0.7);
        }

        /* Modal styles */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            z-index: 2000;
            justify-content: center;
            align-items: center;
            backdrop-filter: blur(5px);
        }

        .modal-content {
            background-color: white;
            border-radius: 10px;
            width: 95%;
            max-width: 450px;
            padding: 2.5rem;
            position: relative;
            animation: modalOpen 0.4s ease;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
            border-top: 5px solid var(--dark-red);
        }

        @keyframes modalOpen {
            from {
                opacity: 0;
                transform: translateY(-50px) scale(0.9);
            }
            to {
                opacity: 1;
                transform: translateY(0) scale(1);
            }
        }

        .close-btn {
            position: absolute;
            top: 1rem;
            right: 1rem;
            font-size: 1.8rem;
            cursor: pointer;
            color: #666;
            background: none;
            border: none;
            transition: all 0.3s ease;
            width: 40px;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
        }

        .close-btn:hover {
            color: var(--dark-red);
            transform: rotate(90deg);
            background-color: rgba(170, 57, 57, 0.1);
        }

        .modal-title {
            margin-bottom: 2rem;
            color: var(--dark-red);
            text-align: center;
            font-size: 1.8rem;
            font-family: 'Noto Sans Devanagari', 'Poppins', sans-serif;
            position: relative;
            padding-bottom: 10px;
        }

        .modal-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background: linear-gradient(to right, var(--saffron), var(--green));
        }

        .form-footer {
            margin-top: 1.5rem;
            text-align: center;
            font-size: 0.95rem;
        }

        .form-footer a {
            color: var(--dark-red);
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .form-footer a:hover {
            color: var(--saffron);
            text-decoration: underline;
        }

        .form-note {
            font-size: 0.85rem;
            color: #666;
            margin-top: 0.5rem;
            display: block;
        }

        /* Responsive styles */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .nav-links {
                display: none;
            }

            .mobile-menu-btn {
                display: block;
                background: none;
                border: none;
                color: var(--dark-gray);
                font-size: 1.8rem;
                cursor: pointer;
            }

            .about-content {
                flex-direction: column;
            }
            
            .section-title {
                font-size: 2rem;
            }
            
            .menu-item {
                margin-bottom: 2rem;
            }
            
            footer {
                padding: 3rem 1.5rem 1.5rem;
            }
            
            .footer-content {
                grid-template-columns: 1fr;
                gap: 2rem;
            }
        }

        /* Hindi language toggle */
        .language-toggle {
            position: fixed;
            bottom: 20px;
            right: 20px;
            z-index: 1000;
        }

        .language-btn {
            background: linear-gradient(to right, var(--saffron), var(--green));
            color: white;
            border: none;
            padding: 0.6rem 1.2rem;
            border-radius: 25px;
            font-weight: 600;
            cursor: pointer;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            font-family: 'Noto Sans Devanagari', 'Poppins', sans-serif;
        }

        .language-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.3);
        }

        .language-btn i {
            margin-right: 8px;
            font-size: 1.1rem;
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <header>
        <nav>
            <a href="#" class="logo">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/eda0d753-7b5a-4e2e-b2ba-02e4c3882441.png" alt="SwadVista logo featuring a traditional Indian cooking pot with colorful spices and steam rising in the shape of the Indian map">
                SwadVista
            </a>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#menu">Menu</a></li>
                <li><a href="#about">About Us</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <div class="auth-buttons">
                <button class="btn btn-secondary" id="loginBtn">Login</button>
                <button class="btn btn-primary" id="registerBtn">Register</button>
            </div>
        </nav>
    </header>

    <main>
        <section id="home" class="hero">
            <div class="hero-content">
                <h1>Experience the <span>Authentic</span> Taste of India</h1>
                <p>From the spicy streets of Delhi to the coastal flavors of Kerala, we bring you the diverse and rich culinary heritage of India straight to your table. Handcrafted with traditional recipes passed down through generations.</p>
                <button class="btn btn-primary">Explore Our Menu</button>
            </div>
        </section>

        <section id="menu">
            <h2 class="section-title">Our Signature Dishes</h2>
            <div class="menu-grid">
                <div class="menu-item">
                    <div class="veg-mark">VEG</div>
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/a2825fcd-064a-4751-9e69-2c1efc91db5c.png" alt="Butter chicken with rich creamy tomato gravy served in brass bowl with naan bread and fresh coriander garnish">
                    <div class="menu-item-content">
                        <h3>Butter Chicken</h3>
                        <p>Tender chicken cooked in creamy tomato gravy with aromatic spices, served with butter naan.</p>
                        <p class="price">₹349 <span>₹499</span></p>
                    </div>
                </div>
                <div class="menu-item">
                    <div class="veg-mark">VEG</div>
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/46430437-0203-49ff-90df-999c5bb1646a.png" alt="Paneer tikka platter with marinated cottage cheese cubes roasted in tandoor served with mint chutney and onions">
                    <div class="menu-item-content">
                        <h3>Paneer Tikka</h3>
                        <p>Cubes of cottage cheese marinated in spices and grilled to perfection in tandoor.</p>
                        <p class="price">₹299 <span>₹399</span></p>
                    </div>
                </div>
                <div class="menu-item">
                    <div class="veg-mark">VEG</div>
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/9d4b5fc9-7b27-45db-b860-d3e8bf5406d9.png" alt="Biryani rice dish served in handi with raita, boiled eggs and spiced curry, garnished with fried onions">
                    <div class="menu-item-content">
                        <h3>Hyderabadi Biryani</h3>
                        <p>Fragrant basmati rice layered with tender meat and spices, cooked in dum style.</p>
                        <p class="price">₹399 <span>₹499</span></p>
                    </div>
                </div>
                <div class="menu-item">
                    <div class="veg-mark">VEG</div>
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/b7521b3b-4f80-4472-b3d7-167d3868e8dd.png" alt="Masala dosa served on banana leaf with sambar and coconut chutney in traditional stainless steel bowls">
                    <div class="menu-item-content">
                        <h3>Masala Dosa</h3>
                        <p>Crispy rice crepe stuffed with spiced potato filling, served with sambar and chutney.</p>
                        <p class="price">₹249 <span>₹299</span></p>
                    </div>
                </div>
            </div>
        </section>

        <section id="about">
            <h2 class="section-title">Our Story</h2>
            <div class="about-content">
                <div class="about-text">
                    <h3>A Legacy of Flavor Since 1985</h3>
                    <p>Founded in Mumbai's bustling Crawford Market, SwadVista began as a small family eatery serving authentic home-style meals. What started as a humble venture has now grown into a celebrated name in Indian cuisine, staying true to our roots while embracing innovation.</p>
                    <p>Our chefs, trained in various regional Indian cooking styles, bring together decades of experience to create dishes that tell the story of India's rich culinary diversity. We source our spices directly from farmers across India and use traditional cooking methods to preserve authenticity.</p>
                    <p>From our tandoor ovens to our hand-ground spice blends, every element is carefully curated to deliver an unforgettable dining experience that honors India's gastronomic heritage.</p>
                </div>
                <div class="about-image">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/7a1b76cf-570c-4c9b-8da6-9ff58523c74e.png" alt="Indian chef in traditional attire preparing food in a kitchen with copper pots and colorful spices">
                </div>
            </div>
        </section>

        <section id="contact">
            <h2 class="section-title">Contact Us</h2>
            <form class="contact-form">
                <div class="form-group">
                    <label for="name">Your Name</label>
                    <input type="text" id="name" class="form-control" required>
                </div>
                <div class="form-group">
                    <label for="email">Email Address</label>
                    <input type="email" id="email" class="form-control" required>
                </div>
                <div class="form-group">
                    <label for="phone">Phone Number</label>
                    <input type="tel" id="phone" class="form-control" required>
                </div>
                <div class="form-group">
                    <label for="subject">Subject</label>
                    <input type="text" id="subject" class="form-control" required>
                </div>
                <div class="form-group">
                    <label for="message">Your Message</label>
                    <textarea id="message" class="form-control" required></textarea>
                </div>
                <button type="submit" class="btn btn-primary">Send Message</button>
            </form>
        </section>

        <!-- Login Modal -->
        <div class="modal" id="loginModal">
            <div class="modal-content">
                <button class="close-btn" id="closeLogin">&times;</button>
                <h2 class="modal-title">Login</h2>
                <form id="loginForm">
                    <div class="form-group">
                        <label for="loginEmail">Email or Phone</label>
                        <input type="text" id="loginEmail" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="loginPassword">Password</label>
                        <input type="password" id="loginPassword" class="form-control" required>
                        <a href="#" class="form-note">Forgot password?</a>
                    </div>
                    <button type="submit" class="btn btn-primary" style="width: 100%;">Login</button>
                    <div class="form-footer">
                        <p>New to SwadVista? <a href="#" id="showRegister">Create an account</a></p>
                    </div>
                </form>
            </div>
        </div>

        <!-- Registration Modal -->
        <div class="modal" id="registerModal">
            <div class="modal-content">
                <button class="close-btn" id="closeRegister">&times;</button>
                <h2 class="modal-title">Register</h2>
                <form id="registerForm">
                    <div class="form-group">
                        <label for="registerName">Full Name</label>
                        <input type="text" id="registerName" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="registerEmail">Email</label>
                        <input type="email" id="registerEmail" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="registerPhone">Phone Number</label>
                        <input type="tel" id="registerPhone" class="form-control" required>
                        <span class="form-note">We'll send OTP for verification</span>
                    </div>
                    <div class="form-group">
                        <label for="registerPassword">Password</label>
                        <input type="password" id="registerPassword" class="form-control" required>
                        <span class="form-note">Minimum 8 characters with letters and numbers</span>
                    </div>
                    <div class="form-group">
                        <label for="registerConfirm">Confirm Password</label>
                        <input type="password" id="registerConfirm" class="form-control" required>
                    </div>
                    <button type="submit" class="btn btn-primary" style="width: 100%;">Register</button>
                    <div class="form-footer">
                        <p>Already have an account? <a href="#" id="showLogin">Login here</a></p>
                    </div>
                </form>
            </div>
        </div>
    </main>

    <footer>
        <div class="footer-content">
            <div class="footer-column">
                <h3>About SwadVista</h3>
                <p>Bringing the authentic taste of India's diverse culinary traditions to your table since 1985. Our commitment to quality and tradition makes every meal a memorable experience.</p>
                <div class="social-links">
                    <a href="#"><i class="fab fa-facebook-f"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-youtube"></i></a>
                </div>
            </div>
            <div class="footer-column">
                <h3>Quick Links</h3>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#menu">Our Menu</a></li>
                    <li><a href="#about">About Us</a></li>
                    <li><a href="#contact">Contact</a></li>
                    <li><a href="#">Locations</a></li>
                    <li><a href="#">Careers</a></li>
                </ul>
            </div>
            <div class="footer-column">
                <h3>Contact Info</h3>
                <ul>
                    <li><i class="fas fa-map-marker-alt"></i> 123 Spice Lane, Mumbai</li>
                    <li><i class="fas fa-phone"></i> +91 98765 43210</li>
                    <li><i class="fas fa-envelope"></i> info@swadvista.com</li>
                    <li><i class="fas fa-clock"></i> Open 11AM - 11PM daily</li>
                </ul>
            </div>
        </div>
        <div class="copyright">
            <p>© 2023 SwadVista Foods. All Rights Reserved. | <a href="#">Privacy Policy</a> | <a href="#">Terms of Service</a></p>
        </div>
    </footer>

    <div class="language-toggle">
        <button class="language-btn" id="langToggle">
            <i class="fas fa-language"></i>
            हिंदी/English
        </button>
    </div>

    <script>
        // Modal functionality
        document.addEventListener('DOMContentLoaded', function() {
            const loginBtn = document.getElementById('loginBtn');
            const registerBtn = document.getElementById('registerBtn');
            const loginModal = document.getElementById('loginModal');
            const registerModal = document.getElementById('registerModal');
            const closeLogin = document.getElementById('closeLogin');
            const closeRegister = document.getElementById('closeRegister');
            const showRegister = document.getElementById('showRegister');
            const showLogin = document.getElementById('showLogin');
            
            // Show login modal
            loginBtn.addEventListener('click', function() {
                loginModal.style.display = 'flex';
                registerModal.style.display = 'none';
                document.body.style.overflow = 'hidden';
            });
            
            // Show register modal
            registerBtn.addEventListener('click', function() {
                registerModal.style.display = 'flex';
                loginModal.style.display = 'none';
                document.body.style.overflow = 'hidden';
            });
            
            // Close modals
            closeLogin.addEventListener('click', function() {
                loginModal.style.display = 'none';
                document.body.style.overflow = 'auto';
            });
            
            closeRegister.addEventListener('click', function() {
                registerModal.style.display = 'none';
                document.body.style.overflow = 'auto';
            });
            
            // Switch between modals
            showRegister.addEventListener('click', function(e) {
                e.preventDefault();
                loginModal.style.display = 'none';
                registerModal.style.display = 'flex';
            });
            
            showLogin.addEventListener('click', function(e) {
                e.preventDefault();
                registerModal.style.display = 'none';
                loginModal.style.display = 'flex';
            });
            
            // Close modal when clicking outside
            window.addEventListener('click', function(e) {
                if (e.target === loginModal) {
                    loginModal.style.display = 'none';
                    document.body.style.overflow = 'auto';
                }
                if (e.target === registerModal) {
                    registerModal.style.display = 'none';
                    document.body.style.overflow = 'auto';
                }
            });
            
            // Form validation for registration
            const registerForm = document.getElementById('registerForm');
            registerForm.addEventListener('submit', function(e) {
                e.preventDefault();
                
                const password = document.getElementById('registerPassword').value;
                const confirmPassword = document.getElementById('registerConfirm').value;
                
                if (password !== confirmPassword) {
                    alert('Passwords do not match!');
                    return;
                }
                
                if (password.length < 8) {
                    alert('Password must be at least 8 characters long!');
                    return;
                }
                
                // Here you would normally send the data to your server
                alert('Registration successful! Please login.');
                registerModal.style.display = 'none';
                loginModal.style.display = 'flex';
                document.body.style.overflow = 'auto';
                
                // Clear form
                registerForm.reset();
            });
            
            // Form validation for login
            const loginForm = document.getElementById('loginForm');
            loginForm.addEventListener('submit', function(e) {
                e.preventDefault();
                
                // Here you would normally authenticate with your server
                alert('Login successful!');
                loginModal.style.display = 'none';
                document.body.style.overflow = 'auto';
                
                // Clear form
                loginForm.reset();
            });

            // Language toggle functionality (placeholder)
            const langToggle = document.getElementById('langToggle');
            let isHindi = false;
            
            langToggle.addEventListener('click', function() {
                isHindi = !isHindi;
                if (isHindi) {
                    // In a real implementation, this would switch text to Hindi
                    langToggle.innerHTML = '<i class="fas fa-language"></i> English/हिंदी';
                    alert('Switching to Hindi (demo only - would update all text in production)');
                } else {
                    langToggle.innerHTML = '<i class="fas fa-language"></i> हिंदी/English';
                    alert('Switching to English');
                }
            });

            // Smooth scrolling for navigation links
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function(e) {
                    e.preventDefault();
                    
                    const targetId = this.getAttribute('href');
                    if (targetId === '#') return;
                    
                    const targetElement = document.querySelector(targetId);
                    if (targetElement) {
                        window.scrollTo({
                            top: targetElement.offsetTop - 80,
                            behavior: 'smooth'
                        });
                    }
                });
            });
        });
    </script>
</body>
</html>

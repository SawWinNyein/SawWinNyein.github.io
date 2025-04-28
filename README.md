<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Saw Win Nyein - Creative Solutions</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        /* Global Styles */
        :root {
            --primary: #6c5ce7;
            --secondary: #a29bfe;
            --dark: #2d3436;
            --light: #f5f6fa;
            --accent: #fd79a8;
            --success: #00b894;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        section {
            padding: 80px 0;
        }
        
        h1, h2, h3, h4 {
            margin-bottom: 20px;
            line-height: 1.2;
        }
        
        h1 {
            font-size: 3.5rem;
        }
        
        h2 {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 50px;
            position: relative;
        }
        
        h2::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: var(--primary);
            border-radius: 2px;
        }
        
        p {
            margin-bottom: 15px;
            font-size: 1.1rem;
        }
        
        a {
            text-decoration: none;
            color: inherit;
        }
        
        .btn {
            display: inline-block;
            padding: 12px 30px;
            background: var(--primary);
            color: white;
            border-radius: 30px;
            font-weight: 600;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            font-size: 1rem;
        }
        
        .btn:hover {
            background: var(--secondary);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        .btn-outline {
            background: transparent;
            border: 2px solid var(--primary);
            color: var(--primary);
        }
        
        .btn-outline:hover {
            background: var(--primary);
            color: white;
        }
        
        /* Header Styles */
        header {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary);
        }
        
        .logo span {
            color: var(--accent);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 30px;
        }
        
        .nav-links a {
            font-weight: 600;
            transition: color 0.3s ease;
        }
        
        .nav-links a:hover {
            color: var(--primary);
        }
        
        .menu-toggle {
            display: none;
            cursor: pointer;
            font-size: 1.5rem;
        }
        
        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            margin-top: 80px;
        }
        
        .hero-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }
        
        .hero-text {
            flex: 1;
            padding-right: 50px;
        }
        
        .hero-image {
            flex: 1;
        }
        
        .hero-image img {
            width: 100%;
            animation: float 3s ease-in-out infinite;
        }
        
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
            100% { transform: translateY(0px); }
        }
        
        .hero-buttons {
            margin-top: 30px;
        }
        
        .hero-buttons .btn:first-child {
            margin-right: 15px;
        }
        
        /* Features Section */
        .features {
            background-color: white;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .feature-card {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            text-align: center;
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .feature-icon {
            font-size: 3rem;
            color: var(--primary);
            margin-bottom: 20px;
        }
        
        /* Testimonials */
        .testimonials {
            background-color: #f9f9f9;
        }
        
        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .testimonial-card {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .testimonial-content {
            margin-bottom: 20px;
            font-style: italic;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
        }
        
        .author-image {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            overflow: hidden;
            margin-right: 15px;
        }
        
        .author-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .author-info h4 {
            margin-bottom: 5px;
        }
        
        .author-info p {
            color: #777;
            font-size: 0.9rem;
            margin-bottom: 0;
        }
        
        /* CTA Section */
        .cta {
            text-align: center;
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            color: white;
        }
        
        .cta h2 {
            color: white;
        }
        
        .cta h2::after {
            background: white;
        }
        
        .cta p {
            max-width: 700px;
            margin: 0 auto 30px;
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 60px 0 20px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-column h3 {
            color: white;
            margin-bottom: 25px;
            font-size: 1.3rem;
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 10px;
        }
        
        .footer-links a {
            color: #bbb;
            transition: color 0.3s ease;
        }
        
        .footer-links a:hover {
            color: white;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
        }
        
        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            background: var(--primary);
            transform: translateY(-3px);
        }
        
        .footer-bottom {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #bbb;
            font-size: 0.9rem;
        }
        
        /* Responsive Styles */
        @media (max-width: 992px) {
            h1 {
                font-size: 2.8rem;
            }
            
            h2 {
                font-size: 2.2rem;
            }
            
            .hero-content {
                flex-direction: column;
                text-align: center;
            }
            
            .hero-text {
                padding-right: 0;
                margin-bottom: 50px;
            }
            
            .hero-image {
                max-width: 500px;
            }
        }
        
        @media (max-width: 768px) {
            .menu-toggle {
                display: block;
            }
            
            .nav-links {
                position: fixed;
                top: 80px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 80px);
                background: white;
                flex-direction: column;
                align-items: center;
                justify-content: center;
                transition: all 0.5s ease;
            }
            
            .nav-links.active {
                left: 0;
            }
            
            .nav-links li {
                margin: 20px 0;
            }
            
            .hero-buttons .btn:first-child {
                margin-right: 0;
                margin-bottom: 15px;
            }
            
            .hero-buttons {
                display: flex;
                flex-direction: column;
            }
        }
        
        @media (max-width: 576px) {
            h1 {
                font-size: 2.2rem;
            }
            
            h2 {
                font-size: 1.8rem;
            }
            
            section {
                padding: 60px 0;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav>
                <a href="#" class="logo">Lumi<span>na</span></a>
                <ul class="nav-links">
                    <li><a href="#">Home</a></li>
                    <li><a href="#features">Features</a></li>
                    <li><a href="#testimonials">Testimonials</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
                <div class="menu-toggle">
                    <i class="fas fa-bars"></i>
                </div>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <div class="hero-text">
                    <h1>Beautiful digital solutions for your business</h1>
                    <p>We help businesses create stunning websites and digital experiences that convert visitors into customers.</p>
                    <div class="hero-buttons">
                        <a href="#" class="btn">Get Started</a>
                        <a href="#" class="btn btn-outline">Learn More</a>
                    </div>
                </div>
                <div class="hero-image">
                    <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Digital Illustration">
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="features" id="features">
        <div class="container">
            <h2>Our Amazing Features</h2>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-rocket"></i>
                    </div>
                    <h3>Fast Performance</h3>
                    <p>Our websites are optimized for speed, ensuring your visitors have the best experience possible.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-mobile-alt"></i>
                    </div>
                    <h3>Responsive Design</h3>
                    <p>Perfect display on any device, from desktop computers to mobile phones and tablets.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-paint-brush"></i>
                    </div>
                    <h3>Modern Design</h3>
                    <p>Clean, professional designs that make your business stand out from the competition.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-cog"></i>
                    </div>
                    <h3>Easy to Customize</h3>
                    <p>Simple customization options to match your brand identity and business needs.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <h3>Secure & Reliable</h3>
                    <p>Enterprise-grade security to protect your data and your customers' information.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-headset"></i>
                    </div>
                    <h3>24/7 Support</h3>
                    <p>Our dedicated support team is always available to help you with any questions.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section class="testimonials" id="testimonials">
        <div class="container">
            <h2>What Our Clients Say</h2>
            <div class="testimonial-grid">
                <div class="testimonial-card">
                    <div class="testimonial-content">
                        <p>"Lumina transformed our online presence completely. Our website traffic has increased by 300% since we launched the new site."</p>
                    </div>
                    <div class="testimonial-author">
                        <div class="author-image">
                            <img src="https://randomuser.me/api/portraits/women/32.jpg" alt="Sarah Johnson">
                        </div>
                        <div class="author-info">
                            <h4>Sarah Johnson</h4>
                            <p>CEO, TechSolutions</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="testimonial-content">
                        <p>"The team at Lumina understood our vision perfectly and delivered beyond our expectations. Highly recommended!"</p>
                    </div>
                    <div class="testimonial-author">
                        <div class="author-image">
                            <img src="https://randomuser.me/api/portraits/men/45.jpg" alt="Michael Chen">
                        </div>
                        <div class="author-info">
                            <h4>Michael Chen</h4>
                            <p>Marketing Director, Bloom Inc.</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="testimonial-content">
                        <p>"Working with Lumina was a game-changer for our e-commerce business. Conversion rates are up and customer feedback has been amazing."</p>
                    </div>
                    <div class="testimonial-author">
                        <div class="author-image">
                            <img src="https://randomuser.me/api/portraits/women/68.jpg" alt="Emma Rodriguez">
                        </div>
                        <div class="author-info">
                            <h4>Emma Rodriguez</h4>
                            <p>Founder, StyleHub</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="cta">
        <div class="container">
            <h2>Ready to Transform Your Business?</h2>
            <p>Join thousands of satisfied customers who have already experienced the Lumina difference.</p>
            <a href="#" class="btn">Get Started Today</a>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contact">
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>Lumina</h3>
                    <p>Creating beautiful digital experiences that drive results for your business.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul class="footer-links">
                        <li><a href="#">Home</a></li>
                        <li><a href="#features">Features</a></li>
                        <li><a href="#testimonials">Testimonials</a></li>
                        <li><a href="#">Pricing</a></li>
                        <li><a href="#">Blog</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Services</h3>
                    <ul class="footer-links">
                        <li><a href="#">Web Design</a></li>
                        <li><a href="#">Development</a></li>
                        <li><a href="#">Branding</a></li>
                        <li><a href="#">Digital Marketing</a></li>
                        <li><a href="#">SEO</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Contact Us</h3>
                    <ul class="footer-links">
                        <li><i class="fas fa-map-marker-alt"></i> 123 Design Street, Creative City</li>
                        <li><i class="fas fa-phone"></i> +1 (555) 123-4567</li>
                        <li><i class="fas fa-envelope"></i> hello@lumina.com</li>
                    </ul>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2023 Lumina. All Rights Reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile Menu Toggle
        const menuToggle = document.querySelector('.menu-toggle');
        const navLinks = document.querySelector('.nav-links');
        
        menuToggle.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });
        
        // Close mobile menu when clicking on a link
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
            });
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // Add shadow to header on scroll
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if(window.scrollY > 10) {
                header.style.boxShadow = '0 4px 15px rgba(0, 0, 0, 0.1)';
            } else {
                header.style.boxShadow = '0 2px 10px rgba(0, 0, 0, 0.1)';
            }
        });
    </script>
</body>
</html>

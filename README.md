<html lang="km">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Toycambo - លក់ប្រដាប់ក្មេងលេង និងកាំភ្លើងទឹក</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Bayon&family=Koulen&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css">
    <style>
        :root {
            --primary: #2563eb;
            --secondary: #f59e0b;
            --dark: #1e293b;
            --light: #f8fafc;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Koulen', 'Bayon', sans-serif;
            background-color: var(--light);
            color: var(--dark);
            overflow-x: hidden;
        }

        /* Header with animated gradient */
        header {
            background: linear-gradient(135deg, #1e3a8a 0%, #2563eb 100%);
            color: white;
            text-align: center;
            padding: 3rem 1rem;
            position: relative;
            overflow: hidden;
        }

        header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://assets.onecompiler.app/43bqg7kby/43bqgbkha/1.png') center/cover;
            opacity: 0.1;
            animation: pulse 15s infinite alternate;
        }

        @keyframes pulse {
            0% { opacity: 0.1; }
            100% { opacity: 0.15; }
        }

        header h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            position: relative;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        header p {
            font-size: 1.5rem;
            position: relative;
        }

        /* Navigation */
        nav {
            background-color: var(--dark);
            padding: 1rem;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
            gap: 2rem;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-size: 1.2rem;
            font-weight: normal;
            padding: 0.5rem 1rem;
            border-radius: 4px;
            transition: all 0.3s ease;
            position: relative;
        }

        nav a:hover {
            color: var(--secondary);
            transform: translateY(-2px);
        }

        nav a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 0;
            height: 2px;
            background: var(--secondary);
            transition: width 0.3s ease;
        }

        nav a:hover::after {
            width: 80%;
        }

        /* Clock */
        .clock-container {
            background: rgba(0,0,0,0.7);
            color: white;
            padding: 1rem;
            border-radius: 8px;
            margin: 1rem auto;
            max-width: 200px;
            text-align: center;
            backdrop-filter: blur(5px);
        }

        .clock {
            font-size: 1.5rem;
            font-family: 'Bayon', sans-serif;
        }

        /* Main content */
        .content {
            max-width: 1200px;
            margin: 2rem auto;
            padding: 2rem;
            background-color: white;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }

        section {
            margin-bottom: 3rem;
        }

        h2 {
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
            color: var(--primary);
            position: relative;
            display: inline-block;
        }

        h2::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 50%;
            height: 3px;
            background: var(--secondary);
            border-radius: 3px;
        }

        /* Product grid */
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .product-card {
            border: 1px solid #e2e8f0;
            border-radius: 12px;
            overflow: hidden;
            text-align: center;
            transition: all 0.3s ease;
            position: relative;
            background: white;
        }

        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }

        .product-badge {
            position: absolute;
            top: 10px;
            right: 10px;
            background: var(--secondary);
            color: white;
            padding: 0.25rem 0.5rem;
            border-radius: 4px;
            font-size: 0.8rem;
            z-index: 1;
        }

        .product-image {
            height: 200px;
            width: 100%;
            object-fit: contain;
            padding: 1rem;
            transition: transform 0.3s ease;
        }

        .product-card:hover .product-image {
            transform: scale(1.05);
        }

        .product-info {
            padding: 1rem;
        }

        .product-info h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            color: var(--dark);
        }

        .product-price {
            font-size: 1.2rem;
            color: var(--primary);
            font-weight: bold;
            margin-bottom: 1rem;
        }

        .btn {
            display: inline-block;
            background: var(--primary);
            color: white;
            padding: 0.6rem 1.5rem;
            border-radius: 6px;
            text-decoration: none;
            font-size: 1rem;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
        }

        .btn:hover {
            background: #1d4ed8;
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(37, 99, 235, 0.3);
        }

        .btn-secondary {
            background: var(--secondary);
        }

        .btn-secondary:hover {
            background: #d97706;
            box-shadow: 0 4px 8px rgba(245, 158, 11, 0.3);
        }

        /* Contact form */
        .contact-form {
            margin-top: 2rem;
        }

        .social-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            margin-top: 1rem;
        }

        .social-btn {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            padding: 0.8rem 1.5rem;
            border-radius: 6px;
            font-size: 1rem;
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .social-btn i {
            font-size: 1.2rem;
        }

        .telegram {
            background: #0088cc;
            color: white;
        }

        .telegram:hover {
            background: #0077b5;
            transform: translateY(-2px);
        }

        .facebook {
            background: #3b5998;
            color: white;
        }

        .facebook:hover {
            background: #344e86;
            transform: translateY(-2px);
        }

        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            text-align: center;
            padding: 2rem;
            margin-top: 3rem;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            text-align: left;
        }

        .footer-section h3 {
            font-size: 1.3rem;
            margin-bottom: 1rem;
            color: var(--secondary);
        }

        .footer-section p, .footer-section a {
            color: #cbd5e1;
            margin-bottom: 0.5rem;
            display: block;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-section a:hover {
            color: var(--secondary);
        }

        .copyright {
            margin-top: 2rem;
            padding-top: 1rem;
            border-top: 1px solid #334155;
        }

        /* Animations */
        .animate-on-scroll {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.6s ease, transform 0.6s ease;
        }

        .animate-on-scroll.visible {
            opacity: 1;
            transform: translateY(0);
        }

        @media (max-width: 768px) {
            header h1 {
                font-size: 2.5rem;
            }
            
            header p {
                font-size: 1.2rem;
            }
            
            nav ul {
                flex-direction: column;
                gap: 0.5rem;
                align-items: center;
            }
            
            .product-grid {
                grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            }
        }
    </style>
</head>
<body>
    <!-- Header with animated background -->
    <header class="animate__animated animate__fadeIn">
        <h1>Toycambo</h1>
        <p>លក់ប្រដាប់ក្មេងលេង និងកាំភ្លើងទឹក</p>
        <div class="clock-container">
            <div class="clock" id="clock">កំពុងគណនា...</div>
        </div>
    </header>

    <!-- Navigation -->
    <nav>
        <ul>
            <li><a href="#home">ទំព័រដើម</a></li>
            <li><a href="#products">ផលិតផល</a></li>
            <li><a href="#about">អំពីយើង</a></li>
            <li><a href="#contact">ទំនាក់ទំនង</a></li>
        </ul>
    </nav>

    <!-- Main Content -->
    <div class="content">
        <!-- Welcome Section -->
        <section id="home" class="animate-on-scroll">
            <h2>ស្វាគមន៍មកកាន់ Toycambo!</h2>
            <p style="font-size: 1.2rem; line-height: 1.6;">យើងខ្ញុំផ្តល់នូវប្រដាប់ក្មេងលេង និងកាំភ្លើងទឹកដែលមានគុណភាពខ្ពស់បំផុតនៅកម្ពុជា។ ផលិតផលរបស់យើងត្រូវបានរចនាឡើងសម្រាប់កុមារគ្រប់វ័យដើម្បីផ្តល់នូវការកម្សាន្ត និងសុវត្ថិភាព។</p>
        </section>

        <!-- Products Section -->
        <section id="products">
            <h2 class="animate-on-scroll">ផលិតផលពេញនិយម</h2>
            <div class="product-grid">
                <!-- Product 1 -->
                <div class="product-card animate-on-scroll">
                    <span class="product-badge animate__animated animate__pulse animate__infinite">ថ្មី!</span>
                    <img src="https://assets.onecompiler.app/43bqg7kby/43bqgbkha/1.png" alt="Toy 1" class="product-image">
                    <div class="product-info">
                        <h3>ប្រដាប់ក្មេងលេង 1</h3>
                        <p>សំរាប់កុមារអាយុ 3-5ឆ្នាំ</p>
                        <div class="product-price">$10.00</div>
                        <button class="btn">ទិញឥឡូវនេះ</button>
                    </div>
                </div>

                <!-- Product 2 -->
                <div class="product-card animate-on-scroll">
                    <img src="https://assets.onecompiler.app/43bqg7kby/43bqgbkha/9.png" alt="Toy 2" class="product-image">
                    <div class="product-info">
                        <h3>ប្រដាប់ក្មេងលេង 2</h3>
                        <p>សំរាប់កុមារអាយុ 6-8ឆ្នាំ</p>
                        <div class="product-price">$15.00</div>
                        <button class="btn">ទិញឥឡូវនេះ</button>
                    </div>
                </div>

                <!-- Product 3 -->
                <div class="product-card animate-on-scroll">
                    <img src="https://assets.onecompiler.app/43bqg7kby/43bqgbkha/13.png" alt="Toy 3" class="product-image">
                    <div class="product-info">
                        <h3>ប្រដាប់ក្មេងលេង 3</h3>
                        <p>សំរាប់កុមារអាយុ 9-12ឆ្នាំ</p>
                        <div class="product-price">$18.00</div>
                        <button class="btn">ទិញឥឡូវនេះ</button>
                    </div>
                </div>

                <!-- Product 4 -->
                <div class="product-card animate-on-scroll">
                    <span class="product-badge" style="background: #ef4444;">លក់ដាច់!</span>
                    <img src="https://assets.onecompiler.app/43bqg7kby/43bqdfxby/19.png" alt="Water Gun 1" class="product-image">
                    <div class="product-info">
                        <h3>កាំភ្លើងទឹក 1</h3>
                        <p>សំរាប់កុមារគ្រប់វ័យ</p>
                        <div class="product-price">$20.00 <span style="text-decoration: line-through; color: #64748b; font-size: 0.9rem;">$25.00</span></div>
                        <button class="btn btn-secondary">ទិញឥឡូវនេះ</button>
                    </div>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact" class="animate-on-scroll">
            <h2>ទំនាក់ទំនងយើងខ្ញុំ</h2>
            <p style="margin-bottom: 1.5rem;">សូមទំនាក់ទំនងមកយើងខ្ញុំតាមរយៈជំនួញអនឡាញខាងក្រោម៖</p>
            
            <div class="social-buttons">
                <a href="https://t.me/ToycamboPP" class="social-btn telegram animate__animated animate__fadeInLeft">
                    <i class="fab fa-telegram"></i> Telegram
                </a>
                <a href="https://www.facebook.com/profile.php?id=100066683705736" class="social-btn facebook animate__animated animate__fadeInRight">
                    <i class="fab fa-facebook-f"></i> Facebook
                </a>
            </div>
        </section>
    </div>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-section">
                <h3>អំពីយើង</h3>
                <p>Toycambo គឺជាហាងលក់ប្រដាប់ក្មេងលេង និងកាំភ្លើងទឹកដែលមានគុណភាពខ្ពស់បំផុតនៅកម្ពុជា។</p>
            </div>
            
            <div class="footer-section">
                <h3>វិធីទំនាក់ទំនង</h3>
                <p><i class="fas fa-phone"></i> +855 12 345 678</p>
                <p><i class="fas fa-envelope"></i> toycambo@gmail.com</p>
                <p><i class="fas fa-map-marker-alt"></i> ភ្នំពេញ, កម្ពុជា</p>
            </div>
            
            <div class="footer-section">
                <h3>ម៉ោងបើកហាង</h3>
                <p>ច័ន្ទ-សុក្រ: 8AM - 6PM</p>
                <p>សៅរ៍: 9AM - 4PM</p>
                <p>អាទិត្យ: បិទ</p>
            </div>
        </div>
        
        <div class="copyright">
            <p>បង្កើតដោយ Toycambo | © 2024 រក្សាសិទ្ធិគ្រប់យ៉ាង</p>
        </div>
    </footer>

    <script>
        // Update clock
        function updateTime() {
            const now = new Date();
            const options = { 
                timeZone: 'Asia/Phnom_Penh', 
                hour: '2-digit', 
                minute: '2-digit', 
                second: '2-digit', 
                hour12: false 
            };
            const timeString = now.toLocaleTimeString('km-KH', options);
            document.getElementById('clock').textContent = timeString;
        }
        
        setInterval(updateTime, 1000);
        updateTime();

        // Scroll animations
        const animateElements = document.querySelectorAll('.animate-on-scroll');
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, { threshold: 0.1 });
        
        animateElements.forEach(element => {
            observer.observe(element);
        });

        // Smooth scrolling for navigation
        document.querySelectorAll('nav a').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                window.scrollTo({
                    top: targetElement.offsetTop - 80,
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>

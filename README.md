<!DOCTYPE html>
<html lang="km">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Toycambo - លក់ប្រដាប់ក្មេងលេង និងកាំភ្លើងទឹក</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Bayon&family=Koulen&display=swap" rel="stylesheet">
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

        /* Mobile Responsive */
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

    <!-- Header Section -->
    <header>
        <h1>Toycambo</h1>
        <p>លក់ប្រដាប់ក្មេងលេង និងកាំភ្លើងទឹក</p>
    </header>

    <!-- Navigation Bar -->
    <nav>
        <ul>
            <li><a href="#home">ទំព័រដើម</a></li>
            <li><a href="#products">ផលិតផល</a></li>
            <li><a href="#about">អំពីយើង</a></li>
            <li><a href="#contact">ទំនាក់ទំនង</a></li>
        </ul>
    </nav>

    <!-- Main Content Section -->
    <section id="products">
        <h2>ផលិតផលពេញនិយម</h2>
        <div class="product-grid">
            <!-- Product 1 -->
            <div class="product-card animate-on-scroll">
                <img src="https://assets.onecompiler.app/43bqg7kby/43bqgbkha/1.png" alt="Product Image" class="product-image">
                <div class="product-info">
                    <h3>Product 1</h3>
                    <p>Description goes here</p>
                    <div class="product-price">$20.00</div>
                    <button class="btn">Add to Cart</button>
                </div>
            </div>

            <!-- Product 2 -->
            <div class="product-card animate-on-scroll">
                <img src="https://assets.onecompiler.app/43bqg7kby/43bqgbkha/9.png" alt="Product Image" class="product-image">
                <div class="product-info">
                    <h3>Product 2</h3>
                    <p>Description goes here</p>
                    <div class="product-price">$25.00</div>
                    <button class="btn">Add to Cart</button>
                </div>
            </div>

            <!-- Product 3 -->
            <div class="product-card animate-on-scroll">
                <img src="https://assets.onecompiler.app/43bqg7kby/43bqgbkha/13.png" alt="Product Image" class="product-image">
                <div class="product-info">
                    <h3>Product 3</h3>
                    <p>Description goes here</p>
                    <div class="product-price">$30.00</div>
                    <button class="btn">Add to Cart</button>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer Section -->
    <footer>
        <div class="footer-content">
            <div class="footer-section">
                <h3>អំពីយើង</h3>
                <p>Toycambo provides high-quality toys and water guns in Cambodia.</p>
            </div>
            <div class="footer-section">
                <h3>Contact</h3>
                <p>Phone: +855 12 345 678</p>
                <p>Email: toycambo@gmail.com</p>
            </div>
        </div>
    </footer>

    <script>
        // Scroll Animations
        const elements = document.querySelectorAll('.animate-on-scroll');
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, { threshold: 0.1 });

        elements.forEach(element => {
            observer.observe(element);
        });

        // Smooth Scroll for Navigation Links
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

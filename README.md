
<html lang="km">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Toycambo - លក់ប្រដាប់ក្មេងលេង និងកាំភ្លើងទឹក</title>
    <style>
        body {
            font-family: Times New Roman, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f9f9f9;
        }

        header {
            background-color: #0000FF;
            color: white;
            text-align: center;
            padding: 2em;
        }

        nav {
            background-color: #333;
            padding: 1em;
            text-align: center;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin: 0 16px;
            font-weight: bold;
        }

        .content {
            max-width: 1200px;
            margin: 20px auto;
            padding: 20px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .product-card {
            border: 1px solid #ddd;
            border-radius: 10px;
            overflow: hidden;
            text-align: center;
            padding: 10px;
            transition: transform 0.3s ease;
        }

        .product-card:hover {
            transform: scale(1.05);
        }

        .product-card img {
            max-width: 100%;
            height: auto;
            border-radius: 10px;
        }

        .product-card h3 {
            margin: 10px 0;
            font-size: 1.2em;
        }

        .product-card p {
            color: #555;
        }

        .product-card button {
            background-color: #0000FF;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        .product-card button:hover {
            background-color: #FF00;
        }

        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 1em;
            position: relative;
            bottom: 0;
            width: 100%;
        }

        .contact-form {
            margin-top: 20px;
        }

        .contact-form input, .contact-form textarea {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ddd;
            border-radius: 5px;
        }

        .contact-form button {
            background-color: #FFFF00;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
        }

        .contact-form button:hover {
            background-color: #FF0000;
        }
    </style>
</head>
<body>
    <!-- ប្រអប់ខាងលើ (Header) -->
    <header>
        <h1>Toycambo</h1>
        <p>លក់ប្រដាប់ក្មេងលេង និងកាំភ្លើងទឹក</p>
    </header>
    <body>
    <div class="clock" id="clock">កំពុងគណនា...</div>

    <script>
        // មុខងារសម្រាប់បង្ហាញម៉ោង
        function updateTime() {
            const now = new Date(); // ទាញយកម៉ោងបច្ចុប្បន្ន
            const options = { timeZone: 'Asia/Phnom_Penh', hour: '2-digit', minute: '2-digit', second: '2-digit', hour12: false };
            const timeString = now.toLocaleTimeString('km-KH', options); // បង្ហាញម៉ោងជាភាសាខ្មែរ
            document.getElementById('clock').textContent = timeString; // ដាក់ម៉ោងទៅក្នុង HTML
        }

        // ធ្វើឱ្យម៉ោងផ្លាស់ប្តូររាល់ 1 វិនាទី
        setInterval(updateTime, 1000);
        updateTime(); // ហៅមុខងារលើកដំបូង
    </script>

    <!-- ប៊ូតុងម៉ឺនុយ (Navigation) -->
    <nav>
        <a href="#home">ទំព័រដើម</a>
        <a href="#about">អំពីយើង</a>
        <a href="#products">ផលិតផល</a>
        <a href="#contact">ទំនាក់ទំនង</a>
    </nav>

    <!-- មាតិកាសំខាន់ (Main Content) -->
    <div class="content">
        <h2>ស្វាគមន៍មកកាន់ Toycambo!</h2>
        <p>យើងខ្ញុំផ្តល់នូវប្រដាប់ក្មេងលេង និងកាំភ្លើងទឹកដែលមានគុណភាពខ្ពស់។</p>

        <!-- ផ្នែកផលិតផល (Products) -->
        <h3>ផលិតផលពេញនិយម</h3>
        <div class="product-grid">
            <div class="product-card">
                <img src="https://assets.onecompiler.app/43bqg7kby/43bqdfxby/19.png" alt="Toy 1">
                <h3>ប្រដាប់ក្មេងលេង 1</h3>
                <p>តម្លៃ: $10</p>
                <button>ទិញឥឡូវនេះ</button>
            </div>
            <div class="product-card">
                <img src="https://assets.onecompiler.app/43bqg7kby/43bqdfxby/19.png" alt="Toy 2">
                <h3>ប្រដាប់ក្មេងលេង 2</h3>
                <p>តម្លៃ: $15</p>
                <button>ទិញឥឡូវនេះ</button>
            </div>
            <div class="product-card">
                <img src="https://assets.onecompiler.app/43bqg7kby/43bqdfxby/19.png" alt="Water Gun 1">
                <h3>កាំភ្លើងទឹក 1</h3>
                <p>តម្លៃ: $20</p>
                <button>ទិញឥឡូវនេះ</button>
            </div>
        </div>

        <!-- ផ្នែកទំនាក់ទំនង (Contact Form) -->
        <h3>ទំនាក់ទំនងយើងខ្ញុំ</h3>
        <div class="contact-form">
            <form action="#" method="post">
              <button type="submit"><a href="https://t.me/ToycamboPP">Telegram</a></button>
            </form>
        </div>
    </div>

    <!-- ប្រអប់ខាងក្រោម (Footer) -->
    <footer>
        <p>បង្កើតដោយ Toycambo | © 2024 រក្សាសិទ្ធិគ្រប់យ៉ាង</p>
    </footer>
</body>
</html>

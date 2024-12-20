<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Super Trade</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f8ff;
            color: #333;
        }

        header {
            background-color: #87cefa;
            color: white;
            padding: 10px 20px;
            text-align: center;
        }

        header h1 {
            margin: 0;
            font-size: 2rem;
        }

        .intro {
            color: #4682b4; /* اللون الأزرق */
            font-size: 1.5rem;
            font-weight: bold;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3); /* تأثير الظل */
            margin: 20px 0;
        }

        section {
            padding: 20px;
            text-align: center;
        }

        .hidden {
            display: none;
        }

        .product {
            border: 1px solid #ccc;
            padding: 10px;
            margin: 10px;
            display: inline-block;
            width: 200px;
            background-color: #fff;
        }

        .product img {
            width: 100%;
            height: auto;
        }

        .product h3 {
            margin: 10px 0;
        }

        footer {
            background-color: #4682b4;
            color: white;
            text-align: center;
            padding: 10px 0;
            position: fixed;
            bottom: 0;
            width: 100%;
        }

        nav {
            display: flex;
            justify-content: center;
            background-color: #4682b4;
            padding: 5px 0;
            position: fixed;
            bottom: 20px;
            width: 100%;
        }

        nav a {
            color: white;
            text-decoration: none;
            padding: 8px 15px;
            font-size: 0.9rem;
            transition: background-color 0.3s;
        }

        nav a:hover {
            background-color: #5f9ea0;
        }

        form {
            text-align: left;
            max-width: 500px;
            margin: 0 auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
        }

        form input, form textarea, form button {
            width: 100%;
            padding: 10px;
            margin-bottom: 15px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        form button {
            background-color: #4682b4;
            color: white;
            cursor: pointer;
            font-size: 1rem;
        }

        form button:hover {
            background-color: #5f9ea0;
        }
    </style>
</head>
<body>
    <header>
        <h1>Super Trade</h1>
    </header>

    <section id="home">
        <p class="intro">!!We are Super</p>
        <h2>مرحبًا بكم في متجر Super Trade</h2>
        <p>استعرض أحدث المنتجات لدينا!</p>
        <div class="product">
            <img src="https://via.placeholder.com/200" alt="Product 1">
            <h3>منتج 1</h3>
            <p>وصف المنتج</p>
        </div>
        <div class="product">
            <img src="https://via.placeholder.com/200" alt="Product 2">
            <h3>منتج 2</h3>
            <p>وصف المنتج</p>
        </div>
    </section>

    <section id="add-product" class="hidden">
        <h2>إضافة منتج جديد</h2>
        <form>
            <label for="product-name">اسم المنتج:</label><br>
            <input type="text" id="product-name" name="product-name" required><br><br>

            <label for="product-desc">وصف المنتج:</label><br>
            <textarea id="product-desc" name="product-desc" required></textarea><br><br>

            <label for="product-price">السعر:</label><br>
            <input type="number" id="product-price" name="product-price" required><br><br>

            <label for="product-phone">رقم الهاتف:</label><br>
            <input type="tel" id="product-phone" name="product-phone" pattern="[0-9]{10}" placeholder="رقم الهاتف يجب أن يحتوي على 10 أرقام" required><br><br>

            <button type="submit">إضافة</button>
        </form>
    </section>

    <section id="cart" class="hidden">
        <h2>سلتي</h2>
        <p>لم تقم بإضافة أي منتجات بعد.</p>
    </section>

    <section id="settings" class="hidden">
        <h2>الإعدادات</h2>
        <p>إعدادات الحساب والموقع.</p>
        <form>
            <label for="login-phone">رقم الهاتف أو البريد الإلكتروني:</label><br>
            <input type="text" id="login-phone" name="login-phone" required><br><br>

            <a href="#" style="color: #4682b4; text-decoration: none;">هل نسيت كلمة المرور؟</a><br><br>

            <button type="submit">تسجيل الدخول</button>
        </form>
    </section>

    <footer></footer>

    <nav>
        <a href="#home" onclick="showSection('home')">🏠 الواجهة الرئيسية</a>
        <a href="#add-product" onclick="showSection('add-product')">➕ إضافة منتج</a>
        <a href="#cart" onclick="showSection('cart')">🛒 سلتي</a>
        <a href="#settings" onclick="showSection('settings')">⚙️ الإعدادات</a>
    </nav>

    <script>
        function showSection(sectionId) {
            document.querySelectorAll("section").forEach(section => {
                section.classList.add("hidden");
            });
            document.getElementById(sectionId).classList.remove("hidden");
        }
    </script>
</body>
</html>

<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>موقع لعرض عمل</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #000;
            margin: 0;
            padding: 0;
            color: #fff;
        }
        .container, .login-container {
            max-width: 600px;
            margin: 50px auto;
            background: rgba(0, 0, 0, 0.8);
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 20px rgba(0, 255, 255, 0.8);
        }
        h1, h2 {
            color: #0ff;
            text-shadow: 0 0 10px #0ff;
        }
        .button {
            display: inline-block;
            padding: 10px 20px;
            background: #0ff;
            color: #000;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            box-shadow: 0 0 10px #0ff;
            transition: 0.3s;
        }
        .button:hover {
            background: #00f;
            box-shadow: 0 0 20px #00f;
        }
        .gallery-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 10px;
            margin-top: 50px;
        }
        .gallery-container img {
            width: 150px;
            height: auto;
            border-radius: 10px;
            box-shadow: 0 0 10px #0ff;
            transition: transform 0.3s ease;
        }
        .gallery-container img:hover {
            transform: scale(1.2);
        }
        .products-container {
            margin-top: 30px;
        }
        .product {
            background: rgba(0, 0, 0, 0.8);
            padding: 15px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 255, 255, 0.8);
            display: inline-block;
            margin: 10px;
        }
        .contact {
            margin-top: 30px;
            padding: 20px;
            background: rgba(0, 0, 0, 0.8);
            border-radius: 10px;
            box-shadow: 0 0 20px rgba(0, 255, 255, 0.8);
        }
        .contact a {
            color: #0ff;
            text-decoration: none;
            font-size: 18px;
        }
        .contact a:hover {
            color: #00f;
        }
    </style>
    <script>
        function login() {
            let username = document.getElementById("username").value;
            let password = document.getElementById("password").value;
            if (username && password) {
                if (confirm("هل تريد حفظ كلمة المرور؟")) {
                    alert("تم حفظ كلمة المرور بنجاح!");
                }
                document.getElementById("content").innerHTML = document.getElementById("gallery").innerHTML;
            } else {
                alert("الرجاء إدخال اسم المستخدم وكلمة المرور!");
            }
        }
    </script>
</head>
<body>
    <div id="content" class="container">
        <h1>مرحبًا بك في موقعي لعرض العمل</h1>
        <p>هذا الموقع مخصص لعرض أعمالك بشكل احترافي.</p>
        <button class="button" onclick="document.getElementById('content').innerHTML = document.getElementById('login').innerHTML;">تسجيل الدخول</button>
    </div>

    <div id="login" class="login-container" style="display:none;">
        <h2>تسجيل الدخول</h2>
        <input type="text" placeholder="اسم المستخدم" id="username">
        <input type="password" placeholder="كلمة المرور" id="password">
        <button class="button" onclick="login()">تسجيل الدخول</button>
    </div>

    <div id="gallery" style="display:none;">
        <h2>معرض الصور</h2>
        <div class="gallery-container">
            <img src="https://i.imgur.com/jwK6mO5.jpeg" alt="صورة 1">
            <img src="https://i.imgur.com/IHz1Hiq.jpeg" alt="صورة 2">
            <img src="https://i.imgur.com/n6tWfpQ.jpeg" alt="صورة 3">
            <img src="https://i.imgur.com/B9zhxiB.jpeg" alt="صورة 4">
        </div>
        
        <div class="products-container">
            <h2>منتجات NOL لإنشاء الصور</h2>
            <div class="product">منتج 1 - أداة تصميم الصور</div>
            <div class="product">منتج 2 - مولد الصور الذكي</div>
            <div class="product">منتج 3 - مؤثرات نيون احترافية</div>
        </div>

        <div class="contact">
            <h2>طرق التواصل</h2>
            <p>واتساب: <a href="https://wa.me/201092623555" target="_blank">201092623555+</a></p>
            <p>إنستجرام: <a href="https://www.instagram.com/k.ui.46" target="_blank">@k.ui.46</a></p>
        </div>
    </div>
</body>
</html>

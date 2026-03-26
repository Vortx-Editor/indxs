<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>كافيه ماستر | Master Cafe</title>
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;700;900&display=swap" rel="stylesheet">
    <style>
        /* منطقة الألوان - هنا تغير لون الكافيه بثانية وحدة للزبون الجديد */
        :root {
            --primary-color: #d4af37; /* لون ذهبي فخم */
            --bg-dark: #121212; /* خلفية داكنة */
            --card-bg: #1e1e1e; /* خلفية المنيو */
            --text-light: #f5f5f5;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Tajawal', sans-serif; scroll-behavior: smooth; }
        
        body { background-color: var(--bg-dark); color: var(--text-light); }

        /* --- الهيدر (الشريط العلوي) --- */
        header {
            position: fixed; top: 0; width: 100%; background: rgba(18, 18, 18, 0.9);
            backdrop-filter: blur(10px); padding: 15px 20px; z-index: 1000;
            display: flex; justify-content: space-between; align-items: center;
            border-bottom: 1px solid rgba(212, 175, 55, 0.2);
        }
        .logo { font-size: 24px; font-weight: 900; color: var(--primary-color); text-decoration: none; }
        .nav-links a { color: var(--text-light); text-decoration: none; margin-right: 15px; font-weight: 700; transition: 0.3s; }
        .nav-links a:hover { color: var(--primary-color); }

        /* --- القسم الأول (الواجهة اللي تصدم الزبون) --- */
        .hero {
            height: 100vh; display: flex; flex-direction: column; justify-content: center; align-items: center;
            text-align: center; padding: 20px;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.8)), url('https://images.unsplash.com/photo-1554118811-1e0d58224f24?q=80&w=2047&auto=format&fit=crop') center/cover;
        }
        .hero h1 { font-size: 3rem; margin-bottom: 15px; color: var(--primary-color); }
        .hero p { font-size: 1.2rem; margin-bottom: 30px; max-width: 600px; color: #ccc; }
        .btn {
            background: var(--primary-color); color: #000; padding: 15px 35px; border-radius: 30px;
            text-decoration: none; font-weight: 900; font-size: 1.1rem;
            box-shadow: 0 5px 20px rgba(212, 175, 55, 0.4); transition: 0.3s;
        }
        .btn:hover { transform: translateY(-5px); box-shadow: 0 8px 25px rgba(212, 175, 55, 0.6); }

        /* --- قسم المنيو (الزبدة) --- */
        .menu-section { padding: 80px 20px; text-align: center; }
        .section-title { font-size: 2.5rem; color: var(--primary-color); margin-bottom: 40px; }
        .menu-grid {
            display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px; max-width: 1000px; margin: 0 auto;
        }
        .menu-item {
            background: var(--card-bg); padding: 20px; border-radius: 15px;
            border: 1px solid rgba(255,255,255,0.05); text-align: right;
            transition: 0.3s; display: flex; justify-content: space-between; align-items: center;
        }
        .menu-item:hover { transform: scale(1.02); border-color: var(--primary-color); }
        .item-info h3 { font-size: 1.2rem; margin-bottom: 5px; }
        .item-info p { color: #888; font-size: 0.9rem; }
        .item-price { font-size: 1.3rem; font-weight: 900; color: var(--primary-color); }

        /* --- قسم الصور (أجوائنا) --- */
        .gallery-section { padding: 60px 20px; background: #0a0a0a; text-align: center; }
        .gallery-grid {
            display: flex; gap: 15px; overflow-x: auto; padding-bottom: 20px; max-width: 1000px; margin: 0 auto;
        }
        .gallery-grid img {
            width: 250px; height: 300px; object-fit: cover; border-radius: 15px;
            border: 2px solid transparent; transition: 0.3s; cursor: pointer;
        }
        .gallery-grid img:hover { border-color: var(--primary-color); transform: scale(1.05); }

        /* --- الفوتر والتواصل --- */
        footer { background: #050505; padding: 40px 20px; text-align: center; border-top: 1px solid #222; }
        .footer-content h3 { color: var(--primary-color); margin-bottom: 15px; }
        .footer-content p { color: #888; margin-bottom: 10px; }
        .whatsapp-float {
            position: fixed; bottom: 30px; right: 30px; background: #25d366; color: white;
            width: 60px; height: 60px; border-radius: 50%; display: flex; justify-content: center; align-items: center;
            font-size: 30px; box-shadow: 0 5px 15px rgba(37, 211, 102, 0.4); text-decoration: none; z-index: 9999;
            transition: 0.3s;
        }
        .whatsapp-float:hover { transform: scale(1.1); }
    </style>
</head>
<body>

    <header>
        <a href="#" class="logo">كافيه ماستر ☕</a>
        <div class="nav-links">
            <a href="#menu">المنيو</a>
            <a href="#gallery">أجوائنا</a>
            <a href="#contact">الفروع</a>
        </div>
    </header>

    <section class="hero">
        <h1>قهوتك.. بمزاجك</h1>
        <p>نقدم لكم أجود أنواع القهوة المختصة والمخبوزات الطازجة في أجواء تليق بروقانكم.</p>
        <a href="#menu" class="btn">تصفح المنيو الرقمي</a>
    </section>

    <section id="menu" class="menu-section">
        <h2 class="section-title">قائمتنا المميزة</h2>
        <div class="menu-grid">
            <div class="menu-item">
                <div class="item-info">
                    <h3>V60 كولومبي</h3>
                    <p>إيحاءات فواكه استوائية وحمضية معتدلة</p>
                </div>
                <div class="item-price">18 ر.س</div>
            </div>
            <div class="menu-item">
                <div class="item-info">
                    <h3>فلات وايت</h3>
                    <p>دبل شوت اسبريسو مع حليب مبخر</p>
                </div>
                <div class="item-price">16 ر.س</div>
            </div>
            <div class="menu-item">
                <div class="item-info">
                    <h3>سبانيش لاتيه بارد</h3>
                    <p>مزيج القهوة المختصة مع الحليب المكثف</p>
                </div>
                <div class="item-price">22 ر.س</div>
            </div>
            <div class="menu-item">
                <div class="item-info">
                    <h3>كيكة العسل الروسية</h3>
                    <p>طبقات العسل الهشة طازجة يومياً</p>
                </div>
                <div class="item-price">25 ر.س</div>
            </div>
        </div>
    </section>

    <section id="gallery" class="gallery-section">
        <h2 class="section-title">أجوائنا</h2>
        <div class="gallery-grid">
            <img src="https://images.unsplash.com/photo-1497935586351-b67a49e012bf?w=500&auto=format&fit=crop" alt="أجواء الكافيه">
            <img src="https://images.unsplash.com/photo-1509042239860-f550ce710b93?w=500&auto=format&fit=crop" alt="قهوة">
            <img src="https://images.unsplash.com/photo-1600093463592-8e36ae95ef56?w=500&auto=format&fit=crop" alt="حلى">
        </div>
    </section>

    <footer id="contact">
        <div class="footer-content">
            <h3>موقعنا وأوقات العمل</h3>
            <p>📍 أبها - حي المنسك (شارع الفن)</p>
            <p>⏰ يومياً من 7:00 صباحاً حتى 12:00 منتصف الليل</p>
            <br>
            <p style="font-size: 12px; color: #555;">برمجة وتطوير: مبرمج الواجهات المحترف</p>
        </div>
    </footer>

    <a href="https://wa.me/966500000000?text=السلام عليكم، حاب استفسر عن الطلبات من موقعكم" target="_blank" class="whatsapp-float">
        💬
    </a>

</body>
</html>

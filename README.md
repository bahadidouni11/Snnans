<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>موقعكم التونسي</title>
  <style>
    :root {
      --primary: #5e3a22;
      --secondary: #cfa36a;
      --accent: #FFD700;
      --card: #ffe6b3;
      --text: #333;
    }
    
    body {
      margin: 0;
      padding: 0;
      font-family: 'Tajawal', sans-serif;
      background: linear-gradient(#8b5e3c, var(--secondary));
      min-height: 100vh;
      color: var(--text);
    }
    
    /* شريط التنبيه */
    .alert-bar {
      background: var(--accent);
      color: var(--primary);
      padding: 8px;
      text-align: center;
      font-weight: bold;
      animation: scroll 15s linear infinite;
      white-space: nowrap;
      position: fixed;
      top: 0;
      width: 100%;
      z-index: 1000;
    }
    @keyframes scroll {
      from { transform: translateX(100%); }
      to { transform: translateX(-100%); }
    }
    
    /* الترويسة */
    .header {
      background: var(--primary);
      color: white;
      padding: 15px;
      text-align: center;
      margin-top: 40px;
    }
    .site-title {
      font-size: 24px;
      margin: 5px 0;
    }
    .tn-logo {
      display: inline-block;
      width: 40px;
      height: 40px;
      background: var(--accent);
      color: var(--primary);
      border-radius: 50%;
      line-height: 40px;
      font-weight: bold;
    }
    
    /* الصفحات */
    .page {
      display: none;
      padding-bottom: 70px;
    }
    .active {
      display: block;
    }
    
    /* الأزرار الرئيسية */
    .card-container {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 15px;
      max-width: 500px;
      margin: 30px auto;
      padding: 0 15px;
    }
    .card {
      background: var(--card);
      border-radius: 12px;
      height: 120px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: bold;
      font-size: 18px;
      color: var(--primary);
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      transition: all 0.3s;
    }
    .card:hover {
      transform: translateY(-5px);
      box-shadow: 0 6px 12px rgba(0,0,0,0.15);
    }
    
    /* زر الصاروخ */
    .rocket-card {
      background: linear-gradient(135deg, #3a7bd5, #00d2ff);
      color: white;
      position: relative;
      overflow: hidden;
    }
    .rocket-card::before {
      content: "🚀";
      font-size: 30px;
      position: absolute;
      top: 15px;
      animation: float 2s ease-in-out infinite;
    }
    .rocket-card span {
      position: relative;
      top: 25px;
    }
    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-8px); }
    }
    
    /* قسم الشركاء */
    .partners-section {
      background: rgba(255,255,255,0.1);
      padding: 30px 15px;
      margin: 30px 0;
      border-radius: 20px;
    }
    .section-title {
      color: white;
      text-align: center;
      font-size: 22px;
      margin-bottom: 20px;
    }
    .partners-grid {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
    }
    .partner-item {
      background: rgba(255,255,255,0.9);
      border-radius: 10px;
      padding: 15px;
      width: 100px;
      text-align: center;
      transition: all 0.3s;
    }
    .partner-item:hover {
      transform: scale(1.05);
    }
    .partner-logo {
      width: 60px;
      height: 60px;
      object-fit: contain;
    }
    .partner-name {
      color: var(--primary);
      font-weight: bold;
      margin-top: 8px;
    }
    
    /* القائمة السفلية */
    .bottom-nav {
      position: fixed;
      bottom: 0;
      width: 100%;
      background: var(--primary);
      display: flex;
      justify-content: space-around;
      padding: 15px 0;
      z-index: 1000;
    }
    .nav-btn {
      background: none;
      border: none;
      color: white;
      font-size: 16px;
      font-weight: bold;
    }
    
    /* صفحة الدخول */
    .login-page {
      text-align: center;
      padding-top: 100px;
    }
    .start-btn {
      background: var(--accent);
      color: var(--primary);
      border: none;
      padding: 12px 30px;
      border-radius: 25px;
      font-size: 18px;
      font-weight: bold;
      margin-top: 30px;
      cursor: pointer;
      transition: all 0.3s;
    }
    .start-btn:hover {
      transform: scale(1.05);
    }
  </style>
</head>
<body>

<div class="alert-bar">موقعنا لا يتحمل ضياع أي أموال - احذر من النصب!</div>

<!-- صفحة الدخول -->
<div id="loginPage" class="page active login-page">
  <div class="header">
    <div class="site-title">موقعكم التونسي</div>
    <div class="tn-logo">TN</div>
  </div>
  
  <button class="start-btn" onclick="goTo('contentPage')">ابدأ الاستخدام</button>
  <p style="color:white; margin-top:30px;">حقوق الموقع | سياسة الخصوصية</p>
</div>

<!-- صفحة المحتوى -->
<div id="contentPage" class="page">
  <div class="header">
    <div class="site-title">موقعكم التونسي</div>
    <div class="tn-logo">TN</div>
  </div>
  
  <div class="card-container">
    <div class="card">مهام يومية</div>
    <div class="card">شراء خطة</div>
    <div class="card">سحب رصيد</div>
    <div class="card rocket-card"><span>اركب الساروخ</span></div>
  </div>
  
  <div class="partners-section">
    <h2 class="section-title">شركاؤنا</h2>
    <div class="partners-grid">
      <a href="https://www.spotify.com" target="_blank" class="partner-item">
        <img src="https://upload.wikimedia.org/wikipedia/commons/1/19/Spotify_logo_without_text.svg" 
             class="partner-logo" alt="Spotify">
        <div class="partner-name">Spotify</div>
      </a>
      <a href="https://www.youtube.com" target="_blank" class="partner-item">
        <img src="https://upload.wikimedia.org/wikipedia/commons/b/b8/YouTube_Logo_2017.svg" 
             class="partner-logo" alt="YouTube">
        <div class="partner-name">YouTube</div>
      </a>
      <a href="https://www.netflix.com" target="_blank" class="partner-item">
        <img src="https://upload.wikimedia.org/wikipedia/commons/0/08/Netflix_2015_logo.svg" 
             class="partner-logo" alt="Netflix">
        <div class="partner-name">Netflix</div>
      </a>
      <a href="https://www.amazon.com" target="_blank" class="partner-item">
        <img src="https://upload.wikimedia.org/wikipedia/commons/a/a9/Amazon_logo.svg" 
             class="partner-logo" alt="Amazon">
        <div class="partner-name">Amazon</div>
      </a>
      <a href="https://www.tunisie.gov.tn" target="_blank" class="partner-item">
        <img src="https://upload.wikimedia.org/wikipedia/commons/8/8a/Tunisia_logo.png" 
             class="partner-logo" alt="Tunisia">
        <div class="partner-name">تونس</div>
      </a>
    </div>
  </div>
  
  <div class="bottom-nav">
    <button class="nav-btn" onclick="goTo('loginPage')">الرئيسية</button>
    <button class="nav-btn" onclick="goTo('contentPage')">المحتوى</button>
  </div>
</div>

<script>
function goTo(pageId) {
  // إخفاء جميع الصفحات
  document.querySelectorAll('.page').forEach(page => {
    page.classList.remove('active');
  });
  
  // إظهار الصفحة المطلوبة
  document.getElementById(pageId).classList.add('active');
  
  // التمرير لأعلى الصفحة
  window.scrollTo(0, 0);
}
</script>

</body>
</html>

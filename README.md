<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>דף נחיתה מודרני ומונפש</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Heebo:wght@100;300;400;500;700;900&display=swap" rel="stylesheet">
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    <style>
        :root {
            --primary: #4F46E5;
            --primary-light: #818CF8;
            --secondary: #10B981;
            --dark: #1F2937;
            --light: #F9FAFB;
            --accent: #F59E0B;
        }
        
        body {
            font-family: 'Heebo', sans-serif;
            direction: rtl;
            background-color: #f9fafb;
            color: #1F2937;
            overflow-x: hidden;
        }
        
        .hero-bg {
            background: linear-gradient(135deg, var(--primary) 0%, var(--primary-light) 100%);
        }
        
        .floating {
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
            100% { transform: translateY(0px); }
        }
        
        .gradient-text {
            background: linear-gradient(90deg, var(--primary) 0%, var(--accent) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-fill-color: transparent;
        }
        
        .feature-card {
            transition: all 0.3s ease;
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }
        
        .scroll-indicator {
            animation: bounce 2s infinite;
        }
        
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-20px); }
            60% { transform: translateY(-10px); }
        }
        
        .pulse-btn {
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(79, 70, 229, 0.7); }
            70% { box-shadow: 0 0 0 10px rgba(79, 70, 229, 0); }
            100% { box-shadow: 0 0 0 0 rgba(79, 70, 229, 0); }
        }
        
        /* מותאם למובייל */
        @media (max-width: 768px) {
            .container {
                padding-left: 1rem;
                padding-right: 1rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="bg-white shadow-sm sticky top-0 z-50">
        <nav class="container mx-auto px-4 py-3 flex justify-between items-center">
            <div class="text-2xl font-bold text-indigo-600">
                <span class="gradient-text">לוגו</span>
            </div>
            
            <!-- תפריט למסך רחב -->
            <div class="hidden md:flex items-center space-x-8 space-x-reverse">
                <a href="#" class="font-medium text-gray-700 hover:text-indigo-600 transition">בית</a>
                <a href="#features" class="font-medium text-gray-700 hover:text-indigo-600 transition">יתרונות</a>
                <a href="#testimonials" class="font-medium text-gray-700 hover:text-indigo-600 transition">המלצות</a>
                <a href="#contact" class="font-medium text-gray-700 hover:text-indigo-600 transition">צור קשר</a>
                <button class="bg-indigo-600 text-white px-6 py-2 rounded-lg hover:bg-indigo-700 transition pulse-btn">
                    התחל עכשיו
                </button>
            </div>
            
            <!-- תפריט למובייל -->
            <div class="md:hidden">
                <button class="text-gray-600 hover:text-gray-900 focus:outline-none">
                    <i class="fas fa-bars text-2xl"></i>
                </button>
            </div>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero-bg text-white py-24 relative overflow-hidden">
        <div class="absolute inset-0 z-0" style="background-image: url('data:image/svg+xml,%3Csvg xmlns=\'http://www.w3.org/2000/svg\' viewBox=\'0 0 1440 320\'%3E%3Cpath fill=\'%23ffffff\' fill-opacity=\'0.05\' d=\'M0,160L48,138.7C96,117,192,75,288,64C384,53,480,75,576,106.7C672,139,768,181,864,170.7C960,160,1056,96,1152,74.7C1248,53,1344,75,1392,85.3L1440,96L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z\'%3E%3C/path%3E%3C/svg%3E');"></div>
        
        <div class="container mx-auto px-4 relative z-10">
            <div class="flex flex-wrap items-center">
                <div class="w-full md:w-1/2 mb-12 md:mb-0" data-aos="fade-left" data-aos-duration="1000">
                    <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6">
                        כותרת מושכת <span class="text-yellow-300">לדף הנחיתה</span> שלך
                    </h1>
                    <p class="text-xl mb-8 text-indigo-100">
                        טקסט משנה שמסביר את היתרונות העיקריים של המוצר או השירות שלך בצורה תמציתית וברורה.
                    </p>
                    <div class="flex flex-col sm:flex-row space-y-4 sm:space-y-0 sm:space-x-4 sm:space-x-reverse">
                        <button class="bg-white text-indigo-600 px-8 py-3 rounded-lg font-semibold hover:bg-gray-100 transition shadow-lg">
                            <i class="fas fa-rocket ml-2"></i>התחל עכשיו
                        </button>
                        <button class="bg-transparent border-2 border-white text-white px-8 py-3 rounded-lg font-semibold hover:bg-white hover:text-indigo-600 transition">
                            <i class="fas fa-play ml-2"></i>צפה בהדגמה
                        </button>
                    </div>
                </div>
                <div class="w-full md:w-1/2 flex justify-center" data-aos="fade-right" data-aos-duration="1000">
                    <div class="relative floating">
                        <img src="https://cdn1.genspark.ai/user-upload-image/gpt_image_generated/d13a762f-6e59-4c48-82c1-107037b3d604_wm" alt="דף נחיתה מודרני" class="rounded-lg shadow-2xl max-w-full h-auto" />
                        <div class="absolute -bottom-10 -right-10 bg-yellow-400 text-indigo-900 py-3 px-6 rounded-full font-bold shadow-lg">
                            חדש!
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="absolute bottom-5 left-1/2 transform -translate-x-1/2 text-center text-white scroll-indicator">
                <p class="mb-2">גלול למטה</p>
                <i class="fas fa-chevron-down text-2xl"></i>
            </div>
        </div>
    </section>

    <!-- מספרים מרשימים -->
    <section class="py-16 bg-gray-50">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-2 md:grid-cols-4 gap-6 text-center">
                <div class="bg-white p-8 rounded-lg shadow-md" data-aos="zoom-in" data-aos-delay="100">
                    <h3 class="text-4xl font-bold text-indigo-600 mb-2">+1000</h3>
                    <p class="text-gray-600">לקוחות מרוצים</p>
                </div>
                <div class="bg-white p-8 rounded-lg shadow-md" data-aos="zoom-in" data-aos-delay="200">
                    <h3 class="text-4xl font-bold text-indigo-600 mb-2">95%</h3>
                    <p class="text-gray-600">שיעור הצלחה</p>
                </div>
                <div class="bg-white p-8 rounded-lg shadow-md" data-aos="zoom-in" data-aos-delay="300">
                    <h3 class="text-4xl font-bold text-indigo-600 mb-2">24/7</h3>
                    <p class="text-gray-600">תמיכה זמינה</p>
                </div>
                <div class="bg-white p-8 rounded-lg shadow-md" data-aos="zoom-in" data-aos-delay="400">
                    <h3 class="text-4xl font-bold text-indigo-600 mb-2">+50</h3>
                    <p class="text-gray-600">פתרונות מותאמים</p>
                </div>
            </div>
        </div>
    </section>

    <!-- יתרונות -->
    <section id="features" class="py-20 bg-white">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl font-bold mb-4">היתרונות שלנו</h2>
                <p class="text-xl text-gray-600 max-w-2xl mx-auto">
                    הפתרונות שלנו מספקים מענה מושלם לצרכים שלך. הנה כמה מהיתרונות המרכזיים שתקבל
                </p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="feature-card bg-gray-50 p-8 rounded-xl shadow-md" data-aos="fade-up" data-aos-delay="100">
                    <div class="bg-indigo-100 text-indigo-600 w-16 h-16 rounded-lg flex items-center justify-center mb-6">
                        <i class="fas fa-bolt text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-4">מהירות מדהימה</h3>
                    <p class="text-gray-600">
                        המערכת שלנו מבטיחה ביצועים מהירים במיוחד, מה שמאפשר לך לחסוך זמן יקר ולהתמקד בדברים החשובים באמת.
                    </p>
                </div>
                
                <div class="feature-card bg-gray-50 p-8 rounded-xl shadow-md" data-aos="fade-up" data-aos-delay="200">
                    <div class="bg-green-100 text-green-600 w-16 h-16 rounded-lg flex items-center justify-center mb-6">
                        <i class="fas fa-shield-alt text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-4">אבטחה מתקדמת</h3>
                    <p class="text-gray-600">
                        אנו מיישמים את אמצעי האבטחה המתקדמים ביותר כדי להבטיח שהמידע שלך נשמר בצורה הבטוחה ביותר.
                    </p>
                </div>
                
                <div class="feature-card bg-gray-50 p-8 rounded-xl shadow-md" data-aos="fade-up" data-aos-delay="300">
                    <div class="bg-yellow-100 text-yellow-600 w-16 h-16 rounded-lg flex items-center justify-center mb-6">
                        <i class="fas fa-cog text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-4">התאמה אישית</h3>
                    <p class="text-gray-600">
                        הפתרונות שלנו ניתנים להתאמה מלאה לצרכים הספציפיים שלך, מה שמאפשר לך לקבל בדיוק את מה שאתה צריך.
                    </p>
                </div>
            </div>
            
            <div class="mt-16 text-center" data-aos="fade-up">
                <a href="#" class="inline-block bg-indigo-600 text-white px-8 py-3 rounded-lg font-semibold hover:bg-indigo-700 transition">
                    גלה עוד יתרונות <i class="fas fa-arrow-left mr-2"></i>
                </a>
            </div>
        </div>
    </section>
    
    <!-- קטע המלצות -->
    <section id="testimonials" class="py-20 bg-gray-50">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl font-bold mb-4">מה הלקוחות שלנו אומרים</h2>
                <p class="text-xl text-gray-600 max-w-2xl mx-auto">
                    לקוחות מרוצים הם העדות הטובה ביותר לאיכות השירות שלנו
                </p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="bg-white p-8 rounded-xl shadow-md" data-aos="fade-up" data-aos-delay="100">
                    <div class="flex justify-center mb-6">
                        <div class="text-yellow-400 flex">
                            <i class="fas fa-star mx-1"></i>
                            <i class="fas fa-star mx-1"></i>
                            <i class="fas fa-star mx-1"></i>
                            <i class="fas fa-star mx-1"></i>
                            <i class="fas fa-star mx-1"></i>
                        </div>
                    </div>
                    <p class="text-gray-600 italic mb-6">
                        "השירות שקיבלנו היה מעל ומעבר למצופה. הצוות היה מקצועי, קשוב וסיפק פתרונות מותאמים בדיוק לצרכים שלנו."
                    </p>
                    <div class="flex items-center">
                        <div class="w-12 h-12 bg-indigo-200 rounded-full flex items-center justify-center mr-4">
                            <span class="text-indigo-600 font-bold">ר.כ</span>
                        </div>
                        <div>
                            <h4 class="font-bold">רונית כהן</h4>
                            <p class="text-gray-500 text-sm">מנכ"לית, חברת אלפא</p>
                        </div>
                    </div>
                </div>
                
                <div class="bg-white p-8 rounded-xl shadow-md" data-aos="fade-up" data-aos-delay="200">
                    <div class="flex justify-center mb-6">
                        <div class="text-yellow-400 flex">
                            <i class="fas fa-star mx-1"></i>
                            <i class="fas fa-star mx-1"></i>
                            <i class="fas fa-star mx-1"></i>
                            <i class="fas fa-star mx-1"></i>
                            <i class="fas fa-star mx-1"></i>
                        </div>
                    </div>
                    <p class="text-gray-600 italic mb-6">
                        "לא האמנתי שאפשר לקבל תוצאות כל כך מרשימות בזמן כל כך קצר. התהליך היה פשוט, מהיר ויעיל מאוד."
                    </p>
                    <div class="flex items-center">
                        <div class="w-12 h-12 bg-green-200 rounded-full flex items-center justify-center mr-4">
                            <span class="text-green-600 font-bold">י.ל</span>
                        </div>
                        <div>
                            <h4 class="font-bold">יוסי לוי</h4>
                            <p class="text-gray-500 text-sm">יזם טכנולוגיה</p>
                        </div>
                    </div>
                </div>
                
                <div class="bg-white p-8 rounded-xl shadow-md" data-aos="fade-up" data-aos-delay="300">
                    <div class="flex justify-center mb-6">
                        <div class="text-yellow-400 flex">
                            <i class="fas fa-star mx-1"></i>
                            <i class="fas fa-star mx-1"></i>
                            <i class="fas fa-star mx-1"></i>
                            <i class="fas fa-star mx-1"></i>
                            <i class="fas fa-star-half-alt mx-1"></i>
                        </div>
                    </div>
                    <p class="text-gray-600 italic mb-6">
                        "הפתרון שהוצע לנו חסך לחברה אלפי שקלים בחודש והגדיל משמעותית את היעילות. זו הייתה החלטה מצוינת לעבוד איתם."
                    </p>
                    <div class="flex items-center">
                        <div class="w-12 h-12 bg-yellow-200 rounded-full flex items-center justify-center mr-4">
                            <span class="text-yellow-600 font-bold">מ.א</span>
                        </div>
                        <div>
                            <h4 class="font-bold">מיכל אברהם</h4>
                            <p class="text-gray-500 text-sm">מנהלת תפעול, חברת ביטא</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- קריאה לפעולה -->
    <section class="py-20 bg-indigo-600 text-white">
        <div class="container mx-auto px-4 text-center">
            <h2 class="text-3xl md:text-4xl font-bold mb-6" data-aos="fade-up">מוכנים להתחיל?</h2>
            <p class="text-xl text-indigo-100 mb-8 max-w-2xl mx-auto" data-aos="fade-up" data-aos-delay="100">
                הצטרפו לאלפי הלקוחות המרוצים שלנו וגלו איך אנחנו יכולים לעזור לכם להגיע ליעדים שלכם.
            </p>
            <div class="flex flex-col sm:flex-row justify-center space-y-4 sm:space-y-0 sm:space-x-4 sm:space-x-reverse" data-aos="fade-up" data-aos-delay="200">
                <button class="bg-white text-indigo-600 px-8 py-3 rounded-lg font-semibold hover:bg-gray-100 transition shadow-lg">
                    התחל עכשיו
                </button>
                <button class="bg-transparent border-2 border-white text-white px-8 py-3 rounded-lg font-semibold hover:bg-white hover:text-indigo-600 transition">
                    דבר איתנו
                </button>
            </div>
        </div>
    </section>
    
    <!-- טופס צור קשר -->
    <section id="contact" class="py-20 bg-white">
        <div class="container mx-auto px-4">
            <div class="max-w-4xl mx-auto">
                <div class="text-center mb-12">
                    <h2 class="text-3xl md:text-4xl font-bold mb-4">צור קשר</h2>
                    <p class="text-xl text-gray-600">
                        יש לך שאלות? אנחנו כאן בשבילך
                    </p>
                </div>
                
                <div class="bg-gray-50 rounded-xl shadow-md p-8" data-aos="fade-up">
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                        <div>
                            <div class="mb-6">
                                <label class="block text-gray-700 font-medium mb-2" for="name">שם מלא</label>
                                <input type="text" id="name" class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:border-indigo-500 focus:ring focus:ring-indigo-200 focus:ring-opacity-50">
                            </div>
                            <div class="mb-6">
                                <label class="block text-gray-700 font-medium mb-2" for="email">דוא"ל</label>
                                <input type="email" id="email" class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:border-indigo-500 focus:ring focus:ring-indigo-200 focus:ring-opacity-50">
                            </div>
                            <div class="mb-6">
                                <label class="block text-gray-700 font-medium mb-2" for="phone">טלפון</label>
                                <input type="tel" id="phone" class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:border-indigo-500 focus:ring focus:ring-indigo-200 focus:ring-opacity-50">
                            </div>
                        </div>
                        <div>
                            <div class="mb-6">
                                <label class="block text-gray-700 font-medium mb-2" for="message">הודעה</label>
                                <textarea id="message" rows="8" class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:border-indigo-500 focus:ring focus:ring-indigo-200 focus:ring-opacity-50"></textarea>
                            </div>
                            <button class="w-full bg-indigo-600 text-white px-8 py-3 rounded-lg font-semibold hover:bg-indigo-700 transition pulse-btn">
                                שלח הודעה <i class="fas fa-paper-plane mr-2"></i>
                            </button>
                        </div>
                    </div>
                </div>
                
                <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mt-12">
                    <div class="text-center" data-aos="fade-up" data-aos-delay="100">
                        <div class="bg-indigo-100 text-indigo-600 w-16 h-16 rounded-lg flex items-center justify-center mx-auto mb-4">
                            <i class="fas fa-map-marker-alt text-2xl"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-2">כתובת</h3>
                        <p class="text-gray-600">רחוב הראשונים 123, תל אביב</p>
                    </div>
                    
                    <div class="text-center" data-aos="fade-up" data-aos-delay="200">
                        <div class="bg-green-100 text-green-600 w-16 h-16 rounded-lg flex items-center justify-center mx-auto mb-4">
                            <i class="fas fa-phone-alt text-2xl"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-2">טלפון</h3>
                        <p class="text-gray-600">03-1234567</p>
                    </div>
                    
                    <div class="text-center" data-aos="fade-up" data-aos-delay="300">
                        <div class="bg-yellow-100 text-yellow-600 w-16 h-16 rounded-lg flex items-center justify-center mx-auto mb-4">
                            <i class="fas fa-envelope text-2xl"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-2">דוא"ל</h3>
                        <p class="text-gray-600">info@example.com</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- פוטר -->
    <footer class="bg-gray-900 text-white py-12">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <div>
                    <h3 class="text-2xl font-bold mb-6">לוגו</h3>
                    <p class="text-gray-400 mb-6">
                        אנו מספקים פתרונות איכותיים שעוזרים ללקוחות שלנו להצליח בעולם דיגיטלי מורכב.
                    </p>
                    <div class="flex space-x-4 space-x-reverse">
                        <a href="#" class="text-gray-400 hover:text-white transition">
                            <i class="fab fa-facebook-f"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition">
                            <i class="fab fa-twitter"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition">
                            <i class="fab fa-instagram"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition">
                            <i class="fab fa-linkedin-in"></i>
                        </a>
                    </div>
                </div>
                
                <div>
                    <h4 class="text-xl font-bold mb-6">קישורים מהירים</h4>
                    <ul class="space-y-3">
                        <li><a href="#" class="text-gray-400 hover:text-white transition">בית</a></li>
                        <li><a href="#features" class="text-gray-400 hover:text-white transition">יתרונות</a></li>
                        <li><a href="#testimonials" class="text-gray-400 hover:text-white transition">המלצות</a></li>
                        <li><a href="#contact" class="text-gray-400 hover:text-white transition">צור קשר</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">תנאי שימוש</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">מדיניות פרטיות</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-xl font-bold mb-6">השירותים שלנו</h4>
                    <ul class="space-y-3">
                        <li><a href="#" class="text-gray-400 hover:text-white transition">פתרון א'</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">פתרון ב'</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">פתרון ג'</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">פתרון ד'</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">פתרון ה'</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-xl font-bold mb-6">הצטרפו לניוזלטר</h4>
                    <p class="text-gray-400 mb-4">
                        קבלו עדכונים ותוכן בלעדי ישירות לתיבת הדוא"ל
                    </p>
                    <form>
                        <div class="flex">
                            <input type="email" placeholder="הזן את כתובת הדוא״ל" class="w-full px-4 py-2 rounded-r-lg focus:outline-none">
                            <button type="submit" class="bg-indigo-600 text-white px-4 py-2 rounded-l-lg hover:bg-indigo-700 transition">
                                <i class="fas fa-paper-plane"></i>
                            </button>
                        </div>
                    </form>
                </div>
            </div>
            
            <div class="border-t border-gray-800 mt-12 pt-8 text-center">
                <p class="text-gray-400">© 2023 כל הזכויות שמורות</p>
            </div>
        </div>
    </footer>

    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script>
        // אתחול אנימציות
        document.addEventListener('DOMContentLoaded', function() {
            AOS.init({
                duration: 800,
                once: true
            });
            
            // תפריט למובייל
            const mobileMenuButton = document.querySelector('.md\\:hidden button');
            if (mobileMenuButton) {
                mobileMenuButton.addEventListener('click', function() {
                    // כאן תוכל להוסיף לוגיקה לפתיחה וסגירה של תפריט מובייל
                    alert('תפריט המובייל יופיע כאן');
                });
            }
            
            // הגדרת גלילה חלקה לקישורים פנימיים
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    
                    const target = document.querySelector(this.getAttribute('href'));
                    if (target) {
                        window.scrollTo({
                            top: target.offsetTop - 100,
                            behavior: 'smooth'
                        });
                    }
                });
            });
        });
    </script>
</body>
</html>

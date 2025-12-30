# ItSolutions
.
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Профессиональные IT-услуги | Премиальные решения</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #0f1a30;
            --secondary: #1a2840;
            --accent: #d4af37;
            --accent-light: #f4e4a6;
            --light: #e8f1ff;
            --dark: #0a1220;
            --card-bg: rgba(255, 255, 255, 0.03);
            --card-border: rgba(212, 175, 55, 0.2);
            --transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.1);
            --shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            --gradient: linear-gradient(135deg, #0f1a30 0%, #1a2840 50%, #0a1220 100%);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Inter', 'Segoe UI', system-ui, sans-serif;
        }

        body {
            background: var(--dark);
            color: var(--light);
            line-height: 1.7;
            overflow-x: hidden;
            background-image: 
                radial-gradient(circle at 20% 30%, rgba(212, 175, 55, 0.05) 0%, transparent 20%),
                radial-gradient(circle at 80% 70%, rgba(212, 175, 55, 0.03) 0%, transparent 20%);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 24px;
        }

        /* Header & Hero */
        header {
            background: var(--gradient);
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(212, 175, 55, 0.1);
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--accent);
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo i {
            font-size: 2rem;
        }

        .nav-contact {
            display: flex;
            align-items: center;
            gap: 20px;
        }

        .phone-link {
            color: var(--accent);
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            padding: 10px 20px;
            border: 1px solid var(--accent);
            border-radius: 50px;
            transition: var(--transition);
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .phone-link:hover {
            background: var(--accent);
            color: var(--dark);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(212, 175, 55, 0.3);
        }

        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding: 120px 0 80px;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            width: 600px;
            height: 600px;
            background: radial-gradient(circle, rgba(212, 175, 55, 0.1) 0%, transparent 70%);
            top: 50%;
            right: -200px;
            transform: translateY(-50%);
            border-radius: 50%;
        }

        .hero-content {
            max-width: 700px;
            position: relative;
            z-index: 1;
        }

        .hero h1 {
            font-size: 4rem;
            font-weight: 800;
            margin-bottom: 1.5rem;
            background: linear-gradient(135deg, var(--light) 0%, var(--accent) 100%);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            line-height: 1.2;
            opacity: 0;
            animation: fadeUp 0.8s ease 0.2s forwards;
        }

        .hero-subtitle {
            font-size: 1.4rem;
            color: var(--accent-light);
            margin-bottom: 2.5rem;
            opacity: 0;
            animation: fadeUp 0.8s ease 0.4s forwards;
        }

        .hero-description {
            font-size: 1.2rem;
            color: #b0c4ff;
            margin-bottom: 3rem;
            opacity: 0;
            animation: fadeUp 0.8s ease 0.6s forwards;
        }

        .hero-buttons {
            display: flex;
            gap: 20px;
            opacity: 0;
            animation: fadeUp 0.8s ease 0.8s forwards;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            gap: 12px;
            background: var(--accent);
            color: var(--dark);
            padding: 1.2rem 2.5rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            border: 2px solid transparent;
            transition: var(--transition);
            cursor: pointer;
            justify-content: center;
        }

        .btn i {
            font-size: 1.2rem;
        }

        .btn:hover {
            background: transparent;
            color: var(--accent);
            border-color: var(--accent);
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 15px 30px rgba(212, 175, 55, 0.2);
        }

        .btn-outline {
            background: transparent;
            color: var(--accent);
            border-color: var(--accent);
        }

        .btn-outline:hover {
            background: var(--accent);
            color: var(--dark);
        }

        /* Sections */
        section {
            padding: 100px 0;
        }

        .section-header {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-title {
            font-size: 3rem;
            font-weight: 700;
            margin-bottom: 1rem;
            color: white;
            position: relative;
            display: inline-block;
        }

        .section-title::after {
            content: '';
            position: absolute;
            width: 100px;
            height: 4px;
            background: linear-gradient(90deg, var(--accent), transparent);
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            border-radius: 2px;
        }

        .section-subtitle {
            font-size: 1.2rem;
            color: var(--accent-light);
            max-width: 600px;
            margin: 0 auto;
        }

        /* Benefits */
        .benefits-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }

        .benefit-card {
            background: var(--card-bg);
            padding: 40px 30px;
            border-radius: 20px;
            text-align: center;
            border: 1px solid var(--card-border);
            transition: var(--transition);
            position: relative;
            overflow: hidden;
            opacity: 0;
            transform: translateY(30px);
        }

        .benefit-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, transparent 0%, rgba(212, 175, 55, 0.03) 100%);
            opacity: 0;
            transition: var(--transition);
        }

        .benefit-card.visible {
            opacity: 1;
            transform: translateY(0);
        }

        .benefit-card:hover {
            transform: translateY(-15px);
            border-color: var(--accent);
            box-shadow: var(--shadow);
        }

        .benefit-card:hover::before {
            opacity: 1;
        }

        .benefit-icon {
            width: 80px;
            height: 80px;
            background: rgba(212, 175, 55, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 25px;
            font-size: 2.5rem;
            color: var(--accent);
            transition: var(--transition);
        }

        .benefit-card:hover .benefit-icon {
            background: rgba(212, 175, 55, 0.2);
            transform: scale(1.1) rotate(5deg);
        }

        .benefit-card h3 {
            font-size: 1.6rem;
            margin-bottom: 15px;
            color: white;
        }

        .benefit-card p {
            color: #b0c4ff;
            font-size: 1.1rem;
        }

        /* Services */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 30px;
        }

        .service-card {
            background: var(--card-bg);
            border-radius: 20px;
            padding: 35px 30px;
            border: 1px solid var(--card-border);
            transition: var(--transition);
            display: flex;
            flex-direction: column;
            height: 100%;
            position: relative;
            overflow: hidden;
            opacity: 0;
            transform: translateY(30px);
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent 30%, rgba(212, 175, 55, 0.05) 50%, transparent 70%);
            transform: rotate(45deg);
            transition: var(--transition);
            opacity: 0;
        }

        .service-card.visible {
            opacity: 1;
            transform: translateY(0);
        }

        .service-card:hover {
            transform: translateY(-15px);
            border-color: var(--accent);
            box-shadow: var(--shadow);
        }

        .service-card:hover::before {
            opacity: 1;
            animation: shine 1.5s ease;
        }

        .service-icon {
            font-size: 2.5rem;
            color: var(--accent);
            margin-bottom: 25px;
            transition: var(--transition);
        }

        .service-card:hover .service-icon {
            transform: scale(1.2) rotate(-5deg);
        }

        .service-card h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: white;
            font-weight: 600;
        }

        .service-card p {
            color: #b0c4ff;
            margin-bottom: 30px;
            flex-grow: 1;
            font-size: 1.1rem;
        }

        .service-card .btn {
            align-self: flex-start;
            padding: 12px 28px;
            font-size: 1rem;
        }

        .personal-service {
            border-color: var(--accent);
            background: rgba(212, 175, 55, 0.05);
        }

        .personal-service .service-icon {
            color: var(--accent-light);
        }

        /* Modal */
        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(10, 18, 32, 0.95);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 2000;
            opacity: 0;
            visibility: hidden;
            transition: var(--transition);
            backdrop-filter: blur(10px);
        }

        .modal-overlay.active {
            opacity: 1;
            visibility: visible;
        }

        .modal {
            background: var(--secondary);
            width: 90%;
            max-width: 500px;
            border-radius: 25px;
            padding: 50px 40px;
            text-align: center;
            transform: translateY(50px) scale(0.9);
            transition: var(--transition);
            border: 1px solid var(--accent);
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.5);
            position: relative;
            overflow: hidden;
        }

        .modal::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--accent), var(--accent-light));
        }

        .modal-overlay.active .modal {
            transform: translateY(0) scale(1);
        }

        .modal-icon {
            font-size: 4rem;
            color: var(--accent);
            margin-bottom: 20px;
        }

        .modal h3 {
            font-size: 2rem;
            margin-bottom: 20px;
            color: white;
        }

        .modal p {
            margin-bottom: 35px;
            color: #b0c4ff;
            font-size: 1.1rem;
            line-height: 1.8;
        }

        .modal-buttons {
            display: flex;
            gap: 15px;
            justify-content: center;
        }

        .modal-btn {
            padding: 14px 35px;
            border-radius: 50px;
            border: none;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            font-size: 1rem;
            min-width: 140px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
        }

        .modal-ok {
            background: linear-gradient(135deg, var(--accent), #e6c158);
            color: var(--dark);
        }

        .modal-cancel {
            background: transparent;
            color: var(--light);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .modal-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }

        .modal-ok:hover {
            background: linear-gradient(135deg, #e6c158, var(--accent));
        }

        .modal-cancel:hover {
            background: rgba(255, 255, 255, 0.1);
            border-color: var(--accent);
        }

        /* Footer */
        footer {
            background: var(--primary);
            padding: 70px 0 30px;
            border-top: 1px solid rgba(212, 175, 55, 0.1);
            position: relative;
            overflow: hidden;
        }

        footer::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 1px;
            background: linear-gradient(90deg, transparent, var(--accent), transparent);
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 50px;
            margin-bottom: 50px;
        }

        .footer-logo {
            font-size: 2rem;
            font-weight: 700;
            color: var(--accent);
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 12px;
            margin-bottom: 20px;
        }

        .footer-info p {
            color: #b0c4ff;
            margin-bottom: 20px;
            font-size: 1.1rem;
        }

        .footer-contact h4 {
            color: white;
            font-size: 1.3rem;
            margin-bottom: 20px;
            font-weight: 600;
        }

        .footer-contact a {
            color: var(--accent);
            text-decoration: none;
            font-size: 1.4rem;
            font-weight: 700;
            display: block;
            margin-bottom: 15px;
            transition: var(--transition);
        }

        .footer-contact a:hover {
            color: var(--accent-light);
            transform: translateX(5px);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        .copyright {
            color: #8a9bc1;
            font-size: 1rem;
        }

        /* Animations */
        @keyframes fadeUp {
            from {
                opacity: 0;
                transform: translateY(40px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes shine {
            0% {
                transform: translateX(-100%) translateY(-100%) rotate(45deg);
            }
            100% {
                transform: translateX(100%) translateY(100%) rotate(45deg);
            }
        }

        /* Responsive */
        @media (max-width: 1024px) {
            .hero h1 {
                font-size: 3.2rem;
            }
            
            .section-title {
                font-size: 2.5rem;
            }
            
            .services-grid {
                grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            }
        }

        @media (max-width: 768px) {
            .navbar {
                flex-direction: column;
                gap: 20px;
            }
            
            .hero {
                padding: 180px 0 80px;
                text-align: center;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero-subtitle {
                font-size: 1.2rem;
            }
            
            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .btn {
                width: 100%;
                max-width: 300px;
            }
            
            .section-title {
                font-size: 2.2rem;
            }
            
            .benefits-grid,
            .services-grid {
                grid-template-columns: 1fr;
            }
            
            .modal-buttons {
                flex-direction: column;
            }
            
            .modal-btn {
                width: 100%;
            }
            
            .footer-content {
                grid-template-columns: 1fr;
                text-align: center;
            }
        }

        @media (max-width: 480px) {
            .container {
                padding: 0 16px;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero-subtitle {
                font-size: 1.1rem;
            }
            
            .section-title {
                font-size: 1.8rem;
            }
            
            .modal {
                padding: 30px 20px;
            }
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="navbar">
                <a href="#" class="logo">
                    <i class="fas fa-code"></i>
                    <span>IT Solutions</span>
                </a>
                <div class="nav-contact">
                    <a href="tel:+998999100097" class="phone-link">
                        <i class="fas fa-phone-alt"></i>
                        +998 (99) 910-00-97
                    </a>
                </div>
            </div>
        </div>
    </header>

    <!-- Hero -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Профессиональные IT-услуги</h1>
                <p class="hero-subtitle">Экспертные решения для вашего бизнеса</p>
                <p class="hero-description">Разработка, автоматизация, боты, дизайн и персональные IT-решения премиум-класса. Индивидуальный подход и конфиденциальность гарантированы.</p>
                <div class="hero-buttons">
                    <a href="#services" class="btn">
                        <i class="fas fa-list-alt"></i>
                        Наши услуги
                    </a>
                    <a href="https://wa.me/998999100097?text=Здравствуйте.%20Хочу%20обсудить%20IT-услуги." target="_blank" class="btn btn-outline">
                        <i class="fab fa-whatsapp"></i>
                        WhatsApp консультация
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Benefits -->
    <section id="benefits">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">Наши преимущества</h2>
                <p class="section-subtitle">Почему клиенты выбирают сотрудничество с нами</p>
            </div>
            <div class="benefits-grid">
                <div class="benefit-card">
                    <div class="benefit-icon">
                        <i class="fas fa-bolt"></i>
                    </div>
                    <h3>Быстрое выполнение</h3>
                    <p>Оперативное решение задач в минимальные сроки без потери качества</p>
                </div>
                <div class="benefit-card">
                    <div class="benefit-icon">
                        <i class="fas fa-user-secret"></i>
                    </div>
                    <h3>Полная конфиденциальность</h3>
                    <p>Строгое соблюдение NDA и защита коммерческой тайны</p>
                </div>
                <div class="benefit-card">
                    <div class="benefit-icon">
                        <i class="fas fa-user-cog"></i>
                    </div>
                    <h3>Индивидуальный подход</h3>
                    <p>Персонализированные решения под уникальные требования</p>
                </div>
                <div class="benefit-card">
                    <div class="benefit-icon">
                        <i class="fas fa-code-branch"></i>
                    </div>
                    <h3>Современные технологии</h3>
                    <p>Используем только актуальные технологии и методологии</p>
                </div>
                <div class="benefit-card">
                    <div class="benefit-icon">
                        <i class="fas fa-handshake"></i>
                    </div>
                    <h3>Работа напрямую</h3>
                    <p>Без посредников, переплат и скрытых комиссий</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Services -->
    <section id="services">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">Каталог IT-услуг</h2>
                <p class="section-subtitle">Полный спектр профессиональных IT-решений</p>
            </div>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-laptop-code"></i>
                    </div>
                    <h3>Создание сайтов</h3>
                    <p>Разработка современных веб-сайтов любой сложности: от лендингов до корпоративных порталов с адаптивным дизайном</p>
                    <button class="btn order-btn" data-service="Создание сайтов">
                        <i class="fas fa-paper-plane"></i>
                        Обсудить проект
                    </button>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-shopping-cart"></i>
                    </div>
                    <h3>Интернет-магазины</h3>
                    <p>Полнофункциональные e-commerce решения с интеграцией платежных систем, CRM и систем логистики</p>
                    <button class="btn order-btn" data-service="Создание интернет-магазинов">
                        <i class="fas fa-paper-plane"></i>
                        Обсудить проект
                    </button>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fab fa-telegram"></i>
                    </div>
                    <h3>Telegram-боты</h3>
                    <p>Автоматизация бизнеса через Telegram: боты для рассылок, продаж, поддержки клиентов и CRM</p>
                    <button class="btn order-btn" data-service="Создание Telegram-ботов">
                        <i class="fas fa-paper-plane"></i>
                        Обсудить проект
                    </button>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fab fa-instagram"></i>
                    </div>
                    <h3>Instagram-боты</h3>
                    <p>Автоматизация работы с Instagram: парсинг, аналитика, автоматические действия и продвижение</p>
                    <button class="btn order-btn" data-service="Создание Instagram-ботов">
                        <i class="fas fa-paper-plane"></i>
                        Обсудить проект
                    </button>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-robot"></i>
                    </div>
                    <h3>Автоматизация бизнеса</h3>
                    <p>Оптимизация и автоматизация рутинных операций для повышения эффективности бизнес-процессов</p>
                    <button class="btn order-btn" data-service="Автоматизация бизнес-процессов">
                        <i class="fas fa-paper-plane"></i>
                        Обсудить проект
                    </button>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-headset"></i>
                    </div>
                    <h3>IT-консультации</h3>
                    <p>Экспертные консультации по технологиям, архитектуре, digital-стратегии и оптимизации процессов</p>
                    <button class="btn order-btn" data-service="IT-консультации">
                        <i class="fas fa-paper-plane"></i>
                        Обсудить проект
                    </button>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-tools"></i>
                    </div>
                    <h3>Поддержка проектов</h3>
                    <p>Постоянная техническая поддержка, доработка и развитие ваших IT-проектов</p>
                    <button class="btn order-btn" data-service="Поддержка и сопровождение проектов">
                        <i class="fas fa-paper-plane"></i>
                        Обсудить проект
                    </button>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-palette"></i>
                    </div>
                    <h3>Дизайн обложек</h3>
                    <p>Профессиональный дизайн обложек для YouTube, Instagram, Telegram и других социальных сетей</p>
                    <button class="btn order-btn" data-service="Создание обложек">
                        <i class="fas fa-paper-plane"></i>
                        Обсудить проект
                    </button>
                </div>
                <div class="service-card personal-service">
                    <div class="service-icon">
                        <i class="fas fa-crown"></i>
                    </div>
                    <h3>Персональные IT-решения</h3>
                    <p>Обсуждение индивидуальных задач, нестандартных запросов и эксклюзивных IT-решений под ваш проект</p>
                    <a href="https://wa.me/998999100097?text=Здравствуйте.%20Хочу%20обсудить%20личную%20IT-услугу.%20Мой%20запрос:" target="_blank" class="btn btn-outline">
                        <i class="fab fa-whatsapp"></i>
                        Обсудить личную услугу
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-info">
                    <a href="#" class="footer-logo">
                        <i class="fas fa-code"></i>
                        IT Solutions
                    </a>
                    <p>Предоставляем премиальные IT-услуги с 2018 года. Индивидуальный подход, конфиденциальность и качество — наши основные принципы.</p>
                </div>
                <div class="footer-contact">
                    <h4>Контакты</h4>
                    <a href="tel:+998999100097">
                        <i class="fas fa-phone-alt"></i>
                        +998 (99) 910-00-97
                    </a>
                    <a href="https://wa.me/998999100097" target="_blank">
                        <i class="fab fa-whatsapp"></i>
                        WhatsApp консультация
                    </a>
                </div>
            </div>
            <div class="footer-bottom">
                <p class="copyright">Все услуги оказываются в рамках действующего законодательства</p>
                <p class="copyright">IT Solutions © 2025. Все права защищены.</p>
            </div>
        </div>
    </footer>

    <!-- Modal -->
    <div class="modal-overlay" id="modalOverlay">
        <div class="modal">
            <div class="modal-icon">
                <i class="fas fa-lock"></i>
            </div>
            <h3>Ограниченный доступ</h3>
            <p>Данный контент имеет ограниченный доступ. Для обсуждения деталей, технических требований и индивидуальной стоимости, пожалуйста, свяжитесь напрямую через WhatsApp.</p>
            <div class="modal-buttons">
                <button class="modal-btn modal-ok" id="modalOk">
                    <i class="fab fa-whatsapp"></i>
                    Перейти в WhatsApp
                </button>
                <button class="modal-btn modal-cancel" id="modalCancel">
                    <i class="fas fa-times"></i>
                    Отмена
                </button>
            </div>
        </div>
    </div>

    <script>
        // Элементы DOM
        const modalOverlay = document.getElementById('modalOverlay');
        const modalOk = document.getElementById('modalOk');
        const modalCancel = document.getElementById('modalCancel');
        const orderButtons = document.querySelectorAll('.order-btn');
        let currentService = '';

        // Анимация появления элементов при скролле
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.benefit-card, .service-card').forEach(card => {
            observer.observe(card);
        });

        // Логика модального окна
        orderButtons.forEach(button => {
            button.addEventListener('click', () => {
                currentService = button.getAttribute('data-service');
                modalOverlay.classList.add('active');
                document.body.style.overflow = 'hidden';
            });
        });

        modalCancel.addEventListener('click', () => {
            modalOverlay.classList.remove('active');
            document.body.style.overflow = 'auto';
        });

        modalOverlay.addEventListener('click', (e) => {
            if (e.target === modalOverlay) {
                modalOverlay.classList.remove('active');
                document.body.style.overflow = 'auto';
            }
        });

        modalOk.addEventListener('click', () => {
            const encodedService = encodeURIComponent(currentService);
            const whatsappUrl = `https://wa.me/998999100097?text=Здравствуйте.%20Я%20хочу%20заказать%20IT-услугу:%20${encodedService}.%20Пожалуйста,%20предоставьте%20дополнительную%20информацию.`;
            window.open(whatsappUrl, '_blank');
            modalOverlay.classList.remove('active');
            document.body.style.overflow = 'auto';
        });

        // Закрытие модалки на Escape
        document.addEventListener('keydown', (e) => {
            if (e.key === 'Escape' && modalOverlay.classList.contains('active')) {
                modalOverlay.classList.remove('active');
                document.body.style.overflow = 'auto';
            }
        });

        // Плавный скролл
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                if (this.getAttribute('href') !== '#') {
                    e.preventDefault();
                    const targetId = this.getAttribute('href');
                    if (targetId === '#') return;
                    
                    const targetElement = document.querySelector(targetId);
                    if (targetElement) {
                        window.scrollTo({
                            top: targetElement.offsetTop - 100,
                            behavior: 'smooth'
                        });
                    }
                }
            });
        });

        // Фиксированный хедер
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(15, 26, 48, 0.95)';
                header.style.backdropFilter = 'blur(10px)';
            } else {
                header.style.background = 'var(--gradient)';
                header.style.backdropFilter = 'blur(10px)';
            }
        });
    </script>
</body>
</html>

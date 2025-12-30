# ItSolutions
.
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>IT-услуги | Профессиональные решения</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #1e40af;
            --primary-light: #3b82f6;
            --secondary: #f8fafc;
            --accent: #10b981;
            --accent-hover: #059669;
            --text: #1e293b;
            --text-light: #64748b;
            --border: #e2e8f0;
            --card-bg: #ffffff;
            --shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
            --shadow-hover: 0 8px 25px rgba(0, 0, 0, 0.12);
            --radius: 12px;
            --radius-sm: 8px;
            --radius-lg: 16px;
            --transition: all 0.2s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            -webkit-tap-highlight-color: transparent;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
            color: var(--text);
            background: var(--secondary);
            line-height: 1.5;
            max-width: 100vw;
            overflow-x: hidden;
        }

        /* Mobile First Design */
        .container {
            width: 100%;
            padding: 0 16px;
        }

        /* Header - Mobile App Style */
        .app-header {
            position: sticky;
            top: 0;
            z-index: 1000;
            background: white;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
            padding: 12px 16px;
        }

        .header-top {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 8px;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
            font-weight: 700;
            font-size: 1.3rem;
            color: var(--primary);
            text-decoration: none;
        }

        .logo i {
            font-size: 1.5rem;
        }

        .header-actions {
            display: flex;
            gap: 16px;
            align-items: center;
        }

        .phone-link {
            display: flex;
            align-items: center;
            gap: 6px;
            color: var(--primary);
            font-weight: 600;
            text-decoration: none;
            padding: 8px 12px;
            border-radius: var(--radius-sm);
            background: rgba(30, 64, 175, 0.05);
            font-size: 0.95rem;
        }

        .header-search {
            padding: 12px 16px;
            background: #f8fafc;
            border-radius: var(--radius-sm);
            display: flex;
            align-items: center;
            gap: 10px;
            color: var(--text-light);
            font-size: 0.9rem;
            margin-top: 8px;
        }

        /* Hero Banner - App Style */
        .hero-banner {
            background: linear-gradient(135deg, var(--primary) 0%, var(--primary-light) 100%);
            color: white;
            padding: 24px 16px;
            border-radius: var(--radius-lg);
            margin: 16px;
            position: relative;
            overflow: hidden;
        }

        .hero-banner::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 200px;
            height: 200px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
        }

        .hero-title {
            font-size: 1.8rem;
            font-weight: 700;
            margin-bottom: 8px;
            position: relative;
            z-index: 1;
        }

        .hero-subtitle {
            font-size: 1rem;
            opacity: 0.9;
            margin-bottom: 20px;
            position: relative;
            z-index: 1;
        }

        .hero-cta {
            display: flex;
            gap: 12px;
            position: relative;
            z-index: 1;
        }

        .btn {
            padding: 14px 24px;
            border-radius: var(--radius);
            border: none;
            font-weight: 600;
            font-size: 1rem;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            cursor: pointer;
            transition: var(--transition);
            text-decoration: none;
        }

        .btn-primary {
            background: white;
            color: var(--primary);
        }

        .btn-secondary {
            background: rgba(255, 255, 255, 0.2);
            color: white;
            backdrop-filter: blur(10px);
        }

        .btn-block {
            width: 100%;
        }

        /* Quick Actions - App Style */
        .quick-actions {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 12px;
            padding: 20px 16px;
            border-bottom: 1px solid var(--border);
        }

        .action-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 8px;
            text-decoration: none;
            color: var(--text);
            transition: var(--transition);
        }

        .action-icon {
            width: 48px;
            height: 48px;
            background: var(--card-bg);
            border-radius: var(--radius);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            color: var(--primary);
            box-shadow: var(--shadow);
        }

        .action-text {
            font-size: 0.8rem;
            text-align: center;
            font-weight: 500;
        }

        /* Categories/Services - App Card Style */
        .section-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 16px 12px;
        }

        .section-title {
            font-size: 1.3rem;
            font-weight: 700;
            color: var(--text);
        }

        .see-all {
            color: var(--primary);
            font-size: 0.9rem;
            text-decoration: none;
            font-weight: 500;
        }

        .services-grid {
            padding: 0 16px;
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .service-card {
            background: var(--card-bg);
            border-radius: var(--radius);
            padding: 16px;
            display: flex;
            align-items: center;
            gap: 16px;
            box-shadow: var(--shadow);
            transition: var(--transition);
            border: 1px solid transparent;
        }

        .service-card:hover {
            transform: translateY(-2px);
            box-shadow: var(--shadow-hover);
            border-color: var(--primary-light);
        }

        .service-icon {
            width: 56px;
            height: 56px;
            background: linear-gradient(135deg, #e0f2fe 0%, #dbeafe 100%);
            border-radius: var(--radius);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            color: var(--primary);
            flex-shrink: 0;
        }

        .service-content {
            flex: 1;
        }

        .service-title {
            font-weight: 600;
            margin-bottom: 4px;
            font-size: 1rem;
            color: var(--text);
        }

        .service-description {
            font-size: 0.85rem;
            color: var(--text-light);
            margin-bottom: 8px;
            display: -webkit-box;
            -webkit-line-clamp: 2;
            -webkit-box-orient: vertical;
            overflow: hidden;
        }

        .service-price {
            font-weight: 700;
            color: var(--primary);
            font-size: 0.9rem;
        }

        .service-price span {
            color: var(--text-light);
            font-weight: 400;
            font-size: 0.8rem;
            margin-left: 4px;
        }

        .service-action {
            width: 40px;
            height: 40px;
            background: var(--primary);
            color: white;
            border-radius: var(--radius-sm);
            display: flex;
            align-items: center;
            justify-content: center;
            border: none;
            cursor: pointer;
            transition: var(--transition);
            flex-shrink: 0;
        }

        .service-action:hover {
            background: var(--primary-light);
            transform: scale(1.1);
        }

        /* Features/Benefits - App Style */
        .features-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 12px;
            padding: 20px 16px;
        }

        .feature-card {
            background: var(--card-bg);
            padding: 16px;
            border-radius: var(--radius);
            text-align: center;
            box-shadow: var(--shadow);
        }

        .feature-icon {
            width: 40px;
            height: 40px;
            background: linear-gradient(135deg, #f0f9ff 0%, #eff6ff 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 12px;
            color: var(--primary);
            font-size: 1rem;
        }

        .feature-title {
            font-weight: 600;
            font-size: 0.9rem;
            margin-bottom: 4px;
        }

        .feature-desc {
            font-size: 0.8rem;
            color: var(--text-light);
        }

        /* Personal Service Card - Special */
        .personal-service {
            background: linear-gradient(135deg, #f0f9ff 0%, #e0f2fe 100%);
            border: 2px solid var(--primary);
        }

        .personal-service .service-icon {
            background: linear-gradient(135deg, var(--primary) 0%, var(--primary-light) 100%);
            color: white;
        }

        /* Modal - App Style */
        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 2000;
            padding: 20px;
            opacity: 0;
            visibility: hidden;
            transition: var(--transition);
            backdrop-filter: blur(5px);
        }

        .modal-overlay.active {
            opacity: 1;
            visibility: visible;
        }

        .modal {
            background: white;
            width: 100%;
            max-width: 400px;
            border-radius: var(--radius-lg);
            padding: 24px;
            transform: translateY(20px);
            transition: var(--transition);
            text-align: center;
        }

        .modal-overlay.active .modal {
            transform: translateY(0);
        }

        .modal-icon {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, #fef3c7 0%, #fee2e2 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 16px;
            font-size: 1.8rem;
            color: var(--primary);
        }

        .modal-title {
            font-size: 1.3rem;
            font-weight: 700;
            margin-bottom: 12px;
        }

        .modal-text {
            color: var(--text-light);
            margin-bottom: 24px;
            font-size: 0.95rem;
            line-height: 1.5;
        }

        .modal-actions {
            display: flex;
            gap: 12px;
        }

        .modal-btn {
            flex: 1;
            padding: 14px;
            border-radius: var(--radius);
            border: none;
            font-weight: 600;
            font-size: 1rem;
            cursor: pointer;
            transition: var(--transition);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }

        .modal-btn-primary {
            background: var(--primary);
            color: white;
        }

        .modal-btn-secondary {
            background: var(--secondary);
            color: var(--text);
            border: 1px solid var(--border);
        }

        /* Bottom Navigation - App Style */
        .bottom-nav {
            position: fixed;
            bottom: 0;
            left: 0;
            width: 100%;
            background: white;
            box-shadow: 0 -2px 10px rgba(0, 0, 0, 0.08);
            display: flex;
            justify-content: space-around;
            padding: 12px 0;
            z-index: 1000;
        }

        .nav-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 4px;
            text-decoration: none;
            color: var(--text-light);
            font-size: 0.75rem;
            transition: var(--transition);
            flex: 1;
        }

        .nav-item.active {
            color: var(--primary);
        }

        .nav-icon {
            font-size: 1.2rem;
        }

        /* Footer - App Style */
        .app-footer {
            background: white;
            padding: 30px 16px 80px;
            border-top: 1px solid var(--border);
        }

        .footer-section {
            margin-bottom: 24px;
        }

        .footer-title {
            font-weight: 600;
            margin-bottom: 12px;
            color: var(--text);
        }

        .footer-links {
            display: flex;
            flex-direction: column;
            gap: 8px;
        }

        .footer-link {
            color: var(--text-light);
            text-decoration: none;
            font-size: 0.9rem;
            transition: var(--transition);
        }

        .footer-link:hover {
            color: var(--primary);
        }

        .footer-contact {
            display: flex;
            align-items: center;
            gap: 12px;
            padding: 12px;
            background: var(--secondary);
            border-radius: var(--radius);
            margin-bottom: 20px;
        }

        .contact-icon {
            width: 40px;
            height: 40px;
            background: var(--primary);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1rem;
        }

        .contact-info {
            flex: 1;
        }

        .contact-title {
            font-weight: 600;
            font-size: 0.9rem;
            color: var(--text);
        }

        .contact-number {
            font-weight: 700;
            color: var(--primary);
            font-size: 1.1rem;
        }

        .footer-bottom {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid var(--border);
            color: var(--text-light);
            font-size: 0.85rem;
        }

        /* Desktop version - Hidden by default */
        .desktop-only {
            display: none;
        }

        /* Tablet and Desktop */
        @media (min-width: 768px) {
            .container {
                max-width: 768px;
                margin: 0 auto;
            }

            .quick-actions {
                grid-template-columns: repeat(6, 1fr);
            }

            .features-grid {
                grid-template-columns: repeat(4, 1fr);
            }

            .services-grid {
                display: grid;
                grid-template-columns: repeat(2, 1fr);
                gap: 16px;
            }

            .service-card {
                flex-direction: column;
                align-items: flex-start;
                height: 100%;
            }

            .service-icon {
                width: 64px;
                height: 64px;
                font-size: 1.8rem;
            }

            .service-action {
                width: 100%;
                margin-top: auto;
            }
        }

        @media (min-width: 1024px) {
            .desktop-only {
                display: block;
            }

            .mobile-only {
                display: none;
            }

            .container {
                max-width: 1200px;
            }

            .services-grid {
                grid-template-columns: repeat(3, 1fr);
            }

            .features-grid {
                grid-template-columns: repeat(5, 1fr);
            }

            .bottom-nav {
                display: none;
            }

            .hero-banner {
                margin: 24px 16px;
                padding: 40px;
            }

            .hero-title {
                font-size: 2.5rem;
            }
        }

        /* Animations */
        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(10px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .animate-fade {
            animation: fadeIn 0.3s ease forwards;
        }
    </style>
</head>
<body>
    <!-- Mobile App Header -->
    <header class="app-header">
        <div class="header-top">
            <a href="#" class="logo">
                <i class="fas fa-code"></i>
                <span>IT Services</span>
            </a>
            <div class="header-actions">
                <a href="tel:+998999100097" class="phone-link">
                    <i class="fas fa-phone-alt"></i>
                    <span class="mobile-only">Позвонить</span>
                    <span class="desktop-only">+998 (99) 910-00-97</span>
                </a>
            </div>
        </div>
        <div class="header-search">
            <i class="fas fa-search"></i>
            <span>Поиск IT-услуг...</span>
        </div>
    </header>

    <!-- Main Content -->
    <main>
        <!-- Hero Banner -->
        <section class="hero-banner">
            <h1 class="hero-title">Профессиональные IT-услуги</h1>
            <p class="hero-subtitle">Разработка, автоматизация, боты, дизайн и персональные решения</p>
            <div class="hero-cta">
                <a href="#services" class="btn btn-primary">
                    <i class="fas fa-list"></i>
                    Все услуги
                </a>
                <a href="https://wa.me/998999100097" target="_blank" class="btn btn-secondary">
                    <i class="fab fa-whatsapp"></i>
                    WhatsApp
                </a>
            </div>
        </section>

        <!-- Quick Actions -->
        <section class="quick-actions">
            <a href="#services" class="action-item">
                <div class="action-icon">
                    <i class="fas fa-laptop"></i>
                </div>
                <span class="action-text">Сайты</span>
            </a>
            <a href="#services" class="action-item">
                <div class="action-icon">
                    <i class="fas fa-shopping-cart"></i>
                </div>
                <span class="action-text">Магазины</span>
            </a>
            <a href="#services" class="action-item">
                <div class="action-icon">
                    <i class="fab fa-telegram"></i>
                </div>
                <span class="action-text">Боты</span>
            </a>
            <a href="#services" class="action-item">
                <div class="action-icon">
                    <i class="fas fa-palette"></i>
                </div>
                <span class="action-text">Дизайн</span>
            </a>
        </section>

        <!-- Services Section -->
        <section id="services">
            <div class="section-header">
                <h2 class="section-title">Популярные услуги</h2>
                <a href="#" class="see-all">Все услуги →</a>
            </div>
            <div class="services-grid">
                <!-- Service 1 -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-laptop-code"></i>
                    </div>
                    <div class="service-content">
                        <h3 class="service-title">Создание сайтов</h3>
                        <p class="service-description">Лендинги, корпоративные сайты, веб-приложения любой сложности</p>
                        <div class="service-price">
                            Индивидуальная цена
                            <span>• Обсуждается в чате</span>
                        </div>
                    </div>
                    <button class="service-action order-btn" data-service="Создание сайтов">
                        <i class="fas fa-arrow-right"></i>
                    </button>
                </div>

                <!-- Service 2 -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-shopping-cart"></i>
                    </div>
                    <div class="service-content">
                        <h3 class="service-title">Интернет-магазины</h3>
                        <p class="service-description">Полноценные e-commerce платформы с платежами и CRM</p>
                        <div class="service-price">
                            Индивидуальная цена
                            <span>• Обсуждается в чате</span>
                        </div>
                    </div>
                    <button class="service-action order-btn" data-service="Создание интернет-магазинов">
                        <i class="fas fa-arrow-right"></i>
                    </button>
                </div>

                <!-- Service 3 -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fab fa-telegram"></i>
                    </div>
                    <div class="service-content">
                        <h3 class="service-title">Telegram-боты</h3>
                        <p class="service-description">Автоматизация продаж, рассылок, поддержки и CRM</p>
                        <div class="service-price">
                            Индивидуальная цена
                            <span>• Обсуждается в чате</span>
                        </div>
                    </div>
                    <button class="service-action order-btn" data-service="Создание Telegram-ботов">
                        <i class="fas fa-arrow-right"></i>
                    </button>
                </div>

                <!-- Service 4 -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fab fa-instagram"></i>
                    </div>
                    <div class="service-content">
                        <h3 class="service-title">Instagram-боты</h3>
                        <p class="service-description">Парсинг, аналитика, автоматизация действий и продвижение</p>
                        <div class="service-price">
                            Индивидуальная цена
                            <span>• Обсуждается в чате</span>
                        </div>
                    </div>
                    <button class="service-action order-btn" data-service="Создание Instagram-ботов">
                        <i class="fas fa-arrow-right"></i>
                    </button>
                </div>

                <!-- Service 5 -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-robot"></i>
                    </div>
                    <div class="service-content">
                        <h3 class="service-title">Автоматизация</h3>
                        <p class="service-description">Оптимизация бизнес-процессов и рутинных операций</p>
                        <div class="service-price">
                            Индивидуальная цена
                            <span>• Обсуждается в чате</span>
                        </div>
                    </div>
                    <button class="service-action order-btn" data-service="Автоматизация бизнес-процессов">
                        <i class="fas fa-arrow-right"></i>
                    </button>
                </div>

                <!-- Service 6 -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-headset"></i>
                    </div>
                    <div class="service-content">
                        <h3 class="service-title">IT-консультации</h3>
                        <p class="service-description">Экспертные консультации по технологиям и стратегии</p>
                        <div class="service-price">
                            Индивидуальная цена
                            <span>• Обсуждается в чате</span>
                        </div>
                    </div>
                    <button class="service-action order-btn" data-service="IT-консультации">
                        <i class="fas fa-arrow-right"></i>
                    </button>
                </div>

                <!-- Service 7 -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-tools"></i>
                    </div>
                    <div class="service-content">
                        <h3 class="service-title">Поддержка проектов</h3>
                        <p class="service-description">Техническая поддержка, доработка и развитие IT-проектов</p>
                        <div class="service-price">
                            Индивидуальная цена
                            <span>• Обсуждается в чате</span>
                        </div>
                    </div>
                    <button class="service-action order-btn" data-service="Поддержка и сопровождение проектов">
                        <i class="fas fa-arrow-right"></i>
                    </button>
                </div>

                <!-- Service 8 -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-palette"></i>
                    </div>
                    <div class="service-content">
                        <h3 class="service-title">Дизайн обложек</h3>
                        <p class="service-description">Профессиональный дизайн для YouTube, Instagram, Telegram</p>
                        <div class="service-price">
                            Индивидуальная цена
                            <span>• Обсуждается в чате</span>
                        </div>
                    </div>
                    <button class="service-action order-btn" data-service="Создание обложек">
                        <i class="fas fa-arrow-right"></i>
                    </button>
                </div>

                <!-- Personal Service - Special Card -->
                <div class="service-card personal-service">
                    <div class="service-icon">
                        <i class="fas fa-crown"></i>
                    </div>
                    <div class="service-content">
                        <h3 class="service-title">Личные IT-услуги</h3>
                        <p class="service-description">Индивидуальные решения, нестандартные задачи, персональные IT-проекты</p>
                        <div class="service-price">
                            Личный разговор
                            <span>• Обсуждение деталей в WhatsApp</span>
                        </div>
                    </div>
                    <a href="https://wa.me/998999100097?text=Здравствуйте.%20Хочу%20обсудить%20личную%20IT-услугу.%20Мой%20запрос:" target="_blank" class="service-action">
                        <i class="fab fa-whatsapp"></i>
                    </a>
                </div>
            </div>
        </section>

        <!-- Features Section -->
        <section>
            <div class="section-header">
                <h2 class="section-title">Наши преимущества</h2>
            </div>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-bolt"></i>
                    </div>
                    <h3 class="feature-title">Быстро</h3>
                    <p class="feature-desc">Оперативное выполнение задач</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-lock"></i>
                    </div>
                    <h3 class="feature-title">Конфиденциально</h3>
                    <p class="feature-desc">Защита ваших данных</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-user"></i>
                    </div>
                    <h3 class="feature-title">Индивидуально</h3>
                    <p class="feature-desc">Персональный подход</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-code"></i>
                    </div>
                    <h3 class="feature-title">Современно</h3>
                    <p class="feature-desc">Актуальные технологии</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-handshake"></i>
                    </div>
                    <h3 class="feature-title">Прямая работа</h3>
                    <p class="feature-desc">Без посредников</p>
                </div>
            </div>
        </section>

        <!-- CTA Section -->
        <section style="padding: 40px 16px; text-align: center;">
            <div style="background: linear-gradient(135deg, #f0f9ff 0%, #e0f2fe 100%); padding: 32px; border-radius: var(--radius-lg);">
                <h2 style="font-size: 1.5rem; margin-bottom: 12px; color: var(--text);">Готовы начать проект?</h2>
                <p style="color: var(--text-light); margin-bottom: 24px;">Обсудим детали в WhatsApp и подготовим решение</p>
                <a href="https://wa.me/998999100097" target="_blank" class="btn btn-primary btn-block" style="max-width: 300px; margin: 0 auto;">
                    <i class="fab fa-whatsapp"></i>
                    Начать общение в WhatsApp
                </a>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer class="app-footer">
        <div class="footer-contact">
            <div class="contact-icon">
                <i class="fas fa-phone-alt"></i>
            </div>
            <div class="contact-info">
                <div class="contact-title">Телефон для связи</div>
                <div class="contact-number">+998 (99) 910-00-97</div>
            </div>
        </div>

        <div class="footer-section">
            <h3 class="footer-title">О нас</h3>
            <div class="footer-links">
                <p style="color: var(--text-light); font-size: 0.9rem; line-height: 1.6;">
                    Профессиональные IT-услуги с индивидуальным подходом. Работаем с 2018 года, выполнили более 200 проектов.
                </p>
            </div>
        </div>

        <div class="footer-section">
            <h3 class="footer-title">Контакты</h3>
            <div class="footer-links">
                <a href="tel:+998999100097" class="footer-link">
                    <i class="fas fa-phone-alt"></i> +998 (99) 910-00-97
                </a>
                <a href="https://wa.me/998999100097" target="_blank" class="footer-link">
                    <i class="fab fa-whatsapp"></i> WhatsApp
                </a>
            </div>
        </div>

        <div class="footer-bottom">
            <p>Все услуги оказываются в рамках действующего законодательства</p>
            <p>IT Services © 2025</p>
        </div>
    </footer>

    <!-- Bottom Navigation (Mobile) -->
    <nav class="bottom-nav mobile-only">
        <a href="#" class="nav-item active">
            <i class="fas fa-home nav-icon"></i>
            <span>Главная</span>
        </a>
        <a href="#services" class="nav-item">
            <i class="fas fa-th-large nav-icon"></i>
            <span>Услуги</span>
        </a>
        <a href="#" class="nav-item">
            <i class="fas fa-shopping-cart nav-icon"></i>
            <span>Заказы</span>
        </a>
        <a href="tel:+998999100097" class="nav-item">
            <i class="fas fa-phone nav-icon"></i>
            <span>Контакты</span>
        </a>
    </nav>

    <!-- Modal -->
    <div class="modal-overlay" id="modalOverlay">
        <div class="modal">
            <div class="modal-icon">
                <i class="fas fa-lock"></i>
            </div>
            <h2 class="modal-title">Ограниченный доступ</h2>
            <p class="modal-text">Для обсуждения деталей и стоимости данной услуги, пожалуйста, свяжитесь с нами напрямую в WhatsApp.</p>
            <div class="modal-actions">
                <button class="modal-btn modal-btn-primary" id="modalOk">
                    <i class="fab fa-whatsapp"></i>
                    WhatsApp
                </button>
                <button class="modal-btn modal-btn-secondary" id="modalCancel">
                    Отмена
                </button>
            </div>
        </div>
    </div>

    <script>
        // DOM Elements
        const modalOverlay = document.getElementById('modalOverlay');
        const modalOk = document.getElementById('modalOk');
        const modalCancel = document.getElementById('modalCancel');
        const orderButtons = document.querySelectorAll('.order-btn');
        let currentService = '';

        // Initialize animations
        document.addEventListener('DOMContentLoaded', () => {
            // Add animation to elements on load
            const cards = document.querySelectorAll('.service-card, .feature-card');
            cards.forEach((card, index) => {
                card.style.animationDelay = `${index * 0.1}s`;
                card.classList.add('animate-fade');
            });
        });

        // Modal Logic
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

        // Close modal on Escape
        document.addEventListener('keydown', (e) => {
            if (e.key === 'Escape' && modalOverlay.classList.contains('active')) {
                modalOverlay.classList.remove('active');
                document.body.style.overflow = 'auto';
            }
        });

        // Smooth scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                if (this.getAttribute('href') !== '#') {
                    e.preventDefault();
                    const targetId = this.getAttribute('href');
                    if (targetId === '#') return;
                    
                    const targetElement = document.querySelector(targetId);
                    if (targetElement) {
                        window.scrollTo({
                            top: targetElement.offsetTop - 80,
                            behavior: 'smooth'
                        });
                    }
                }
            });
        });

        // Bottom navigation active state
        const navItems = document.querySelectorAll('.nav-item');
        navItems.forEach(item => {
            item.addEventListener('click', () => {
                navItems.forEach(nav => nav.classList.remove('active'));
                item.classList.add('active');
            });
        });

        // Search functionality
        const searchInput = document.querySelector('.header-search');
        searchInput.addEventListener('click', () => {
            alert('Введите название услуги для поиска...');
        });

        // Add hover effects for desktop
        if (window.innerWidth >= 1024) {
            document.querySelectorAll('.service-card').forEach(card => {
                card.addEventListener('mouseenter', () => {
                    card.style.transform = 'translateY(-8px)';
                    card.style.boxShadow = '0 15px 35px rgba(0, 0, 0, 0.15)';
                });
                
                card.addEventListener('mouseleave', () => {
                    card.style.transform = 'translateY(0)';
                    card.style.boxShadow = '0 2px 8px rgba(0, 0, 0, 0.08)';
                });
            });
        }
    </script>
</body>
</html>

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

        /* Promo Banner */
        .promo-banner {
            background: linear-gradient(135deg, #f59e0b 0%, #fbbf24 100%);
            color: #78350f;
            padding: 12px 16px;
            text-align: center;
            font-weight: 600;
            position: relative;
            overflow: hidden;
            animation: pulse 2s infinite;
        }

        .promo-banner::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent 30%, rgba(255, 255, 255, 0.2) 50%, transparent 70%);
            transform: rotate(45deg);
            animation: shine 3s infinite;
        }

        .promo-text {
            position: relative;
            z-index: 1;
        }

        .promo-timer {
            font-weight: 700;
            color: #dc2626;
            background: white;
            padding: 2px 8px;
            border-radius: 20px;
            margin-left: 8px;
            display: inline-block;
            animation: heartbeat 1.5s infinite;
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

        .cart-badge {
            position: relative;
            background: none;
            border: none;
            cursor: pointer;
        }

        .cart-count {
            position: absolute;
            top: -8px;
            right: -8px;
            background: #ef4444;
            color: white;
            font-size: 0.7rem;
            min-width: 18px;
            height: 18px;
            border-radius: 9px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 600;
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
            cursor: pointer;
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

        /* Daily Prize Section */
        .daily-prize {
            background: linear-gradient(135deg, #7c3aed 0%, #a78bfa 100%);
            color: white;
            padding: 20px;
            border-radius: var(--radius-lg);
            margin: 20px 16px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .daily-prize::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url("data:image/svg+xml,%3Csvg width='100' height='100' viewBox='0 0 100 100' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M11 18c3.866 0 7-3.134 7-7s-3.134-7-7-7-7 3.134-7 7 3.134 7 7 7zm48 25c3.866 0 7-3.134 7-7s-3.134-7-7-7-7 3.134-7 7 3.134 7 7 7zm-43-7c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zm63 31c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zM34 90c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zm56-76c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zM12 86c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm28-65c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm23-11c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zm-6 60c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm29 22c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zM32 63c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zm57-13c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zm-9-21c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2zM60 91c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2zM35 41c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2zM12 60c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2z' fill='%23ffffff' fill-opacity='0.1' fill-rule='evenodd'/%3E%3C/svg%3E");
            opacity: 0.1;
        }

        .prize-title {
            font-size: 1.4rem;
            font-weight: 700;
            margin-bottom: 8px;
            position: relative;
            z-index: 1;
        }

        .prize-subtitle {
            font-size: 0.9rem;
            opacity: 0.9;
            margin-bottom: 16px;
            position: relative;
            z-index: 1;
        }

        .prize-item {
            background: rgba(255, 255, 255, 0.2);
            padding: 16px;
            border-radius: var(--radius);
            margin-bottom: 16px;
            backdrop-filter: blur(10px);
            border: 2px solid rgba(255, 255, 255, 0.3);
            position: relative;
            z-index: 1;
        }

        .prize-item-name {
            font-size: 1.2rem;
            font-weight: 700;
            margin-bottom: 8px;
        }

        .prize-item-desc {
            font-size: 0.9rem;
            opacity: 0.9;
        }

        .win-button {
            background: white;
            color: #7c3aed;
            border: none;
            padding: 12px 24px;
            border-radius: 50px;
            font-weight: 700;
            font-size: 1rem;
            cursor: pointer;
            transition: var(--transition);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            margin: 0 auto;
            position: relative;
            z-index: 1;
        }

        .win-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 20px rgba(124, 58, 237, 0.3);
        }

        .winner-info {
            margin-top: 16px;
            font-size: 0.9rem;
            opacity: 0.9;
            position: relative;
            z-index: 1;
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

        .service-actions {
            display: flex;
            gap: 8px;
            align-items: center;
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

        .add-to-cart-btn {
            background: var(--accent);
        }

        .add-to-cart-btn:hover {
            background: var(--accent-hover);
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

        /* Cart Modal */
        .cart-modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            display: flex;
            align-items: flex-end;
            justify-content: center;
            z-index: 2001;
            opacity: 0;
            visibility: hidden;
            transition: var(--transition);
        }

        .cart-modal-overlay.active {
            opacity: 1;
            visibility: visible;
        }

        .cart-modal {
            background: white;
            width: 100%;
            max-height: 80vh;
            border-radius: var(--radius-lg) var(--radius-lg) 0 0;
            transform: translateY(100%);
            transition: var(--transition);
            display: flex;
            flex-direction: column;
        }

        .cart-modal-overlay.active .cart-modal {
            transform: translateY(0);
        }

        .cart-header {
            padding: 20px;
            border-bottom: 1px solid var(--border);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .cart-title {
            font-size: 1.3rem;
            font-weight: 700;
        }

        .cart-close {
            background: none;
            border: none;
            font-size: 1.2rem;
            color: var(--text-light);
            cursor: pointer;
        }

        .cart-items {
            flex: 1;
            overflow-y: auto;
            padding: 20px;
        }

        .cart-empty {
            text-align: center;
            padding: 40px 20px;
            color: var(--text-light);
        }

        .cart-empty i {
            font-size: 3rem;
            margin-bottom: 16px;
            opacity: 0.5;
        }

        .cart-item {
            display: flex;
            align-items: center;
            gap: 12px;
            padding: 12px 0;
            border-bottom: 1px solid var(--border);
        }

        .cart-item-icon {
            width: 40px;
            height: 40px;
            background: linear-gradient(135deg, #e0f2fe 0%, #dbeafe 100%);
            border-radius: var(--radius-sm);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary);
        }

        .cart-item-info {
            flex: 1;
        }

        .cart-item-title {
            font-weight: 600;
            font-size: 0.9rem;
            margin-bottom: 4px;
        }

        .cart-item-remove {
            background: none;
            border: none;
            color: #ef4444;
            font-size: 1.2rem;
            cursor: pointer;
            padding: 4px;
        }

        .cart-footer {
            padding: 20px;
            border-top: 1px solid var(--border);
            background: var(--secondary);
        }

        .cart-total {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 16px;
            font-weight: 600;
        }

        .cart-total-items {
            color: var(--text-light);
            font-size: 0.9rem;
        }

        .cart-total-count {
            color: var(--primary);
            font-size: 1.1rem;
        }

        /* Search Modal */
        .search-modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: white;
            z-index: 2002;
            opacity: 0;
            visibility: hidden;
            transition: var(--transition);
        }

        .search-modal-overlay.active {
            opacity: 1;
            visibility: visible;
        }

        .search-header {
            padding: 16px;
            border-bottom: 1px solid var(--border);
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .search-input {
            flex: 1;
            padding: 12px 16px;
            border: 1px solid var(--border);
            border-radius: var(--radius);
            font-size: 1rem;
            outline: none;
        }

        .search-input:focus {
            border-color: var(--primary);
        }

        .search-close {
            background: none;
            border: none;
            font-size: 1.2rem;
            color: var(--text-light);
            cursor: pointer;
        }

        .search-results {
            padding: 16px;
            max-height: calc(100vh - 80px);
            overflow-y: auto;
        }

        .search-result-item {
            display: flex;
            align-items: center;
            gap: 12px;
            padding: 12px;
            border-radius: var(--radius);
            margin-bottom: 8px;
            cursor: pointer;
            transition: var(--transition);
        }

        .search-result-item:hover {
            background: var(--secondary);
        }

        .search-result-icon {
            width: 40px;
            height: 40px;
            background: linear-gradient(135deg, #e0f2fe 0%, #dbeafe 100%);
            border-radius: var(--radius-sm);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary);
        }

        .search-result-info {
            flex: 1;
        }

        .search-result-title {
            font-weight: 600;
            font-size: 0.95rem;
            margin-bottom: 2px;
        }

        .search-result-desc {
            font-size: 0.85rem;
            color: var(--text-light);
        }

        .no-results {
            text-align: center;
            padding: 40px 20px;
            color: var(--text-light);
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

        /* Win Modal */
        .win-modal .modal-icon {
            background: linear-gradient(135deg, #7c3aed 0%, #a78bfa 100%);
            color: white;
        }

        .prize-details {
            text-align: left;
            background: #f8fafc;
            padding: 16px;
            border-radius: var(--radius);
            margin-bottom: 20px;
        }

        .prize-name {
            font-weight: 700;
            color: #7c3aed;
            font-size: 1.2rem;
            margin-bottom: 8px;
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
            background: none;
            border: none;
            cursor: pointer;
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

            .service-actions {
                width: 100%;
                margin-top: auto;
            }

            .cart-modal {
                max-width: 500px;
                max-height: 600px;
                border-radius: var(--radius-lg);
                margin: auto;
                align-self: center;
            }

            .search-modal-overlay {
                display: flex;
                align-items: center;
                justify-content: center;
            }

            .search-results {
                max-width: 600px;
                max-height: 600px;
                border-radius: var(--radius-lg);
                background: white;
                margin: auto;
                box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
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

        @keyframes pulse {
            0% { opacity: 1; }
            50% { opacity: 0.8; }
            100% { opacity: 1; }
        }

        @keyframes shine {
            0% { transform: translateX(-100%) translateY(-100%) rotate(45deg); }
            100% { transform: translateX(100%) translateY(100%) rotate(45deg); }
        }

        @keyframes heartbeat {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }

        .animate-fade {
            animation: fadeIn 0.3s ease forwards;
        }

        @keyframes slideIn {
            from {
                transform: translateY(20px);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        .animate-slide {
            animation: slideIn 0.3s ease forwards;
        }

        /* Confetti */
        .confetti {
            position: fixed;
            width: 10px;
            height: 10px;
            background: #f59e0b;
            top: 0;
            opacity: 0;
            z-index: 9999;
            pointer-events: none;
        }

        .confetti:nth-child(odd) {
            background: #ef4444;
        }

        .confetti:nth-child(even) {
            background: #3b82f6;
        }

        .confetti:nth-child(3n) {
            background: #10b981;
        }

        .confetti:nth-child(5n) {
            width: 6px;
            height: 6px;
            animation-duration: 2s;
        }
    </style>
</head>
<body>
    <!-- Promo Banner -->
    <div class="promo-banner">
        <div class="promo-text">
            🎁 АКЦИЯ: Выиграйте услугу БЕСПЛАТНО до 
            <span class="promo-timer" id="promoTimer">5 января</span>
            🎁
        </div>
    </div>

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
                <button class="cart-badge" id="cartButton">
                    <i class="fas fa-shopping-cart" style="font-size: 1.2rem; color: var(--primary);"></i>
                    <span class="cart-count" id="cartCount">0</span>
                </button>
            </div>
        </div>
        <div class="header-search" id="searchButton">
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

        <!-- Daily Prize Section -->
        <section class="daily-prize" id="dailyPrize">
            <h2 class="prize-title">🎁 Ежедневный розыгрыш! 🎁</h2>
            <p class="prize-subtitle">Попробуйте удачу и выиграйте услугу БЕСПЛАТНО!</p>
            
            <div class="prize-item">
                <div class="prize-item-name" id="prizeName">Создание Telegram-бота</div>
                <div class="prize-item-desc" id="prizeDesc">Автоматизация продаж, рассылок и поддержки</div>
            </div>
            
            <button class="win-button" id="winButton">
                <i class="fas fa-gift"></i>
                Испытать удачу
            </button>
            
            <div class="winner-info" id="winnerInfo">
                Сегодня уже выиграли: <span id="winnerCount">0</span> человек
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
            <div class="services-grid" id="servicesList">
                <!-- Service cards will be populated by JavaScript -->
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
        <button class="nav-item" id="mobileCartButton">
            <i class="fas fa-shopping-cart nav-icon"></i>
            <span>Корзина</span>
            <span class="cart-count" id="mobileCartCount" style="position: absolute; top: 0; right: 25px; background: #ef4444; color: white; font-size: 0.6rem; min-width: 16px; height: 16px; border-radius: 8px; display: flex; align-items: center; justify-content: center;">0</span>
        </button>
        <button class="nav-item" id="mobilePrizeButton">
            <i class="fas fa-gift nav-icon"></i>
            <span>Подарок</span>
        </button>
    </nav>

    <!-- Cart Modal -->
    <div class="cart-modal-overlay" id="cartModal">
        <div class="cart-modal">
            <div class="cart-header">
                <h3 class="cart-title">Корзина услуг</h3>
                <button class="cart-close" id="cartClose">
                    <i class="fas fa-times"></i>
                </button>
            </div>
            <div class="cart-items" id="cartItems">
                <!-- Cart items will be populated by JavaScript -->
                <div class="cart-empty" id="emptyCart">
                    <i class="fas fa-shopping-cart"></i>
                    <p>Корзина пуста</p>
                    <p style="font-size: 0.9rem; margin-top: 8px;">Добавьте услуги из каталога</p>
                </div>
            </div>
            <div class="cart-footer">
                <div class="cart-total">
                    <span class="cart-total-items">Всего услуг:</span>
                    <span class="cart-total-count" id="cartTotalCount">0</span>
                </div>
                <button class="btn btn-primary btn-block" id="checkoutButton" style="display: none;">
                    <i class="fab fa-whatsapp"></i>
                    Оформить заказ в WhatsApp
                </button>
            </div>
        </div>
    </div>

    <!-- Search Modal -->
    <div class="search-modal-overlay" id="searchModal">
        <div class="search-header">
            <input type="text" class="search-input" id="searchInput" placeholder="Поиск IT-услуг..." autofocus>
            <button class="search-close" id="searchClose">
                <i class="fas fa-times"></i>
            </button>
        </div>
        <div class="search-results" id="searchResults">
            <!-- Search results will be populated by JavaScript -->
        </div>
    </div>

    <!-- Order Modal -->
    <div class="modal-overlay" id="orderModal">
        <div class="modal">
            <div class="modal-icon">
                <i class="fas fa-shopping-cart"></i>
            </div>
            <h2 class="modal-title">Отправить заказ?</h2>
            <p class="modal-text" id="orderModalText">Ваш заказ будет отправлен в WhatsApp. Продолжить?</p>
            <div class="modal-actions">
                <button class="modal-btn modal-btn-primary" id="confirmOrder">
                    <i class="fab fa-whatsapp"></i>
                    Отправить
                </button>
                <button class="modal-btn modal-btn-secondary" id="cancelOrder">
                    Отмена
                </button>
            </div>
        </div>
    </div>

    <!-- Win Modal -->
    <div class="modal-overlay win-modal" id="winModal">
        <div class="modal">
            <div class="modal-icon">
                <i class="fas fa-gift"></i>
            </div>
            <h2 class="modal-title" id="winModalTitle">Поздравляем! 🎉</h2>
            <div class="prize-details">
                <div class="prize-name" id="wonPrizeName">Создание Telegram-бота</div>
                <p>Вы выиграли эту услугу БЕСПЛАТНО!</p>
                <p>Услуга будет предоставлена бесплатно при заказе любой другой услуги.</p>
            </div>
            <p class="modal-text">Хотите добавить выигранную услугу в корзину и оформить заказ?</p>
            <div class="modal-actions">
                <button class="modal-btn modal-btn-primary" id="addPrizeToCart">
                    <i class="fas fa-cart-plus"></i>
                    Добавить и заказать
                </button>
                <button class="modal-btn modal-btn-secondary" id="closeWinModal">
                    Позже
                </button>
            </div>
        </div>
    </div>

    <!-- Confetti Container -->
    <div id="confettiContainer"></div>

    <script>
        // Data
        const services = [
            {
                id: 1,
                title: "Создание сайтов",
                description: "Лендинги, корпоративные сайты, веб-приложения любой сложности",
                icon: "fas fa-laptop-code",
                category: "web"
            },
            {
                id: 2,
                title: "Интернет-магазины",
                description: "Полноценные e-commerce платформы с платежами и CRM",
                icon: "fas fa-shopping-cart",
                category: "web"
            },
            {
                id: 3,
                title: "Telegram-боты",
                description: "Автоматизация продаж, рассылок, поддержки и CRM",
                icon: "fab fa-telegram",
                category: "bots"
            },
            {
                id: 4,
                title: "Instagram-боты",
                description: "Парсинг, аналитика, автоматизация действий и продвижение",
                icon: "fab fa-instagram",
                category: "bots"
            },
            {
                id: 5,
                title: "Автоматизация",
                description: "Оптимизация бизнес-процессов и рутинных операций",
                icon: "fas fa-robot",
                category: "automation"
            },
            {
                id: 6,
                title: "IT-консультации",
                description: "Экспертные консультации по технологиям и стратегии",
                icon: "fas fa-headset",
                category: "consulting"
            },
            {
                id: 7,
                title: "Поддержка проектов",
                description: "Техническая поддержка, доработка и развитие IT-проектов",
                icon: "fas fa-tools",
                category: "support"
            },
            {
                id: 8,
                title: "Дизайн обложек",
                description: "Профессиональный дизайн для YouTube, Instagram, Telegram",
                icon: "fas fa-palette",
                category: "design"
            },
            {
                id: 9,
                title: "Личные IT-услуги",
                description: "Индивидуальные решения, нестандартные задачи, персональные IT-проекты",
                icon: "fas fa-crown",
                category: "personal",
                isPersonal: true
            }
        ];

        // State
        let cart = JSON.parse(localStorage.getItem('it-cart')) || [];
        let searchResults = [];
        let dailyPrize = null;
        let todayWinners = parseInt(localStorage.getItem('today-winners')) || 0;
        let userWonToday = localStorage.getItem('user-won-today') === 'true';

        // DOM Elements
        const cartButton = document.getElementById('cartButton');
        const mobileCartButton = document.getElementById('mobileCartButton');
        const cartModal = document.getElementById('cartModal');
        const cartClose = document.getElementById('cartClose');
        const cartItems = document.getElementById('cartItems');
        const emptyCart = document.getElementById('emptyCart');
        const cartCount = document.getElementById('cartCount');
        const mobileCartCount = document.getElementById('mobileCartCount');
        const cartTotalCount = document.getElementById('cartTotalCount');
        const checkoutButton = document.getElementById('checkoutButton');
        const searchButton = document.getElementById('searchButton');
        const searchModal = document.getElementById('searchModal');
        const searchClose = document.getElementById('searchClose');
        const searchInput = document.getElementById('searchInput');
        const searchResultsContainer = document.getElementById('searchResults');
        const servicesList = document.getElementById('servicesList');
        const orderModal = document.getElementById('orderModal');
        const orderModalText = document.getElementById('orderModalText');
        const confirmOrder = document.getElementById('confirmOrder');
        const cancelOrder = document.getElementById('cancelOrder');
        const winButton = document.getElementById('winButton');
        const winModal = document.getElementById('winModal');
        const winModalTitle = document.getElementById('winModalTitle');
        const wonPrizeName = document.getElementById('wonPrizeName');
        const addPrizeToCart = document.getElementById('addPrizeToCart');
        const closeWinModal = document.getElementById('closeWinModal');
        const prizeName = document.getElementById('prizeName');
        const prizeDesc = document.getElementById('prizeDesc');
        const winnerInfo = document.getElementById('winnerInfo');
        const winnerCount = document.getElementById('winnerCount');
        const mobilePrizeButton = document.getElementById('mobilePrizeButton');
        const promoTimer = document.getElementById('promoTimer');

        // Initialize
        document.addEventListener('DOMContentLoaded', () => {
            initDailyPrize();
            renderServices();
            updateCartCount();
            renderCart();
            updatePromoTimer();
            
            // Add event listeners
            cartButton.addEventListener('click', openCart);
            mobileCartButton.addEventListener('click', openCart);
            cartClose.addEventListener('click', closeCart);
            checkoutButton.addEventListener('click', openOrderModal);
            searchButton.addEventListener('click', openSearch);
            searchClose.addEventListener('click', closeSearch);
            searchInput.addEventListener('input', handleSearch);
            confirmOrder.addEventListener('click', sendOrderToWhatsApp);
            cancelOrder.addEventListener('click', closeOrderModal);
            winButton.addEventListener('click', tryToWin);
            addPrizeToCart.addEventListener('click', addPrizeAndOrder);
            closeWinModal.addEventListener('click', closeWinModalFunc);
            mobilePrizeButton.addEventListener('click', () => {
                document.getElementById('dailyPrize').scrollIntoView({ behavior: 'smooth' });
            });
            
            // Close modals on overlay click
            cartModal.addEventListener('click', (e) => {
                if (e.target === cartModal) closeCart();
            });
            
            searchModal.addEventListener('click', (e) => {
                if (e.target === searchModal) closeSearch();
            });
            
            orderModal.addEventListener('click', (e) => {
                if (e.target === orderModal) closeOrderModal();
            });
            
            winModal.addEventListener('click', (e) => {
                if (e.target === winModal) closeWinModalFunc();
            });
            
            // Close modals on Escape
            document.addEventListener('keydown', (e) => {
                if (e.key === 'Escape') {
                    closeSearch();
                    closeCart();
                    closeOrderModal();
                    closeWinModalFunc();
                }
            });
        });

        // Initialize Daily Prize
        function initDailyPrize() {
            // Check if it's a new day
            const today = new Date().toDateString();
            const lastPrizeDate = localStorage.getItem('last-prize-date');
            
            if (lastPrizeDate !== today) {
                // New day - reset
                localStorage.setItem('last-prize-date', today);
                localStorage.setItem('today-winners', '0');
                localStorage.setItem('user-won-today', 'false');
                todayWinners = 0;
                userWonToday = false;
                
                // Select random prize
                const eligibleServices = services.filter(s => !s.isPersonal);
                dailyPrize = eligibleServices[Math.floor(Math.random() * eligibleServices.length)];
                localStorage.setItem('daily-prize', JSON.stringify(dailyPrize));
            } else {
                // Same day - load existing prize
                dailyPrize = JSON.parse(localStorage.getItem('daily-prize')) || 
                    services.find(s => s.id === 3); // Default to Telegram bot
            }
            
            // Update display
            prizeName.textContent = dailyPrize.title;
            prizeDesc.textContent = dailyPrize.description;
            winnerCount.textContent = todayWinners;
            
            // Update win button if user already won today
            if (userWonToday) {
                winButton.innerHTML = '<i class="fas fa-check"></i> Вы уже участвовали сегодня';
                winButton.style.background = '#10b981';
                winButton.disabled = true;
            }
        }

        // Render Services
        function renderServices() {
            servicesList.innerHTML = '';
            
            services.forEach(service => {
                const isInCart = cart.some(item => item.id === service.id);
                
                const serviceCard = document.createElement('div');
                serviceCard.className = `service-card ${service.isPersonal ? 'personal-service' : ''}`;
                serviceCard.innerHTML = `
                    <div class="service-icon">
                        <i class="${service.icon}"></i>
                    </div>
                    <div class="service-content">
                        <h3 class="service-title">${service.title}</h3>
                        <p class="service-description">${service.description}</p>
                        <div class="service-price">
                            Индивидуальная цена
                            <span>• Обсуждается в чате</span>
                        </div>
                    </div>
                    <div class="service-actions">
                        ${service.isPersonal ? 
                            `<a href="https://wa.me/998999100097?text=${encodeURIComponent(`Здравствуйте. Хочу обсудить личную IT-услугу: ${service.title}. Мой запрос:`)}" target="_blank" class="service-action">
                                <i class="fab fa-whatsapp"></i>
                            </a>` :
                            `<button class="service-action ${isInCart ? 'add-to-cart-btn' : ''}" data-id="${service.id}" data-title="${service.title}">
                                <i class="${isInCart ? 'fas fa-check' : 'fas fa-plus'}"></i>
                            </button>
                            <button class="service-action order-btn" data-service="${service.title}">
                                <i class="fas fa-arrow-right"></i>
                            </button>`
                        }
                    </div>
                `;
                
                servicesList.appendChild(serviceCard);
            });
            
            // Add event listeners to service buttons
            document.querySelectorAll('.order-btn').forEach(button => {
                button.addEventListener('click', (e) => {
                    e.stopPropagation();
                    const serviceTitle = button.getAttribute('data-service');
                    showSingleOrderModal(serviceTitle);
                });
            });
            
            document.querySelectorAll('.service-action[data-id]').forEach(button => {
                button.addEventListener('click', (e) => {
                    e.stopPropagation();
                    const id = parseInt(button.getAttribute('data-id'));
                    const title = button.getAttribute('data-title');
                    toggleCartItem(id, title);
                });
            });
        }

        // Cart Functions
        function toggleCartItem(id, title) {
            const existingIndex = cart.findIndex(item => item.id === id);
            
            if (existingIndex > -1) {
                cart.splice(existingIndex, 1);
            } else {
                cart.push({ id, title });
            }
            
            saveCart();
            updateCartCount();
            renderCart();
            renderServices();
        }

        function removeCartItem(id) {
            cart = cart.filter(item => item.id !== id);
            saveCart();
            updateCartCount();
            renderCart();
            renderServices();
        }

        function updateCartCount() {
            const count = cart.length;
            cartCount.textContent = count;
            mobileCartCount.textContent = count;
            cartTotalCount.textContent = count;
            
            if (count > 0) {
                checkoutButton.style.display = 'block';
            } else {
                checkoutButton.style.display = 'none';
            }
        }

        function renderCart() {
            cartItems.innerHTML = '';
            
            if (cart.length === 0) {
                cartItems.appendChild(emptyCart.cloneNode(true));
                return;
            }
            
            cart.forEach(item => {
                const service = services.find(s => s.id === item.id);
                
                const cartItem = document.createElement('div');
                cartItem.className = 'cart-item animate-slide';
                cartItem.innerHTML = `
                    <div class="cart-item-icon">
                        <i class="${service.icon}"></i>
                    </div>
                    <div class="cart-item-info">
                        <div class="cart-item-title">${service.title}</div>
                        <div style="font-size: 0.8rem; color: var(--text-light);">Индивидуальная цена</div>
                    </div>
                    <button class="cart-item-remove" data-id="${item.id}">
                        <i class="fas fa-trash"></i>
                    </button>
                `;
                
                cartItems.appendChild(cartItem);
            });
            
            // Add event listeners to remove buttons
            document.querySelectorAll('.cart-item-remove').forEach(button => {
                button.addEventListener('click', (e) => {
                    const id = parseInt(button.getAttribute('data-id'));
                    removeCartItem(id);
                });
            });
        }

        function saveCart() {
            localStorage.setItem('it-cart', JSON.stringify(cart));
        }

        // Modal Functions
        function openCart() {
            cartModal.classList.add('active');
            document.body.style.overflow = 'hidden';
        }

        function closeCart() {
            cartModal.classList.remove('active');
            document.body.style.overflow = 'auto';
        }

        function openSearch() {
            searchModal.classList.add('active');
            document.body.style.overflow = 'hidden';
            searchInput.focus();
        }

        function closeSearch() {
            searchModal.classList.remove('active');
            document.body.style.overflow = 'auto';
            searchInput.value = '';
            searchResultsContainer.innerHTML = '';
        }

        function openOrderModal() {
            orderModal.classList.add('active');
            document.body.style.overflow = 'hidden';
        }

        function closeOrderModal() {
            orderModal.classList.remove('active');
            document.body.style.overflow = 'auto';
        }

        function closeWinModalFunc() {
            winModal.classList.remove('active');
            document.body.style.overflow = 'auto';
        }

        // Search Functions
        function handleSearch(e) {
            const query = e.target.value.toLowerCase().trim();
            
            if (query.length === 0) {
                searchResultsContainer.innerHTML = '';
                return;
            }
            
            searchResults = services.filter(service => 
                service.title.toLowerCase().includes(query) || 
                service.description.toLowerCase().includes(query)
            );
            
            renderSearchResults();
        }

        function renderSearchResults() {
            searchResultsContainer.innerHTML = '';
            
            if (searchResults.length === 0) {
                searchResultsContainer.innerHTML = `
                    <div class="no-results">
                        <i class="fas fa-search" style="font-size: 2rem; margin-bottom: 16px; opacity: 0.5;"></i>
                        <p>Ничего не найдено</p>
                        <p style="font-size: 0.9rem; margin-top: 8px;">Попробуйте другой запрос</p>
                    </div>
                `;
                return;
            }
            
            searchResults.forEach(service => {
                const resultItem = document.createElement('div');
                resultItem.className = 'search-result-item';
                resultItem.innerHTML = `
                    <div class="search-result-icon">
                        <i class="${service.icon}"></i>
                    </div>
                    <div class="search-result-info">
                        <div class="search-result-title">${service.title}</div>
                        <div class="search-result-desc">${service.description}</div>
                    </div>
                `;
                
                resultItem.addEventListener('click', () => {
                    closeSearch();
                    // Scroll to services
                    document.getElementById('services').scrollIntoView({ behavior: 'smooth' });
                    // Highlight the service
                    setTimeout(() => {
                        const serviceCard = document.querySelector(`[data-id="${service.id}"]`)?.closest('.service-card');
                        if (serviceCard) {
                            serviceCard.style.animation = 'none';
                            setTimeout(() => {
                                serviceCard.style.animation = 'pulse 0.5s';
                                serviceCard.style.backgroundColor = 'rgba(30, 64, 175, 0.05)';
                                setTimeout(() => {
                                    serviceCard.style.backgroundColor = '';
                                }, 2000);
                            }, 10);
                        }
                    }, 300);
                });
                
                searchResultsContainer.appendChild(resultItem);
            });
        }

        // Try to Win Function
        function tryToWin() {
            if (userWonToday) {
                alert('Вы уже участвовали в розыгрыше сегодня. Попробуйте завтра!');
                return;
            }
            
            // 30% chance to win
            const won = Math.random() < 0.3;
            
            if (won) {
                // User wins!
                todayWinners++;
                userWonToday = true;
                localStorage.setItem('today-winners', todayWinners.toString());
                localStorage.setItem('user-won-today', 'true');
                
                // Update UI
                winnerCount.textContent = todayWinners;
                winButton.innerHTML = '<i class="fas fa-check"></i> Вы уже участвовали сегодня';
                winButton.style.background = '#10b981';
                winButton.disabled = true;
                
                // Show win modal
                wonPrizeName.textContent = dailyPrize.title;
                winModalTitle.textContent = 'Поздравляем! 🎉 Вы выиграли!';
                winModal.classList.add('active');
                document.body.style.overflow = 'hidden';
                
                // Create confetti
                createConfetti();
            } else {
                // User loses
                alert('К сожалению, вы не выиграли сегодня. Попробуйте завтра!');
            }
        }

        // Add Prize to Cart and Order
        function addPrizeAndOrder() {
            // Add prize to cart if not already there
            const isPrizeInCart = cart.some(item => item.id === dailyPrize.id);
            if (!isPrizeInCart) {
                cart.push({ id: dailyPrize.id, title: dailyPrize.title });
                saveCart();
                updateCartCount();
                renderCart();
                renderServices();
            }
            
            closeWinModalFunc();
            openOrderModal();
        }

        // Show Single Service Order Modal
        function showSingleOrderModal(serviceTitle) {
            orderModalText.textContent = `Вы хотите заказать услугу: "${serviceTitle}"? Заказ будет отправлен в WhatsApp.`;
            
            // Store the service for ordering
            orderModal.dataset.service = serviceTitle;
            orderModal.dataset.isSingle = 'true';
            
            openOrderModal();
        }

        // WhatsApp Order Functions
        function sendOrderToWhatsApp() {
            const isSingleOrder = orderModal.dataset.isSingle === 'true';
            
            if (isSingleOrder) {
                // Single service order
                const serviceTitle = orderModal.dataset.service;
                const message = `Здравствуйте! Хочу заказать IT-услугу: ${serviceTitle}. Пожалуйста, свяжитесь со мной для обсуждения деталей и стоимости.`;
                sendWhatsAppMessage(message);
            } else {
                // Cart order
                if (cart.length === 0) return;
                
                let message = "Здравствуйте! Хочу заказать следующие IT-услуги:\n\n";
                
                cart.forEach((item, index) => {
                    const service = services.find(s => s.id === item.id);
                    message += `${index + 1}. ${service.title}\n`;
                });
                
                message += `\nВсего услуг: ${cart.length}\n`;
                message += "Пожалуйста, свяжитесь со мной для обсуждения деталей и стоимости.";
                
                sendWhatsAppMessage(message);
                
                // Clear cart after order
                cart = [];
                saveCart();
                updateCartCount();
                renderCart();
                renderServices();
            }
            
            closeOrderModal();
            closeCart();
        }

        function sendWhatsAppMessage(message) {
            const encodedMessage = encodeURIComponent(message);
            const whatsappUrl = `https://wa.me/998999100097?text=${encodedMessage}`;
            window.open(whatsappUrl, '_blank');
        }

        // Confetti Animation
        function createConfetti() {
            const container = document.getElementById('confettiContainer');
            const colors = ['#f59e0b', '#ef4444', '#3b82f6', '#10b981', '#8b5cf6'];
            
            for (let i = 0; i < 150; i++) {
                const confetti = document.createElement('div');
                confetti.className = 'confetti';
                confetti.style.left = Math.random() * 100 + 'vw';
                confetti.style.background = colors[Math.floor(Math.random() * colors.length)];
                confetti.style.transform = `rotate(${Math.random() * 360}deg)`;
                
                const animation = confetti.animate([
                    { 
                        top: '-10px',
                        opacity: 1,
                        transform: `rotate(${Math.random() * 360}deg)`
                    },
                    { 
                        top: '100vh',
                        opacity: 0,
                        transform: `rotate(${Math.random() * 720}deg)`
                    }
                ], {
                    duration: Math.random() * 3000 + 2000,
                    easing: 'cubic-bezier(0.215, 0.610, 0.355, 1)'
                });
                
                container.appendChild(confetti);
                animation.onfinish = () => confetti.remove();
            }
        }

        // Promo Timer
        function updatePromoTimer() {
            const targetDate = new Date('2025-01-05T23:59:59').getTime();
            const now = new Date().getTime();
            const timeLeft = targetDate - now;
            
            if (timeLeft > 0) {
                const days = Math.floor(timeLeft / (1000 * 60 * 60 * 24));
                const hours = Math.floor((timeLeft % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
                promoTimer.textContent = `${days}д ${hours}ч`;
            } else {
                promoTimer.textContent = 'Акция завершена';
            }
        }

        // Update timer every minute
        setInterval(updatePromoTimer, 60000);
    </script>
</body>
</html>

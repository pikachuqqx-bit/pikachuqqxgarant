#pikachuqqxgarant
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Профиль пользователя</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
Сделай намек что кнопки ниже такие как безапасность и отзывы нажимаются
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
            color: #333;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            text-align: center;
            position: relative;
        }
        
        h1 {
            color: white;
            margin-bottom: 30px;
            font-size: 2.5rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }
        
        .profile-card {
            background-color: white;
            border-radius: 16px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            width: 100%;
            max-width: 380px;
            overflow: hidden;
            text-align: center;
            position: relative;
            margin: 0 auto;
        }
        
        .card-header {
            background: linear-gradient(to right, #3498db, #2c3e50);
            padding: 30px 20px;
            color: white;
        }
        
        .username {
            font-size: 22px;
            font-weight: 700;
            margin-bottom: 5px;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.3);
        }
        
        .contact-info {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 15px;
            margin-bottom: 15px;
            flex-wrap: wrap;
        }
        
        .user-email {
            font-size: 14px;
            opacity: 0.9;
            display: flex;
            align-items: center;
            justify-content: center;
            background: rgba(255, 255, 255, 0.15);
            padding: 6px 12px;
            border-radius: 15px;
            backdrop-filter: blur(5px);
        }
        
        .user-email i {
            margin-right: 8px;
            font-size: 12px;
        }
        
        .info-btn {
            background: rgba(255, 255, 255, 0.15);
            color: white;
            padding: 6px 12px;
            border-radius: 15px;
            font-size: 14px;
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 5px;
            transition: all 0.3s ease;
            backdrop-filter: blur(5px);
        }
        
        .info-btn:hover {
            background: rgba(255, 255, 255, 0.25);
            transform: translateY(-2px);
        }
        
        .contact-btn {
            background: rgba(255, 255, 255, 0.2);
            color: white;
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 14px;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            transition: all 0.3s ease;
            margin-bottom: 15px;
            backdrop-filter: blur(5px);
        }
        
        .contact-btn:hover {
            background: rgba(255, 255, 255, 0.3);
            transform: translateY(-2px);
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
        }
        
        .guarantee-badge {
            background-color: rgba(255, 255, 255, 0.2);
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 14px;
            font-weight: 500;
            display: inline-block;
            backdrop-filter: blur(5px);
        }
        
        .card-content {
            padding: 25px;
        }
        
        .location {
            color: #7f8c8d;
            font-size: 15px;
            margin-bottom: 25px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .location i {
            margin-right: 8px;
            color: #e74c3c;
        }
        
        .stats {
            display: flex;
            justify-content: space-around;
            margin-bottom: 25px;
        }
        
        .stat {
            display: flex;
            flex-direction: column;
        }
        
        .stat-value {
            font-size: 28px;
            font-weight: 700;
            color: #2c3e50;
        }
        
        .stat-label {
            font-size: 13px;
            color: #95a5a6;
            margin-top: 5px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }
        
        .divider {
            height: 1px;
            background-color: #ecf0f1;
            margin: 20px 0;
        }
        
        .guarantor-info {
            background-color: #f8f9fa;
            padding: 15px;
            border-radius: 10px;
            color: #2c3e50;
            font-size: 14px;
            line-height: 1.5;
            text-align: left;
        }
        
        .guarantor-title {
            font-weight: 600;
            margin-bottom: 8px;
            color: #3498db;
            text-align: center;
        }
        
        .social-icons {
            display: flex;
            justify-content: center;
            margin-top: 20px;
            gap: 15px;
        }
        
        .telegram-btn, .email-btn {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            transition: all 0.3s ease;
            cursor: pointer;
        }
        
        .telegram-btn {
            background: linear-gradient(135deg, #0088cc, #00aced);
            box-shadow: 0 4px 15px rgba(0, 136, 204, 0.3);
        }
        
        .email-btn {
            background: linear-gradient(135deg, #D44638, #EA4335);
            box-shadow: 0 4px 15px rgba(212, 70, 56, 0.3);
        }
        
        .telegram-btn:hover, .email-btn:hover {
            transform: translateY(-5px) scale(1.1);
            box-shadow: 0 8px 25px rgba(0, 136, 204, 0.5);
        }
        
        .nft-badge {
            position: absolute;
            top: 15px;
            right: 15px;
            background-color: #ff9f43;
            color: white;
            font-size: 12px;
            font-weight: bold;
            padding: 5px 10px;
            border-radius: 20px;
            box-shadow: 0 4px 10px rgba(255, 159, 67, 0.3);
        }
        
        .features {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            margin-top: 40px;
        }
        
        .feature {
            background: white;
            border-radius: 12px;
            padding: 20px;
            width: 250px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
            cursor: pointer;
        }
        
        .feature:hover {
            transform: translateY(-5px);
        }
        
        .feature i {
            font-size: 2rem;
            color: #3498db;
            margin-bottom: 15px;
        }
        
        .feature h3 {
            margin-bottom: 10px;
            color: #2c3e50;
        }
        
        .feature p {
            color: #7f8c8d;
            font-size: 14px;
        }
        
        .footer {
            margin-top: 50px;
            color: white;
            font-size: 14px;
            opacity: 0.8;
        }
        
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }
        
        .modal-content {
            background-color: white;
            padding: 30px;
            border-radius: 16px;
            max-width: 500px;
            width: 90%;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            position: relative;
        }
        
        .close-btn {
            position: absolute;
            top: 15px;
            right: 15px;
            font-size: 24px;
            cursor: pointer;
            color: #7f8c8d;
            transition: color 0.3s ease;
        }
        
        .close-btn:hover {
            color: #e74c3c;
        }
        
        .modal-title {
            color: #2c3e50;
            margin-bottom: 20px;
            text-align: center;
        }
        
        .modal-text {
            color: #34495e;
            line-height: 1.6;
            font-size: 16px;
            text-align: left;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Профиль пользователя</h1>
        
        <div class="profile-card">
            <div class="nft-badge">NFT</div>
            <div class="card-header">
                <h1 class="username">Alexandr</h1>
                <div class="contact-info">
                    <div class="user-email">
                        <i class="far fa-envelope"></i>pikachuqqx@gmail.com
                    </div>
                    <a href="https://t.me/replapika" target="_blank" class="info-btn">
                        <i class="fas fa-info-circle"></i>info
                    </a>
                </div>
                <a href="https://t.me/pikachuqx" target="_blank" class="contact-btn">
                    <i class="fab fa-telegram"></i>Связаться с @pikachuqx
                </a>
                <div class="guarantee-badge">garant 2% | CKYΠΛΙΟ NFT</div>
            </div>
            
            <div class="card-content">
                <div class="location">
                    <i class="fas fa-map-marker-alt"></i>Russia, Moscow
                </div>
                
                <div class="stats">
                    <div class="stat">
                        <div class="stat-value">132</div>
                        <div class="stat-label">Транзакции</div>
                    </div>
                    <div class="stat">
                        <div class="stat-value">98%</div>
                        <div class="stat-label">Рейтинг</div>
                    </div>
                </div>
                
                <div class="divider"></div>
                
                <div class="guarantor-info">
                    <div class="guarantor-title">Что такое гарант?</div>
                    Гарант — это третье лицо, которое берёт на себя ответственность за выполнение обязательств одной из сторон сделки. Гарант выступает в роли посредника, который гарантирует, что обязательства будут выполнены, а средства не утеряны.
                </div>
                
                <div class="social-icons">
                    <a href="https://t.me/pikachuqx" target="_blank" class="telegram-btn">
                        <i class="fab fa-telegram"></i>
                    </a>
                    <a href="mailto:pikachuqqx@gmail.com" class="email-btn">
                        <i class="far fa-envelope"></i>
                    </a>
                </div>
            </div>
        </div>
        
        <div class="features">
            <div class="feature" id="security-feature">
                <i class="fas fa-shield-alt"></i>
                <h3>Безопасность</h3>
                <p>Гарантированная защита всех ваших транзакций и данных</p>
            </div>
            <div class="feature" id="reviews-feature">
                <i class="fas fa-star"></i>
                <h3>Отзывы</h3>
                <p>Посмотрите отзывы наших клиентов о сотрудничестве</p>
            </div>
            <div class="feature">
                <i class="fas fa-globe"></i>
                <h3>Доступность</h3>
                <p>Работаем по всему миру без ограничений</p>
            </div>
        </div>
        
        <div class="footer">
            <p>© 2023 Все права защищены. Данный сайт предназначен только для легальных целей.</p>
        </div>
    </div>

    <!-- Модальное окно для описания гаранта -->
    <div class="modal" id="guarantor-modal">
        <div class="modal-content">
            <span class="close-btn" id="close-modal">&times;</span>
            <h2 class="modal-title">Что такое гарант?</h2>
            <p class="modal-text">
                Гарант — это третье лицо, которое берёт на себя ответственность за выполнение обязательств одной из сторон сделки. 
                Гарант выступает в роли посредника, который гарантирует, что обязательства будут выполнены, а средства не утеряны.
                <br><br>
                В нашем сервисе гарант обеспечивает безопасность сделки, контролируя процесс обмена и возвращая средства в случае 
                возникновения проблем. Это дополнительный уровень защиты для всех участников транзакции.
            </p>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Работа с модальным окном
            const securityFeature = document.getElementById('security-feature');
            const modal = document.getElementById('guarantor-modal');
            const closeModal = document.getElementById('close-modal');
            
            security
            Feature.addEventListener('click', function() {
                modal.style.display = 'flex';
            });
            
            closeModal.addEventListener('click', function() {
                modal.style.display = 'none';
            });
            
            window.addEventListener('click', function(event) {
                if (event.target === modal) {
                    modal.style.display = 'none';
                }
            });

            // Переход на Telegram при клике на Отзывы
            const reviewsFeature = document.getElementById('reviews-feature');
            
            reviewsFeature.addEventListener('click', function() {
                window.open('https://t.me/repapikchahu', '_blank');
            });
        });
    </script>
</body>

</html>

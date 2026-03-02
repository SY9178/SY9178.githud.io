<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>创新科技 | 企业官网</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            line-height: 1.6;
            color: #333;
            background-color: #f9f9f9;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* 导航栏样式 */
        header {
            background-color: #fff;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }
        
        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
        }
        
        .logo {
            font-size: 24px;
            font-weight: 700;
            color: #2563eb;
            text-decoration: none;
        }
        
        .logo span {
            color: #f59e0b;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 30px;
        }
        
        nav ul li a {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: #2563eb;
        }
        
        .mobile-menu-btn {
            display: none;
            font-size: 24px;
            background: none;
            border: none;
            cursor: pointer;
            color: #2563eb;
        }
        
        /* 主视觉区域 */
        .hero {
            background: linear-gradient(135deg, #2563eb 0%, #1d4ed8 100%);
            color: white;
            padding: 150px 0 100px;
            text-align: center;
            margin-top: 70px;
        }
        
        .hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
            line-height: 1.2;
        }
        
        .hero p {
            font-size: 20px;
            max-width: 700px;
            margin: 0 auto 30px;
            opacity: 0.9;
        }
        
        .cta-button {
            display: inline-block;
            background-color: #f59e0b;
            color: white;
            padding: 15px 35px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 18px;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
        }
        
        .cta-button:hover {
            background-color: #d97706;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        /* 特色服务区域 */
        .features {
            padding: 100px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }
        
        .section-title h2 {
            font-size: 36px;
            color: #1e293b;
            margin-bottom: 15px;
        }
        
        .section-title p {
            color: #64748b;
            max-width: 600px;
            margin: 0 auto;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .feature-card {
            background-color: white;
            border-radius: 10px;
            padding: 40px 30px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s;
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
        }
        
        .feature-icon {
            font-size: 48px;
            color: #2563eb;
            margin-bottom: 20px;
        }
        
        .feature-card h3 {
            font-size: 24px;
            margin-bottom: 15px;
            color: #1e293b;
        }
        
        /* 关于我们区域 */
        .about {
            padding: 100px 0;
            background-color: #f1f5f9;
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-text h2 {
            font-size: 36px;
            margin-bottom: 20px;
            color: #1e293b;
        }
        
        .about-image {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .about-image img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        /* 联系表单 */
        .contact {
            padding: 100px 0;
        }
        
        .contact-form {
            max-width: 700px;
            margin: 0 auto;
            background-color: white;
            padding: 50px;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
        }
        
        .form-group {
            margin-bottom: 25px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
            color: #1e293b;
        }
        
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 15px;
            border: 1px solid #cbd5e1;
            border-radius: 5px;
            font-size: 16px;
            transition: border-color 0.3s;
        }
        
        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #2563eb;
        }
        
        /* 页脚 */
        footer {
            background-color: #1e293b;
            color: #cbd5e1;
            padding: 70px 0 30px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 50px;
        }
        
        .footer-column h3 {
            color: white;
            font-size: 20px;
            margin-bottom: 25px;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-column h3:after {
            content: '';
            position: absolute;
            left: 0;
            bottom: 0;
            width: 50px;
            height: 3px;
            background-color: #2563eb;
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 12px;
        }
        
        .footer-links a {
            color: #cbd5e1;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-links a:hover {
            color: #2563eb;
        }
        
        .social-icons {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-icons a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: #334155;
            border-radius: 50%;
            color: white;
            text-decoration: none;
            transition: background-color 0.3s;
        }
        
        .social-icons a:hover {
            background-color: #2563eb;
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid #334155;
            font-size: 14px;
        }
        
        /* 响应式设计 */
        @media (max-width: 992px) {
            .hero h1 {
                font-size: 40px;
            }
            
            .about-content {
                flex-direction: column;
            }
        }
        
        @media (max-width: 768px) {
            .mobile-menu-btn {
                display: block;
            }
            
            nav ul {
                position: fixed;
                top: 70px;
                left: 0;
                width: 100%;
                background-color: white;
                flex-direction: column;
                align-items: center;
                padding: 20px 0;
                box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
                display: none;
            }
            
            nav ul.active {
                display: flex;
            }
            
            nav ul li {
                margin: 15px 0;
            }
            
            .hero h1 {
                font-size: 32px;
            }
            
            .hero p {
                font-size: 18px;
            }
            
            .contact-form {
                padding: 30px;
            }
        }
    </style>
</head>
<body>
    <!-- 导航栏 -->
    <header>
        <div class="container nav-container">
            <a href="#" class="logo">创新<span>科技</span></a>
            
            <button class="mobile-menu-btn" id="mobileMenuBtn">
                <i class="fas fa-bars"></i>
            </button>
            
            <nav>
                <ul id="navMenu">
                    <li><a href="#home">首页</a></li>
                    <li><a href="#about">关于我们</a></li>
                    <li><a href="#services">服务项目</a></li>
                    <li><a href="#contact">联系我们</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- 主视觉区域 -->
    <section class="hero" id="home">
        <div class="container">
            <h1>创新驱动未来，科技改变生活</h1>
            <p>我们是一家专注于前沿技术研发与应用的科技公司，致力于为客户提供最优质的数字化解决方案，助力企业实现数字化转型与升级。</p>
            <a href="#contact" class="cta-button">立即咨询</a>
        </div>
    </section>

    <!-- 特色服务区域 -->
    <section class="features" id="services">
        <div class="container">
            <div class="section-title">
                <h2>我们的核心服务</h2>
                <p>我们提供全方位的数字化解决方案，从咨询到实施，全程为您保驾护航</p>
            </div>
            
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-laptop-code"></i>
                    </div>
                    <h3>定制软件开发</h3>
                    <p>根据您的业务需求，量身打造高性能、可扩展的软件系统，提升工作效率。</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-mobile-alt"></i>
                    </div>
                    <h3>移动应用开发</h3>
                    <p>开发iOS和Android平台的原生应用与跨平台应用，打造卓越的用户体验。</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-cloud"></i>
                    </div>
                    <h3>云解决方案</h3>
                    <p>提供全面的云端部署、迁移与管理服务，确保您的业务高效稳定运行。</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <h3>数据分析</h3>
                    <p>通过先进的数据分析技术，帮助您从海量数据中提取有价值的信息，指导决策。</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 关于我们区域 -->
    <section class="about" id="about">
        <div class="container">
            <div class="about-content">
                <div class="about-text">
                    <h2>关于创新科技</h2>
                    <p>我们成立于2015年，是一家专注于前沿技术研发与应用的科技公司。我们拥有一支由资深工程师、设计师和产品经理组成的专业团队，致力于为客户提供最优质的数字化解决方案。</p>
                    <p>我们的使命是通过技术创新帮助企业提升竞争力，实现数字化转型。我们已成功为超过200家企业提供了专业的科技服务，涵盖金融、教育、医疗、零售等多个行业。</p>
                    <p>我们始终坚持以客户为中心，以技术为驱动，以创新为灵魂，持续为客户创造价值，共同成长。</p>
                    <a href="#contact" class="cta-button" style="margin-top: 20px;">了解更多</a>
                </div>
                
                <div class="about-image">
                    <!-- 占位图片，实际使用时应替换为真实图片 -->
                    <div style="width:100%; height:400px; background:linear-gradient(135deg, #2563eb 0%, #1d4ed8 100%); display:flex; align-items:center; justify-content:center; color:white; font-size:24px;">
                        <div style="text-align:center;">
                            <i class="fas fa-users" style="font-size:60px; margin-bottom:15px;"></i>
                            <p>我们的团队</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 联系表单 -->
    <section class="contact" id="contact">
        <div class="container">
            <div class="section-title">
                <h2>联系我们</h2>
                <p>如果您有任何问题或合作意向，请随时联系我们，我们将尽快回复您</p>
            </div>
            
            <div class="contact-form">
                <form id="contactForm">
                    <div class="form-group">
                        <label for="name">姓名</label>
                        <input type="text" id="name" name="name" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="email">邮箱</label>
                        <input type="email" id="email" name="email" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="phone">电话</label>
                        <input type="tel" id="phone" name="phone">
                    </div>
                    
                    <div class="form-group">
                        <label for="message">留言内容</label>
                        <textarea id="message" name="message" rows="5" required></textarea>
                    </div>
                    
                    <button type="submit" class="cta-button">发送消息</button>
                </form>
            </div>
        </div>
    </section>

    <!-- 页脚 -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>创新科技</h3>
                    <p>我们是一家专注于前沿技术研发与应用的科技公司，致力于为客户提供最优质的数字化解决方案。</p>
                    <div class="social-icons">
                        <a href="#"><i class="fab fa-weixin"></i></a>
                        <a href="#"><i class="fab fa-weibo"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                        <a href="#"><i class="fab fa-github"></i></a>
                    </div>
                </div>
                
                <div class="footer-column">
                    <h3>快速链接</h3>
                    <ul class="footer-links">
                        <li><a href="#home">首页</a></li>
                        <li><a href="#about">关于我们</a></li>
                        <li><a href="#services">服务项目</a></li>
                        <li><a href="#contact">联系我们</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>服务项目</h3>
                    <ul class="footer-links">
                        <li><a href="#">定制软件开发</a></li>
                        <li><a href="#">移动应用开发</a></li>
                        <li><a href="#">云解决方案</a></li>
                        <li><a href="#">数据分析</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>联系我们</h3>
                    <ul class="footer-links">
                        <li><i class="fas fa-map-marker-alt"></i> 北京市朝阳区科技园A座12层</li>
                        <li><i class="fas fa-phone"></i> 400-123-4567</li>
                        <li><i class="fas fa-envelope"></i> info@innovationtech.com</li>
                        <li><i class="fas fa-clock"></i> 周一至周五 9:00-18:00</li>
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2026 创新科技有限公司 版权所有 | 京ICP备12345678号</p>
            </div>
        </div>
    </footer>

    <script>
        // 移动端菜单切换
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const navMenu = document.getElementById('navMenu');
        
        mobileMenuBtn.addEventListener('click', function() {
            navMenu.classList.toggle('active');
            mobileMenuBtn.innerHTML = navMenu.classList.contains('active') 
                ? '<i class="fas fa-times"></i>' 
                : '<i class="fas fa-bars"></i>';
        });
        
        // 点击菜单链接后关闭移动菜单
        const navLinks = document.querySelectorAll('nav a');
        navLinks.forEach(link => {
            link.addEventListener('click', function() {
                navMenu.classList.remove('active');
                mobileMenuBtn.innerHTML = '<i class="fas fa-bars"></i>';
            });
        });
        
        // 表单提交处理
        const contactForm = document.getElementById('contactForm');
        contactForm.addEventListener('submit', function(e) {
            e.preventDefault();
            
            // 在实际应用中，这里应该将表单数据发送到服务器
            // 这里只是一个简单的演示
            alert('感谢您的留言！我们会尽快与您联系。');
            contactForm.reset();
        });
        
        // 平滑滚动到锚点
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 70,
                        behavior: 'smooth'
                    });
                }
            });
        });
    </script>
</body>
</html>

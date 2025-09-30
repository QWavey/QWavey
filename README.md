<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>QWavey's GitHub Profile</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Segoe+UI:wght@300;400;500;600;700&display=swap');
        @import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 50%, #0f3460 100%);
            color: #fff;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }
        
        .profile-container {
            max-width: 1200px;
            width: 100%;
            margin: 40px auto;
            padding: 40px;
            border-radius: 25px;
            background: linear-gradient(135deg, #ff6a00, #ee0979);
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.6);
            position: relative;
            overflow: hidden;
            z-index: 1;
        }
        
        .profile-container::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" width="100" height="100" opacity="0.1"><defs><pattern id="grain" width="100" height="100" patternUnits="userSpaceOnUse"><circle cx="50" cy="50" r="1" fill="white"/></pattern></defs><rect width="100" height="100" fill="url(%23grain)"/></svg>');
            z-index: -1;
        }
        
        .profile-header {
            text-align: center;
            margin-bottom: 40px;
            position: relative;
            animation: fadeInDown 1s ease-out;
        }
        
        .profile-header h1 {
            font-size: 3.5em;
            margin-bottom: 10px;
            text-shadow: 3px 3px 5px rgba(0, 0, 0, 0.3);
            letter-spacing: 1px;
        }
        
        .profile-header p {
            font-size: 1.3em;
            opacity: 0.9;
            max-width: 600px;
            margin: 0 auto;
        }
        
        .stats-container {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
            margin-bottom: 40px;
        }
        
        .stat-card {
            background: rgba(255, 255, 255, 0.15);
            border-radius: 20px;
            padding: 25px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            animation: fadeInUp 1s ease-out;
            flex: 1;
            min-width: 300px;
            max-width: 400px;
        }
        
        .stat-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
            background: rgba(255, 255, 255, 0.2);
        }
        
        .stat-card img {
            border-radius: 15px;
            max-width: 100%;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            transition: transform 0.5s ease;
        }
        
        .stat-card:hover img {
            transform: scale(1.03);
        }
        
        .languages-section {
            margin-top: 50px;
            text-align: center;
            animation: fadeIn 1.5s ease-out;
        }
        
        .languages-section h2 {
            font-size: 2.5em;
            margin-bottom: 30px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }
        
        .languages-container {
            display: flex;
            justify-content: center;
            gap: 40px;
            flex-wrap: wrap;
            margin-top: 30px;
        }
        
        .language-item {
            text-align: center;
            transition: all 0.3s ease;
            position: relative;
            padding: 20px;
            border-radius: 15px;
            background: rgba(255, 255, 255, 0.1);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            min-width: 140px;
            backdrop-filter: blur(5px);
        }
        
        .language-item:hover {
            transform: translateY(-10px) scale(1.05);
            background: rgba(255, 255, 255, 0.2);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
        }
        
        .language-icon {
            font-size: 60px;
            margin-bottom: 15px;
            display: block;
            transition: all 0.3s ease;
        }
        
        .language-item:hover .language-icon {
            transform: rotate(15deg) scale(1.2);
        }
        
        .language-name {
            font-size: 1.3em;
            font-weight: 600;
            display: block;
        }
        
        .language-stats {
            margin-top: 10px;
            height: 8px;
            background: rgba(255, 255, 255, 0.2);
            border-radius: 4px;
            overflow: hidden;
            position: relative;
        }
        
        .language-bar {
            height: 100%;
            border-radius: 4px;
            position: absolute;
            left: 0;
            top: 0;
            animation: fillBar 2s ease-out forwards;
        }
        
        .python-bar {
            width: 85%;
            background: linear-gradient(90deg, #3776ab, #4b8bbe);
        }
        
        .javascript-bar {
            width: 75%;
            background: linear-gradient(90deg, #f7df1e, #f0db4f);
        }
        
        .go-bar {
            width: 60%;
            background: linear-gradient(90deg, #00add8, #7fd5ea);
        }
        
        .buttons-container {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 50px;
            flex-wrap: wrap;
        }
        
        .profile-button {
            padding: 15px 30px;
            border-radius: 50px;
            background: rgba(255, 255, 255, 0.2);
            color: white;
            border: none;
            font-size: 1.1em;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            backdrop-filter: blur(5px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .profile-button:hover {
            background: rgba(255, 255, 255, 0.3);
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
        }
        
        .profile-button:active {
            transform: translateY(0);
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 40px;
        }
        
        .social-link {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.15);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5em;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            text-decoration: none;
        }
        
        .social-link:hover {
            transform: translateY(-5px) rotate(10deg);
            background: rgba(255, 255, 255, 0.25);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
        }
        
        .floating-elements {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            overflow: hidden;
            z-index: -1;
        }
        
        .floating-element {
            position: absolute;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            animation: float 15s infinite ease-in-out;
        }
        
        .floating-element:nth-child(1) {
            width: 80px;
            height: 80px;
            top: 10%;
            left: 5%;
            animation-delay: 0s;
        }
        
        .floating-element:nth-child(2) {
            width: 120px;
            height: 120px;
            top: 70%;
            left: 80%;
            animation-delay: -5s;
        }
        
        .floating-element:nth-child(3) {
            width: 60px;
            height: 60px;
            top: 20%;
            left: 85%;
            animation-delay: -10s;
        }
        
        .floating-element:nth-child(4) {
            width: 100px;
            height: 100px;
            top: 80%;
            left: 10%;
            animation-delay: -7s;
        }
        
        .pulse-animation {
            animation: pulse 2s infinite;
        }
        
        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }
        
        @keyframes float {
            0%, 100% {
                transform: translateY(0) rotate(0deg);
            }
            33% {
                transform: translateY(-20px) rotate(120deg);
            }
            66% {
                transform: translateY(10px) rotate(240deg);
            }
        }
        
        @keyframes fillBar {
            from {
                width: 0%;
            }
        }
        
        @keyframes pulse {
            0% {
                box-shadow: 0 0 0 0 rgba(255, 255, 255, 0.4);
            }
            70% {
                box-shadow: 0 0 0 15px rgba(255, 255, 255, 0);
            }
            100% {
                box-shadow: 0 0 0 0 rgba(255, 255, 255, 0);
            }
        }
        
        .achievement-badge {
            display: inline-block;
            background: rgba(255, 255, 255, 0.2);
            padding: 8px 15px;
            border-radius: 20px;
            margin: 5px;
            font-size: 0.9em;
            animation: fadeIn 1s ease-out;
            backdrop-filter: blur(5px);
        }
        
        .badge-container {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            margin-top: 20px;
            gap: 10px;
        }
        
        .section-divider {
            height: 3px;
            background: rgba(255, 255, 255, 0.3);
            margin: 40px 0;
            border-radius: 3px;
            position: relative;
            overflow: hidden;
        }
        
        .section-divider::after {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.6), transparent);
            animation: shimmer 3s infinite;
        }
        
        @keyframes shimmer {
            0% {
                left: -100%;
            }
            100% {
                left: 100%;
            }
        }
        
        .highlight-text {
            background: linear-gradient(90deg, #ff8a00, #e52e71);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            font-weight: 700;
        }
        
        @media (max-width: 768px) {
            .profile-container {
                padding: 25px;
            }
            
            .profile-header h1 {
                font-size: 2.5em;
            }
            
            .stats-container {
                flex-direction: column;
                align-items: center;
            }
            
            .stat-card {
                min-width: 100%;
            }
            
            .languages-container {
                gap: 20px;
            }
            
            .language-item {
                min-width: 120px;
            }
        }
    </style>
</head>
<body>
    <div class="profile-container">
        <div class="floating-elements">
            <div class="floating-element"></div>
            <div class="floating-element"></div>
            <div class="floating-element"></div>
            <div class="floating-element"></div>
        </div>
        
        <div class="profile-header">
            <h1>QWavey's <span class="highlight-text">GitHub</span> Profile</h1>
            <p>Passionate developer creating innovative solutions with code</p>
            
            <div class="badge-container">
                <div class="achievement-badge pulse-animation">🚀 Active Developer</div>
                <div class="achievement-badge">⭐ GitHub Star</div>
                <div class="achievement-badge">🔧 Open Source Contributor</div>
                <div class="achievement-badge">💻 Code Enthusiast</div>
            </div>
        </div>
        
        <div class="stats-container">
            <div class="stat-card">
                <img src="https://github-readme-stats.vercel.app/api?username=QWavey&show_icons=true&theme=radical&hide_border=true&include_all_commits=true&count_private=true" alt="GitHub Stats">
            </div>
            <div class="stat-card">
                <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=QWavey&layout=compact&theme=radical&hide_border=true&langs_count=8" alt="Top Languages">
            </div>
        </div>
        
        <div class="section-divider"></div>
        
        <div class="languages-section">
            <h2>Most Used <span class="highlight-text">Languages</span></h2>
            
            <div class="languages-container">
                <div class="language-item">
                    <span class="language-icon">🐍</span>
                    <span class="language-name">Python</span>
                    <div class="language-stats">
                        <div class="language-bar python-bar"></div>
                    </div>
                    <div style="margin-top: 8px; font-size: 0.9em;">85%</div>
                </div>
                
                <div class="language-item">
                    <span class="language-icon">🌐</span>
                    <span class="language-name">JavaScript</span>
                    <div class="language-stats">
                        <div class="language-bar javascript-bar"></div>
                    </div>
                    <div style="margin-top: 8px; font-size: 0.9em;">75%</div>
                </div>
                
                <div class="language-item">
                    <span class="language-icon">⚙️</span>
                    <span class="language-name">Go</span>
                    <div class="language-stats">
                        <div class="language-bar go-bar"></div>
                    </div>
                    <div style="margin-top: 8px; font-size: 0.9em;">60%</div>
                </div>
            </div>
        </div>
        
        <div class="buttons-container">
            <button class="profile-button">
                <i class="fas fa-code"></i> View Projects
            </button>
            <button class="profile-button">
                <i class="fas fa-star"></i> Star Repositories
            </button>
            <button class="profile-button">
                <i class="fas fa-download"></i> Download Resume
            </button>
            <button class="profile-button">
                <i class="fas fa-envelope"></i> Contact Me
            </button>
        </div>
        
        <div class="social-links">
            <a href="#" class="social-link">
                <i class="fab fa-github"></i>
            </a>
            <a href="#" class="social-link">
                <i class="fab fa-linkedin"></i>
            </a>
            <a href="#" class="social-link">
                <i class="fab fa-twitter"></i>
            </a>
            <a href="#" class="social-link">
                <i class="fab fa-dev"></i>
            </a>
            <a href="#" class="social-link">
                <i class="fas fa-globe"></i>
            </a>
        </div>
    </div>

    <script>
        // Add interactive functionality to buttons
        document.addEventListener('DOMContentLoaded', function() {
            const buttons = document.querySelectorAll('.profile-button');
            
            buttons.forEach(button => {
                button.addEventListener('click', function() {
                    // Add ripple effect
                    const ripple = document.createElement('span');
                    const rect = this.getBoundingClientRect();
                    const size = Math.max(rect.width, rect.height);
                    const x = event.clientX - rect.left - size / 2;
                    const y = event.clientY - rect.top - size / 2;
                    
                    ripple.style.width = ripple.style.height = size + 'px';
                    ripple.style.left = x + 'px';
                    ripple.style.top = y + 'px';
                    ripple.classList.add('ripple');
                    
                    this.appendChild(ripple);
                    
                    setTimeout(() => {
                        ripple.remove();
                    }, 600);
                });
            });
            
            // Add animation to stat cards on scroll
            const statCards = document.querySelectorAll('.stat-card');
            const observerOptions = {
                threshold: 0.1,
                rootMargin: '0px 0px -50px 0px'
            };
            
            const observer = new IntersectionObserver(function(entries) {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.animation = 'fadeInUp 0.8s ease-out forwards';
                        observer.unobserve(entry.target);
                    }
                });
            }, observerOptions);
            
            statCards.forEach(card => {
                observer.observe(card);
            });
            
            // Add typing effect to header
            const headerText = "QWavey's GitHub Profile";
            const headerElement = document.querySelector('.profile-header h1');
            let i = 0;
            
            function typeWriter() {
                if (i < headerText.length) {
                    headerElement.innerHTML = headerText.substring(0, i+1) + '<span class="highlight-text">' + headerText.substring(i+1) + '</span>';
                    i++;
                    setTimeout(typeWriter, 100);
                }
            }
            
            // Start typing effect after a delay
            setTimeout(typeWriter, 1000);
        });
        
        // Add ripple effect styles dynamically
        const style = document.createElement('style');
        style.textContent = `
            .ripple {
                position: absolute;
                border-radius: 50%;
                background: rgba(255, 255, 255, 0.6);
                transform: scale(0);
                animation: ripple-animation 0.6s linear;
            }
            
            @keyframes ripple-animation {
                to {
                    transform: scale(4);
                    opacity: 0;
                }
            }
        `;
        document.head.appendChild(style);
    </script>
</body>
</html>

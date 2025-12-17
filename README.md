<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Himesh Raghuwanshi - GitHub Profile</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #0d1117 0%, #1a1f2e 100%);
            color: #c9d1d9;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Header Section */
        .header {
            text-align: center;
            padding: 60px 20px;
            background: linear-gradient(135deg, #1a1f2e 0%, #0d1117 100%);
            border-radius: 20px;
            margin-bottom: 40px;
            box-shadow: 0 10px 30px rgba(0, 217, 255, 0.1);
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(0, 217, 255, 0.1) 0%, transparent 70%);
            animation: rotate 20s linear infinite;
        }

        @keyframes rotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .header-content {
            position: relative;
            z-index: 1;
        }

        .wave {
            display: inline-block;
            animation: wave-animation 2.5s infinite;
            transform-origin: 70% 70%;
        }

        @keyframes wave-animation {
            0%, 100% { transform: rotate(0deg); }
            10%, 30% { transform: rotate(14deg); }
            20% { transform: rotate(-8deg); }
            40% { transform: rotate(-4deg); }
            50% { transform: rotate(10deg); }
        }

        h1 {
            font-size: 3em;
            color: #00D9FF;
            margin: 20px 0;
            text-shadow: 0 0 20px rgba(0, 217, 255, 0.5);
        }

        .typing-text {
            font-size: 1.5em;
            color: #58a6ff;
            margin: 20px 0;
            min-height: 60px;
        }

        .profile-stats {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
            flex-wrap: wrap;
        }

        .stat-badge {
            background: rgba(0, 217, 255, 0.1);
            padding: 10px 20px;
            border-radius: 10px;
            border: 2px solid #00D9FF;
            font-weight: bold;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .stat-badge:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 217, 255, 0.3);
        }

        /* About Section */
        .about-section {
            background: rgba(255, 255, 255, 0.05);
            padding: 40px;
            border-radius: 20px;
            margin-bottom: 40px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(0, 217, 255, 0.2);
        }

        .code-block {
            background: #0d1117;
            padding: 30px;
            border-radius: 15px;
            font-family: 'Courier New', monospace;
            font-size: 0.95em;
            line-height: 1.8;
            border-left: 4px solid #00D9FF;
            overflow-x: auto;
        }

        .keyword { color: #ff7b72; }
        .function { color: #d2a8ff; }
        .string { color: #a5d6ff; }
        .comment { color: #8b949e; }

        /* Stats Grid */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }

        .stat-card {
            background: linear-gradient(135deg, #1a1f2e 0%, #0d1117 100%);
            padding: 30px;
            border-radius: 15px;
            text-align: center;
            border: 2px solid rgba(0, 217, 255, 0.3);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .stat-card::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(0, 217, 255, 0.1) 0%, transparent 70%);
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .stat-card:hover::before {
            opacity: 1;
        }

        .stat-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 217, 255, 0.3);
            border-color: #00D9FF;
        }

        .stat-number {
            font-size: 3em;
            color: #00D9FF;
            font-weight: bold;
            text-shadow: 0 0 20px rgba(0, 217, 255, 0.5);
        }

        /* Tech Stack */
        .tech-section {
            margin-bottom: 40px;
        }

        .section-title {
            font-size: 2.5em;
            text-align: center;
            margin: 40px 0;
            color: #00D9FF;
            text-shadow: 0 0 20px rgba(0, 217, 255, 0.5);
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }

        .tech-card {
            background: rgba(255, 255, 255, 0.05);
            padding: 25px;
            border-radius: 15px;
            text-align: center;
            transition: all 0.3s ease;
            border: 2px solid transparent;
            cursor: pointer;
        }

        .tech-card:hover {
            transform: translateY(-10px) rotateY(10deg);
            border-color: #00D9FF;
            box-shadow: 0 15px 30px rgba(0, 217, 255, 0.3);
            background: rgba(0, 217, 255, 0.1);
        }

        .tech-icon {
            font-size: 3em;
            margin-bottom: 10px;
            animation: float 3s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        /* Achievements */
        .achievements-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }

        .achievement-card {
            background: linear-gradient(135deg, rgba(255, 215, 0, 0.1) 0%, rgba(0, 217, 255, 0.1) 100%);
            padding: 30px;
            border-radius: 15px;
            border: 2px solid rgba(255, 215, 0, 0.3);
            transition: all 0.3s ease;
            position: relative;
        }

        .achievement-card:hover {
            transform: scale(1.05);
            box-shadow: 0 15px 30px rgba(255, 215, 0, 0.3);
        }

        .trophy-icon {
            font-size: 3em;
            margin-bottom: 15px;
        }

        /* Contact Section */
        .contact-section {
            text-align: center;
            padding: 60px 20px;
            background: linear-gradient(135deg, #1a1f2e 0%, #0d1117 100%);
            border-radius: 20px;
            margin-bottom: 40px;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            margin-top: 30px;
        }

        .social-btn {
            padding: 15px 30px;
            background: rgba(0, 217, 255, 0.1);
            border: 2px solid #00D9FF;
            border-radius: 10px;
            color: #00D9FF;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s ease;
            display: inline-block;
        }

        .social-btn:hover {
            background: #00D9FF;
            color: #0d1117;
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 217, 255, 0.4);
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 40px 20px;
            background: rgba(0, 0, 0, 0.3);
            border-top: 2px solid rgba(0, 217, 255, 0.2);
        }

        .footer-wave {
            width: 100%;
            height: 100px;
            background: linear-gradient(90deg, #00D9FF, #58a6ff, #00D9FF);
            margin-top: 40px;
            animation: wave-motion 3s ease-in-out infinite;
        }

        @keyframes wave-motion {
            0%, 100% { transform: scaleY(1); }
            50% { transform: scaleY(0.5); }
        }

        /* 3D Cube Animation */
        .cube-container {
            perspective: 1000px;
            margin: 40px auto;
            width: 200px;
            height: 200px;
        }

        .cube {
            width: 100%;
            height: 100%;
            position: relative;
            transform-style: preserve-3d;
            animation: rotateCube 10s infinite linear;
        }

        @keyframes rotateCube {
            0% { transform: rotateX(0deg) rotateY(0deg); }
            100% { transform: rotateX(360deg) rotateY(360deg); }
        }

        .cube-face {
            position: absolute;
            width: 200px;
            height: 200px;
            background: rgba(0, 217, 255, 0.2);
            border: 2px solid #00D9FF;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2em;
            font-weight: bold;
        }

        .cube-face:nth-child(1) { transform: rotateY(0deg) translateZ(100px); }
        .cube-face:nth-child(2) { transform: rotateY(90deg) translateZ(100px); }
        .cube-face:nth-child(3) { transform: rotateY(180deg) translateZ(100px); }
        .cube-face:nth-child(4) { transform: rotateY(-90deg) translateZ(100px); }
        .cube-face:nth-child(5) { transform: rotateX(90deg) translateZ(100px); }
        .cube-face:nth-child(6) { transform: rotateX(-90deg) translateZ(100px); }

        @media (max-width: 768px) {
            h1 { font-size: 2em; }
            .typing-text { font-size: 1.2em; }
            .stats-grid { grid-template-columns: 1fr; }
            .tech-grid { grid-template-columns: repeat(auto-fit, minmax(100px, 1fr)); }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <div class="header">
            <div class="header-content">
                <span class="wave">👋</span>
                <h1>Hey there, I'm Himesh Shailendra Raghuwanshi!</h1>
                <div class="typing-text" id="typingText"></div>
                <div class="profile-stats">
                    <div class="stat-badge">👥 3000+ LinkedIn Connections</div>
                    <div class="stat-badge">🏆 8x Winner/Runner-up</div>
                    <div class="stat-badge">🎖️ Rank 8 IIT Madras</div>
                </div>
            </div>
        </div>

        <!-- 3D Cube -->
        <div class="cube-container">
            <div class="cube">
                <div class="cube-face">AI</div>
                <div class="cube-face">ML</div>
                <div class="cube-face">WEB</div>
                <div class="cube-face">DATA</div>
                <div class="cube-face">CODE</div>
                <div class="cube-face">TECH</div>
            </div>
        </div>

        <!-- About Section -->
        <div class="about-section">
            <h2 class="section-title">👨‍💻 About Me</h2>
            <div class="code-block">
<span class="keyword">class</span> <span class="function">HimeshRaghuwanshi</span>:
    <span class="keyword">def</span> <span class="function">__init__</span>(self):
        self.username = <span class="string">"himeshraghuwanshi"</span>
        self.name = <span class="string">"Himesh Shailendra Raghuwanshi"</span>
        self.role = <span class="string">"Computer Engineering Student"</span>
        self.location = <span class="string">"Maharashtra, India 📍"</span>
        self.passions = [<span class="string">"AI/ML"</span>, <span class="string">"Data Science"</span>, <span class="string">"Web Development"</span>]
        
    <span class="keyword">def</span> <span class="function">get_achievements</span>(self):
        <span class="keyword">return</span> {
            <span class="string">"🏆 Hackathons"</span>: <span class="string">"6x Winner/Runner-up"</span>,
            <span class="string">"🎓 Top 50"</span>: <span class="string">"IIT Bombay NEC 2024"</span>,
            <span class="string">"🥈 2nd Place"</span>: <span class="string">"Avinya Competition"</span>,
            <span class="string">"🌟 Finalist"</span>: <span class="string">"IIT Jodhpur, NMIMS"</span>
        }
    
    <span class="keyword">def</span> <span class="function">current_focus</span>(self):
        <span class="keyword">return</span> [
            <span class="string">"Building AI-powered solutions 🤖"</span>,
            <span class="string">"Exploring Deep Learning 🧠"</span>,
            <span class="string">"Creating impactful projects 💡"</span>,
            <span class="string">"Contributing to open source 🌟"</span>
        ]
            </div>
        </div>

        <!-- Quick Stats -->
        <h2 class="section-title">🎯 Quick Stats</h2>
        <div class="stats-grid">
            <div class="stat-card">
                <div class="stat-number" id="commits">1000+</div>
                <p>Total Commits</p>
            </div>
            <div class="stat-card">
                <div class="stat-number" id="projects">25+</div>
                <p>Projects Completed</p>
            </div>
            <div class="stat-card">
                <div class="stat-number" id="streak">150+</div>
                <p>Day Streak</p>
            </div>
            <div class="stat-card">
                <div class="stat-number" id="contributions">2500+</div>
                <p>Contributions</p>
            </div>
        </div>

        <!-- Tech Stack -->
        <div class="tech-section">
            <h2 class="section-title">🛠️ Tech Arsenal</h2>
            <h3 style="text-align: center; color: #58a6ff; margin: 30px 0;">🤖 AI & Data Science</h3>
            <div class="tech-grid">
                <div class="tech-card">
                    <div class="tech-icon">🐍</div>
                    <p>Python</p>
                </div>
                <div class="tech-card">
                    <div class="tech-icon">📊</div>
                    <p>NumPy</p>
                </div>
                <div class="tech-card">
                    <div class="tech-icon">🐼</div>
                    <p>Pandas</p>
                </div>
                <div class="tech-card">
                    <div class="tech-icon">📈</div>
                    <p>Matplotlib</p>
                </div>
                <div class="tech-card">
                    <div class="tech-icon">🌊</div>
                    <p>Seaborn</p>
                </div>
                <div class="tech-card">
                    <div class="tech-icon">👁️</div>
                    <p>OpenCV</p>
                </div>
                <div class="tech-card">
                    <div class="tech-icon">🎯</div>
                    <p>MediaPipe</p>
                </div>
                <div class="tech-card">
                    <div class="tech-icon">📉</div>
                    <p>Power BI</p>
                </div>
            </div>

            <h3 style="text-align: center; color: #58a6ff; margin: 30px 0;">💻 Web Development</h3>
            <div class="tech-grid">
                <div class="tech-card">
                    <div class="tech-icon">⚛️</div>
                    <p>React.js</p>
                </div>
                <div class="tech-card">
                    <div class="tech-icon">📜</div>
                    <p>JavaScript</p>
                </div>
                <div class="tech-card">
                    <div class="tech-icon">🎨</div>
                    <p>HTML/CSS</p>
                </div>
                <div class="tech-card">
                    <div class="tech-icon">🟢</div>
                    <p>Node.js</p>
                </div>
                <div class="tech-card">
                    <div class="tech-icon">🎨</div>
                    <p>Figma</p>
                </div>
                <div class="tech-card">
                    <div class="tech-icon">🗄️</div>
                    <p>SQL/MySQL</p>
                </div>
            </div>
        </div>

        <!-- Achievements -->
        <h2 class="section-title">🏆 Achievements & Milestones</h2>
        <div class="achievements-grid">
            <div class="achievement-card">
                <div class="trophy-icon">🎖️</div>
                <h3>IIT Madras Project Horizon</h3>
                <p>Rank 8 - National Level Competition</p>
            </div>
            <div class="achievement-card">
                <div class="trophy-icon">🥈</div>
                <h3>Avishkar Competition</h3>
                <p>2nd Place & Qualified for University Level</p>
            </div>
            <div class="achievement-card">
                <div class="trophy-icon">🏆</div>
                <h3>IIT Jodhpur</h3>
                <p>Finalist in AI/Tech Innovation Competition</p>
            </div>
            <div class="achievement-card">
                <div class="trophy-icon">🥈</div>
                <h3>Avinya Competition</h3>
                <p>2nd Place - MES Garware Commerce College</p>
            </div>
            <div class="achievement-card">
                <div class="trophy-icon">⭐</div>
                <h3>IIT Bombay NEC</h3>
                <p>Top 50 - National Entrepreneurship Challenge 2024</p>
            </div>
            <div class="achievement-card">
                <div class="trophy-icon">🎯</div>
                <h3>NMIMS Mumbai</h3>
                <p>Finalist in Innovation Competition</p>
            </div>
            <div class="achievement-card">
                <div class="trophy-icon">💼</div>
                <h3>Octanet Internship</h3>
                <p>1-Month Web Development Internship</p>
            </div>
            <div class="achievement-card">
                <div class="trophy-icon">👑</div>
                <h3>Leadership Roles</h3>
                <p>Vice President - ABVP & BroCode</p>
            </div>
        </div>

        <!-- Contact Section -->
        <div class="contact-section">
            <h2 class="section-title">🌐 Connect With Me</h2>
            <p style="font-size: 1.2em; margin: 20px 0;">Let's collaborate and innovate together! 🚀</p>
            <div class="social-links">
                <a href="#" class="social-btn">💼 LinkedIn</a>
                <a href="#" class="social-btn">🐦 Twitter</a>
                <a href="#" class="social-btn">📧 Email</a>
                <a href="#" class="social-btn">🌐 Portfolio</a>
                <a href="#" class="social-btn">📸 Instagram</a>
                <a href="#" class="social-btn">💻 GitHub</a>
            </div>
        </div>

        <!-- Footer -->
        <footer>
            <h3 style="color: #00D9FF; margin-bottom: 20px;">💙 Thanks for visiting!</h3>
            <p style="font-style: italic; font-size: 1.1em;">"Building the future, one commit at a time." 🚀</p>
            <p style="margin-top: 20px;">© 2024 Himesh Raghuwanshi | Made with ❤️ and Code</p>
            <div class="footer-wave"></div>
        </footer>
    </div>

    <script>
        // Typing Animation
        const texts = [
            "AI & Data Science Enthusiast 🚀",
            "Full Stack Web Developer 💻",
            "6x Hackathon Winner 🏆",
            "Building the Future with AI ✨"
        ];
        let textIndex = 0;
        let charIndex = 0;
        let isDeleting = false;
        const typingSpeed = 100;
        const deletingSpeed = 50;
        const pauseTime = 2000;

        function type() {
            const currentText = texts[textIndex];
            const typingElement = document.getElementById('typingText');

            if (!isDeleting) {
                typingElement.textContent = currentText.substring(0, charIndex + 1);
                charIndex++;

                if (charIndex === currentText.length) {
                    isDeleting = true;
                    setTimeout(type, pauseTime);
                    return;
                }
            } else {
                typingElement.textContent = currentText.substring(0, charIndex - 1);
                charIndex--;

                if (charIndex === 0) {
                    isDeleting = false;
                    textIndex = (textIndex + 1) % texts.length;
                }
            }

            setTimeout(type, isDeleting ? deletingSpeed : typingSpeed);
        }

        // Profile View Counter - REMOVED
        // function updateViewCount() {
        //     let views = localStorage.getItem('profileViews') || 0;
        //     views = parseInt(views) + 1;
        //     localStorage.setItem('profileViews', views);
        //     document.getElementById('viewCount').textContent = views;
        // }

        // Animate numbers
        function animateNumber(element, target) {
            let current = 0;
            const increment = target / 50;
            const timer = setInterval(() => {
                current += increment;
                if (current >= target) {
                    element.textContent = target + '+';
                    clearInterval(timer);
                } else {
                    element.textContent = Math.floor(current) + '+';
                }
            }, 30);
        }

        // Initialize on page load
        window.addEventListener('load', () => {
            type();
            
            // Animate stat numbers
            animateNumber(document.getElementById('commits'), 1000);
            animateNumber(document.getElementById('projects'), 25);
            animateNumber(document.getElementById('streak'), 150);
            animateNumber(document.getElementById('contributions'), 2500);
        });

        // Add parallax effect to header
        document.addEventListener('mousemove', (e) => {
            const header = document.querySelector('.header');
            const x = (e.clientX / window.innerWidth - 0.5) * 20;
            const y = (e.clientY / window.innerHeight - 0.5) * 20;
            header.style.transform = `translate(${x}px, ${y}px)`;
        });
    </script>
</body>
</html>

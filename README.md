<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Atharwa Vatsyayan - Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 50%, #0f3460 100%);
            color: #ecf0f1;
            overflow-x: hidden;
            min-height: 100vh;
            padding: 20px;
        }

        /* Animated background */
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
        }

        /* Hero Section */
        .hero {
            text-align: center;
            margin-bottom: 60px;
            animation: slideDown 0.8s ease-out;
        }

        @keyframes slideDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .avatar {
            width: 150px;
            height: 150px;
            margin: 0 auto 20px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 80px;
            box-shadow: 0 0 40px rgba(102, 126, 234, 0.4);
            animation: float 3s ease-in-out infinite, pulse 2s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { box-shadow: 0 0 40px rgba(102, 126, 234, 0.4); }
            50% { box-shadow: 0 0 60px rgba(102, 126, 234, 0.8); }
        }

        h1 {
            font-size: 3.5em;
            font-weight: 800;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 50%, #f093fb 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 10px;
            letter-spacing: -1px;
        }

        .subtitle {
            font-size: 1.2em;
            color: #a8dadc;
            margin-bottom: 30px;
            font-weight: 300;
            letter-spacing: 2px;
        }

        /* Glassmorphism Card */
        .glass-card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 40px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
            animation: slideUp 0.8s ease-out 0.2s both;
            transition: all 0.3s ease;
        }

        @keyframes slideUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .glass-card:hover {
            background: rgba(255, 255, 255, 0.08);
            border: 1px solid rgba(255, 255, 255, 0.2);
            box-shadow: 0 12px 40px rgba(102, 126, 234, 0.2);
            transform: translateY(-5px);
        }

        .section-title {
            font-size: 1.8em;
            font-weight: 700;
            margin-bottom: 25px;
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .section-title::before {
            content: '';
            width: 40px;
            height: 4px;
            background: linear-gradient(90deg, #667eea 0%, #764ba2 100%);
            border-radius: 2px;
        }

        /* About Section */
        .about-text {
            font-size: 1.1em;
            line-height: 1.8;
            color: #d1d5db;
        }

        .highlight {
            color: #667eea;
            font-weight: 600;
        }

        /* Tech Stack */
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }

        .tech-item {
            background: linear-gradient(135deg, rgba(102, 126, 234, 0.2), rgba(118, 75, 162, 0.2));
            border: 1px solid rgba(102, 126, 234, 0.3);
            border-radius: 12px;
            padding: 15px 10px;
            text-align: center;
            font-size: 0.95em;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            animation: slideUp 0.8s ease-out;
        }

        .tech-item:hover {
            background: linear-gradient(135deg, rgba(102, 126, 234, 0.4), rgba(118, 75, 162, 0.4));
            border: 1px solid rgba(102, 126, 234, 0.6);
            transform: translateY(-5px);
            box-shadow: 0 8px 24px rgba(102, 126, 234, 0.3);
        }

        /* Current Projects */
        .project-item {
            background: rgba(102, 126, 234, 0.1);
            border-left: 4px solid #667eea;
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 15px;
            transition: all 0.3s ease;
        }

        .project-item:hover {
            background: rgba(102, 126, 234, 0.15);
            border-left-color: #764ba2;
            transform: translateX(10px);
        }

        .project-item strong {
            color: #667eea;
        }

        /* Socials */
        .socials {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            margin-top: 20px;
        }

        .social-btn {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            text-decoration: none;
            padding: 12px 24px;
            border-radius: 50px;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(102, 126, 234, 0.3);
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        .social-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(102, 126, 234, 0.5);
        }

        /* Stats Section */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .stat-card {
            background: linear-gradient(135deg, rgba(240, 147, 251, 0.1), rgba(102, 126, 234, 0.1));
            padding: 25px;
            border-radius: 15px;
            text-align: center;
            border: 1px solid rgba(102, 126, 234, 0.2);
        }

        .stat-number {
            font-size: 2.5em;
            font-weight: 800;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .stat-label {
            color: #a8dadc;
            margin-top: 10px;
            font-size: 0.9em;
        }

        /* Fun Fact */
        .fun-fact {
            background: linear-gradient(135deg, rgba(240, 147, 251, 0.15), rgba(102, 126, 234, 0.15));
            border: 1px solid rgba(240, 147, 251, 0.3);
            padding: 25px;
            border-radius: 15px;
            text-align: center;
            margin-top: 40px;
            animation: slideUp 0.8s ease-out 0.6s both;
        }

        .fun-fact-text {
            font-size: 1.3em;
            color: #f093fb;
            font-weight: 600;
            letter-spacing: 1px;
        }

        /* Responsive */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.5em;
            }

            .glass-card {
                padding: 25px;
            }

            .tech-grid {
                grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
            }
        }

        /* Decorative elements */
        .glow-1 {
            position: fixed;
            width: 300px;
            height: 300px;
            background: radial-gradient(circle, rgba(102, 126, 234, 0.2), transparent);
            border-radius: 50%;
            top: -100px;
            right: -100px;
            pointer-events: none;
        }

        .glow-2 {
            position: fixed;
            width: 250px;
            height: 250px;
            background: radial-gradient(circle, rgba(118, 75, 162, 0.15), transparent);
            border-radius: 50%;
            bottom: -50px;
            left: -50px;
            pointer-events: none;
        }
    </style>
</head>
<body>
    <div class="glow-1"></div>
    <div class="glow-2"></div>

    <div class="container">
        <!-- Hero Section -->
        <div class="hero">
            <div class="avatar">👨‍💻</div>
            <h1>Atharwa Vatsyayan</h1>
            <p class="subtitle">Full-Stack Developer | ML Enthusiast | Quantum Explorer</p>
        </div>

        <!-- About Section -->
        <div class="glass-card">
            <div class="section-title">About Me</div>
            <p class="about-text">
                🎓 <span class="highlight">4th-year B.Tech CSE student</span> at VIT Vellore<br><br>
                I'm a passionate developer who loves building <span class="highlight">intelligent solutions</span> that bridge the gap between cutting-edge technology and real-world problems. From crafting beautiful web experiences to diving deep into quantum neural networks, I'm always exploring the next frontier.
            </p>
        </div>

        <!-- Tech Stack -->
        <div class="glass-card">
            <div class="section-title">Technology Arsenal</div>
            <div class="tech-grid">
                <div class="tech-item">Python</div>
                <div class="tech-item">JavaScript</div>
                <div class="tech-item">React.js</div>
                <div class="tech-item">Node.js</div>
                <div class="tech-item">C++</div>
                <div class="tech-item">TensorFlow</div>
                <div class="tech-item">OpenCV</div>
                <div class="tech-item">MongoDB</div>
                <div class="tech-item">MySQL</div>
                <div class="tech-item">HTML/CSS</div>
                <div class="tech-item">Git</div>
                <div class="tech-item">Data Science</div>
            </div>
        </div>

        <!-- Current Work -->
        <div class="glass-card">
            <div class="section-title">Current Explorations</div>
            <div class="project-item">
                🎯 <strong>Quantum Neural Networks (QNN)</strong> for disease detection — merging quantum computing with medical AI
            </div>
            <div class="project-item">
                📚 <strong>Advanced DSA</strong> — leveling up problem-solving skills for competitive programming
            </div>
            <div class="project-item">
                🚀 <strong>Full-Stack Projects</strong> — building production-ready applications with modern tech stack
            </div>
        </div>

        <!-- Stats -->
        <div class="glass-card">
            <div class="section-title">Quick Stats</div>
            <div class="stats-grid">
                <div class="stat-card">
                    <div class="stat-number">50+</div>
                    <div class="stat-label">Projects</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">1000+</div>
                    <div class="stat-label">Commits</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">100%</div>
                    <div class="stat-label">Dedication</div>
                </div>
            </div>
        </div>

        <!-- Connect -->
        <div class="glass-card">
            <div class="section-title">Let's Connect</div>
            <p class="about-text" style="margin-bottom: 20px;">
                Interested in collaborating or just want to chat? Reach out!
            </p>
            <div class="socials">
                <a href="https://linkedin.com/in/AtharwaVatsyayan" class="social-btn">
                    💼 LinkedIn
                </a>
                <a href="https://instagram.com/atharwa.23" class="social-btn">
                    📸 Instagram
                </a>
                <a href="mailto:atharwared@gmail.com" class="social-btn">
                    ✉️ Email
                </a>
                <a href="https://github.com/snorelax08" class="social-btn">
                    🐙 GitHub
                </a>
            </div>
        </div>

        <!-- Fun Fact -->
        <div class="fun-fact">
            <p class="fun-fact-text">⏰ Fun Fact: I can wake up without an alarm</p>
        </div>
    </div>
</body>
</html>

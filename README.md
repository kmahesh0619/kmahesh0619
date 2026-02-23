<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mahesh Kumar - Senior Android Engineer</title>
    <link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Outfit:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #3DDC84;
            --primary-dark: #2DB66D;
            --secondary: #7F52FF;
            --dark: #0D1117;
            --dark-card: #161B22;
            --text: #E6EDF3;
            --text-muted: #8B949E;
            --accent-orange: #FF6B35;
            --accent-blue: #4285F4;
            --border: #30363D;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Outfit', -apple-system, BlinkMacSystemFont, sans-serif;
            background: var(--dark);
            color: var(--text);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Animated Grid Background */
        .grid-background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: 
                linear-gradient(rgba(61, 220, 132, 0.05) 1px, transparent 1px),
                linear-gradient(90deg, rgba(61, 220, 132, 0.05) 1px, transparent 1px);
            background-size: 40px 40px;
            z-index: 0;
            animation: gridMove 20s linear infinite;
        }

        @keyframes gridMove {
            0% { transform: translate(0, 0); }
            100% { transform: translate(40px, 40px); }
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
            position: relative;
            z-index: 1;
        }

        /* Header Section */
        header {
            padding: 80px 0 60px;
            text-align: center;
            position: relative;
        }

        .profile-badge {
            display: inline-block;
            width: 140px;
            height: 140px;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            position: relative;
            margin-bottom: 30px;
            animation: float 6s ease-in-out infinite;
            box-shadow: 0 0 60px rgba(61, 220, 132, 0.3);
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(5deg); }
        }

        .profile-badge::before {
            content: '👋';
            position: absolute;
            font-size: 60px;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }

        h1 {
            font-family: 'Space Mono', monospace;
            font-size: 3.5em;
            font-weight: 700;
            margin-bottom: 15px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: fadeInUp 0.8s ease-out;
        }

        .subtitle {
            font-size: 1.4em;
            color: var(--text-muted);
            margin-bottom: 30px;
            animation: fadeInUp 1s ease-out;
        }

        .social-badges {
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
            animation: fadeInUp 1.2s ease-out;
        }

        .social-badge {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            padding: 12px 24px;
            background: var(--dark-card);
            border: 2px solid var(--border);
            border-radius: 12px;
            color: var(--text);
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            font-size: 0.95em;
        }

        .social-badge:hover {
            transform: translateY(-3px);
            border-color: var(--primary);
            box-shadow: 0 5px 20px rgba(61, 220, 132, 0.2);
        }

        .badge-icon {
            font-size: 1.2em;
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

        /* Section Styling */
        section {
            margin-bottom: 100px;
            animation: fadeInUp 0.8s ease-out;
        }

        .section-header {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 40px;
        }

        .section-icon {
            font-size: 2.5em;
        }

        .section-title {
            font-family: 'Space Mono', monospace;
            font-size: 2.2em;
            font-weight: 700;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        /* About Section */
        .about-content {
            background: var(--dark-card);
            border: 2px solid var(--border);
            border-radius: 20px;
            padding: 40px;
            position: relative;
            overflow: hidden;
        }

        .about-content::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(61, 220, 132, 0.05) 0%, transparent 70%);
            animation: pulse 8s infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }

        .about-text {
            font-size: 1.15em;
            line-height: 1.8;
            color: var(--text);
            margin-bottom: 30px;
            position: relative;
        }

        .focus-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            position: relative;
        }

        .focus-item {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 12px 20px;
            background: rgba(61, 220, 132, 0.1);
            border-left: 3px solid var(--primary);
            border-radius: 8px;
            font-weight: 500;
            transition: all 0.3s ease;
        }

        .focus-item:hover {
            background: rgba(61, 220, 132, 0.2);
            transform: translateX(5px);
        }

        /* Tech Stack Grid */
        .tech-category {
            margin-bottom: 50px;
        }

        .category-title {
            font-family: 'Space Mono', monospace;
            font-size: 1.5em;
            margin-bottom: 20px;
            color: var(--primary);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }

        .tech-badge {
            background: var(--dark-card);
            border: 2px solid var(--border);
            border-radius: 15px;
            padding: 20px;
            text-align: center;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
        }

        .tech-badge::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(61, 220, 132, 0.1), transparent);
            transition: left 0.5s;
        }

        .tech-badge:hover::before {
            left: 100%;
        }

        .tech-badge:hover {
            border-color: var(--primary);
            transform: translateY(-8px) scale(1.02);
            box-shadow: 0 10px 30px rgba(61, 220, 132, 0.2);
        }

        .tech-icon {
            font-size: 2.5em;
            margin-bottom: 10px;
            display: block;
        }

        .tech-name {
            font-weight: 600;
            font-size: 1.1em;
            margin-bottom: 5px;
        }

        .tech-level {
            font-size: 0.9em;
            color: var(--text-muted);
        }

        /* Experience Timeline */
        .timeline {
            position: relative;
            padding-left: 50px;
        }

        .timeline::before {
            content: '';
            position: absolute;
            left: 0;
            top: 0;
            bottom: 0;
            width: 3px;
            background: linear-gradient(180deg, var(--primary), var(--secondary));
        }

        .timeline-item {
            background: var(--dark-card);
            border: 2px solid var(--border);
            border-radius: 20px;
            padding: 35px;
            margin-bottom: 30px;
            position: relative;
            transition: all 0.4s ease;
        }

        .timeline-item::before {
            content: '';
            position: absolute;
            left: -63px;
            top: 40px;
            width: 24px;
            height: 24px;
            border-radius: 50%;
            background: var(--primary);
            border: 4px solid var(--dark);
            box-shadow: 0 0 0 4px var(--border);
            animation: pulse-dot 2s infinite;
        }

        @keyframes pulse-dot {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.2); }
        }

        .timeline-item:hover {
            border-color: var(--primary);
            transform: translateX(10px);
            box-shadow: 0 10px 40px rgba(61, 220, 132, 0.15);
        }

        .job-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 20px;
            flex-wrap: wrap;
            gap: 15px;
        }

        .job-title {
            font-size: 1.6em;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 5px;
        }

        .company {
            font-size: 1.2em;
            color: var(--text);
            font-weight: 500;
        }

        .duration {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: rgba(61, 220, 132, 0.15);
            border: 1px solid var(--primary);
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.95em;
            font-weight: 500;
            white-space: nowrap;
        }

        .responsibilities {
            list-style: none;
            margin-top: 20px;
        }

        .responsibilities li {
            padding: 12px 0;
            padding-left: 30px;
            position: relative;
            color: var(--text-muted);
            line-height: 1.6;
        }

        .responsibilities li::before {
            content: '✓';
            position: absolute;
            left: 0;
            color: var(--primary);
            font-weight: bold;
            font-size: 1.2em;
        }

        /* Projects Grid */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
            gap: 30px;
        }

        .project-card {
            background: var(--dark-card);
            border: 2px solid var(--border);
            border-radius: 20px;
            padding: 40px;
            position: relative;
            overflow: hidden;
            transition: all 0.4s ease;
        }

        .project-card::after {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 150px;
            height: 150px;
            background: radial-gradient(circle, rgba(127, 82, 255, 0.2) 0%, transparent 70%);
            border-radius: 50%;
            transform: translate(50%, -50%);
            transition: all 0.4s ease;
        }

        .project-card:hover::after {
            transform: translate(30%, -30%) scale(1.5);
        }

        .project-card:hover {
            border-color: var(--secondary);
            transform: translateY(-10px);
            box-shadow: 0 15px 50px rgba(127, 82, 255, 0.2);
        }

        .project-icon {
            font-size: 3em;
            margin-bottom: 20px;
            display: block;
        }

        .project-title {
            font-size: 1.8em;
            font-weight: 700;
            margin-bottom: 10px;
            color: var(--secondary);
        }

        .project-subtitle {
            color: var(--text-muted);
            margin-bottom: 20px;
            font-size: 1.05em;
        }

        .project-features {
            list-style: none;
            margin-top: 20px;
        }

        .project-features li {
            padding: 8px 0;
            padding-left: 25px;
            position: relative;
            color: var(--text);
        }

        .project-features li::before {
            content: '▸';
            position: absolute;
            left: 0;
            color: var(--secondary);
            font-weight: bold;
        }

        /* GitHub Stats */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 30px;
        }

        .stat-card {
            background: var(--dark-card);
            border: 2px solid var(--border);
            border-radius: 20px;
            padding: 30px;
            text-align: center;
            transition: all 0.3s ease;
        }

        .stat-card:hover {
            border-color: var(--primary);
            transform: scale(1.05);
        }

        .stat-card img {
            width: 100%;
            height: auto;
            border-radius: 10px;
        }

        /* Current Focus */
        .focus-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
        }

        .focus-card {
            background: var(--dark-card);
            border: 2px solid var(--border);
            border-radius: 15px;
            padding: 30px;
            transition: all 0.3s ease;
            position: relative;
        }

        .focus-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            border-radius: 15px 15px 0 0;
        }

        .focus-card:hover {
            border-color: var(--primary);
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(61, 220, 132, 0.15);
        }

        .focus-card-icon {
            font-size: 2.5em;
            margin-bottom: 15px;
            display: block;
        }

        .focus-card-title {
            font-size: 1.3em;
            font-weight: 600;
            color: var(--text);
        }

        /* Contact Section */
        .contact-cta {
            text-align: center;
            background: var(--dark-card);
            border: 3px solid var(--primary);
            border-radius: 25px;
            padding: 60px 40px;
            position: relative;
            overflow: hidden;
        }

        .contact-cta::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 300px;
            height: 300px;
            background: radial-gradient(circle, rgba(61, 220, 132, 0.1) 0%, transparent 70%);
            transform: translate(-50%, -50%);
            animation: pulse 4s infinite;
        }

        .contact-cta-content {
            position: relative;
            z-index: 1;
        }

        .cta-title {
            font-family: 'Space Mono', monospace;
            font-size: 2.5em;
            margin-bottom: 15px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .cta-subtitle {
            font-size: 1.2em;
            color: var(--text-muted);
            margin-bottom: 30px;
        }

        .contact-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }

        .cta-button {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            padding: 15px 35px;
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
            color: var(--dark);
            border-radius: 12px;
            text-decoration: none;
            font-weight: 700;
            font-size: 1.1em;
            transition: all 0.3s ease;
            border: none;
        }

        .cta-button:hover {
            transform: scale(1.08);
            box-shadow: 0 10px 30px rgba(61, 220, 132, 0.4);
        }

        .cta-button.secondary {
            background: transparent;
            border: 2px solid var(--primary);
            color: var(--primary);
        }

        /* Footer Quote */
        .footer-quote {
            text-align: center;
            padding: 60px 20px 40px;
            font-family: 'Space Mono', monospace;
            font-size: 1.5em;
            color: var(--text-muted);
            font-style: italic;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            h1 { font-size: 2.2em; }
            .subtitle { font-size: 1.1em; }
            .section-title { font-size: 1.8em; }
            .timeline { padding-left: 30px; }
            .timeline-item::before { left: -43px; }
            .projects-grid { grid-template-columns: 1fr; }
            .focus-grid { grid-template-columns: 1fr; }
            header { padding: 50px 0 40px; }
        }

        /* Smooth Scroll */
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body>
    <div class="grid-background"></div>
    
    <div class="container">
        <!-- Header Section -->
        <header>
            <div class="profile-badge"></div>
            <h1>Hi 👋, I'm Mahesh Kumar</h1>
            <p class="subtitle">🚀 Senior Android Engineer | Kotlin Expert | Compose Enthusiast</p>
            
            <div class="social-badges">
                <a href="https://www.linkedin.com/in/maheshntz2019" class="social-badge" target="_blank">
                    <span class="badge-icon">💼</span>
                    LinkedIn
                </a>
                <a href="https://twitter.com/k.mahesh0619" class="social-badge" target="_blank">
                    <span class="badge-icon">🐦</span>
                    Twitter
                </a>
                <a href="mailto:k.mahesh.21@gmail.com" class="social-badge" target="_blank">
                    <span class="badge-icon">✉️</span>
                    Email
                </a>
            </div>
        </header>

        <!-- About Section -->
        <section id="about">
            <div class="section-header">
                <span class="section-icon">👤</span>
                <h2 class="section-title">About Me</h2>
            </div>
            
            <div class="about-content">
                <p class="about-text">
                    🎯 Passionate <strong>Android Engineer</strong> with <strong>5+ years of experience</strong> building scalable, 
                    high-performance mobile applications that serve thousands of users daily.
                </p>
                <p class="about-text">
                    💡 I love solving real-world problems using modern Android technologies and clean architecture principles. 
                    My focus is on creating seamless, performant user experiences while maintaining code quality and scalability.
                </p>
                
                <div class="focus-list">
                    <div class="focus-item">🔥 Performance Optimization</div>
                    <div class="focus-item">🏗️ Clean Architecture</div>
                    <div class="focus-item">📦 Scalable Modular Apps</div>
                    <div class="focus-item">🌐 Kotlin Multiplatform</div>
                    <div class="focus-item">🎨 Jetpack Compose</div>
                </div>
            </div>
        </section>

        <!-- Tech Stack Section -->
        <section id="tech-stack">
            <div class="section-header">
                <span class="section-icon">🧠</span>
                <h2 class="section-title">Tech Stack & Skills</h2>
            </div>

            <div class="tech-category">
                <h3 class="category-title">📱 Mobile Development</h3>
                <div class="tech-grid">
                    <div class="tech-badge">
                        <span class="tech-icon">🤖</span>
                        <div class="tech-name">Android</div>
                        <div class="tech-level">Expert</div>
                    </div>
                    <div class="tech-badge">
                        <span class="tech-icon">🔷</span>
                        <div class="tech-name">Kotlin</div>
                        <div class="tech-level">Advanced</div>
                    </div>
                    <div class="tech-badge">
                        <span class="tech-icon">☕</span>
                        <div class="tech-name">Java</div>
                        <div class="tech-level">Strong</div>
                    </div>
                    <div class="tech-badge">
                        <span class="tech-icon">🎨</span>
                        <div class="tech-name">Jetpack Compose</div>
                        <div class="tech-level">Modern</div>
                    </div>
                    <div class="tech-badge">
                        <span class="tech-icon">🌐</span>
                        <div class="tech-name">Compose Multiplatform</div>
                        <div class="tech-level">Cross-Platform</div>
                    </div>
                </div>
            </div>

            <div class="tech-category">
                <h3 class="category-title">🏗 Architecture & Tools</h3>
                <div class="tech-grid">
                    <div class="tech-badge">
                        <span class="tech-icon">🏛️</span>
                        <div class="tech-name">Clean Architecture</div>
                        <div class="tech-level">Scalable</div>
                    </div>
                    <div class="tech-badge">
                        <span class="tech-icon">📐</span>
                        <div class="tech-name">MVVM</div>
                        <div class="tech-level">Pattern</div>
                    </div>
                    <div class="tech-badge">
                        <span class="tech-icon">💉</span>
                        <div class="tech-name">Hilt</div>
                        <div class="tech-level">Dependency Injection</div>
                    </div>
                    <div class="tech-badge">
                        <span class="tech-icon">🗄️</span>
                        <div class="tech-name">Room</div>
                        <div class="tech-level">Database</div>
                    </div>
                    <div class="tech-badge">
                        <span class="tech-icon">🌐</span>
                        <div class="tech-name">Retrofit</div>
                        <div class="tech-level">API Integration</div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Experience Section -->
        <section id="experience">
            <div class="section-header">
                <span class="section-icon">💼</span>
                <h2 class="section-title">Professional Experience</h2>
            </div>

            <div class="timeline">
                <div class="timeline-item">
                    <div class="job-header">
                        <div>
                            <div class="job-title">Senior Android Developer</div>
                            <div class="company">Netsmartz Infotech Pvt. Ltd.</div>
                        </div>
                        <div class="duration">
                            📅 Jul 2023 – Present
                        </div>
                    </div>
                    
                    <ul class="responsibilities">
                        <li>Architected and developed multiple high-traffic Android applications serving thousands of users daily</li>
                        <li>Led the implementation of modern UI paradigms using <strong>Jetpack Compose</strong>, improving development efficiency by 40%</li>
                        <li>Improved app performance and scalability through optimization techniques and clean architecture patterns</li>
                        <li>Led feature architecture design and conducted comprehensive code reviews to maintain high quality standards</li>
                        <li>Mentored junior developers and established best practices for the mobile development team</li>
                    </ul>
                </div>

                <div class="timeline-item">
                    <div class="job-header">
                        <div>
                            <div class="job-title">Android Developer</div>
                            <div class="company">Krescent IT Labs</div>
                        </div>
                        <div class="duration">
                            📅 Apr 2021 – Jun 2023
                        </div>
                    </div>
                    
                    <ul class="responsibilities">
                        <li>Designed and shipped multiple production-ready Android applications from concept to deployment</li>
                        <li>Collaborated with cross-functional teams including designers, product managers, and backend engineers</li>
                        <li>Worked extensively on feature planning, implementation, and performance improvements</li>
                        <li>Implemented robust Android applications using Java and Kotlin with clean architecture principles</li>
                        <li>Integrated RESTful APIs, third-party SDKs, and modern Android libraries</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- Projects Section -->
        <section id="projects">
            <div class="section-header">
                <span class="section-icon">📂</span>
                <h2 class="section-title">Featured Projects</h2>
            </div>

            <div class="projects-grid">
                <div class="project-card">
                    <span class="project-icon">🚀</span>
                    <div class="project-title">Project A</div>
                    <div class="project-subtitle">Enterprise Mobile Solution</div>
                    <p style="color: var(--text-muted); margin-bottom: 20px;">
                        High-performance Android application designed for enterprise users with complex business requirements.
                    </p>
                    <ul class="project-features">
                        <li>Clean Architecture with MVVM pattern</li>
                        <li>Offline-first approach with Room database</li>
                        <li>Modular structure for scalability</li>
                        <li>Scalable backend integration with Retrofit</li>
                        <li>Modern UI with Jetpack Compose</li>
                    </ul>
                </div>

                <div class="project-card">
                    <span class="project-icon">🌍</span>
                    <div class="project-title">Project B</div>
                    <div class="project-subtitle">Compose Multiplatform App</div>
                    <p style="color: var(--text-muted); margin-bottom: 20px;">
                        Cross-platform application leveraging Compose Multiplatform for code sharing across Android and Desktop.
                    </p>
                    <ul class="project-features">
                        <li>Shared business logic across platforms</li>
                        <li>Android + Desktop support</li>
                        <li>Kotlin Multiplatform architecture</li>
                        <li>Modern UI with declarative approach</li>
                        <li>Efficient code reusability</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- GitHub Stats Section -->
        <section id="stats">
            <div class="section-header">
                <span class="section-icon">📊</span>
                <h2 class="section-title">GitHub Statistics</h2>
            </div>

            <div class="stats-grid">
                <div class="stat-card">
                    <img src="https://github-readme-stats.vercel.app/api?username=maheshntz2019&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=3DDC84&icon_color=7F52FF&text_color=E6EDF3" alt="GitHub Stats" />
                </div>
                <div class="stat-card">
                    <img src="https://github-readme-streak-stats.herokuapp.com/?user=maheshntz2019&theme=tokyonight&hide_border=true&background=0D1117&stroke=30363D&ring=3DDC84&fire=7F52FF&currStreakLabel=E6EDF3" alt="GitHub Streak" />
                </div>
            </div>
        </section>

        <!-- Current Focus Section -->
        <section id="focus">
            <div class="section-header">
                <span class="section-icon">🎯</span>
                <h2 class="section-title">Current Focus</h2>
            </div>

            <div class="focus-grid">
                <div class="focus-card">
                    <span class="focus-card-icon">🔥</span>
                    <div class="focus-card-title">Advanced Kotlin Multiplatform</div>
                </div>
                <div class="focus-card">
                    <span class="focus-card-icon">🚀</span>
                    <div class="focus-card-title">AI-Powered Mobile Apps</div>
                </div>
                <div class="focus-card">
                    <span class="focus-card-icon">🧩</span>
                    <div class="focus-card-title">Modular Scalable Systems</div>
                </div>
                <div class="focus-card">
                    <span class="focus-card-icon">🤖</span>
                    <div class="focus-card-title">AI + Compose Integration</div>
                </div>
            </div>
        </section>

        <!-- Contact CTA Section -->
        <section id="contact">
            <div class="contact-cta">
                <div class="contact-cta-content">
                    <h2 class="cta-title">Let's Connect!</h2>
                    <p class="cta-subtitle">
                        I'm always open to discussing new projects, creative ideas, or opportunities to be part of your vision.
                    </p>
                    
                    <div class="contact-buttons">
                        <a href="mailto:k.mahesh.21@gmail.com" class="cta-button">
                            ✉️ Email Me
                        </a>
                        <a href="https://www.linkedin.com/in/maheshntz2019" class="cta-button secondary" target="_blank">
                            💼 LinkedIn
                        </a>
                    </div>
                </div>
            </div>
        </section>

        <!-- Footer Quote -->
        <div class="footer-quote">
            💬 "Turning Ideas into Scalable Mobile Solutions"
        </div>
    </div>

    <script>
        // Smooth scroll for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth', block: 'start' });
                }
            });
        });

        // Intersection Observer for fade-in animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        document.querySelectorAll('section').forEach(section => {
            section.style.opacity = '0';
            section.style.transform = 'translateY(30px)';
            section.style.transition = 'opacity 0.8s ease, transform 0.8s ease';
            observer.observe(section);
        });
    </script>
</body>
</html>

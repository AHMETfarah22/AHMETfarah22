<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ahmed Farah | Full Stack Developer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #2563eb;
            --secondary: #7e22ce;
            --dark: #1e293b;
            --light: #f8fafc;
            --gray: #64748b;
            --success: #10b981;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0f172a, #1e293b);
            color: var(--light);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header & Navigation */
        header {
            padding: 20px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            background: rgba(15, 23, 42, 0.9);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        .nav-links {
            display: flex;
            gap: 30px;
        }
        
        .nav-links a {
            color: var(--light);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        .nav-links a:hover {
            color: var(--primary);
        }
        
        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding-top: 80px;
            position: relative;
        }
        
        .hero-content {
            max-width: 800px;
            z-index: 1;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        .typing-text {
            font-size: 1.8rem;
            margin-bottom: 30px;
            color: var(--light);
            font-weight: 600;
        }
        
        .typing-text span {
            color: var(--primary);
        }
        
        .hero-buttons {
            display: flex;
            gap: 15px;
            margin-top: 30px;
        }
        
        .btn {
            padding: 12px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
            display: inline-block;
        }
        
        .btn-primary {
            background: linear-gradient(to right, var(--primary), var(--secondary));
            color: white;
            border: none;
        }
        
        .btn-outline {
            border: 2px solid var(--primary);
            color: var(--primary);
            background: transparent;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        /* Languages Section */
        .languages {
            padding: 100px 0;
        }
        
        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 60px;
            position: relative;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            border-radius: 2px;
        }
        
        .language-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .language-card {
            background: rgba(30, 41, 59, 0.8);
            border-radius: 15px;
            padding: 30px;
            text-align: center;
            transition: transform 0.3s, box-shadow 0.3s;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .language-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.4);
        }
        
        .language-icon {
            font-size: 3rem;
            margin-bottom: 20px;
        }
        
        .language-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
        }
        
        .language-card p {
            color: var(--gray);
        }
        
        /* Stats Section */
        .stats {
            padding: 80px 0;
            background: rgba(15, 23, 42, 0.7);
        }
        
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            text-align: center;
        }
        
        .stat-item h3 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        /* Projects Section */
        .projects {
            padding: 100px 0;
        }
        
        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .project-card {
            background: rgba(30, 41, 59, 0.8);
            border-radius: 15px;
            overflow: hidden;
            transition: transform 0.3s;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .project-card:hover {
            transform: translateY(-10px);
        }
        
        .project-img {
            height: 200px;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
            color: white;
        }
        
        .project-content {
            padding: 20px;
        }
        
        .project-content h3 {
            font-size: 1.5rem;
            margin-bottom: 10px;
        }
        
        .project-content p {
            color: var(--gray);
            margin-bottom: 20px;
        }
        
        /* Footer */
        footer {
            background: rgba(15, 23, 42, 0.9);
            padding: 50px 0 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .footer-content {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-column {
            flex: 1;
            min-width: 250px;
        }
        
        .footer-column h3 {
            font-size: 1.5rem;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-column h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 40px;
            height: 3px;
            background: linear-gradient(to right, var(--primary), var(--secondary));
        }
        
        .footer-column p {
            margin-bottom: 15px;
            color: var(--gray);
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            color: var(--light);
            text-decoration: none;
            transition: all 0.3s;
        }
        
        .social-links a:hover {
            background: linear-gradient(to right, var(--primary), var(--secondary));
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: var(--gray);
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .typing-text {
                font-size: 1.5rem;
            }
            
            .hero-buttons {
                flex-direction: column;
            }
            
            .nav-links {
                display: none;
            }
        }
        
        /* Animations */
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-15px); }
            100% { transform: translateY(0px); }
        }
        
        .floating {
            animation: float 5s ease-in-out infinite;
        }
    </style>
</head>
<body>
    <!-- Header & Navigation -->
    <header>
        <div class="container">
            <nav>
                <div class="logo">AFM.Coding</div>
                <div class="nav-links">
                    <a href="#home">Home</a>
                    <a href="#languages">Skills</a>
                    <a href="#projects">Projects</a>
                    <a href="#contact">Contact</a>
                </div>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <h1>Ahmed Farah</h1>
                <div class="typing-text">I'm a <span id="typing"></span></div>
                <p>Creative developer from Somalia & Türkiye with a passion for building modern applications and interfaces. I love clean code and beautiful design that creates exceptional user experiences.</p>
                <div class="hero-buttons">
                    <a href="#projects" class="btn btn-primary">View My Work</a>
                    <a href="#contact" class="btn btn-outline">Get In Touch</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Languages Section -->
    <section class="languages" id="languages">
        <div class="container">
            <h2 class="section-title">Technical Skills</h2>
            <div class="language-grid">
                <div class="language-card floating">
                    <div class="language-icon">
                        <i class="fab fa-html5" style="color: #e34f26;"></i>
                    </div>
                    <h3>HTML5</h3>
                    <p>Semantic markup, accessibility, modern APIs</p>
                </div>
                
                <div class="language-card floating" style="animation-delay: 0.5s;">
                    <div class="language-icon">
                        <i class="fab fa-css3-alt" style="color: #264de4;"></i>
                    </div>
                    <h3>CSS3</h3>
                    <p>Flexbox, Grid, animations, responsive design</p>
                </div>
                
                <div class="language-card floating" style="animation-delay: 1s;">
                    <div class="language-icon">
                        <i class="fab fa-js-square" style="color: #f7df1e;"></i>
                    </div>
                    <h3>JavaScript</h3>
                    <p>ES6+, React, Vue, Node.js, Express</p>
                </div>
                
                <div class="language-card floating" style="animation-delay: 1.5s;">
                    <div class="language-icon">
                        <i class="fab fa-python" style="color: #3776ab;"></i>
                    </div>
                    <h3>Python</h3>
                    <p>Django, Flask, data analysis, automation</p>
                </div>
                
                <div class="language-card floating" style="animation-delay: 2s;">
                    <div class="language-icon">
                        <i class="fab fa-java" style="color: #007396;"></i>
                    </div>
                    <h3>Java</h3>
                    <p>Spring Boot, Android development</p>
                </div>
                
                <div class="language-card floating" style="animation-delay: 2.5s;">
                    <div class="language-icon">
                        <i class="fab fa-microsoft" style="color: #5e367d;"></i>
                    </div>
                    <h3>C#</h3>
                    <p>.NET framework, Unity game development</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Stats Section -->
    <section class="stats">
        <div class="container">
            <div class="stats-grid">
                <div class="stat-item">
                    <h3>50+</h3>
                    <p>Projects Completed</p>
                </div>
                <div class="stat-item">
                    <h3>5+</h3>
                    <p>Years Experience</p>
                </div>
                <div class="stat-item">
                    <h3>36</h3>
                    <p>Happy Clients</p>
                </div>
                <div class="stat-item">
                    <h3>15+</h3>
                    <p>Technologies Mastered</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section class="projects" id="projects">
        <div class="container">
            <h2 class="section-title">Featured Projects</h2>
            <div class="project-grid">
                <div class="project-card">
                    <div class="project-img">
                        <i class="fas fa-shopping-cart"></i>
                    </div>
                    <div class="project-content">
                        <h3>E-Commerce Platform</h3>
                        <p>Full-stack e-commerce solution with React, Node.js, and MongoDB</p>
                        <a href="#" class="btn btn-primary">View Project</a>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-img">
                        <i class="fas fa-mobile-alt"></i>
                    </div>
                    <div class="project-content">
                        <h3>Fitness App</h3>
                        <p>Mobile fitness tracking application with React Native and Firebase</p>
                        <a href="#" class="btn btn-primary">View Project</a>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-img">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <div class="project-content">
                        <h3>Data Visualization</h3>
                        <p>Interactive data dashboard with Python, D3.js, and Flask</p>
                        <a href="#" class="btn btn-primary">View Project</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contact">
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>Ahmed Farah</h3>
                    <p>Full Stack Developer & UI/UX Designer with a passion for creating beautiful, functional applications.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-github"></i></a>
                        <a href="#"><i class="fab fa-linkedin"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                    </div>
                </div>
                
                <div class="footer-column">
                    <h3>Contact Me</h3>
                    <p><i class="fas fa-envelope"></i> guray0449@gmail.com</p>
                    <p><i class="fas fa-map-marker-alt"></i> Somalia / Türkiye</p>
                </div>
                
                <div class="footer-column">
                    <h3>Skills Overview</h3>
                    <p>Frontend: HTML, CSS, JavaScript, React</p>
                    <p>Backend: Node.js, Python, PHP, Java</p>
                    <p>Database: MongoDB, MySQL, Firebase</p>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 Ahmed Farah. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Typing effect
        const typingElement = document.getElementById('typing');
        const typingTexts = ['Full Stack Developer', 'UI/UX Designer', 'Problem Solver', 'Creative Thinker'];
        let textIndex = 0;
        let charIndex = 0;
        let isDeleting = false;
        let typingSpeed = 100;

        function type() {
            const currentText = typingTexts[textIndex];
            
            if (isDeleting) {
                // Remove char
                typingElement.textContent = currentText.substring(0, charIndex - 1);
                charIndex--;
                typingSpeed = 50;
            } else {
                // Add char
                typingElement.textContent = currentText.substring(0, charIndex + 1);
                charIndex++;
                typingSpeed = 100;
            }
            
            // Check if text is complete
            if (!isDeleting && charIndex === currentText.length) {
                isDeleting = true;
                typingSpeed = 1000; // Pause at end
            } else if (isDeleting && charIndex === 0) {
                isDeleting = false;
                textIndex++;
                if (textIndex === typingTexts.length) textIndex = 0;
                typingSpeed = 500; // Pause before starting next
            }
            
            setTimeout(type, typingSpeed);
        }

        // Start typing effect when page loads
        document.addEventListener('DOMContentLoaded', type);
        
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
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
            });
        });
    </script>
</body>
</html>

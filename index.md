<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Muhammad Rusydi | IT Portfolio</title>
    <meta name="description" content="Software Developer | ERP & Cloud Engineer | Security-Aware" />
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/devicon.min.css">
    <style>
        .markdown-body h1 {
            display: none;
        }
        :root {
            --bg: #0a141a;
            --card: #1c3a4a;
            --text: #ecf4f8;
            --muted: #8fbdd6;
            --accent: #4591ba;
        }

        * {
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            margin: 0;
            font-family: system-ui, -apple-system, BlinkMacSystemFont, sans-serif;
            background: var(--bg);
            color: var(--text);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Animated gradient background */
        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(circle at 20% 50%, rgba(69, 145, 186, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 80% 80%, rgba(106, 167, 200, 0.08) 0%, transparent 50%);
            animation: gradientShift 15s ease infinite;
            pointer-events: none;
            z-index: 0;
        }

        @keyframes gradientShift {
            0%, 100% { opacity: 1; transform: scale(1); }
            50% { opacity: 0.8; transform: scale(1.1); }
        }

        body > * {
            position: relative;
            z-index: 1;
        }

        a {
            color: var(--accent);
            text-decoration: none;
        }

        header {
            padding: 3rem 1.5rem;
            text-align: center;
            animation: fadeInDown 0.8s ease-out;
        }

        header h1 {
            font-size: 2.2rem;
            margin-bottom: .5rem;
            background: linear-gradient(135deg, var(--text) 0%, var(--accent) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: fadeInDown 0.8s ease-out 0.2s backwards;
        }

        header p {
            color: var(--muted);
            max-width: 720px;
            margin: auto;
            animation: fadeInDown 0.8s ease-out 0.4s backwards;
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

        @keyframes scaleIn {
            from {
                opacity: 0;
                transform: scale(0.9);
            }
            to {
                opacity: 1;
                transform: scale(1);
            }
        }

        nav {
            display: flex;
            justify-content: center;
            gap: 1rem;
            flex-wrap: wrap;
            margin-top: 1.5rem;
        }

        nav a {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            background: var(--card);
            padding: 0.75rem 1.25rem;
            border-radius: 25px;
            font-size: 1rem;
            font-weight: 500;
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            color: var(--text);
            position: relative;
            overflow: hidden;
            animation: fadeInUp 0.6s ease-out backwards;
        }

        nav a:nth-child(1) { animation-delay: 0.5s; }
        nav a:nth-child(2) { animation-delay: 0.6s; }
        nav a:nth-child(3) { animation-delay: 0.7s; }
        nav a:nth-child(4) { animation-delay: 0.8s; }
        nav a:nth-child(5) { animation-delay: 0.9s; }

        nav a::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(236, 244, 248, 0.1), transparent);
            transition: left 0.5s ease;
        }

        nav a:hover::before {
            left: 100%;
        }

        nav a:hover {
            background: var(--accent);
            color: var(--bg);
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(69, 145, 186, 0.3);
        }

        nav a:active {
            transform: translateY(-1px);
        }

        section {
            max-width: 1000px;
            margin: auto;
            padding: 1.5rem 1.5rem;
        }

        h2 {
            font-size: 1.6rem;
            margin-bottom: 1rem;
            margin-top: 0;
            position: relative;
            display: inline-block;
        }

        h2::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 3px;
            background: linear-gradient(90deg, var(--accent), transparent);
            animation: expandWidth 0.8s ease-out forwards;
            animation-delay: 0.3s;
        }

        @keyframes expandWidth {
            to {
                width: 100%;
            }
        }

        .grid {
            display: grid;
            gap: 1.5rem;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        }

        .card {
            background: var(--card);
            padding: 1.5rem;
            border-radius: 14px;
            box-shadow: 0 10px 30px rgba(10, 20, 26, .5);
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
            border: 1px solid transparent;
        }

        .card::before {
            content: '';
            position: absolute;
            top: -2px;
            left: -2px;
            right: -2px;
            bottom: -2px;
            background: linear-gradient(135deg, var(--accent), transparent);
            border-radius: 14px;
            opacity: 0;
            transition: opacity 0.4s ease;
            z-index: -1;
        }

        .card:hover {
            transform: translateY(-8px) scale(1.02);
            box-shadow: 0 20px 40px rgba(69, 145, 186, 0.2);
            border-color: rgba(69, 145, 186, 0.3);
        }

        .card:hover::before {
            opacity: 1;
        }

        .card h3 {
            margin-top: 0;
            color: var(--text);
            transition: color 0.3s ease;
        }

        .card:hover h3 {
            color: var(--accent);
        }

        .tag {
            display: inline-flex;
            align-items: center;
            gap: 0.35rem;
            background: rgba(69, 145, 186, .15);
            color: var(--accent);
            padding: .35rem .75rem;
            border-radius: 999px;
            font-size: .8rem;
            margin: .3rem .3rem 0 0;
            transition: all 0.3s ease;
            cursor: default;
        }

        .tag i {
            font-size: 1rem;
            color: var(--accent);
            transition: color 0.3s ease;
        }

        .tag img {
            width: 16px;
            height: 16px;
            object-fit: contain;
            transition: filter 0.3s ease;
        }

        .tag:hover {
            background: var(--accent);
            color: var(--bg);
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(69, 145, 186, 0.3);
        }

        .tag:hover i {
            color: var(--bg);
        }

        .tag:hover img {
            filter: brightness(0) invert(1);
        }

        footer {
            text-align: center;
            padding: 2rem 1.5rem;
            color: var(--muted);
            font-size: .9rem;
            animation: fadeIn 1s ease-out 1.5s backwards;
        }

        /* Scroll-triggered animations */
        .fade-in-scroll {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.6s ease-out, transform 0.6s ease-out;
        }

        .fade-in-scroll.visible {
            opacity: 1;
            transform: translateY(0);
        }

        /* Stagger effect for grid items */
        .grid .card {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.6s ease-out, transform 0.6s ease-out;
        }

        .grid .card.visible {
            opacity: 1;
            transform: translateY(0);
        }

        .grid .card:nth-child(1).visible { transition-delay: 0.1s; }
        .grid .card:nth-child(2).visible { transition-delay: 0.2s; }
        .grid .card:nth-child(3).visible { transition-delay: 0.3s; }
        .grid .card:nth-child(4).visible { transition-delay: 0.4s; }
        .grid .card:nth-child(5).visible { transition-delay: 0.5s; }
        .grid .card:nth-child(6).visible { transition-delay: 0.6s; }

        /* Project year headers */
        .year-header {
            margin-top: 1.5rem;
            margin-bottom: 1rem;
            color: var(--accent);
            opacity: 0;
            transform: translateX(-30px);
            transition: all 0.6s ease-out;
        }

        .year-header.visible {
            opacity: 1;
            transform: translateX(0);
        }

        /* Link hover effects */
        a {
            position: relative;
            transition: color 0.3s ease;
        }

        section a:not(nav a) {
            color: var(--accent);
            text-decoration: none;
        }

        section a:not(nav a)::after {
            content: '';
            position: absolute;
            bottom: -2px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--accent);
            transition: width 0.3s ease;
        }

        section a:not(nav a):hover::after {
            width: 100%;
        }

        section a:not(nav a):hover {
            color: var(--text);
        }

        /* Floating animation for icons in nav */
        @keyframes float {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-3px);
            }
        }

        nav a:hover {
            animation: float 0.6s ease-in-out;
        }

        /* Scroll to top button */
        .scroll-top {
            position: fixed;
            bottom: 2rem;
            right: 2rem;
            width: 50px;
            height: 50px;
            background: var(--accent);
            color: var(--bg);
            border: none;
            border-radius: 50%;
            font-size: 1.5rem;
            cursor: pointer;
            opacity: 0;
            transform: translateY(100px);
            transition: all 0.3s ease;
            box-shadow: 0 5px 20px rgba(69, 145, 186, 0.4);
            z-index: 1000;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .scroll-top.visible {
            opacity: 1;
            transform: translateY(0);
        }

        .scroll-top:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(69, 145, 186, 0.6);
        }

        .scroll-top:active {
            transform: scale(0.95);
        }

        /* Loading animation */
        @keyframes pulse {
            0%, 100% {
                opacity: 1;
            }
            50% {
                opacity: 0.5;
            }
        }

        /* Responsive adjustments */
        @media (max-width: 768px) {
            header h1 {
                font-size: 1.8rem;
            }

            nav a {
                padding: 0.6rem 1rem;
                font-size: 0.9rem;
            }

            .card {
                padding: 1.25rem;
            }

            .scroll-top {
                bottom: 1rem;
                right: 1rem;
                width: 45px;
                height: 45px;
            }
        }
    </style>
</head>

<body>

    <header id="home">
        <h2>Muhammad Rusydi Bin Sazali</h2>
        <p>Software Developer • ERP & Cloud Engineer</p>
        <nav>
            <a href="#about">📋 About</a>
            <a href="#skills">🛠️ Skills</a>
            <a href="#projects">🚀 Projects</a>
            <a href="#contact">📧 Contact</a>
            <a href="business.html">💼 Business</a>
        </nav>
    </header>

    <section id="about">
        <h2>About Me</h2>
        <p>
            Software Developer with 6+ years of experience building and maintaining
            IoT monitoring systems, government and enterprise applications. Strong background in 
            Django, Python, React.js, React Native, LoRaWAN integration, ERPNext, cloud deployment, 
            and system integration. Experienced in building end-to-end solutions from sensor 
            integration to web dashboards and mobile applications. Currently expanding expertise 
            in cybersecurity (CEH).
            View <a href="business.html">freelance services</a> for project-based and contract work.
        </p>
    </section>

    <section id="skills">
        <h2>Skills</h2>
        <div class="grid">
            <div class="card">
                <h3>Programming</h3>
                <span class="tag"><i class="devicon-python-plain"></i> Python</span>
                <span class="tag"><i class="devicon-django-plain"></i> Django</span>
                <span class="tag"><i class="devicon-react-original"></i> React.js</span>
                <span class="tag"><i class="devicon-react-original"></i> React Native</span>
                <span class="tag"><i class="devicon-csharp-plain"></i> C# / .NET</span>
                <span class="tag"><i class="devicon-azuresqldatabase-plain"></i> SQL / PL-SQL</span>
                <span class="tag"><i class="devicon-html5-plain"></i> HTML</span>
                <span class="tag"><i class="devicon-css3-plain"></i> CSS</span>
            </div>
            <div class="card">
                <h3>IoT & Integration</h3>
                <span class="tag">LoRaWAN</span>
                <span class="tag">ChirpStack</span>
                <span class="tag"><img src="https://cdn.simpleicons.org/mqtt/4591ba" alt="MQTT"> MQTT</span>
                <span class="tag">🔌 RS485</span>
                <span class="tag"><img src="https://cdn.simpleicons.org/fastapi/4591ba" alt="API"> REST API</span>
                <span class="tag">📡 Sensor Decoders</span>
            </div>
            <div class="card">
                <h3>Databases</h3>
                <span class="tag"><i class="devicon-mysql-plain"></i> MySQL / MariaDB</span>
                <span class="tag"><i class="devicon-mongodb-plain"></i> MongoDB</span>
                <span class="tag"><i class="devicon-postgresql-plain"></i> PostgreSQL</span>
                <span class="tag"><i class="devicon-redis-plain"></i> Redis</span>
                <span class="tag"><i class="devicon-oracle-original"></i> Oracle</span>
                <span class="tag"><img src="https://cdn.simpleicons.org/erpnext/4591ba" alt="ERPNext"> ERPNext (Frappe)</span>
            </div>
            <div class="card">
                <h3>Tools & Platforms</h3>
                <span class="tag"><i class="devicon-grafana-original"></i> Grafana</span>
                <span class="tag"><i class="devicon-docker-plain"></i> Docker</span>
                <span class="tag"><i class="devicon-ubuntu-plain"></i> Linux (Ubuntu)</span>
                <span class="tag"><i class="devicon-digitalocean-plain"></i> DigitalOcean</span>
                <span class="tag"><i class="devicon-amazonwebservices-plain-wordmark"></i> AWS EC2</span>
                <span class="tag"><i class="devicon-amazonwebservices-plain-wordmark"></i> AWS RDS</span>
                <span class="tag"><i class="devicon-nginx-original"></i> Nginx</span>
            </div>
        </div>
    </section>

    <section id="projects">
        <h2>Projects</h2>
        
        <h3 class="year-header">2024</h3>
        <div class="grid">
            <div class="card">
                <h3>IoT DB Breaker Monitoring & Control System</h3>
                <p>
                    Built WiFi + MQTT-based breaker monitoring system with real-time monitoring and control capabilities.
                </p>
                <p><strong>Tech:</strong> Python, Django, MQTT, WiFi, Sensor Data Decoding</p>
            </div>
            <div class="card">
                <h3>Electronic Complaint Perlis System</h3>
                <p>
                    Full-stack complaint management system with web and mobile interfaces. Supports complaint submission, 
                    tracking, and comprehensive admin workflows.
                </p>
                <p><strong>Tech:</strong> Django, React Native, REST API, MySQL</p>
            </div>
            <div class="card">
                <h3>Smart Streetlight Monitoring System Upgrade</h3>
                <p>
                    Upgraded legacy system with modern React.js frontend and ERPNext backend integration. 
                    Improved scalability with Docker deployment.
                </p>
                <p><strong>Tech:</strong> React.js, ERPNext, MySQL, Redis, MongoDB, Docker</p>
            </div>
        </div>

        <h3 class="year-header">2023</h3>
        <div class="grid">
            <div class="card">
                <h3>ERPNext Evaluation & Exploration</h3>
                <p>
                    Explored and evaluated ERPNext framework for backend operations and system architecture.
                </p>
                <p><strong>Tech:</strong> ERPNext, Python, Frappe Framework</p>
            </div>
        </div>

        <h3 class="year-header">2022</h3>
        <div class="grid">
            <div class="card">
                <h3>Displacement Sensor Monitoring System</h3>
                <p>
                    Implemented RS485 serial communication system for SIRIM sensor testing. Built Python 
                    decoder and Django web interface for real-time monitoring.
                </p>
                <p><strong>Tech:</strong> Python, Django, RS485, Serial Communication</p>
            </div>
        </div>

        <h3 class="year-header">2021</h3>
        <div class="grid">
            <div class="card">
                <h3>Mangrove Ecosystem Monitoring Web System (MEITA)</h3>
                <p>
                    Comprehensive ecosystem monitoring system with LoRaWAN integration. Implemented weather 
                    station and water level monitoring with real-time dashboards.
                </p>
                <p><strong>Tech:</strong> LoRaWAN, ChirpStack, Django, Grafana, Weather Station Sensors</p>
            </div>
            <div class="card">
                <h3>Smart Streetlight Monitoring Mobile App</h3>
                <p>
                    Developed cross-platform mobile application for streetlight monitoring. Connected to 
                    in-house Django REST API for real-time data access.
                </p>
                <p><strong>Tech:</strong> React Native, Django REST API, Mobile Development</p>
            </div>
        </div>

        <h3 class="year-header">2020</h3>
        <div class="grid">
            <div class="card">
                <h3>Smart Attendance System (Hadir)</h3>
                <p>
                    Developed attendance system integrating temperature scanner and Android face detection. 
                    Built full-stack solution with Django and deployed on DigitalOcean with Docker.
                </p>
                <p><strong>Tech:</strong> Django, Android, Face Detection, Temperature Scanner, MySQL, MongoDB, Docker, DigitalOcean</p>
            </div>
            <div class="card">
                <h3>Server Room Monitoring (Hospital Tunku Azizah)</h3>
                <p>
                    LoRaWAN-based server room monitoring system. Integrated sensors with ChirpStack and 
                    developed Python decoders for telemetry data with Django + Grafana dashboards.
                </p>
                <p><strong>Tech:</strong> LoRaWAN, ChirpStack, Python, Django, Grafana, Sensor Integration</p>
            </div>
            <div class="card">
                <h3>Indoor Air Quality Monitoring (Multiple Hospitals)</h3>
                <p>
                    Comprehensive air quality monitoring system integrating CO₂, temperature, humidity, and 
                    pressure sensors. Developed Python decoders and Django dashboards for multiple hospital deployments.
                </p>
                <p><strong>Tech:</strong> Python, Django, CO₂ Sensors, Temperature/Humidity Sensors, Pressure Sensors</p>
            </div>
        </div>

        <h3 class="year-header">2019</h3>
        <div class="grid">
            <div class="card">
                <h3>Smart Street Light Monitoring Web System (Lightsol)</h3>
                <p>
                    Complete web system for monitoring and controlling street lights. Integrated LoRaWAN 
                    using ChirpStack with full-stack Django application and multi-database architecture.
                </p>
                <p><strong>Tech:</strong> Django, LoRaWAN, ChirpStack, MySQL, MongoDB, Redis, PostgreSQL, MQTT</p>
            </div>
            <div class="card">
                <h3>Smart Traffic Light Monitoring Web System</h3>
                <p>
                    Monitoring system for traffic light controllers via MQTT protocol. Developed Django-based 
                    frontend and backend with multi-database support and Redis caching.
                </p>
                <p><strong>Tech:</strong> Django, MQTT, MySQL, MongoDB, Redis</p>
            </div>
            <div class="card">
                <h3>Peatland Monitoring System (NICT)</h3>
                <p>
                    Integrated multiple sensors including weather station, temperature/humidity, and water level 
                    sensors. Developed Python decoders for LoRa sensor payloads with Django + Grafana dashboards.
                </p>
                <p><strong>Tech:</strong> Python, Django, LoRa, Grafana, Weather Station, Temperature/Humidity Sensors, Water Level Sensors</p>
            </div>
        </div>
    </section>

    <section id="contact">
        <h2>Contact</h2>
        <p>Email: <a href="mailto:muhdrusydiszli@gmail.com">muhdrusydiszli@gmail.com</a></p>
        <p>GitHub: <a href="https://github.com/rusydi101" target="_blank">github.com/rusydi101</a></p>
        <p>LinkedIn: <a href="https://www.linkedin.com/in/rusydi-sazali" target="_blank">www.linkedin.com/in/rusydi-sazali</a></p>
    </section>

    <footer>
        © 2025 Muhammad Rusydi Bin Sazali • Built for GitHub Pages
    </footer>

    <button class="scroll-top" id="scrollTop" aria-label="Scroll to top">↑</button>

    <script>
        // Intersection Observer for scroll animations
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

        // Wait for DOM to load
        document.addEventListener('DOMContentLoaded', () => {
            // Observe all cards for animation
            const cards = document.querySelectorAll('.grid .card');
            cards.forEach(card => observer.observe(card));

            // Observe year headers
            const yearHeaders = document.querySelectorAll('.year-header');
            yearHeaders.forEach(header => observer.observe(header));

            // Smooth scroll for navigation links
            document.querySelectorAll('nav a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    const target = document.querySelector(this.getAttribute('href'));
                    if (target) {
                        target.scrollIntoView({
                            behavior: 'smooth',
                            block: 'start'
                        });
                    }
                });
            });

            // Scroll to top button functionality
            const scrollTopBtn = document.getElementById('scrollTop');
            
            window.addEventListener('scroll', () => {
                if (window.pageYOffset > 300) {
                    scrollTopBtn.classList.add('visible');
                } else {
                    scrollTopBtn.classList.remove('visible');
                }
            });

            scrollTopBtn.addEventListener('click', () => {
                window.scrollTo({
                    top: 0,
                    behavior: 'smooth'
                });
            });

            // Add hover effect to cards - slight tilt on mouse move
            cards.forEach(card => {
                card.addEventListener('mousemove', (e) => {
                    const rect = card.getBoundingClientRect();
                    const x = e.clientX - rect.left;
                    const y = e.clientY - rect.top;
                    
                    const centerX = rect.width / 2;
                    const centerY = rect.height / 2;
                    
                    const rotateX = (y - centerY) / 20;
                    const rotateY = (centerX - x) / 20;
                    
                    card.style.transform = `perspective(1000px) rotateX(${rotateX}deg) rotateY(${rotateY}deg) translateY(-8px) scale(1.02)`;
                });
                
                card.addEventListener('mouseleave', () => {
                    card.style.transform = '';
                });
            });

            // Animate tags on hover with random delay
            const tags = document.querySelectorAll('.tag');
            tags.forEach((tag, index) => {
                tag.style.animationDelay = `${index * 0.05}s`;
            });

            // Add typing effect to header (optional - subtle)
            const headerText = document.querySelector('header h1');
            if (headerText) {
                headerText.style.opacity = '1';
            }
        });

        // Performance-optimized scroll handler
        let ticking = false;
        window.addEventListener('scroll', () => {
            if (!ticking) {
                window.requestAnimationFrame(() => {
                    // Additional scroll-based animations can go here
                    ticking = false;
                });
                ticking = true;
            }
        });
    </script>

</body>

</html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Freelance Services | Muhammad Rusydi</title>
    <meta name="description" content="Freelance software development — Django, React, IoT monitoring, ERPNext, cloud deployment, and system integration. Contact for a quote." />
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

        header h2 {
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
            from { opacity: 0; }
            to { opacity: 1; }
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
            to { width: 100%; }
        }

        .intro {
            color: var(--muted);
            max-width: 720px;
        }

        .grid {
            display: grid;
            gap: 1.5rem;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
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

        .card ul {
            margin: 0.75rem 0 0;
            padding-left: 1.25rem;
            color: var(--muted);
            font-size: 0.95rem;
        }

        .card ul li {
            margin-bottom: 0.35rem;
        }

        .quote-cta {
            display: inline-block;
            margin-top: 1rem;
            padding: 0.5rem 1rem;
            background: rgba(69, 145, 186, .2);
            border-radius: 999px;
            font-size: 0.9rem;
            font-weight: 500;
            color: var(--accent);
            transition: all 0.3s ease;
        }

        .quote-cta:hover {
            background: var(--accent);
            color: var(--bg);
        }

        .quote-cta::after {
            display: none;
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
        }

        .tag img {
            width: 16px;
            height: 16px;
            object-fit: contain;
        }

        .tag:hover {
            background: var(--accent);
            color: var(--bg);
            transform: translateY(-2px);
        }

        .tag:hover i {
            color: var(--bg);
        }

        .proof-list {
            list-style: none;
            padding: 0;
            margin: 0;
            display: grid;
            gap: 0.75rem;
        }

        .proof-list li {
            background: var(--card);
            padding: 1rem 1.25rem;
            border-radius: 10px;
            color: var(--muted);
            border-left: 3px solid var(--accent);
        }

        .proof-list strong {
            color: var(--text);
            display: block;
            margin-bottom: 0.25rem;
        }

        .process-grid {
            display: grid;
            gap: 1rem;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
        }

        .process-step {
            background: var(--card);
            padding: 1.25rem;
            border-radius: 14px;
            text-align: center;
        }

        .process-step .step-num {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 2rem;
            height: 2rem;
            border-radius: 50%;
            background: var(--accent);
            color: var(--bg);
            font-weight: 700;
            margin-bottom: 0.5rem;
        }

        .process-step h3 {
            margin: 0 0 0.5rem;
            font-size: 1.05rem;
        }

        .process-step p {
            margin: 0;
            color: var(--muted);
            font-size: 0.9rem;
        }

        .contact-cta {
            background: var(--card);
            padding: 1.5rem;
            border-radius: 14px;
            margin-top: 1rem;
            text-align: center;
        }

        .contact-cta a.primary {
            display: inline-block;
            margin-top: 0.75rem;
            padding: 0.75rem 1.5rem;
            background: var(--accent);
            color: var(--bg);
            border-radius: 999px;
            font-weight: 600;
        }

        .contact-cta a.primary:hover {
            color: var(--bg);
            transform: translateY(-2px);
            box-shadow: 0 8px 20px rgba(69, 145, 186, 0.35);
        }

        .contact-cta a.primary::after {
            display: none;
        }

        footer {
            text-align: center;
            padding: 2rem 1.5rem;
            color: var(--muted);
            font-size: .9rem;
            animation: fadeIn 1s ease-out 1.5s backwards;
        }

        .fade-in-scroll {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.6s ease-out, transform 0.6s ease-out;
        }

        .fade-in-scroll.visible {
            opacity: 1;
            transform: translateY(0);
        }

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
        .grid .card:nth-child(2).visible { transition-delay: 0.15s; }
        .grid .card:nth-child(3).visible { transition-delay: 0.2s; }
        .grid .card:nth-child(4).visible { transition-delay: 0.25s; }
        .grid .card:nth-child(5).visible { transition-delay: 0.3s; }
        .grid .card:nth-child(6).visible { transition-delay: 0.35s; }
        .grid .card:nth-child(7).visible { transition-delay: 0.4s; }

        section a:not(nav a) {
            color: var(--accent);
        }

        section a:not(nav a):not(.quote-cta):not(.primary) {
            position: relative;
        }

        section a:not(nav a):not(.quote-cta):not(.primary)::after {
            content: '';
            position: absolute;
            bottom: -2px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--accent);
            transition: width 0.3s ease;
        }

        section a:not(nav a):not(.quote-cta):not(.primary):hover::after {
            width: 100%;
        }

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

        @media (max-width: 768px) {
            header h2 {
                font-size: 1.8rem;
            }

            nav a {
                padding: 0.6rem 1rem;
                font-size: 0.9rem;
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
        <h2>Freelance &amp; Consulting</h2>
        <p>Muhammad Rusydi Bin Sazali — Software Developer • ERP &amp; Cloud Engineer</p>
        <p>Available for contract and project-based work. End-to-end delivery from sensors and APIs to web, mobile, and cloud.</p>
        <nav>
            <a href="index.html">🏠 Portfolio</a>
            <a href="#services">💼 Services</a>
            <a href="#experience">✅ Experience</a>
            <a href="#process">🔄 Process</a>
            <a href="#contact">📧 Contact</a>
        </nav>
    </header>

    <section id="services">
        <h2>Services</h2>
        <p class="intro">Below are the kinds of freelance work I take on, based on 6+ years building IoT, government, and enterprise systems. Every engagement is scoped to your needs—contact me for a quote.</p>
        <div class="grid">
            <div class="card">
                <h3>Custom Web Applications</h3>
                <p>Full-stack web apps with admin workflows, reporting, and secure access for teams and the public.</p>
                <ul>
                    <li>Requirements and architecture planning</li>
                    <li>Backend APIs and admin panels</li>
                    <li>Responsive web frontends</li>
                </ul>
                <span class="tag"><i class="devicon-python-plain"></i> Python</span>
                <span class="tag"><i class="devicon-django-plain"></i> Django</span>
                <span class="tag"><i class="devicon-react-original"></i> React.js</span>
                <span class="tag"><i class="devicon-mysql-plain"></i> MySQL</span>
                <p><a class="quote-cta" href="mailto:muhdrusydiszli@gmail.com?subject=Freelance%20inquiry%20-%20Web%20Applications">Get a quote</a></p>
            </div>
            <div class="card">
                <h3>Mobile Apps</h3>
                <p>Cross-platform mobile apps connected to your existing or new backend via REST APIs.</p>
                <ul>
                    <li>iOS and Android from one codebase</li>
                    <li>Real-time data and offline-friendly flows</li>
                    <li>Integration with Django or third-party APIs</li>
                </ul>
                <span class="tag"><i class="devicon-react-original"></i> React Native</span>
                <span class="tag"><img src="https://cdn.simpleicons.org/fastapi/4591ba" alt="API"> REST API</span>
                <span class="tag"><i class="devicon-django-plain"></i> Django</span>
                <p><a class="quote-cta" href="mailto:muhdrusydiszli@gmail.com?subject=Freelance%20inquiry%20-%20Mobile%20Apps">Get a quote</a></p>
            </div>
            <div class="card">
                <h3>IoT Monitoring &amp; Control</h3>
                <p>Connect sensors and devices over LoRaWAN, MQTT, WiFi, or RS485—with decoding, storage, and live dashboards.</p>
                <ul>
                    <li>Payload decoders and device onboarding</li>
                    <li>Monitoring and remote control features</li>
                    <li>Alerts and historical telemetry</li>
                </ul>
                <span class="tag">LoRaWAN</span>
                <span class="tag">ChirpStack</span>
                <span class="tag"><img src="https://cdn.simpleicons.org/mqtt/4591ba" alt="MQTT"> MQTT</span>
                <span class="tag">🔌 RS485</span>
                <span class="tag"><i class="devicon-python-plain"></i> Python</span>
                <p><a class="quote-cta" href="mailto:muhdrusydiszli@gmail.com?subject=Freelance%20inquiry%20-%20IoT">Get a quote</a></p>
            </div>
            <div class="card">
                <h3>ERPNext Implementation</h3>
                <p>Deploy and customize ERPNext (Frappe) for operations, or integrate it with existing monitoring and field systems.</p>
                <ul>
                    <li>Module setup and custom DocTypes</li>
                    <li>Legacy system migration paths</li>
                    <li>API bridges to external apps</li>
                </ul>
                <span class="tag"><img src="https://cdn.simpleicons.org/erpnext/4591ba" alt="ERPNext"> ERPNext</span>
                <span class="tag"><i class="devicon-python-plain"></i> Frappe</span>
                <p><a class="quote-cta" href="mailto:muhdrusydiszli@gmail.com?subject=Freelance%20inquiry%20-%20ERPNext">Get a quote</a></p>
            </div>
            <div class="card">
                <h3>Cloud Deployment &amp; DevOps</h3>
                <p>Production-ready hosting on Linux cloud VMs with containers, reverse proxy, and managed databases.</p>
                <ul>
                    <li>Dockerized app stacks</li>
                    <li>Nginx, SSL, and server hardening basics</li>
                    <li>AWS EC2/RDS or DigitalOcean setups</li>
                </ul>
                <span class="tag"><i class="devicon-docker-plain"></i> Docker</span>
                <span class="tag"><i class="devicon-nginx-original"></i> Nginx</span>
                <span class="tag"><i class="devicon-ubuntu-plain"></i> Linux</span>
                <span class="tag"><i class="devicon-amazonwebservices-plain-wordmark"></i> AWS</span>
                <span class="tag"><i class="devicon-digitalocean-plain"></i> DigitalOcean</span>
                <p><a class="quote-cta" href="mailto:muhdrusydiszli@gmail.com?subject=Freelance%20inquiry%20-%20Cloud%20DevOps">Get a quote</a></p>
            </div>
            <div class="card">
                <h3>Dashboards &amp; Observability</h3>
                <p>Visualize sensor and business metrics with Grafana and custom Django dashboards for operators and management.</p>
                <ul>
                    <li>Panel design and data source wiring</li>
                    <li>Environmental and facility monitoring views</li>
                    <li>Export and reporting hooks</li>
                </ul>
                <span class="tag"><i class="devicon-grafana-original"></i> Grafana</span>
                <span class="tag"><i class="devicon-django-plain"></i> Django</span>
                <p><a class="quote-cta" href="mailto:muhdrusydiszli@gmail.com?subject=Freelance%20inquiry%20-%20Dashboards">Get a quote</a></p>
            </div>
            <div class="card">
                <h3>API &amp; System Integration</h3>
                <p>Connect disparate systems—databases, hardware, and third-party services—into one reliable data flow.</p>
                <ul>
                    <li>REST API design and documentation</li>
                    <li>Multi-database and caching strategies</li>
                    <li>Legacy upgrades without full rewrites</li>
                </ul>
                <span class="tag"><img src="https://cdn.simpleicons.org/fastapi/4591ba" alt="API"> REST API</span>
                <span class="tag"><i class="devicon-mongodb-plain"></i> MongoDB</span>
                <span class="tag"><i class="devicon-redis-plain"></i> Redis</span>
                <span class="tag"><i class="devicon-postgresql-plain"></i> PostgreSQL</span>
                <p><a class="quote-cta" href="mailto:muhdrusydiszli@gmail.com?subject=Freelance%20inquiry%20-%20Integration">Get a quote</a></p>
            </div>
        </div>
    </section>

    <section id="experience">
        <h2>Relevant Work</h2>
        <p class="intro">Selected projects from my portfolio that reflect the services above.</p>
        <ul class="proof-list fade-in-scroll">
            <li><strong>IoT &amp; control</strong> IoT DB Breaker Monitoring, Smart Street Light (Lightsol), Smart Traffic Light, Server Room Monitoring (HTA), Indoor Air Quality (hospitals), MEITA mangrove monitoring, Peatland (NICT), Displacement Sensor (SIRIM)</li>
            <li><strong>Web &amp; mobile</strong> Electronic Complaint Perlis System, Smart Attendance (Hadir), Smart Streetlight Mobile App</li>
            <li><strong>ERP &amp; upgrades</strong> Smart Streetlight Monitoring System Upgrade (React + ERPNext), ERPNext Evaluation &amp; Exploration</li>
            <li><strong>Cloud</strong> Docker and DigitalOcean production deployments (e.g. Hadir attendance system)</li>
        </ul>
    </section>

    <section id="process">
        <h2>How It Works</h2>
        <div class="process-grid">
            <div class="process-step fade-in-scroll">
                <span class="step-num">1</span>
                <h3>Discovery</h3>
                <p>We discuss goals, constraints, and existing systems—no commitment required.</p>
            </div>
            <div class="process-step fade-in-scroll">
                <span class="step-num">2</span>
                <h3>Scope &amp; quote</h3>
                <p>You receive a clear scope, timeline, and fixed or milestone-based quote.</p>
            </div>
            <div class="process-step fade-in-scroll">
                <span class="step-num">3</span>
                <h3>Build</h3>
                <p>Iterative development with updates; IoT and integration tested against real devices where needed.</p>
            </div>
            <div class="process-step fade-in-scroll">
                <span class="step-num">4</span>
                <h3>Handoff</h3>
                <p>Deployment, documentation, and optional support for fixes or enhancements.</p>
            </div>
        </div>
    </section>

    <section id="contact">
        <h2>Contact</h2>
        <div class="contact-cta">
            <p><strong>Email me to discuss your project.</strong> Share a short brief and I will reply with next steps and a quote.</p>
            <a class="primary" href="mailto:muhdrusydiszli@gmail.com?subject=Freelance%20inquiry">muhdrusydiszli@gmail.com</a>
        </div>
        <p style="margin-top: 1.5rem;">GitHub: <a href="https://github.com/rusydi101" target="_blank" rel="noopener">github.com/rusydi101</a></p>
        <p>LinkedIn: <a href="https://www.linkedin.com/in/rusydi-sazali" target="_blank" rel="noopener">www.linkedin.com/in/rusydi-sazali</a></p>
        <p>Full portfolio: <a href="index.html">rusydi101.github.io</a></p>
    </section>

    <footer>
        © 2026 Muhammad Rusydi Bin Sazali • Built for GitHub Pages
    </footer>

    <button class="scroll-top" id="scrollTop" aria-label="Scroll to top">↑</button>

    <script>
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

        document.addEventListener('DOMContentLoaded', () => {
            const cards = document.querySelectorAll('.grid .card');
            cards.forEach(card => observer.observe(card));

            document.querySelectorAll('.fade-in-scroll').forEach(el => observer.observe(el));

            document.querySelectorAll('nav a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    const target = document.querySelector(this.getAttribute('href'));
                    if (target) {
                        target.scrollIntoView({ behavior: 'smooth', block: 'start' });
                    }
                });
            });

            const scrollTopBtn = document.getElementById('scrollTop');
            window.addEventListener('scroll', () => {
                if (window.pageYOffset > 300) {
                    scrollTopBtn.classList.add('visible');
                } else {
                    scrollTopBtn.classList.remove('visible');
                }
            });

            scrollTopBtn.addEventListener('click', () => {
                window.scrollTo({ top: 0, behavior: 'smooth' });
            });

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
        });
    </script>

</body>

</html>

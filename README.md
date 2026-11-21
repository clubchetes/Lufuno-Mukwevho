
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="theme-color" content="#080611">

    <title>Lufuno Mukwevho | Software Developer</title>

    <meta name="description" content="Lufuno Mukwevho - Software Development Graduate, Cisco and AWS certified, available for software development and IT opportunities.">

    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=JetBrains+Mono:wght@400;500;700&display=swap" rel="stylesheet">

    <style>
        :root {
            --background: #080611;
            --surface: #100d1d;
            --surface-light: #171228;
            --purple: #9333ea;
            --violet: #a855f7;
            --light-purple: #c4b5fd;
            --white: #f8f7ff;
            --muted: #aaa4bc;
            --border: rgba(168, 85, 247, 0.19);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            background: var(--background);
            color: var(--white);
            font-family: 'Inter', sans-serif;
            overflow-x: hidden;
            line-height: 1.7;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        .container {
            width: min(1120px, 90%);
            margin: auto;
        }

        /* Animated background */

        .background-effects {
            position: fixed;
            inset: 0;
            z-index: -2;
            overflow: hidden;
            pointer-events: none;
        }

        .orb {
            position: absolute;
            width: 400px;
            height: 400px;
            border-radius: 50%;
            filter: blur(110px);
            opacity: .19;
            animation: float 12s ease-in-out infinite alternate;
        }

        .orb.one {
            background: #7e22ce;
            top: -150px;
            left: -150px;
        }

        .orb.two {
            background: #4c1d95;
            right: -150px;
            top: 35%;
            animation-delay: -5s;
        }

        .orb.three {
            background: #9333ea;
            bottom: -250px;
            left: 35%;
            animation-delay: -8s;
        }

        @keyframes float {
            from {
                transform: translate(0, 0) scale(1);
            }
            to {
                transform: translate(70px, 50px) scale(1.25);
            }
        }

        /* Navigation */

        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 100;
            background: rgba(8, 6, 17, .85);
            backdrop-filter: blur(18px);
            border-bottom: 1px solid var(--border);
        }

        nav {
            min-height: 75px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-family: 'JetBrains Mono', monospace;
            font-weight: 700;
            color: var(--light-purple);
            font-size: 19px;
        }

        .logo span {
            color: var(--violet);
        }

        .nav-links {
            display: flex;
            align-items: center;
            gap: 27px;
            list-style: none;
        }

        .nav-links a {
            color: var(--muted);
            font-size: 13px;
            transition: .3s;
        }

        .nav-links a:hover {
            color: var(--light-purple);
        }

        .menu-toggle {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 25px;
            cursor: pointer;
        }

        /* Hero */

        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding: 120px 0 75px;
            position: relative;
        }

        .hero-content {
            max-width: 850px;
        }

        .availability {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            padding: 9px 15px;
            border: 1px solid var(--border);
            border-radius: 30px;
            color: var(--light-purple);
            background: rgba(147, 51, 234, .09);
            font-size: 12px;
            margin-bottom: 30px;
        }

        .status-dot {
            width: 8px;
            height: 8px;
            background: #22c55e;
            border-radius: 50%;
            box-shadow: 0 0 12px #22c55e;
            animation: pulse 1.8s infinite;
        }

        @keyframes pulse {
            50% { opacity: .3; }
        }

        .eyebrow {
            color: var(--violet);
            font-family: 'JetBrains Mono', monospace;
            font-size: 14px;
            margin-bottom: 12px;
        }

        h1 {
            font-size: clamp(42px, 8vw, 78px);
            line-height: 1.1;
            letter-spacing: -3px;
            margin-bottom: 18px;
        }

        .gradient-text {
            background: linear-gradient(90deg, #c4b5fd, #a855f7, #7c3aed);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        .role {
            font-family: 'JetBrains Mono', monospace;
            font-size: clamp(17px, 3vw, 23px);
            color: var(--light-purple);
            min-height: 38px;
            margin-bottom: 23px;
        }

        .cursor {
            animation: blink .8s infinite;
        }

        @keyframes blink {
            50% { opacity: 0; }
        }

        .hero-description {
            max-width: 690px;
            color: var(--muted);
            font-size: 16px;
            margin-bottom: 32px;
        }

        .buttons {
            display: flex;
            gap: 14px;
            flex-wrap: wrap;
        }

        .btn {
            display: inline-flex;
            justify-content: center;
            align-items: center;
            gap: 9px;
            padding: 13px 23px;
            border-radius: 8px;
            font-size: 13px;
            font-weight: 700;
            transition: .3s;
            border: 1px solid var(--border);
        }

        .btn-primary {
            background: linear-gradient(110deg, #7e22ce, #9333ea);
            color: white;
            box-shadow: 0 8px 30px rgba(147, 51, 234, .2);
        }

        .btn-secondary {
            background: var(--surface);
            color: var(--white);
        }

        .btn:hover {
            transform: translateY(-4px);
            box-shadow: 0 10px 30px rgba(147, 51, 234, .25);
        }

        .scroll-indicator {
            margin-top: 65px;
            color: #777087;
            font-family: 'JetBrains Mono', monospace;
            font-size: 11px;
            letter-spacing: 2px;
        }

        /* General sections */

        section {
            padding: 100px 0;
            scroll-margin-top: 75px;
        }

        .section-label {
            font-family: 'JetBrains Mono', monospace;
            color: var(--violet);
            font-size: 12px;
            margin-bottom: 10px;
        }

        .section-title {
            font-size: clamp(28px, 5vw, 42px);
            letter-spacing: -1.5px;
            margin-bottom: 16px;
        }

        .section-description {
            color: var(--muted);
            max-width: 650px;
            margin-bottom: 40px;
            font-size: 14px;
        }

        /* About */

        .about-grid {
            display: grid;
            grid-template-columns: 1.4fr .8fr;
            gap: 35px;
        }

        .panel {
            background: rgba(16, 13, 29, .85);
            border: 1px solid var(--border);
            border-radius: 15px;
            padding: 30px;
            transition: .3s;
        }

        .panel:hover {
            border-color: rgba(168, 85, 247, .55);
            transform: translateY(-5px);
        }

        .panel p {
            color: var(--muted);
            font-size: 14px;
            margin-bottom: 16px;
        }

        .details {
            list-style: none;
            margin-top: 22px;
        }

        .details li {
            padding: 11px 0;
            border-bottom: 1px solid rgba(255,255,255,.06);
            font-size: 13px;
        }

        .details strong {
            color: var(--light-purple);
        }

        .quick-info {
            display: grid;
            gap: 15px;
        }

        .info-item {
            padding: 19px;
            border-radius: 10px;
            background: var(--surface-light);
            border: 1px solid var(--border);
        }

        .info-item small {
            color: var(--muted);
            display: block;
            font-size: 11px;
            margin-bottom: 5px;
        }

        .info-item strong {
            font-size: 14px;
        }

        /* Skills */

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
        }

        .skill-card {
            background: var(--surface);
            border: 1px solid var(--border);
            padding: 25px;
            border-radius: 12px;
            transition: .3s;
        }

        .skill-card:hover {
            transform: translateY(-6px);
            border-color: var(--violet);
        }

        .skill-card h3 {
            font-size: 15px;
            margin-bottom: 17px;
            color: var(--light-purple);
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 9px;
        }

        .tag {
            font-size: 11px;
            color: #ddd6fe;
            background: rgba(147, 51, 234, .12);
            border: 1px solid var(--border);
            padding: 7px 10px;
            border-radius: 5px;
        }

        /* Certifications */

        .cert-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
        }

        .cert-card {
            display: flex;
            align-items: center;
            gap: 20px;
            padding: 25px;
            border-radius: 13px;
            background: var(--surface);
            border: 1px solid var(--border);
            transition: .3s;
        }

        .cert-card:hover {
            transform: translateY(-5px);
            border-color: var(--violet);
        }

        .cert-icon {
            min-width: 55px;
            height: 55px;
            display: grid;
            place-items: center;
            border-radius: 12px;
            background: rgba(147, 51, 234, .16);
            color: var(--light-purple);
            font-size: 25px;
            font-weight: 800;
        }

        .cert-card h3 {
            font-size: 16px;
            margin-bottom: 4px;
        }

        .cert-card p {
            color: var(--muted);
            font-size: 12px;
        }

        /* Projects */

        .project-card {
            background: linear-gradient(140deg, #151027, #0d0a18);
            border: 1px solid var(--border);
            border-radius: 15px;
            padding: 35px;
            transition: .3s;
        }

        .project-card:hover {
            transform: translateY(-5px);
            border-color: var(--violet);
        }

        .project-top {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 15px;
            margin-bottom: 20px;
        }

        .project-number {
            color: var(--violet);
            font-family: 'JetBrains Mono', monospace;
            font-size: 13px;
        }

        .project-card h3 {
            font-size: 23px;
            margin-bottom: 12px;
        }

        .project-card p {
            color: var(--muted);
            font-size: 14px;
            max-width: 800px;
        }

        .feature-list {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 12px;
            list-style: none;
            margin: 25px 0;
        }

        .feature-list li {
            font-size: 12px;
            color: #d5cde6;
        }

        .feature-list li::before {
            content: "▹ ";
            color: var(--violet);
        }

        /* Education */

        .education-card {
            border-left: 3px solid var(--violet);
            padding: 8px 25px;
            background: linear-gradient(90deg, rgba(147,51,234,.09), transparent);
        }

        .education-card h3 {
            font-size: 19px;
            margin-bottom: 8px;
        }

        .education-card p {
            font-size: 13px;
            color: var(--muted);
        }

        /* Opportunity */

        .opportunity {
            text-align: center;
            padding: 55px 35px;
            border: 1px solid var(--border);
            border-radius: 17px;
            background:
                radial-gradient(ellipse at top, rgba(147,51,234,.2), transparent 65%),
                var(--surface);
        }

        .opportunity h2 {
            font-size: clamp(27px, 5vw, 39px);
            margin-bottom: 16px;
        }

        .opportunity p {
            max-width: 700px;
            margin: 0 auto 25px;
            color: var(--muted);
            font-size: 14px;
        }

        .opportunity-tags {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 10px;
            margin-bottom: 28px;
        }

        /* Contact */

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 18px;
        }

        .contact-card {
            background: var(--surface);
            border: 1px solid var(--border);
            padding: 23px;
            border-radius: 10px;
            transition: .3s;
        }

        .contact-card:hover {
            border-color: var(--violet);
            transform: translateY(-4px);
        }

        .contact-card small {
            color: var(--muted);
            display: block;
            margin-bottom: 7px;
        }

        .contact-card strong {
            color: var(--light-purple);
            font-size: 14px;
        }

        footer {
            border-top: 1px solid var(--border);
            padding: 30px 0;
            text-align: center;
            color: var(--muted);
            font-size: 12px;
        }

        /* Scroll animations */

        .reveal {
            opacity: 0;
            transform: translateY(25px);
            transition: opacity .7s ease, transform .7s ease;
        }

        .reveal.visible {
            opacity: 1;
            transform: translateY(0);
        }

        .back-top {
            position: fixed;
            bottom: 25px;
            right: 25px;
            width: 43px;
            height: 43px;
            display: grid;
            place-items: center;
            background: var(--purple);
            border-radius: 9px;
            font-size: 20px;
            opacity: 0;
            visibility: hidden;
            transition: .3s;
            z-index: 90;
        }

        .back-top.show {
            opacity: 1;
            visibility: visible;
        }

        /* Responsive */

        @media(max-width: 800px) {
            .nav-links {
                display: none;
                position: absolute;
                top: 75px;
                left: 0;
                width: 100%;
                background: #100d1d;
                padding: 25px;
                flex-direction: column;
                border-bottom: 1px solid var(--border);
            }

            .nav-links.active {
                display: flex;
            }

            .menu-toggle {
                display: block;
            }

            .about-grid {
                grid-template-columns: 1fr;
            }

            .skills-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media(max-width: 550px) {
            section {
                padding: 75px 0;
            }

            .skills-grid,
            .cert-grid,
            .contact-grid,
            .feature-list {
                grid-template-columns: 1fr;
            }

            .hero {
                min-height: 90vh;
            }

            h1 {
                letter-spacing: -2px;
            }

            .panel,
            .project-card {
                padding: 22px;
            }

            .cert-card {
                align-items: flex-start;
            }
        }

        @media(prefers-reduced-motion: reduce) {
            *, *::before, *::after {
                animation-duration: .01ms !important;
                animation-iteration-count: 1 !important;
                scroll-behavior: auto !important;
                transition-duration: .01ms !important;
            }

            .reveal {
                opacity: 1;
                transform: none;
            }
        }
    </style>
</head>

<body>

<div class="background-effects">
    <div class="orb one"></div>
    <div class="orb two"></div>
    <div class="orb three"></div>
</div>

<header>
    <nav class="container">

        <a href="#home" class="logo">
            LM<span>.</span>
        </a>

        <button class="menu-toggle" id="menuToggle"
                aria-label="Toggle navigation" aria-expanded="false">
            ☰
        </button>

        <ul class="nav-links" id="navLinks">
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#certifications">Certifications</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#education">Education</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>

    </nav>
</header>

<main>

    <!-- HERO -->

    <section class="hero container" id="home">

        <div class="hero-content">

            <div class="availability">
                <span class="status-dot"></span>
                AVAILABLE FOR PROFESSIONAL OPPORTUNITIES
            </div>

            <p class="eyebrow">HELLO, I'M</p>

            <h1>
                Lufuno<br>
                <span class="gradient-text">Mukwevho.</span>
            </h1>

            <div class="role">
                <span id="typedRole"></span><span class="cursor">|</span>
            </div>

            <p class="hero-description">
                Software Development graduate with a passion for
                building practical technology solutions. I enjoy
                developing applications, working with databases and
                exploring technologies that solve real-world problems.
                I am ready to contribute, collaborate and grow within
                a professional technology environment.
            </p>

            <div class="buttons">

                <a href="#projects" class="btn btn-primary">
                    Explore My Projects →
                </a>

                <a href="#contact" class="btn btn-secondary">
                    Get In Touch
                </a>

                <a href="https://github.com/clubchetes"
                   target="_blank" rel="noopener"
                   class="btn btn-secondary">
                    GitHub ↗
                </a>

            </div>

            <div class="scroll-indicator">
                SCROLL TO EXPLORE ↓
            </div>

        </div>
    </section>

    <!-- ABOUT -->

    <section id="about">
        <div class="container reveal">

            <p class="section-label">01 / INTRODUCTION</p>
            <h2 class="section-title">About Me</h2>

            <p class="section-description">
                A software development professional focused on
                learning, problem-solving and building useful
                applications.
            </p>

            <div class="about-grid">

                <div class="panel">

                    <p>
                        I am Lufuno Mukwevho, an Information Technology
                        graduate specialising in Software Development
                        from Nelson Mandela University.
                    </p>

                    <p>
                        Through my academic work and software projects,
                        I have developed practical experience in
                        application development, database management,
                        programming and system design.
                    </p>

                    <p>
                        I am particularly interested in developing
                        reliable software, improving my technical
                        abilities and contributing to meaningful
                        technology projects.
                    </p>

                    <ul class="details">
                        <li><strong>Qualification:</strong> Diploma in Information Technology (Software Development)</li>
                        <li><strong>Institution:</strong> Nelson Mandela University</li>
                        <li><strong>Specialisation:</strong> Software Development</li>
                        <li><strong>Focus:</strong> Application Development and IT</li>
                        <li><strong>Professional Status:</strong> Graduate</li>
                    </ul>

                </div>

                <div class="quick-info">

                    <div class="info-item">
                        <small>PRIMARY SPECIALISATION</small>
                        <strong>Software Development</strong>
                    </div>

                    <div class="info-item">
                        <small>PROGRAMMING FOCUS</small>
                        <strong>C# & ASP.NET MVC</strong>
                    </div>

                    <div class="info-item">
                        <small>CLOUD KNOWLEDGE</small>
                        <strong>AWS</strong>
                    </div>

                    <div class="info-item">
                        <small>NETWORKING KNOWLEDGE</small>
                        <strong>Cisco</strong>
                    </div>

                </div>

            </div>
        </div>
    </section>

    <!-- SKILLS -->

    <section id="skills">
        <div class="container reveal">

            <p class="section-label">02 / TECHNICAL EXPERTISE</p>
            <h2 class="section-title">Technical Skills</h2>

            <p class="section-description">
                Technologies and development tools I have worked
                with through academic projects and practical learning.
            </p>

            <div class="skills-grid">

                <div class="skill-card">
                    <h3>Programming Languages</h3>
                    <div class="skill-tags">
                        <span class="tag">C#</span>
                        <span class="tag">Python</span>
                        <span class="tag">JavaScript</span>
                    </div>
                </div>

                <div class="skill-card">
                    <h3>Web Development</h3>
                    <div class="skill-tags">
                        <span class="tag">ASP.NET MVC</span>
                        <span class="tag">HTML5</span>
                        <span class="tag">CSS3</span>
                        <span class="tag">.NET</span>
                    </div>
                </div>

                <div class="skill-card">
                    <h3>Database Technologies</h3>
                    <div class="skill-tags">
                        <span class="tag">SQL Server</span>
                        <span class="tag">Entity Framework</span>
                        <span class="tag">Database Design</span>
                    </div>
                </div>

                <div class="skill-card">
                    <h3>Development Tools</h3>
                    <div class="skill-tags">
                        <span class="tag">Visual Studio</span>
                        <span class="tag">Git</span>
                        <span class="tag">GitHub</span>
                    </div>
                </div>

                <div class="skill-card">
                    <h3>Cloud & Infrastructure</h3>
                    <div class="skill-tags">
                        <span class="tag">AWS</span>
                        <span class="tag">Cloud Fundamentals</span>
                    </div>
                </div>

                <div class="skill-card">
                    <h3>Professional Skills</h3>
                    <div class="skill-tags">
                        <span class="tag">Problem Solving</span>
                        <span class="tag">System Design</span>
                        <span class="tag">Team Collaboration</span>
                        <span class="tag">Critical Thinking</span>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- CERTIFICATIONS -->

    <section id="certifications">
        <div class="container reveal">

            <p class="section-label">03 / PROFESSIONAL DEVELOPMENT</p>
            <h2 class="section-title">Certifications</h2>

            <p class="section-description">
                Additional learning and professional development
                through Cisco and Amazon Web Services.
            </p>

            <div class="cert-grid">

                <div class="cert-card">
                    <div class="cert-icon">C</div>
                    <div>
                        <h3>Cisco Certifications</h3>
                        <p>Networking and technology-related certification credentials.</p>
                    </div>
                </div>

                <div class="cert-card">
                    <div class="cert-icon">AWS</div>
                    <div>
                        <h3>AWS Certifications</h3>
                        <p>Amazon Web Services learning and certification credentials.</p>
                    </div>
                </div>

            </div>

        </div>
    </section>

    <!-- PROJECTS -->

    <section id="projects">
        <div class="container reveal">

            <p class="section-label">04 / SELECTED WORK</p>
            <h2 class="section-title">Featured Project</h2>

            <p class="section-description">
                An example of applying software development
                knowledge to a practical system.
            </p>

            <div class="project-card">

                <div class="project-top">
                    <span class="project-number">PROJECT_001</span>
                    <span class="tag">ASP.NET MVC</span>
                </div>

                <h3>ElderlyCareHospital</h3>

                <p>
                    A hospital management system developed to support
                    healthcare operations and improve the management
                    of hospital services. The application includes
                    role-based functionality for different hospital
                    users and operational processes.
                </p>

                <ul class="feature-list">
                    <li>Administrator dashboard</li>
                    <li>Patient management</li>
                    <li>Doctor and nurse management</li>
                    <li>Medication administration</li>
                    <li>Family member registration</li>
                    <li>Role-based authentication</li>
                    <li>Hospital operational management</li>
                    <li>Database-driven application functionality</li>
                </ul>

                <div class="skill-tags">
                    <span class="tag">C#</span>
                    <span class="tag">ASP.NET MVC</span>
                    <span class="tag">Entity Framework</span>
                    <span class="tag">SQL Server</span>
                    <span class="tag">HTML</span>
                    <span class="tag">CSS</span>
                    <span class="tag">JavaScript</span>
                </div>

                <br>

                <a href="https://github.com/clubchetes/ElderlyCareHospital"
                   target="_blank" rel="noopener"
                   class="btn btn-primary">
                    View Project on GitHub ↗
                </a>

            </div>

        </div>
    </section>

    <!-- EDUCATION -->

    <section id="education">
        <div class="container reveal">

            <p class="section-label">05 / ACADEMIC BACKGROUND</p>
            <h2 class="section-title">Education</h2>

            <div class="education-card">

                <h3>Diploma in Information Technology</h3>

                <p>Specialisation: Software Development</p>
                <p>Nelson Mandela University</p>
                <p>Graduate | 2026</p>

            </div>

        </div>
    </section>

    <!-- OPPORTUNITIES -->

    <section id="opportunities">
        <div class="container reveal">

            <div class="opportunity">

                <p class="section-label">06 / CAREER OPPORTUNITIES</p>

                <h2>
                    Ready for the next
                    <span class="gradient-text">opportunity.</span>
                </h2>

                <p>
                    I am actively seeking opportunities to apply my
                    knowledge, gain professional experience and
                    contribute to technology-driven organisations.
                </p>

                <div class="opportunity-tags">
                    <span class="tag">Software Development Internships</span>
                    <span class="tag">IT Internships</span>
                    <span class="tag">Learnerships</span>
                    <span class="tag">Junior Developer Roles</span>
                    <span class="tag">Graduate Programmes</span>
                    <span class="tag">Entry-Level IT Opportunities</span>
                </div>

                <a href="#contact" class="btn btn-primary">
                    Contact Me →
                </a>

            </div>

        </div>
    </section>

    <!-- CONTACT -->

    <section id="contact">
        <div class="container reveal">

            <p class="section-label">07 / LET'S CONNECT</p>
            <h2 class="section-title">Get In Touch</h2>

            <p class="section-description">
                Interested in my profile, projects or professional
                opportunities? Connect with me through the platforms
                below.
            </p>

            <div class="contact-grid">

                <a href="https://github.com/clubchetes"
                   target="_blank" rel="noopener"
                   class="contact-card">

                    <small>GITHUB PROFILE</small>
                    <strong>github.com/clubchetes ↗</strong>

                </a>

                <a href="https://www.linkedin.com/"
                   target="_blank" rel="noopener"
                   class="contact-card">

                    <small>LINKEDIN</small>
                    <strong>Connect professionally ↗</strong>

                </a>

            </div>

        </div>
    </section>

</main>

<footer>
    <div class="container">
        <p>© <span id="year"></span> Lufuno Mukwevho.</p>
        <p>Software Development | Technology | Innovation</p>
    </div>
</footer>

<a href="#home" class="back-top" id="backTop"
   aria-label="Back to top">↑</a>

<script>

    // Rotating professional titles

    const roles = [
        "Software Developer",
        "C# & ASP.NET MVC Developer",
        "Application Developer",
        "Technology Enthusiast",
        "Aspiring Cloud Professional"
    ];

    const typedRole = document.getElementById("typedRole");

    let roleIndex = 0;
    let characterIndex = 0;
    let deleting = false;

    function typeEffect() {

        const currentRole = roles[roleIndex];

        if (!deleting) {

            typedRole.textContent =
                currentRole.substring(0, characterIndex + 1);

            characterIndex++;

            if (characterIndex === currentRole.length) {
                deleting = true;
                setTimeout(typeEffect, 1700);
                return;
            }

        } else {

            typedRole.textContent =
                currentRole.substring(0, characterIndex - 1);

            characterIndex--;

            if (characterIndex === 0) {
                deleting = false;
                roleIndex = (roleIndex + 1) % roles.length;
            }

        }

        setTimeout(typeEffect, deleting ? 45 : 85);
    }

    typeEffect();


    // Mobile navigation

    const menuToggle = document.getElementById("menuToggle");
    const navLinks = document.getElementById("navLinks");

    menuToggle.addEventListener("click", () => {

        const isOpen = navLinks.classList.toggle("active");

        menuToggle.setAttribute("aria-expanded", isOpen);
        menuToggle.textContent = isOpen ? "✕" : "☰";

    });

    document.querySelectorAll(".nav-links a").forEach(link => {

        link.addEventListener("click", () => {
            navLinks.classList.remove("active");
            menuToggle.setAttribute("aria-expanded", "false");
            menuToggle.textContent = "☰";
        });

    });


    // Reveal sections when scrolling

    const revealElements = document.querySelectorAll(".reveal");

    if ("IntersectionObserver" in window) {

        const observer = new IntersectionObserver(entries => {

            entries.forEach(entry => {

                if (entry.isIntersecting) {
                    entry.target.classList.add("visible");
                    observer.unobserve(entry.target);
                }

            });

        }, {
            threshold: 0.12
        });

        revealElements.forEach(element => observer.observe(element));

    } else {

        revealElements.forEach(element => {
            element.classList.add("visible");
        });

    }


    // Back to top button

    const backTop = document.getElementById("backTop");

    window.addEventListener("scroll", () => {

        if (window.scrollY > 450) {
            backTop.classList.add("show");
        } else {
            backTop.classList.remove("show");
        }

    });


    // Automatically update copyright year

    document.getElementById("year").textContent =
        new Date().getFullYear();

</script>

</body>
</html>

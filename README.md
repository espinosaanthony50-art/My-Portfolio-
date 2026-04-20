<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Anthony Espinosa | IT Student & Developer</title>
    <link rel="stylesheet" href="style.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head>
<body>

<header>
    <nav>
        <div class="logo">AE<span>.</span></div>
        <ul>
            <li><a href="#about">About</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>
</header>

<section class="hero">
    <div class="hero-text">
        <h2>Hello, I'm <span>Anthony Espinosa</span></h2>
        <p>IT Student & Aspiring Full-Stack Developer</p>
        <p class="sub-text">Bridging the gap between academic theory and real-world code.</p>
        <div class="hero-btns">
            <a href="#projects" class="btn">View My Work</a>
            <a href="#contact" class="btn secondary">Get In Touch</a>
        </div>
    </div>
</section>

<section id="about">
    <div class="container">
        <h2>About Me</h2>
        <div class="about-content">
            <p>
                I am an **Information Technology student** passionate about building clean, functional web applications. 
                While my studies focus on systems and networking, my heart is in **Full-Stack Development**.
            </p>
            <p>
                I specialize in the **MERN stack** and enjoy turning complex problems into simple, user-friendly solutions. 
                I’m currently looking for opportunities to contribute to professional projects and grow as a developer.
            </p>
        </div>
    </div>
</section>

<section id="skills">
    <div class="container">
        <h2>Technical Toolbox</h2>
        <div class="skills-grid">
            <div class="skill-card">
                <i class="fas fa-code"></i>
                <h3>Frontend</h3>
                <p>HTML5, CSS3, JavaScript, React.js, Tailwind</p>
            </div>
            <div class="skill-card">
                <i class="fas fa-database"></i>
                <h3>Backend</h3>
                <p>Node.js, Python, MySQL, MongoDB</p>
            </div>
            <div class="skill-card">
                <i class="fas fa-tools"></i>
                <h3>Tools</h3>
                <p>Git, Docker, Linux, Figma</p>
            </div>
        </div>
    </div>
</section>

<section id="projects">
    <div class="container">
        <h2>Featured Projects</h2>
        <div class="project-grid">
            <div class="project-card">
                <h3>Academic Management System</h3>
                <p>A full-stack app for tracking grades and assignments. Built as a capstone project.</p>
                <span class="tags">PHP • MySQL • Bootstrap</span>
                <div class="project-links">
                    <a href="#"><i class="fab fa-github"></i> Code</a>
                </div>
            </div>

            <div class="project-card">
                <h3>Finance Tracker</h3>
                <p>A minimalist web app to manage expenses and visualize spending habits.</p>
                <span class="tags">React • Firebase • Chart.js</span>
                <div class="project-links">
                    <a href="#"><i class="fab fa-github"></i> Code</a>
                </div>
            </div>
        </div>
    </div>
</section>

<section id="contact">
    <div class="container">
        <h2>Let's Connect</h2>
        <p>Interested in working together? Shoot me an email!</p>
        <a href="mailto:your@email.com" class="btn">Email Me</a>
    </div>
</section>

</body>
</html>
/* General Styles */
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    line-height: 1.6;
    margin: 0;
    color: #333;
}

.container {
    max-width: 1100px;
    margin: auto;
    padding: 2rem;
}

section { padding: 4rem 0; }
h2 { text-align: center; margin-bottom: 2rem; }

/* Navigation */
nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 5%;
    background: #fff;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}

nav ul { display: flex; list-style: none; }
nav ul li a { margin-left: 20px; text-decoration: none; color: #333; font-weight: bold; }

/* Hero Section */
.hero {
    text-align: center;
    background: #f4f4f4;
    padding: 6rem 1rem;
}

.btn {
    display: inline-block;
    background: #007bff;
    color: #fff;
    padding: 0.8rem 1.5rem;
    text-decoration: none;
    border-radius: 5px;
    margin: 5px;
}

.btn.secondary { background: #333; }

/* Skills Grid */
.skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
}

.skill-card {
    background: #f9f9f9;
    padding: 1.5rem;
    border-radius: 10px;
    text-align: center;
    transition: transform 0.3s ease;
    border: 1px solid #ddd;
}

.skill-card i {
    font-size: 2.5rem;
    color: #007bff;
    margin-bottom: 1rem;
}

.skill-card:hover { transform: translateY(-5px); }

/* Project Cards */
.project-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
}

.project-card {
    border: 1px solid #ddd;
    padding: 1.5rem;
    border-radius: 10px;
}

.tags {
    display: block;
    margin: 10px 0;
    font-size: 0.8rem;
    font-weight: bold;
    color: #007bff;
}


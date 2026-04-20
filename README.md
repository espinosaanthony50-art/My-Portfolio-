<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Anthony Espinosa | Portfolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;500;700&display=swap" rel="stylesheet">
  
  <style>
    :root {
      --bg: #020617; /* Deep Obsidian */
      --card-bg: rgba(15, 23, 42, 0.7);
      --accent: #10b981; /* Electric Emerald */
      --accent-glow: rgba(16, 185, 129, 0.3);
      --text-main: #f0fdf4; /* Mint-tinted white */
      --text-dim: #94a3b8;
    }

    body { 
      background-color: var(--bg);
      color: var(--text-main);
      font-family: 'Space Grotesk', sans-serif;
      margin: 0;
      padding: 0;
      overflow-x: hidden;
      line-height: 1.6;
      /* Emerald mesh gradient */
      background-image: 
        radial-gradient(at 0% 0%, rgba(16, 185, 129, 0.1) 0px, transparent 50%),
        radial-gradient(at 100% 100%, rgba(52, 211, 153, 0.1) 0px, transparent 50%);
    }

    .blob {
      position: fixed;
      width: 500px;
      height: 500px;
      background: var(--accent);
      filter: blur(140px);
      border-radius: 50%;
      z-index: -1;
      opacity: 0.12;
      animation: move 25s infinite alternate;
    }

    .blob-2 {
      background: #059669;
      right: -100px;
      bottom: -100px;
      animation-delay: -7s;
    }

    @keyframes move {
      from { transform: translate(-15%, -15%); }
      to { transform: translate(25%, 25%); }
    }

    header {
      text-align: center;
      padding: 100px 20px 40px;
    }

    header h1 {
      font-size: clamp(3rem, 10vw, 4.5rem);
      margin: 0;
      background: linear-gradient(135deg, #fff 40%, var(--accent));
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      letter-spacing: -2px;
      font-weight: 700;
    }

    header p {
      font-size: 1.2rem;
      color: var(--text-dim);
      margin-top: 10px;
    }

    nav {
      display: flex;
      justify-content: center;
      gap: 10px;
      padding: 10px;
      background: rgba(2, 6, 23, 0.6);
      backdrop-filter: blur(25px);
      -webkit-backdrop-filter: blur(25px);
      position: sticky;
      top: 20px;
      width: fit-content;
      margin: 0 auto;
      border-radius: 100px;
      z-index: 1000;
      border: 1px solid rgba(16, 185, 129, 0.2);
      box-shadow: 0 10px 40px rgba(0,0,0,0.6);
    }

    nav a {
      text-decoration: none;
      color: var(--text-dim);
      font-weight: 500;
      padding: 8px 24px;
      border-radius: 100px;
      font-size: 0.9rem;
      transition: 0.3s;
    }

    nav a:hover, nav a.active {
      color: #fff;
      background: rgba(16, 185, 129, 0.2);
      box-shadow: 0 0 20px var(--accent-glow);
    }

    section {
      display: none;
      max-width: 900px;
      margin: 60px auto;
      padding: 50px 40px;
      background: var(--card-bg);
      backdrop-filter: blur(15px);
      border-radius: 32px;
      border: 1px solid rgba(16, 185, 129, 0.1);
      box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.7);
    }

    section.active {
      display: block;
      animation: slideUp 0.6s cubic-bezier(0.16, 1, 0.3, 1) forwards;
    }

    @keyframes slideUp {
      from { opacity: 0; transform: translateY(40px); }
      to { opacity: 1; transform: translateY(0); }
    }

    h2 {
      font-size: 2.2rem;
      margin-bottom: 30px;
      border-left: 5px solid var(--accent);
      padding-left: 20px;
      color: var(--accent);
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 25px;
    }

    .item-card {
      background: rgba(255, 255, 255, 0.02);
      padding: 25px;
      border-radius: 24px;
      border: 1px solid rgba(255, 255, 255, 0.05);
      transition: all 0.4s ease;
    }

    .item-card:hover {
      transform: translateY(-10px);
      border-color: var(--accent);
      background: rgba(16, 185, 129, 0.05);
      box-shadow: 0 10px 30px rgba(16, 185, 129, 0.1);
    }

    .project-thumb {
      width: 100%;
      height: 200px;
      object-fit: cover;
      border-radius: 16px;
      margin-bottom: 20px;
      border: 1px solid rgba(16, 185, 129, 0.2);
    }

    .file-link {
      display: inline-block;
      margin-top: 15px;
      color: var(--accent);
      text-decoration: none;
      font-size: 0.85rem;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 1px;
      border: 1px solid var(--accent);
      padding: 8px 20px;
      border-radius: 10px;
      transition: 0.3s;
    }

    .file-link:hover {
      background: var(--accent);
      color: var(--bg);
    }

    .contact-links a {
      display: block;
      margin-bottom: 15px;
      color: var(--accent);
      text-decoration: none;
      font-size: 1.1rem;
      transition: 0.2s;
    }

    .contact-links a:hover {
      transform: translateX(10px);
      text-shadow: 0 0 15px var(--accent);
    }

    .chatbot {
      position: fixed;
      bottom: 25px;
      right: 25px;
      width: 300px;
      background: rgba(2, 6, 23, 0.9);
      backdrop-filter: blur(15px);
      border-radius: 20px;
      border: 1px solid rgba(16, 185, 129, 0.4);
      overflow: hidden;
      box-shadow: 0 15px 40px rgba(0,0,0,0.8);
      z-index: 2000;
    }

    .chat-header {
      background: var(--accent);
      color: #000;
      padding: 12px;
      font-weight: bold;
      text-align: center;
      letter-spacing: 1px;
    }

    .chat-body {
      height: 250px;
      padding: 15px;
      overflow-y: auto;
      font-size: 0.85rem;
      background: rgba(2, 6, 23, 0.5);
    }

    #chatInput {
      width: 100%;
      background: rgba(15, 23, 42, 1);
      border: none;
      border-top: 1px solid rgba(16, 185, 129, 0.2);
      padding: 15px;
      color: white;
      outline: none;
    }

    .explore-button {
      display: inline-block;
      margin-top: 20px;
      padding: 14px 40px;
      background: var(--accent);
      color: #000;
      border-radius: 50px;
      text-decoration: none;
      font-weight: 700;
      transition: 0.3s;
      box-shadow: 0 10px 20px rgba(16, 185, 129, 0.2);
    }

    .explore-button:hover {
      box-shadow: 0 0 30px var(--accent);
      transform: translateY(-2px);
    }

    footer {
      text-align: center;
      padding: 60px 20px;
      color: var(--text-dim);
      font-size: 0.85rem;
    }
  </style>
</head>
<body>

  <div class="blob"></div>
  <div class="blob blob-2"></div>

  <header>
    <h1>Anthony Espinosa</h1>
    <p>IT Student & Digital Architect</p>
  </header>

  <nav>
    <a href="#home" class="active" onclick="showSection('home')">Home</a>
    <a href="#about" onclick="showSection('about')">About</a>
    <a href="#projects" onclick="showSection('projects')">Projects</a>
    <a href="#skills" onclick="showSection('skills')">Skills</a>
    <a href="#contact" onclick="showSection('contact')">Contact</a>
  </nav>

  <section id="home" class="active">
    <h2>Welcome</h2>
    <p>I build elegant solutions for the modern web. Aspiring IT specialist focused on bridging the gap between design and functionality.</p>
    <a href="#projects" class="explore-button" onclick="showSection('projects')">View My Work</a>
  </section>

  <section id="about">
    <h2>Biography</h2>
    <p>Passionate about the intersection of technology and human experience. Currently pursuing my IT degree with a focus on full-stack development.</p>
    <img src="https://via.placeholder.com/600x300/0f172a/10b981?text=Future+Tech+Vision" alt="Tech Background" style="width:100%; border-radius: 20px; margin-top:20px; border: 1px solid rgba(16,185,129,0.2);">
  </section>

  <section id="projects">
    <h2>Featured Work</h2>
    <div class="grid">
      <div class="item-card">
        <img src="A.jpg" alt="Jersey Layout" class="project-thumb">
        <h3>Jersey Layout</h3>
        <p>Creative sports apparel design and layout configuration.</p>
        <a href="A.jpg" target="_blank" class="file-link">View Design</a>
      </div>
      <div class="item-card">
        <img src="project2.png" alt="Logic Engine" class="project-thumb">
        <h3>Logic Engine</h3>
        <p>Custom JavaScript tools to handle complex data workflows.</p>
        <a href="logic-engine.zip" download class="file-link">Download Files</a>
      </div>
    </div>
  </section>

  <section id="skills">
    <h2>Technical Stack</h2>
    <div class="grid">
      <div class="item-card">
        <h3 style="color:var(--accent);">Languages</h3>
        <p>HTML, Java, JavaScript</p>
      </div>
      <div class="item-card">
        <h3 style="color:var(--accent);">Design</h3>
        <p>Figma, UI/UX Design</p>
      </div>
      <div class="item-card">
        <h3 style="color:var(--accent);">Certification</h3>
        <img src="B.jpg" alt="Certification" class="project-thumb" style="height:120px;">
        <p>Verified Professional Training</p>
      </div>
    </div>
  </section>

  <section id="contact">
    <h2>Let's Connect</h2>
    <div class="contact-links">
      <a href="mailto:espinosaanthony50@gmail.com">📧 espinosaanthony50@gmail.com</a>
      <a href="https://www.facebook.com/share/1AyUQ6gKmh/" target="_blank">👤 Anthony Espinosa</a>
      <a href="https://www.instagram.com/toni_2high?igsh=MXFxcXVwc2Y5bXRpeQ==" target="_blank">📸 @toni_2high</a>
    </div>
  </section>

  <div class="chatbot">
    <div class="chat-header">SYSTEM ASSISTANT</div>
    <div class="chat-body" id="chatBody">
      <p><span style="color:var(--accent)">[Bot]:</span> System online. How can I assist you today?</p>
    </div>
    <input type="text" id="chatInput" placeholder="Ask a question..." onkeypress="handleChat(event)">
  </div>

  <footer>
    <p>&copy; 2026 Anthony Espinosa // Built with Precision & Emerald Code.</p>
  </footer>

  <script>
    function showSection(sectionId) {
      document.querySelectorAll('section').forEach(sec => sec.classList.remove('active'));
      document.querySelectorAll('nav a').forEach(link => link.classList.remove('active'));

      const target = document.getElementById(sectionId);
      if(target) {
        target.classList.add('active');
        const activeLink = document.querySelector(`nav a[href="#${sectionId}"]`);
        if (activeLink) activeLink.classList.add('active');
        window.history.pushState(null, null, `#${sectionId}`);
      }
    }

    function handleChat(event) {
      if (event.key === 'Enter') {
        const input = document.getElementById('chatInput');
        const chatBody = document.getElementById('chatBody');
        const val = input.value.trim();

        if (val) {
          chatBody.innerHTML += `<p><span style="color:#fff">[You]:</span> ${val}</p>`;
          let response = "Message received. Anthony will get back to you soon.";
          if(val.toLowerCase().includes("skill")) response = "Anthony is skilled in HTML, Java, and Figma UI design.";
          
          setTimeout(() => {
            chatBody.innerHTML += `<p><span style="color:var(--accent)">[Bot]:</span> ${response}</p>`;
            chatBody.scrollTop = chatBody.scrollHeight;
          }, 500);
          input.value = "";
        }
      }
    }

    window.addEventListener('load', () => {
      const hash = window.location.hash.substring(1) || 'home';
      showSection(hash);
    });
  </script>
</body>
</html>




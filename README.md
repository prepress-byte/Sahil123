<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Graphic Designer Portfolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
  <style>
    /* ===== Reset ===== */
    * { margin:0; padding:0; box-sizing:border-box; }
    body { font-family: 'Poppins', sans-serif; line-height:1.6; transition: background 0.3s, color 0.3s; }
    a { text-decoration:none; color:inherit; }
    img { max-width:100%; display:block; }

    /* ===== Light / Dark Mode ===== */
    body.light { background:#f5f5f5; color:#222; }
    body.dark { background:#1a1a1a; color:#fff; }
    .toggle-btn { position:fixed; top:1rem; right:1rem; background:#ff6b6b; border:none; padding:0.5rem 1rem; border-radius:5px; cursor:pointer; z-index:1000; color:#fff; font-weight:600; transition: background 0.3s; }
    .toggle-btn:hover { background:#ff4757; }

    /* ===== Header / Hero ===== */
    header.hero { padding:4rem 1rem; text-align:center; }
    header nav { display:flex; justify-content:center; gap:2rem; flex-wrap:wrap; margin-bottom:2rem; }
    header nav a { font-weight:500; padding:0.5rem; border-radius:5px; transition: background 0.3s; }
    header nav a:hover { background:rgba(255,107,107,0.2); }
    header .hero-content h2 { font-size:2rem; margin-bottom:1rem; }
    header .hero-content h2 span { color:#ff6b6b; }
    header .hero-content p { font-size:1.2rem; opacity:0; transform: translateY(20px); transition: all 0.8s ease; }

    /* ===== Section ===== */
    section { padding:4rem 1rem; max-width:1200px; margin:0 auto; opacity:0; transform: translateY(20px); transition: all 0.8s ease; }
    section h2 { margin-bottom:2rem; font-size:2rem; color:#ff6b6b; }

    /* ===== Portfolio Gallery ===== */
    .gallery { display:grid; grid-template-columns:repeat(auto-fit,minmax(250px,1fr)); gap:1rem; }
    .gallery img { border-radius:10px; transition: transform 0.3s, box-shadow 0.3s; cursor:pointer; }
    .gallery img:hover { transform: scale(1.05); box-shadow:0 10px 20px rgba(0,0,0,0.3); }

    /* ===== Contact ===== */
    .social-links { display:flex; justify-content:center; gap:1rem; margin-top:1rem; }
    .social-links a { padding:0.5rem 1rem; border-radius:5px; background:#ff6b6b; color:#fff; transition: background 0.3s; }
    .social-links a:hover { background:#ff4757; }

    /* ===== Footer ===== */
    footer { background:rgba(0,0,0,0.1); text-align:center; padding:1rem; }

    /* ===== Animations ===== */
    .visible { opacity:1 !important; transform: translateY(0) !important; }

    /* ===== Responsive ===== */
    @media(max-width:768px) {
      header nav { flex-direction:column; gap:1rem; }
    }
  </style>
</head>
<body class="light">
  <!-- Light/Dark Mode Toggle -->
  <button class="toggle-btn" id="modeToggle">Dark Mode</button>

  <!-- Hero Section -->
  <header class="hero">
    <nav>
      <a href="#about">About</a>
      <a href="#portfolio">Portfolio</a>
      <a href="#contact">Contact</a>
    </nav>
    <div class="hero-content">
      <h2>Hi, I'm <span>Jane Doe</span></h2>
      <p>Graphic Designer & Visual Storyteller</p>
    </div>
  </header>

  <!-- About Section -->
  <section id="about">
    <h2>About Me</h2>
    <p>I am a creative graphic designer specializing in branding, UI/UX, and illustration. I help brands tell their stories visually.</p>
  </section>

  <!-- Portfolio Section -->
  <section id="portfolio">
    <h2>My Work</h2>
    <div class="gallery">
      <img src="https://via.placeholder.com/400x300?text=Project+1" alt="Project 1">
      <img src="https://via.placeholder.com/400x300?text=Project+2" alt="Project 2">
      <img src="https://via.placeholder.com/400x300?text=Project+3" alt="Project 3">
      <img src="https://via.placeholder.com/400x300?text=Project+4" alt="Project 4">
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact">
    <h2>Contact Me</h2>
    <p>Email me at <a href="mailto:yourname@example.com">yourname@example.com</a></p>
    <div class="social-links">
      <a href="#" target="_blank">LinkedIn</a>
      <a href="#" target="_blank">Behance</a>
      <a href="#" target="_blank">Dribbble</a>
    </div>
  </section>

  <footer>
    <p>&copy; 2026 Jane Doe. All Rights Reserved.</p>
  </footer>

  <script>
    // ===== Light/Dark Mode Toggle =====
    const toggleBtn = document.getElementById('modeToggle');
    toggleBtn.addEventListener('click', () => {
      if(document.body.classList.contains('light')){
        document.body.classList.remove('light');
        document.body.classList.add('dark');
        toggleBtn.textContent = "Light Mode";
      } else {
        document.body.classList.remove('dark');
        document.body.classList.add('light');
        toggleBtn.textContent = "Dark Mode";
      }
    });

    // ===== Smooth Scroll =====
    const links = document.querySelectorAll('nav a');
    links.forEach(link => {
      link.addEventListener('click', e => {
        e.preventDefault();
        document.querySelector(link.getAttribute('href')).scrollIntoView({ behavior:'smooth' });
      });
    });

    // ===== Scroll Reveal Animations =====
    const sections = document.querySelectorAll('section, .hero-content p');
    const revealOnScroll = () => {
      sections.forEach(sec => {
        const top = sec.getBoundingClientRect().top;
        const windowHeight = window.innerHeight;
        if(top < windowHeight - 100){
          sec.classList.add('visible');
        }
      });
    }
    window.addEventListener('scroll', revealOnScroll);
    window.addEventListener('load', revealOnScroll);
  </script>
</body>
</html>

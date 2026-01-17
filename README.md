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

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Graphic Designer Portfolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

  <style>
    /* ===== Reset ===== */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Poppins', sans-serif;
      line-height: 1.6;
      transition: background 0.3s, color 0.3s;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    img {
      max-width: 100%;
      display: block;
    }

    /* ===== Light / Dark Mode ===== */
    body.light {
      background: #f9f9f9;
      color: #222;
    }

    body.dark {
      background: #121212;
      color: #f1f1f1;
    }

    /* ===== Toggle Button ===== */
    .toggle-btn {
      position: fixed;
      top: 20px;
      right: 20px;
      padding: 10px 15px;
      border: none;
      border-radius: 20px;
      cursor: pointer;
      background: #6c63ff;
      color: white;
      z-index: 1000;
    }

    /* ===== Hero ===== */
    .hero {
      min-height: 100vh;
      padding: 40px;
      background: linear-gradient(135deg, #6c63ff, #928cff);
      color: white;
    }

    nav {
      display: flex;
      gap: 20px;
      justify-content: flex-end;
    }

    .hero-content {
      text-align: center;
      margin-top: 150px;
    }

    /* ===== Sections ===== */
    section {
      padding: 80px 10%;
      opacity: 0;
      transform: translateY(40px);
      transition: all 0.6s ease;
    }

    section.visible {
      opacity: 1;
      transform: translateY(0);
    }

    /* ===== Portfolio ===== */
    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
    }

    /* ===== Footer ===== */
    footer {
      text-align: center;
      padding: 20px;
    }
  </style>
</head>

<body class="light">

<button class="toggle-btn" id="modeToggle">Dark Mode</button>

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

<section id="about">
  <h2>About Me</h2>
  <p>I am a creative graphic designer specializing in branding, UI/UX, and illustration.</p>
</section>

<section id="portfolio">
  <h2>My Work</h2>
  <div class="gallery">
    <img src="https://via.placeholder.com/400x300">
    <img src="https://via.placeholder.com/400x300">
    <img src="https://via.placeholder.com/400x300">
    <img src="https://via.placeholder.com/400x300">
  </div>
</section>

<section id="contact">
  <h2>Contact Me</h2>
  <p>Email: yourname@example.com</p>
</section>

<footer>
  <p>&copy; 2026 Jane Doe</p>
</footer>

<script>
  const toggleBtn = document.getElementById('modeToggle');

  toggleBtn.addEventListener('click', () => {
    document.body.classList.toggle('dark');
    document.body.classList.toggle('light');

    toggleBtn.textContent =
      document.body.classList.contains('dark')
      ? 'Light Mode'
      : 'Dark Mode';
  });

  const sections = document.querySelectorAll('section');

  const revealOnScroll = () => {
    sections.forEach(sec => {
      if (sec.getBoundingClientRect().top < window.innerHeight - 100) {
        sec.classList.add('visible');
      }
    });
  };

  window.addEventListener('scroll', revealOnScroll);
  window.addEventListener('load', revealOnScroll);
</script>

</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Jane Doe | Graphic Designer</title>

  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

  <style>
    /* ===== RESET ===== */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Poppins', sans-serif;
      transition: background 0.3s, color 0.3s;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    img {
      width: 100%;
      display: block;
      border-radius: 12px;
    }

    /* ===== THEME ===== */
    body.light {
      background: #f8f9fc;
      color: #222;
    }

    body.dark {
      background: #0f172a;
      color: #e5e7eb;
    }

    /* ===== TOGGLE ===== */
    .toggle-btn {
      position: fixed;
      top: 20px;
      right: 20px;
      padding: 10px 16px;
      border-radius: 20px;
      border: none;
      cursor: pointer;
      background: #6366f1;
      color: #fff;
      z-index: 1000;
    }

    /* ===== NAV ===== */
    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 30px 10%;
    }

    nav h1 {
      font-weight: 700;
      font-size: 22px;
    }

    nav ul {
      display: flex;
      gap: 25px;
      list-style: none;
    }

    /* ===== HERO ===== */
    .hero {
      min-height: 90vh;
      display: flex;
      align-items: center;
      padding: 0 10%;
    }

    .hero-text h2 {
      font-size: 42px;
      margin-bottom: 10px;
    }

    .hero-text span {
      color: #6366f1;
    }

    .hero-text p {
      font-size: 18px;
      opacity: 0.8;
    }

    /* ===== SECTIONS ===== */
    section {
      padding: 80px 10%;
      opacity: 0;
      transform: translateY(40px);
      transition: 0.6s ease;
    }

    section.visible {
      opacity: 1;
      transform: translateY(0);
    }

    section h2 {
      font-size: 32px;
      margin-bottom: 20px;
    }

    /* ===== SKILLS ===== */
    .skills {
      display: flex;
      flex-wrap: wrap;
      gap: 15px;
    }

    .skill {
      padding: 10px 16px;
      background: #6366f1;
      color: white;
      border-radius: 20px;
      font-size: 14px;
    }

    /* ===== PORTFOLIO ===== */
    .portfolio {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 25px;
    }

    /* ===== CONTACT ===== */
    .contact p {
      margin-bottom: 10px;
    }

    /* ===== FOOTER ===== */
    footer {
      text-align: center;
      padding: 30px;
      opacity: 0.7;
    }

    /* ===== RESPONSIVE ===== */
    @media(max-width: 768px) {
      .hero-text h2 {
        font-size: 32px;
      }

      nav ul {
        gap: 15px;
      }
    }
  </style>
</head>

<body class="light">

<button class="toggle-btn" id="modeToggle">Dark Mode</button>

<nav>
  <h1>Jane Doe</h1>
  <ul>
    <li><a href="#about">About</a></li>
    <li><a href="#work">Work</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<div class="hero">
  <div class="hero-text">
    <h2>Hi, I'm <span>Jane Doe</span></h2>
    <p>Professional Graphic Designer & Visual Creator</p>
  </div>
</div>

<section id="about">
  <h2>About Me</h2>
  <p>I design modern, meaningful visuals for brands. I specialize in branding, UI/UX, and social media design.</p>

  <div class="skills">
    <div class="skill">Photoshop</div>
    <div class="skill">Illustrator</div>
    <div class="skill">Figma</div>
    <div class="skill">UI/UX</div>
    <div class="skill">Branding</div>
  </div>
</section>

<section id="work">
  <h2>My Work</h2>
  <div class="portfolio">
    <img src="https://via.placeholder.com/400x300?text=Project+1">
    <img src="https://via.placeholder.com/400x300?text=Project+2">
    <img src="https://via.placeholder.com/400x300?text=Project+3">
    <img src="https://via.placeholder.com/400x300?text=Project+4">
  </div>
</section>

<section id="contact" class="contact">
  <h2>Contact</h2>
  <p>Email: yourname@example.com</p>
  <p>LinkedIn | Behance | Dribbble</p>
</section>

<footer>
  © 2026 Jane Doe. All Rights Reserved.
</footer>

<script>
  const toggleBtn = document.getElementById("modeToggle");

  toggleBtn.addEventListener("click", () => {
    document.body.classList.toggle("dark");
    document.body.classList.toggle("light");

    toggleBtn.textContent =
      document.body.classList.contains("dark")
      ? "Light Mode"
      : "Dark Mode";
  });

  const sections = document.querySelectorAll("section");

  const reveal = () => {
    sections.forEach(sec => {
      if (sec.getBoundingClientRect().top < window.innerHeight - 100) {
        sec.classList.add("visible");
      }
    });
  };

  window.addEventListener("scroll", reveal);
  window.addEventListener("load", reveal);
</script>

</body>
</html>

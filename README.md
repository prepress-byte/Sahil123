<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Your Name – Graphic Designer</title>
  <link rel="stylesheet" href="style.css">
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&family=Inter&display=swap" rel="stylesheet">
</head>
<body>

<header class="hero">
  <h1>Your Name</h1>
  <p class="tagline">Professional Graphic Designer</p>
  <a href="#work" class="btn">View Work</a>
</header>

<section class="about">
  <h2>About Me</h2>
  <p>
    I’m a professional graphic designer specializing in brand identity,
    logo design, and visual storytelling. I create bold, modern, and
    meaningful designs that help brands stand out.
  </p>
</section>

<section id="work" class="portfolio">
  <h2>Selected Work</h2>
  <div class="grid">
    <div class="card">Project 1</div>
    <div class="card">Project 2</div>
    <div class="card">Project 3</div>
    <div class="card">Project 4</div>
  </div>
</section>

<section class="services">
  <h2>Services</h2>
  <ul>
    <li>Logo Design</li>
    <li>Brand Identity</li>
    <li>Social Media Creatives</li>
    <li>UI Design</li>
  </ul>
</section>

<section class="contact">
  <h2>Let’s Work Together</h2>
  <p>Email: yourname@email.com</p>
  <p>
    <a href="#">Behance</a> •
    <a href="#">Instagram</a> •
    <a href="#">LinkedIn</a>
  </p>
</section>

<footer>
  © 2026 Your Name. All Rights Reserved.
</footer>

<script src="script.js"></script>
</body>
</html>
:root {
  --bg: #0f0f0f;
  --card: #181818;
  --text: #ffffff;
  --muted: #9ca3af;
  --accent: #6366f1;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Inter', sans-serif;
  background: var(--bg);
  color: var(--text);
  line-height: 1.6;
}

.hero {
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.hero h1 {
  font-family: 'Poppins', sans-serif;
  font-size: 4rem;
}

.tagline {
  color: var(--muted);
  margin: 1rem 0;
}

.btn {
  padding: 12px 28px;
  background: var(--accent);
  color: #fff;
  text-decoration: none;
  border-radius: 30px;
}

section {
  padding: 80px 10%;
}

h2 {
  font-family: 'Poppins', sans-serif;
  margin-bottom: 30px;
}

.portfolio .grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
}

.card {
  background: var(--card);
  height: 220px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--muted);
  transition: transform 0.3s;
}

.card:hover {
  transform: translateY(-8px);
}

.services ul {
  list-style: none;
}

.services li {
  margin-bottom: 10px;
}

.contact a {
  color: var(--accent);
  text-decoration: none;
}

footer {
  text-align: center;
  padding: 20px;
  color: var(--muted);
}

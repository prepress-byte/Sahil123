<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Professional Portfolio</title>

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
  background: #000;
  color: #e5e5e5;
}

/* ===== GLOBAL ===== */
a {
  text-decoration: none;
  color: inherit;
}

section {
  padding: 80px 10%;
}

h2 {
  font-size: 32px;
  margin-bottom: 20px;
  color: #fff;
}

/* ===== NAV ===== */
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 30px 10%;
}

nav h1 {
  font-size: 22px;
  font-weight: 700;
  color: #fff;
}

nav ul {
  display: flex;
  gap: 25px;
  list-style: none;
}

/* ===== HERO ===== */
.hero {
  min-height: 90vh;
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;
}

.hero-text h2 {
  font-size: 42px;
}

.hero-text span {
  color: #22c55e;
}

.hero-text p {
  margin-top: 10px;
  opacity: 0.8;
}

.hero-image img {
  border-radius: 20px;
}

/* ===== ABOUT (2 COLUMN) ===== */
.about {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 40px;
}

.skills {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
}

.skill {
  padding: 8px 14px;
  background: #22c55e;
  color: #000;
  border-radius: 20px;
  font-size: 14px;
}

/* ===== PORTFOLIO (GRID COLUMNS) ===== */
.portfolio {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 25px;
}

.portfolio img {
  width: 100%;
  border-radius: 16px;
  transition: transform 0.3s;
}

.portfolio img:hover {
  transform: scale(1.05);
}

/* ===== CONTACT (2 COLUMN) ===== */
.contact {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 40px;
}

.contact-info p {
  margin-bottom: 10px;
}

form input,
form textarea {
  width: 100%;
  padding: 12px;
  margin-bottom: 15px;
  background: #111;
  border: 1px solid #333;
  color: #fff;
  border-radius: 8px;
}

form button {
  padding: 12px;
  border: none;
  background: #22c55e;
  color: #000;
  font-weight: 600;
  border-radius: 8px;
  cursor: pointer;
}

/* ===== FOOTER ===== */
footer {
  text-align: center;
  padding: 30px;
  border-top: 1px solid #222;
  opacity: 0.6;
}

/* ===== RESPONSIVE ===== */
@media (max-width: 900px) {
  .hero,
  .about,
  .contact {
    grid-template-columns: 1fr;
  }

  .hero-text h2 {
    font-size: 32px;
  }
}
</style>
</head>

<body>

<nav>
  <h1>Jane Doe</h1>
  <ul>
    <li><a href="#about">About</a></li>
    <li><a href="#work">Work</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<section class="hero">
  <div class="hero-text">
    <h2>Hi, I'm <span>Jane Doe</span></h2>
    <p>Professional Graphic Designer & Visual Creator</p>
  </div>
  <div class="hero-image">
    <img src="https://via.placeholder.com/400x400?text=Your+Photo">
  </div>
</section>

<section id="about">
  <h2>About Me</h2>
  <div class="about">
    <p>
      I create modern, clean and powerful designs for brands.  
      Specializing in branding, UI/UX and social media creatives.
    </p>

    <div class="skills">
      <div class="skill">Photoshop</div>
      <div class="skill">Illustrator</div>
      <div class="skill">Figma</div>
      <div class="skill">UI/UX</div>
      <div class="skill">Branding</div>
    </div>
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

<section id="contact">
  <h2>Contact Me</h2>
  <div class="contact">
    <div class="contact-info">
      <p>Email: yourname@example.com</p>
      <p>LinkedIn | Behance | Dribbble</p>
    </div>

    <form>
      <input type="text" placeholder="Your Name">
      <input type="email" placeholder="Your Email">
      <textarea rows="4" placeholder="Message"></textarea>
      <button>Send Message</button>
    </form>
  </div>
</section>

<footer>
  © 2026 Jane Doe. All Rights Reserved.
</footer>

</body>
</html>

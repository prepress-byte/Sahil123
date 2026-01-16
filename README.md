<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Your Name | Graphic Designer</title>

<!-- Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&family=Inter&display=swap" rel="stylesheet">

<style>
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

html {
  scroll-behavior: smooth;
}

body {
  font-family: 'Inter', sans-serif;
  background: var(--bg);
  color: var(--text);
  line-height: 1.6;
}

/* ---------- HERO ---------- */
.hero {
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 0 20px;
}

.hero h1 {
  font-family: 'Poppins', sans-serif;
  font-size: 4rem;
}

.hero p {
  color: var(--muted);
  margin: 15px 0 30px;
}

.btn {
  padding: 14px 36px;
  background: var(--accent);
  color: #fff;
  text-decoration: none;
  border-radius: 30px;
  font-weight: 600;
  transition: transform 0.3s, box-shadow 0.3s;
}

.btn:hover {
  transform: translateY(-3px);
  box-shadow: 0 10px 30px rgba(99,102,241,0.4);
}

/* ---------- SECTIONS ---------- */
section {
  padding: 90px 10%;
}

h2 {
  font-family: 'Poppins', sans-serif;
  margin-bottom: 30px;
  font-size: 2.2rem;
}

/* ---------- ABOUT ---------- */
.about p {
  max-width: 700px;
  color: var(--muted);
}

/* ---------- PORTFOLIO ---------- */
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 25px;
}

.card {
  background: var(--card);
  height: 220px;
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 600;
  color: var(--muted);
  position: relative;
  overflow: hidden;
  cursor: pointer;
}

.card::after {
  content: "View Project";
  position: absolute;
  inset: 0;
  background: rgba(0,0,0,0.7);
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0;
  transition: 0.3s;
}

.card:hover::after {
  opacity: 1;
}

/* ---------- SERVICES ---------- */
.services ul {
  list-style: none;
}

.services li {
  margin-bottom: 12px;
  color: var(--muted);
}

/* ---------- TESTIMONIALS ---------- */
.testimonial {
  background: var(--card);
  padding: 30px;
  border-radius: 12px;
  margin-bottom: 20px;
  color: var(--muted);
}

/* ---------- CONTACT ---------- */
.contact a {
  color: var(--accent);
  text-decoration: none;
  margin-right: 10px;
}

/* ---------- FOOTER ---------- */
footer {
  text-align: center;
  padding: 30px;
  color: var(--muted);
  border-top: 1px solid #222;
}

/* ---------- RESPONSIVE ---------- */
@media (max-width: 768px) {
  .hero h1 {
    font-size: 2.8rem;
  }
  section {
    padding: 70px 7%;
  }
}
</style>
</head>

<body>

<!-- HERO -->
<div class="hero">
  <h1>Your Name</h1>
  <p>Professional Graphic Designer</p>
  <a href="#portfolio" class="btn">View My Work</a>
</div>

<!-- ABOUT -->
<section class="about">
  <h2>About Me</h2>
  <p>
    I’m a professional graphic designer focused on creating bold,
    clean, and impactful visual identities. I specialize in logo design,
    branding, social media creatives, and UI visuals that help brands
    stand out in the digital world.
  </p>
</section>

<!-- PORTFOLIO -->
<section id="portfolio">
  <h2>Selected Work</h2>
  <div class="grid">
    <div class="card">Logo Design</div>
    <div class="card">Brand Identity</div>
    <div class="card">Social Media</div>
    <div class="card">UI Design</div>
  </div>
</section>

<!-- SERVICES -->
<section class="services">
  <h2>Services</h2>
  <ul>
    <li>Logo Design</li>
    <li>Brand Identity</li>
    <li>Social Media Creatives</li>
    <li>UI / Web Graphics</li>
  </ul>
</section>

<!-- TESTIMONIALS -->
<section>
  <h2>Testimonials</h2>
  <div class="testimonial">
    “Amazing designer with a strong eye for detail. Highly recommended.”
  </div>
  <div class="testimonial">
    “Delivered professional branding that elevated our business.”
  </div>
</section>

<!-- CONTACT -->
<section class="contact">
  <h2>Let’s Work Together</h2>
  <p>Email: yourname@email.com</p>
  <p>
    <a href="#">Behance</a>
    <a href="#">Instagram</a>
    <a href="#">LinkedIn</a>
  </p>
</section>

<footer>
  © 2026 Your Name. All Rights Reserved.
</footer>

<script>
// Simple fade-in on scroll
const sections = document.querySelectorAll("section");
const observer = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.style.opacity = 1;
      entry.target.style.transform = "translateY(0)";
    }
  });
}, { threshold: 0.1 });

sections.forEach(sec => {
  sec.style.opacity = 0;
  sec.style.transform = "translateY(40px)";
  sec.style.transition = "0.6s ease";
  observer.observe(sec);
});
</script>

</body>
</html>

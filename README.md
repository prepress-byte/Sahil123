<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Graphic Designer Portfolio</title>
    <link rel="stylesheet" href="style.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        /* Simple CSS directly in HTML for GitHub Pages simplicity */

        * { margin:0; padding:0; box-sizing:border-box; }
        body { font-family: 'Poppins', sans-serif; line-height:1.6; color:#333; }

        a { text-decoration:none; color:inherit; }

        header.hero { background:#1a1a1a; color:#fff; padding:2rem 1rem; text-align:center; }
        header nav { display:flex; justify-content:space-between; align-items:center; max-width:1200px; margin:0 auto; }
        header nav ul { list-style:none; display:flex; gap:1rem; }
        header nav ul li a { color:#fff; font-weight:500; }
        header .hero-content h2 span { color:#ff6b6b; }

        section { padding:4rem 1rem; text-align:center; max-width:1000px; margin:0 auto; }
        section h2 { margin-bottom:1rem; font-size:2rem; color:#ff6b6b; }

        .gallery { display:grid; grid-template-columns:repeat(auto-fit,minmax(250px,1fr)); gap:1rem; margin-top:2rem; }
        .gallery img { width:100%; border-radius:10px; transition: transform 0.3s ease; }
        .gallery img:hover { transform:scale(1.05); }

        .social-links { display:flex; justify-content:center; gap:1rem; margin-top:1rem; }

        footer { background:#222; color:#fff; padding:1rem; text-align:center; }

    </style>
</head>
<body>
    <!-- Hero Section -->
    <header class="hero">
        <nav>
            <h1 class="logo">MyPortfolio</h1>
            <ul>
                <li><a href="#about">About</a></li>
                <li><a href="#portfolio">Portfolio</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
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
        // Smooth scrolling for nav links
        const links = document.querySelectorAll('nav ul li a');
        for (const link of links) {
            link.addEventListener('click', function(e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                target.scrollIntoView({ behavior: 'smooth' });
            });
        }
    </script>
</body>
</html>

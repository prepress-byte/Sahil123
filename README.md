<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Graphic Designer Portfolio</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@500;700&family=Inter&display=swap" rel="stylesheet">

<style>
body {
  margin: 0;
  font-family: 'Inter', sans-serif;
  background: #0f0f0f;
  color: #ffffff;
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
  font-size: 3.5rem;
}

.hero p {
  color: #9ca3af;
}

button {
  margin-top: 20px;
  padding: 12px 30px;
  border: none;
  background: #6366f1;
  color: white;
  font-size: 16px;
  border-radius: 30px;
  cursor: pointer;
}

section {
  padding: 80px 10%;
}

.card {
  background: #181818;
  padding: 60px;
  margin-bottom: 20px;
  border-radius: 12px;
}
</style>
</head>

<body>

<div class="hero">
  <h1>Your Name</h1>
  <p>Professional Graphic Designer</p>
  <button onclick="scrollToWork()">View Work</button>
</div>

<section id="work">
  <h2>My Work</h2>
  <div class="card">Logo Design</div>
  <div class="card">Brand Identity</div>
  <div class="card">Social Media Design</div>
</section>

<script>
function scrollToWork() {
  document.getElementById("work").scrollIntoView({ behavior: "smooth" });
}
</script>

</body>
</html>

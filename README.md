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

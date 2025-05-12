<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Responsive Layout</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>

  <header class="navbar">
    <div class="logo">MySite</div>
    <nav class="nav-links">
      <a href="#">Home</a>
      <a href="#">About</a>
      <a href="#">Services</a>
      <a href="#">Contact</a>
    </nav>
  </header>

  <main class="grid-layout">
    <section class="box box1">Welcome</section>
    <section class="box box2">Content</section>
    <section class="box box3">More Info</section>
    <section class="box box4">Extras</section>
  </main>

  <footer class="footer">
    &copy; 2025 MySite | All rights reserved.
  </footer>

</body>
</html>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Segoe UI', sans-serif;
  line-height: 1.6;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
  background-color: #1e90ff;
  color: white;
}

.nav-links a {
  color: white;
  margin-left: 1rem;
  text-decoration: none;
}

.grid-layout {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1rem;
  padding: 2rem;
}

.box {
  padding: 2rem;
  background-color: #f0f0f0;
  border-radius: 6px;
  text-align: center;
}

.footer {
  background: #333;
  color: #fff;
  padding: 1rem;
  text-align: center;
}

@media (max-width: 992px) {
  .grid-layout {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 600px) {
  .grid-layout {
    grid-template-columns: 1fr;
  }

  .nav-links {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    margin-top: 1rem;
  }

  .navbar {
    flex-direction: column;
    align-items: flex-start;
  }
}

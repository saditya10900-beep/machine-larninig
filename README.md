
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Aditya Singh | Machine Learning</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: Arial, sans-serif;
      background: #0b1020;
      color: #f1f5f9;
      line-height: 1.6;
    }

    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 20px 8%;
      background: #11182b;
      position: sticky;
      top: 0;
      z-index: 10;
      border-bottom: 1px solid #26334b;
    }

    .logo {
      font-size: 23px;
      font-weight: bold;
      color: #38bdf8;
    }

    nav a {
      color: #e2e8f0;
      text-decoration: none;
      margin-left: 20px;
    }

    nav a:hover {
      color: #38bdf8;
    }

    .hero {
      min-height: 75vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 70px 20px;
      background: radial-gradient(
        circle at top,
        #1e3a5f,
        #0b1020 65%
      );
    }

    .hero h1 {
      font-size: clamp(36px, 7vw, 68px);
      line-height: 1.2;
      margin-bottom: 20px;
    }

    .highlight {
      color: #38bdf8;
    }

    .hero p {
      max-width: 650px;
      color: #cbd5e1;
      margin-bottom: 28px;
    }

    .btn {
      display: inline-block;
      padding: 12px 24px;
      background: #0284c7;
      color: white;
      border-radius: 8px;
      text-decoration: none;
      border: none;
      cursor: pointer;
      font-size: 15px;
    }

    .btn:hover {
      background: #0369a1;
    }

    section {
      padding: 65px 8%;
    }

    .section-title {
      font-size: 32px;
      text-align: center;
      margin-bottom: 35px;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(
        auto-fit, minmax(220px, 1fr)
      );
      gap: 22px;
    }

    .card {
      padding: 25px;
      background: #151e32;
      border: 1px solid #29374f;
      border-radius: 14px;
      transition: 0.25s;
    }

    .card:hover {
      transform: translateY(-5px);
      border-color: #38bdf8;
    }

    .card h3 {
      color: #38bdf8;
      margin-bottom: 12px;
    }

    .card p {
      color: #cbd5e1;
    }

    .about {
      max-width: 800px;
      margin: auto;
      text-align: center;
      color: #cbd5e1;
    }

    .demo {
      max-width: 550px;
      margin: auto;
      background: #151e32;
      padding: 28px;
      border-radius: 14px;
      border: 1px solid #29374f;
    }

    label {
      display: block;
      margin: 15px 0 6px;
    }

    input {
      width: 100%;
      padding: 12px;
      border-radius: 7px;
      border: 1px solid #475569;
      background: #0b1020;
      color: white;
      font-size: 16px;
    }

    #result {
      margin-top: 20px;
      color: #7dd3fc;
      overflow-wrap: anywhere;
    }

    footer {
      text-align: center;
      padding: 25px;
      background: #11182b;
      color: #94a3b8;
    }

    @media (max-width: 600px) {
      nav {
        flex-direction: column;
        gap: 12px;
      }

      nav a {
        margin: 0 7px;
        font-size: 14px;
      }

      section {
        padding: 45px 6%;
      }
    }
  </style>
</head>

<body>

  <nav>
    <div class="logo">Aditya Singh</div>
    <div>
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#projects">Projects</a>
      <a href="#demo">Demo</a>
    </div>
  </nav>

  <header class="hero" id="home">
    <h1>Explore the World of<br>
      <span class="highlight">Machine Learning</span>
    </h1>

    <p>
      Hi, I'm Aditya Singh. Welcome to my Machine Learning
      website, where technology, data and artificial
      intelligence come together.
    </p>

    <a class="btn" href="#projects">Explore Projects</a>
  </header>

  <section id="about">
    <h2 class="section-title">About Me</h2>

    <div class="about">
      <p>
        Hello! My name is Aditya Singh. I am interested in
        Machine Learning, Artificial Intelligence and Python.
        My goal is to explore intelligent systems and build
        useful technology projects.
      </p>
    </div>
  </section>

  <section id="projects">
    <h2 class="section-title">Machine Learning Projects</h2>

    <div class="grid">
      <div class="card">
        <h3>🤖 Prediction System</h3>
        <p>
          Learn how machine learning models use data
          to predict possible outcomes.
        </p>
      </div>

      <div class="card">
        <h3>📊 Data Analysis</h3>
        <p>
          Explore datasets, find patterns and understand
          information using Python.
        </p>
      </div>

      <div class="card">
        <h3>🧠 AI Assistant</h3>
        <p>
          Discover how artificial intelligence can
          understand inputs and generate responses.
        </p>
      </div>

      <div class="card">
        <h3>📷 Image Recognition</h3>
        <p>
          Learn how computer vision systems classify
          images using trained models.
        </p>
      </div>
    </div>
  </section>

  <section id="demo">
    <h2 class="section-title">ML Demo</h2>

    <div class="demo">
      <p>
        Enter study hours to see a sample score estimate.
      </p>

      <label for="hours">Study hours (0–10)</label>
      <input
        type="number"
        id="hours"
        min="0"
        max="10"
        step="0.5"
        placeholder="Example: 5"
      >

      <br><br>

      <button class="btn" onclick="predictScore()">
        Predict Score
      </button>

      <p id="result" aria-live="polite"></p>
    </div>
  </section>

  <footer>
    <p>© <span id="year"></span> Aditya Singh</p>
    <p>Learning Machine Learning, One Project at a Time.</p>
  </footer>

  <script>
    document.getElementById("year").textContent =
      new Date().getFullYear();

    function predictScore() {
      const input = document.getElementById("hours");
      const result = document.getElementById("result");
      const hours = Number(input.value);

      if (
        input.value.trim() === "" ||
        !Number.isFinite(hours) ||
        hours < 0 ||
        hours > 10
      ) {
        result.textContent =
          "Please enter study hours between 0 and 10.";
        return;
      }

      // Demo formula, not a trained ML model.
      const score = Math.round(
        Math.min(100, hours * 10)
      );

      result.textContent =
        "Sample estimated score: " + score + "/100";
    }
  </script>

</body>
</html>

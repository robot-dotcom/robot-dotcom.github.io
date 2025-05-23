<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Solar Surveillance Robot</title>
  <style>
    :root {
      --bg: #f5f5f5;
      --text: #333;
      --card: #fff;
    }
    body.dark {
      --bg: #1e1e1e;
      --text: #eee;
      --card: #2b2b2b;
    }

    body {
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      padding: 0;
      background-color: var(--bg);
      color: var(--text);
      transition: 0.3s;
    }

    header {
      position: sticky;
      top: 0;
      background-color: var(--card);
      padding: 15px 20px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
      display: flex;
      justify-content: space-between;
      align-items: center;
      z-index: 10;
    }

    header h1 {
      font-size: 1rem;
      color: red;
    }

    nav a {
      margin: 0 10px;
      text-decoration: none;
      font-weight: bold;
      color: var(--text);
    }

    nav a:hover {
      text-decoration: underline;
    }

    .toggle-btn {
      padding: 5px 10px;
      background-color: #2980b9;
      border: none;
      border-radius: 5px;
      color: white;
      cursor: pointer;
    }

    section {
      background: var(--card);
      margin: 20px;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.05);
      animation: fadeIn 0.7s ease-in;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    img {
      max-width: 100%;
      border-radius: 10px;
      margin-top: 10px;
    }

    ul {
      padding-left: 20px;
    }

    footer {
      text-align: center;
      padding: 20px;
      font-size: 0.9rem;
    }

    @media (max-width: 768px) {
      nav a {
        display: inline-block;
        margin: 8px 5px;
      }
      header {
        flex-direction: column;
        align-items: flex-start;
      }
    }
  </style>
</head>
<body>

  <header>
    <h1>SOLAR-CHARGED ROBOT WITH AI</h1>
    <div>
      <nav>
        <a href="#introduction">Intro</a>
        <a href="#architecture">Architecture</a>
        <a href="#features">Features</a>
        <a href="#results">Results</a>
        <a href="#applications">Applications</a>
        <a href="#conclusion">Conclusion</a>
      </nav>
      <button class="toggle-btn" onclick="toggleMode()">🌙/☀️</button>
    </div>
  </header>

  <main>
    <section id="introduction">
      <h2>Introduction & Problem Statement</h2>
      <p><strong>Purpose:</strong> An autonomous robot for real-time monitoring and detection.</p>
      <p><strong>Problem:</strong> Traditional systems lack 24/7 automation. This solves that.</p>
    </section>

    <section id="architecture">
      <h2>System Architecture & Components</h2>
      <h3>Hardware</h3>
      <ul>
        <li>Raspberry Pi Pico & Pi 3</li>
        <li>Sensors: AI Camera, IR, Ultrasonic, Gyroscope</li>
        <li>Solar-powered battery system</li>
      </ul>
      <h3>Software</h3>
      <ul>
        <li>Blynk (remote control)</li>
        <li>Gmail (alert system)</li>
      </ul>
    </section>

    <section id="features">
      <h2>Key Features & Functions</h2>

      <h3>Object Detection</h3>
      <p>AI camera detects people and sends email alerts.</p>
      <img src="aicamera.jpg" alt="AI Camera">

      <h3>Obstacle Avoidance</h3>
      <p>IR + Ultrasonic sensors help the robot avoid crashes.</p>
      <img src="IR.png" alt="Obstacle Avoidance">

      <h3>Path Following</h3>
      <p>IR sensors follow precise black line paths.</p>
      <img src="line.png" alt="Line Following">

      <h3>Upside-down Alert</h3>
      <p>Gyroscope triggers buzzer when flipped.</p>
      <img src="gyro.png" alt="Gyroscope Alert">

      <h3>Remote Control</h3>
      <p>Use Bluetooth app to manually drive the robot.</p>
      <img src="remote.png" alt="Bluetooth Remote">
    </section>

    <section id="results">
      <h2>Results & Performance</h2>
      <ul>
        <li>Object Detection Accuracy</li>
        <li>Alert Response Time</li>
        <li>Solar Energy Efficiency</li>
      </ul>
    </section>

    <section id="applications">
      <h2>Applications</h2>
      <ul>
        <li>Home and Industrial Surveillance</li>
        <li>Smart Home Monitoring</li>
      </ul>
    </section>

    <section id="conclusion">
      <h2>Conclusion & Future Improvements</h2>
      <p>This robot provides smart, sustainable surveillance.</p>
      <ul>
        <li>Better AI for detection</li>
        <li>Low-light camera upgrade</li>
        <li>Durable weatherproof build</li>
      </ul>
    </section>

    <footer>
      <p>Contact: <a href="mailto:harith.abdmanan@gmail.com">harith.abdmanan@gmail.com</a></p>
    </footer>
  </main>

  <script>
    function toggleMode() {
      document.body.classList.toggle("dark");
    }
    // Smooth scroll for anchor links
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function(e) {
        e.preventDefault();
        document.querySelector(this.getAttribute('href'))
          .scrollIntoView({ behavior: 'smooth' });
      });
    });
  </script>
</body>
</html>

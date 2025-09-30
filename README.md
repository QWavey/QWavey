<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>QWavey GitHub Profile</title>
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
<style>
  /* ===== Reset & Global ===== */
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body {
    font-family: 'Roboto', sans-serif;
    background: linear-gradient(135deg, #1f1c2c, #928dab);
    color: #fff;
    line-height: 1.6;
  }

  a {
    text-decoration: none;
    color: inherit;
  }

  /* ===== Container ===== */
  .container {
    max-width: 1000px;
    margin: 50px auto;
    padding: 20px;
  }

  /* ===== Header ===== */
  header {
    text-align: center;
    margin-bottom: 50px;
  }

  header h1 {
    font-size: 3em;
    background: linear-gradient(90deg, #ff6a00, #ee0979);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    animation: slideIn 2s ease-out;
  }

  @keyframes slideIn {
    from { opacity: 0; transform: translateY(-50px);}
    to { opacity: 1; transform: translateY(0);}
  }

  header p {
    font-size: 1.2em;
    margin-top: 10px;
    color: #ddd;
  }

  /* ===== Buttons ===== */
  .buttons {
    display: flex;
    justify-content: center;
    gap: 20px;
    margin-top: 25px;
  }

  .buttons a {
    padding: 12px 25px;
    border-radius: 30px;
    background: linear-gradient(90deg, #ff6a00, #ee0979);
    color: #fff;
    font-weight: bold;
    transition: 0.3s;
  }

  .buttons a:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 20px rgba(0,0,0,0.3);
  }

  /* ===== Stats Section ===== */
  .stats-section {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 30px;
    margin-bottom: 50px;
    animation: fadeIn 2s ease-out;
  }

  .card {
    background: rgba(255,255,255,0.05);
    border-radius: 20px;
    padding: 20px;
    min-width: 300px;
    flex: 1;
    max-width: 450px;
    box-shadow: 0 5px 15px rgba(0,0,0,0.3);
    transition: transform 0.3s, box-shadow 0.3s;
  }

  .card:hover {
    transform: translateY(-10px);
    box-shadow: 0 15px 30px rgba(0,0,0,0.5);
  }

  .card img {
    width: 100%;
    border-radius: 15px;
  }

  @keyframes fadeIn {
    from { opacity: 0;}
    to { opacity: 1;}
  }

  /* ===== Language Bars ===== */
  .languages {
    margin: 50px 0;
  }

  .languages h2 {
    text-align: center;
    font-size: 2em;
    margin-bottom: 30px;
    background: linear-gradient(90deg, #ee0979, #ff6a00);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }

  .language {
    display: flex;
    align-items: center;
    margin-bottom: 15px;
    animation: slideLeft 1s ease-out;
  }

  .language span {
    flex: 1;
    font-size: 1.1em;
  }

  .bar {
    flex: 3;
    height: 20px;
    background: rgba(255,255,255,0.2);
    border-radius: 10px;
    overflow: hidden;
    margin-left: 15px;
  }

  .fill {
    height: 100%;
    border-radius: 10px;
    width: 0;
    text-align: right;
    padding-right: 10px;
    color: #fff;
    font-weight: bold;
    line-height: 20px;
  }

  .python { background: #306998; animation: grow 1s forwards 0.5s; }
  .javascript { background: #f0db4f; color: #000; animation: grow 1s forwards 0.8s; }
  .go { background: #00add8; animation: grow 1s forwards 1.1s; }

  @keyframes grow {
    from { width: 0;}
    to { width: 90%;}
  }

  @keyframes slideLeft {
    from { opacity: 0; transform: translateX(-50px);}
    to { opacity: 1; transform: translateX(0);}
  }

  /* ===== Footer ===== */
  footer {
    text-align: center;
    margin: 50px 0;
    color: #aaa;
    font-size: 0.9em;
  }

  /* ===== Section Separators ===== */
  .separator {
    height: 4px;
    width: 150px;
    background: linear-gradient(90deg, #ff6a00, #ee0979);
    margin: 50px auto;
    border-radius: 2px;
  }

  /* ===== Animations for cards ===== */
  .card:hover img {
    transform: scale(1.05);
    transition: transform 0.3s;
  }

  /* ===== Extra Info Section ===== */
  .extra {
    text-align: center;
    margin-top: 50px;
  }

  .extra h3 {
    font-size: 1.8em;
    margin-bottom: 20px;
  }

  .extra p {
    font-size: 1.1em;
    max-width: 700px;
    margin: 0 auto;
    color: #ddd;
  }

</style>
</head>
<body>
  <div class="container">
    <!-- Header -->
    <header>
      <h1>QWavey</h1>
      <p>Full-stack Developer | Open Source Enthusiast | Lifelong Learner</p>
      <div class="buttons">
        <a href="https://github.com/QWavey" target="_blank">GitHub</a>
        <a href="https://twitter.com/QWavey" target="_blank">Twitter</a>
        <a href="https://www.linkedin.com/in/QWavey/" target="_blank">LinkedIn</a>
      </div>
    </header>

  <div class="separator"></div>

    <!-- Stats Section -->
   <section class="stats-section">
      <div class="card">
        <img src="https://github-readme-stats.vercel.app/api?username=QWavey&show_icons=true&theme=radical&hide_border=true" alt="GitHub Stats">
      </div>
      <div class="card">
        <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=QWavey&layout=compact&theme=radical" alt="Top Languages">
      </div>
    </section>

  <div class="separator"></div>

 
  <section class="languages">
      <h2>Most Used Languages</h2>

     
      
  <div class="language">
        <span>🐍 Python</span>
        <div class="bar"><div class="fill python">90%</div></div>
      </div>
      <div class="language">
        <span>🌐 JavaScript</span>
        <div class="bar"><div class="fill javascript">75%</div></div>
      </div>
      <div class="language">
        <span>⚙️ Go</span>
        <div class="bar"><div class="fill go">60%</div></div>
      </div>
    </section>

  <div class="separator"></div>

   
  <section class="extra">
      <h3>About Me</h3>
      <p>
        I am QWavey, a passionate developer who loves building things that make a difference.
        I contribute to open source, explore new technologies, and share my knowledge with the
        community. My goal is to continuously improve and help others grow in the world of software.
      </p>
    </section>

  <footer>
      &copy; 2025 QWavey | Built with ❤️ and Code
    </footer>
  </div>
</body>
</html>

# Portfolio-Frontend-Website

<!DOCTYPE html>

<head>
  <meta charset="UTF-8">
  <title>Radhika Loni - Portfolio</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: LightBlue;
    }

    .section {
      display: none;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      min-height: 100vh;
      padding: 20px;
    }

    .section.active {
      display: flex;
    }

    .profile-pic {
      width: 200px;
      height: 200px;
      object-fit: cover;
      border-radius: 50%;
      border: 5px solid #0077b6;
      margin-bottom: 20px;
    }

    .profile-pic:hover {
      transform: translateY(-2px);
    }

    h1 {
      font-size: 2rem;
      color: Blue;
    }

    .box-container {
      display: flex;
      justify-content: center;
      gap: 40px;
      flex-wrap: wrap;
      margin-top: 40px;
    }

    .info-box {
      background: Beige;
      border-radius: 20px;
      padding: 25px;
      width: 280px;
      text-align: left;
      
    }

    .info-box:hover {
      transform: translateY(-10px);
    }

    .info-box h2 {
      color: Blue;
      font-size: 1.3rem;
      margin-bottom: 10px;
    }

    .info-box p {
      font-size: 1rem;
      line-height: 1.5;
    }

    .back-btn {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background-color: Blue;
      color: White;
      border: none;
      padding: 12px 20px;
      border-radius: 10px;
      font-size: 0.9rem;
    }

    .back-btn:hover {
      transform: translateY(-2px);
    }

    .pro-box {
      background: White;
      border-radius: 20px;
      padding: 30px;
      width: 90%;
      max-width: 900px;
      margin-top: 20px;
      text-align: left;
    }

    .pro-box h2 {
      color:Blue;
      margin-bottom: 10px;
    }

    .pro-box ul {
      padding-left: 20px;
      margin: 0 0 20px 0;
    }

    .pro-box li {
      margin-bottom: 8px;
      line-height: 1.5;
    }

    @media (max-width: 700px) {
      .box-container {
        flex-direction: column;
        align-items: center;
      }

      .pro-box {
        padding: 20px;
      }
    }
  </style>
</head>
<body>

  
  <div class="section active" id="welcome">
    <img src="https://i.pinimg.com/736x/dc/31/a6/dc31a6a049e827db0c71391b7c4c2897.jpg" alt="Radhika Loni" class="profile-pic" onclick="showSection('about')">
    <h1>Welcome! Let's know me</h1>
  </div>

  
  <div class="section" id="about">
    <h1>Hello, I'm Radhika Loni</h1>
    <div class="box-container">
      <div class="info-box" onclick="showSection('personal')">
        <h2>Know Me Personally</h2>
        <p>Tap to know my hobbies, traits, values, and fun facts!</p>
      </div>
      <div class="info-box" onclick="showSection('professional')">
        <h2>Know Me Professionally</h2>
        <p>Tap to explore my background, work experience, and skills!</p>
      </div>
    </div>
    <button class="back-btn" onclick="showSection('welcome')">Back</button>
  </div>

  
  <div class="section" id="personal">
    <h1>Know Me Personally</h1>
    <div class="pro-box">
      <h2>Hobbies</h2>
      <ul>
        <li>Swimming</li>
        <li>Travelling</li>
        <li>Cycling</li>
        <li>Badminton</li>
      </ul>

      <h2>Personality Traits</h2>
      <ul>
        <li>Mostly extrovert</li>
        <li>Curious</li>
        <li>Empathetic</li>
      </ul>

      <h2>Values & Beliefs</h2>
      <ul>
        <li>Creativity</li>
        <li>Raising voice for oneself</li>
        <li>Being politically correct when speaking</li>
      </ul>

      <h2>Fun Fact</h2>
      <ul>
        <li>I talk to myself when brainstorming</li>
        
      </ul>
    </div>
    <button class="back-btn" onclick="showSection('about')">Back</button>
  </div>

  
  <div class="section" id="professional">
    <h1>Know Me Professionally</h1>
    <div class="pro-box">
      <h2>Introduction</h2>
      <ul>
        <li><strong>Name:</strong> Radhika Vivekanand Loni</li>
        <li><strong>Email:</strong> radhikaloni1664@gmail.com</li>
        <li><strong>Contact:</strong> +91 7021193182</li>
      </ul>

      <h2>Educational Qualifications</h2>
      <ul>
        <li>Diploma – Agnel Polytechnic Vashi (2017–2020)</li>
        <li>Bachelor’s – Fr. C. Rodrigues Institute of Technology, Vashi (2022–2025)</li>
      </ul>

      <h2>Work Experience</h2>
      <ul>
        <li>Senior Executive – Godrej & Boyce (2020–2022)</li>
        <li>Summer Intern – Nuclear Power Corporation of India Ltd. (June–July 2024)</li>
        <li>Data Analyst Intern – Reliance Jio Infocomm Ltd. (Dec 2024 – Feb 2025)</li>
      </ul>

      <h2>Skills</h2>
      <ul>
        <li>Tableau, PowerBI, HTML, CSS, JavaScript, Python, SQL, KNIME</li>
        
      </ul>
    </div>
    <button class="back-btn" onclick="showSection('about')">Back</button>
  </div>

  <script>
    function showSection(id) {
      document.querySelectorAll('.section').forEach(sec => sec.classList.remove('active'));
      document.getElementById(id).classList.add('active');
    }
  </script>

</body>
</html>

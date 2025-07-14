```<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Velros Portfolio</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin: 0;
      padding: 0;
      background-color: #f5f5f5;
    }
    h1 {
      font-size: 36px;
      color: #333;
      margin-top: 50px;
    }
    p {
      font-size: 18px;
      color: #555;
    }
    .typing-effect {
      font-size: 22px;
      color: #007BFF;
      font-weight: bold;
      display: inline-block;
    }
    .skill-bar-container {
      width: 80%;
      margin: 20px auto;
      text-align: left;
    }
    .skill-bar {
      height: 30px;
      width: 100%;
      background-color: #e0e0e0;
      border-radius: 5px;
      margin-bottom: 15px;
    }
    .skill {
      height: 100%;
      border-radius: 5px;
      text-align: center;
      line-height: 30px;
      color: white;
      font-weight: bold;
    }
    .skill1 { width: 90%; background-color: #4CAF50; }
    .skill2 { width: 80%; background-color: #2196F3; }
    .skill3 { width: 75%; background-color: #FF9800; }
    .skill4 { width: 60%; background-color: #F44336; }
  </style>
</head>
<body>

<h1>Hey there, I'm Velros 👋</h1>
<p align="center">I'm a passionate full-stack web developer with a love for building innovative bots, dashboards, and smart tools that solve real-world problems.</p>

<div class="typing-effect" id="typing-effect"></div>

<h3>🛠 Tech I'm Confident With</h3>

<div class="skill-bar-container">
  <div class="skill-bar">
    <div class="skill skill1">JavaScript (90%)</div>
  </div>
  <div class="skill-bar">
    <div class="skill skill2">Node.js (80%)</div>
  </div>
  <div class="skill-bar">
    <div class="skill skill3">HTML/CSS (75%)</div>
  </div>
  <div class="skill-bar">
    <div class="skill skill4">Python (60%)</div>
  </div>
</div>

<script>
  const typingText = [
    "A self-taught developer",
    "Passionate about clean interfaces",
    "Loves blending creativity with logic",
    "Building bots and AI integrations"
  ];

  let currentTextIndex = 0;
  let currentLetterIndex = 0;
  const typingElement = document.getElementById("typing-effect");

  function typeText() {
    if (currentLetterIndex < typingText[currentTextIndex].length) {
      typingElement.innerHTML += typingText[currentTextIndex].charAt(currentLetterIndex);
      currentLetterIndex++;
      setTimeout(typeText, 100);
    } else {
      setTimeout(() => {
        typingElement.innerHTML = "";
        currentTextIndex = (currentTextIndex + 1) % typingText.length;
        currentLetterIndex = 0;
        typeText();
      }, 2000);
    }
  }

  typeText();
</script>

</body>
</html>


<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>The Sptel Boy – Official Website</title>
  <style>
    body {
      background: linear-gradient(135deg, #ff0000, #000, #ff7300, #111);
      background-size: 400% 400%;
      animation: gradientBG 10s ease infinite;
      color: white;
      font-family: Arial, sans-serif;
      text-align: center;
      margin: 0;
      padding: 0;
    }
    @keyframes gradientBG {
      0% {background-position: 0% 50%;}
      50% {background-position: 100% 50%;}
      100% {background-position: 0% 50%;}
    }
    header {
      padding: 20px;
    }
    header img {
      width: 120px;
      border-radius: 50%;
      border: 4px solid gold;
    }
    header h1 {
      margin: 10px 0 0;
      font-size: 28px;
    }
    .subscribe-btn {
      background: gold;
      color: black;
      font-weight: bold;
      padding: 12px 25px;
      margin-top: 15px;
      border: none;
      border-radius: 8px;
      font-size: 18px;
      cursor: pointer;
    }
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 15px;
      padding: 20px;
    }
    iframe {
      width: 100%;
      height: 200px;
      border: none;
      border-radius: 10px;
    }
    .comments {
      background: rgba(0,0,0,0.5);
      padding: 20px;
      border-radius: 10px;
      margin: 20px;
      max-width: 800px;
      margin-left: auto;
      margin-right: auto;
    }
    .comment {
      text-align: left;
      margin-bottom: 10px;
      padding: 8px;
      background: rgba(255,255,255,0.1);
      border-radius: 6px;
    }
    canvas {
      border: 2px solid white;
      background: #111;
      margin-top: 15px;
    }
  </style>
</head>
<body>

<header>
  <img src="channels4_profile.jpg" alt="The Sptel Boy Logo">
  <h1>The Sptel Boy – Official Website</h1>
  <button class="subscribe-btn" onclick="window.location.href='https://www.youtube.com/@thesptelboy2.030?sub_confirmation=1'">Subscribe</button>
</header>

<h2>Popular Videos</h2>
<div class="grid">
  <iframe src="https://www.youtube.com/embed/ZuZik-WZ_t4?autoplay=1&mute=1&loop=1&playlist=ZuZik-WZ_t4"></iframe>
  <iframe src="https://www.youtube.com/embed/tu9nOe8Q3Ic?autoplay=1&mute=1&loop=1&playlist=tu9nOe8Q3Ic"></iframe>
  <iframe src="https://www.youtube.com/embed/FdY7Bsi4wHk?autoplay=1&mute=1&loop=1&playlist=FdY7Bsi4wHk"></iframe>
  <iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ?autoplay=1&mute=1&loop=1&playlist=dQw4w9WgXcQ"></iframe>
  <iframe src="https://www.youtube.com/embed/kJQP7kiw5Fk?autoplay=1&mute=1&loop=1&playlist=kJQP7kiw5Fk"></iframe>
</div>

<h2>YouTube Shorts</h2>
<div class="grid">
  <iframe src="https://www.youtube.com/embed/4E_ygr1QvlU?autoplay=1&mute=1&loop=1&playlist=4E_ygr1QvlU"></iframe>
  <iframe src="https://www.youtube.com/embed/iJXPzW-n978?autoplay=1&mute=1&loop=1&playlist=iJXPzW-n978"></iframe>
  <iframe src="https://www.youtube.com/embed/Vjz7u9c8O_Q?autoplay=1&mute=1&loop=1&playlist=Vjz7u9c8O_Q"></iframe>
  <iframe src="https://www.youtube.com/embed/O7FK5hQ_YnI?autoplay=1&mute=1&loop=1&playlist=O7FK5hQ_YnI"></iframe>
  <iframe src="https://www.youtube.com/embed/UZVQN07C3Zs?autoplay=1&mute=1&loop=1&playlist=UZVQN07C3Zs"></iframe>
</div>

<h2>Fan Comments</h2>
<div class="comments">
  <div class="comment">🔥 Awesome video! – GamerX</div>
  <div class="comment">😂 That click challenge was fun! – LOLMaster</div>
  <div class="comment">Subbed! Keep up the great work. – NewFan123</div>
  <div class="comment">Your editing is insane! – ProEditor</div>
  <div class="comment">Watched 5 times already – VidLover</div>
  <div class="comment">Next game idea: Jump challenge! – GameSuggestor</div>
  <div class="comment">Legendary channel 👑 – KingFan</div>
  <div class="comment">When's your next stream? – CuriousCat</div>
  <div class="comment">Music choice 🔥 – BeatLover</div>
  <div class="comment">I can't stop playing the game! – AddictGamer</div>
  <div class="comment">The shorts are so funny 😂 – LOLFan</div>
  <div class="comment">You deserve 1M subs – BigSupporter</div>
  <div class="comment">I beat my friend's score! – ScoreBreaker</div>
  <div class="comment">Teach us your tricks – Learner</div>
  <div class="comment">Shoutout pls! – FanBoy</div>
  <div class="comment">Love from India 🇮🇳 – DesiFan</div>
  <div class="comment">Epic win moment – HighlightHunter</div>
  <div class="comment">More collabs please – CollabFan</div>
  <div class="comment">This site is cool! – WebSurfer</div>
  <div class="comment">Best YouTuber ❤️ – LoyalFan</div>
</div>

<h2>Click Challenge Game</h2>
<canvas id="gameCanvas" width="500" height="400"></canvas>
<p>Click the moving logo as many times as you can in 30 seconds!</p>

<script>
const canvas = document.getElementById('gameCanvas');
const ctx = canvas.getContext('2d');
let x = Math.random()*450, y = Math.random()*350, score = 0, timeLeft = 30;

const logo = new Image();
logo.src = 'channels4_profile.jpg';

function draw() {
    ctx.clearRect(0,0,500,400);
    ctx.drawImage(logo, x, y, 50, 50);
    ctx.fillStyle = 'white';
    ctx.font = '18px Arial';
    ctx.fillText(`Score: ${score}`, 10, 20);
    ctx.fillText(`Time: ${timeLeft}`, 420, 20);
}

function moveLogo() {
    x = Math.random()*450;
    y = Math.random()*350;
    draw();
}

canvas.addEventListener('click', function(e) {
    const rect = canvas.getBoundingClientRect();
    const clickX = e.clientX - rect.left;
    const clickY = e.clientY - rect.top;
    if (clickX >= x && clickX <= x+50 && clickY >= y && clickY <= y+50) {
        sc

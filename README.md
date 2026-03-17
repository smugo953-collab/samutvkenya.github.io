<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SAMU TV KENYA</title>

<style>
body {
    font-family: Arial;
    margin: 0;
    background: #f2f2f2;
    transition: 0.3s;
}

/* DARK MODE */
.dark {
    background: #111;
    color: white;
}

/* HEADER */
header {
    background: #002147;
    color: white;
    text-align: center;
    padding: 15px;
}

/* LIVE BADGE */
.live-badge {
    background: red;
    padding: 4px 8px;
    border-radius: 5px;
    animation: blink 1s infinite;
}
@keyframes blink {
    50% {opacity: 0.2;}
}

/* NAV */
nav {
    background: #004080;
    text-align: center;
    padding: 10px;
}
nav a {
    color: white;
    margin: 10px;
    text-decoration: none;
    font-weight: bold;
}

/* TICKER */
.ticker {
    background: black;
    color: #00ffcc;
    overflow: hidden;
    white-space: nowrap;
    padding: 8px;
}
.ticker span {
    display: inline-block;
    padding-left: 100%;
    animation: scroll 15s linear infinite;
}
@keyframes scroll {
    100% { transform: translateX(-100%); }
}

/* VIDEO */
.live-container {
    position: relative;
    padding-top: 56.25%;
}
.live-container iframe {
    position: absolute;
    width: 100%;
    height: 100%;
}

/* BUTTONS */
.controls button {
    margin: 5px;
    padding: 10px;
    border: none;
    background: red;
    color: white;
    cursor: pointer;
    font-weight: bold;
}

/* GRID VIDEOS */
.grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px,1fr));
    gap: 10px;
}
.grid iframe {
    width: 100%;
    height: 150px;
}

/* FOOTER */
footer {
    background: #002147;
    color: white;
    text-align: center;
    padding: 10px;
}

/* MOBILE */
@media(max-width:768px){
    nav a {display:block;}
}
</style>
</head>

<body>

<header>
<h1>📺 SAMU TV KENYA <span class="live-badge">LIVE</span></h1>
</header>

<nav>
<a href="#live">Live</a>
<a href="#videos">Videos</a>
<a href="#news">News</a>
<a href="#contact">Contact</a>
</nav>

<!-- NEWS TICKER -->
<div class="ticker">
<span>🔴 BREAKING: SAMU TV KENYA is now LIVE 24/7 | Stay tuned for news, music & entertainment 🌍</span>
</div>

<main style="padding:20px">

<!-- LIVE -->
<section id="live">
<h2>🔴 LIVE NOW</h2>

<div class="controls">
<button onclick="goFull()">📺 Fullscreen</button>
<button onclick="toggleDark()">🌙 Dark Mode</button>
<button onclick="unmute()">🔊 Sound</button>
</div>

<div class="live-container">
<iframe id="player"
src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU&autoplay=1&loop=1&mute=1"
allow="autoplay"
allowfullscreen></iframe>
</div>

</section>

<!-- VIDEOS -->
<section id="videos">
<h2>🔥 Featured Videos</h2>

<div class="grid">
<iframe src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU"></iframe>
<iframe src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU"></iframe>
<iframe src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU"></iframe>
</div>

</section>

<!-- NEWS -->
<section id="news">
<h2>📰 Latest News</h2>
<p>Stay updated with breaking news across Kenya and worldwide.</p>
</section>

<!-- CONTACT -->
<section id="contact">
<h2>📞 Contact</h2>
<p>Email: info@samutvkenya.co.ke</p>
</section>

</main>

<footer>
© 2026 SAMU TV KENYA
</footer>

<script>
function goFull(){
document.getElementById("player").requestFullscreen();
}

function toggleDark(){
document.body.classList.toggle("dark");
}

function unmute(){
let iframe = document.getElementById("player");
iframe.src = iframe.src.replace("mute=1","mute=0");
}
</script>

</body>
</html><h2>Privacy Policy</h2>
<p>Your privacy matters...</p>

<h2>Terms of Service</h2>
<p>Use this website responsibly...</p>
<link rel="manifest" href="manifest.json">{
  "name": "SAMU TV",
  "short_name": "SAMU TV",
  "start_url": "/",
  "display": "standalone",
  "background_color": "#000",
  "theme_color": "#002147"
}

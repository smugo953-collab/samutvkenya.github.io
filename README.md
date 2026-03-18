<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SAMU TV KENYA</title>
<meta name="description" content="Official website of SAMU TV KENYA – Live news, entertainment, and YouTube playlists.">
<link rel="icon" href="favicon.ico">
<style>
    body { font-family: Arial, sans-serif; margin:0; background:#f2f2f2; color:#333; transition:0.3s; }
    .dark { background:#111; color:white; }
    header { background:#002147; color:white; text-align:center; padding:20px; }
    nav { background:#004080; text-align:center; padding:10px; }
    nav a { color:white; margin:0 15px; text-decoration:none; font-weight:bold; }
    .live-badge { background:red; padding:4px 8px; border-radius:5px; animation:blink 1s infinite; }
    @keyframes blink { 50% { opacity:0.2; } }
    .ticker { background:black; color:#00ffcc; overflow:hidden; white-space:nowrap; padding:8px; }
    .ticker span { display:inline-block; padding-left:100%; animation:scroll 15s linear infinite; }
    @keyframes scroll { 100% { transform:translateX(-100%); } }
    .live-container { position:relative; padding-top:56.25%; margin-bottom:20px; }
    .live-container iframe { position:absolute; width:100%; height:100%; border:0; }
    .controls button { margin:5px; padding:10px; border:none; background:red; color:white; cursor:pointer; font-weight:bold; }
    .grid { display:grid; grid-template-columns:repeat(auto-fit,minmax(200px,1fr)); gap:10px; }
    .grid iframe { width:100%; height:150px; border:0; }
    footer { background:#002147; color:white; text-align:center; padding:15px; margin-top:20px; }
    @media(max-width:768px){ nav a{display:block;margin:10px 0;} }
</style>
</head>
<body>

<header>
    <h1>Welcome to SAMU TV KENYA</h1>
    <p>Your trusted source for news, entertainment, and live streaming</p>
</header>

<nav>
    <a href="#news">News</a>
    <a href="#videos">Videos</a>
    <a href="#live">Live</a>
    <a href="#contact">Contact</a>
</nav>

<section class="ticker">
    <span>🔴 BREAKING: SAMU TV KENYA LIVE 24/7 | Stay tuned for news, music & entertainment 🌍</span>
</section>

<main>
<section id="live">
    <h2>🔴 SAMU TV LIVE</h2>
    <div class="live-container">
        <iframe id="player"
            src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU&autoplay=1&loop=1&mute=1"
            allow="autoplay; fullscreen"
            allowfullscreen>
        </iframe>
    </div>
    <div class="controls">
        <button onclick="goFull()">Fullscreen</button>
        <button onclick="toggleDark()">🌙 Dark Mode</button>
        <button onclick="unmute()">🔊 Sound</button>
    </div>
</section>

<section id="videos">
    <h2>🔥 Featured Videos</h2>
    <div class="grid">
        <iframe src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU" allowfullscreen></iframe>
        <iframe src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU" allowfullscreen></iframe>
        <iframe src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU" allowfullscreen></iframe>
    </div>
</section>

<section id="news">
    <h2>📰 Latest News</h2>
    <p>Stay updated with breaking news across Kenya and worldwide. SAMU TV brings you reliable reporting, interviews, and special coverage from Nairobi and beyond.</p>
</section>

<section id="contact">
    <h2>📞 Contact Us</h2>
    <p>Email: <a href="mailto:info@samutvkenya.co.ke">info@samutvkenya.co.ke</a></p>
</section>
</main>

<footer>
    <p>&copy; 2026 SAMU TV KENYA. All rights reserved.</p>
</footer>

<script>
function goFull(){ document.getElementById("player").requestFullscreen(); }
function toggleDark(){ document.body.classList.toggle("dark"); }
function unmute(){
    let iframe = document.getElementById("player");
    iframe.src = iframe.src.replace("mute=1","mute=0");
}
</script>

</body>
</html>

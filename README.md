
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>SAMU TV KENYA</title>

<meta name="description" content="SAMU TV KENYA – Live 24/7 news, music, entertainment and more.">
<meta name="keywords" content="SAMU TV, Kenya live TV, music, news, entertainment">
<meta name="author" content="SAMU TV KENYA">

<style>
body { font-family: Arial; margin:0; background:#f2f2f2; }
.dark { background:#111; color:white; }

header { background:#002147; color:white; text-align:center; padding:20px; }
nav { background:#004080; text-align:center; padding:10px; }
nav a { color:white; margin:0 15px; text-decoration:none; }

.ticker { background:black; color:#00ffcc; padding:8px; overflow:hidden; white-space:nowrap; }
.ticker span { display:inline-block; padding-left:100%; animation:scroll 20s linear infinite; }
@keyframes scroll { 0%{transform:translateX(100%);} 100%{transform:translateX(-100%);} }

.live-container { position:relative; padding-top:56.25%; }
.live-container iframe { position:absolute; width:100%; height:100%; }

.grid { display:grid; grid-template-columns:repeat(auto-fit,minmax(200px,1fr)); gap:10px; padding:10px; }
.grid iframe { width:100%; height:150px; }

button { padding:10px; margin:5px; background:red; color:white; border:none; border-radius:5px; }

footer { background:#002147; color:white; text-align:center; padding:10px; margin-top:20px; }

#mini-container { position:fixed; bottom:80px; right:20px; width:300px; height:170px; display:none; z-index:9999; }
</style>
</head>

<body>

<header>
<h1>SAMU TV KENYA</h1>
<p>Watch Live 24/7 | Music • News • Entertainment</p>
</header>

<nav>
<a href="#">Home</a>
<a href="#">Videos</a>
<a href="#">Live</a>
</nav>

<div class="ticker">
<span>🔴 LIVE 24/7 SAMU TV KENYA | Stay tuned 🔥</span>
</div>

<h2 style="text-align:center;">🔴 LIVE TV</h2>

<div class="live-container">
<iframe id="player" src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU&autoplay=1&mute=1" allowfullscreen></iframe>
</div>

<div style="text-align:center;">
<button onclick="toggleDark()">🌙 Dark</button>
<button onclick="unmute()">🔊 Sound</button>
<button onclick="openMini()">Mini Player</button>
</div>

<p style="text-align:center; font-weight:bold;">
🔥 Support this movement 👉 
<a href="https://www.youtube.com/" target="_blank">Watch on YouTube</a>
</p>

<h2 style="text-align:center;">🔥 Featured</h2>

<div class="grid">
<iframe src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU"></iframe>
<iframe src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU"></iframe>
</div>

<h2 style="text-align:center;">💰 Support</h2>
<p style="text-align:center;">
<a href="https://www.youtube.com/">👉 Support via YouTube</a><br><br>
<a href="#">🎧 Studio Gear (Affiliate)</a>
</p>

<footer>
© 2026 SAMU TV KENYA
</footer>

<!-- MINI PLAYER -->
<div id="mini-container">
<iframe src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU&autoplay=1&mute=1" allowfullscreen style="width:100%; height:100%;"></iframe>
</div>

<script>
function toggleDark(){ document.body.classList.toggle("dark"); }

function unmute(){
let iframe=document.getElementById("player");
iframe.src=iframe.src.replace("mute=1","mute=0");
}

function openMini(){
let mini=document.getElementById("mini-container");
mini.style.display = mini.style.display==="none" ? "block" : "none";
}
</script>

</body>
</html>
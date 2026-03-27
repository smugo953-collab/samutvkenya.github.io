<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="SAMU TV Kenya – Live streaming, music, news & entertainment.">
<title>SAMU TV KENYA</title>

<style>
body{font-family:Arial,sans-serif;margin:0;background:#f2f2f2;color:#333}
header{background:#002147;color:#fff;text-align:center;padding:20px}
nav{background:#004080;text-align:center;padding:10px}
nav a{color:#fff;margin:0 15px;text-decoration:none;font-weight:bold}
.ticker{background:#000;color:#0ff;padding:8px;text-align:center}
.live-container{position:relative;padding-top:56.25%}
.live-container iframe{position:absolute;width:100%;height:100%;border:0}
.controls{text-align:center;margin:10px}
button{padding:10px;margin:5px;background:red;color:#fff;border:none;border-radius:5px}
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:10px;padding:10px}
.grid iframe{width:100%;height:150px}
footer{background:#002147;color:#fff;text-align:center;padding:15px;margin-top:20px}
</style>
</head>

<body>

<header>
<h1>SAMU TV KENYA</h1>
<nav>
<a href="index.html">Home</a>
<a href="about.html">About</a>
<a href="privacy.html">Privacy</a>
<a href="terms.html">Terms</a>
</nav>
</header>

<div class="ticker">
🔴 SAMU TV KENYA LIVE 24/7 | News • Music • Entertainment
</div>

<section class="live-container">
<iframe id="player"
src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU&autoplay=1&mute=1"
allowfullscreen>
</iframe>
</section>

<div class="controls">
<button onclick="goFull()">Fullscreen</button>
<button onclick="unmute()">🔊 Sound</button>
</div>

<section class="grid">
<h2>🔥 Featured Videos</h2>
<iframe src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU"></iframe>
<iframe src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU"></iframe>
</section>

<footer>
<p>© 2026 SAMU TV KENYA</p>
<p>Email: info@samutvkenya.co.ke</p>
</footer>

<script>
function goFull(){
let iframe=document.getElementById("player");
if(iframe.requestFullscreen){iframe.requestFullscreen();}
}
function unmute(){
let iframe=document.getElementById("player");
iframe.src = iframe.src.replace("mute=1","mute=0");
}
</script>

</body>
</html>
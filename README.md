<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SAMU TV KENYA</title>

<style>
body{font-family:Arial,sans-serif;margin:0;background:#f2f2f2;color:#333}
header{background:#002147;color:#fff;text-align:center;padding:20px}
nav{background:#004080;text-align:center;padding:10px}
nav a{color:#fff;margin:0 15px;text-decoration:none;font-weight:bold}
.ticker{background:#000;color:#0ff;padding:8px;text-align:center}
.live-container{position:relative;padding-top:56.25%;margin:20px}
.live-container iframe{position:absolute;width:100%;height:100%;border:0}
.controls{text-align:center;margin:10px}
button{padding:10px;margin:5px;background:red;color:#fff;border:none;border-radius:5px}
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:10px;padding:10px}
.grid iframe{width:100%;height:150px;border:0}
footer{background:#002147;color:#fff;text-align:center;padding:15px;margin-top:20px}

section{
max-width:900px;
margin:40px auto;
padding:20px;
background:#fff;
border-radius:10px;
}

section h2{
color:#002147;
}

html{
scroll-behavior:smooth;
}
</style>
</head>

<body>

<header>SAMU TV KENYA</header>

<nav>
<a href="#">Home</a>
<a href="#about">About</a>
<a href="#privacy">Privacy</a>
<a href="#terms">Terms</a>
<a href="#contact">Contact</a>
</nav>

<div class="ticker">🔴 SAMU TV KENYA LIVE 24/7 | News • Music • Entertainment</div>

<div class="live-container">
<iframe id="player"
src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU&autoplay=1&mute=1"
allowfullscreen></iframe>
</div>

<div class="controls">
<button onclick="goFull()">Fullscreen</button>
<button onclick="unmute()">Sound</button>
</div>

<h2 style="text-align:center;">🔥 Featured Videos</h2>

<div class="grid">
<iframe src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU"></iframe>
<iframe src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU"></iframe>
</div>

<section id="about">
<h2>About Us</h2>
<p>SAMU TV KENYA is a digital entertainment platform offering live streaming, music, and trending content.</p>
</section>

<section id="privacy">
<h2>Privacy Policy</h2>
<p>We use cookies and third-party advertising services such as Google AdSense to display ads.</p>
</section>

<section id="terms">
<h2>Terms of Service</h2>
<p>By using this website, you agree not to misuse the content.</p>
</section>

<section id="contact">
<h2>Contact</h2>
<p>Email: info@samutvkenya.co.ke<br>WhatsApp: +254 759 821389</p>
</section>

<footer>
© 2026 SAMU TV KENYA
</footer>

<script>
function goFull(){
let iframe=document.getElementById("player");
if(iframe.requestFullscreen){iframe.requestFullscreen();}
}

function unmute(){
let iframe=document.getElementById("player");
iframe.src=iframe.src.replace("mute=1","mute=0");
}
</script>

</body>
</html>
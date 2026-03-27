<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Samu TV Kenya: Live news, music, and entertainment content.">
<meta name="robots" content="index, follow">

<meta property="og:title" content="Samu TV Kenya">
<meta property="og:description" content="Live news, music, and entertainment content from Kenya.">
<meta property="og:image" content="images/og-image.jpg">
<meta property="og:url" content="https://samutvkenya.github.io/">

<title>SAMU TV KENYA</title>

<link rel="stylesheet" href="css/style.css">
<style>
/* --- Basic Styling --- */
body{font-family:Arial,sans-serif;margin:0;background:#f2f2f2;color:#333;transition:0.3s}.dark{background:#111;color:#fff}header{background:#002147;color:#fff;text-align:center;padding:20px}nav{background:#004080;text-align:center;padding:10px}nav a{color:#fff;margin:0 15px;text-decoration:none;font-weight:bold}nav a:hover{text-decoration:underline}.live-badge{background:red;padding:4px 8px;border-radius:5px;animation:blink 1s infinite}@keyframes blink{50%{opacity:0.2}}.ticker{background:#000;color:#0ff;overflow:hidden;white-space:nowrap;padding:8px;font-weight:bold}.ticker span{display:inline-block;padding-left:100%;animation:scroll 20s linear infinite}@keyframes scroll{0%{transform:translateX(100%)}100%{transform:translateX(-100%)}}.live-container{position:relative;padding-top:56.25%;margin-bottom:20px}.live-container iframe{position:absolute;width:100%;height:100%;border:0}.controls button{margin:5px;padding:10px;border:none;background:red;color:#fff;cursor:pointer;font-weight:bold;border-radius:5px}.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:10px}.grid iframe{width:100%;height:150px;border:0}footer{background:#002147;color:#fff;text-align:center;padding:15px;margin-top:20px}@media(max-width:768px){nav a{display:block;margin:10px 0}}.mini-hidden{opacity:0;transition:opacity .3s}.merch-section{padding:20px;background-color:#f9f9f9}.merch-section h2{text-align:center;margin-bottom:20px}.merch-container{display:flex;flex-wrap:wrap;justify-content:center;gap:20px}.merch-item{border:1px solid #ccc;padding:10px;text-align:center;width:200px;border-radius:8px;background:#fff}.merch-item img{max-width:100%;border-radius:5px;margin-bottom:10px}.merch-item a{display:inline-block;margin-top:5px;padding:5px 10px;background:#004080;color:#fff;text-decoration:none;border-radius:4px}.merch-item a:hover{background:#002147}
</style>
</head>
<body>

<header>
<h1>SAMU TV KENYA</h1>
<nav>
<a href="index.html">Home</a> | 
<a href="about.html">About</a> | 
<a href="privacy.html">Privacy Policy</a> | 
<a href="terms.html">Terms</a>
</nav>
</header>

<div class="ticker"><span>🔴 BREAKING: SAMU TV KENYA LIVE 24/7 | Stay tuned for news, music & entertainment 🌍</span></div>

<section class="live-container">
<iframe id="player" src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU&autoplay=1&loop=1&mute=1" allow="autoplay; fullscreen" allowfullscreen></iframe>
</section>

<div class="controls">
<button onclick="goFull()">Fullscreen</button>
<button onclick="toggleDark()">🌙 Dark Mode</button>
<button onclick="unmute()">🔊 Sound</button>
</div>

<section class="grid">
<h2>🔥 Featured Videos</h2>
<iframe src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU" allowfullscreen></iframe>
<iframe src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU" allowfullscreen></iframe>
<iframe src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU" allowfullscreen></iframe>
</section>

<section class="merch-section">
<h2>🎬 Official SAMU TV Merchandise</h2>
<div class="merch-container">
<div class="merch-item">
<img src="merchandise/tshirts/sample1.jpg" alt="SAMU TV T-Shirt">
<p>Official SAMU TV T-Shirt - KSh 1,500</p>
<a href="https://wa.me/YOUR_NUMBER?text=I+want+to+buy+this+T-shirt" target="_blank">Order via WhatsApp</a>
</div>
<div class="merch-item">
<img src="merchandise/hoodies/sample2.jpg" alt="SAMU TV Hoodie">
<p>Official SAMU TV Hoodie - KSh 2,500</p>
<a href="https://wa.me/YOUR_NUMBER?text=I+want+to+buy+this+Hoodie" target="_blank">Order via WhatsApp</a>
</div>
<div class="merch-item">
<img src="merchandise/posters/sample3.jpg" alt="SAMU TV Poster">
<p>SAMU TV Poster - KSh 500</p>
<a href="https://wa.me/YOUR_NUMBER?text=I+want+to+buy+this+Poster" target="_blank">Order via WhatsApp</a>
</div>
</div>
</section>

<section id="adsense-section">
<!-- AdSense Placeholder -->
<div class="adsense-placeholder">
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
<ins class="adsbygoogle"
     style="display:block"
     data-ad-client="ca-pub-XXXXXXXXXXXXXXX"
     data-ad-slot="XXXXXXXXXX"
     data-ad-format="auto"
     data-full-width-responsive="true"></ins>
<script>
     (adsbygoogle = window.adsbygoogle || []).push({});
</script>
</div>
</section>

<footer>
<p>© 2026 SAMU TV KENYA. All rights reserved.</p>
<p>Email: info@samutvkenya.co.ke</p>
</footer>

<script>
// --- Player Controls ---
function goFull(){ let iframe=document.getElementById("player"); if(iframe.requestFullscreen){iframe.requestFullscreen();} }
function toggleDark(){ document.body.classList.toggle("dark"); }
function unmute(){ let iframe=document.getElementById("player"); iframe.src = iframe.src.replace("mute=1","mute=0"); }

// --- Auto Dark Mode ---
let hour=new Date().getHours(); if(hour>=18||hour<6){document.body.classList.add("dark");}

// --- Draggable mini-player, schedule ticker, and other scripts can be added here ---
</script>

</body>
</html>
}<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="About SAMU TV Kenya – Live news, entertainment, and music.">
<title>About SAMU TV Kenya</title>
<link rel="stylesheet" href="css/style.css">
</head>
<body>

<header>
<h1>SAMU TV KENYA</h1>
<nav>
<a href="index.html">Home</a> | 
<a href="about.html">About</a> | 
<a href="privacy.html">Privacy Policy</a> | 
<a href="terms.html">Terms</a>
</nav>
</header>

<main>
<h2>About SAMU TV Kenya</h2>
<p>SAMU TV Kenya is your trusted source for live news, music, and entertainment content from Kenya. We bring you trending videos, live streaming, interviews, and exclusive coverage from Nairobi and beyond.</p>

<section id="adsense-section">
<!-- AdSense Placeholder -->
<div class="adsense-placeholder">
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
<ins class="adsbygoogle"
     style="display:block"
     data-ad-client="ca-pub-XXXXXXXXXXXXXXX"
     data-ad-slot="XXXXXXXXXX"
     data-ad-format="auto"
     data-full-width-responsive="true"></ins>
<script>
     (adsbygoogle = window.adsbygoogle || []).push({});
</script>
</div>
</section>

</main>

<footer>
<p>© 2026 SAMU TV KENYA. All rights reserved.</p>
<p>Email: info@samutvkenya.co.ke</p>
</footer>

</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="About SAMU TV Kenya – Live news, entertainment, and music.">
<title>About SAMU TV Kenya</title>
<link rel="stylesheet" href="css/style.css">
</head>
<body>

<header>
<h1>SAMU TV KENYA</h1>
<nav>
<a href="index.html">Home</a> | 
<a href="about.html">About</a> | 
<a href="privacy.html">Privacy Policy</a> | 
<a href="terms.html">Terms</a>
</nav>
</header>

<main>
<h2>About SAMU TV Kenya</h2>
<p>SAMU TV Kenya is your trusted source for live news, music, and entertainment content from Kenya. We bring you trending videos, live streaming, interviews, and exclusive coverage from Nairobi and beyond.</p>

<section id="adsense-section">
<!-- AdSense Placeholder -->
<div class="adsense-placeholder">
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
<ins class="adsbygoogle"
     style="display:block"
     data-ad-client="ca-pub-XXXXXXXXXXXXXXX"
     data-ad-slot="XXXXXXXXXX"
     data-ad-format="auto"
     data-full-width-responsive="true"></ins>
<script>
     (adsbygoogle = window.adsbygoogle || []).push({});
</script>
</div>
</section>

</main>

<footer>
<p>© 2026 SAMU TV KENYA. All rights reserved.</p>
<p>Email: info@samutvkenya.co.ke</p>
</footer>

</body>
</html>https://samutvkenya.github.io/
https://samutvkenya.github.io/about.html
https://samutvkenya.github.io/privacy.html
https://samutvkenya.github.io/terms.html
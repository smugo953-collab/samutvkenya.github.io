<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SAMU TV KENYA</title>
<style>
body { font-family: Arial, sans-serif; margin:0; background:#f2f2f2; color:#333; transition:0.3s; }
.dark { background:#111; color:white; }
header { background:#002147; color:white; text-align:center; padding:20px; }
nav { background:#004080; text-align:center; padding:10px; }
nav a { color:white; margin:0 15px; text-decoration:none; font-weight:bold; }
.live-badge { background:red; padding:4px 8px; border-radius:5px; animation:blink 1s infinite; }
@keyframes blink { 50% { opacity:0.2; } }
.ticker { background:black; color:#00ffcc; overflow:hidden; white-space:nowrap; padding:8px; font-weight:bold; }
.ticker span { display:inline-block; padding-left:100%; animation:scroll 20s linear infinite; }
@keyframes scroll { 0% { transform:translateX(100%);} 100% { transform:translateX(-100%); } }
.live-container { position:relative; padding-top:56.25%; margin-bottom:20px; }
.live-container iframe { position:absolute; width:100%; height:100%; border:0; }
.controls button { margin:5px; padding:10px; border:none; background:red; color:white; cursor:pointer; font-weight:bold; border-radius:5px; }
.grid { display:grid; grid-template-columns:repeat(auto-fit,minmax(200px,1fr)); gap:10px; }
.grid iframe { width:100%; height:150px; border:0; }
footer { background:#002147; color:white; text-align:center; padding:15px; margin-top:20px; }
@media(max-width:768px){ nav a{display:block;margin:10px 0;} }
.mini-hidden { opacity:0; transition:opacity 0.3s; }
</style>
</head>
<body>

<header>
  <h1>SAMU TV KENYA</h1>
  <p>Your trusted source for news, entertainment, and live streaming</p>
</header>

<nav>
  <a href="#">News</a>
  <a href="#">Videos</a>
  <a href="#">Live</a>
  <a href="#">Contact</a>
</nav>

<div class="ticker">
  <span>🔴 BREAKING: SAMU TV KENYA LIVE 24/7 | Stay tuned for news, music & entertainment 🌍</span>
</div>

<main>
  <section>
    <h2>🔴 SAMU TV LIVE</h2>
    <div class="live-container">
      <!-- Main live player (YouTube ready) -->
      <iframe id="player" src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU&autoplay=1&loop=1&mute=1" allow="autoplay; fullscreen" allowfullscreen></iframe>
    </div>
    <div class="controls">
      <button onclick="goFull()">Fullscreen</button>
      <button onclick="toggleDark()">🌙 Dark Mode</button>
      <button onclick="unmute()">🔊 Sound</button>
    </div>
  </section>

  <section>
    <h2>🔥 Featured Videos</h2>
    <div class="grid">
      <iframe src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU" allowfullscreen></iframe>
      <iframe src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU" allowfullscreen></iframe>
      <iframe src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU" allowfullscreen></iframe>
    </div>
  </section>

  <section>
    <h2>📰 Latest News</h2>
    <p>Stay updated with breaking news across Kenya and worldwide. SAMU TV brings you reliable reporting, interviews, and special coverage from Nairobi and beyond.</p>
  </section>

  <section>
    <h2>📺 Upcoming Shows</h2>
    <div class="ticker" id="schedule-ticker">
      <span>Loading schedule...</span>
    </div>
  </section>

  <section>
    <h2>📡 Watch SAMU TV on Multiple Platforms</h2>
    <div class="grid">
      <!-- For now, all point to YouTube. Replace later with Restream URLs -->
      <iframe src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU" allowfullscreen></iframe>
      <iframe src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU" allowfullscreen></iframe>
      <iframe src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU" allowfullscreen></iframe>
      <iframe src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU" allowfullscreen></iframe>
    </div>
  </section>

  <section>
    <h2>📞 Contact Us</h2>
    <p>Email: info@samutvkenya.co.ke</p>
  </section>
</main>

<footer>
  © 2026 SAMU TV KENYA. All rights reserved.
</footer>

<!-- Floating Mini-Player Button -->
<div id="mini-player" style="position:fixed; bottom:20px; right:20px; width:80px; height:45px; background:red; border-radius:8px; cursor:pointer; display:flex; align-items:center; justify-content:center; color:white; font-weight:bold; z-index:9999;">
  LIVE
</div>

<!-- Mini player container -->
<div id="mini-container" style="position:fixed; width:300px; height:170px; display:none; border:2px solid #004080; border-radius:8px; z-index:9998; overflow:hidden; cursor:move;">
  <iframe id="mini-iframe" src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU&autoplay=1&mute=1" frameborder="0" allow="autoplay; fullscreen" allowfullscreen style="width:100%; height:100%;"></iframe>
</div>

<script>
// Fullscreen
function goFull(){ let iframe=document.getElementById("player"); if(iframe.requestFullscreen){ iframe.requestFullscreen(); } }
// Dark Mode toggle
function toggleDark(){ document.body.classList.toggle("dark"); }
// Unmute
function unmute(){ let iframe=document.getElementById("player"); iframe.src = iframe.src.replace("mute=1","mute=0"); }

// Auto Dark Mode
let hour=new Date().getHours();
if(hour>=18 || hour<6){ document.body.classList.add("dark"); }

// Ticker refresh
function refreshTicker(){ document.querySelectorAll('.ticker span').forEach(t=>t.innerHTML=t.innerHTML); }
setInterval(refreshTicker, 20000);

// Schedule
const schedule=[{time:"06:00",show:"Morning News"},{time:"08:00",show:"Music Hour"},{time:"10:00",show:"Interviews & Talks"},{time:"12:00",show:"Live Sports"},{time:"14:00",show:"Entertainment Blast"},{time:"16:00",show:"Afternoon News"},{time:"18:00",show:"Evening Music"},{time:"20:00",show:"Prime Time Live"},{time:"22:00",show:"Night Highlights"}];
function timeToMinutes(str){ const [h,m]=str.split(":").map(Number); return h*60+m; }
function currentMinutes(){ const now=new Date(); return now.getHours()*60+now.getMinutes(); }
function updateScheduleTicker(){ const ticker=document.getElementById("schedule-ticker").querySelector("span"); const nowMin=currentMinutes(); ticker.innerHTML=schedule.map((item,i)=>{ const start=timeToMinutes(item.time); const nextStart=i<schedule.length-1?timeToMinutes(schedule[i+1].time):1440; return nowMin>=start && nowMin<nextStart ? `🕒 ${item.time} - <strong>${item.show} (Now Live)</strong> ` : `🕒 ${item.time} - ${item.show} `; }).join(" | "); }
updateScheduleTicker();
setInterval(updateScheduleTicker,60000);

// Mini-player toggle
const miniBtn=document.getElementById("mini-player");
const mini=document.getElementById("mini-container");
miniBtn.addEventListener("click",()=>{ mini.style.display=mini.style.display==="none"?"block":"none"; });

// Draggable + snap + persistent + auto-hide
let isDragging=false,offsetX=0,offsetY=0;
const saved=localStorage.getItem("miniPlayerPos");
if(saved){ const pos=JSON.parse(saved); mini.style.left=pos.left+"px"; mini.style.top=pos.top+"px"; } else { mini.style.right="20px"; mini.style.bottom="80px"; }
function savePosition(){ const rect=mini.getBoundingClientRect(); localStorage.setItem("miniPlayerPos",JSON.stringify({left:rect.left,top:rect.top})); }
function snapToCorner(){ const vw=window.innerWidth,vh=window.innerHeight,rect=mini.getBoundingClientRect(); const centerX=rect.left+rect.width/2,centerY=rect.top+rect.height/2; let finalX=centerX<vw/2?0:vw-rect.width; let finalY=centerY<vh/2?0:vh-rect.height; mini.style.transition="left 0.2s, top 0.2s"; mini.style.left=finalX+"px"; mini.style.top=finalY+"px"; setTimeout(()=>{ mini.style.transition=""; savePosition(); },250); }
mini.addEventListener("mousedown",e=>{ isDragging=true; offsetX=e.clientX-mini.getBoundingClientRect().left; offsetY=e.clientY-mini.getBoundingClientRect().top; });
document.addEventListener("mouseup",()=>{ if(isDragging)snapToCorner(); isDragging=false; });
document.addEventListener("mousemove",e=>{ if(!isDragging)return; let x=e.clientX-offsetX; let y=e.clientY-offsetY; x=Math.max(0,Math.min(window.innerWidth-mini.offsetWidth,x)); y=Math.max(0,Math.min(window.innerHeight-mini.offsetHeight,y)); mini.style.left=x+"px"; mini.style.top=y+"px"; });
mini.addEventListener("touchstart",e=>{ isDragging=true; const t=e.touches[0]; offsetX=t.clientX-mini.getBoundingClientRect().left; offsetY=t.clientY-mini.getBoundingClientRect().top; },{passive:false});
mini.addEventListener("touchend",()=>{ if(isDragging)snapToCorner(); isDragging=false; });
mini.addEventListener("touchmove",e=>{ if(!isDragging)return; e.preventDefault(); const t=e.touches[0]; let x=t.clientX-offsetX; let y=t.clientY-offsetY; x=Math.max(0,Math.min(window.innerWidth-mini.offsetWidth,x)); y=Math.max(0,Math.min(window.innerHeight-mini.offsetHeight,y)); mini.style.left=x+"px"; mini.style.top=y+"px"; });
let hideTimeout;
function resetHide(){ mini.classList.remove("mini-hidden"); clearTimeout(hideTimeout); hideTimeout=setTimeout(()=>mini.classList.add("mini-hidden"),5000); }
mini.addEventListener("mouseenter",()=>{ mini.classList.remove("mini-hidden"); clearTimeout(hideTimeout); });
mini.addEventListener("mouseleave",resetHide);
document.addEventListener("mousemove",resetHide);
document.addEventListener("touchstart",resetHide);
resetHide();
</script>

</body>
</html><meta name="description" content="SAMU TV KENYA – Your trusted source for live news, entertainment, music, and sports. Watch live streams, featured videos, and breaking news from Nairobi and across Kenya 24/7.">
<meta name="keywords" content="SAMU TV, Kenya live TV, news, music, sports, entertainment, live streaming, Nairobi, African TV">
<meta name="author" content="SAMU TV KENYA"><header>
  <h1>SAMU TV KENYA</h1>
  <p>Your trusted source for news, entertainment, and live streaming</p>
  <p>🎬 Watch SAMU TV KENYA live 24/7! Enjoy breaking news, music, sports, interviews, and exclusive Kenyan entertainment, all in one place.</p>
</header>
<!-- Merchandise Section -->
<section class="merch-section">
    <h2>Official SAMU TV Merchandise</h2>
    <div class="merch-container">

        <!-- Merch Item 1 -->
        <div class="merch-item">
            <img src="merchandise/tshirts/sample1.jpg" alt="SAMU TV T-Shirt">
            <p>Official SAMU TV T-Shirt - KSh 1,500</p>
            <a href="https://wa.me/YOUR_NUMBER?text=I+want+to+buy+this+T-shirt" target="_blank">Order via WhatsApp</a>
        </div>

        <!-- Merch Item 2 -->
        <div class="merch-item">
            <img src="merchandise/hoodies/sample2.jpg" alt="SAMU TV Hoodie">
            <p>Official SAMU TV Hoodie - KSh 2,500</p>
            <a href="https://wa.me/YOUR_NUMBER?text=I+want+to+buy+this+Hoodie" target="_blank">Order via WhatsApp</a>
        </div>

        <!-- Merch Item 3 -->
        <div class="merch-item">
            <img src="merchandise/posters/sample3.jpg" alt="SAMU TV Poster">
            <p>SAMU TV Poster - KSh 500</p>
            <a href="https://wa.me/YOUR_NUMBER?text=I+want+to+buy+this+Poster" target="_blank">Order via WhatsApp</a>
        </div>

        .merch-section {
    padding: 20px;
    background-color: #f9f9f9;
}

.merch-section h2 {
    text-align: center;
    margin-bottom: 20px;
}

.merch-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
}

.merch-item {
    border: 1px solid #ccc;
    padding: 10px;
    text-align: center;
    width: 200px;
    border-radius: 8px;
    background-color: white;
}

.merch-item img {
    max-width: 100%;
    border-radius: 5px;
    margin-bottom: 10px;
}

.merch-item a {
    display: inline-block;
    margin-top: 5px;
    padding: 5px 10px;
    background-color: #004080;
    color: white;
    text-decoration: none;
    border-radius: 4px;
}

.merch-item a:hover {
    background-color: #002147;
}
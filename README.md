
}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SAMU TV KENYA</title>
    <meta name="description" content="Official website of SAMU TV KENYA – Latest news, videos, and live streaming from Nairobi and beyond.">
    <link rel="icon" href="favicon.ico">
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            background-color: #f2f2f2;
            color: #333;
            transition: 0.3s;
        }
        /* DARK MODE */
        .dark { background-color: #111; color: #fff; }

        /* HEADER */
        header {
            background-color: #002147;
            color: white;
            text-align: center;
            padding: 20px;
        }
        header img { max-width: 150px; margin-bottom: 10px; }

        /* LIVE BADGE */
        .live-badge {
            background: red;
            color: white;
            padding: 4px 8px;
            border-radius: 5px;
            animation: blink 1s infinite;
            font-weight: bold;
        }
        @keyframes blink { 50% { opacity: 0.2; } }

        /* NAVIGATION */
        nav {
            background-color: #004080;
            text-align: center;
            padding: 10px;
        }
        nav a {
            color: white;
            margin: 0 15px;
            text-decoration: none;
            font-weight: bold;
        }
        @media(max-width:768px){ nav a { display:block; margin:10px 0; } }

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
        @keyframes scroll { 100% { transform: translateX(-100%); } }

        /* MAIN SECTIONS */
        main { padding: 20px; }
        section { margin-bottom: 30px; }

        /* LIVE VIDEO */
        .live-container {
            position: relative;
            padding-top: 56.25%;
        }
        .live-container iframe {
            position: absolute;
            top: 0; left: 0;
            width: 100%;
            height: 100%;
        }

        /* VIDEO GRID */
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px,1fr));
            gap: 10px;
        }
        .grid iframe { width: 100%; height: 150px; }

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

        /* FOOTER */
        footer {
            background-color: #002147;
            color: white;
            text-align: center;
            padding: 15px;
        }
    </style>
</head>
<body>
    <header>
        <img src="a_vector_style_digital_logo_for_samu_tv_kenya_feat.png" alt="SAMU TV KENYA Logo">
        <h1>Welcome to SAMU TV KENYA</h1>
        <p>Your trusted source for news, entertainment, and live streaming</p>
    </header>

    <nav>
        <a href="#news">News</a>
        <a href="#videos">Videos</a>
        <a href="#live">Live</a>
        <a href="#contact">Contact</a>
    </nav>

    <div class="ticker">
        <span>🔴 BREAKING: SAMU TV KENYA is now LIVE 24/7 | Stay tuned for news, music & entertainment 🌍</span>
    </div>

    <main>
        <section id="news">
            <h2>📰 Latest News</h2>
            <p>Stay updated with the most recent happenings in Nairobi, Kenya, and worldwide. SAMU TV brings you breaking news, in-depth reports, and exclusive interviews from trusted sources.</p>
        </section>

        <section id="videos">
            <h2>🔥 Featured Videos</h2>
            <div class="grid">
                <iframe src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU" allowfullscreen></iframe>
                <iframe src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU" allowfullscreen></iframe>
                <iframe src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU" allowfullscreen></iframe>
            </div>
        </section>

        <section id="live">
            <h2>🔴 SAMU TV LIVE</h2>
            <div class="controls">
                <button onclick="goFull()">📺 Fullscreen</button>
                <button onclick="toggleDark()">🌙 Dark Mode</button>
                <button onclick="unmute()">🔊 Sound</button>
            </div>
            <div class="live-container">
                <iframe id="player" src="https://www.youtube.com/embed/videoseries?list=PLazHNRREZJPvUAMd3K2HuSqxZJVSR5BdU&autoplay=1&loop=1&mute=1" allow="autoplay" allowfullscreen></iframe>
            </div>
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
</html>

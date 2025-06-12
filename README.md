<!DOCTYPE html>
<html lang="zh-Hant">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>水母特集</title>
  <style>
    body {
      margin: 0;
      font-family: "Noto Sans TC", sans-serif;
      transition: background-color 0.5s, color 0.5s;
    }

    header {
      text-align: center;
      padding: 30px 10px;
    }

    header h1 {
      font-size: 3em;
      margin-bottom: 10px;
    }

    .theme-switcher {
      text-align: center;
      margin-bottom: 20px;
    }

    .theme-switcher button {
      padding: 10px 20px;
      font-size: 1em;
      margin: 0 10px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: background 0.3s;
    }

    .theme-cute {
      background-color: #003366;
      color: white;
    }

    .theme-cute header {
      background-color: rgba(0, 80, 150, 0.7);
    }

    .theme-cute button {
      background-color: #66ccff;
      color: #003366;
    }

    .theme-cute button:hover {
      background-color: #99ddff;
    }

    .theme-dark {
      background-color: #0a0a0a;
      color: #ff6699;
    }

    .theme-dark header {
      background-color: rgba(80, 0, 80, 0.7);
    }

    .theme-dark button {
      background-color: #990033;
      color: white;
    }

    .theme-dark button:hover {
      background-color: #cc3366;
    }

    video {
      display: block;
      margin: 20px auto;
      width: 80%;
      max-width: 800px;
      border-radius: 12px;
      box-shadow: 0 0 15px rgba(255, 255, 255, 0.3);
    }

    .gallery {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
      padding: 30px;
    }

    .gallery img {
      width: 300px;
      border-radius: 15px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
      transition: transform 0.3s;
    }

    .gallery img:hover {
      transform: scale(1.05);
    }

    footer {
      text-align: center;
      padding: 20px;
      font-size: 0.9em;
    }
  </style>
</head>
<body class="theme-cute">
  <header>
    <h1 id="main-title">水母的可愛療癒特集</h1>
    <p id="main-description">看著柔軟漂浮的水母，放鬆你的心靈。</p>
  </header>

  <div class="theme-switcher">
    <button onclick="switchTheme('cute')">可愛療癒</button>
    <button onclick="switchTheme('dark')">危險神秘</button>
  </div>

  <main>
    <video controls autoplay loop muted>
      <source src="856882-hd_1920_1080_24fps.mp4" type="video/mp4" />
      您的瀏覽器不支援影片播放。
    </video>

    <section class="gallery">
      <img src="pexels-hungtran-3699437.jpg" alt="漂浮的水母" />
      <img src="pexels-pspov-3046581.jpg" alt="藍色的深海水母" />
      <img src="pexels-ryutaro-5220010.jpg" alt="神秘的水母群" />
    </section>
  </main>

  <footer>
    &copy; 2025 水母觀察站｜本網站為學習用途製作
  </footer>

  <script>
    function switchTheme(theme) {
      const body = document.body;
      const title = document.getElementById("main-title");
      const desc = document.getElementById("main-description");

      if (theme === 'cute') {
        body.className = "theme-cute";
        title.textContent = "水母的可愛療癒特集";
        desc.textContent = "看著柔軟漂浮的水母，放鬆你的心靈。";
      } else if (theme === 'dark') {
        body.className = "theme-dark";
        title.textContent = "水母的危險神秘特集";
        desc.textContent = "潛入深海，探索水母的黑暗與奇幻。";
      }
    }
  </script>
</body>
</html>

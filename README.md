<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Rei Tsukumo Art Commissions</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <!-- Cute Google Font: QUICKSAND -->
  <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@300;400;500;600&display=swap" rel="stylesheet" />

  <style>
    :root {
      --pink-light: #ffe6f2;
      --pink-main: #ffb6d9;
      --pink-hot:  #ff6fa9;
      --pink-deep: #f25a92;
      --white: #ffffff;
      --text-main: #4c2740;
      --shadow-soft: 0 8px 20px rgba(255, 167, 211, 0.5);
      --radius-big: 1.75rem;
      --radius-small: 1rem;
    }

    body {
      font-family: "Quicksand", sans-serif;
      background: radial-gradient(circle at top left, #ffeaf5 0, #ffd8f2 35%, #ffc2e4 70%, #ffb0da 100%);
      color: var(--text-main);
      margin: 0;
      padding: 0;
    }

    /* Floating BACK TO TOP button */
    #topBtn {
      position: fixed;
      bottom: 30px;
      right: 30px;
      background: var(--pink-hot);
      color: white;
      border: none;
      padding: 12px 15px;
      border-radius: 50%;
      font-size: 18px;
      cursor: pointer;
      box-shadow: var(--shadow-soft);
      z-index: 999;
      display: none;
      transition: transform .2s;
    }

    #topBtn:hover {
      transform: translateY(-4px) scale(1.05);
      background: var(--pink-deep);
    }

    /* --- EXISTING STYLES (FROM PREVIOUS VERSION) --- */
    .page-wrapper { max-width: 1100px; margin: 0 auto; padding: 1.5rem; }
    header {
      display: flex; justify-content: space-between; align-items: center;
      padding: .75rem 1.25rem; margin-bottom: 1.5rem;
      background: rgba(255,255,255,0.7); backdrop-filter: blur(10px);
      border-radius: 999px; box-shadow: var(--shadow-soft);
      position: sticky; top: 0.75rem; z-index: 10;
    }
    .logo { display: flex; align-items: center; gap: .5rem; font-weight: 600; font-size: 1.2rem; }
    .logo-badge {
      width: 32px; height: 32px; border-radius: 999px;
      background: linear-gradient(135deg, var(--pink-main), var(--pink-hot));
      display: flex; align-items: center; justify-content: center;
      color: var(--white); box-shadow: 0 0 0 3px #ffe9f7;
    }
    nav { display: flex; gap: .5rem; font-size: .95rem; }
    .nav-link { padding: .4rem .85rem; border-radius: 999px; cursor: pointer; }
    .nav-link:hover { background: rgba(255,182,217,0.6); }
    .nav-link.primary { background: var(--pink-hot); color: white; }

    main { display: flex; flex-direction: column; gap: 2.5rem; }

    section {
      background: rgba(255,255,255,0.85);
      padding: 1.75rem 1.5rem;
      border-radius: var(--radius-big);
      box-shadow: var(--shadow-soft);
      position: relative;
      overflow: hidden;
    }

    .section-title {
      font-size: 1.7rem;
      margin-bottom: .5rem;
      display: flex; align-items: center; gap: .5rem;
    }

    .hero { display: grid; grid-template-columns: 1.2fr 1fr; gap: 2rem; }
    .hero-pill {
      background: rgba(255,255,255,0.9); padding: .4rem .9rem;
      border-radius: 999px; font-size: .85rem;
      margin-bottom: .7rem; box-shadow: var(--shadow-soft);
    }

    .hero-title { font-size: 2.3rem; }
    .hero-text { font-size: 1rem; }

    .btn {
      display: inline-flex; padding: .6rem 1.3rem;
      border: none; border-radius: 999px;
      cursor: pointer; font-size: 1rem;
      transition: transform .15s;
    }

    .btn-primary { background: var(--pink-deep); color: white; }
    .btn-primary:hover { transform: translateY(-3px); }

    .btn-ghost { border: 2px dashed var(--pink-main); background: white; }
    .btn-ghost:hover { background: var(--pink-light); }

    .gallery-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(180px,1fr)); gap: 1rem; }

    .art-card {
      background: var(--pink-light);
      border-radius: var(--radius-small);
      overflow: hidden;
      box-shadow: var(--shadow-soft);
    }

    .commission-layout {
      display: grid; grid-template-columns: repeat(auto-fit,minmax(250px,1fr)); gap: 1rem;
    }

    /* CONTACT FORM */
    .contact-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; }
    .contact-card { background: white; padding: 1rem; border-radius: 1rem; box-shadow: var(--shadow-soft); }

    select, input, textarea {
      width: 100%; padding: .6rem; border-radius: .8rem;
      border: 1px solid var(--pink-main); font-family: "Quicksand"; font-size: .9rem;
    }

    select:focus, input:focus, textarea:focus {
      border-color: var(--pink-hot);
      box-shadow: 0 0 0 3px rgba(255,165,210,0.4);
      outline: none;
    }

    footer { text-align: center; padding: 2rem; opacity: 0.7; }

    @media(max-width: 800px) {
      .hero { grid-template-columns: 1fr; }
      .contact-grid { grid-template-columns: 1fr; }
    }
  </style>
</head>

<body>

<!-- FLOATING TOP BUTTON -->
<button onclick="scrollToTop()" id="topBtn">↑</button>

<script>
  window.onscroll = function() {
    document.getElementById("topBtn").style.display =
      (document.documentElement.scrollTop > 200) ? "block" : "none";
  };

  function scrollToTop() {
    window.scrollTo({ top: 0, behavior: 'smooth' });
  }
</script>

<div class="page-wrapper">

  <!-- HEADER -->
  <header>
    <div class="logo">
      <div class="logo-badge">✿</div>
      <span>Rei Tsukumo Art</span>
    </div>
    <nav>
      <a href="#home" class="nav-link">Home</a>
      <a href="#gallery" class="nav-link">Gallery</a>
      <a href="#commissions" class="nav-link">Commissions</a>
      <a href="#about" class="nav-link">About</a>
      <a href="#contact" class="nav-link primary">Contact</a>
    </nav>
  </header>

  <!-- HERO -->
  <section id="home">
    <div class="hero">
      <div>
        <div class="hero-pill">💕 Commissions OPEN! (˶˃ ᵕ ˂˶)♡</div>
        <h1 class="hero-title">Anime & NSFW (18+) Art Commissions</h1>
        <p class="hero-text">
          Hi, I’m <strong>Rei Tsukumo (津雲 玲)</strong> — an anime-based digital artist offering
          SFW and NSFW (18+) commissions for all genders and character types.
        </p>
        <button class="btn btn-primary" onclick="location.href='#commissions'">View Prices</button>
        <button class="btn btn-ghost" onclick="location.href='#gallery'">See My Art</button>
      </div>
      <div></div>
    </div>
  </section>

  <!-- GALLERY -->
  <section id="gallery">
    <h2 class="section-title">Gallery 🎨 (๑˃ᴗ˂)ﻭ</h2>
    <p>SFW sample artwork shown here. Replace images once uploaded.</p>

    <div class="gallery-grid">
      <div class="art-card"><img src="images/sample1.png"></div>
      <div class="art-card"><img src="images/sample2.png"></div>
      <div class="art-card"><img src="images/sample3.png"></div>
      <div class="art-card"><img src="images/sample4.png"></div>
    </div>
  </section>

  <!-- COMMISSIONS -->
  <section id="commissions">
    <h2 class="section-title">Commission Prices 🧾 (ᵔᴥᵔ)</h2>

    <div class="commission-layout">

      <div class="commission-card">
        <h3>🖊️ Line Art</h3>
        <p><strong>Head:</strong> $5+</p>
        <p><strong>Bust:</strong> $6+</p>
        <p><strong>Waist:</strong> $10+</p>
        <p><strong>Knees:</strong> $12+</p>
        <p><strong>Full Body:</strong> $15+</p>
      </div>

      <div class="commission-card">
        <h3>🎨 Colored + Rendered</h3>
        <p><strong>Head:</strong> $10+</p>
        <p><strong>Bust:</strong> $12+</p>
        <p><strong>Waist:</strong> $15+</p>
        <p><strong>Knees:</strong> $20+</p>
        <p><strong>Full Body:</strong> $26+</p>
      </div>

    </div>
  </section>

  <!-- ABOUT -->
  <section id="about">
    <h2 class="section-title">About Rei 🍰 (˶ᵔ ᵕ ᵔ˶)</h2>
    <p>I am Rei, a soft, expressive anime-based artist who loves drawing OCs and fanart for clients worldwide.</p>
  </section>

  <!-- CONTACT -->
  <section id="contact">
    <h2 class="section-title">Contact Form 📮 (๑˃ᴗ˂)ﻭ</h2>
    <p>Choose your preferred contact method and enter your username.</p>

    <div class="contact-grid">

      <div>
        <p>Please include:</p>
        <ul>
          <li>Commission type (lineart/colored)</li>
          <li>SFW or NSFW (18+)</li>
          <li>References</li>
          <li>Your preferred contact</li>
        </ul>
      </div>

      <div class="contact-card">
        <form action="mailto:rei.tsukumo00@gmail.com" method="post" enctype="text/plain">

          <label>Preferred Contact Method:</label>
          <select name="Preferred Contact">
            <option value="Discord">Discord</option>
            <option value="Instagram">Instagram</option>
            <option value="Twitter / X">Twitter / X</option>
            <option value="TikTok">TikTok</option>
            <option value="Email">Email</option>
          </select>

          <br><br>

          <label>Their Username / ID:</label>
          <input name="User ID" placeholder="Enter your @username, Discord tag, etc." required>

          <br><br>

          <label>Commission Type:</label>
          <input name="Type" placeholder="Example: Colored waist-up SFW">

          <br><br>

          <label>Details:</label>
          <textarea name="Details" placeholder="Describe your character, pose, and references."></textarea>

          <br>
          <button class="btn btn-primary" type="submit" style="width:100%;">Send Request 💌</button>
        </form>
      </div>

    </div>
  </section>

</div>

<footer>
  © <span id="year"></span> Rei Tsukumo — All rights reserved ♡
</footer>

<script>
  document.getElementById("year").innerText = new Date().getFullYear();
</script>

</body>
</html>

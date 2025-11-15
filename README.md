<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Rei Tsukumo Art Commissions</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <!-- Cute Google Font: Quicksand -->
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

    /* Force Quicksand everywhere */
    html, body, * {
      font-family: "Quicksand", system-ui, -apple-system, BlinkMacSystemFont, sans-serif !important;
      box-sizing: border-box;
    }

    body {
      margin: 0;
      padding: 0;
      background: radial-gradient(circle at top left, #ffeaf5 0, #ffd8f2 35%, #ffc2e4 70%, #ffb0da 100%);
      color: var(--text-main);
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .page-wrapper {
      max-width: 1100px;
      margin: 0 auto;
      padding: 1.5rem 1.25rem 3rem;
      width: 100%;
    }

    /* Header / Nav */
    header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0.75rem 1.25rem;
      margin-bottom: 1.5rem;
      background: rgba(255, 255, 255, 0.75);
      backdrop-filter: blur(10px);
      border-radius: 999px;
      box-shadow: var(--shadow-soft);
      position: sticky;
      top: 0.75rem;
      z-index: 10;
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 0.5rem;
      font-weight: 600;
      font-size: 1.2rem;
    }

    .logo-badge {
      width: 32px;
      height: 32px;
      border-radius: 999px;
      background: linear-gradient(135deg, var(--pink-main), var(--pink-hot));
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--white);
      font-size: 1.2rem;
      box-shadow: 0 0 0 3px #ffe9f7;
    }

    nav {
      display: flex;
      gap: 0.5rem;
      flex-wrap: wrap;
      justify-content: flex-end;
      font-size: 0.95rem;
    }

    .nav-link {
      padding: 0.4rem 0.85rem;
      border-radius: 999px;
      background: transparent;
      cursor: pointer;
      transition: background 0.2s, transform 0.1s;
    }

    .nav-link:hover {
      background: rgba(255, 182, 217, 0.6);
      transform: translateY(-1px);
    }

    .nav-link.primary {
      background: var(--pink-hot);
      color: var(--white);
      box-shadow: var(--shadow-soft);
    }

    .nav-link.primary:hover {
      background: var(--pink-deep);
    }

    main {
      display: flex;
      flex-direction: column;
      gap: 2.5rem;
      margin-top: 1rem;
    }

    section {
      border-radius: var(--radius-big);
      background: rgba(255, 255, 255, 0.9);
      padding: 1.75rem 1.5rem;
      box-shadow: var(--shadow-soft);
      position: relative;
      overflow: hidden;
    }

    section::before {
      content: "";
      position: absolute;
      width: 220px;
      height: 220px;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(255, 182, 217, 0.55), transparent 70%);
      top: -70px;
      right: -60px;
      opacity: 0.8;
      pointer-events: none;
    }

    section::after {
      content: "";
      position: absolute;
      width: 180px;
      height: 180px;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(255, 255, 255, 0.85), transparent 70%);
      bottom: -70px;
      left: -40px;
      opacity: 0.6;
      pointer-events: none;
    }

    .section-inner {
      position: relative;
      z-index: 1;
    }

    .section-title {
      font-size: 1.7rem;
      margin-bottom: 0.5rem;
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }

    .section-subtitle {
      font-size: 0.95rem;
      opacity: 0.85;
      margin-bottom: 1rem;
    }

    /* Hero */
    .hero {
      display: grid;
      grid-template-columns: minmax(0, 1.2fr) minmax(0, 1fr);
      gap: 1.75rem;
      align-items: center;
    }

    .hero-pill {
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      padding: 0.3rem 0.9rem;
      border-radius: 999px;
      font-size: 0.85rem;
      background: rgba(255, 255, 255, 0.9);
      margin-bottom: 0.7rem;
      box-shadow: var(--shadow-soft);
    }

    .hero-title {
      font-size: 2.2rem;
      line-height: 1.15;
      margin-bottom: 0.75rem;
    }

    .hero-text {
      font-size: 0.98rem;
      margin-bottom: 1rem;
    }

    .hero-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 0.6rem;
      margin-bottom: 0.6rem;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      border-radius: 999px;
      padding: 0.6rem 1.3rem;
      font-size: 0.95rem;
      border: none;
      cursor: pointer;
      transition: transform 0.15s, box-shadow 0.15s, background 0.15s;
      white-space: nowrap;
    }

    .btn-primary {
      background: linear-gradient(135deg, var(--pink-hot), var(--pink-deep));
      color: var(--white);
      box-shadow: var(--shadow-soft);
    }

    .btn-primary:hover {
      transform: translateY(-2px);
      box-shadow: 0 10px 24px rgba(242, 90, 146, 0.6);
    }

    .btn-ghost {
      background: rgba(255, 255, 255, 0.98);
      border: 1px dashed var(--pink-hot);
    }

    .btn-ghost:hover {
      background: var(--pink-main);
    }

    .hero-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 0.4rem;
      margin-top: 0.5rem;
      font-size: 0.8rem;
    }

    .tag {
      padding: 0.2rem 0.7rem;
      border-radius: 999px;
      background: rgba(255, 255, 255, 0.9);
      border: 1px solid rgba(255, 111, 169, 0.25);
    }

    .hero-art-preview {
      position: relative;
      width: 100%;
      min-height: 230px;
    }

    .hero-card {
      position: absolute;
      inset: 0;
      border-radius: var(--radius-big);
      background: linear-gradient(145deg, #ffe6f2, #ffbfdc);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 0.75rem;
      text-align: center;
      padding: 1.5rem;
      box-shadow: var(--shadow-soft);
    }

    .hero-pfp {
      width: 120px;
      height: 120px;
      border-radius: 999px;
      background: radial-gradient(circle at 30% 20%, #fff, #ffc1dd 60%, #ff9bc8);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 2.6rem;
      box-shadow: 0 0 0 5px #ffe9f7;
    }

    .hero-username {
      font-weight: 600;
    }

    .hero-status {
      font-size: 0.8rem;
      padding: 0.15rem 0.75rem;
      border-radius: 999px;
      background: rgba(255, 255, 255, 0.9);
      border: 1px solid rgba(255, 111, 169, 0.35);
      display: inline-flex;
      align-items: center;
      gap: 0.3rem;
    }

    .floating-chip {
      position: absolute;
      padding: 0.35rem 0.7rem;
      border-radius: 999px;
      font-size: 0.75rem;
      background: var(--white);
      box-shadow: var(--shadow-soft);
    }

    .chip-1 {
      top: 10px;
      left: -3px;
    }

    .chip-2 {
      bottom: 18px;
      right: -5px;
    }

    /* Social strip */
    .social-strip {
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem;
      align-items: center;
      justify-content: center;
      padding: 0.7rem 1rem;
      background: rgba(255, 255, 255, 0.9);
      border-radius: 999px;
      box-shadow: var(--shadow-soft);
      margin: -0.75rem auto 0;
      max-width: 720px;
      position: relative;
      z-index: 2;
    }

    .social-label {
      font-size: 0.9rem;
      opacity: 0.8;
    }

    .social-links {
      display: flex;
      flex-wrap: wrap;
      gap: 0.4rem;
    }

    .social-pill {
      display: inline-flex;
      align-items: center;
      gap: 0.35rem;
      font-size: 0.9rem;
      padding: 0.3rem 0.7rem;
      border-radius: 999px;
      background: var(--pink-main);
      cursor: pointer;
      transition: transform 0.1s, box-shadow 0.1s;
    }

    .social-pill:hover {
      transform: translateY(-1px);
      box-shadow: var(--shadow-soft);
    }

    /* Gallery */
    .gallery-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
      gap: 1rem;
      margin-top: 1rem;
    }

    .art-card {
      position: relative;
      overflow: hidden;
      border-radius: var(--radius-small);
      background: var(--pink-light);
      box-shadow: 0 6px 16px rgba(255, 167, 211, 0.6);
    }

    .art-card img {
      display: block;
      width: 100%;
      height: 180px;
      object-fit: cover;
      transition: transform 0.25s;
    }

    .art-card:hover img {
      transform: scale(1.05);
    }

    .art-label {
      position: absolute;
      left: 0.5rem;
      bottom: 0.5rem;
      padding: 0.25rem 0.55rem;
      border-radius: 999px;
      font-size: 0.75rem;
      background: rgba(255, 255, 255, 0.9);
      border: 1px solid rgba(255, 111, 169, 0.35);
    }

    .gallery-note {
      font-size: 0.85rem;
      margin-top: 0.75rem;
      opacity: 0.85;
    }

    /* Commissions */
    .commission-layout {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 1.25rem;
      margin-top: 1rem;
    }

    .commission-card {
      background: rgba(255, 255, 255, 0.96);
      border-radius: var(--radius-small);
      padding: 1rem;
      box-shadow: 0 6px 16px rgba(255, 167, 211, 0.5);
      border: 1px solid rgba(255, 111, 169, 0.25);
      font-size: 0.9rem;
    }

    .commission-name {
      font-weight: 600;
      margin-bottom: 0.35rem;
      display: flex;
      align-items: center;
      gap: 0.3rem;
    }

    .commission-list {
      list-style: none;
      padding: 0;
      margin: 0.4rem 0 0;
    }

    .commission-list li {
      margin-bottom: 0.25rem;
    }

    .commission-list strong {
      display: inline-block;
      min-width: 90px;
    }

    .tos-list {
      margin-top: 1.1rem;
      font-size: 0.88rem;
      padding-left: 1.1rem;
    }

    .tos-list li {
      margin-bottom: 0.35rem;
    }

    /* About */
    .about-text {
      font-size: 0.95rem;
      line-height: 1.6;
    }

    .about-highlight {
      display: inline-block;
      padding: 0.15rem 0.5rem;
      border-radius: 999px;
      background: var(--pink-main);
      margin: 0 0.15rem;
      font-size: 0.85rem;
    }

    /* Contact */
    .contact-grid {
      display: grid;
      grid-template-columns: minmax(0, 1.1fr) minmax(0, 1fr);
      gap: 1.25rem;
      margin-top: 1rem;
    }

    .contact-info {
      font-size: 0.9rem;
      line-height: 1.5;
    }

    .contact-info ul {
      margin-top: 0.4rem;
      padding-left: 1.1rem;
      font-size: 0.88rem;
    }

    .contact-card {
      background: rgba(255, 255, 255, 0.96);
      border-radius: var(--radius-small);
      padding: 1rem;
      box-shadow: 0 6px 16px rgba(255, 167, 211, 0.5);
      border: 1px solid rgba(255, 111, 169, 0.25);
      font-size: 0.9rem;
    }

    .contact-row {
      display: flex;
      flex-direction: column;
      gap: 0.35rem;
      margin-bottom: 0.8rem;
    }

    label {
      font-size: 0.8rem;
      opacity: 0.9;
    }

    input,
    select,
    textarea {
      border-radius: 0.9rem;
      border: 1px solid rgba(255, 111, 169, 0.4);
      padding: 0.45rem 0.75rem;
      font-size: 0.88rem;
      outline: none;
      background: #fff;
    }

    input:focus,
    select:focus,
    textarea:focus {
      border-color: var(--pink-deep);
      box-shadow: 0 0 0 3px rgba(255, 147, 196, 0.35);
    }

    textarea {
      resize: vertical;
      min-height: 90px;
    }

    .contact-hint {
      font-size: 0.75rem;
      opacity: 0.8;
    }

    footer {
      margin-top: auto;
      text-align: center;
      padding: 1.5rem 0.5rem 2rem;
      font-size: 0.75rem;
      opacity: 0.8;
    }

    /* Back to top button */
    #topBtn {
      position: fixed;
      bottom: 30px;
      right: 30px;
      background: var(--pink-hot);
      color: var(--white);
      border: none;
      padding: 12px 15px;
      border-radius: 50%;
      font-size: 18px;
      cursor: pointer;
      box-shadow: var(--shadow-soft);
      z-index: 999;
      display: none;
      transition: transform 0.2s, background 0.2s;
    }

    #topBtn:hover {
      transform: translateY(-4px) scale(1.05);
      background: var(--pink-deep);
    }

    /* Responsive */
    @media (max-width: 800px) {
      header {
        flex-direction: column;
        align-items: flex-start;
        gap: 0.5rem;
      }

      .hero {
        grid-template-columns: 1fr;
      }

      .contact-grid {
        grid-template-columns: 1fr;
      }
    }

    @media (max-width: 480px) {
      .hero-title {
        font-size: 1.8rem;
      }

      section {
        padding: 1.4rem 1.1rem;
      }

      .page-wrapper {
        padding-inline: 0.75rem;
      }
    }
  </style>
</head>
<body>
  <!-- Back to top button -->
  <button id="topBtn" aria-label="Back to top">↑</button>

  <div class="page-wrapper">
    <!-- Header -->
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

    <main>
      <!-- Hero -->
      <section id="home">
        <div class="section-inner hero">
          <div>
            <div class="hero-pill">
              <span>💕</span>
              <span>Commissions currently <strong>OPEN</strong> (˶˃ ᵕ ˂˶)♡</span>
            </div>
            <h1 class="hero-title">Anime &amp; NSFW (18+) Art Commissions</h1>
            <p class="hero-text">
              Hi, I’m <strong>Rei Tsukumo (津雲 玲)</strong> — an anime-based digital artist
              drawing characters of all genders and ages (for SFW pieces), and offering NSFW
              artwork for adults (18+ only). Icons, illustrations, and more, with expressive,
              detailed anime vibes.
            </p>
            <div class="hero-buttons">
              <a href="#commissions" class="btn btn-primary">View Prices</a>
              <a href="#gallery" class="btn btn-ghost">See My Art</a>
            </div>
            <div class="hero-tags">
              <span class="tag">Anime Style</span>
              <span class="tag">SFW &amp; NSFW (18+)</span>
              <span class="tag">OCs &amp; Fanart</span>
              <span class="tag">Any Gender</span>
            </div>
          </div>

          <div class="hero-art-preview">
            <div class="hero-card">
              <div class="hero-pfp">玲</div>
              <div class="hero-username">@rei_tsukumo00</div>
              <div class="hero-status">
              </div>
              <div class="floating-chip chip-1">✨ SFW &amp; NSFW (18+)</div>
            </div>
          </div>
        </div>
      </section>

      <!-- Social strip -->
      <div class="social-strip">
        <span class="social-label">Find me here:</span>
        <div class="social-links">
          <a href="https://www.instagram.com/rei_tsukumo00/" target="_blank" class="social-pill">
            <span>📸</span><span>Instagram</span>
          </a>
          <a href="https://x.com/rei_tsukumo00" target="_blank" class="social-pill">
            <span>🐦</span><span>X (Twitter)</span>
          </a>
          <a href="https://www.tiktok.com/@rei_tsukumo00" target="_blank" class="social-pill">
            <span>🎵</span><span>TikTok</span>
          </a>
          <a href="https://www.patreon.com/c/rei_tsukumo00?fromConcierge=true&redirect=true" target="_blank" class="social-pill">
            <span>🩷</span><span>Patreon</span>
          </a>
        </div>
      </div>

      <!-- Gallery -->
      <section id="gallery">
        <div class="section-inner">
          <h2 class="section-title">Gallery 🎨 (๑˃ᴗ˂)ﻭ</h2>
          <p class="section-subtitle">
            SFW preview of my work. Replace these placeholders with your actual art files once you upload them.
          </p>
          <div class="gallery-grid">
            <div class="art-card">
              <img src="images/sample1.png" alt="Sample artwork 1" />
              <div class="art-label">Anime Portrait</div>
            </div>
            <div class="art-card">
              <img src="images/sample2.png" alt="Sample artwork 2" />
              <div class="art-label">Full-Body Character</div>
            </div>
            <div class="art-card">
              <img src="images/sample3.png" alt="Sample artwork 3" />
              <div class="art-label">Dynamic Pose</div>
            </div>
            <div class="art-card">
              <img src="images/sample4.png" alt="Sample artwork 4" />
              <div class="art-label">Detailed Outfit</div>
            </div>
          </div>
          <p class="gallery-note">
            ✧ Create an <code>images</code> folder in your repo, upload your art
            (e.g. <code>icon1.png</code>, <code>fullbody1.png</code>), and update the
            <code>src=""</code> paths above to match your filenames.
          </p>
        </div>
      </section>

      <!-- Commissions -->
      <section id="commissions">
        <div class="section-inner">
          <h2 class="section-title">Commissions &amp; Pricing 🧾 (ᵔᴥᵔ)</h2>
          <p class="section-subtitle">
            Base prices in <strong>USD</strong>. Final quotes may change for complexity, backgrounds,
            multiple characters, or specific NSFW content (18+ only). Furry drawings and/or drawings with 
            another person(s) will be charged more than, if not double, the og price.
          </p>

          <div class="commission-layout">
            <!-- Line Art -->
            <div class="commission-card">
              <div class="commission-name">Line Art <span>🖊️</span></div>
              <p>Clean linework only, no color.</p>
              <ul class="commission-list">
                <li><strong>Head:</strong> $5+</li>
                <li><strong>Bust:</strong> $6+</li>
                <li><strong>Waist:</strong> $10+</li>
                <li><strong>Knees:</strong> $12+</li>
                <li><strong>Full Body:</strong> $15+</li>
              </ul>
            </div>

            <!-- Colored + Rendered -->
            <div class="commission-card">
              <div class="commission-name">Colored + Rendered <span>🎨</span></div>
              <p>Flat color plus rendering, shading, and details.</p>
              <ul class="commission-list">
                <li><strong>Head:</strong> $10+</li>
                <li><strong>Bust:</strong> $12+</li>
                <li><strong>Waist:</strong> $15+</li>
                <li><strong>Knees:</strong> $20+</li>
                <li><strong>Full Body:</strong> $26+</li>
              </ul>
            </div>
          </div>

          <ul class="tos-list">
            <li>I draw anime-style characters of any gender. SFW art can feature characters of any age; NSFW pieces are strictly for adults (18+) and adult characters only.</li>
            <li>NSFW, suggestive, and mature themes are available for 18+ clients. Please describe your idea clearly so I can confirm if it’s acceptable.</li>
            <li>Complex designs, detailed outfits, armor, or elaborate backgrounds may increase the price.</li>
            <li>Commissions are for personal use (icons, headers, prints) by default. For commercial use, a separate quote is required.</li>
            <li>Payment details and final confirmation will be handled after we discuss your request.</li>
          </ul>
        </div>
      </section>

      <!-- About -->
      <section id="about">
        <div class="section-inner">
          <h2 class="section-title">About Rei 🍰 (˶ᵔ ᵕ ᵔ˶)</h2>
          <p class="about-text">
            I’m <span class="about-highlight">Rei Tsukumo (津雲 玲)</span>, an anime-based digital artist
            who loves drawing expressive characters, OCs, and fanart. From soft and cute vibes to darker
            or more mature atmospheres, I focus on mood, pose, and expression.
          </p>
          <br />
          <p class="about-text">
            I accept both SFW and NSFW (18+) commissions, and I enjoy bringing people’s ideas to life in a
            way that feels personal and emotionally rich. Thank you for supporting my work — it means a lot
            (˶˃ ᵕ ˂˶)♡
          </p>
        </div>
      </section>

      <!-- Contact -->
      <section id="contact">
        <div class="section-inner">
          <h2 class="section-title">Contact &amp; Order Form 📮 (๑˃ᴗ˂)ﻭ</h2>
          <p class="section-subtitle">
            Please fill out the form with your idea and preferred contact method. I’ll reach out to you
            on the platform you choose once I review your request.
          </p>

          <div class="contact-grid">
            <div class="contact-info">
              <p>When you request a commission, it helps if you include:</p>
              <ul>
                <li>Type of commission (line art / colored, head / bust / waist / knees / full body)</li>
                <li>SFW or NSFW (18+ only) and the general idea</li>
                <li>Character references (links, images, or descriptions)</li>
                <li>Preferred mood (cute, dark, elegant, etc.)</li>
                <li>Rough deadline (if any) and your budget</li>
              </ul>
              <br />
              <p class="contact-hint">
                I’ll respond using the contact method you choose below, not by email directly.
              </p>
            </div>

            <div class="contact-card">
              <!-- This sends the form data through the user's mail client to Rei's email -->
              <form action="mailto:rei.tsukumo00@gmail.com" method="post" enctype="text/plain">
                <div class="contact-row">
                  <label for="name">Name / Username</label>
                  <input id="name" name="Name" type="text" placeholder="Your name or main handle" required />
                </div>

                <div class="contact-row">
                  <label for="contact-method">Preferred Contact Method</label>
                  <select id="contact-method" name="Preferred Contact Method" required>
                    <option value="Discord">Discord</option>
                    <option value="Instagram">Instagram</option>
                    <option value="Twitter / X">Twitter / X</option>
                    <option value="TikTok">TikTok</option>
                    <option value="Email">Email</option>
                  </select>
                  <p class="contact-hint">
                    I will contact you using this platform, so please make sure your username/ID is correct.
                  </p>
                </div>

                <div class="contact-row">
                  <label for="contact-id">Your Username / ID</label>
                  <input id="contact-id" name="Contact Username / ID" type="text" placeholder="@example / user#0000" required />
                </div>

                <div class="contact-row">
                  <label for="type">Commission Type</label>
                  <input id="type" name="Commission Type" type="text" placeholder="Example: Colored bust, SFW / NSFW (18+)" />
                </div>

                <div class="contact-row">
                  <label for="details">Details &amp; References</label>
                  <textarea id="details" name="Details" placeholder="Tell me about your character, pose, mood, and add links to references."></textarea>
                  <p class="contact-hint">
                    You can paste links to reference images (Drive, Instagram, etc.) here.
                  </p>
                </div>

                <button type="submit" class="btn btn-primary" style="width: 100%;">
                  Send Commission Request 💌
                </button>
              </form>
            </div>
          </div>
        </div>
      </section>
    </main>

    <footer>
      © <span id="year"></span> Rei Tsukumo · All rights reserved ♡
    </footer>
  </div>

  <script>
    // Auto-update year
    document.getElementById("year").textContent = new Date().getFullYear();

    // Back to top button behavior
    const topBtn = document.getElementById("topBtn");
    window.addEventListener("scroll", () => {
      if (document.documentElement.scrollTop > 200 || document.body.scrollTop > 200) {
        topBtn.style.display = "block";
      } else {
        topBtn.style.display = "none";
      }
    });

    topBtn.addEventListener("click", () => {
      window.scrollTo({ top: 0, behavior: "smooth" });
    });
  </script>
</body>
</html>

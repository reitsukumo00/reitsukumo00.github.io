<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Art Commissions | Your Name</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <!-- Cute Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Fredoka:wght@300;400;500;600&display=swap" rel="stylesheet" />

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

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: "Fredoka", system-ui, -apple-system, BlinkMacSystemFont, sans-serif;
      background: radial-gradient(circle at top left, #ffeaf5 0, #ffd8f2 35%, #ffc2e4 70%, #ffb0da 100%);
      color: var(--text-main);
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    /* ---------- Layout ---------- */

    .page-wrapper {
      max-width: 1100px;
      margin: 0 auto;
      padding: 1.5rem 1.25rem 3rem;
    }

    header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0.75rem 1.25rem;
      margin-bottom: 1.5rem;
      background: rgba(255, 255, 255, 0.7);
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
      font-size: 0.95rem;
      flex-wrap: wrap;
      justify-content: flex-end;
    }

    .nav-link {
      padding: 0.4rem 0.85rem;
      border-radius: 999px;
      background: transparent;
      transition: background 0.2s, transform 0.1s;
      cursor: pointer;
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
      background: rgba(255, 255, 255, 0.85);
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
      font-size: 1.6rem;
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

    /* ---------- Hero ---------- */

    .hero {
      display: grid;
      grid-template-columns: minmax(0, 1.2fr) minmax(0, 1fr);
      gap: 1.75rem;
      align-items: center;
    }

    .hero-title {
      font-size: 2.1rem;
      line-height: 1.15;
      margin-bottom: 0.75rem;
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
      box-shadow: 0 6px 14px rgba(255, 182, 217, 0.8);
    }

    .hero-text {
      font-size: 0.98rem;
      margin-bottom: 1rem;
    }

    .hero-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 0.6rem;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      border-radius: 999px;
      padding: 0.55rem 1.25rem;
      font-size: 0.95rem;
      border: none;
      cursor: pointer;
      transition: transform 0.1s, box-shadow 0.1s, background 0.2s;
      white-space: nowrap;
    }

    .btn-primary {
      background: linear-gradient(135deg, var(--pink-hot), var(--pink-deep));
      color: var(--white);
      box-shadow: var(--shadow-soft);
    }

    .btn-primary:hover {
      transform: translateY(-1px);
      box-shadow: 0 10px 24px rgba(242, 90, 146, 0.6);
    }

    .btn-ghost {
      background: rgba(255, 255, 255, 0.9);
      border: 1px dashed var(--pink-hot);
    }

    .btn-ghost:hover {
      background: var(--pink-main);
    }

    .hero-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 0.4rem;
      margin-top: 0.7rem;
      font-size: 0.8rem;
    }

    .tag {
      padding: 0.2rem 0.7rem;
      border-radius: 999px;
      background: rgba(255, 255, 255, 0.9);
      border: 1px solid rgba(255, 111, 169, 0.2);
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
      font-size: 3rem;
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
      top: 12px;
      left: -5px;
    }

    .chip-2 {
      bottom: 18px;
      right: -2px;
    }

    /* ---------- Socials strip ---------- */

    .social-strip {
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem;
      align-items: center;
      justify-content: center;
      padding: 0.7rem 1rem;
      background: rgba(255, 255, 255, 0.8);
      border-radius: 999px;
      box-shadow: var(--shadow-soft);
      margin: -0.75rem auto 0;
      max-width: 640px;
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
      color: var(--text-main);
      cursor: pointer;
      transition: transform 0.1s, box-shadow 0.1s;
    }

    .social-pill:hover {
      transform: translateY(-1px);
      box-shadow: var(--shadow-soft);
    }

    /* ---------- Gallery ---------- */

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
      cursor: pointer;
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

    /* ---------- Commissions ---------- */

    .commission-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(210px, 1fr));
      gap: 1rem;
      margin-top: 1rem;
    }

    .commission-card {
      background: rgba(255, 255, 255, 0.95);
      border-radius: var(--radius-small);
      padding: 1rem;
      box-shadow: 0 6px 16px rgba(255, 167, 211, 0.5);
      border: 1px solid rgba(255, 111, 169, 0.25);
    }

    .commission-name {
      font-weight: 600;
      margin-bottom: 0.25rem;
      display: flex;
      align-items: center;
      gap: 0.3rem;
    }

    .commission-price {
      font-size: 0.95rem;
      color: var(--pink-deep);
      margin-bottom: 0.4rem;
    }

    .commission-detail {
      font-size: 0.82rem;
      opacity: 0.9;
      margin-bottom: 0.4rem;
    }

    .commission-extra {
      font-size: 0.78rem;
      opacity: 0.8;
    }

    .tos-list {
      margin-top: 1rem;
      font-size: 0.88rem;
      padding-left: 1.1rem;
    }

    .tos-list li {
      margin-bottom: 0.35rem;
    }

    /* ---------- About / Contact ---------- */

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
      gap: 0.4rem;
      margin-bottom: 0.8rem;
    }

    label {
      font-size: 0.8rem;
      opacity: 0.9;
    }

    input,
    textarea {
      border-radius: 0.9rem;
      border: 1px solid rgba(255, 111, 169, 0.4);
      padding: 0.45rem 0.75rem;
      font-family: inherit;
      font-size: 0.88rem;
      outline: none;
      background: #fff;
    }

    input:focus,
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

    /* ---------- Responsive ---------- */

    @media (max-width: 800px) {
      .hero {
        grid-template-columns: 1fr;
      }

      header {
        flex-direction: column;
        align-items: flex-start;
        gap: 0.5rem;
      }

      .contact-grid {
        grid-template-columns: 1fr;
      }
    }

    @media (max-width: 480px) {
      .hero-title {
        font-size: 1.7rem;
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
  <div class="page-wrapper">
    <!-- Header / Nav -->
    <header>
      <div class="logo">
        <div class="logo-badge">✿</div>
        <span>YourName Art</span>
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
      <!-- HERO / HOME -->
      <section id="home">
        <div class="section-inner hero">
          <div>
            <div class="hero-pill">
              <span>💕</span>
              <span>Commissions currently <strong>OPEN</strong></span>
            </div>
            <h1 class="hero-title">Cute &amp; Kawaii Art Commissions</h1>
            <p class="hero-text">
              Hi, I’m <strong>Your Name</strong> — I draw soft pastel, anime-inspired art,
              perfect for icons, banners, and VTuber / OC illustrations. Check out my
              portfolio and commission info below! ₊˚ʚ ♡ɞ˚₊
            </p>
            <div class="hero-buttons">
              <a href="#commissions" class="btn btn-primary">View Prices</a>
              <a href="#gallery" class="btn btn-ghost">See My Art</a>
            </div>
            <div class="hero-tags">
              <span class="tag">Chibi</span>
              <span class="tag">Icons</span>
              <span class="tag">Anime Style</span>
              <span class="tag">Pastel / Kawaii</span>
            </div>
          </div>

          <div class="hero-art-preview">
            <div class="hero-card">
              <div class="hero-pfp">☆</div>
              <div class="hero-username">@your_handle</div>
              <div class="hero-status">
                <span>🧁</span>
                <span>Soft pastel artist</span>
              </div>
              <div class="floating-chip chip-1">✨ OC portraits</div>
              <div class="floating-chip chip-2">🎀 Matching icons</div>
            </div>
          </div>
        </div>
      </section>

      <!-- SOCIAL STRIP -->
      <div class="social-strip">
        <span class="social-label">Find me here:</span>
        <div class="social-links">
          <!-- Replace # with your actual links -->
          <a href="https://instagram.com/yourhandle" target="_blank" class="social-pill">
            <span>📸</span><span>Instagram</span>
          </a>
          <a href="https://twitter.com/yourhandle" target="_blank" class="social-pill">
            <span>🐦</span><span>Twitter / X</span>
          </a>
          <a href="https://www.tiktok.com/@yourhandle" target="_blank" class="social-pill">
            <span>🎵</span><span>TikTok</span>
          </a>
          <a href="https://github.com/yourusername" target="_blank" class="social-pill">
            <span>💾</span><span>GitHub</span>
          </a>
        </div>
      </div>

      <!-- GALLERY -->
      <section id="gallery">
        <div class="section-inner">
          <h2 class="section-title">Gallery <span>🎨</span></h2>
          <p class="section-subtitle">
            A small preview of my work. Replace these images with your actual art pieces.
          </p>
          <div class="gallery-grid">
            <!-- Replace src with your own image paths -->
            <div class="art-card">
              <img src="images/sample1.png" alt="Sample artwork 1" />
              <div class="art-label">OC Portrait</div>
            </div>
            <div class="art-card">
              <img src="images/sample2.png" alt="Sample artwork 2" />
              <div class="art-label">Chibi Fullbody</div>
            </div>
            <div class="art-card">
              <img src="images/sample3.png" alt="Sample artwork 3" />
              <div class="art-label">Icon Set</div>
            </div>
            <div class="art-card">
              <img src="images/sample4.png" alt="Sample artwork 4" />
              <div class="art-label">Couple Illustration</div>
            </div>
          </div>
          <p class="gallery-note">
            ✧ Tip: create an <code>images</code> folder in your repo, upload your art,
            and update the <code>src=""</code> paths above to match your file names.
          </p>
        </div>
      </section>

      <!-- COMMISSIONS -->
      <section id="commissions">
        <div class="section-inner">
          <h2 class="section-title">Commissions &amp; Pricing <span>🧾</span></h2>
          <p class="section-subtitle">
            Prices are base estimates and may change depending on complexity. All prices
            listed in <strong>USD</strong>. Please read the Terms of Service before ordering.
          </p>

          <div class="commission-grid">
            <div class="commission-card">
              <div class="commission-name">Chibi <span>🍓</span></div>
              <div class="commission-price">From $20</div>
              <div class="commission-detail">
                Cute, simplified full-body chibi. Perfect for profile pics or stickers.
              </div>
              <div class="commission-extra">
                Includes: simple pastel background + soft shading.
              </div>
            </div>

            <div class="commission-card">
              <div class="commission-name">Bust / Icon <span>🌸</span></div>
              <div class="commission-price">From $25</div>
              <div class="commission-detail">
                Head &amp; shoulders illustration with your choice of expression.
              </div>
              <div class="commission-extra">
                Includes: detailed eyes, simple props (stars, hearts, etc.).
              </div>
            </div>

            <div class="commission-card">
              <div class="commission-name">Half-Body <span>🩰</span></div>
              <div class="commission-price">From $35</div>
              <div class="commission-detail">
                Half-body anime style. Great for banners and character sheets.
              </div>
              <div class="commission-extra">
                Complex outfits may add an extra fee.
              </div>
            </div>

            <div class="commission-card">
              <div class="commission-name">Full-Body <span>💖</span></div>
              <div class="commission-price">From $50</div>
              <div class="commission-detail">
                Full-body illustration with dynamic posing and pastel background.
              </div>
              <div class="commission-extra">
                Extra characters: +50% base price each.
              </div>
            </div>
          </div>

          <ul class="tos-list">
            <li>Personal use only (icons, headers, prints). Commercial use = please ask.</li>
            <li>Payment via PayPal / [your method] after sketch approval.</li>
            <li>No NFTs, AI training, hate content, or extremely NSFW work.</li>
            <li>I keep the right to post finished artwork in my portfolio and socials.</li>
            <li>Turnaround time: ~1–4 weeks depending on queue and complexity.</li>
          </ul>
        </div>
      </section>

      <!-- ABOUT -->
      <section id="about">
        <div class="section-inner">
          <h2 class="section-title">About Me <span>🍰</span></h2>
          <p class="about-text">
            Hello! I’m <span class="about-highlight">Your Name</span>, a self-taught
            digital artist who loves drawing pastel, anime-inspired characters. I’m
            especially obsessed with <span class="about-highlight">soft pinks</span>,
            sparkles, cozy vibes, and expressive faces. ♡
          </p>
          <br />
          <p class="about-text">
            When I’m not drawing, I’m probably scrolling through cute character designs,
            studying, or working on original stories. My goal is to bring your OC,
            persona, or favorite character to life in a way that feels warm, gentle, and
            very, very <span class="about-highlight">kawaii</span>. ✧
          </p>
        </div>
      </section>

      <!-- CONTACT -->
      <section id="contact">
        <div class="section-inner">
          <h2 class="section-title">Contact &amp; Order Form <span>📮</span></h2>
          <p class="section-subtitle">
            Ready to commission me? Please send a message using the form below or DM me
            on any of my socials with your idea and references.
          </p>

          <div class="contact-grid">
            <div class="contact-info">
              <p>
                To request a commission, please include:
              </p>
              <ul>
                <li>Type of commission (chibi / bust / half-body / full-body)</li>
                <li>Character references (images, moodboards, or detailed description)</li>
                <li>Preferred vibe (soft, sparkly, dark, etc.)</li>
                <li>Deadline (if any) and budget</li>
              </ul>
              <br />
              <p>
                You can also email me directly at:
                <strong>youremail@example.com</strong> ✧
              </p>
            </div>

            <div class="contact-card">
              <!-- Basic mailto form (opens email client, not a backend) -->
              <form action="mailto:youremail@example.com" method="post" enctype="text/plain">
                <div class="contact-row">
                  <label for="name">Name / Username</label>
                  <input id="name" name="Name" type="text" placeholder="Your name or @handle" required />
                </div>

                <div class="contact-row">
                  <label for="email">Email</label>
                  <input id="email" name="Email" type="email" placeholder="you@example.com" required />
                </div>

                <div class="contact-row">
                  <label for="type">Commission Type</label>
                  <input id="type" name="Type" type="text" placeholder="Chibi, bust, half-body, etc." />
                </div>

                <div class="contact-row">
                  <label for="details">Details &amp; References</label>
                  <textarea id="details" name="Details" placeholder="Tell me about your character, pose, vibe, etc."></textarea>
                  <p class="contact-hint">
                    You can paste links to reference images here (Instagram, Google Drive, etc.).
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
      © <span id="year"></span> Your Name · Made with lots of ♡ and pink.
    </footer>
  </div>

  <script>
    // Auto-update year
    document.getElementById("year").textContent = new Date().getFullYear();
  </script>
</body>
</html>


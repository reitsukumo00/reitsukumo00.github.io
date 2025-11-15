<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Rei Tsukumo Art Commissions</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <!-- Cute Google Font: Quicksand -->
  <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@300;400;500;600&display=swap" rel="stylesheet" />

  <style>
    :root {
      --pink-very-light: #fff1f9;
      --pink-light: #ffe0f3;
      --pink: #ffb7de;
      --pink-bright: #ff75bc;
      --pink-deep: #f4519b;
      --text: #4c2442;
      --white: #ffffff;
      --shadow-soft: 0 10px 25px rgba(255, 143, 203, 0.4);
      --radius-big: 1.6rem;
      --radius-med: 1.1rem;
      --radius-pill: 999px;
    }

    * ,
    *::before,
    *::after {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: "Quicksand", system-ui, -apple-system, BlinkMacSystemFont, sans-serif;
    }

    body {
      min-height: 100vh;
      background: radial-gradient(circle at top left, #ffeaf6 0%, #ffd5f0 40%, #ffc1e8 70%, #ffb0df 100%);
      color: var(--text);
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .page-wrapper {
      max-width: 1100px;
      margin: 0 auto;
      padding: 1.5rem 1.25rem 3rem;
    }

    /* ---------------- Header ---------------- */

    header {
      position: sticky;
      top: 0.75rem;
      z-index: 20;
      background: rgba(255, 255, 255, 0.85);
      backdrop-filter: blur(10px);
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0.7rem 1.25rem;
      border-radius: var(--radius-pill);
      box-shadow: var(--shadow-soft);
      margin-bottom: 1.5rem;
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 0.55rem;
      font-weight: 600;
      font-size: 1.1rem;
    }

    .logo-badge {
      width: 32px;
      height: 32px;
      border-radius: var(--radius-pill);
      background: linear-gradient(135deg, var(--pink), var(--pink-bright));
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--white);
      font-size: 1.1rem;
      box-shadow: 0 0 0 4px #ffe6f8;
    }

    nav {
      display: flex;
      align-items: center;
      flex-wrap: wrap;
      gap: 0.45rem;
      font-size: 0.95rem;
    }

    .nav-link {
      padding: 0.38rem 0.85rem;
      border-radius: var(--radius-pill);
      cursor: pointer;
      transition: background 0.15s ease, transform 0.1s ease;
    }

    .nav-link:hover {
      background: rgba(255, 183, 223, 0.7);
      transform: translateY(-1px);
    }

    .nav-link.primary {
      background: var(--pink-bright);
      color: var(--white);
      box-shadow: var(--shadow-soft);
    }

    .nav-link.primary:hover {
      background: var(--pink-deep);
    }

    /* ---------------- Sections ---------------- */

    main {
      display: flex;
      flex-direction: column;
      gap: 2.4rem;
    }

    section {
      position: relative;
      overflow: hidden;
      background: rgba(255, 255, 255, 0.92);
      border-radius: var(--radius-big);
      padding: 1.75rem 1.6rem;
      box-shadow: var(--shadow-soft);
    }

    section::before {
      content: "";
      position: absolute;
      width: 220px;
      height: 220px;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(255, 183, 223, 0.7), transparent 70%);
      top: -70px;
      right: -60px;
      opacity: 0.7;
      pointer-events: none;
    }

    section::after {
      content: "";
      position: absolute;
      width: 170px;
      height: 170px;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(255, 255, 255, 0.9), transparent 70%);
      bottom: -60px;
      left: -40px;
      opacity: 0.7;
      pointer-events: none;
    }

    .section-inner {
      position: relative;
      z-index: 1;
    }

    .section-title {
      font-size: 1.65rem;
      margin-bottom: 0.4rem;
      display: flex;
      align-items: center;
      gap: 0.45rem;
    }

    .section-subtitle {
      font-size: 0.95rem;
      opacity: 0.85;
      margin-bottom: 0.8rem;
    }

    /* ---------------- Hero ---------------- */

    .hero-grid {
      display: grid;
      grid-template-columns: minmax(0, 1.3fr) minmax(0, 1fr);
      gap: 1.8rem;
      align-items: center;
    }

    .hero-pill {
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      padding: 0.35rem 0.9rem;
      border-radius: var(--radius-pill);
      background: var(--pink-very-light);
      font-size: 0.85rem;
      margin-bottom: 0.7rem;
      box-shadow: var(--shadow-soft);
    }

    .hero-title {
      font-size: 2.1rem;
      line-height: 1.15;
      margin-bottom: 0.6rem;
    }

    .hero-text {
      font-size: 0.98rem;
      margin-bottom: 1rem;
    }

    .hero-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 0.6rem;
      margin-bottom: 0.7rem;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      padding: 0.55rem 1.25rem;
      border-radius: var(--radius-pill);
      border: none;
      font-size: 0.95rem;
      cursor: pointer;
      transition: transform 0.1s ease, box-shadow 0.1s ease, background 0.2s ease;
      white-space: nowrap;
    }

    .btn-primary {
      background: linear-gradient(135deg, var(--pink-bright), var(--pink-deep));
      color: var(--white);
      box-shadow: var(--shadow-soft);
    }

    .btn-primary:hover {
      transform: translateY(-1px);
      box-shadow: 0 12px 28px rgba(244, 81, 155, 0.55);
    }

    .btn-ghost {
      background: var(--white);
      border: 1px dashed var(--pink-bright);
      color: var(--text);
    }

    .btn-ghost:hover {
      background: var(--pink-light);
    }

    .hero-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 0.4rem;
      font-size: 0.8rem;
      margin-top: 0.2rem;
    }

    .tag {
      padding: 0.2rem 0.7rem;
      border-radius: var(--radius-pill);
      border: 1px solid rgba(255, 117, 188, 0.35);
      background: rgba(255, 255, 255, 0.95);
    }

    .hero-card-wrap {
      position: relative;
      min-height: 230px;
    }

    .hero-card {
      position: absolute;
      inset: 0;
      border-radius: var(--radius-big);
      background: linear-gradient(145deg, #ffeaf7, #ffc4e6);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 0.7rem;
      text-align: center;
      padding: 1.4rem;
      box-shadow: var(--shadow-soft);
    }

    .hero-avatar {
      width: 115px;
      height: 115px;
      border-radius: 50%;
      background: radial-gradient(circle at 30% 20%, #fff, #ffc0e4 60%, #ff95cf);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 2.3rem;
      box-shadow: 0 0 0 5px #ffe6f8;
    }

    .hero-username {
      font-weight: 600;
      font-size: 1rem;
    }

    .hero-status {
      font-size: 0.8rem;
      padding: 0.15rem 0.75rem;
      border-radius: var(--radius-pill);
      background: rgba(255, 255, 255, 0.95);
      border: 1px solid rgba(255, 117, 188, 0.4);
      display: inline-flex;
      align-items: center;
      gap: 0.3rem;
    }

    .floating-chip {
      position: absolute;
      padding: 0.35rem 0.7rem;
      border-radius: var(--radius-pill);
      font-size: 0.75rem;
      background: var(--white);
      box-shadow: var(--shadow-soft);
    }

    .chip-1 {
      top: 12px;
      left: -4px;
    }

    .chip-2 {
      bottom: 16px;
      right: -4px;
    }

    /* ---------------- Social strip ---------------- */

    .social-strip {
      margin: -0.8rem auto 0;
      max-width: 700px;
      background: rgba(255, 255, 255, 0.94);
      padding: 0.7rem 1rem;
      border-radius: var(--radius-pill);
      box-shadow: var(--shadow-soft);
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: center;
      gap: 0.5rem;
      position: relative;
      z-index: 2;
    }

    .social-label {
      font-size: 0.9rem;
      opacity: 0.9;
    }

    .social-links {
      display: flex;
      flex-wrap: wrap;
      gap: 0.4rem;
    }

    .social-pill {
      display: inline-flex;
      align-items: center;
     

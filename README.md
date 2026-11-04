<div align="center">
  <style>
    body { background: #050b1d; }
    .profile-shell {
      max-width: 1280px;
      margin: 0 auto;
      padding: 18px 12px 40px;
      background:
        radial-gradient(circle at top, rgba(99,102,241,0.28), transparent 32%),
        radial-gradient(circle at 50% 100%, rgba(168,85,247,0.18), transparent 30%),
        #050b1d;
      color: #edf3ff;
      font-family: Inter, Segoe UI, sans-serif;
    }

    .hero {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 24px;
      padding: 10px 20px 18px;
      background:
        radial-gradient(circle at 18% 28%, rgba(168,85,247,0.20), transparent 18%),
        radial-gradient(circle at 65% 18%, rgba(59,130,246,0.24), transparent 26%),
        linear-gradient(90deg, rgba(7,13,31,0.96), rgba(7,12,28,0.92) 30%, rgba(10,14,31,0.94));
      border: 1px solid rgba(147, 197, 253, 0.15);
      border-radius: 24px 24px 0 0;
      overflow: hidden;
      box-shadow: 0 0 28px rgba(139,92,246,0.12);
    }

    .brand-quote {
      width: 180px;
      color: #f2d5ff;
      font-size: 18px;
      line-height: 1.25;
      font-style: italic;
      font-weight: 600;
      text-shadow: 0 0 18px rgba(168,85,247,0.35);
      opacity: 0.9;
      padding-left: 12px;
    }

    .brand-quote strong {
      display: block;
      background: linear-gradient(90deg, #f6d7ff, #d0b6ff, #8ad9ff);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    .title-wrap {
      text-align: center;
      flex: 1;
      min-width: 0;
    }

    .title-wrap h1 {
      margin: 10px 0 0;
      font-size: clamp(42px, 5vw, 84px);
      line-height: 0.95;
      font-weight: 800;
      letter-spacing: -0.05em;
      background: linear-gradient(90deg, #f4ebff 8%, #debefd 24%, #a7d7ff 56%, #f2f4ff 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      text-shadow: 0 0 22px rgba(191, 132, 252, 0.2);
    }

    .title-wrap .subtitle {
      margin-top: 10px;
      font-size: clamp(16px, 1.6vw, 26px);
      letter-spacing: 0.38em;
      text-transform: uppercase;
      color: #b3c4ff;
      font-weight: 600;
    }

    .title-wrap .tagline {
      margin-top: 18px;
      font-size: clamp(18px, 1.72vw, 30px);
      font-style: italic;
      color: #dfe8ff;
      opacity: 0.82;
      font-weight: 500;
      text-shadow: 0 0 18px rgba(147,197,253,0.25);
    }

    .brain-wrap {
      width: 260px;
      display: flex;
      justify-content: center;
      align-items: center;
      padding-right: 8px;
    }

    .brain-orb {
      position: relative;
      width: 200px;
      height: 160px;
      border-radius: 50%;
      background:
        radial-gradient(circle at 35% 35%, rgba(255,255,255,0.9), rgba(168,85,247,0.4) 18%, rgba(59,130,246,0.12) 52%, rgba(2,6,23,0.2) 100%);
      box-shadow: 0 0 25px rgba(107, 80, 255, 0.38), inset 0 0 32px rgba(162, 162, 255, 0.2);
    }

    .brain-orb::before,
    .brain-orb::after {
      content: "";
      position: absolute;
      inset: 12px 18px 14px 18px;
      border-radius: 50%;
      border: 1px solid rgba(191, 219, 254, 0.25);
      background: radial-gradient(circle at center, rgba(14, 165, 233, 0.18), transparent 60%);
    }

    .brain-orb::after {
      inset: 28px 28px 26px 28px;
      background: linear-gradient(135deg, rgba(196,181,253,0.18), rgba(59,130,246,0.05), rgba(255,255,255,0.08));
      border: 1px solid rgba(125,211,252,0.15);
    }

    .brain-orb .node {
      position: absolute;
      width: 8px;
      height: 8px;
      border-radius: 50%;
      background: white;
      box-shadow: 0 0 12px rgba(255,255,255,0.9);
    }

    .brain-orb .node:nth-child(1) { left: 22%; top: 35%; }
    .brain-orb .node:nth-child(2) { left: 52%; top: 18%; }
    .brain-orb .node:nth-child(3) { left: 68%; top: 42%; }
    .brain-orb .node:nth-child(4) { left: 42%; top: 64%; }
    .brain-orb .node:nth-child(5) { left: 72%; top: 68%; }
    .brain-orb .node:nth-child(6) { left: 30%; top: 68%; }

    .nav {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 18px;
      padding: 12px 20px 8px;
      background: rgba(7,12,27,0.96);
      border: 1px solid rgba(147, 197, 253, 0.14);
      border-top: 0;
      border-bottom: 0;
      font-size: 15px;
      color: #d7e7ff;
    }

    .nav a {
      color: #e5f0ff;
      text-decoration: none;
      opacity: 0.82;
      padding: 10px 10px 8px;
      border-bottom: 2px solid transparent;
      transition: 0.2s ease;
    }

    .nav a.active {
      opacity: 1;
      border-color: #d9b8ff;
      color: #f2ebff;
    }

    .content {
      display: grid;
      grid-template-columns: 330px minmax(0, 1fr) 300px;
      gap: 22px;
      padding: 22px 18px 4px;
      background: rgba(8, 12, 28, 0.96);
      border: 1px solid rgba(147, 197, 253, 0.14);
      border-top: 0;
      border-radius: 0 0 24px 24px;
      box-shadow: 0 18px 30px rgba(5, 8, 21, 0.5);
    }

    .panel {
      background: rgba(11, 18, 35, 0.92);
      border: 1px solid rgba(147, 197, 253, 0.18);
      border-radius: 18px;
      box-shadow: inset 0 1px 0 rgba(255,255,255,0.03);
    }

    .left-rail {
      padding: 22px 18px 18px;
      display: flex;
      flex-direction: column;
      align-items: center;
      position: relative;
    }

    .avatar-shell {
      width: 200px;
      height: 200px;
      border-radius: 50%;
      background: linear-gradient(135deg, #b76af5, #612dff, #6ca7ff);
      padding: 5px;
      box-shadow: 0 0 0 5px rgba(196, 124, 255, 0.2), 0 0 28px rgba(159, 92, 255, 0.35);
      margin-bottom: 22px;
    }

    .avatar-shell img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      border-radius: 50%;
      display: block;
      border: 2px solid rgba(255,255,255,0.15);
    }

    .profile-name {
      font-size: 38px;
      line-height: 0.95;
      font-weight: 800;
      letter-spacing: -0.05em;
      text-align: center;
      margin: 0 0 6px;
      background: linear-gradient(90deg, #fff, #deddff 35%, #9ad7ff 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    .handle {
      color: #b7c6f0;
      font-size: 17px;
      margin: 0 0 14px;
      text-align: center;
    }

    .bio {
      margin-top: 12px;
      color: #dce9ff;
      font-size: 18px;
      line-height: 1.55;
      text-align: left;
      width: 100%;
      padding: 8px 0;
    }

    .mini-btn {
      margin-top: 18px;
      width: 100%;
      padding: 12px 16px;
      border-radius: 12px;
      border: 1px solid rgba(196,132,255,0.4);
      background: rgba(17, 24, 39, 0.8);
      color: #ebf4ff;
      text-align: center;
      font-size: 15px;
      box-shadow: inset 0 1px 0 rgba(255,255,255,0.04);
    }

    .social-row {
      margin-top: 18px;
      width: 100%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      color: #dbeafe;
      font-size: 14px;
      opacity: 0.8;
    }

    .social-row small {
      color: #afc0ea;
    }

    .icon-strip {
      margin-top: 18px;
      width: 100%;
      display: flex;
      justify-content: center;
      gap: 8px;
      flex-wrap: wrap;
    }

    .chip {
      width: 38px;
      height: 38px;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      border-radius: 12px;
      font-size: 20px;
      background: linear-gradient(135deg, rgba(168,85,247,0.24), rgba(96,165,250,0.18));
      border: 1px solid rgba(196, 132, 255, 0.28);
      box-shadow: inset 0 0 16px rgba(255,255,255,0.05);
    }

    .main-panel {
      padding: 18px 20px 20px;
      min-width: 0;
    }

    .section-title {
      display: flex;
      align-items: center;
      gap: 10px;
      margin: 4px 0 16px;
      font-size: 21px;
      font-weight: 800;
      letter-spacing: -0.02em;
      color: #edf6ff;
    }

    .section-title .icon {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: 34px;
      height: 34px;
      border-radius: 10px;
      background: linear-gradient(135deg, rgba(168,85,247,0.28), rgba(55, 125, 255, 0.2));
      box-shadow: inset 0 0 20px rgba(255,255,255,0.04);
    }

    .about-block {
      display: grid;
      grid-template-columns: 1.3fr 0.8fr;
      gap: 20px;
      align-items: center;
      margin-bottom: 20px;
    }

    .about-copy {
      color: #dfeafc;
      font-size: 22px;
      line-height: 1.5;
      margin: 0;
    }

    .about-copy strong {
      color: #f3efff;
    }

    .feature-list {
      list-style: none;
      padding: 0;
      margin-top: 12px;
      display: grid;
      gap: 10px;
    }

    .feature-list li {
      display: flex;
      align-items: center;
      gap: 10px;
      color: #e7efff;
      font-size: 18px;
    }

    .feature-list li::before {
      content: "✓";
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: 22px;
      height: 22px;
      border-radius: 50%;
      background: linear-gradient(135deg, rgba(167,139,250,0.28), rgba(59,130,246,0.24));
      border: 1px solid rgba(196,132,255,0.3);
      color: #f3ebff;
      font-weight: 700;
      font-size: 13px;
      box-shadow: 0 0 12px rgba(168,85,247,0.2);
    }

    .code-glow {
      height: 180px;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 18px;
      background: radial-gradient(circle at center, rgba(147, 197, 253, 0.12) 0%, rgba(168,85,247,0.08) 40%, rgba(2,6,23,0.1) 100%);
      border: 1px solid rgba(147, 197, 253, 0.15);
      color: #d9d2ff;
      font-size: 82px;
      font-weight: 800;
      text-shadow: 0 0 20px rgba(160,120,255,0.3);
      letter-spacing: -0.08em;
      font-family: 'Consolas', monospace;
    }

    .stack-grid {
      display: grid;
      grid-template-columns: repeat(6, minmax(0, 1fr));
      gap: 16px;
      margin: 20px 0 18px;
    }

    .stack-item {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 10px;
      min-height: 90px;
      border-radius: 14px;
      background: rgba(13, 20, 34, 0.8);
      border: 1px solid rgba(157, 177, 255, 0.12);
      padding: 12px 8px;
      font-size: 13px;
      font-weight: 600;
      color: #e9f2ff;
      box-shadow: inset 0 1px 0 rgba(255,255,255,0.04);
    }

    .stack-item .logo {
      font-size: 28px;
      line-height: 1;
    }

    .tags {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 12px;
    }

    .tag {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      padding: 8px 14px;
      border-radius: 999px;
      background: rgba(17, 24, 39, 0.8);
      border: 1px solid rgba(147, 197, 253, 0.18);
      color: #ebf5ff;
      font-size: 14px;
      font-weight: 600;
      letter-spacing: 0.02em;
      box-shadow: inset 0 1px 0 rgba(255,255,255,0.03);
    }

    .quote {
      margin-top: 24px;
      text-align: center;
      font-size: clamp(16px, 1.7vw, 27px);
      font-style: italic;
      color: #dfeaff;
      opacity: 0.92;
      letter-spacing: 0.04em;
    }

    .right-rail {
      padding: 18px 16px 16px;
      display: flex;
      flex-direction: column;
      gap: 16px;
    }

    .stats-card {
      padding: 14px 12px 8px;
    }

    .stats-head {
      display: flex;
      align-items: center;
      gap: 10px;
      margin-bottom: 12px;
      font-size: 18px;
      font-weight: 800;
      color: #edf5ff;
    }

    .metric-list {
      list-style: none;
      padding: 0;
      margin: 0;
      display: grid;
      gap: 12px;
    }

    .metric-list li {
      display: flex;
      justify-content: space-between;
      align-items: center;
      color: #e7f0ff;
      font-size: 15px;
      font-weight: 600;
    }

    .metric-label {
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .dot {
      width: 10px;
      height: 10px;
      border-radius: 50%;
      background: linear-gradient(135deg, #a78bfa, #60a5fa);
      box-shadow: 0 0 12px rgba(147,197,253,0.35);
    }

    .calendar {
      display: grid;
      grid-template-columns: repeat(7, 1fr);
      gap: 4px;
      margin-top: 14px;
      padding: 8px 2px 0;
    }

    .day {
      width: 11px;
      height: 11px;
      border-radius: 2px;
      background: rgba(168, 85, 247, 0.14);
      border: 1px solid rgba(147, 197, 253, 0.08);
    }

    .day.l1 { background: rgba(168, 85, 247, 0.25); }
    .day.l2 { background: rgba(168, 85, 247, 0.42); }
    .day.l3 { background: rgba(168, 85, 247, 0.62); }

    .lang-list {
      list-style: none;
      margin: 12px 0 0;
      padding: 0;
      display: grid;
      gap: 10px;
    }

    .lang-item {
      display: grid;
      grid-template-columns: 1fr auto;
      align-items: center;
      gap: 8px;
      color: #edf4ff;
      font-size: 13px;
      font-weight: 600;
    }

    .lang-line {
      position: relative;
      display: block;
      height: 8px;
      border-radius: 999px;
      background: rgba(148, 163, 184, 0.12);
      overflow: hidden;
      grid-column: 1 / -1;
    }

    .lang-line > span {
      position: absolute;
      inset: 0 auto 0 0;
      border-radius: inherit;
      background: linear-gradient(90deg, #60a5fa, #8b5cf6);
    }

    @media (max-width: 980px) {
      .content {
        grid-template-columns: 1fr;
      }
      .about-block {
        grid-template-columns: 1fr;
      }
      .stack-grid {
        grid-template-columns: repeat(3, minmax(0, 1fr));
      }
      .hero {
        flex-wrap: wrap;
        justify-content: center;
      }
      .brain-wrap, .brand-quote {
        width: auto;
      }
    }

    @media (max-width: 620px) {
      .stack-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }
      .profile-name {
        font-size: 30px;
      }
      .title-wrap h1 {
        font-size: 42px;
      }
      .title-wrap .subtitle {
        letter-spacing: 0.18em;
      }
    }
  </style>

  <div class="profile-shell">
    <div class="hero">
      <div class="brand-quote">
        <strong>“Dream.<br>Code.<br>Innovate.”</strong>
      </div>

      <div class="title-wrap">
        <h1>Neural Architect</h1>
        <div class="subtitle">AI × DATA × SYSTEMS</div>
        <div class="tagline">Engineering Intelligence Through Code</div>
      </div>

      <div class="brain-wrap">
        <div class="brain-orb">
          <span class="node"></span>
          <span class="node"></span>
          <span class="node"></span>
          <span class="node"></span>
          <span class="node"></span>
          <span class="node"></span>
        </div>
      </div>
    </div>

    <nav class="nav">
      <a href="#" class="active">Overview</a>
      <a href="#">Repositories</a>
      <a href="#">Projects</a>
      <a href="#">Packages</a>
      <a href="#">Stars</a>
      <a href="#">Gists</a>
    </nav>

    <div class="content">
      <aside class="panel left-rail">
        <div class="avatar-shell">
          <img src="https://images.unsplash.com/photo-1544005313-94ddf0286df2?auto=format&fit=crop&w=800&q=80" alt="Profile portrait" />
        </div>

        <div class="profile-name">NeuralArchitect</div>
        <div class="handle">@NeuralArchitect</div>

        <div class="bio">
          Building intelligent solutions at the intersection of AI, data, and systems.
        </div>

        <div class="mini-btn">Edit profile</div>

        <div class="social-row">
          <span>247 followers</span>
          <span>•</span>
          <span>18 following</span>
        </div>

        <div class="icon-strip">
          <span class="chip">🧠</span>
          <span class="chip">⚙️</span>
          <span class="chip">📊</span>
          <span class="chip">🔒</span>
        </div>
      </aside>

      <main class="panel main-panel">
        <div class="section-title"><span class="icon">✦</span>About Me</div>

        <div class="about-block">
          <div>
            <p class="about-copy">
              I'm a passionate developer and researcher, exploring the frontiers of <strong>Artificial Intelligence</strong>, <strong>Data Science</strong>, and <strong>Cybersecurity</strong>.
            </p>

            <ul class="feature-list">
              <li>Understand. Engineer. Optimize.</li>
              <li>Turn complex problems into intelligent solutions.</li>
              <li>Always learning, always building.</li>
            </ul>
          </div>

          <div class="code-glow">&lt;/&gt;</div>
        </div>

        <div class="section-title"><span class="icon">⚡</span>Tech Stack</div>

        <div class="stack-grid">
          <div class="stack-item"><span class="logo">🐍</span>Python</div>
          <div class="stack-item"><span class="logo">C++</span>C++</div>
          <div class="stack-item"><span class="logo">☕</span>Java</div>
          <div class="stack-item"><span class="logo">JS</span>JavaScript</div>
          <div class="stack-item"><span class="logo">TS</span>TypeScript</div>
          <div class="stack-item"><span class="logo">🧠</span>PyTorch</div>
        </div>

        <div class="section-title"><span class="icon">🔬</span>Research Interests</div>
        <div class="tags">
          <span class="tag">🤖 Artificial Intelligence</span>
          <span class="tag">📈 Machine Learning</span>
          <span class="tag">📊 Data Science</span>
          <span class="tag">🛡️ Cybersecurity</span>
          <span class="tag">🧮 Computational Science</span>
          <span class="tag">⚙️ System Engineering</span>
          <span class="tag">🌐 Explainable AI</span>
        </div>

        <div class="quote">Think Computationally. Build Intelligently.</div>
      </main>

      <aside class="panel right-rail">
        <div class="stats-card">
          <div class="stats-head"><span>📊</span> GitHub Stats</div>

          <ul class="metric-list">
            <li><span class="metric-label"><span class="dot"></span>Total Stars</span><strong>1.2k</strong></li>
            <li><span class="metric-label"><span class="dot"></span>Total Commits</span><strong>5.8k</strong></li>
            <li><span class="metric-label"><span class="dot"></span>Repositories</span><strong>52</strong></li>
            <li><span class="metric-label"><span class="dot"></span>Contributions</span><strong>1.6k</strong></li>
          </ul>

          <div class="calendar">
            <span class="day l1"></span>
            <span class="day"></span>
            <span class="day l2"></span>
            <span class="day l3"></span>
            <span class="day"></span>
            <span class="day l2"></span>
            <span class="day l1"></span>
            <span class="day"></span>
            <span class="day l3"></span>
            <span class="day l2"></span>
            <span class="day l1"></span>
            <span class="day l3"></span>
            <span class="day l2"></span>
            <span class="day"></span>
            <span class="day l1"></span>
            <span class="day l3"></span>
            <span class="day"></span>
            <span class="day l2"></span>
            <span class="day l3"></span>
            <span class="day l1"></span>
            <span class="day"></span>
            <span class="day l2"></span>
            <span class="day l3"></span>
            <span class="day l1"></span>
            <span class="day l2"></span>
            <span class="day"></span>
            <span class="day l3"></span>
            <span class="day l1"></span>
            <span class="day"></span>
            <span class="day l2"></span>
            <span class="day l3"></span>
            <span class="day l1"></span>
            <span class="day l2"></span>
            <span class="day"></span>
            <span class="day l3"></span>
            <span class="day"></span>
            <span class="day l1"></span>
            <span class="day l2"></span>
            <span class="day"></span>
            <span class="day l3"></span>
          </div>
        </div>

        <div class="stats-card">
          <div class="stats-head"><span>📈</span> Top Languages</div>

          <ul class="lang-list">
            <li class="lang-item">
              <span>Python</span><strong>42.3%</strong>
              <span class="lang-line"><span style="width:42.3%"></span></span>
            </li>
            <li class="lang-item">
              <span>C++</span><strong>24.1%</strong>
              <span class="lang-line"><span style="width:24.1%"></span></span>
            </li>
            <li class="lang-item">
              <span>JavaScript</span><strong>15.6%</strong>
              <span class="lang-line"><span style="width:15.6%"></span></span>
            </li>
            <li class="lang-item">
              <span>TypeScript</span><strong>8.7%</strong>
              <span class="lang-line"><span style="width:8.7%"></span></span>
            </li>
            <li class="lang-item">
              <span>Others</span><strong>9.3%</strong>
              <span class="lang-line"><span style="width:9.3%"></span></span>
            </li>
          </ul>
        </div>
      </aside>
    </div>
  </div>
</div>

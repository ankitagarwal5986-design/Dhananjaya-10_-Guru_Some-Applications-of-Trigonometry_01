<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Brain &amp; Mind Academy • DHANANJAYA 10 - Some Applications of Trigonometry</title>

  <!-- MathJax v3 Configuration & Loader -->
  <script>
    window.MathJax = {
      tex: {
        inlineMath: [['\\(', '\\)']],
        displayMath: [['\\[', '\\]']],
        processEscapes: true
      },
      svg: { fontCache: 'global' }
    };
  </script>
  <script type="text/javascript" id="MathJax-script" async
    src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
  </script>

  <style>
    :root {
      --navy-dark: #0c4a6e;
      --brand-blue: #0284c7;
      --accent-cyan: #0ea5e9;
      --bg-tint: #f0f9ff;
      --card-surf: #ffffff;
      --border-accent: #7dd3fc;
      --border-soft: #bae6fd;
      --green-ok: #059669;
      --green-surf: #d1fae5;
      --red-fail: #dc2626;
      --red-surf: #fee2e2;
      --brand-gold: #f59e0b;
      --gold-dark: #d97706;
      --gold-surf: #fef3c7;
      --text-main: #0f172a;
      --text-muted: #475569;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
    }

    body {
      background-color: var(--bg-tint);
      color: var(--text-main);
      display: flex;
      flex-direction: column;
      min-height: 100vh;
    }

    header {
      background: var(--navy-dark);
      color: #fff;
      padding: 12px 24px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 4px 12px rgba(12, 74, 110, 0.15);
      position: sticky;
      top: 0;
      z-index: 100;
    }

    .brand-wrap {
      display: flex;
      align-items: center;
      gap: 14px;
    }

    .logo-badge {
      width: 46px;
      height: 46px;
      background: #ffffff;
      border-radius: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 2px 6px rgba(0,0,0,0.2);
    }

    .brand-title h1 {
      font-size: 1.15rem;
      font-weight: 700;
      letter-spacing: 0.5px;
    }

    .brand-title p {
      font-size: 0.78rem;
      color: var(--accent-cyan);
      font-weight: 500;
    }

    .header-controls {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .chip {
      background: rgba(255, 255, 255, 0.12);
      border: 1px solid var(--border-accent);
      padding: 6px 14px;
      border-radius: 20px;
      font-size: 0.85rem;
      font-weight: 600;
      display: flex;
      align-items: center;
      gap: 6px;
    }

    .btn-icon {
      background: transparent;
      border: 1px solid var(--border-accent);
      color: #fff;
      border-radius: 50%;
      width: 36px;
      height: 36px;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1rem;
    }

    nav {
      background: #ffffff;
      border-bottom: 1px solid var(--border-soft);
      display: flex;
      justify-content: center;
      gap: 8px;
      padding: 8px 16px;
    }

    nav button {
      background: none;
      border: none;
      outline: none;
      padding: 10px 20px;
      font-size: 0.95rem;
      font-weight: 600;
      color: var(--text-muted);
      cursor: pointer;
      border-radius: 8px;
      transition: all 0.2s;
    }

    nav button.active {
      background: var(--bg-tint);
      color: var(--brand-blue);
      border-bottom: 3px solid var(--brand-blue);
    }

    main {
      flex: 1;
      padding: 24px;
      max-width: 1400px;
      margin: 0 auto;
      width: 100%;
    }

    .view {
      display: none;
    }

    .view.active {
      display: block;
    }

    #loginGateView {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: rgba(12, 74, 110, 0.88);
      backdrop-filter: blur(5px);
      z-index: 1000;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .login-box {
      background: #fff;
      padding: 36px;
      border-radius: 16px;
      width: 100%;
      max-width: 420px;
      text-align: center;
      box-shadow: 0 14px 35px rgba(0,0,0,0.3);
    }

    .login-box h2 {
      font-size: 1.45rem;
      color: var(--navy-dark);
      margin-bottom: 6px;
    }

    .login-box p {
      font-size: 0.88rem;
      color: var(--text-muted);
      margin-bottom: 24px;
    }

    .login-box input {
      width: 100%;
      padding: 12px 16px;
      border: 1px solid var(--border-soft);
      border-radius: 8px;
      font-size: 1rem;
      margin-bottom: 16px;
      outline: none;
    }

    .btn-primary {
      background: var(--brand-blue);
      color: #fff;
      border: none;
      padding: 12px 24px;
      font-size: 1rem;
      font-weight: 600;
      border-radius: 8px;
      cursor: pointer;
      width: 100%;
      transition: background 0.2s;
    }

    .btn-primary:hover {
      background: var(--navy-dark);
    }

    .theory-card {
      background: #fff;
      border-radius: 12px;
      border: 1px solid var(--border-soft);
      padding: 24px;
      margin-bottom: 24px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.02);
    }

    .theory-card h3 {
      color: var(--navy-dark);
      margin-bottom: 14px;
      display: flex;
      align-items: center;
      gap: 8px;
      font-size: 1.25rem;
    }

    .theory-intro-text {
      color: var(--text-main);
      line-height: 1.65;
      margin-bottom: 18px;
      font-size: 0.95rem;
    }

    .compendium-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(360px, 1fr));
      gap: 20px;
      margin: 16px 0;
    }

    .comp-card {
      background: #ffffff;
      border: 1px solid var(--border-soft);
      border-radius: 10px;
      padding: 20px;
      display: flex;
      flex-direction: column;
      box-shadow: 0 2px 6px rgba(12, 74, 110, 0.04);
    }

    .comp-card h4 {
      color: var(--navy-dark);
      border-bottom: 2px solid var(--border-soft);
      padding-bottom: 8px;
      margin-bottom: 12px;
      font-size: 1.05rem;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .diagram-guide-step {
      background: #f8fafc;
      border-left: 4px solid var(--brand-blue);
      padding: 10px 14px;
      margin-bottom: 10px;
      border-radius: 0 6px 6px 0;
      font-size: 0.92rem;
      line-height: 1.6;
    }

    .video-callout-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 14px;
      margin-top: 18px;
    }

    .video-callout {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      background: #f8fafc;
      border: 1px solid var(--border-soft);
      padding: 14px 16px;
      border-radius: 8px;
      border-left: 4px solid var(--accent-cyan);
    }

    .video-callout a {
      color: var(--brand-blue);
      font-weight: 700;
      text-decoration: none;
      margin-top: 8px;
      font-size: 0.88rem;
    }

    .sheet-grid {
      display: grid;
      grid-template-columns: 1fr 350px;
      gap: 24px;
    }

    @media (max-width: 990px) {
      .sheet-grid {
        grid-template-columns: 1fr;
      }
    }

    .question-card {
      background: #fff;
      border-radius: 12px;
      border: 1px solid var(--border-soft);
      padding: 24px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.03);
    }

    .concept-tag {
      display: inline-block;
      padding: 4px 10px;
      border-radius: 14px;
      font-size: 0.75rem;
      font-weight: 700;
      letter-spacing: 0.4px;
      text-transform: uppercase;
      margin-bottom: 8px;
    }

    .concept-tag.single {
      background: #e0f2fe;
      color: #0369a1;
      border: 1px solid #7dd3fc;
    }

    .concept-tag.double {
      background: #fef3c7;
      color: #b45309;
      border: 1px solid #fde68a;
    }

    .svg-container {
      display: flex;
      justify-content: center;
      margin: 18px 0;
      padding: 16px;
      background: var(--bg-tint);
      border-radius: 8px;
      border: 1px solid var(--border-soft);
      overflow-x: auto;
    }

    .diagram-objective-card {
      background: #f0fdf4;
      border: 1px solid #bbf7d0;
      border-radius: 8px;
      padding: 12px 16px;
      margin: 12px 0 16px 0;
      font-size: 0.9rem;
      line-height: 1.6;
      color: #166534;
    }

    .diagram-objective-card strong {
      color: #14532d;
    }

    .step-box {
      margin-top: 16px;
      padding: 18px;
      border: 1px solid var(--border-soft);
      border-radius: 8px;
      background: #fff;
      display: none;
    }

    .step-box.unlocked {
      display: block;
      animation: fadeIn 0.3s ease-in;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(6px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .step-box.success {
      border-color: var(--green-ok);
      background: var(--green-surf);
    }

    .step-text-wrap {
      font-size: 1rem;
      line-height: 1.8;
      display: flex;
      align-items: center;
      flex-wrap: wrap;
      gap: 8px;
    }

    .inline-blank {
      width: 150px;
      padding: 6px 10px;
      font-size: 0.95rem;
      border: 2px dashed var(--brand-blue);
      border-radius: 6px;
      outline: none;
      background: #fff;
      color: var(--navy-dark);
      font-weight: 600;
      text-align: center;
    }

    .inline-blank:focus {
      border-style: solid;
      border-color: var(--accent-cyan);
      box-shadow: 0 0 0 3px rgba(14,165,233,0.2);
    }

    .inline-blank:disabled {
      border: 1px solid var(--green-ok);
      background: #fff;
      color: var(--green-ok);
      cursor: not-allowed;
    }

    .btn-verify {
      background: var(--accent-cyan);
      color: #fff;
      border: none;
      padding: 7px 16px;
      border-radius: 6px;
      font-weight: 600;
      cursor: pointer;
    }

    .btn-verify:hover {
      background: var(--brand-blue);
    }

    .btn-reveal {
      background: var(--brand-gold);
      color: #fff;
      border: none;
      padding: 6px 12px;
      border-radius: 6px;
      font-weight: 600;
      font-size: 0.85rem;
      cursor: pointer;
      margin-left: 6px;
    }

    .btn-reveal:hover {
      background: var(--gold-dark);
    }

    .attempts-badge {
      font-size: 0.8rem;
      font-weight: 700;
      padding: 3px 8px;
      border-radius: 12px;
      background: #f1f5f9;
      color: #64748b;
      margin-left: 6px;
    }

    .nav-toolbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 26px;
      padding-top: 18px;
      border-top: 1px solid var(--border-soft);
    }

    .nav-btn-group {
      display: flex;
      gap: 10px;
    }

    .btn-nav-action {
      background: #f8fafc;
      border: 1px solid var(--border-accent);
      color: var(--navy-dark);
      padding: 8px 18px;
      border-radius: 6px;
      font-weight: 600;
      font-size: 0.9rem;
      cursor: pointer;
      display: flex;
      align-items: center;
      gap: 6px;
      transition: all 0.15s;
    }

    .btn-nav-action:hover:not(:disabled) {
      background: var(--bg-tint);
      border-color: var(--brand-blue);
    }

    .btn-nav-action:disabled {
      opacity: 0.45;
      cursor: not-allowed;
    }

    .btn-skip {
      border-color: var(--brand-gold);
      color: var(--gold-dark);
      background: var(--gold-surf);
    }

    .btn-skip:hover {
      background: #fde68a;
    }

    .palette-box {
      background: #fff;
      border: 1px solid var(--border-soft);
      border-radius: 12px;
      padding: 16px;
      margin-bottom: 20px;
    }

    .palette-legend {
      display: flex;
      justify-content: space-between;
      font-size: 0.75rem;
      margin: 8px 0 12px 0;
      padding: 6px 8px;
      background: var(--bg-tint);
      border-radius: 6px;
    }

    .legend-item {
      display: flex;
      align-items: center;
      gap: 4px;
      font-weight: 600;
    }

    .legend-dot {
      width: 10px;
      height: 10px;
      border-radius: 50%;
    }

    .palette-section-title {
      font-size: 0.8rem;
      font-weight: 700;
      color: var(--text-muted);
      text-transform: uppercase;
      letter-spacing: 0.5px;
      margin: 12px 0 6px 0;
    }

    .palette-grid {
      display: grid;
      grid-template-columns: repeat(5, 1fr);
      gap: 6px;
      margin-bottom: 12px;
    }

    .palette-btn {
      aspect-ratio: 1;
      border: 1px solid var(--border-soft);
      background: var(--bg-tint);
      border-radius: 6px;
      font-weight: 600;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      transition: all 0.15s;
      font-size: 0.82rem;
      color: var(--navy-dark);
    }

    .palette-btn.active {
      border: 2px solid var(--navy-dark) !important;
      background: var(--border-accent);
      color: #fff;
      font-weight: 800;
    }

    .palette-btn.completed {
      background: var(--green-ok) !important;
      color: #fff !important;
      border-color: var(--green-ok) !important;
    }

    .palette-btn.skipped {
      background: var(--brand-gold) !important;
      color: #fff !important;
      border-color: var(--gold-dark) !important;
    }

    .tool-tabs {
      display: flex;
      border-bottom: 1px solid var(--border-soft);
      margin-bottom: 12px;
    }

    .tool-tabs button {
      flex: 1;
      border: none;
      background: none;
      padding: 8px;
      font-weight: 600;
      font-size: 0.85rem;
      cursor: pointer;
      color: var(--text-muted);
    }

    .tool-tabs button.active {
      color: var(--brand-blue);
      border-bottom: 2px solid var(--brand-blue);
    }

    .keypad-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 6px;
    }

    .keypad-btn {
      padding: 8px 4px;
      border: 1px solid var(--border-soft);
      background: #fff;
      border-radius: 4px;
      font-weight: 600;
      font-size: 0.85rem;
      cursor: pointer;
      text-align: center;
    }

    .keypad-btn:hover {
      background: var(--bg-tint);
    }

    #calcDisplay {
      width: 100%;
      padding: 8px;
      border: 1px solid var(--border-soft);
      border-radius: 4px;
      font-size: 1rem;
      text-align: right;
      margin-bottom: 8px;
      background: #f8fafc;
    }

    .hero-score-card {
      background: #fff;
      border-radius: 12px;
      border: 1px solid var(--border-soft);
      padding: 24px;
      text-align: center;
      margin-bottom: 24px;
    }

    .score-badge {
      font-size: 2.4rem;
      font-weight: 800;
      color: var(--brand-blue);
    }

    .toast {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background: var(--navy-dark);
      color: #fff;
      padding: 12px 20px;
      border-radius: 8px;
      box-shadow: 0 4px 16px rgba(0,0,0,0.2);
      display: none;
      z-index: 1000;
    }

    @media print {
      header, nav, .palette-box, #toolsPanel, .btn-primary, .btn-verify, #loginGateView, .nav-toolbar {
        display: none !important;
      }
      body { background: #fff; }
      main { width: 100%; max-width: 100%; padding: 0; }
      .sheet-grid { display: block; }
      .view { display: block !important; }
    }
  </style>
</head>
<body>

  <!-- Brand Header -->
  <header>
    <div class="brand-wrap">
      <div class="logo-badge">
        <svg width="34" height="34" viewBox="0 0 100 100" fill="none">
          <path d="M 20 30 Q 50 10 80 30" stroke="#f59e0b" stroke-width="8" stroke-linecap="round"/>
          <path d="M 26 40 Q 50 22 74 40" stroke="#f59e0b" stroke-width="8" stroke-linecap="round"/>
          <path d="M 32 50 Q 50 36 68 50" stroke="#f59e0b" stroke-width="7" stroke-linecap="round"/>
          <path d="M 18 80 Q 50 68 50 82 Q 50 68 82 80 L 82 52 Q 50 42 50 56 Q 50 42 18 52 Z" fill="#ffffff" stroke="#334155" stroke-width="7" stroke-linejoin="round"/>
        </svg>
      </div>
      <div class="brand-title">
        <h1>Brain &amp; Mind Academy</h1>
        <p>B&amp;M – The Experts • DHANANJAYA 10 (Some Applications of Trigonometry)</p>
      </div>
    </div>
    <div class="header-controls">
      <div class="chip" id="timerChip">⏱️ 00:00</div>
      <div class="chip" id="userPill">Roll No: Guest</div>
      <button class="btn-icon" id="audioToggleBtn" title="Toggle Audio">🔊</button>
    </div>
  </header>

  <!-- Navigation Bar -->
  <nav>
    <button class="tab-btn active" onclick="switchView('theoryView')">📖 Theory &amp; Strategy Guide</button>
    <button class="tab-btn" onclick="switchView('sheetView')">✍️ Interactive Practice Sheet</button>
    <button class="tab-btn" onclick="switchView('solutionsView')">📋 Complete Solutions</button>
  </nav>

  <!-- Login Gate Modal -->
  <div id="loginGateView">
    <div class="login-box">
      <h2>DHANANJAYA 10 Portal</h2>
      <p>Class 10 CBSE Chapter Mastery — Heights and Distances</p>
      <input type="text" id="rollInput" placeholder="Enter Student ID / Roll No" />
      <input type="password" id="passInput" placeholder="Passcode (Optional)" />
      <button class="btn-primary" onclick="initDirectLogin()">Initialize Workspace</button>
    </div>
  </div>

  <main>
    <!-- View 1: Theory & Strategy Guide -->
    <div id="theoryView" class="view active">
      <div class="theory-card">
        <h3>📐 Mastery Guide: Constructing Geometric Diagrams from Applied Scenarios</h3>
        <p class="theory-intro-text">
          In heights and distances problems, <strong>drawing an accurate geometric diagram is the first and most critical learning objective</strong>. A problem cannot be solved algebraically until the physical narrative (observers, towers, shadows, kites, angles) is faithfully converted into one or more coupled right-angled triangles.
        </p>

        <div class="compendium-grid">
          <!-- Guide 1: Line of Sight and Angles -->
          <div class="comp-card">
            <h4>1. Visual Reference Angles</h4>
            <div class="diagram-guide-step">
              <strong>Line of Sight:</strong> The straight line drawn from the eye of the observer to the target point being observed on an object.
            </div>
            <div class="diagram-guide-step">
              <strong>Angle of Elevation:</strong> The angle formed by the line of sight with the horizontal ground/eye-level when looking <em>upwards</em> (object is above observer level).
            </div>
            <div class="diagram-guide-step">
              <strong>Angle of Depression:</strong> The angle formed by the line of sight with the horizontal baseline when looking <em>downwards</em> (object is below observer level).
              <br/>
              <em>Crucial Rule:</em> By alternate interior angles across parallel horizontal lines, \(\text{Angle of Depression from top} = \text{Angle of Elevation at ground level}\).
            </div>
          </div>

          <!-- Guide 2: 4-Step Diagram Construction Algorithm -->
          <div class="comp-card">
            <h4>2. Four-Step Diagram Construction Algorithm</h4>
            <div class="diagram-guide-step">
              <strong>Step 1 (Ground &amp; Vertical Baseline):</strong> Draw the horizontal ground line. Erect vertical line segment(s) perpendicular (\(90^\circ\)) to represent towers, poles, buildings, or trees.
            </div>
            <div class="diagram-guide-step">
              <strong>Step 2 (Observer Height Distinction):</strong> If observer height is not mentioned, treat observer as a point on the ground. If given (e.g. \(1.5\text{ m}\) boy or \(1.2\text{ m}\) girl), draw an elevated horizontal line parallel to the ground at that height.
            </div>
            <div class="diagram-guide-step">
              <strong>Step 3 (Sightlines &amp; Angle Tagging):</strong> Connect observer point to target vertices. Draw angle arcs strictly between the line of sight and the <em>horizontal</em> reference.
            </div>
            <div class="diagram-guide-step">
              <strong>Step 4 (Variable Labeling &amp; Segment Splitting):</strong> Assign letters (\(A, B, C, D\)). Represent segments algebraically (e.g. \(x\), \(h - 1.5\), \(40 + x\)) to prepare for trigonometric substitution.
            </div>
          </div>

          <!-- Guide 3: Ratio Selection Strategy -->
          <div class="comp-card">
            <h4>3. Trigonometric Ratio Selection Strategy</h4>
            <div class="diagram-guide-step">
              <strong>Case A (Height &amp; Distance):</strong> When dealing with vertical heights (perpendicular) and horizontal ground separations (base), use <strong>\(\tan \theta\)</strong> (\(30^\circ, 45^\circ, 60^\circ\)):
              \[\tan 30^\circ = \frac{1}{\sqrt{3}}, \quad \tan 45^\circ = 1, \quad \tan 60^\circ = \sqrt{3}\]
            </div>
            <div class="diagram-guide-step">
              <strong>Case B (Slant Lengths):</strong> When dealing with taut ropes, slides, kite strings, or ladders (hypotenuse), select <strong>\(\sin \theta\)</strong> or <strong>\(\cos \theta\)</strong>:
              \[\sin 30^\circ = \frac{1}{2}, \quad \sin 45^\circ = \frac{1}{\sqrt{2}}, \quad \sin 60^\circ = \frac{\sqrt{3}}{2}\]
            </div>
          </div>
        </div>
      </div>

      <!-- Video Callouts Card -->
      <div class="theory-card">
        <h3>📹 Curated Master Video Lectures (Khan Academy)</h3>
        <div class="video-callout-grid">
          <div class="video-callout">
            <strong>Intro to Heights and Distances</strong>
            <p>Visualizing angles of elevation, angles of depression, and line-of-sight geometry.</p>
            <a href="https://www.khanacademy.org/math/ncert-class-10/xd6a17b08edbd2443:some-applications-of-trigonometry-ncert-new/xd6a17b08edbd2443:heights-and-distances/v/intro-to-heights-and-distances" target="_blank">Watch on Khan Academy →</a>
          </div>
          <div class="video-callout">
            <strong>Example 1: Heights and Distances</strong>
            <p>Step-by-step conversion of word problems into right-angled triangles with exact trigonometric substitution.</p>
            <a href="https://www.khanacademy.org/math/ncert-class-10/xd6a17b08edbd2443:some-applications-of-trigonometry-ncert-new/xd6a17b08edbd2443:heights-and-distances/v/example-1-heights-and-distances" target="_blank">Watch on Khan Academy →</a>
          </div>
          <div class="video-callout">
            <strong>Example 2: Heights and Distances</strong>
            <p>Working with two coupled right triangles, common baselines, and depression angles.</p>
            <a href="https://www.khanacademy.org/math/ncert-class-10/xd6a17b08edbd2443:some-applications-of-trigonometry-ncert-new/xd6a17b08edbd2443:heights-and-distances/v/example-2-heights-and-distances" target="_blank">Watch on Khan Academy →</a>
          </div>
        </div>
      </div>
    </div>

    <!-- View 2: Interactive Practice Sheet -->
    <div id="sheetView" class="view">
      <div class="sheet-grid">
        <div class="question-card" id="activeQuestionCard"></div>

        <aside>
          <div class="palette-box">
            <div style="display: flex; justify-content: space-between; align-items: center;">
              <h4>Question Palette</h4>
              <span style="font-size:0.8rem; color:var(--text-muted);" id="paletteCount">0 / 22</span>
            </div>

            <div class="palette-legend">
              <div class="legend-item"><span class="legend-dot" style="background:#059669;"></span> Done</div>
              <div class="legend-item"><span class="legend-dot" style="background:#f59e0b;"></span> Skipped</div>
              <div class="legend-item"><span class="legend-dot" style="background:#7dd3fc;"></span> Active</div>
              <div class="legend-item"><span class="legend-dot" style="background:#f0f9ff; border:1px solid #bae6fd;"></span> Unseen</div>
            </div>
            
            <div class="palette-section-title">Worked Examples (Q1 – Q7)</div>
            <div class="palette-grid" id="paletteExamplesGrid"></div>

            <div class="palette-section-title">Exercise 9.1 (Q8 – Q22)</div>
            <div class="palette-grid" id="paletteExerciseGrid"></div>
          </div>

          <div class="palette-box" id="toolsPanel">
            <div class="tool-tabs">
              <button id="tabKeypadBtn" class="active" onclick="toggleTool('keypad')">Math Keypad</button>
              <button id="tabCalcBtn" onclick="toggleTool('calc')">Calculator</button>
            </div>

            <div id="toolKeypad">
              <div class="keypad-grid">
                <button class="keypad-btn" onclick="insertSymbol('/')">/</button>
                <button class="keypad-btn" onclick="insertSymbol('√')">√</button>
                <button class="keypad-btn" onclick="insertSymbol('+')">+</button>
                <button class="keypad-btn" onclick="insertSymbol('-')">-</button>
                <button class="keypad-btn" onclick="insertSymbol('(')">(</button>
                <button class="keypad-btn" onclick="insertSymbol(')')">)</button>
                <button class="keypad-btn" onclick="insertSymbol('.')">.</button>
                <button class="keypad-btn" onclick="insertSymbol('1')">1</button>
                <button class="keypad-btn" onclick="insertSymbol('2')">2</button>
                <button class="keypad-btn" onclick="insertSymbol('3')">3</button>
                <button class="keypad-btn" onclick="insertSymbol('h')">h</button>
                <button class="keypad-btn" onclick="insertSymbol('x')">x</button>
              </div>
            </div>

            <div id="toolCalc" style="display: none;">
              <input type="text" id="calcDisplay" readonly value="" />
              <div class="keypad-grid">
                <button class="keypad-btn" onclick="pressCalc('7')">7</button>
                <button class="keypad-btn" onclick="pressCalc('8')">8</button>
                <button class="keypad-btn" onclick="pressCalc('9')">9</button>
                <button class="keypad-btn" onclick="pressCalc('/')">/</button>
                <button class="keypad-btn" onclick="pressCalc('4')">4</button>
                <button class="keypad-btn" onclick="pressCalc('5')">5</button>
                <button class="keypad-btn" onclick="pressCalc('6')">6</button>
                <button class="keypad-btn" onclick="pressCalc('*')">*</button>
                <button class="keypad-btn" onclick="pressCalc('1')">1</button>
                <button class="keypad-btn" onclick="pressCalc('2')">2</button>
                <button class="keypad-btn" onclick="pressCalc('3')">3</button>
                <button class="keypad-btn" onclick="pressCalc('-')">-</button>
                <button class="keypad-btn" onclick="pressCalc('0')">0</button>
                <button class="keypad-btn" onclick="pressCalc('.')">.</button>
                <button class="keypad-btn" onclick="calcEval()">=</button>
                <button class="keypad-btn" onclick="pressCalc('+')">+</button>
                <button class="keypad-btn" style="grid-column: span 2;" onclick="calcClear()">C</button>
                <button class="keypad-btn" style="grid-column: span 2;" onclick="calcSqrt()">√</button>
              </div>
            </div>
          </div>
        </aside>
      </div>
    </div>

    <!-- View 3: Complete Solutions -->
    <div id="solutionsView" class="view">
      <div class="hero-score-card">
        <h2>Chapter Performance Report</h2>
        <div class="score-badge" id="scoreValue">0 / 22</div>
        <p id="scoreSubtitle">Complete active questions to review your diagnostic analysis.</p>
        <button class="btn-primary" style="margin-top: 14px; max-width: 200px;" onclick="window.print()">🖨️ Print Solutions</button>
      </div>
      <div id="completeSolutionsContainer"></div>
    </div>
  </main>

  <div class="toast" id="toastMessage"></div>

  <script>
    // --- Master 22-Question Dataset for Some Applications of Trigonometry ---
    const CHAPTER_QUESTIONS = [
      // ========== WORKED EXAMPLES (Q1 - Q7) ==========
      {
        id: 1,
        concept: "single",
        source: "Example 1",
        title: "Height of Vertical Tower",
        prompt: "A tower stands vertically on the ground. From a point on the ground 15 m away from the foot of the tower, the angle of elevation of the top of the tower is found to be 60°. Find the height of the tower.",
        diagramObjective: "Draw vertical segment AB for the tower, horizontal segment BC = 15 m for the ground, and join hypotenuse AC with elevation angle ∠ACB = 60°.",
        svg: `<svg width="220" height="150" viewBox="0 0 140 100">
          <line x1="15" y1="85" x2="120" y2="85" stroke="#475569" stroke-width="2"/>
          <line x1="100" y1="85" x2="100" y2="15" stroke="#0c4a6e" stroke-width="3"/>
          <line x1="30" y1="85" x2="100" y2="15" stroke="#0284c7" stroke-width="2"/>
          <path d="M 45 85 A 15 15 0 0 0 42 77" fill="none" stroke="#f59e0b" stroke-width="1.5"/>
          <text x="48" y="80" font-size="7">60°</text>
          <text x="25" y="93" font-size="8" font-weight="bold">C</text>
          <text x="100" y="93" font-size="8" font-weight="bold">B</text>
          <text x="100" y="10" font-size="8" font-weight="bold">A</text>
          <text x="58" y="93" font-size="7">15 m</text>
          <text x="104" y="50" font-size="7" fill="#0c4a6e">h</text>
        </svg>`,
        steps: [
          { prefix: "Step 1: In right triangle \\(\\triangle ABC\\), \\(\\tan 60^\\circ = \\frac{AB}{BC} = \\frac{AB}{15}\\). Value of \\(\\tan 60^\\circ =\\)", expected: "√3", suffix: ".", explanation: "\\[\\tan 60^\\circ = \\sqrt{3}\\]" },
          { prefix: "Step 2: Equating \\(\\sqrt{3} = \\frac{AB}{15} \\implies AB =\\)", expected: "15√3", suffix: "m.", explanation: "\\[AB = 15\\sqrt{3}\\text{ m}\\]" }
        ]
      },
      {
        id: 2,
        concept: "single",
        source: "Example 2",
        title: "Electrician's Ladder Inclination",
        prompt: "An electrician has to repair an electric fault on a pole of height 5 m. She needs to reach a point 1.3 m below the top of the pole. The ladder is inclined at 60° to the horizontal. Find the length of the ladder and how far from the foot of the pole the ladder foot should be placed. (Take √3 = 1.73)",
        diagramObjective: "Draw vertical pole AD = 5 m. Mark reach point B such that AB = 1.3 m and BD = 3.7 m. Draw ladder BC inclined at 60° to horizontal ground CD.",
        svg: `<svg width="220" height="150" viewBox="0 0 140 110">
          <line x1="20" y1="95" x2="120" y2="95" stroke="#475569" stroke-width="2"/>
          <line x1="30" y1="95" x2="30" y2="15" stroke="#0c4a6e" stroke-width="3"/>
          <line x1="30" y1="40" x2="90" y2="95" stroke="#0284c7" stroke-width="2.5"/>
          <circle cx="30" cy="40" r="2" fill="#dc2626"/>
          <text x="20" y="15" font-size="7">A</text>
          <text x="18" y="42" font-size="7">B</text>
          <text x="22" y="103" font-size="7">D</text>
          <text x="94" y="103" font-size="7">C</text>
          <text x="68" y="90" font-size="7">60°</text>
          <text x="5" y="68" font-size="6">3.7 m</text>
        </svg>`,
        steps: [
          { prefix: "Step 1: Effective height \\(BD = 5 - 1.3 =\\)", expected: "3.7", suffix: "m.", explanation: "\\[BD = 5 - 1.3 = 3.7\\text{ m}\\]" },
          { prefix: "Step 2: Using \\(\\sin 60^\\circ = \\frac{BD}{BC} \\implies \\frac{\\sqrt{3}}{2} = \\frac{3.7}{BC}\\). Ladder length \\(BC = \\frac{7.4}{1.73} \\approx\\)", expected: "4.28", suffix: "m.", explanation: "\\[BC = \\frac{7.4}{1.73} \\approx 4.28\\text{ m}\\]" },
          { prefix: "Step 3: Distance of foot \\(CD = \\frac{BD}{\\tan 60^\\circ} = \\frac{3.7}{1.73} \\approx\\)", expected: "2.14", suffix: "m.", explanation: "\\[CD = \\frac{3.7}{\\sqrt{3}} \\approx 2.14\\text{ m}\\]" }
        ]
      },
      {
        id: 3,
        concept: "single",
        source: "Example 3",
        title: "Height of Chimney with Observer's Stature",
        prompt: "An observer 1.5 m tall is 28.5 m away from a chimney. The angle of elevation of the top of the chimney from her eyes is 45°. What is the height of the chimney?",
        diagramObjective: "Draw observer CD = 1.5 m and chimney AB. Draw horizontal eye-level line DE = 28.5 m parallel to ground CB. Sightline DA forms 45° with DE.",
        svg: `<svg width="220" height="150" viewBox="0 0 140 100">
          <line x1="15" y1="85" x2="125" y2="85" stroke="#475569" stroke-width="2"/>
          <line x1="30" y1="85" x2="30" y2="65" stroke="#0c4a6e" stroke-width="2"/>
          <line x1="110" y1="85" x2="110" y2="15" stroke="#0c4a6e" stroke-width="3"/>
          <line x1="30" y1="65" x2="110" y2="65" stroke="#94a3b8" stroke-dasharray="2"/>
          <line x1="30" y1="65" x2="110" y2="15" stroke="#0284c7" stroke-width="2"/>
          <text x="22" y="75" font-size="7">1.5</text>
          <text x="65" y="60" font-size="7">45°</text>
          <text x="65" y="93" font-size="7">28.5 m</text>
        </svg>`,
        steps: [
          { prefix: "Step 1: In \\(\\triangle ADE\\), \\(\\tan 45^\\circ = \\frac{AE}{DE} \\implies 1 = \\frac{AE}{28.5} \\implies AE =\\)", expected: "28.5", suffix: "m.", explanation: "\\[AE = 28.5\\text{ m}\\]" },
          { prefix: "Step 2: Total height \\(AB = AE + BE = 28.5 + 1.5 =\\)", expected: "30", suffix: "m.", explanation: "\\[AB = 28.5 + 1.5 = 30\\text{ m}\\]" }
        ]
      },
      {
        id: 4,
        concept: "double",
        source: "Example 4",
        title: "Flagstaff Hoisted on a 10 m Building",
        prompt: "From a point P on the ground, the angle of elevation of the top of a 10 m tall building is 30°. A flagstaff is hoisted at the top and the angle of elevation of the top of the flagstaff from P is 45°. Find the length of the flagstaff and the distance of the building from P. (Take √3 = 1.732)",
        diagramObjective: "Draw vertical building AB = 10 m with flagstaff BD on top. From ground point P, draw sightline PB at 30° and sightline PD at 45°.",
        svg: `<svg width="220" height="150" viewBox="0 0 140 100">
          <line x1="15" y1="85" x2="120" y2="85" stroke="#475569" stroke-width="2"/>
          <rect x="95" y="55" width="20" height="30" fill="#f8fafc" stroke="#0c4a6e" stroke-width="1.5"/>
          <line x1="100" y1="55" x2="100" y2="20" stroke="#0c4a6e" stroke-width="2"/>
          <line x1="25" y1="85" x2="100" y2="55" stroke="#0284c7" stroke-width="1.5"/>
          <line x1="25" y1="85" x2="100" y2="20" stroke="#0284c7" stroke-width="1.5"/>
          <text x="45" y="80" font-size="6">30°</text>
          <text x="50" y="70" font-size="6">45°</text>
          <text x="18" y="90" font-size="7">P</text>
        </svg>`,
        steps: [
          { prefix: "Step 1: In \\(\\triangle PAB\\), \\(\\tan 30^\\circ = \\frac{10}{AP} \\implies \\frac{1}{\\sqrt{3}} = \\frac{10}{AP}\\). Distance \\(AP = 10\\sqrt{3} =\\)", expected: "17.32", suffix: "m.", explanation: "\\[AP = 10 \\times 1.732 = 17.32\\text{ m}\\]" },
          { prefix: "Step 2: In \\(\\triangle PAD\\), \\(\\tan 45^\\circ = \\frac{10 + x}{10\\sqrt{3}} \\implies 1 = \\frac{10 + x}{17.32}\\). Length of flagstaff \\(x = 17.32 - 10 =\\)", expected: "7.32", suffix: "m.", explanation: "\\[x = 10(\\sqrt{3}-1) = 7.32\\text{ m}\\]" }
        ]
      },
      {
        id: 5,
        concept: "double",
        source: "Example 5",
        title: "Shadow Lengthening as Sun Altitude Decreases",
        prompt: "The shadow of a tower standing on level ground is found to be 40 m longer when the Sun's altitude is 30° than when it is 60°. Find the height of the tower.",
        diagramObjective: "Draw tower AB = h. Connect top A to ground shadow point C (where ∠ACB = 60° and BC = x) and point D (where ∠ADB = 30° and CD = 40 m).",
        svg: `<svg width="220" height="150" viewBox="0 0 150 90">
          <line x1="10" y1="75" x2="140" y2="75" stroke="#475569" stroke-width="2"/>
          <line x1="125" y1="75" x2="125" y2="15" stroke="#0c4a6e" stroke-width="3"/>
          <line x1="85" y1="75" x2="125" y2="15" stroke="#0284c7" stroke-width="1.5"/>
          <line x1="25" y1="75" x2="125" y2="15" stroke="#0284c7" stroke-width="1.5"/>
          <text x="35" y="70" font-size="6">30°</text>
          <text x="90" y="70" font-size="6">60°</text>
          <text x="50" y="83" font-size="6">40 m</text>
          <text x="105" y="83" font-size="6">x</text>
        </svg>`,
        steps: [
          { prefix: "Step 1: From \\(\\triangle ABC\\), \\(h = x\\tan 60^\\circ = x\\sqrt{3}\\). In \\(\\triangle ABD\\), \\(\\frac{h}{x + 40} = \\tan 30^\\circ = \\frac{1}{\\sqrt{3}}\\). Substituting \\(h\\) gives \\(3x = x + 40 \\implies x =\\)", expected: "20", suffix: "m.", explanation: "\\[3x - x = 40 \\implies 2x = 40 \\implies x = 20\\text{ m}\\]" },
          { prefix: "Step 2: Height of tower \\(h = 20\\sqrt{3}\\). Enter simplified exact radical:", expected: "20√3", suffix: "m.", explanation: "\\[h = 20\\sqrt{3}\\text{ m}\\]" }
        ]
      },
      {
        id: 6,
        concept: "double",
        source: "Example 6",
        title: "Depression of Building Top and Bottom from Multi-Storeyed Building",
        prompt: "The angles of depression of the top and bottom of an 8 m tall building from the top of a multi-storeyed building are 30° and 45° respectively. Find the height of the multi-storeyed building and the distance between them.",
        diagramObjective: "Draw multi-storeyed building PC and building AB = 8 m. Draw horizontal line PQ at top. Alternate angles give ∠PBD = 30° and ∠PAC = 45°.",
        svg: `<svg width="220" height="150" viewBox="0 0 140 110">
          <line x1="20" y1="95" x2="130" y2="95" stroke="#475569" stroke-width="2"/>
          <rect x="35" y="55" width="20" height="40" fill="#f8fafc" stroke="#0c4a6e" stroke-width="1.5"/>
          <line x1="110" y1="95" x2="110" y2="15" stroke="#0c4a6e" stroke-width="3"/>
          <line x1="110" y1="15" x2="80" y2="15" stroke="#94a3b8" stroke-dasharray="2"/>
          <line x1="55" y1="55" x2="110" y2="55" stroke="#94a3b8" stroke-dasharray="2"/>
          <line x1="55" y1="55" x2="110" y2="15" stroke="#0284c7" stroke-width="1.5"/>
          <line x1="35" y1="95" x2="110" y2="15" stroke="#0284c7" stroke-width="1.5"/>
          <text x="65" y="50" font-size="6">30°</text>
          <text x="50" y="85" font-size="6">45°</text>
        </svg>`,
        steps: [
          { prefix: "Step 1: Let \\(PC = h\\) and distance \\(AC = BD = d\\). In \\(\\triangle PAC\\), \\(\\tan 45^\\circ = \\frac{h}{d} = 1 \\implies h = d\\). In \\(\\triangle PBD\\), \\(\\tan 30^\\circ = \\frac{h - 8}{d} \\implies \\frac{1}{\\sqrt{3}} = \\frac{h - 8}{h}\\). Solving gives \\(h = 4(3 + \\text{?})\\):", expected: "√3", suffix: ".", explanation: "\\[h(\\sqrt{3}-1) = 8\\sqrt{3} \\implies h = 4(3 + \\sqrt{3})\\text{ m}\\]" },
          { prefix: "Step 2: Distance between buildings \\(AC = h = 4(3 + \\sqrt{3})\\text{ m}\\). Both height and distance equal", expected: "4(3+√3)", suffix: "m.", explanation: "\\[4(3 + \\sqrt{3})\\text{ m}\\]" }
        ]
      },
      {
        id: 7,
        concept: "double",
        source: "Example 7",
        title: "Width of River from Bridge Depressions",
        prompt: "From a point on a bridge across a river, the angles of depression of the banks on opposite sides are 30° and 45°. If the bridge is at a height of 3 m from the banks, find the width of the river.",
        diagramObjective: "Draw horizontal river surface AB with bridge point P directly above D (PD = 3 m). Line of sight PA has depression 30° (∠PAD = 30°), PB has depression 45° (∠PBD = 45°).",
        svg: `<svg width="220" height="130" viewBox="0 0 140 80">
          <line x1="15" y1="65" x2="125" y2="65" stroke="#0ea5e9" stroke-width="3"/>
          <line x1="70" y1="65" x2="70" y2="20" stroke="#0c4a6e" stroke-width="2" stroke-dasharray="2"/>
          <line x1="25" y1="65" x2="70" y2="20" stroke="#0284c7" stroke-width="2"/>
          <line x1="110" y1="65" x2="70" y2="20" stroke="#0284c7" stroke-width="2"/>
          <text x="73" y="45" font-size="7">3 m</text>
          <text x="35" y="60" font-size="6">30°</text>
          <text x="95" y="60" font-size="6">45°</text>
          <text x="20" y="74" font-size="7">A</text>
          <text x="68" y="74" font-size="7">D</text>
          <text x="112" y="74" font-size="7">B</text>
        </svg>`,
        steps: [
          { prefix: "Step 1: In \\(\\triangle APD\\), \\(\\tan 30^\\circ = \\frac{3}{AD} \\implies AD =\\)", expected: "3√3", suffix: "m.", explanation: "\\[AD = 3\\sqrt{3}\\text{ m}\\]" },
          { prefix: "Step 2: In \\(\\triangle PBD\\), \\(\\tan 45^\\circ = \\frac{3}{BD} \\implies BD =\\)", expected: "3", suffix: "m.", explanation: "\\[BD = 3\\text{ m}\\]" },
          { prefix: "Step 3: Total river width \\(AB = AD + BD = 3\\sqrt{3} + 3 = 3(\\sqrt{3} + \\text{?})\\):", expected: "1", suffix: "m.", explanation: "\\[AB = 3(\\sqrt{3} + 1)\\text{ m}\\]" }
        ]
      },

      // ========== EXERCISE 9.1 (Q8 - Q22) ==========
      {
        id: 8,
        concept: "single",
        source: "Exercise 9.1 Q1",
        title: "Circus Artist Climbing Vertical Pole Rope",
        prompt: "A circus artist is climbing a 20 m long rope tightly stretched and tied from the top of a vertical pole to the ground. Find the height of the pole if the angle made by the rope with the ground is 30°.",
        diagramObjective: "Draw vertical pole AB and ground BC. The hypotenuse AC represents the 20 m rope making angle ∠ACB = 30° with the ground.",
        svg: `<svg width="220" height="140" viewBox="0 0 130 90">
          <line x1="15" y1="75" x2="115" y2="75" stroke="#475569" stroke-width="2"/>
          <line x1="25" y1="75" x2="25" y2="20" stroke="#0c4a6e" stroke-width="3"/>
          <line x1="25" y1="20" x2="105" y2="75" stroke="#0284c7" stroke-width="2"/>
          <text x="15" y="20" font-size="8">A</text><text x="15" y="83" font-size="8">B</text><text x="108" y="83" font-size="8">C</text>
          <text x="65" y="42" font-size="7">20 m</text><text x="80" y="70" font-size="7">30°</text>
        </svg>`,
        steps: [
          { prefix: "Step 1: We select \\(\\sin 30^\\circ = \\frac{AB}{AC} = \\frac{AB}{20}\\). Since \\(\\sin 30^\\circ = \\frac{1}{2}\\), height \\(AB =\\)", expected: "10", suffix: "m.", explanation: "\\[AB = 20 \\times \\frac{1}{2} = 10\\text{ m}\\]" }
        ]
      },
      {
        id: 9,
        concept: "single",
        source: "Exercise 9.1 Q2",
        title: "Tree Broken by Storm Touching Ground",
        prompt: "A tree breaks due to a storm and the broken part bends so that the top of the tree touches the ground making an angle of 30° with it. The distance from the foot of the tree to the point where the top touches the ground is 8 m. Find the height of the tree.",
        diagramObjective: "Draw unbroken stem BC of height h1 and broken falling trunk CA of length h2 touching the ground at A (AB = 8 m, ∠CAB = 30°). Total height is h1 + h2.",
        svg: `<svg width="220" height="140" viewBox="0 0 130 90">
          <line x1="15" y1="75" x2="115" y2="75" stroke="#475569" stroke-width="2"/>
          <line x1="100" y1="75" x2="100" y2="35" stroke="#059669" stroke-width="3"/>
          <line x1="25" y1="75" x2="100" y2="35" stroke="#15803d" stroke-width="2.5"/>
          <line x1="100" y1="35" x2="100" y2="10" stroke="#94a3b8" stroke-dasharray="2"/>
          <text x="18" y="80" font-size="8">A</text><text x="104" y="80" font-size="8">B</text><text x="104" y="35" font-size="8">C</text>
          <text x="55" y="83" font-size="7">8 m</text><text x="40" y="70" font-size="7">30°</text>
        </svg>`,
        steps: [
          { prefix: "Step 1: Vertical part \\(BC = 8\\tan 30^\\circ = \\frac{8}{\\sqrt{3}}\\) m. Hypotenuse \\(AC = \\frac{8}{\\cos 30^\\circ} = \\frac{16}{\\sqrt{3}}\\) m. Total height \\(= \\frac{8}{\\sqrt{3}} + \\frac{16}{\\sqrt{3}} = \\frac{24}{\\sqrt{3}} =\\)", expected: "8√3", suffix: "m.", explanation: "\\[\\text{Total Height} = \\frac{24}{\\sqrt{3}} = 8\\sqrt{3}\\text{ m}\\]" }
        ]
      },
      {
        id: 10,
        concept: "single",
        source: "Exercise 9.1 Q3",
        title: "Park Contractor Installing Two Slides",
        prompt: "A contractor plans two slides: for children under 5, height is 1.5 m inclined at 30°; for elder children, steep slide of height 3 m inclined at 60°. Find the length of the slide in each case.",
        diagramObjective: "Draw two independent right triangles: Triangle 1 has altitude 1.5 m with 30° incline; Triangle 2 has altitude 3 m with 60° incline.",
        svg: `<svg width="220" height="120" viewBox="0 0 160 80">
          <polygon points="10,65 55,65 10,25" fill="#f0f9ff" stroke="#0c4a6e" stroke-width="1.5"/>
          <polygon points="80,65 140,65 80,10" fill="#f0f9ff" stroke="#0c4a6e" stroke-width="1.5"/>
          <text x="35" y="60" font-size="6">30°</text><text x="120" y="60" font-size="6">60°</text>
          <text x="2" y="45" font-size="6">1.5</text><text x="72" y="38" font-size="6">3</text>
        </svg>`,
        steps: [
          { prefix: "Step 1: For younger children, \\(\\sin 30^\\circ = \\frac{1.5}{L_1} \\implies L_1 = 1.5 \\times 2 =\\)", expected: "3", suffix: "m.", explanation: "\\[L_1 = 3\\text{ m}\\]" },
          { prefix: "Step 2: For elder children, \\(\\sin 60^\\circ = \\frac{3}{L_2} \\implies \\frac{\\sqrt{3}}{2} = \\frac{3}{L_2} \\implies L_2 = \\frac{6}{\\sqrt{3}} =\\)", expected: "2√3", suffix: "m.", explanation: "\\[L_2 = 2\\sqrt{3}\\text{ m}\\]" }
        ]
      },
      {
        id: 11,
        concept: "single",
        source: "Exercise 9.1 Q4",
        title: "Tower Elevation from 30 m Ground Point",
        prompt: "The angle of elevation of the top of a tower from a point on the ground 30 m away from its foot is 30°. Find the height of the tower.",
        diagramObjective: "Draw vertical tower AB and ground point C at distance BC = 30 m with elevation angle ∠ACB = 30°.",
        svg: `<svg width="220" height="130" viewBox="0 0 130 80">
          <line x1="15" y1="65" x2="115" y2="65" stroke="#475569" stroke-width="2"/>
          <line x1="100" y1="65" x2="100" y2="15" stroke="#0c4a6e" stroke-width="3"/>
          <line x1="25" y1="65" x2="100" y2="15" stroke="#0284c7" stroke-width="2"/>
          <text x="45" y="60" font-size="7">30°</text><text x="55" y="75" font-size="7">30 m</text>
        </svg>`,
        steps: [
          { prefix: "Step 1: \\(\\tan 30^\\circ = \\frac{h}{30} \\implies h = 30 \\times \\frac{1}{\\sqrt{3}} = \\frac{30}{\\sqrt{3}} =\\)", expected: "10√3", suffix: "m.", explanation: "\\[h = 10\\sqrt{3}\\text{ m}\\]" }
        ]
      },
      {
        id: 12,
        concept: "single",
        source: "Exercise 9.1 Q5",
        title: "Length of Taut Kite String",
        prompt: "A kite is flying at a height of 60 m above the ground. The string attached to the kite is tied to the ground with inclination 60°. Find the length of the string, assuming no slack.",
        diagramObjective: "Draw kite at point A with vertical height AB = 60 m above ground B. Hypotenuse AC represents string tied at ground point C with ∠ACB = 60°.",
        svg: `<svg width="220" height="130" viewBox="0 0 130 80">
          <line x1="15" y1="65" x2="115" y2="65" stroke="#475569" stroke-width="2"/>
          <line x1="90" y1="65" x2="90" y2="15" stroke="#0c4a6e" stroke-width="2" stroke-dasharray="2"/>
          <line x1="25" y1="65" x2="90" y2="15" stroke="#0284c7" stroke-width="2"/>
          <text x="95" y="42" font-size="7">60 m</text><text x="45" y="60" font-size="7">60°</text>
        </svg>`,
        steps: [
          { prefix: "Step 1: \\(\\sin 60^\\circ = \\frac{60}{L} \\implies \\frac{\\sqrt{3}}{2} = \\frac{60}{L} \\implies L = \\frac{120}{\\sqrt{3}} =\\)", expected: "40√3", suffix: "m.", explanation: "\\[L = 40\\sqrt{3}\\text{ m}\\]" }
        ]
      },
      {
        id: 13,
        concept: "double",
        source: "Exercise 9.1 Q6",
        title: "Distance Walked by a Boy Towards a 30 m Building",
        prompt: "A 1.5 m tall boy stands at some distance from a 30 m tall building. The angle of elevation from his eyes to the top of the building increases from 30° to 60° as he walks towards it. Find the distance he walked.",
        diagramObjective: "Draw building of 30 m and observer height of 1.5 m (effective vertical height = 28.5 m). Elevation increases from 30° to 60° as eye moves along horizontal level.",
        svg: `<svg width="220" height="140" viewBox="0 0 140 100">
          <line x1="10" y1="85" x2="130" y2="85" stroke="#475569" stroke-width="2"/>
          <line x1="20" y1="85" x2="20" y2="65" stroke="#0c4a6e" stroke-width="2"/>
          <line x1="120" y1="85" x2="120" y2="15" stroke="#0c4a6e" stroke-width="3"/>
          <line x1="20" y1="65" x2="120" y2="65" stroke="#94a3b8" stroke-dasharray="2"/>
          <line x1="20" y1="65" x2="120" y2="15" stroke="#0284c7" stroke-width="1.5"/>
          <line x1="70" y1="65" x2="120" y2="15" stroke="#0284c7" stroke-width="1.5"/>
          <text x="35" y="60" font-size="6">30°</text><text x="80" y="60" font-size="6">60°</text>
          <text x="124" y="45" font-size="6">28.5 m</text>
        </svg>`,
        steps: [
          { prefix: "Step 1: Effective height \\(= 30 - 1.5 = 28.5\\text{ m}\\). Initial distance \\(d_1 = \\frac{28.5}{\\tan 30^\\circ} = 28.5\\sqrt{3}\\) m. Final distance \\(d_2 = \\frac{28.5}{\\tan 60^\\circ} = \\frac{28.5}{\\sqrt{3}} = 9.5\\sqrt{3}\\) m. Distance walked \\(= 28.5\\sqrt{3} - 9.5\\sqrt{3} =\\)", expected: "19√3", suffix: "m.", explanation: "\\[\\text{Distance Walked} = 19\\sqrt{3}\\text{ m}\\]" }
        ]
      },
      {
        id: 14,
        concept: "double",
        source: "Exercise 9.1 Q7",
        title: "Transmission Tower on Top of a 20 m Building",
        prompt: "From a point on the ground, the angles of elevation of the bottom and top of a transmission tower fixed at the top of a 20 m high building are 45° and 60° respectively. Find the height of the tower.",
        diagramObjective: "Draw building AB = 20 m with tower AD = h on top. From ground point C, sightline to bottom of tower (A) is 45° and to top (D) is 60°.",
        svg: `<svg width="220" height="140" viewBox="0 0 130 95">
          <line x1="15" y1="80" x2="115" y2="80" stroke="#475569" stroke-width="2"/>
          <rect x="90" y="50" width="15" height="30" fill="#f8fafc" stroke="#0c4a6e" stroke-width="1.5"/>
          <line x1="97" y1="50" x2="97" y2="15" stroke="#dc2626" stroke-width="2.5"/>
          <line x1="25" y1="80" x2="97" y2="50" stroke="#0284c7" stroke-width="1.5"/>
          <line x1="25" y1="80" x2="97" y2="15" stroke="#0284c7" stroke-width="1.5"/>
          <text x="45" y="74" font-size="6">45°</text><text x="50" y="62" font-size="6">60°</text>
          <text x="105" y="65" font-size="6">20 m</text>
        </svg>`,
        steps: [
          { prefix: "Step 1: In base triangle, \\(\\tan 45^\\circ = \\frac{20}{x} \\implies x = 20\\text{ m}\\). In large triangle, \\(\\tan 60^\\circ = \\frac{20 + h}{20} \\implies 20\\sqrt{3} = 20 + h\\). Tower height \\(h = 20(\\sqrt{3} - \\text{?})\\):", expected: "1", suffix: "m.", explanation: "\\[h = 20(\\sqrt{3}-1)\\text{ m}\\]" }
        ]
      },
      {
        id: 15,
        concept: "double",
        source: "Exercise 9.1 Q8",
        title: "Height of Pedestal Supporting a 1.6 m Statue",
        prompt: "A statue 1.6 m tall stands on top of a pedestal. From a point on the ground, the angle of elevation of the top of the statue is 60° and of the top of the pedestal is 45°. Find the height of the pedestal.",
        diagramObjective: "Draw pedestal of height h with statue 1.6 m on top. From common ground point, elevation to pedestal top is 45° and to statue top is 60°.",
        svg: `<svg width="220" height="140" viewBox="0 0 130 95">
          <line x1="15" y1="80" x2="115" y2="80" stroke="#475569" stroke-width="2"/>
          <rect x="90" y="50" width="15" height="30" fill="#f8fafc" stroke="#0c4a6e" stroke-width="1.5"/>
          <line x1="97" y1="50" x2="97" y2="18" stroke="#10b981" stroke-width="2.5"/>
          <line x1="25" y1="80" x2="97" y2="50" stroke="#0284c7" stroke-width="1.5"/>
          <line x1="25" y1="80" x2="97" y2="18" stroke="#0284c7" stroke-width="1.5"/>
          <text x="102" y="35" font-size="6">1.6 m</text><text x="102" y="65" font-size="6">h</text>
        </svg>`,
        steps: [
          { prefix: "Step 1: Ground distance \\(x = h / \\tan 45^\\circ = h\\). For statue top, \\(\\tan 60^\\circ = \\frac{h + 1.6}{h} \\implies h\\sqrt{3} = h + 1.6 \\implies h(\\sqrt{3}-1) = 1.6\\). Rationalizing gives \\(h = 0.8(\\sqrt{3} + \\text{?})\\):", expected: "1", suffix: "m.", explanation: "\\[h = \\frac{1.6}{\\sqrt{3}-1} = 0.8(\\sqrt{3}+1)\\text{ m}\\]" }
        ]
      },
      {
        id: 16,
        concept: "double",
        source: "Exercise 9.1 Q9",
        title: "Height of Building from 50 m Tower",
        prompt: "The angle of elevation of the top of a building from the foot of a 50 m high tower is 30°, and the angle of elevation of the top of the tower from the foot of the building is 60°. Find the height of the building.",
        diagramObjective: "Draw tower AB = 50 m and building CD = h opposite each other. Connect foot B to D (30°) and foot D to A (60°).",
        svg: `<svg width="220" height="140" viewBox="0 0 140 90">
          <line x1="15" y1="75" x2="125" y2="75" stroke="#475569" stroke-width="2"/>
          <line x1="25" y1="75" x2="25" y2="15" stroke="#0c4a6e" stroke-width="3"/>
          <line x1="110" y1="75" x2="110" y2="45" stroke="#0c4a6e" stroke-width="2.5"/>
          <line x1="110" y1="75" x2="25" y2="15" stroke="#0284c7" stroke-width="1.5"/>
          <line x1="25" y1="75" x2="110" y2="45" stroke="#0284c7" stroke-width="1.5"/>
          <text x="12" y="45" font-size="7">50 m</text><text x="114" y="60" font-size="7">h</text>
        </svg>`,
        steps: [
          { prefix: "Step 1: Between feet, distance \\(d = \\frac{50}{\\tan 60^\\circ} = \\frac{50}{\\sqrt{3}}\\) m. Building height \\(h = d\\tan 30^\\circ = \\frac{50}{\\sqrt{3}} \\times \\frac{1}{\\sqrt{3}} =\\)", expected: "50/3", suffix: "m (or 16.67 m).", explanation: "\\[h = \\frac{50}{3} = 16\\frac{2}{3}\\text{ m}\\]" }
        ]
      },
      {
        id: 17,
        concept: "double",
        source: "Exercise 9.1 Q10",
        title: "Two Equal Poles Standing on Either Side of 80 m Road",
        prompt: "Two poles of equal heights stand on either side of an 80 m wide road. From a point between them on the road, the angles of elevation of the tops of the poles are 60° and 30°. Find the height of the poles and distances of the point from the poles.",
        diagramObjective: "Draw two equal vertical poles AB = CD = h separated by road BD = 80 m. Mark point P on road such that ∠APB = 60° and ∠CPD = 30°.",
        svg: `<svg width="220" height="140" viewBox="0 0 140 90">
          <line x1="15" y1="75" x2="125" y2="75" stroke="#475569" stroke-width="2"/>
          <line x1="25" y1="75" x2="25" y2="25" stroke="#0c4a6e" stroke-width="2.5"/>
          <line x1="115" y1="75" x2="115" y2="25" stroke="#0c4a6e" stroke-width="2.5"/>
          <line x1="55" y1="75" x2="25" y2="25" stroke="#0284c7" stroke-width="1.5"/>
          <line x1="55" y1="75" x2="115" y2="25" stroke="#0284c7" stroke-width="1.5"/>
          <text x="40" y="70" font-size="6">60°</text><text x="70" y="70" font-size="6">30°</text>
          <text x="65" y="85" font-size="6">80 m</text>
        </svg>`,
        steps: [
          { prefix: "Step 1: Let distance from 60° pole be \\(x\\), then other is \\(80 - x\\). \\(h = x\\sqrt{3} = \\frac{80 - x}{\\sqrt{3}} \\implies 3x = 80 - x \\implies 4x = 80 \\implies x =\\)", expected: "20", suffix: "m.", explanation: "\\[x = 20\\text{ m}, \\quad 80 - x = 60\\text{ m}\\]" },
          { prefix: "Step 2: Pole height \\(h = x\\sqrt{3} =\\)", expected: "20√3", suffix: "m.", explanation: "\\[h = 20\\sqrt{3}\\text{ m}\\]" }
        ]
      },
      {
        id: 18,
        concept: "double",
        source: "Exercise 9.1 Q11",
        title: "TV Tower on a Canal Bank",
        prompt: "A TV tower stands on a canal bank. From a point on the other bank opposite the tower, the elevation of the top is 60°. From another point 20 m away along the same line, the elevation is 30°. Find the tower height and canal width.",
        diagramObjective: "Draw tower AB = h, canal width BC = x, and extension CD = 20 m. Angle of elevation from C is 60° and from D is 30°.",
        svg: `<svg width="220" height="140" viewBox="0 0 150 90">
          <line x1="10" y1="75" x2="140" y2="75" stroke="#475569" stroke-width="2"/>
          <line x1="125" y1="75" x2="125" y2="15" stroke="#0c4a6e" stroke-width="3"/>
          <line x1="85" y1="75" x2="125" y2="15" stroke="#0284c7" stroke-width="1.5"/>
          <line x1="25" y1="75" x2="125" y2="15" stroke="#0284c7" stroke-width="1.5"/>
          <text x="45" y="70" font-size="6">30°</text><text x="95" y="70" font-size="6">60°</text>
          <text x="50" y="83" font-size="6">20 m</text><text x="105" y="83" font-size="6">x</text>
        </svg>`,
        steps: [
          { prefix: "Step 1: \\(h = x\\sqrt{3} = \\frac{x + 20}{\\sqrt{3}} \\implies 3x = x + 20 \\implies 2x = 20\\). Canal width \\(x =\\)", expected: "10", suffix: "m.", explanation: "\\[x = 10\\text{ m}\\]" },
          { prefix: "Step 2: Tower height \\(h = 10\\sqrt{3}\\). Enter exact form:", expected: "10√3", suffix: "m.", explanation: "\\[h = 10\\sqrt{3}\\text{ m}\\]" }
        ]
      },
      {
        id: 19,
        concept: "double",
        source: "Exercise 9.1 Q12",
        title: "Cable Tower Observed from 7 m Building",
        prompt: "From the top of a 7 m high building, the angle of elevation of the top of a cable tower is 60° and the angle of depression of its foot is 45°. Determine the height of the tower.",
        diagramObjective: "Draw building AB = 7 m and cable tower CD. From eye level at A, sightline to tower top C is 60° and depression to tower base D is 45° (giving horizontal distance d = 7 m).",
        svg: `<svg width="220" height="140" viewBox="0 0 130 100">
          <line x1="15" y1="85" x2="115" y2="85" stroke="#475569" stroke-width="2"/>
          <line x1="30" y1="85" x2="30" y2="55" stroke="#0c4a6e" stroke-width="2.5"/>
          <line x1="95" y1="85" x2="95" y2="15" stroke="#0c4a6e" stroke-width="3"/>
          <line x1="30" y1="55" x2="95" y2="55" stroke="#94a3b8" stroke-dasharray="2"/>
          <line x1="30" y1="55" x2="95" y2="15" stroke="#0284c7" stroke-width="1.5"/>
          <line x1="30" y1="55" x2="95" y2="85" stroke="#0284c7" stroke-width="1.5"/>
          <text x="20" y="70" font-size="7">7 m</text><text x="50" y="50" font-size="6">60°</text><text x="50" y="65" font-size="6">45°</text>
        </svg>`,
        steps: [
          { prefix: "Step 1: Distance between building and tower \\(d = \\frac{7}{\\tan 45^\\circ} = 7\\text{ m}\\). Upper portion \\(= 7\\tan 60^\\circ =\\)", expected: "7√3", suffix: "m.", explanation: "\\[7\\sqrt{3}\\text{ m}\\]" },
          { prefix: "Step 2: Total tower height \\(= 7 + 7\\sqrt{3} = 7(\\sqrt{3} + \\text{?})\\):", expected: "1", suffix: "m.", explanation: "\\[\\text{Height} = 7(\\sqrt{3}+1)\\text{ m}\\]" }
        ]
      },
      {
        id: 20,
        concept: "double",
        source: "Exercise 9.1 Q13",
        title: "Two Ships Observed from 75 m Lighthouse",
        prompt: "As observed from the top of a 75 m high lighthouse, the angles of depression of two ships in line on the same side are 30° and 45°. Find the distance between the two ships.",
        diagramObjective: "Draw lighthouse AB = 75 m. From top A, sightlines to ships C and D on sea level give alternate angles of elevation ∠ACB = 45° and ∠ADB = 30°.",
        svg: `<svg width="220" height="130" viewBox="0 0 150 80">
          <line x1="10" y1="65" x2="140" y2="65" stroke="#0ea5e9" stroke-width="3"/>
          <line x1="125" y1="65" x2="125" y2="15" stroke="#0c4a6e" stroke-width="3"/>
          <line x1="125" y1="15" x2="80" y2="65" stroke="#0284c7" stroke-width="1.5"/>
          <line x1="125" y1="15" x2="25" y2="65" stroke="#0284c7" stroke-width="1.5"/>
          <text x="130" y="40" font-size="7">75 m</text><text x="85" y="60" font-size="6">45°</text><text x="40" y="60" font-size="6">30°</text>
        </svg>`,
        steps: [
          { prefix: "Step 1: Distance to nearer ship \\(= 75/\\tan 45^\\circ = 75\\text{ m}\\). Distance to farther ship \\(= 75/\\tan 30^\\circ = 75\\sqrt{3}\\) m. Distance between ships \\(= 75(\\sqrt{3} - \\text{?})\\):", expected: "1", suffix: "m.", explanation: "\\[\\text{Distance} = 75(\\sqrt{3}-1)\\text{ m}\\]" }
        ]
      },
      {
        id: 21,
        concept: "double",
        source: "Exercise 9.1 Q14",
        title: "Moving Balloon Observed by a 1.2 m Girl",
        prompt: "A 1.2 m tall girl spots a balloon moving horizontally at a height of 88.2 m from the ground. The angle of elevation from her eyes reduces from 60° to 30°. Find the distance travelled by the balloon.",
        diagramObjective: "Draw horizontal ground and girl eye-level line. Net vertical height = 88.2 - 1.2 = 87 m. Balloon moves horizontally between 60° and 30° elevation sightlines.",
        svg: `<svg width="220" height="140" viewBox="0 0 150 90">
          <line x1="10" y1="75" x2="140" y2="75" stroke="#475569" stroke-width="2"/>
          <line x1="20" y1="75" x2="20" y2="60" stroke="#0c4a6e" stroke-width="2"/>
          <circle cx="70" cy="20" r="8" fill="#f87171"/>
          <circle cx="125" cy="20" r="8" fill="#f87171"/>
          <line x1="20" y1="60" x2="70" y2="20" stroke="#0284c7" stroke-width="1.5"/>
          <line x1="20" y1="60" x2="125" y2="20" stroke="#0284c7" stroke-width="1.5"/>
          <text x="38" y="55" font-size="6">60°</text><text x="55" y="55" font-size="6">30°</text>
        </svg>`,
        steps: [
          { prefix: "Step 1: Effective height \\(= 88.2 - 1.2 = 87\\text{ m}\\). Initial horizontal distance \\(= \\frac{87}{\\sqrt{3}} = 29\\sqrt{3}\\) m. Final distance \\(= 87\\sqrt{3}\\) m. Distance travelled \\(= 87\\sqrt{3} - 29\\sqrt{3} =\\)", expected: "58√3", suffix: "m.", explanation: "\\[\\text{Distance} = 58\\sqrt{3}\\text{ m}\\]" }
        ]
      },
      {
        id: 22,
        concept: "double",
        source: "Exercise 9.1 Q15",
        title: "Uniform Speed Car Approaching Tower",
        prompt: "A man on top of a tower observes a car at depression 30° approaching the foot of the tower. Six seconds later, the depression of the car is 60°. Find the time taken by the car to reach the foot of the tower from this point.",
        diagramObjective: "Draw tower of height h. Car moves from point C (angle 30°, distance d1 = h√3) to point D (angle 60°, distance d2 = h/√3) in 6 seconds.",
        svg: `<svg width="220" height="130" viewBox="0 0 150 85">
          <line x1="10" y1="70" x2="140" y2="70" stroke="#475569" stroke-width="2"/>
          <line x1="125" y1="70" x2="125" y2="15" stroke="#0c4a6e" stroke-width="3"/>
          <line x1="125" y1="15" x2="80" y2="70" stroke="#0284c7" stroke-width="1.5"/>
          <line x1="125" y1="15" x2="25" y2="70" stroke="#0284c7" stroke-width="1.5"/>
          <text x="40" y="65" font-size="6">30°</text><text x="85" y="65" font-size="6">60°</text>
          <text x="45" y="78" font-size="6">6 sec</text><text x="98" y="78" font-size="6">t = ?</text>
        </svg>`,
        steps: [
          { prefix: "Step 1: Distance covered in 6 s \\(= h\\sqrt{3} - \\frac{h}{\\sqrt{3}} = \\frac{2h}{\\sqrt{3}}\\). The remaining distance to foot is \\(\\frac{h}{\\sqrt{3}}\\), which is half the initial distance. Since speed is uniform, time taken \\(= 6 / 2 =\\)", expected: "3", suffix: "seconds.", explanation: "\\[t = \\frac{6}{2} = 3\\text{ seconds}\\]" }
        ]
      }
    ];

    let currentAuthUser = null;
    let currentQuestionIndex = 0;
    let stepProgress = CHAPTER_QUESTIONS.map(() => ({ completedSteps: 0, status: "unseen" }));
    let stepAttempts = {};
    let audioMuted = false;
    let totalSeconds = 0;
    let timerInterval = null;
    let activeInputRef = null;

    const AudioEngine = {
      ctx: null,
      init() {
        if (!this.ctx) {
          this.ctx = new (window.AudioContext || window.webkitAudioContext)();
        }
      },
      playTone(freq, type, duration, delay = 0) {
        if (audioMuted || !this.ctx) return;
        setTimeout(() => {
          try {
            const osc = this.ctx.createOscillator();
            const gain = this.ctx.createGain();
            osc.type = type;
            osc.frequency.setValueAtTime(freq, this.ctx.currentTime);
            gain.gain.setValueAtTime(0.12, this.ctx.currentTime);
            gain.gain.exponentialRampToValueAtTime(0.0001, this.ctx.currentTime + duration);
            osc.connect(gain);
            gain.connect(this.ctx.destination);
            osc.start();
            osc.stop(this.ctx.currentTime + duration);
          } catch (e) {
            console.warn("AudioContext error", e);
          }
        }, delay * 1000);
      },
      correct() {
        this.init();
        this.playTone(659.25, 'sine', 0.15, 0);
        this.playTone(880.00, 'sine', 0.25, 0.12);
      },
      incorrect() {
        this.init();
        this.playTone(196.00, 'triangle', 0.2, 0);
        this.playTone(146.83, 'triangle', 0.3, 0.12);
      },
      milestone() {
        this.init();
        [523.25, 659.25, 783.99, 1046.50].forEach((freq, idx) => {
          this.playTone(freq, 'sine', 0.25, idx * 0.1);
        });
      }
    };

    function startTimer() {
      if (timerInterval) clearInterval(timerInterval);
      timerInterval = setInterval(() => {
        totalSeconds++;
        const mins = String(Math.floor(totalSeconds / 60)).padStart(2, '0');
        const secs = String(totalSeconds % 60).padStart(2, '0');
        document.getElementById('timerChip').innerText = `⏱️ ${mins}:${secs}`;

        if (totalSeconds === 1200 || (totalSeconds > 1200 && totalSeconds % 300 === 0)) {
          AudioEngine.milestone();
          showToast(`Pacing Check: ${Math.floor(totalSeconds / 60)} minutes elapsed.`);
        }
      }, 1000);
    }

    function showToast(msg) {
      const t = document.getElementById('toastMessage');
      t.innerText = msg;
      t.style.display = 'block';
      setTimeout(() => { t.style.display = 'none'; }, 3500);
    }

    function initDirectLogin() {
      const roll = document.getElementById('rollInput').value.trim() || 'Student-10';
      currentAuthUser = roll;
      sessionStorage.setItem('bm_user', roll);
      document.getElementById('userPill').innerText = `Roll No: ${roll}`;
      document.getElementById('loginGateView').style.display = 'none';
      AudioEngine.init();
      startTimer();
      renderPalettes();
      loadQuestion(0);
      renderSolutions();
    }

    function normalizeInput(str) {
      return str.toLowerCase().replace(/\s+/g, '').replace(/−/g, '-');
    }

    function parseNumeric(val) {
      if (val.includes('/')) {
        const parts = val.split('/');
        return parseFloat(parts[0]) / parseFloat(parts[1]);
      }
      return parseFloat(val);
    }

    function checkNumericalTolerance(val1, val2) {
      const n1 = parseNumeric(val1);
      const n2 = parseNumeric(val2);
      if (isNaN(n1) || isNaN(n2)) return false;
      return Math.abs(n1 - n2) <= 0.05;
    }

    function switchView(viewId) {
      document.querySelectorAll('.view').forEach(v => v.classList.remove('active'));
      document.querySelectorAll('nav button').forEach(b => b.classList.remove('active'));
      document.getElementById(viewId).classList.add('active');

      const btnMap = { 'theoryView': 0, 'sheetView': 1, 'solutionsView': 2 };
      document.querySelectorAll('nav button')[btnMap[viewId]].classList.add('active');

      if (window.MathJax && window.MathJax.typesetPromise) {
        MathJax.typesetPromise();
      }
    }

    function renderPalettes() {
      const exGrid = document.getElementById('paletteExamplesGrid');
      const qGrid = document.getElementById('paletteExerciseGrid');
      exGrid.innerHTML = '';
      qGrid.innerHTML = '';

      let doneCount = 0;
      CHAPTER_QUESTIONS.forEach((q, idx) => {
        const state = stepProgress[idx];
        if (state.status === "completed") doneCount++;

        const btn = document.createElement('button');
        let stateClass = '';
        if (idx === currentQuestionIndex) {
          stateClass = 'active';
        } else if (state.status === "completed") {
          stateClass = 'completed';
        } else if (state.status === "skipped") {
          stateClass = 'skipped';
        }

        btn.className = `palette-btn ${stateClass}`;
        btn.innerText = idx + 1;
        btn.title = `${q.source}: ${q.title}`;
        btn.onclick = () => loadQuestion(idx);

        if (idx < 7) {
          exGrid.appendChild(btn);
        } else {
          qGrid.appendChild(btn);
        }
      });
      document.getElementById('paletteCount').innerText = `${doneCount} / ${CHAPTER_QUESTIONS.length}`;
    }

    function loadQuestion(idx) {
      currentQuestionIndex = idx;
      renderPalettes();
      const q = CHAPTER_QUESTIONS[idx];
      const prog = stepProgress[idx];

      let stepsHtml = '';
      q.steps.forEach((st, sIdx) => {
        const isUnlocked = sIdx <= prog.completedSteps;
        const isPassed = sIdx < prog.completedSteps;
        const key = `${idx}_${sIdx}`;
        const attempts = stepAttempts[key] || 0;

        stepsHtml += `
          <div class="step-box ${isUnlocked ? 'unlocked' : ''} ${isPassed ? 'success' : ''}" id="stepBox_${idx}_${sIdx}">
            <div class="step-text-wrap">
              <span>${st.prefix}</span>
              <input type="text" class="inline-blank" id="stepInput_${idx}_${sIdx}" 
                value="${isPassed ? st.expected : ''}" 
                placeholder="enter answer"
                ${isPassed ? 'disabled' : ''} 
                onfocus="activeInputRef = this;" />
              <span>${st.suffix}</span>
              ${!isPassed ? `
                <button class="btn-verify" onclick="verifyStep(${idx}, ${sIdx})">Verify</button>
                <span class="attempts-badge" id="attemptBadge_${idx}_${sIdx}">Attempts: ${attempts}/2</span>
                ${attempts >= 2 ? `<button class="btn-reveal" onclick="autoFillStep(${idx}, ${sIdx})">Auto-Fill Correct Answer</button>` : ''}
              ` : `<span style="color: var(--green-ok); font-weight: bold; margin-left: 8px;">✓ Verified</span>`}
            </div>
            ${isPassed ? `<div style="margin-top:10px; padding:10px; background:#eff6ff; border-radius:6px; border-left:4px solid var(--brand-blue); font-size:0.92rem; color:var(--text-main);">${st.explanation}</div>` : ''}
          </div>
        `;
      });

      const tagClass = q.concept === 'single' ? 'single' : 'double';
      const tagText = q.concept === 'single' ? 'Single Right Triangle' : 'Two Coupled Triangles';

      const prevDisabled = idx === 0 ? 'disabled' : '';
      const nextDisabled = idx === CHAPTER_QUESTIONS.length - 1 ? 'disabled' : '';

      const html = `
        <span class="concept-tag ${tagClass}">${tagText}</span>
        <span style="font-size:0.85rem; font-weight:700; color:var(--text-muted); margin-left: 8px;">[${q.source}]</span>
        <h2 style="color:var(--navy-dark); margin: 6px 0 10px 0;">Problem ${q.id}: ${q.title}</h2>
        <p style="margin-top: 8px; line-height: 1.65;">${q.prompt}</p>
        
        <div class="diagram-objective-card">
          <strong>📐 Diagram Learning Objective:</strong> ${q.diagramObjective}
        </div>

        <div class="svg-container">${q.svg}</div>
        <div id="stepsContainer">${stepsHtml}</div>

        <!-- Action Toolbar -->
        <div class="nav-toolbar">
          <button class="btn-nav-action" onclick="navigateQuestion(-1)" ${prevDisabled}>
            ⏮ Previous
          </button>
          <div class="nav-btn-group">
            <button class="btn-nav-action btn-skip" onclick="skipQuestion()">
              ⏭ Skip Question
            </button>
            <button class="btn-nav-action" onclick="navigateQuestion(1)" ${nextDisabled}>
              Next ❯
            </button>
          </div>
        </div>
      `;

      document.getElementById('activeQuestionCard').innerHTML = html;
      if (window.MathJax && window.MathJax.typesetPromise) {
        MathJax.typesetPromise();
      }
    }

    function navigateQuestion(delta) {
      const target = currentQuestionIndex + delta;
      if (target >= 0 && target < CHAPTER_QUESTIONS.length) {
        loadQuestion(target);
      }
    }

    function skipQuestion() {
      if (stepProgress[currentQuestionIndex].status !== "completed") {
        stepProgress[currentQuestionIndex].status = "skipped";
      }
      showToast(`Question ${currentQuestionIndex + 1} marked as Skipped (Amber/Gold).`);
      renderPalettes();
      navigateQuestion(1);
    }

    function autoFillStep(qIdx, sIdx) {
      const inputEl = document.getElementById(`stepInput_${qIdx}_${sIdx}`);
      if (inputEl) {
        inputEl.value = CHAPTER_QUESTIONS[qIdx].steps[sIdx].expected;
        verifyStep(qIdx, sIdx);
      }
    }

    function verifyStep(qIdx, sIdx) {
      const inputEl = document.getElementById(`stepInput_${qIdx}_${sIdx}`);
      const val = normalizeInput(inputEl.value);
      const expected = normalizeInput(CHAPTER_QUESTIONS[qIdx].steps[sIdx].expected);
      const key = `${qIdx}_${sIdx}`;

      const isCorrect = (val === expected) || checkNumericalTolerance(val, expected);

      if (isCorrect) {
        AudioEngine.correct();
        stepProgress[qIdx].completedSteps++;
        if (stepProgress[qIdx].completedSteps >= CHAPTER_QUESTIONS[qIdx].steps.length) {
          stepProgress[qIdx].status = "completed";
          AudioEngine.milestone();
          showToast(`Problem ${qIdx + 1} Fully Completed!`);
        }
        renderPalettes();
        loadQuestion(qIdx);
        renderSolutions();
      } else {
        AudioEngine.incorrect();
        stepAttempts[key] = (stepAttempts[key] || 0) + 1;
        inputEl.style.borderColor = "var(--red-fail)";
        
        if (stepAttempts[key] >= 2) {
          showToast(`Hint: 2 attempts reached. The correct answer is '${CHAPTER_QUESTIONS[qIdx].steps[sIdx].expected}'. Click Auto-Fill to continue.`);
        } else {
          showToast("Incorrect answer. Check your trigonometric substitution and try again!");
        }
        loadQuestion(qIdx);
      }
    }

    function renderSolutions() {
      const container = document.getElementById('completeSolutionsContainer');
      let completedCount = stepProgress.filter(p => p.status === "completed").length;
      document.getElementById('scoreValue').innerText = `${completedCount} / ${CHAPTER_QUESTIONS.length}`;

      let html = '';
      let lastConcept = '';

      CHAPTER_QUESTIONS.forEach((q) => {
        if (q.concept !== lastConcept) {
          lastConcept = q.concept;
          const sectionHeader = q.concept === 'single' 
            ? 'Section A: Single Right Triangle Configurations'
            : 'Section B: Two Coupled Triangles & Elevation/Depression Problems';
          html += `<h2 style="color:var(--navy-dark); margin: 30px 0 14px 0; border-bottom: 2px solid var(--border-soft); padding-bottom: 6px;">${sectionHeader}</h2>`;
        }

        html += `
          <div class="theory-card">
            <span class="concept-tag ${q.concept}">${q.concept.toUpperCase()}</span>
            <span style="font-size:0.8rem; font-weight:bold; color:var(--text-muted); margin-left:6px;">${q.source}</span>
            <h3 style="margin-top:6px;">Problem ${q.id}: ${q.title}</h3>
            <p>${q.prompt}</p>
            <div class="svg-container" style="max-width: 240px; margin: 12px 0;">${q.svg}</div>
            <div class="diagram-objective-card">
              <strong>📐 Diagram Guide:</strong> ${q.diagramObjective}
            </div>
            <div class="proof-section">
              ${q.steps.map((st, sIdx) => `
                <div class="proof-block">
                  <strong>Step ${sIdx + 1}:</strong> ${st.prefix} <strong>[ ${st.expected} ]</strong> ${st.suffix}<br/>
                  <div style="margin-top:6px;">${st.explanation}</div>
                </div>
              `).join('')}
            </div>
          </div>
        `;
      });
      container.innerHTML = html;
      if (window.MathJax && window.MathJax.typesetPromise) {
        MathJax.typesetPromise();
      }
    }

    function toggleTool(tool) {
      if (tool === 'keypad') {
        document.getElementById('toolKeypad').style.display = 'block';
        document.getElementById('toolCalc').style.display = 'none';
        document.getElementById('tabKeypadBtn').classList.add('active');
        document.getElementById('tabCalcBtn').classList.remove('active');
      } else {
        document.getElementById('toolKeypad').style.display = 'none';
        document.getElementById('toolCalc').style.display = 'block';
        document.getElementById('tabCalcBtn').classList.add('active');
        document.getElementById('tabKeypadBtn').classList.remove('active');
      }
    }

    function insertSymbol(sym) {
      if (activeInputRef) {
        activeInputRef.value += sym;
        activeInputRef.focus();
      }
    }

    function pressCalc(val) {
      document.getElementById('calcDisplay').value += val;
    }

    function calcClear() {
      document.getElementById('calcDisplay').value = '';
    }

    function calcEval() {
      try {
        const res = eval(document.getElementById('calcDisplay').value);
        document.getElementById('calcDisplay').value = res;
      } catch (e) {
        document.getElementById('calcDisplay').value = 'Error';
      }
    }

    function calcSqrt() {
      try {
        const val = parseFloat(document.getElementById('calcDisplay').value);
        document.getElementById('calcDisplay').value = Math.sqrt(val);
      } catch (e) {
        document.getElementById('calcDisplay').value = 'Error';
      }
    }

    document.getElementById('audioToggleBtn').onclick = () => {
      audioMuted = !audioMuted;
      document.getElementById('audioToggleBtn').innerText = audioMuted ? '🔇' : '🔊';
    };
  </script>
</body>
</html>

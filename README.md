<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="KW Tech Solution LTD provides software development, cloud infrastructure, platform integration, and technical consulting services for digital platforms." />
  <title>KW Tech Solution LTD</title>
  <style>
    :root {
      --bg: #0b1220;
      --bg-soft: #111a2e;
      --card: #151f35;
      --text: #f5f7fb;
      --muted: #aeb9cc;
      --line: rgba(255,255,255,0.12);
      --green: #2ee67f;
      --green-2: #85f28d;
      --blue: #4da3ff;
      --shadow: 0 20px 60px rgba(0,0,0,0.35);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      background: radial-gradient(circle at top left, rgba(46,230,127,0.18), transparent 32%),
                  radial-gradient(circle at top right, rgba(77,163,255,0.16), transparent 28%),
                  var(--bg);
      color: var(--text);
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .container {
      width: min(1120px, calc(100% - 40px));
      margin: 0 auto;
    }

    header {
      position: sticky;
      top: 0;
      z-index: 20;
      backdrop-filter: blur(18px);
      background: rgba(11,18,32,0.72);
      border-bottom: 1px solid var(--line);
    }

    .nav {
      height: 76px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 24px;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 12px;
      font-weight: 800;
      letter-spacing: -0.04em;
      font-size: 22px;
    }

    .logo {
      width: 38px;
      height: 38px;
      border-radius: 12px;
      background: linear-gradient(135deg, var(--green), var(--green-2));
      display: grid;
      place-items: center;
      color: #07110b;
      font-weight: 900;
      box-shadow: 0 10px 30px rgba(46,230,127,0.25);
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 24px;
      color: var(--muted);
      font-size: 14px;
      font-weight: 600;
    }

    .nav-links a:hover {
      color: var(--text);
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      border-radius: 999px;
      padding: 13px 22px;
      font-weight: 800;
      border: 1px solid transparent;
      transition: transform 0.2s ease, border-color 0.2s ease, background 0.2s ease;
    }

    .btn:hover {
      transform: translateY(-2px);
    }

    .btn-primary {
      background: linear-gradient(135deg, var(--green), var(--green-2));
      color: #07110b;
      box-shadow: 0 16px 40px rgba(46,230,127,0.22);
    }

    .btn-secondary {
      border-color: var(--line);
      color: var(--text);
      background: rgba(255,255,255,0.04);
    }

    .hero {
      padding: 92px 0 70px;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.1fr 0.9fr;
      gap: 46px;
      align-items: center;
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      color: var(--green-2);
      background: rgba(46,230,127,0.1);
      border: 1px solid rgba(46,230,127,0.22);
      padding: 9px 14px;
      border-radius: 999px;
      font-size: 13px;
      font-weight: 800;
      margin-bottom: 22px;
    }

    .hero h1 {
      font-size: clamp(42px, 7vw, 76px);
      line-height: 0.98;
      letter-spacing: -0.07em;
      margin-bottom: 24px;
    }

    .hero p {
      font-size: 18px;
      color: var(--muted);
      max-width: 650px;
      margin-bottom: 32px;
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 14px;
      margin-bottom: 32px;
    }

    .trust-row {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      color: var(--muted);
      font-size: 14px;
    }

    .chip {
      border: 1px solid var(--line);
      background: rgba(255,255,255,0.04);
      padding: 9px 12px;
      border-radius: 999px;
    }

    .hero-card {
      background: linear-gradient(180deg, rgba(255,255,255,0.08), rgba(255,255,255,0.03));
      border: 1px solid var(--line);
      border-radius: 30px;
      padding: 28px;
      box-shadow: var(--shadow);
      position: relative;
      overflow: hidden;
    }

    .hero-card::before {
      content: "";
      position: absolute;
      width: 220px;
      height: 220px;
      right: -80px;
      top: -80px;
      background: rgba(46,230,127,0.2);
      filter: blur(8px);
      border-radius: 999px;
    }

    .metric-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 14px;
      position: relative;
      z-index: 1;
    }

    .metric {
      background: rgba(11,18,32,0.76);
      border: 1px solid var(--line);
      border-radius: 20px;
      padding: 18px;
    }

    .metric strong {
      display: block;
      font-size: 28px;
      letter-spacing: -0.04em;
      margin-bottom: 4px;
    }

    .metric span {
      color: var(--muted);
      font-size: 13px;
      font-weight: 700;
    }

    section {
      padding: 72px 0;
    }

    .section-title {
      max-width: 720px;
      margin-bottom: 34px;
    }

    .section-title h2 {
      font-size: clamp(32px, 5vw, 48px);
      letter-spacing: -0.055em;
      line-height: 1.05;
      margin-bottom: 14px;
    }

    .section-title p {
      color: var(--muted);
      font-size: 17px;
    }

    .cards {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
    }

    .card {
      background: rgba(255,255,255,0.045);
      border: 1px solid var(--line);
      border-radius: 26px;
      padding: 24px;
      min-height: 230px;
    }

    .card-icon {
      width: 46px;
      height: 46px;
      border-radius: 16px;
      display: grid;
      place-items: center;
      background: rgba(46,230,127,0.12);
      color: var(--green-2);
      font-size: 22px;
      margin-bottom: 18px;
    }

    .card h3 {
      font-size: 20px;
      margin-bottom: 10px;
      letter-spacing: -0.03em;
    }

    .card p {
      color: var(--muted);
      font-size: 15px;
    }

    .process {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 16px;
    }

    .step {
      border-left: 2px solid rgba(46,230,127,0.55);
      padding: 4px 0 4px 18px;
    }

    .step span {
      color: var(--green-2);
      font-weight: 900;
      font-size: 13px;
    }

    .step h3 {
      margin: 8px 0;
      font-size: 18px;
    }

    .step p {
      color: var(--muted);
      font-size: 14px;
    }

    .contact-box {
      background: linear-gradient(135deg, rgba(46,230,127,0.16), rgba(77,163,255,0.12));
      border: 1px solid var(--line);
      border-radius: 32px;
      padding: 36px;
      display: grid;
      grid-template-columns: 1fr auto;
      gap: 24px;
      align-items: center;
      box-shadow: var(--shadow);
    }

    .contact-box h2 {
      font-size: clamp(30px, 5vw, 44px);
      letter-spacing: -0.055em;
      margin-bottom: 10px;
    }

    .contact-box p {
      color: var(--muted);
    }

    footer {
      padding: 34px 0;
      border-top: 1px solid var(--line);
      color: var(--muted);
      font-size: 14px;
    }

    .footer-row {
      display: flex;
      justify-content: space-between;
      gap: 18px;
      flex-wrap: wrap;
    }

    .footer-links {
      display: flex;
      gap: 18px;
    }

    @media (max-width: 900px) {
      .hero-grid,
      .contact-box {
        grid-template-columns: 1fr;
      }

      .cards,
      .process {
        grid-template-columns: 1fr 1fr;
      }

      .nav-links {
        display: none;
      }
    }

    @media (max-width: 560px) {
      .container {
        width: min(100% - 28px, 1120px);
      }

      .hero {
        padding-top: 64px;
      }

      .cards,
      .process,
      .metric-grid {
        grid-template-columns: 1fr;
      }

      .contact-box {
        padding: 26px;
      }
    }
  </style>
</head>
<body>
  <header>
    <div class="container nav">
      <a href="#" class="brand" aria-label="KW Tech Solution Home">
        <span class="logo">KW</span>
        <span>KW Tech Solution</span>
      </a>
      <nav class="nav-links" aria-label="Main navigation">
        <a href="#about">About</a>
        <a href="#services">Services</a>
        <a href="#process">Process</a>
        <a href="#contact">Contact</a>
      </nav>
    </div>
  </header>

  <main>
    <section class="hero">
      <div class="container hero-grid">
        <div>
          <div class="eyebrow">Software • Cloud • Platform Integration</div>
          <h1>Technology solutions for modern digital platforms.</h1>
          <p>
            KW Tech Solution LTD provides software development, cloud infrastructure support,
            system integration, and technical consulting for scalable digital products.
          </p>
          <div class="hero-actions">
            <a href="#contact" class="btn btn-primary">Contact Us</a>
            <a href="#services" class="btn btn-secondary">View Services</a>
          </div>
          <div class="trust-row">
            <span class="chip">Backend Systems</span>
            <span class="chip">Cloud Deployment</span>
            <span class="chip">API Integration</span>
            <span class="chip">Technical Consulting</span>
          </div>
        </div>

        <div class="hero-card" aria-label="Company capabilities summary">
          <div class="metric-grid">
            <div class="metric">
              <strong>24/7</strong>
              <span>Operational mindset</span>
            </div>
            <div class="metric">
              <strong>API</strong>
              <span>Integration ready</span>
            </div>
            <div class="metric">
              <strong>Cloud</strong>
              <span>Scalable infrastructure</span>
            </div>
            <div class="metric">
              <strong>Secure</strong>
              <span>Production-first delivery</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="about">
      <div class="container">
        <div class="section-title">
          <h2>Built for companies that need reliable technical execution.</h2>
          <p>
            We help businesses design, build, and maintain digital systems with a focus on
            performance, security, maintainability, and operational reliability.
          </p>
        </div>
      </div>
    </section>

    <section id="services">
      <div class="container">
        <div class="section-title">
          <h2>Services</h2>
          <p>Practical technology services for product teams, startups, and digital operators.</p>
        </div>
        <div class="cards">
          <article class="card">
            <div class="card-icon">⚙️</div>
            <h3>Software Development</h3>
            <p>Frontend, backend, admin portals, API services, automation tools, and internal platforms.</p>
          </article>
          <article class="card">
            <div class="card-icon">☁️</div>
            <h3>Cloud Infrastructure</h3>
            <p>Cloud deployment, DNS, CDN, SSL, monitoring, environment setup, and production support.</p>
          </article>
          <article class="card">
            <div class="card-icon">🔗</div>
            <h3>System Integration</h3>
            <p>Third-party API integration, payment flow support, webhook handling, and data synchronization.</p>
          </article>
          <article class="card">
            <div class="card-icon">📊</div>
            <h3>Data & Reporting</h3>
            <p>Operational dashboards, reporting workflows, summary data pipelines, and performance optimization.</p>
          </article>
          <article class="card">
            <div class="card-icon">🛡️</div>
            <h3>Security & Reliability</h3>
            <p>Access control, audit logs, environment hardening, incident support, and reliability planning.</p>
          </article>
          <article class="card">
            <div class="card-icon">🧭</div>
            <h3>Technical Consulting</h3>
            <p>Architecture review, vendor coordination, project planning, technical documentation, and delivery strategy.</p>
          </article>
        </div>
      </div>
    </section>

    <section id="process">
      <div class="container">
        <div class="section-title">
          <h2>How we work</h2>
          <p>A clear delivery process from requirement clarification to production readiness.</p>
        </div>
        <div class="process">
          <div class="step">
            <span>01</span>
            <h3>Understand</h3>
            <p>Clarify goals, constraints, workflows, risks, and success metrics.</p>
          </div>
          <div class="step">
            <span>02</span>
            <h3>Design</h3>
            <p>Prepare practical architecture, data flow, API design, and implementation plan.</p>
          </div>
          <div class="step">
            <span>03</span>
            <h3>Build</h3>
            <p>Develop, integrate, test, and validate with clear version control.</p>
          </div>
          <div class="step">
            <span>04</span>
            <h3>Operate</h3>
            <p>Deploy, monitor, optimize, and support production systems.</p>
          </div>
        </div>
      </div>
    </section>

    <section id="contact">
      <div class="container">
        <div class="contact-box">
          <div>
            <h2>Let’s build something reliable.</h2>
            <p>For business enquiries, technical collaboration, or project discussion, contact our team.</p>
          </div>
          <a href="mailto:contact@kwtechsolution.com" class="btn btn-primary">contact@kwtechsolution.com</a>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container footer-row">
      <div>© <span id="year"></span> KW Tech Solution LTD. All rights reserved.</div>
      <div class="footer-links">
        <a href="#">Privacy Policy</a>
        <a href="#">Terms</a>
      </div>
    </div>
  </footer>

  <script>
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>

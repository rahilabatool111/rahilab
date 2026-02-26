index.html
Portfolio
file:///Users/rahilabatool/Downloads/index.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Rahila Batool | Operations & Risk Analyst</title>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@300;400;600;700&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --navy: #0f1e2e;
      --navy-mid: #162436;
      --gold: #c9a84c;
      --gold-light: #e8c97a;
      --cream: #f5f0e8;
      --text: #1a1a2e;
      --muted: #6b7280;
      --border: #e2d9c8;
    }

    html { scroll-behavior: smooth; }

    body {
      font-family: 'DM Sans', sans-serif;
      background: var(--cream);
      color: var(--text);
      line-height: 1.7;
    }

    /* ── HEADER ── */
    header {
      background: var(--navy);
      color: white;
      padding: 70px 40px 50px;
      position: relative;
      overflow: hidden;
    }

    header::before {
      content: '';
      position: absolute;
      top: -60px; right: -60px;
      width: 320px; height: 320px;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(201,168,76,0.15), transparent 70%);
    }

    header::after {
      content: '';
      position: absolute;
      bottom: 0; left: 0; right: 0;
      height: 3px;
      background: linear-gradient(90deg, var(--gold), transparent);
    }

    .header-inner {
      max-width: 860px;
      margin: 0 auto;
      position: relative;
      z-index: 1;
      opacity: 0;
      animation: fadeUp 0.8s ease forwards;
    }

    .header-inner h1 {
      font-family: 'Cormorant Garamond', serif;
      font-size: clamp(2.6rem, 6vw, 4rem);
      font-weight: 700;
      letter-spacing: 0.02em;
      line-height: 1.1;
      margin-bottom: 8px;
    }

    .title-tag {
      font-size: 0.78rem;
      font-weight: 500;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      color: var(--gold);
      margin-bottom: 22px;
    }

    .contact-row {
      display: flex;
      flex-wrap: wrap;
      gap: 18px;
      margin-top: 18px;
    }

    .contact-row a, .contact-row span {
      color: rgba(255,255,255,0.75);
      font-size: 0.88rem;
      text-decoration: none;
      display: flex;
      align-items: center;
      gap: 6px;
      transition: color 0.2s;
    }

    .contact-row a:hover { color: var(--gold-light); }

    .contact-row svg { width: 14px; height: 14px; fill: var(--gold); flex-shrink: 0; }

    /* ── LAYOUT ── */
    .page {
      max-width: 860px;
      margin: 0 auto;
      padding: 48px 24px 80px;
      display: grid;
      grid-template-columns: 1fr 280px;
      gap: 48px;
      align-items: start;
    }

    /* ── SECTIONS ── */
    section {
      margin-bottom: 44px;
      opacity: 0;
      animation: fadeUp 0.7s ease forwards;
    }

    section:nth-child(1) { animation-delay: 0.1s; }
    section:nth-child(2) { animation-delay: 0.2s; }
    section:nth-child(3) { animation-delay: 0.3s; }
    section:nth-child(4) { animation-delay: 0.4s; }
    section:nth-child(5) { animation-delay: 0.5s; }

    .section-title {
      font-family: 'Cormorant Garamond', serif;
      font-size: 1.25rem;
      font-weight: 600;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      color: var(--navy);
      padding-bottom: 10px;
      border-bottom: 2px solid var(--gold);
      margin-bottom: 24px;
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .section-title svg { width: 16px; height: 16px; fill: var(--gold); }

    /* ── SUMMARY ── */
    .summary p {
      font-size: 0.95rem;
      color: #374151;
      line-height: 1.8;
    }

    /* ── EXPERIENCE ── */
    .job { margin-bottom: 30px; }

    .job-header {
      display: flex;
      justify-content: space-between;
      align-items: baseline;
      flex-wrap: wrap;
      gap: 4px;
      margin-bottom: 2px;
    }

    .job-company {
      font-weight: 600;
      font-size: 1rem;
      color: var(--navy);
    }

    .job-date {
      font-size: 0.78rem;
      color: var(--gold);
      font-weight: 500;
      letter-spacing: 0.05em;
      white-space: nowrap;
    }

    .job-role {
      font-size: 0.85rem;
      color: var(--muted);
      font-style: italic;
      margin-bottom: 10px;
    }

    .job ul {
      padding-left: 16px;
      list-style: none;
    }

    .job ul li {
      font-size: 0.88rem;
      color: #4b5563;
      margin-bottom: 6px;
      padding-left: 14px;
      position: relative;
    }

    .job ul li::before {
      content: '›';
      position: absolute;
      left: 0;
      color: var(--gold);
      font-weight: 700;
    }

    /* ── PROJECTS ── */
    .project-card {
      background: white;
      border: 1px solid var(--border);
      border-left: 3px solid var(--gold);
      border-radius: 6px;
      padding: 16px 18px;
      margin-bottom: 14px;
      transition: box-shadow 0.2s;
    }

    .project-card:hover { box-shadow: 0 4px 16px rgba(0,0,0,0.07); }

    .project-card h4 {
      font-weight: 600;
      font-size: 0.95rem;
      color: var(--navy);
      margin-bottom: 4px;
    }

    .project-card p {
      font-size: 0.85rem;
      color: var(--muted);
    }

    .placeholder-tag {
      display: inline-block;
      background: #fef3c7;
      color: #92400e;
      font-size: 0.72rem;
      padding: 2px 8px;
      border-radius: 20px;
      margin-bottom: 8px;
      font-weight: 500;
    }

    /* ── SIDEBAR ── */
    .sidebar section { margin-bottom: 36px; }

    /* ── SKILLS ── */
    .skill-group { margin-bottom: 16px; }

    .skill-group-label {
      font-size: 0.75rem;
      font-weight: 600;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      color: var(--navy);
      margin-bottom: 8px;
    }

    .skill-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 6px;
    }

    .skill-tag {
      background: white;
      border: 1px solid var(--border);
      border-radius: 4px;
      padding: 4px 10px;
      font-size: 0.78rem;
      color: #374151;
      transition: all 0.2s;
    }

    .skill-tag:hover {
      border-color: var(--gold);
      color: var(--navy);
    }

    /* ── EDUCATION ── */
    .edu-item { margin-bottom: 18px; }

    .edu-item h4 {
      font-weight: 600;
      font-size: 0.9rem;
      color: var(--navy);
    }

    .edu-item p {
      font-size: 0.82rem;
      color: var(--muted);
    }

    /* ── CERT / LANG / VOLUNTEER ── */
    .list-item {
      display: flex;
      align-items: flex-start;
      gap: 10px;
      margin-bottom: 12px;
      font-size: 0.86rem;
      color: #374151;
    }

    .list-item::before {
      content: '◆';
      color: var(--gold);
      font-size: 0.5rem;
      margin-top: 6px;
      flex-shrink: 0;
    }

    .list-item strong { display: block; color: var(--navy); font-size: 0.88rem; }
    .list-item span { font-size: 0.8rem; color: var(--muted); }

    /* ── EXTRAS ── */
    .activity-item {
      margin-bottom: 12px;
      font-size: 0.86rem;
    }

    .activity-item strong { color: var(--navy); display: block; }
    .activity-item span { color: var(--muted); font-size: 0.8rem; }

    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(18px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    @media (max-width: 680px) {
      .page { grid-template-columns: 1fr; gap: 0; }
      header { padding: 50px 24px 40px; }
    }
  </style>
</head>
<body>

<!-- ── HEADER ── -->
<header>
  <div class="header-inner">
    <p class="title-tag">Operations &amp; Risk Analyst · Finance &amp; Cybersecurity</p>
    <h1>Rahila Batool</h1>
    <div class="contact-row">
      <span>
        <svg viewBox="0 0 24 24"><path d="M6.6 10.8c1.4 2.8 3.8 5.1 6.6 6.6l2.2-2.2c.3-.3.7-.4 1-.2 1.1.4 2.3.6 3.6.6.6 0 1 .4 1 1V20c0 .6-.4 1-1 1-9.4 0-17-7.6-17-17 0-.6.4-1 1-1h3.5c.6 0 1 .4 1 1 0 1.3.2 2.5.6 3.6.1.3 0 .7-.2 1L6.6 10.8z"/></svg>
        (385) 465-4082
      </span>
      <a href="mailto:rahilabatool03@gmail.com">
        <svg viewBox="0 0 24 24"><path d="M20 4H4c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/></svg>
        rahilabatool03@gmail.com
      </a>
      <span>
        <svg viewBox="0 0 24 24"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"/></svg>
        Salt Lake City, UT
      </span>
      <a href="https://www.linkedin.com/in/rahila-batool-b470381aa" target="_blank">
        <svg viewBox="0 0 24 24"><path d="M19 3a2 2 0 012 2v14a2 2 0 01-2 2H5a2 2 0 01-2-2V5a2 2 0 012-2h14m-.5 15.5v-5.3a3.26 3.26 0 00-3.26-3.26c-.85 0-1.84.52-2.32 1.3v-1.11h-2.79v8.37h2.79v-4.93c0-.77.62-1.4 1.39-1.4a1.4 1.4 0 011.4 1.4v4.93h2.79M6.88 8.56a1.68 1.68 0 001.68-1.68c0-.93-.75-1.69-1.68-1.69a1.69 1.69 0 00-1.69 1.69c0 .93.76 1.68 1.69 1.68m1.39 9.94v-8.37H5.5v8.37h2.77z"/></svg>
        LinkedIn
      </a>
    </div>
  </div>
</header>

<!-- ── MAIN CONTENT ── -->
<div class="page">

  <!-- LEFT COLUMN -->
  <main>

    <!-- Summary -->
    <section class="summary">
      <h2 class="section-title">
        <svg viewBox="0 0 24 24"><path d="M12 2a10 10 0 110 20A10 10 0 0112 2zm0 2a8 8 0 100 16A8 8 0 0012 4zm0 3a1 1 0 011 1v4l3 1.5-.9 1.8L12 13.5V8a1 1 0 00-1-1z"/></svg>
        Profile
      </h2>
      <p>Operations and Risk Analyst with experience supporting large financial institutions including Wells Fargo and Morgan Stanley. Background spans financial operations, account maintenance, data integrity, and regulatory controls within highly regulated environments. Holds a Bachelor's degree in Cybersecurity with applied knowledge of risk management, access controls, and data protection. Actively leveraging SQL and advanced Excel to support analytics, risk, and technology-focused roles across finance and cybersecurity.</p>
    </section>

    <!-- Experience -->
    <section>
      <h2 class="section-title">
        <svg viewBox="0 0 24 24"><path d="M20 6h-2.18c.07-.44.18-.88.18-1a3 3 0 00-6 0c0 .12.11.56.18 1H10c0-.12.07-.56.07-1a5 5 0 0110 0c0 .44-.11.88-.07 1zM4 8h16v12H4V8zm2 2v8h12v-8H6zm2 2h8v1H8v-1zm0 3h5v1H8v-1z"/></svg>
        Professional Experience
      </h2>

      <div class="job">
        <div class="job-header">
          <span class="job-company">Wells Fargo</span>
          <span class="job-date">SEP 2025 – Present</span>
        </div>
        <p class="job-role">Securities Operations Associate</p>
        <ul>
          <li>Maintain and update client/account data within enterprise financial systems, ensuring accuracy, access controls, and regulatory compliance</li>
          <li>Perform quality checks, exception resolution, and reconciliation to support operational risk and audit readiness</li>
          <li>Apply Excel (XLOOKUP, PivotTables, formulas) to validate data and support reporting workflows</li>
        </ul>
      </div>

      <div class="job">
        <div class="job-header">
          <span class="job-company">Morgan Stanley</span>
          <span class="job-date">Aug 2024 – Aug 2025</span>
        </div>
        <p class="job-role">Client Relationship Manager</p>
        <ul>
          <li>Supported account servicing and operational processing within a highly regulated financial environment</li>
          <li>Ensured data integrity, documentation accuracy, and compliance with internal controls and risk standards</li>
          <li>Collaborated cross-functionally to resolve issues and support timely processing</li>
        </ul>
      </div>

      <div class="job">
        <div class="job-header">
          <span class="job-company">Fastenal</span>
          <span class="job-date">Jul 2023 – Aug 2024</span>
        </div>
        <p class="job-role">Project Coordinator</p>
        <ul>
          <li>Supported compliance documentation, risk tracking, and audit-ready project records</li>
          <li>Assisted with budget monitoring, variance tracking, and governance support</li>
        </ul>
      </div>
    </section>

    <!-- Projects -->
    <section>
      <h2 class="section-title">
        <svg viewBox="0 0 24 24"><path d="M3 3h18v18H3V3zm2 2v14h14V5H5zm2 2h10v2H7V7zm0 4h10v2H7v-2zm0 4h7v2H7v-2z"/></svg>
        Projects
      </h2>
      <div class="project-card">
        <span class="placeholder-tag">✏️ Add your project</span>
        <h4>Project Name</h4>
        <p>Brief description of what you built or contributed to, the tools used, and the outcome or impact.</p>
      </div>
      <div class="project-card">
        <span class="placeholder-tag">✏️ Add your project</span>
        <h4>Project Name</h4>
        <p>Brief description of what you built or contributed to, the tools used, and the outcome or impact.</p>
      </div>
    </section>

    <!-- Volunteer -->
    <section>
      <h2 class="section-title">
        <svg viewBox="0 0 24 24"><path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>
        Volunteer Work
      </h2>
      <div class="list-item">
        <div>
          <strong>Organization Name</strong>
          <span>Role · Dates — <em style="color:#b45309">Replace with your volunteer experience</em></span>
        </div>
      </div>
    </section>

  </main>

  <!-- RIGHT SIDEBAR -->
  <aside class="sidebar">

    <!-- Skills -->
    <section>
      <h2 class="section-title">Skills</h2>
      <div class="skill-group">
        <p class="skill-group-label">Finance & Risk</p>
        <div class="skill-tags">
          <span class="skill-tag">Financial Operations</span>
          <span class="skill-tag">Risk & Controls</span>
          <span class="skill-tag">Audit Readiness</span>
          <span class="skill-tag">Compliance</span>
          <span class="skill-tag">Reconciliation</span>
          <span class="skill-tag">Data Integrity</span>
        </div>
      </div>
      <div class="skill-group">
        <p class="skill-group-label">Cybersecurity</p>
        <div class="skill-tags">
          <span class="skill-tag">Access Controls</span>
          <span class="skill-tag">Data Protection</span>
          <span class="skill-tag">Risk Management</span>
        </div>
      </div>
      <div class="skill-group">
        <p class="skill-group-label">Technical</p>
        <div class="skill-tags">
          <span class="skill-tag">SQL</span>
          <span class="skill-tag">Excel (Advanced)</span>
          <span class="skill-tag">XLOOKUP</span>
          <span class="skill-tag">PivotTables</span>
        </div>
      </div>
    </section>

    <!-- Education -->
    <section>
      <h2 class="section-title">Education</h2>
      <div class="edu-item">
        <h4>B.S. Cybersecurity</h4>
        <p>Major: Cybersecurity & Finance</p>
        <p>University of Phoenix</p>
      </div>
    </section>

    <!-- Certifications -->
    <section>
      <h2 class="section-title">Certifications</h2>
      <div class="list-item">
        <div>
          <strong>Graduate Project Management</strong>
          <span>PMI Group</span>
        </div>
      </div>
      <div class="list-item">
        <div>
          <strong style="color:#b45309">✏️ Add certification</strong>
          <span>Issuing organization · Year</span>
        </div>
      </div>
    </section>

    <!-- Languages -->
    <section>
      <h2 class="section-title">Languages</h2>
      <div class="list-item">
        <div>
          <strong style="color:#b45309">✏️ Add a language</strong>
          <span>e.g. English · Fluent</span>
        </div>
      </div>
    </section>

    <!-- Extracurricular -->
    <section>
      <h2 class="section-title">Activities</h2>
      <div class="activity-item">
        <strong>PMI Northern UT</strong>
        <span>Director of Newsletter</span>
      </div>
      <div class="activity-item">
        <strong>Morgan Stanley</strong>
        <span>Employee Group Ambassador</span>
      </div>
    </section>

  </aside>
</div>

</body>
</html>


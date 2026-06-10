# Portofolio
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Hendro Cahyo Ramadhan — Data Analyst Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Mono:wght@300;400;500&family=Syne:wght@400;600;700;800&display=swap" rel="stylesheet" />
<style>
  :root {
    --ink: #0d0d0d;
    --cream: #f5f1eb;
    --gold: #c9a84c;
    --gold-light: #e8d5a3;
    --teal: #1a6b6b;
    --teal-light: #e6f4f1;
    --rust: #b5451b;
    --mid: #6b6560;
    --border: #d9d3c9;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Mono', monospace;
    background: var(--cream);
    color: var(--ink);
    font-size: 14px;
    line-height: 1.7;
  }

  /* ── HEADER / HERO ── */
  header {
    background: var(--ink);
    color: var(--cream);
    padding: 80px 60px 60px;
    position: relative;
    overflow: hidden;
  }
  header::before {
    content: '';
    position: absolute;
    top: -80px; right: -80px;
    width: 400px; height: 400px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(201,168,76,0.18) 0%, transparent 70%);
    pointer-events: none;
  }
  header::after {
    content: 'DATA';
    position: absolute;
    bottom: -30px; right: 40px;
    font-family: 'DM Serif Display', serif;
    font-size: 160px;
    color: rgba(255,255,255,0.04);
    letter-spacing: -8px;
    pointer-events: none;
    user-select: none;
  }

  .badge {
    display: inline-block;
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    font-weight: 500;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--gold);
    border: 1px solid var(--gold);
    padding: 4px 12px;
    border-radius: 2px;
    margin-bottom: 24px;
  }

  h1 {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(42px, 6vw, 72px);
    line-height: 1.05;
    letter-spacing: -1px;
    margin-bottom: 8px;
    color: #fff;
  }

  .subtitle {
    font-family: 'Syne', sans-serif;
    font-weight: 600;
    font-size: 14px;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--gold-light);
    margin-bottom: 28px;
  }

  .header-desc {
    max-width: 560px;
    color: rgba(245,241,235,0.75);
    font-size: 13.5px;
    line-height: 1.8;
    margin-bottom: 40px;
  }

  .contact-row {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    align-items: center;
  }

  .contact-item {
    display: flex;
    align-items: center;
    gap: 8px;
    font-size: 12.5px;
    color: rgba(245,241,235,0.8);
    text-decoration: none;
    transition: color 0.2s;
  }
  .contact-item:hover { color: var(--gold); }
  .contact-item .dot {
    width: 6px; height: 6px;
    border-radius: 50%;
    background: var(--gold);
    flex-shrink: 0;
  }

  /* ── LAYOUT ── */
  .container {
    max-width: 1000px;
    margin: 0 auto;
    padding: 0 40px;
  }

  section {
    padding: 60px 0;
    border-bottom: 1px solid var(--border);
  }
  section:last-child { border-bottom: none; }

  .section-label {
    font-family: 'Syne', sans-serif;
    font-weight: 700;
    font-size: 11px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--teal);
    margin-bottom: 6px;
  }

  .section-title {
    font-family: 'DM Serif Display', serif;
    font-size: 32px;
    color: var(--ink);
    margin-bottom: 32px;
    line-height: 1.2;
  }

  /* ── SKILLS GRID ── */
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 16px;
  }

  .skill-card {
    background: #fff;
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 20px;
    position: relative;
    transition: border-color 0.2s, box-shadow 0.2s;
  }
  .skill-card:hover {
    border-color: var(--teal);
    box-shadow: 0 4px 20px rgba(26,107,107,0.1);
  }

  .skill-category {
    font-family: 'Syne', sans-serif;
    font-weight: 700;
    font-size: 11px;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--teal);
    margin-bottom: 10px;
  }

  .skill-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
  }

  .tag {
    background: var(--cream);
    border: 1px solid var(--border);
    border-radius: 2px;
    padding: 3px 8px;
    font-size: 11.5px;
    font-family: 'DM Mono', monospace;
    color: var(--ink);
  }

  /* ── PROJECTS ── */
  .project-card {
    background: #fff;
    border: 1px solid var(--border);
    border-radius: 4px;
    overflow: hidden;
    margin-bottom: 24px;
    transition: box-shadow 0.25s;
  }
  .project-card:hover {
    box-shadow: 0 8px 32px rgba(13,13,13,0.1);
  }

  .project-header {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    gap: 20px;
    padding: 28px 28px 0;
  }

  .project-number {
    font-family: 'DM Serif Display', serif;
    font-size: 48px;
    color: var(--gold-light);
    line-height: 1;
    flex-shrink: 0;
  }

  .project-title {
    font-family: 'DM Serif Display', serif;
    font-size: 22px;
    color: var(--ink);
    margin-bottom: 6px;
    line-height: 1.2;
  }

  .project-type {
    font-family: 'Syne', sans-serif;
    font-weight: 600;
    font-size: 10.5px;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--rust);
    margin-bottom: 14px;
  }

  .project-body { padding: 16px 28px 28px; }

  .project-desc {
    color: var(--mid);
    font-size: 13px;
    line-height: 1.75;
    margin-bottom: 20px;
  }

  .project-highlights {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 8px;
    margin-bottom: 20px;
  }
  .project-highlights li {
    display: flex;
    gap: 10px;
    font-size: 13px;
    color: var(--ink);
  }
  .project-highlights li::before {
    content: '→';
    color: var(--teal);
    flex-shrink: 0;
    font-size: 12px;
    margin-top: 1px;
  }

  .project-tech {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
    margin-bottom: 20px;
  }

  .tech-tag {
    background: var(--teal-light);
    color: var(--teal);
    border-radius: 2px;
    padding: 4px 10px;
    font-size: 11.5px;
    font-family: 'DM Mono', monospace;
    font-weight: 500;
  }

  .project-link {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    color: var(--teal);
    font-size: 12px;
    font-family: 'Syne', sans-serif;
    font-weight: 700;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    text-decoration: none;
    border-bottom: 1px solid var(--teal);
    padding-bottom: 1px;
    transition: opacity 0.2s;
  }
  .project-link:hover { opacity: 0.7; }

  /* ── KPI STRIP ── */
  .kpi-strip {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
    gap: 1px;
    background: var(--border);
    border: 1px solid var(--border);
    border-radius: 4px;
    overflow: hidden;
    margin-bottom: 24px;
  }

  .kpi-item {
    background: #fff;
    padding: 20px;
    text-align: center;
  }

  .kpi-value {
    font-family: 'DM Serif Display', serif;
    font-size: 26px;
    color: var(--teal);
    display: block;
    margin-bottom: 4px;
  }

  .kpi-label {
    font-size: 10.5px;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--mid);
    font-family: 'Syne', sans-serif;
    font-weight: 600;
  }

  /* ── ABOUT / SUMMARY ── */
  .summary-box {
    background: var(--ink);
    color: var(--cream);
    border-radius: 4px;
    padding: 40px 44px;
    position: relative;
    overflow: hidden;
  }
  .summary-box::before {
    content: '"';
    position: absolute;
    top: -10px; left: 20px;
    font-family: 'DM Serif Display', serif;
    font-size: 120px;
    color: rgba(201,168,76,0.15);
    line-height: 1;
    pointer-events: none;
  }
  .summary-box p {
    font-size: 15px;
    line-height: 1.9;
    color: rgba(245,241,235,0.88);
    position: relative;
    z-index: 1;
  }

  /* ── EXPERIENCE / EDUCATION TIMELINE ── */
  .timeline { position: relative; }
  .timeline::before {
    content: '';
    position: absolute;
    left: 8px; top: 6px; bottom: 0;
    width: 1px;
    background: var(--border);
  }

  .tl-item {
    display: flex;
    gap: 28px;
    margin-bottom: 32px;
    position: relative;
  }

  .tl-dot {
    width: 17px;
    height: 17px;
    border-radius: 50%;
    background: var(--teal);
    border: 3px solid var(--cream);
    outline: 1px solid var(--border);
    flex-shrink: 0;
    margin-top: 4px;
    z-index: 1;
  }

  .tl-content { flex: 1; }

  .tl-date {
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    color: var(--mid);
    margin-bottom: 4px;
    letter-spacing: 0.05em;
  }

  .tl-title {
    font-family: 'Syne', sans-serif;
    font-weight: 700;
    font-size: 15px;
    color: var(--ink);
    margin-bottom: 2px;
  }

  .tl-org {
    font-size: 12.5px;
    color: var(--teal);
    font-family: 'DM Mono', monospace;
    margin-bottom: 8px;
  }

  .tl-desc {
    font-size: 13px;
    color: var(--mid);
    line-height: 1.7;
  }

  /* ── FOOTER ── */
  footer {
    background: var(--ink);
    color: rgba(245,241,235,0.5);
    text-align: center;
    padding: 36px 40px;
    font-size: 12px;
    letter-spacing: 0.05em;
  }
  footer span { color: var(--gold); }

  /* ── PRINT / ATS LAYER ── */
  @media print {
    header::after, header::before { display: none; }
    .summary-box::before { display: none; }
    .project-card, .skill-card { break-inside: avoid; }
    body { font-size: 12px; }
  }

  /* ── RESPONSIVE ── */
  @media (max-width: 640px) {
    header { padding: 50px 24px 40px; }
    .container { padding: 0 20px; }
    .project-header { flex-direction: column; }
    .summary-box { padding: 28px 24px; }
  }

  /* ── ANIMATIONS ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to   { opacity: 1; transform: translateY(0); }
  }
  .anim { animation: fadeUp 0.55s ease both; }
  .anim-d1 { animation-delay: 0.1s; }
  .anim-d2 { animation-delay: 0.22s; }
  .anim-d3 { animation-delay: 0.34s; }
  .anim-d4 { animation-delay: 0.46s; }
</style>
</head>
<body>

<!-- ════════ HERO ════════ -->
<header>
  <div class="badge">Portfolio · Data Analytics</div>
  <h1 class="anim anim-d1">Hendro Cahyo<br>Ramadhan</h1>
  <p class="subtitle anim anim-d2">Data Analyst &amp; Data Engineer</p>
  <p class="header-desc anim anim-d3">
    Results-driven data professional specializing in data warehouse architecture,
    business intelligence reporting, and end-to-end analytics pipelines. Passionate
    about transforming raw data into clear, actionable insights that drive decisions.
  </p>
  <div class="contact-row anim anim-d4">
    <a href="mailto:hendrocr20@gmail.com" class="contact-item">
      <span class="dot"></span>hendrocr20@gmail.com
    </a>
    <a href="https://github.com/HendroCahyoRamadhan" target="_blank" class="contact-item">
      <span class="dot"></span>github.com/HendroCahyoRamadhan
    </a>
    <span class="contact-item">
      <span class="dot"></span>Indonesia
    </span>
  </div>
</header>

<div class="container">

  <!-- ════════ PROFESSIONAL SUMMARY ════════ -->
  <section>
    <p class="section-label">About</p>
    <h2 class="section-title">Professional Summary</h2>
    <div class="summary-box">
      <p>
        Data Analyst with hands-on experience in designing end-to-end data solutions —
        from architecting SQL-based Data Warehouses following industry-standard Medallion Architecture
        (Bronze → Silver → Gold), to delivering interactive Power BI dashboards that surface
        business-critical KPIs. Proficient in T-SQL, DAX, Power Query (M), and star-schema
        data modeling. Demonstrates strong analytical thinking, clear documentation practices,
        and the ability to translate complex datasets into meaningful narratives for both
        technical teams and business stakeholders.
      </p>
    </div>
  </section>

  <!-- ════════ SKILLS ════════ -->
  <section>
    <p class="section-label">Capabilities</p>
    <h2 class="section-title">Technical Skills</h2>
    <div class="skills-grid">
      <div class="skill-card">
        <p class="skill-category">Languages &amp; Query</p>
        <div class="skill-tags">
          <span class="tag">T-SQL</span>
          <span class="tag">SQL Server</span>
          <span class="tag">DAX</span>
          <span class="tag">Power Query (M)</span>
        </div>
      </div>
      <div class="skill-card">
        <p class="skill-category">BI &amp; Visualization</p>
        <div class="skill-tags">
          <span class="tag">Power BI Desktop</span>
          <span class="tag">Interactive Dashboards</span>
          <span class="tag">KPI Design</span>
        </div>
      </div>
      <div class="skill-card">
        <p class="skill-category">Data Engineering</p>
        <div class="skill-tags">
          <span class="tag">ETL Pipelines</span>
          <span class="tag">Medallion Architecture</span>
          <span class="tag">Star Schema</span>
          <span class="tag">Data Modeling</span>
        </div>
      </div>
      <div class="skill-card">
        <p class="skill-category">Tools &amp; Platforms</p>
        <div class="skill-tags">
          <span class="tag">SQL Server Express</span>
          <span class="tag">SSMS</span>
          <span class="tag">DrawIO</span>
          <span class="tag">GitHub</span>
          <span class="tag">Git</span>
        </div>
      </div>
      <div class="skill-card">
        <p class="skill-category">Analytics</p>
        <div class="skill-tags">
          <span class="tag">Revenue Analysis</span>
          <span class="tag">Customer Segmentation</span>
          <span class="tag">Churn & Returns</span>
          <span class="tag">Trend Analysis</span>
        </div>
      </div>
      <div class="skill-card">
        <p class="skill-category">Soft Skills</p>
        <div class="skill-tags">
          <span class="tag">Data Storytelling</span>
          <span class="tag">Documentation</span>
          <span class="tag">Stakeholder Comms</span>
        </div>
      </div>
    </div>
  </section>

  <!-- ════════ PROJECTS ════════ -->
  <section>
    <p class="section-label">Work</p>
    <h2 class="section-title">Featured Projects</h2>

    <!-- PROJECT 1 -->
    <div class="project-card">
      <div class="project-header">
        <div>
          <p class="project-type">Data Engineering · SQL · Data Warehouse</p>
          <h3 class="project-title">Data Warehouse & Analytics Project (SQL)</h3>
        </div>
        <div class="project-number">01</div>
      </div>
      <div class="project-body">
        <p class="project-desc">
          A comprehensive, production-grade Data Warehouse built on SQL Server following
          Medallion Architecture principles. The project consolidates sales data from multiple
          source systems (ERP &amp; CRM) through a structured Bronze → Silver → Gold pipeline,
          enabling reliable analytical reporting and decision support.
        </p>
        <ul class="project-highlights">
          <li>Designed and implemented a three-layer Medallion Architecture (Bronze: raw ingestion, Silver: cleansed &amp; standardized, Gold: star-schema optimized for analytics)</li>
          <li>Built ETL pipelines to extract, transform, and load data from CSV-based ERP and CRM source systems into SQL Server</li>
          <li>Developed fact and dimension tables optimized for analytical queries with clear foreign-key relationships</li>
          <li>Authored comprehensive data model documentation to support both business stakeholders and engineering teams</li>
          <li>Applied data quality checks and cleansing routines prior to Gold layer promotion</li>
        </ul>
        <div class="project-tech">
          <span class="tech-tag">T-SQL</span>
          <span class="tech-tag">SQL Server Express</span>
          <span class="tech-tag">SSMS</span>
          <span class="tech-tag">Medallion Architecture</span>
          <span class="tech-tag">ETL</span>
          <span class="tech-tag">Star Schema</span>
          <span class="tech-tag">DrawIO</span>
        </div>
        <a href="https://github.com/HendroCahyoRamadhan/DataWarehouseProjectSQL" target="_blank" class="project-link">
          View on GitHub ↗
        </a>
      </div>
    </div>

    <!-- PROJECT 2 -->
    <div class="project-card">
      <div class="project-header">
        <div>
          <p class="project-type">Business Intelligence · Power BI · E-Commerce Analytics</p>
          <h3 class="project-title">E-Commerce Analytics Dashboard (Power BI)</h3>
        </div>
        <div class="project-number">02</div>
      </div>
      <div class="project-body">

        <!-- KPI Strip -->
        <div class="kpi-strip">
          <div class="kpi-item">
            <span class="kpi-value">34.18B</span>
            <span class="kpi-label">Total Revenue</span>
          </div>
          <div class="kpi-item">
            <span class="kpi-value">790K+</span>
            <span class="kpi-label">Total Orders</span>
          </div>
          <div class="kpi-item">
            <span class="kpi-value">103K</span>
            <span class="kpi-label">Total Returns</span>
          </div>
          <div class="kpi-item">
            <span class="kpi-value">43.2K</span>
            <span class="kpi-label">Avg Order Value</span>
          </div>
          <div class="kpi-item">
            <span class="kpi-value">13%</span>
            <span class="kpi-label">Return Rate</span>
          </div>
        </div>

        <p class="project-desc">
          A full end-to-end Business Intelligence solution built with Power BI, covering sales performance,
          customer segmentation, return analysis, seller rankings, fulfillment operations, and marketing
          campaign tracking. Transforms raw transactional data into a Gold-layer star schema, then surfaces
          insights through interactive, cross-filterable visualizations.
        </p>
        <ul class="project-highlights">
          <li>Designed a Gold-layer star schema with 3 fact tables (orders, returns, fulfillment) and 6 dimension tables (product, customer, seller, payment, delivery, campaign)</li>
          <li>Wrote 6+ core DAX measures including Total Revenue, Returns Rate, MoM Revenue, and Average Order Value</li>
          <li>Identified that Electronics drives the highest order volume (63K) but also the highest return volume (8.2K) — surfacing a product quality investigation opportunity</li>
          <li>Discovered a 4.6× revenue gap between the North (9.6bn) and Central (2.1bn) regions, indicating regional expansion opportunity</li>
          <li>Segmented 790K+ orders across customer income brackets (Middle, Lower-Middle, Low, Upper-Middle) to inform targeted marketing strategy</li>
          <li>Ranked top sellers by order volume with Wali Group leading at 794 orders, ~7% above the next seller</li>
        </ul>
        <div class="project-tech">
          <span class="tech-tag">Power BI Desktop</span>
          <span class="tech-tag">DAX</span>
          <span class="tech-tag">Power Query (M)</span>
          <span class="tech-tag">Star Schema</span>
          <span class="tech-tag">Medallion Architecture</span>
          <span class="tech-tag">KPI Analysis</span>
          <span class="tech-tag">Customer Segmentation</span>
        </div>
        <a href="https://github.com/HendroCahyoRamadhan/E-CommerceDashboardBreakdownPowerBI" target="_blank" class="project-link">
          View on GitHub ↗
        </a>
      </div>
    </div>
  </section>

  <!-- ════════ EDUCATION / BACKGROUND ════════ -->
  <section>
    <p class="section-label">Background</p>
    <h2 class="section-title">Education &amp; Development</h2>
    <div class="timeline">
      <div class="tl-item">
        <div class="tl-dot"></div>
        <div class="tl-content">
          <p class="tl-date">Ongoing</p>
          <p class="tl-title">Self-Directed Learning — Data Engineering &amp; Analytics</p>
          <p class="tl-org">Independent / GitHub Portfolio</p>
          <p class="tl-desc">
            Continuously building practical skills through project-based learning,
            implementing industry standards including Medallion Architecture, star-schema
            design, ETL pipelines, and Power BI dashboarding with real-world datasets.
          </p>
        </div>
      </div>
      <div class="tl-item">
        <div class="tl-dot"></div>
        <div class="tl-content">
          <p class="tl-date">Project — 2025</p>
          <p class="tl-title">Data Warehouse Project (SQL)</p>
          <p class="tl-org">github.com/HendroCahyoRamadhan</p>
          <p class="tl-desc">
            Delivered a full-stack data warehouse from raw CSV ingestion to Gold-layer
            analytical tables, including ETL scripting (58 commits), data quality checks,
            and architecture documentation.
          </p>
        </div>
      </div>
      <div class="tl-item">
        <div class="tl-dot"></div>
        <div class="tl-content">
          <p class="tl-date">Project — 2025</p>
          <p class="tl-title">E-Commerce Power BI Dashboard</p>
          <p class="tl-org">github.com/HendroCahyoRamadhan</p>
          <p class="tl-desc">
            Built a production-ready BI dashboard covering 790K+ orders, 8 data tables,
            and multi-dimensional KPI analysis including revenue, returns, fulfillment,
            and marketing attribution.
          </p>
        </div>
      </div>
    </div>
  </section>

  <!-- ════════ WHAT I BRING ════════ -->
  <section>
    <p class="section-label">Value Proposition</p>
    <h2 class="section-title">What I Bring to the Table</h2>
    <div class="skills-grid">
      <div class="skill-card">
        <p class="skill-category">End-to-End Ownership</p>
        <p style="font-size:13px;color:var(--mid);line-height:1.7;margin-top:4px;">
          From raw data ingestion to polished dashboards — I own the full pipeline, not just one layer.
        </p>
      </div>
      <div class="skill-card">
        <p class="skill-category">Business-First Mindset</p>
        <p style="font-size:13px;color:var(--mid);line-height:1.7;margin-top:4px;">
          Every query and visual is framed around business questions: revenue, retention, efficiency.
        </p>
      </div>
      <div class="skill-card">
        <p class="skill-category">Documentation Culture</p>
        <p style="font-size:13px;color:var(--mid);line-height:1.7;margin-top:4px;">
          Clean, well-documented code and data models that teams can onboard to quickly.
        </p>
      </div>
      <div class="skill-card">
        <p class="skill-category">Industry Best Practices</p>
        <p style="font-size:13px;color:var(--mid);line-height:1.7;margin-top:4px;">
          Medallion Architecture, star schema, version-controlled SQL — not shortcuts, real craft.
        </p>
      </div>
    </div>
  </section>

</div>

<footer>
  Hendro Cahyo Ramadhan &nbsp;·&nbsp; Data Analyst &nbsp;·&nbsp;
  <span>hendrocr20@gmail.com</span> &nbsp;·&nbsp;
  github.com/HendroCahyoRamadhan
</footer>

</body>
</html>

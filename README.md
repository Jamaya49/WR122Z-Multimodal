<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Why Small Service Businesses Fail | Justus Dockery</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;900&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --ink: #1a1208;
    --ink-soft: #4a3f2e;
    --ink-muted: #8a7d6a;
    --paper: #faf7f2;
    --paper-warm: #f2ede3;
    --paper-dark: #e8e0d0;
    --accent: #c0392b;
    --accent-light: #f5e6e4;
    --accent-mid: #e8a099;
    --gold: #b07d2a;
    --gold-light: #f5edd5;
  }
  * { margin: 0; padding: 0; box-sizing: border-box; }
  html { scroll-behavior: smooth; }
  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--paper);
    color: var(--ink);
    font-size: 17px;
    line-height: 1.75;
  }

  /* NAV */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    background: rgba(250,247,242,0.94);
    backdrop-filter: blur(8px);
    border-bottom: 1px solid var(--paper-dark);
    padding: 0 3rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 56px;
  }
  .nav-brand {
    font-family: 'Playfair Display', serif;
    font-size: 15px;
    font-weight: 700;
    color: var(--accent);
    letter-spacing: 0.02em;
    text-decoration: none;
  }
  .nav-links {
    display: flex;
    gap: 2rem;
    list-style: none;
  }
  .nav-links a {
    font-size: 13px;
    font-weight: 500;
    color: var(--ink-soft);
    text-decoration: none;
    letter-spacing: 0.05em;
    text-transform: uppercase;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--accent); }

  /* AUDIENCE BANNER */
  .audience-banner {
    margin-top: 56px;
    background: var(--gold-light);
    border-bottom: 1px solid #d4b87a;
    padding: 0.9rem 6rem;
    display: flex;
    align-items: center;
    gap: 1.5rem;
  }
  .audience-label {
    font-size: 11px;
    font-weight: 500;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--gold);
    flex-shrink: 0;
  }
  .audience-text {
    font-size: 14px;
    color: var(--ink-soft);
    font-weight: 300;
  }
  .audience-text strong { font-weight: 500; color: var(--ink); }

  /* HERO */
  .hero {
    min-height: 92vh;
    padding: 5rem 6rem 5rem;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: center;
    background: var(--paper);
    position: relative;
    overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute;
    top: -80px; right: -80px;
    width: 560px; height: 560px;
    border-radius: 50%;
    background: var(--accent-light);
    opacity: 0.45;
    z-index: 0;
  }
  .hero-text { position: relative; z-index: 1; }
  .hero-eyebrow {
    font-size: 12px;
    font-weight: 500;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 1.2rem;
  }
  .hero-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.6rem, 5vw, 4.2rem);
    font-weight: 900;
    line-height: 1.08;
    color: var(--ink);
    margin-bottom: 1.5rem;
  }
  .hero-title span { color: var(--accent); display: block; }
  .hero-subtitle {
    font-size: 1.1rem;
    color: var(--ink-soft);
    max-width: 480px;
    margin-bottom: 2rem;
    font-weight: 300;
    line-height: 1.8;
  }
  .hero-meta {
    display: flex;
    gap: 2rem;
    font-size: 13px;
    color: var(--ink-muted);
    border-top: 1px solid var(--paper-dark);
    padding-top: 1.2rem;
  }
  .hero-meta strong {
    display: block;
    font-size: 11px;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--ink-muted);
    margin-bottom: 2px;
    font-weight: 500;
  }

  /* STAT CARDS */
  .hero-visual {
    position: relative;
    z-index: 1;
    display: flex;
    flex-direction: column;
    gap: 1.2rem;
  }
  .stat-card {
    background: white;
    border: 1px solid var(--paper-dark);
    border-radius: 12px;
    padding: 1.5rem 1.75rem;
    display: flex;
    align-items: center;
    gap: 1.25rem;
    box-shadow: 0 2px 16px rgba(0,0,0,0.06);
    animation: slideIn 0.6s ease forwards;
    opacity: 0;
    transform: translateX(30px);
  }
  .stat-card:nth-child(1) { animation-delay: 0.2s; }
  .stat-card:nth-child(2) { animation-delay: 0.4s; }
  .stat-card:nth-child(3) { animation-delay: 0.6s; }
  @keyframes slideIn { to { opacity: 1; transform: translateX(0); } }
  .stat-num {
    font-family: 'Playfair Display', serif;
    font-size: 2.8rem;
    font-weight: 900;
    color: var(--accent);
    line-height: 1;
    min-width: 90px;
  }
  .stat-label { font-size: 14px; color: var(--ink-soft); line-height: 1.5; }
  .stat-label strong { display: block; font-size: 15px; color: var(--ink); margin-bottom: 2px; }

  /* THESIS BAND */
  .thesis-band {
    background: var(--accent);
    color: white;
    padding: 4rem 6rem;
    text-align: center;
  }
  .thesis-band blockquote {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.3rem, 2.5vw, 2rem);
    font-weight: 400;
    font-style: italic;
    max-width: 860px;
    margin: 0 auto 1.5rem;
    line-height: 1.5;
  }
  .thesis-band cite {
    font-size: 13px;
    opacity: 0.75;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    font-style: normal;
  }

  /* PHOTO BANNER */
  .photo-banner {
    width: 100%;
    height: 340px;
    overflow: hidden;
    position: relative;
  }
  .photo-banner img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center;
    display: block;
  }
  .photo-banner-caption {
    position: absolute;
    bottom: 0; left: 0; right: 0;
    background: linear-gradient(transparent, rgba(0,0,0,0.55));
    color: rgba(255,255,255,0.85);
    font-size: 12px;
    padding: 2rem 2.5rem 1rem;
    letter-spacing: 0.05em;
  }

  /* SECTIONS */
  .section { padding: 6rem 6rem; }
  .section:nth-child(even) { background: var(--paper-warm); }
  .section-eyebrow {
    font-size: 11px;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--accent);
    font-weight: 500;
    margin-bottom: 0.6rem;
  }
  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.8rem, 3vw, 2.6rem);
    font-weight: 700;
    color: var(--ink);
    margin-bottom: 1.5rem;
    line-height: 1.2;
    max-width: 700px;
  }
  .section-body {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: start;
  }
  .section-body.wide { grid-template-columns: 1.4fr 1fr; }
  .prose p { color: var(--ink-soft); margin-bottom: 1.2rem; font-weight: 300; }
  .prose p:last-child { margin-bottom: 0; }

  /* PHOTO IN SECTION */
  .section-photo {
    width: 100%;
    border-radius: 14px;
    overflow: hidden;
    margin-bottom: 1rem;
  }
  .section-photo img {
    width: 100%;
    height: 220px;
    object-fit: cover;
    display: block;
  }
  .photo-credit {
    font-size: 11px;
    color: var(--ink-muted);
    margin-top: 5px;
    text-align: right;
  }

  /* PULLQUOTE */
  .pullquote {
    border-left: 4px solid var(--accent);
    padding: 1.2rem 1.5rem;
    background: white;
    border-radius: 0 10px 10px 0;
    margin: 1.5rem 0;
  }
  .pullquote p {
    font-family: 'Playfair Display', serif;
    font-size: 1.15rem;
    font-style: italic;
    color: var(--ink);
    margin-bottom: 0.4rem;
  }
  .pullquote cite {
    font-size: 12px;
    color: var(--ink-muted);
    letter-spacing: 0.08em;
    font-style: normal;
  }

  /* VISUAL CARDS */
  .visual-stack { display: flex; flex-direction: column; gap: 1rem; }
  .v-card {
    background: white;
    border: 1px solid var(--paper-dark);
    border-radius: 12px;
    padding: 1.4rem 1.5rem;
    display: flex;
    gap: 1.2rem;
    align-items: flex-start;
  }
  .v-card-icon {
    width: 44px; height: 44px;
    border-radius: 10px;
    background: var(--accent-light);
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    font-size: 1.4rem;
  }
  .v-card-content strong {
    display: block;
    font-size: 15px;
    font-weight: 500;
    color: var(--ink);
    margin-bottom: 4px;
  }
  .v-card-content p {
    font-size: 14px;
    color: var(--ink-soft);
    line-height: 1.55;
    font-weight: 300;
  }

  /* CHART */
  .chart-container {
    background: white;
    border: 1px solid var(--paper-dark);
    border-radius: 14px;
    padding: 2rem;
  }
  .chart-title {
    font-size: 13px;
    font-weight: 500;
    color: var(--ink-muted);
    letter-spacing: 0.08em;
    text-transform: uppercase;
    margin-bottom: 1.5rem;
  }
  .bar-row { display: flex; align-items: center; gap: 1rem; margin-bottom: 1rem; }
  .bar-row:last-child { margin-bottom: 0; }
  .bar-label {
    font-size: 13px;
    color: var(--ink-soft);
    width: 140px;
    flex-shrink: 0;
    text-align: right;
    font-weight: 400;
  }
  .bar-track {
    flex: 1;
    height: 28px;
    background: var(--paper-warm);
    border-radius: 4px;
    overflow: hidden;
  }
  .bar-fill {
    height: 100%;
    border-radius: 4px;
    display: flex;
    align-items: center;
    padding-right: 10px;
    justify-content: flex-end;
    font-size: 12px;
    font-weight: 500;
    color: white;
    background: var(--accent);
    width: 0%;
    transition: width 1.5s ease;
  }
  .bar-fill.secondary { background: var(--ink-soft); }
  .bar-fill.tertiary { background: var(--ink-muted); }

  /* CYCLE */
  .cycle {
    background: white;
    border: 1px solid var(--paper-dark);
    border-radius: 14px;
    padding: 2rem;
  }
  .cycle-title {
    font-size: 13px;
    font-weight: 500;
    color: var(--ink-muted);
    letter-spacing: 0.08em;
    text-transform: uppercase;
    margin-bottom: 1.5rem;
  }
  .cycle-step {
    display: flex;
    gap: 1rem;
    align-items: flex-start;
    padding-bottom: 1.5rem;
    position: relative;
  }
  .cycle-step:last-child { padding-bottom: 0; }
  .step-line { display: flex; flex-direction: column; align-items: center; flex-shrink: 0; }
  .step-dot {
    width: 28px; height: 28px;
    border-radius: 50%;
    background: var(--accent);
    color: white;
    font-size: 12px;
    font-weight: 700;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .step-connector {
    width: 2px; flex: 1;
    background: var(--paper-dark);
    margin-top: 4px;
    min-height: 28px;
  }
  .cycle-step:last-child .step-connector { display: none; }
  .step-text strong {
    display: block;
    font-size: 14px;
    font-weight: 500;
    color: var(--ink);
    margin-bottom: 2px;
    padding-top: 4px;
  }
  .step-text p { font-size: 13px; color: var(--ink-muted); line-height: 1.5; }

  /* CONCLUSION */
  .conclusion {
    background: var(--ink);
    color: white;
    padding: 6rem;
    text-align: center;
  }
  .conclusion h2 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.8rem, 3.5vw, 3rem);
    font-weight: 700;
    margin-bottom: 1.5rem;
    line-height: 1.2;
  }
  .conclusion h2 span { color: var(--accent-mid); }
  .conclusion p {
    max-width: 700px;
    margin: 0 auto 1.2rem;
    font-weight: 300;
    font-size: 1.05rem;
    line-height: 1.8;
    color: rgba(255,255,255,0.8);
  }
  .conclusion p:last-of-type { margin-bottom: 2.5rem; }
  .action-box {
    display: inline-flex;
    flex-direction: column;
    gap: 0.8rem;
    background: rgba(255,255,255,0.06);
    border: 1px solid rgba(255,255,255,0.15);
    border-radius: 14px;
    padding: 1.5rem 2.5rem;
    text-align: left;
    max-width: 560px;
    margin: 0 auto;
  }
  .action-box-title {
    font-size: 11px;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--accent-mid);
    font-weight: 500;
  }
  .action-item {
    display: flex;
    gap: 0.75rem;
    align-items: flex-start;
    font-size: 14px;
    color: rgba(255,255,255,0.85);
    font-weight: 300;
    line-height: 1.5;
  }
  .action-num {
    background: var(--accent);
    color: white;
    width: 22px; height: 22px;
    border-radius: 50%;
    font-size: 11px;
    font-weight: 700;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    margin-top: 1px;
  }

  /* WORKS CITED */
  .works-cited { padding: 5rem 6rem; background: var(--paper-warm); }
  .works-cited h2 {
    font-family: 'Playfair Display', serif;
    font-size: 1.8rem;
    font-weight: 700;
    color: var(--ink);
    margin-bottom: 0.5rem;
  }
  .works-cited .subtitle { font-size: 13px; color: var(--ink-muted); margin-bottom: 2.5rem; }
  .citations-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; }
  .citation-card {
    background: white;
    border: 1px solid var(--paper-dark);
    border-radius: 10px;
    padding: 1.2rem 1.4rem;
  }
  .citation-card .author { font-size: 13px; font-weight: 500; color: var(--ink); margin-bottom: 4px; }
  .citation-card .ref { font-size: 12px; color: var(--ink-muted); line-height: 1.55; font-style: italic; }
  .citation-card .ref a { color: var(--accent); text-decoration: none; }

  /* FOOTER */
  footer {
    background: var(--ink);
    color: rgba(255,255,255,0.4);
    text-align: center;
    padding: 1.8rem;
    font-size: 12px;
    letter-spacing: 0.05em;
  }

  /* ANIMATIONS */
  .fade-up {
    opacity: 0;
    transform: translateY(24px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }
  .fade-up.visible { opacity: 1; transform: translateY(0); }

  @media (max-width: 900px) {
    .hero, .section-body, .section-body.wide, .citations-grid { grid-template-columns: 1fr; }
    .hero, .section, .works-cited, .conclusion, .thesis-band, .audience-banner { padding-left: 1.5rem; padding-right: 1.5rem; }
    nav { padding: 0 1.5rem; }
    .nav-links { display: none; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#" class="nav-brand">Why Small Businesses Fail</a>
  <ul class="nav-links">
    <li><a href="#demand">Market Demand</a></li>
    <li><a href="#marketing">Marketing</a></li>
    <li><a href="#retention">Retention</a></li>
    <li><a href="#conclusion">Key Takeaways</a></li>
    <li><a href="#citations">Sources</a></li>
  </ul>
</nav>

<!-- AUDIENCE BANNER -->
<div class="audience-banner">
  <span class="audience-label">Written for</span>
  <span class="audience-text"><strong>Aspiring entrepreneurs and new small business owners</strong> people considering launching a service business who may not yet realize that customer strategy matters more than financial planning in the early stages.</span>
</div>

<!-- HERO -->
<section class="hero">
  <div class="hero-text fade-up visible">
    <p class="hero-eyebrow">WR 122Z &nbsp;·&nbsp; Research Argument &nbsp;·&nbsp; Justus Dockery</p>
    <h1 class="hero-title">
      Why Small Service Businesses
      <span>Really Fail</span>
    </h1>
    <p class="hero-subtitle">
      When a service business closes, most people blame the money. But financial collapse is never where failure begins. The real cause breaks long before the bank account runs dry and it starts with customers.
    </p>
    <div class="hero-meta">
      <div><strong>Topic</strong>Entrepreneurship</div>
      <div><strong>Focus</strong>Service Businesses</div>
      <div><strong>Argument</strong>Customers drive everything</div>
    </div>
  </div>
  <div class="hero-visual">
    <div class="stat-card">
      <div class="stat-num">42%</div>
      <div class="stat-label">
        <strong>No market demand</strong>
        The #1 reason startups fail customers simply didn't want the service (CB Insights, 2021)
      </div>
    </div>
    <div class="stat-card">
      <div class="stat-num">20%</div>
      <div class="stat-label">
        <strong>Fail in year one</strong>
        Most failures trace back to customers, not cash flow
      </div>
    </div>
    <div class="stat-card">
      <div class="stat-num">#1</div>
      <div class="stat-label">
        <strong>Cash flow problems</strong>
        Cited by SBA (2023) as a top predictor of failure but cash problems don't start with money
      </div>
    </div>
  </div>
</section>

<!-- THESIS BAND -->
<div class="thesis-band">
  <blockquote>
    "Customer relationships are not one factor among many in small business survival. Customer relationships are the factor everything else depends on."
  </blockquote>
  <cite>  Central Argument</cite>
</div>

<!-- PHOTO BANNER 1 -->
<div class="photo-banner">
  <img src="https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=1400&q=80&fit=crop" alt="Small service business worker in the field" loading="lazy">
  <div class="photo-banner-caption">Service businesses landscaping, detailing, repair are among the most common small businesses launched each year, and among the most likely to close within two years.</div>
</div>

<!-- SECTION 1: NO MARKET DEMAND -->
<section class="section" id="demand">
  <div class="section-eyebrow">Problem 01</div>
  <h2 class="section-title fade-up">Launching Before Confirming Anyone Wants the Service</h2>
  <div class="section-body wide">
    <div class="prose fade-up">
      <p>
        Many entrepreneurs trust their technical skills their ability to cut lawns, detail cars, or fix appliances. But technical skill does not guarantee customer demand. Owners spend months building operations around assumptions they never tested with real customers.
      </p>
      <p>
        Steve Blank's concept of <em>customer discovery</em> challenges the traditional business planning model. Instead of treating customer behavior as predictable, Blank argues owners must gather feedback from real potential customers before committing serious time or money (Blank, 2013). Test a limited version of the service first. Measure the response. Adjust before expanding.
      </p>
      <p>
        Eric Ries echoes this in <em>The Lean Startup</em>, describing business assumptions as hypotheses that must be tested rather than trusted (Ries, 2011). A landscaping company may believe customers care most about low prices while customers may actually value communication and reliability far more. Businesses that skip testing end up improving things customers don't care about.
      </p>
      <div class="pullquote">
        <p>"42% of failed startups collapsed because customers did not want the product or service."</p>
        <cite>  CB Insights, 2021</cite>
      </div>
      <p>
        That statistic matters because it shows that many businesses fail <em>before</em> financial problems even begin. The money doesn't run out first the customers never showed up in the first place.
      </p>
    </div>
    <div class="fade-up">
      <div class="section-photo">
        <img src="https://images.unsplash.com/photo-1521791136064-7986c2920216?w=800&q=80&fit=crop" alt="Entrepreneur planning a business">
        <p class="photo-credit">Photo: Unsplash</p>
      </div>
      <div class="chart-container" style="margin-top:1rem;">
        <p class="chart-title">Top reasons startups fail (CB Insights, 2021)</p>
        <div class="bar-row">
          <div class="bar-label">No market need</div>
          <div class="bar-track"><div class="bar-fill" data-width="42%">42%</div></div>
        </div>
        <div class="bar-row">
          <div class="bar-label">Ran out of cash</div>
          <div class="bar-track"><div class="bar-fill secondary" data-width="29%">29%</div></div>
        </div>
        <div class="bar-row">
          <div class="bar-label">Wrong team</div>
          <div class="bar-track"><div class="bar-fill tertiary" data-width="23%">23%</div></div>
        </div>
        <div class="bar-row">
          <div class="bar-label">Outcompeted</div>
          <div class="bar-track"><div class="bar-fill tertiary" data-width="19%">19%</div></div>
        </div>
        <div class="bar-row">
          <div class="bar-label">Pricing issues</div>
          <div class="bar-track"><div class="bar-fill tertiary" data-width="18%">18%</div></div>
        </div>
      </div>
      <div class="v-card" style="margin-top:1rem;">
        <div class="v-card-icon">💡</div>
        <div class="v-card-content">
          <strong>The Build-Measure-Learn Cycle</strong>
          <p>Ries (2011) recommends launching small, gathering feedback fast, and improving based on what real customers say not what owners assume they want.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- SECTION 2: MARKETING -->
<section class="section" id="marketing">
  <div class="section-eyebrow">Problem 02</div>
  <h2 class="section-title fade-up">Relying on Word-of-Mouth Instead of Building Visibility</h2>
  <div class="section-body">
    <div class="visual-stack fade-up">
      <div class="section-photo">
        <img src="https://images.unsplash.com/photo-1611926653458-09294b3142bf?w=800&q=80&fit=crop" alt="Social media marketing on phone">
        <p class="photo-credit">Photo: Unsplash</p>
      </div>
      <div class="v-card">
        <div class="v-card-icon">👁️</div>
        <div class="v-card-content">
          <strong>Customers can't evaluate quality in advance</strong>
          <p>In service industries, customers judge trust before they judge skill. Reviews, response times, and social media presence signal credibility before any work begins (Scarborough & Cornwall, 2019).</p>
        </div>
      </div>
      <div class="v-card">
        <div class="v-card-icon">🔍</div>
        <div class="v-card-content">
          <strong>The invisibility problem</strong>
          <p>Skilled providers lose customers when potential clients never notice the business. Strong work earns loyalty but only from customers who find you first (Kotler & Keller, 2016).</p>
        </div>
      </div>
      <div class="v-card">
        <div class="v-card-icon">⚖️</div>
        <div class="v-card-content">
          <strong>When businesses look the same, trust wins</strong>
          <p>Without a visible brand or clear value, customers choose the competitor that appears easier to contact or more professional (Longenecker et al., 2013).</p>
        </div>
      </div>
    </div>
    <div class="prose fade-up">
      <p>
        Many service business owners rely on word-of-mouth and assume strong work will naturally attract customers. Quality matters but quality does not create enough growth on its own, especially early on.
      </p>
      <p>
        Kotler and Keller define marketing as identifying customer needs and explaining why one business meets those needs better than competitors (Kotler & Keller, 2016). A business that never communicates its value leaves that explanation to chance.
      </p>
      <p>
        The challenge is sharpened by the nature of services. A customer comparing two detailing companies cannot evaluate quality before making a choice they lack the technical knowledge. So they judge credibility instead. Businesses that appear unprofessional or difficult to contact lose customers even when their actual work is superior.
      </p>
      <div class="pullquote">
        <p>"When customers cannot distinguish businesses from one another, they choose the business that appears easier to contact or easier to trust."</p>
        <cite>  Longenecker et al., 2013</cite>
      </div>
      <p>
        Businesses without a visible brand or a clear explanation of value lose potential customers because customers see no reason to choose one business over another. Visibility is not vanity it is survival.
      </p>
    </div>
  </div>
</section>

<!-- PHOTO BANNER 2 -->
<div class="photo-banner">
  <img src="https://images.unsplash.com/photo-1454165804606-c3d57bc86b40?w=1400&q=80&fit=crop" alt="Business owner reviewing finances" loading="lazy">
  <div class="photo-banner-caption">By the time financial trouble becomes visible, the customer problem causing it has often been developing for months.</div>
</div>

<!-- SECTION 3: FINANCIAL SPIRAL -->
<section class="section" id="retention">
  <div class="section-eyebrow">Problem 03</div>
  <h2 class="section-title fade-up">Customer Problems Become Financial Problems Then It's Too Late</h2>
  <div class="section-body wide">
    <div class="prose fade-up">
      <p>
        The standard advice given to struggling small businesses is financial: cut costs, find investors, improve cash flow. That advice is not wrong but it arrives too late. By the time a service business needs financial rescue, the customer problem causing it has been developing for months.
      </p>
      <p>
        The U.S. Small Business Administration (2023) identifies poor cash flow management as one of the strongest predictors of business failure. But cash flow problems do not appear without warning. They develop when owners fail to maintain a stable customer base. A business with repeat customers can survive a slow season. A business searching for new customers at the start of every slow period cannot survive those same conditions.
      </p>
      <p>
        Susan Coleman's research confirms the connection: businesses with limited capital face greater risk because they lack financial protection when revenue drops (Coleman, 2014). But loans cannot replace consistent customers. Businesses that ignore customer relationships borrow money to compensate for weak demand a cycle that ends in closure.
      </p>
      <div class="pullquote">
        <p>"Blaming business failure on finances is like blaming a car accident on the ambulance bill. The cost is real, but the cost is not the cause."</p>
        <cite>  Central Argument</cite>
      </div>
      <p>
        Owners who stop adapting after the startup phase make this worse. Taneja, Pryor, and Hayek found that businesses lose customers because owners continue using outdated methods while customer expectations change (Taneja et al., 2016). Customers who once valued low prices may later prioritize convenience. Those who once called to schedule may now expect online booking. Businesses that ignore those shifts lose relevance and then revenue.
      </p>
      <p>
        Service businesses that adopted online booking systems, social media marketing, and mobile payment options adapted to changing customer expectations better than those that ignored those tools. Customers saw those changes as signs the business was paying attention to their needs building loyalty even through difficult economic periods (Ries, 2011).
      </p>
    </div>
    <div class="fade-up">
      <div class="cycle">
        <p class="cycle-title">The customer-to-financial failure spiral</p>
        <div class="cycle-steps">
          <div class="cycle-step">
            <div class="step-line"><div class="step-dot">1</div><div class="step-connector"></div></div>
            <div class="step-text"><strong>No market testing</strong><p>Owner launches based on assumptions, not verified customer demand.</p></div>
          </div>
          <div class="cycle-step">
            <div class="step-line"><div class="step-dot">2</div><div class="step-connector"></div></div>
            <div class="step-text"><strong>Weak visibility & trust</strong><p>No marketing strategy means potential customers never find the business.</p></div>
          </div>
          <div class="cycle-step">
            <div class="step-line"><div class="step-dot">3</div><div class="step-connector"></div></div>
            <div class="step-text"><strong>No repeat customer base</strong><p>Each slow season requires rebuilding from scratch. No loyalty buffer exists.</p></div>
          </div>
          <div class="cycle-step">
            <div class="step-line"><div class="step-dot">4</div><div class="step-connector"></div></div>
            <div class="step-text"><strong>Cash flow collapses</strong><p>Revenue drops without the cushion of loyal, returning customers.</p></div>
          </div>
          <div class="cycle-step">
            <div class="step-line"><div class="step-dot">5</div><div class="step-connector"></div></div>
            <div class="step-text"><strong>Business closes</strong><p>The financial failure is visible but it began with the customer failure months earlier.</p></div>
          </div>
        </div>
      </div>
      <div class="section-photo" style="margin-top:1rem;">
        <img src="https://images.unsplash.com/photo-1600880292203-757bb62b4baf?w=800&q=80&fit=crop" alt="Small business owner meeting with customer">
        <p class="photo-credit">Photo: Unsplash</p>
      </div>
    </div>
  </div>
</section>

<!-- CONCLUSION -->
<section class="conclusion" id="conclusion">
  <h2>The Money Follows When <span>Customers Want You to Exist</span></h2>
  <p>
    Economic conditions, market saturation, and competition from larger companies all create real pressure on small businesses (Storey, 2016). These forces are real and outside any owner's control.
  </p>
  <p>
    But businesses with strong customer relationships survive those pressures with far greater success than businesses without them. Loyal customers support businesses they trust during difficult periods. Strong differentiation protects businesses from competitors that compete only on price.
  </p>
  <p>
    The entrepreneurs most likely to build lasting service businesses are not those with the strongest financial plans. They are the ones who understand what customers want, earn trust before they have to, and keep paying attention as customers change over time.
  </p>
  <div class="action-box">
    <p class="action-box-title">Before buying equipment or placing your first ad:</p>
    <div class="action-item"><div class="action-num">1</div>Speak with potential customers and test your assumptions about what they actually value</div>
    <div class="action-item"><div class="action-num">2</div>Build visibility and trust before you need customers to trust you</div>
    <div class="action-item"><div class="action-num">3</div>Keep adapting customer expectations evolve, and businesses that stop listening lose relevance</div>
  </div>
</section>

<!-- WORKS CITED -->
<section class="works-cited" id="citations">
  <h2>Works Cited</h2>
  <p class="subtitle">All sources consulted in this research argument MLA/APA hybrid format as used in the original paper</p>
  <div class="citations-grid">
    <div class="citation-card">
      <p class="author">Blank, S. (2013)</p>
      <p class="ref">Why the lean start-up changes everything. <em>Harvard Business Review, 91</em>(5), 63–72.</p>
    </div>
    <div class="citation-card">
      <p class="author">CB Insights (2021)</p>
      <p class="ref">The top 12 reasons startups fail. <a href="https://www.cbinsights.com/research/report/startup-failure-reasons-top/" target="_blank">cbinsights.com ↗</a></p>
    </div>
    <div class="citation-card">
      <p class="author">Coleman, S. (2014)</p>
      <p class="ref">Access to capital and terms of credit: A comparison of men- and women-owned small businesses. <em>Journal of Small Business Management, 52</em>(2), 252–272.</p>
    </div>
    <div class="citation-card">
      <p class="author">Kotler, P., & Keller, K. L. (2016)</p>
      <p class="ref"><em>Marketing management</em> (15th ed.). Pearson.</p>
    </div>
    <div class="citation-card">
      <p class="author">Longenecker, J. G., Petty, J. W., Palich, L. E., & Hoy, F. (2013)</p>
      <p class="ref"><em>Small business management: Launching and growing entrepreneurial ventures</em> (17th ed.). Cengage Learning.</p>
    </div>
    <div class="citation-card">
      <p class="author">Ries, E. (2011)</p>
      <p class="ref"><em>The lean startup.</em> Crown Business.</p>
    </div>
    <div class="citation-card">
      <p class="author">Scarborough, N. M., & Cornwall, J. R. (2019)</p>
      <p class="ref"><em>Essentials of entrepreneurship and small business management</em> (9th ed.). Pearson.</p>
    </div>
    <div class="citation-card">
      <p class="author">Storey, D. J. (2016)</p>
      <p class="ref"><em>Understanding the small business sector.</em> Routledge.</p>
    </div>
    <div class="citation-card">
      <p class="author">Taneja, S., Pryor, M. G., & Hayek, M. (2016)</p>
      <p class="ref">Leaping innovation barriers to small business longevity. <em>Journal of Business Strategy, 37</em>(3), 44–51.</p>
    </div>
    <div class="citation-card">
      <p class="author">U.S. Small Business Administration (2023)</p>
      <p class="ref">Small business trends and statistics. <a href="https://www.sba.gov/business-guide/plan-your-business/market-research-competitive-analysis" target="_blank">sba.gov ↗</a></p>
    </div>
  </div>
</section>

<footer>
  Justus Dockery &nbsp;·&nbsp; WR 122Z &nbsp;·&nbsp; Multimodal Research Revision &nbsp;·&nbsp; Photos via Unsplash (free use license)
</footer>

<script>
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
  }, { threshold: 0.12 });
  document.querySelectorAll('.fade-up').forEach(el => observer.observe(el));

  const bars = document.querySelectorAll('.bar-fill');
  const barObserver = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        bars.forEach(b => { b.style.width = b.dataset.width; });
        barObserver.disconnect();
      }
    });
  }, { threshold: 0.3 });
  const chart = document.querySelector('.chart-container');
  if (chart) barObserver.observe(chart);
</script>
</body>
</html>

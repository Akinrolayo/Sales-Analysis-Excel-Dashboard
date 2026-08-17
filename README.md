<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Retail Sales Analysis – Project Write-Up</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Playfair+Display:wght@700&display=swap');

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --ink:      #1a1d23;
    --muted:    #5a6070;
    --accent:   #1d6fa4;
    --accent2:  #e8f3fb;
    --rule:     #d4dae3;
    --bg:       #f7f9fc;
    --card:     #ffffff;
    --green:    #1a7a4a;
    --green-bg: #eaf5ef;
  }

  body {
    font-family: 'Inter', sans-serif;
    background: var(--bg);
    color: var(--ink);
    line-height: 1.7;
    padding: 48px 24px 80px;
  }

  .wrapper {
    max-width: 860px;
    margin: 0 auto;
  }

  /* ── Header ── */
  .eyebrow {
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 12px;
  }

  h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(28px, 5vw, 46px);
    line-height: 1.15;
    color: var(--ink);
    margin-bottom: 20px;
  }

  h1 span {
    color: var(--accent);
  }

  .intro {
    font-size: 17px;
    color: var(--muted);
    max-width: 680px;
    margin-bottom: 36px;
    border-left: 3px solid var(--accent);
    padding-left: 16px;
  }

  hr.rule {
    border: none;
    border-top: 1px solid var(--rule);
    margin: 36px 0;
  }

  /* ── Tools badge row ── */
  .tools-label {
    font-size: 12px;
    font-weight: 600;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 12px;
  }

  .badges {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-bottom: 40px;
  }

  .badge {
    background: var(--accent2);
    color: var(--accent);
    font-size: 13px;
    font-weight: 600;
    padding: 6px 14px;
    border-radius: 20px;
    border: 1px solid #b8d9f0;
  }

  /* ── Section headings ── */
  h2 {
    font-family: 'Playfair Display', serif;
    font-size: 22px;
    color: var(--ink);
    margin-bottom: 14px;
    padding-bottom: 8px;
    border-bottom: 2px solid var(--rule);
  }

  /* ── Screenshot cards ── */
  .screenshot-card {
    background: var(--card);
    border: 1px solid var(--rule);
    border-radius: 10px;
    overflow: hidden;
    margin-bottom: 28px;
    box-shadow: 0 2px 8px rgba(0,0,0,.05);
  }

  .screenshot-card img {
    width: 100%;
    display: block;
  }

  .screenshot-card figcaption {
    padding: 10px 16px;
    font-size: 13px;
    color: var(--muted);
    border-top: 1px solid var(--rule);
    background: #fafbfc;
    font-style: italic;
  }

  /* ── Insights ── */
  .insights {
    background: var(--card);
    border: 1px solid var(--rule);
    border-radius: 10px;
    padding: 28px 32px;
    margin-bottom: 28px;
    box-shadow: 0 2px 8px rgba(0,0,0,.05);
  }

  .insights ul {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 16px;
  }

  .insights ul li {
    display: flex;
    gap: 14px;
    align-items: flex-start;
    font-size: 15px;
    line-height: 1.6;
  }

  .bullet-icon {
    flex-shrink: 0;
    width: 28px;
    height: 28px;
    border-radius: 50%;
    background: var(--green-bg);
    color: var(--green);
    font-size: 14px;
    font-weight: 700;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 2px;
  }

  strong.highlight { color: var(--accent); }

  /* ── Summary stat strip ── */
  .stat-strip {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
    gap: 16px;
    margin-bottom: 40px;
  }

  .stat-box {
    background: var(--card);
    border: 1px solid var(--rule);
    border-radius: 10px;
    padding: 20px 18px;
    text-align: center;
    box-shadow: 0 2px 6px rgba(0,0,0,.04);
  }

  .stat-box .number {
    font-family: 'Playfair Display', serif;
    font-size: 26px;
    color: var(--accent);
    font-weight: 700;
  }

  .stat-box .label {
    font-size: 12px;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.07em;
    color: var(--muted);
    margin-top: 4px;
  }
</style>
</head>
<body>
<div class="wrapper">

  <!-- ── Header ── -->
  <p class="eyebrow">Data Analytics Project</p>
  <h1>Retail Sales <span>Performance Analysis</span></h1>
  <p class="intro">
    This project analyses a full year of retail transaction data across multiple countries and customer segments, uncovering revenue trends, top-performing products, and high-value customers. Raw invoice records were cleaned, transformed, and visualised entirely within Excel — turning thousands of rows into actionable business intelligence through structured pivot analysis.
  </p>

  <!-- ── Key stats ── -->
  <div class="stat-strip">
    <div class="stat-box">
      <div class="number">$7.78M</div>
      <div class="label">Total Revenue</div>
    </div>
    <div class="stat-box">
      <div class="number">6</div>
      <div class="label">Countries</div>
    </div>
    <div class="stat-box">
      <div class="number">10</div>
      <div class="label">Top Customers Tracked</div>
    </div>
    <div class="stat-box">
      <div class="number">12 mo.</div>
      <div class="label">Period Covered</div>
    </div>
  </div>

  <!-- ── Tools ── -->
  <p class="tools-label">Tools Used</p>
  <div class="badges">
    <span class="badge">Microsoft Excel</span>
    <span class="badge">PivotTables</span>
    <span class="badge">Power Query</span>
    <span class="badge">PivotCharts</span>
    <span class="badge">Data Cleaning</span>
  </div>

  <hr class="rule">

  <!-- ── Screenshots ── -->
  <h2>Monthly Total Revenue</h2>
  <figure class="screenshot-card">
    <img src="Monthly_total_Revenue.JPG" alt="Monthly Total Revenue chart showing bar chart by month">
    <figcaption>Fig 1 – Monthly revenue pivot table and bar chart. November peaks at $1.22M; early months (Jan–Feb) are the weakest.</figcaption>
  </figure>

  <h2>Top Products by Revenue &amp; Quantity</h2>
  <figure class="screenshot-card">
    <img src="Top_project.JPG" alt="Top products pivot table showing revenue and quantity side by side">
    <figcaption>Fig 2 – Top 10 products ranked by total revenue and quantity sold. WHITE HANGING HEART T-LIGHT HOLDER leads in revenue at £81,188.</figcaption>
  </figure>

  <h2>Raw Sales Data</h2>
  <figure class="screenshot-card">
    <img src="sales.JPG" alt="Raw sales transaction data showing invoice records">
    <figcaption>Fig 3 – Cleaned transaction-level dataset with InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country, and Total Revenue columns.</figcaption>
  </figure>

  <h2>Top 10 Customers by Revenue</h2>
  <figure class="screenshot-card">
    <img src="Top_10_customers.JPG" alt="Top 10 customers bar chart with CustomerID and total revenue">
    <figcaption>Fig 4 – Customer ID 16251 is the single highest-value customer, generating $1.34M — more than 6× the second-ranked customer.</figcaption>
  </figure>

  <h2>Sales by Country</h2>
  <figure class="screenshot-card">
    <img src="Sales_by_coubtry.JPG" alt="Sales by country pivot table and horizontal bar chart">
    <figcaption>Fig 5 – United Kingdom dominates at $6.54M (88% of total revenue), followed by EIRE at $220K and Germany at $191K.</figcaption>
  </figure>

  <hr class="rule">

  <!-- ── Insights ── -->
  <h2>Key Insights</h2>
  <div class="insights">
    <ul>
      <li>
        <span class="bullet-icon">1</span>
        <span><strong class="highlight">Q4 drove the biggest revenue spike</strong> — November alone reached $1.22M, making it the highest single month of the year, likely driven by holiday gifting demand. December remained strong at $1.0M, suggesting a concentrated seasonal sales window that warrants dedicated inventory and marketing preparation.</span>
      </li>
      <li>
        <span class="bullet-icon">2</span>
        <span><strong class="highlight">Customer 16251 is a critical account</strong> — contributing $1.34M out of the $2.18M tracked across the top 10 customers (~62%). This level of concentration represents both an opportunity (nurture the relationship) and a risk (over-reliance on a single buyer).</span>
      </li>
      <li>
        <span class="bullet-icon">3</span>
        <span><strong class="highlight">WHITE HANGING HEART T-LIGHT HOLDER leads product revenue</strong> at £81,188 across 28,648 units, indicating strong, steady demand. It should be prioritised in stock forecasting and could anchor bundling or upsell strategies.</span>
      </li>
      <li>
        <span class="bullet-icon">4</span>
        <span><strong class="highlight">The United Kingdom accounts for ~88% of total revenue</strong> ($6.54M of $7.39M), while EIRE, Germany, France, Netherlands, and Australia together contribute just 12%. International markets remain largely untapped, presenting a clear growth opportunity if logistics and localisation challenges are addressed.</span>
      </li>
    </ul>
  </div>

</div>
</body>
</html>

---
name: infographic-generator
description: Generate beautiful data-driven infographics as HTML/SVG/PNG. Use when user asks to create infographics, data visualizations, charts, timelines, comparison graphics, process flows, statistical graphics, or visual data presentations. Supports Chart.js, D3.js, and pure SVG approaches.
license: MIT
metadata:
  version: 1.0.0
  author: Sam
  category: design
  domain: data-visualization
  updated: 2026-02-25
  tech-stack: HTML, SVG, CSS, Chart.js, D3.js, Puppeteer
---

# Infographic Generator

Create stunning, publication-ready infographics from data using HTML/SVG rendering.

---

## Keywords

infographic, data visualization, chart, graph, timeline, comparison, process flow, statistics, bar chart, pie chart, line graph, data graphics, visual presentation, D3.js, Chart.js, SVG infographic, data storytelling

---

## Infographic Types

### 1. Statistical Infographic
Best for: numbers, percentages, survey results

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&display=swap');
  * { margin: 0; padding: 0; box-sizing: border-box; }
  body { font-family: 'Inter', sans-serif; background: #0f172a; color: #f1f5f9; }
  .infographic { width: 1080px; margin: 0 auto; padding: 60px 50px; }
  .title { font-size: 42px; font-weight: 800; text-align: center; 
    background: linear-gradient(135deg, #6366f1, #ec4899);
    -webkit-background-clip: text; -webkit-text-fill-color: transparent; margin-bottom: 10px; }
  .subtitle { text-align: center; color: #94a3b8; font-size: 18px; margin-bottom: 50px; }
  .stat-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 30px; margin-bottom: 40px; }
  .stat-card { background: linear-gradient(135deg, rgba(99,102,241,0.1), rgba(236,72,153,0.1));
    border: 1px solid rgba(99,102,241,0.3); border-radius: 20px; padding: 35px; text-align: center; }
  .stat-number { font-size: 52px; font-weight: 800;
    background: linear-gradient(135deg, #6366f1, #ec4899);
    -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
  .stat-label { color: #94a3b8; font-size: 14px; margin-top: 8px; text-transform: uppercase; letter-spacing: 1px; }
  .bar-section { margin-top: 40px; }
  .bar-item { margin-bottom: 20px; }
  .bar-label { display: flex; justify-content: space-between; margin-bottom: 8px; font-size: 14px; }
  .bar-track { height: 12px; background: rgba(99,102,241,0.15); border-radius: 6px; overflow: hidden; }
  .bar-fill { height: 100%; border-radius: 6px;
    background: linear-gradient(90deg, #6366f1, #ec4899); transition: width 1s ease; }
  .footer { text-align: center; color: #475569; font-size: 12px; margin-top: 50px; padding-top: 20px;
    border-top: 1px solid rgba(99,102,241,0.2); }
</style>
</head>
<body>
<div class="infographic">
  <div class="title">YOUR TITLE HERE</div>
  <div class="subtitle">Subtitle with context</div>
  <div class="stat-grid">
    <div class="stat-card">
      <div class="stat-number">87%</div>
      <div class="stat-label">Metric One</div>
    </div>
    <div class="stat-card">
      <div class="stat-number">2.4M</div>
      <div class="stat-label">Metric Two</div>
    </div>
    <div class="stat-card">
      <div class="stat-number">156</div>
      <div class="stat-label">Metric Three</div>
    </div>
  </div>
  <div class="bar-section">
    <div class="bar-item">
      <div class="bar-label"><span>Category A</span><span>85%</span></div>
      <div class="bar-track"><div class="bar-fill" style="width:85%"></div></div>
    </div>
    <div class="bar-item">
      <div class="bar-label"><span>Category B</span><span>72%</span></div>
      <div class="bar-track"><div class="bar-fill" style="width:72%"></div></div>
    </div>
    <div class="bar-item">
      <div class="bar-label"><span>Category C</span><span>63%</span></div>
      <div class="bar-track"><div class="bar-fill" style="width:63%"></div></div>
    </div>
  </div>
  <div class="footer">Source: Your Data Source | Created 2026</div>
</div>
</body>
</html>
```

### 2. Timeline Infographic
Best for: history, project milestones, roadmaps

```html
<!-- Timeline infographic structure -->
<style>
  .timeline { position: relative; padding: 20px 0; }
  .timeline::before { content: ''; position: absolute; left: 50%; width: 3px; height: 100%;
    background: linear-gradient(180deg, #6366f1, #ec4899); transform: translateX(-50%); }
  .timeline-item { display: flex; margin-bottom: 40px; position: relative; }
  .timeline-item:nth-child(odd) { flex-direction: row-reverse; }
  .timeline-content { width: 45%; background: rgba(99,102,241,0.1); border: 1px solid rgba(99,102,241,0.3);
    border-radius: 16px; padding: 25px; }
  .timeline-dot { position: absolute; left: 50%; width: 20px; height: 20px; border-radius: 50%;
    background: linear-gradient(135deg, #6366f1, #ec4899); transform: translateX(-50%);
    border: 3px solid #0f172a; z-index: 1; }
  .timeline-date { font-size: 13px; color: #6366f1; font-weight: 600; text-transform: uppercase; }
  .timeline-title { font-size: 18px; font-weight: 700; margin: 8px 0; }
  .timeline-desc { font-size: 14px; color: #94a3b8; line-height: 1.6; }
</style>
```

### 3. Comparison Infographic
Best for: product comparisons, before/after, options analysis

```html
<style>
  .comparison { display: grid; grid-template-columns: 1fr 60px 1fr; gap: 0; align-items: start; }
  .option { background: rgba(99,102,241,0.08); border-radius: 20px; padding: 35px; }
  .option.right { background: rgba(236,72,153,0.08); }
  .vs-divider { display: flex; align-items: center; justify-content: center; }
  .vs-circle { width: 50px; height: 50px; border-radius: 50%;
    background: linear-gradient(135deg, #6366f1, #ec4899);
    display: flex; align-items: center; justify-content: center;
    font-weight: 800; font-size: 16px; }
  .feature-row { display: flex; justify-content: space-between; padding: 12px 0;
    border-bottom: 1px solid rgba(255,255,255,0.05); font-size: 14px; }
  .check { color: #22c55e; } .cross { color: #ef4444; }
</style>
```

### 4. Process/Flow Infographic
Best for: step-by-step guides, workflows, how-to content

```html
<style>
  .process { display: flex; flex-direction: column; gap: 0; }
  .step { display: flex; align-items: flex-start; gap: 25px; position: relative; }
  .step-number { width: 60px; height: 60px; border-radius: 50%; flex-shrink: 0;
    background: linear-gradient(135deg, #6366f1, #ec4899);
    display: flex; align-items: center; justify-content: center;
    font-size: 24px; font-weight: 800; }
  .step-connector { position: absolute; left: 30px; top: 60px; width: 3px; height: 40px;
    background: linear-gradient(180deg, #ec4899, #6366f1); }
  .step-content { flex: 1; padding-bottom: 40px; }
  .step-title { font-size: 20px; font-weight: 700; margin-bottom: 8px; }
  .step-desc { color: #94a3b8; font-size: 14px; line-height: 1.6; }
</style>
```

---

## Rendering to PNG

### Using Puppeteer (Node.js)
```javascript
const puppeteer = require('puppeteer');

async function renderInfographic(htmlPath, outputPath, width = 1080) {
  const browser = await puppeteer.launch();
  const page = await browser.newPage();
  await page.goto(`file://${htmlPath}`, { waitUntil: 'networkidle0' });
  
  // Auto-detect height
  const bodyHeight = await page.evaluate(() => document.body.scrollHeight);
  await page.setViewport({ width, height: bodyHeight });
  
  await page.screenshot({ path: outputPath, fullPage: true, type: 'png' });
  await browser.close();
}

renderInfographic('./infographic.html', './infographic.png');
```

### Using CLI
```bash
# Install puppeteer globally
npm install -g puppeteer

# Or use a simpler tool
npx capture-website infographic.html --output=infographic.png --width=1080 --full-page
```

---

## Chart.js Integration

```html
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<canvas id="myChart" width="800" height="400"></canvas>
<script>
new Chart(document.getElementById('myChart'), {
  type: 'bar', // 'line', 'pie', 'doughnut', 'radar', 'polarArea'
  data: {
    labels: ['Jan', 'Feb', 'Mar', 'Apr', 'May'],
    datasets: [{
      label: 'Revenue',
      data: [12000, 19000, 15000, 25000, 22000],
      backgroundColor: ['#6366f1', '#8b5cf6', '#a855f7', '#d946ef', '#ec4899'],
      borderRadius: 8,
    }]
  },
  options: {
    responsive: true,
    plugins: { legend: { labels: { color: '#f1f5f9' } } },
    scales: {
      y: { ticks: { color: '#94a3b8' }, grid: { color: 'rgba(99,102,241,0.1)' } },
      x: { ticks: { color: '#94a3b8' }, grid: { display: false } }
    }
  }
});
</script>
```

---

## Design Principles

1. **One clear message** per infographic — don't overcrowd
2. **Visual hierarchy**: Title → Key stats → Supporting data → Source
3. **Color palette**: Max 3-4 colors, use gradients for depth
4. **Typography**: Max 2 fonts, clear size hierarchy
5. **White space**: Give elements room to breathe
6. **Data integrity**: Always cite sources, don't distort scales
7. **Dimensions**: 1080px wide for social, 800px for blog, 1920px for presentation

---

## Social Media Sizes

| Platform | Infographic Size | Format |
|----------|-----------------|--------|
| Instagram Post | 1080x1350 | PNG/JPG |
| Instagram Story | 1080x1920 | PNG |
| LinkedIn Post | 1200x1500 | PNG |
| Twitter/X | 1200x675 | PNG |
| Pinterest | 1000x2100 | PNG |
| Blog | 800xAuto | PNG/SVG |

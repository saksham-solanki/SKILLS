---
name: presentation-design
description: Create beautiful slide decks and presentations using Reveal.js HTML framework. Use when user asks to create a presentation, slide deck, pitch deck, keynote, conference talk, or any visual presentation. Supports speaker notes, data visualizations in slides, and PDF export.
license: MIT
metadata:
  version: 1.0.0
  author: Sam
  category: design
  domain: presentations
  updated: 2026-02-25
  tech-stack: Reveal.js, HTML, CSS
---

# Presentation Design

Create stunning HTML presentations with Reveal.js — pitch decks, conference talks, reports.

---

## Keywords

presentation, slide deck, pitch deck, keynote, conference talk, slides, reveal.js, html presentation, speaker notes, data slides, pdf presentation, startup pitch, investor deck

---

## Quick Start

```bash
# Create a new presentation
mkdir my-presentation && cd my-presentation
npm init -y
npm install reveal.js
```

### Complete Presentation Template

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Presentation Title</title>
  <link rel="stylesheet" href="node_modules/reveal.js/dist/reveal.css">
  <link rel="stylesheet" href="node_modules/reveal.js/dist/theme/black.css">
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&family=Space+Grotesk:wght@500;600;700&display=swap');
    :root {
      --r-background-color: #0f172a;
      --r-main-font: 'Inter', sans-serif;
      --r-heading-font: 'Space Grotesk', sans-serif;
      --r-main-color: #f1f5f9;
      --r-heading-color: #ffffff;
      --r-link-color: #6366f1;
    }
    .reveal { font-family: var(--r-main-font); }
    .reveal h1, .reveal h2, .reveal h3 { font-family: var(--r-heading-font); }
    .gradient-text {
      background: linear-gradient(135deg, #6366f1, #ec4899);
      -webkit-background-clip: text; -webkit-text-fill-color: transparent;
    }
    .stat-big { font-size: 120px; font-weight: 800; line-height: 1; }
    .glass-card {
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid rgba(99, 102, 241, 0.2);
      border-radius: 16px; padding: 30px;
    }
    .columns { display: flex; gap: 30px; align-items: start; }
    .columns > * { flex: 1; }
    .tag { display: inline-block; padding: 4px 12px; border-radius: 20px;
      background: rgba(99,102,241,0.2); color: #a5b4fc; font-size: 14px; }
  </style>
</head>
<body>
<div class="reveal">
  <div class="slides">
    
    <!-- TITLE SLIDE -->
    <section>
      <h1 class="gradient-text">Your Title Here</h1>
      <p style="color: #94a3b8; font-size: 24px;">Subtitle or tagline</p>
      <p style="color: #64748b; font-size: 16px; margin-top: 40px;">
        Your Name · Company · Date
      </p>
      <aside class="notes">Speaker notes go here — only visible in speaker view (press S).</aside>
    </section>
    
    <!-- AGENDA SLIDE -->
    <section>
      <h2>Agenda</h2>
      <div style="text-align: left; max-width: 600px; margin: 0 auto;">
        <p style="padding: 15px 0; border-bottom: 1px solid rgba(99,102,241,0.2);">
          <span class="gradient-text" style="font-weight: 700;">01</span> &nbsp; Problem Statement
        </p>
        <p style="padding: 15px 0; border-bottom: 1px solid rgba(99,102,241,0.2);">
          <span class="gradient-text" style="font-weight: 700;">02</span> &nbsp; Our Solution
        </p>
        <p style="padding: 15px 0; border-bottom: 1px solid rgba(99,102,241,0.2);">
          <span class="gradient-text" style="font-weight: 700;">03</span> &nbsp; Market Opportunity
        </p>
        <p style="padding: 15px 0;">
          <span class="gradient-text" style="font-weight: 700;">04</span> &nbsp; Roadmap & Ask
        </p>
      </div>
    </section>
    
    <!-- BIG STAT SLIDE -->
    <section>
      <p class="stat-big gradient-text">73%</p>
      <p style="font-size: 24px; color: #94a3b8; max-width: 600px; margin: 20px auto;">
        of companies face this exact problem, costing the industry $4.2B annually
      </p>
    </section>
    
    <!-- TWO COLUMN SLIDE -->
    <section>
      <h2>Before & After</h2>
      <div class="columns" style="margin-top: 30px;">
        <div class="glass-card">
          <h3 style="color: #ef4444; font-size: 20px;">❌ Before</h3>
          <ul style="text-align: left; font-size: 18px; color: #94a3b8;">
            <li>Manual processes</li>
            <li>Hours of work</li>
            <li>Error-prone</li>
          </ul>
        </div>
        <div class="glass-card">
          <h3 style="color: #22c55e; font-size: 20px;">✅ After</h3>
          <ul style="text-align: left; font-size: 18px; color: #94a3b8;">
            <li>Fully automated</li>
            <li>Done in seconds</li>
            <li>99.9% accurate</li>
          </ul>
        </div>
      </div>
    </section>
    
    <!-- CTA SLIDE -->
    <section>
      <h2 class="gradient-text">Let's Talk</h2>
      <p style="font-size: 22px; color: #94a3b8;">email@example.com</p>
      <p style="margin-top: 40px;">
        <span class="tag">🚀 Available Now</span>
      </p>
    </section>
    
  </div>
</div>
<script src="node_modules/reveal.js/dist/reveal.js"></script>
<script>
  Reveal.initialize({
    hash: true,
    transition: 'slide',
    backgroundTransition: 'fade',
    controls: true,
    progress: true,
    center: true,
  });
</script>
</body>
</html>
```

---

## Controls

| Key | Action |
|-----|--------|
| → / Space | Next slide |
| ← | Previous slide |
| S | Speaker view (with notes) |
| F | Fullscreen |
| O / Esc | Overview mode |
| B / . | Black screen (pause) |

---

## Export to PDF

```bash
# Open presentation in Chrome, append ?print-pdf to URL
# Then Cmd+P → Save as PDF

# Or use decktape CLI
npm install -g decktape
decktape reveal http://localhost:8000 slides.pdf

# Automated with Puppeteer
npx capture-website "http://localhost:8000?print-pdf" --output=slides.pdf --type=pdf --width=1920 --height=1080
```

---

## Slide Types Reference

1. **Title**: Big heading + subtitle + author
2. **Agenda/TOC**: Numbered list of topics
3. **Big Stat**: One huge number + context
4. **Quote**: Blockquote with attribution
5. **Two Column**: Side-by-side comparison
6. **Image Full**: Full-bleed background image
7. **Code**: Syntax-highlighted code block
8. **Timeline**: Horizontal step progression
9. **Team**: Grid of photos + names
10. **CTA**: Call to action + contact info

---

## Best Practices

1. **One idea per slide** — never overcrowd
2. **Max 6 words per bullet point**
3. **Use speaker notes** for details (press S to see)
4. **Dark backgrounds** are easier on projectors/screens
5. **Font size minimum 24px** — must read from back of room
6. **Use fragments** for progressive reveal: `class="fragment"`
7. **Keep presentations under 20 slides** for most talks

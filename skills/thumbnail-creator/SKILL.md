---
name: thumbnail-creator
description: Create eye-catching thumbnails for YouTube, social media, and content platforms. Use when user asks to create thumbnails, YouTube thumbnails, video thumbnails, social media preview images, OG images, or click-worthy preview graphics. Includes A/B testing variations and platform-specific optimizations.
license: MIT
metadata:
  version: 1.0.0
  author: Sam
  category: design
  domain: thumbnails
  updated: 2026-02-25
  tech-stack: HTML, Canvas, CSS, Puppeteer
---

# Thumbnail Creator

Design high-CTR thumbnails for YouTube, social media, and content platforms.

---

## Keywords

thumbnail, youtube thumbnail, video thumbnail, social media thumbnail, og image, preview image, click-through rate, ctr, thumbnail design, video cover, social preview, content thumbnail, blog thumbnail

---

## Core Workflows

### Workflow 1: YouTube Thumbnail (1280×720)

**High-CTR Formula: Face + Text + Contrast + Emotion**

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@800;900&display=swap');
  * { margin: 0; padding: 0; box-sizing: border-box; }
  body { width: 1280px; height: 720px; overflow: hidden; font-family: 'Inter', sans-serif; }
  .thumbnail {
    width: 1280px; height: 720px; position: relative;
    background: linear-gradient(135deg, #0f172a 0%, #1e1b4b 50%, #0f172a 100%);
    display: flex; align-items: center; padding: 60px;
  }
  .text-side { flex: 1; z-index: 2; }
  .main-text {
    font-size: 72px; font-weight: 900; line-height: 1.1;
    color: #ffffff; text-transform: uppercase;
    text-shadow: 0 4px 20px rgba(0,0,0,0.5);
  }
  .main-text .highlight {
    background: linear-gradient(135deg, #fbbf24, #f59e0b);
    -webkit-background-clip: text; -webkit-text-fill-color: transparent;
  }
  .badge {
    display: inline-block; padding: 8px 20px; border-radius: 8px;
    background: #ef4444; color: white; font-size: 22px; font-weight: 800;
    text-transform: uppercase; margin-bottom: 15px; letter-spacing: 2px;
  }
  .subtitle {
    font-size: 28px; color: #94a3b8; font-weight: 800; margin-top: 15px;
  }
  /* Decorative elements */
  .glow-1 { position: absolute; top: -100px; right: -100px; width: 500px; height: 500px;
    background: radial-gradient(circle, rgba(99,102,241,0.3) 0%, transparent 70%); }
  .glow-2 { position: absolute; bottom: -50px; left: 200px; width: 400px; height: 400px;
    background: radial-gradient(circle, rgba(236,72,153,0.2) 0%, transparent 70%); }
  .arrow { position: absolute; right: 80px; bottom: 60px; font-size: 80px; }
</style>
</head>
<body>
<div class="thumbnail">
  <div class="glow-1"></div>
  <div class="glow-2"></div>
  <div class="text-side">
    <div class="badge">🔥 NEW</div>
    <div class="main-text">
      How I Made<br>
      <span class="highlight">$10,000</span><br>
      In One Week
    </div>
    <div class="subtitle">Step-by-step breakdown →</div>
  </div>
  <div class="arrow">👉</div>
</div>
</body>
</html>
```

### Workflow 2: Generate A/B Variations

Create 3 variations to test:

**Variation A: Bold text focus**
- Large text, minimal graphics, high contrast background
- Colors: Dark bg + bright yellow text

**Variation B: Number-driven**
- Huge number/statistic as focal point
- Supporting text smaller, contrasting color

**Variation C: Question-based**
- Provocative question as headline  
- Use "?" prominently
- Curiosity-gap style

### Workflow 3: Render HTML Thumbnail to PNG

```bash
# Using Puppeteer
npx capture-website thumbnail.html --output=thumbnail.png --width=1280 --height=720 --no-default-background

# Using Chrome headless
google-chrome --headless --screenshot=thumbnail.png --window-size=1280,720 thumbnail.html
```

```javascript
// Puppeteer script for batch rendering
const puppeteer = require('puppeteer');
async function renderThumbnail(htmlFile, outputFile) {
  const browser = await puppeteer.launch();
  const page = await browser.newPage();
  await page.setViewport({ width: 1280, height: 720 });
  await page.goto(`file://${htmlFile}`, { waitUntil: 'networkidle0' });
  await page.screenshot({ path: outputFile, type: 'png' });
  await browser.close();
}
```

---

## Thumbnail Design Rules

### DO ✅
1. **Use 3 or fewer words** for the main headline
2. **High contrast** between text and background
3. **Use faces** showing strong emotions when possible
4. **Bold, thick fonts** (min 60px for YouTube)
5. **Create visual depth** with shadows and layers
6. **Use brand-consistent colors** for recognition
7. **Keep it simple** — must read at mobile sizes (160×90)

### DON'T ❌
1. Don't use thin or light-weight fonts
2. Don't place text in the bottom-right (YouTube timestamp overlay)
3. Don't use more than 2 colors for text
4. Don't make text smaller than 48px
5. Don't clutter with too many elements
6. Don't use low-contrast color combos

---

## Platform Dimensions

| Platform | Size | Notes |
|----------|------|-------|
| YouTube | 1280×720 | 16:9, avoid bottom-right corner |
| Instagram Post | 1080×1080 | Square, preview crops to center |
| LinkedIn Article | 1200×627 | Horizontal |
| Twitter/X Card | 1200×628 | Horizontal |
| Facebook Link | 1200×630 | Horizontal |
| OG Image | 1200×630 | For website link previews |
| Blog Featured | 1200×675 | Common blog size |

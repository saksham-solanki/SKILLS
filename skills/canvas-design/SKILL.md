---
name: canvas-design
description: Create visual art, social media graphics, banners, and generative designs using HTML5 Canvas. Use when user asks to generate social media posts, cover images, banners, artistic graphics, generative art, abstract backgrounds, promotional graphics, or any visual content that needs to be exported as PNG/JPEG/WebP.
license: MIT
metadata:
  version: 1.0.0
  author: Sam
  category: design
  domain: visual-design
  updated: 2026-02-25
  tech-stack: HTML5 Canvas, JavaScript
---

# Canvas Design

Create stunning visual graphics using HTML5 Canvas — social posts, banners, generative art, promotional materials.

---

## Keywords

canvas design, social media graphics, banner design, generative art, abstract backgrounds, promotional graphics, cover image, post design, visual content, HTML5 canvas, graphic creation, social media post, instagram post, linkedin banner, twitter header

---

## Core Workflows

### Workflow 1: Social Media Post Graphic

```html
<!DOCTYPE html>
<html>
<head><meta charset="utf-8"></head>
<body>
<canvas id="canvas" width="1080" height="1080"></canvas>
<script>
const canvas = document.getElementById('canvas');
const ctx = canvas.getContext('2d');
const W = canvas.width, H = canvas.height;

// Background gradient
const bg = ctx.createLinearGradient(0, 0, W, H);
bg.addColorStop(0, '#0f172a');
bg.addColorStop(0.5, '#1e1b4b');
bg.addColorStop(1, '#0f172a');
ctx.fillStyle = bg;
ctx.fillRect(0, 0, W, H);

// Decorative circles
function drawGlowCircle(x, y, r, color, alpha) {
  const grad = ctx.createRadialGradient(x, y, 0, x, y, r);
  grad.addColorStop(0, color + Math.round(alpha * 255).toString(16).padStart(2, '0'));
  grad.addColorStop(1, color + '00');
  ctx.fillStyle = grad;
  ctx.fillRect(x - r, y - r, r * 2, r * 2);
}
drawGlowCircle(200, 200, 300, '#6366f1', 0.3);
drawGlowCircle(880, 800, 250, '#ec4899', 0.25);
drawGlowCircle(540, 540, 200, '#8b5cf6', 0.2);

// Grid overlay
ctx.strokeStyle = 'rgba(99, 102, 241, 0.06)';
ctx.lineWidth = 1;
for (let i = 0; i < W; i += 40) {
  ctx.beginPath(); ctx.moveTo(i, 0); ctx.lineTo(i, H); ctx.stroke();
  ctx.beginPath(); ctx.moveTo(0, i); ctx.lineTo(W, i); ctx.stroke();
}

// Title text
ctx.textAlign = 'center';
ctx.fillStyle = '#f1f5f9';
ctx.font = 'bold 64px Inter, sans-serif';
ctx.fillText('YOUR HEADLINE', W/2, H/2 - 40);

// Subtitle
ctx.font = '300 28px Inter, sans-serif';
ctx.fillStyle = '#94a3b8';
ctx.fillText('Supporting text goes here', W/2, H/2 + 30);

// Accent line
const lineGrad = ctx.createLinearGradient(W/2 - 100, 0, W/2 + 100, 0);
lineGrad.addColorStop(0, '#6366f1');
lineGrad.addColorStop(1, '#ec4899');
ctx.strokeStyle = lineGrad;
ctx.lineWidth = 3;
ctx.beginPath(); ctx.moveTo(W/2 - 100, H/2 + 60); ctx.lineTo(W/2 + 100, H/2 + 60); ctx.stroke();

// Brand logo area
ctx.font = '600 18px Inter, sans-serif';
ctx.fillStyle = 'rgba(241, 245, 249, 0.6)';
ctx.fillText('@yourbrand', W/2, H - 60);
</script>
</body>
</html>
```

### Workflow 2: Gradient Banner/Header

```javascript
// LinkedIn banner (1584x396) or Twitter header (1500x500)
const canvas = document.getElementById('canvas');
canvas.width = 1584; canvas.height = 396;
const ctx = canvas.getContext('2d');
const W = canvas.width, H = canvas.height;

// Mesh gradient background
const colors = [
  { x: 0, y: 0, r: 400, color: '#6366f1' },
  { x: W * 0.6, y: H, r: 350, color: '#ec4899' },
  { x: W, y: 0, r: 300, color: '#06b6d4' },
];
ctx.fillStyle = '#0f172a';
ctx.fillRect(0, 0, W, H);
colors.forEach(({ x, y, r, color }) => {
  const grad = ctx.createRadialGradient(x, y, 0, x, y, r);
  grad.addColorStop(0, color + '60');
  grad.addColorStop(1, color + '00');
  ctx.fillStyle = grad;
  ctx.fillRect(0, 0, W, H);
});

// Glassmorphism card
ctx.fillStyle = 'rgba(255, 255, 255, 0.05)';
ctx.roundRect(60, 60, W - 120, H - 120, 20);
ctx.fill();
ctx.strokeStyle = 'rgba(255, 255, 255, 0.1)';
ctx.lineWidth = 1;
ctx.roundRect(60, 60, W - 120, H - 120, 20);
ctx.stroke();

// Text
ctx.textAlign = 'left';
ctx.fillStyle = '#f1f5f9';
ctx.font = 'bold 42px Inter, sans-serif';
ctx.fillText('Your Name', 100, 180);
ctx.font = '300 22px Inter, sans-serif';
ctx.fillStyle = '#94a3b8';
ctx.fillText('Title | Company | Building awesome things', 100, 220);
```

### Workflow 3: Generative Art

```javascript
// Particle field
for (let i = 0; i < 200; i++) {
  const x = Math.random() * W;
  const y = Math.random() * H;
  const r = Math.random() * 3 + 0.5;
  const alpha = Math.random() * 0.5 + 0.1;
  ctx.beginPath();
  ctx.arc(x, y, r, 0, Math.PI * 2);
  ctx.fillStyle = `rgba(99, 102, 241, ${alpha})`;
  ctx.fill();
}

// Connect nearby particles with lines
// Wave patterns
for (let x = 0; x < W; x += 2) {
  for (let layer = 0; layer < 5; layer++) {
    const y = H/2 + Math.sin(x * 0.01 + layer * 0.5) * (50 + layer * 20) + layer * 30;
    ctx.fillStyle = `rgba(99, 102, 241, ${0.15 - layer * 0.02})`;
    ctx.fillRect(x, y, 2, H - y);
  }
}
```

---

## Export to PNG

```javascript
// In browser: right-click canvas → Save As
// Or programmatically:
const dataURL = canvas.toDataURL('image/png');
const link = document.createElement('a');
link.download = 'design.png';
link.href = dataURL;
link.click();

// High-quality JPEG
const jpegURL = canvas.toDataURL('image/jpeg', 0.95);

// WebP (smaller files)
const webpURL = canvas.toDataURL('image/webp', 0.90);
```

### Using Node.js (node-canvas)
```bash
npm install canvas
```
```javascript
const { createCanvas } = require('canvas');
const fs = require('fs');
const canvas = createCanvas(1080, 1080);
const ctx = canvas.getContext('2d');
// ... draw ...
fs.writeFileSync('output.png', canvas.toBuffer('image/png'));
```

---

## Platform Dimensions

| Platform | Type | Size |
|----------|------|------|
| Instagram Post | Square | 1080×1080 |
| Instagram Story | Vertical | 1080×1920 |
| LinkedIn Post | Landscape | 1200×627 |
| LinkedIn Banner | Banner | 1584×396 |
| Twitter/X Post | Landscape | 1200×675 |
| Twitter Header | Banner | 1500×500 |
| Facebook Post | Landscape | 1200×630 |
| Facebook Cover | Banner | 820×312 |
| YouTube Thumbnail | Landscape | 1280×720 |
| Pinterest Pin | Vertical | 1000×1500 |

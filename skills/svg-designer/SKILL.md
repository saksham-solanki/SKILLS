---
name: svg-designer
description: Design professional SVG logos, icons, illustrations, patterns, and animated graphics. Use when user asks to create logos, icons, SVG illustrations, vector graphics, icon sets, patterns, badges, or animated SVG elements. Produces clean, optimized SVG code.
license: MIT
metadata:
  version: 1.0.0
  author: Sam
  category: design
  domain: vector-graphics
  updated: 2026-02-25
  tech-stack: SVG, CSS, SVGO
---

# SVG Designer

Create professional vector graphics: logos, icons, illustrations, patterns, and animations.

---

## Keywords

svg, logo design, icon design, vector graphics, illustration, icon set, svg animation, svg pattern, badge design, svg optimization, logo creator, vector illustration, flat icon, svg logo, brand mark, monogram

---

## Core Workflows

### Workflow 1: Logo Design

**Step 1: Define Brand Parameters**
- Brand name and industry
- Style: minimal, geometric, organic, abstract, lettermark, emblem
- Colors: primary + secondary (max 3)
- Usage: web, print, app icon, favicon

**Step 2: Generate SVG Logo**

```svg
<!-- Modern Geometric Logo Example -->
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 200 200" width="200" height="200">
  <defs>
    <linearGradient id="grad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#6366f1"/>
      <stop offset="100%" style="stop-color:#ec4899"/>
    </linearGradient>
  </defs>
  <!-- Background circle -->
  <circle cx="100" cy="100" r="90" fill="url(#grad)"/>
  <!-- Abstract mark -->
  <path d="M65 130 L100 55 L135 130 L100 105 Z" fill="white" opacity="0.95"/>
  <!-- Inner detail -->
  <circle cx="100" cy="82" r="8" fill="white" opacity="0.6"/>
</svg>
```

**Step 3: Generate Variations**
- Full color version
- White/knockout version (for dark backgrounds)
- Single color version (for print)
- Favicon (16x16, 32x32)
- App icon (512x512 with padding)

### Workflow 2: Icon Set Design

**Design System for Consistent Icons:**

```svg
<!-- Icon Template: 24x24 grid, 2px stroke, round caps -->
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24"
  fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
  <!-- Icon content goes here -->
</svg>
```

**Common Icons:**

```svg
<!-- Home Icon -->
<svg viewBox="0 0 24 24" width="24" height="24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
  <path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"/>
  <polyline points="9 22 9 12 15 12 15 22"/>
</svg>

<!-- Settings/Gear Icon -->
<svg viewBox="0 0 24 24" width="24" height="24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
  <circle cx="12" cy="12" r="3"/>
  <path d="M19.4 15a1.65 1.65 0 0 0 .33 1.82l.06.06a2 2 0 0 1 0 2.83 2 2 0 0 1-2.83 0l-.06-.06a1.65 1.65 0 0 0-1.82-.33 1.65 1.65 0 0 0-1 1.51V21a2 2 0 0 1-2 2 2 2 0 0 1-2-2v-.09A1.65 1.65 0 0 0 9 19.4a1.65 1.65 0 0 0-1.82.33l-.06.06a2 2 0 0 1-2.83 0 2 2 0 0 1 0-2.83l.06-.06A1.65 1.65 0 0 0 4.68 15a1.65 1.65 0 0 0-1.51-1H3a2 2 0 0 1-2-2 2 2 0 0 1 2-2h.09A1.65 1.65 0 0 0 4.6 9a1.65 1.65 0 0 0-.33-1.82l-.06-.06a2 2 0 0 1 0-2.83 2 2 0 0 1 2.83 0l.06.06A1.65 1.65 0 0 0 9 4.68a1.65 1.65 0 0 0 1-1.51V3a2 2 0 0 1 2-2 2 2 0 0 1 2 2v.09a1.65 1.65 0 0 0 1 1.51 1.65 1.65 0 0 0 1.82-.33l.06-.06a2 2 0 0 1 2.83 0 2 2 0 0 1 0 2.83l-.06.06a1.65 1.65 0 0 0-.33 1.82V9a1.65 1.65 0 0 0 1.51 1H21a2 2 0 0 1 2 2 2 2 0 0 1-2 2h-.09a1.65 1.65 0 0 0-1.51 1z"/>
</svg>

<!-- Chart/Analytics Icon -->
<svg viewBox="0 0 24 24" width="24" height="24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
  <line x1="18" y1="20" x2="18" y2="10"/>
  <line x1="12" y1="20" x2="12" y2="4"/>
  <line x1="6" y1="20" x2="6" y2="14"/>
</svg>
```

### Workflow 3: Animated SVG

```svg
<!-- Animated Loading Spinner -->
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" width="100" height="100">
  <circle cx="50" cy="50" r="40" stroke="#e2e8f0" stroke-width="6" fill="none"/>
  <circle cx="50" cy="50" r="40" stroke="url(#spinGrad)" stroke-width="6" fill="none"
    stroke-dasharray="80 170" stroke-linecap="round">
    <animateTransform attributeName="transform" type="rotate"
      from="0 50 50" to="360 50 50" dur="1s" repeatCount="indefinite"/>
  </circle>
  <defs>
    <linearGradient id="spinGrad">
      <stop offset="0%" stop-color="#6366f1"/>
      <stop offset="100%" stop-color="#ec4899"/>
    </linearGradient>
  </defs>
</svg>

<!-- Animated Checkmark -->
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" width="100" height="100">
  <circle cx="50" cy="50" r="45" fill="#22c55e" opacity="0.15"/>
  <circle cx="50" cy="50" r="45" fill="none" stroke="#22c55e" stroke-width="3"
    stroke-dasharray="283" stroke-dashoffset="283">
    <animate attributeName="stroke-dashoffset" to="0" dur="0.5s" fill="freeze"/>
  </circle>
  <path d="M30 50 L45 65 L70 35" fill="none" stroke="#22c55e" stroke-width="4"
    stroke-linecap="round" stroke-linejoin="round"
    stroke-dasharray="60" stroke-dashoffset="60">
    <animate attributeName="stroke-dashoffset" to="0" dur="0.3s" begin="0.5s" fill="freeze"/>
  </path>
</svg>
```

### Workflow 4: SVG Patterns

```svg
<!-- Geometric Background Pattern -->
<svg xmlns="http://www.w3.org/2000/svg" width="400" height="400">
  <defs>
    <pattern id="dots" x="0" y="0" width="20" height="20" patternUnits="userSpaceOnUse">
      <circle cx="10" cy="10" r="1.5" fill="#6366f1" opacity="0.3"/>
    </pattern>
    <pattern id="grid" x="0" y="0" width="40" height="40" patternUnits="userSpaceOnUse">
      <path d="M 40 0 L 0 0 0 40" fill="none" stroke="#6366f1" stroke-width="0.5" opacity="0.1"/>
    </pattern>
  </defs>
  <rect width="100%" height="100%" fill="#0f172a"/>
  <rect width="100%" height="100%" fill="url(#grid)"/>
  <rect width="100%" height="100%" fill="url(#dots)"/>
</svg>
```

---

## SVG Optimization

```bash
# Install SVGO
npm install -g svgo

# Optimize single file
svgo input.svg -o output.svg

# Optimize with config
svgo input.svg --config='{"plugins":[{"name":"preset-default","params":{"overrides":{"removeViewBox":false}}}]}'

# Batch optimize
svgo -f ./icons/ -o ./icons-optimized/
```

---

## Design Guidelines

| Aspect | Guideline |
|--------|-----------|
| Logo viewBox | `0 0 200 200` (square) or `0 0 300 100` (horizontal) |
| Icon viewBox | `0 0 24 24` (standard) |
| Stroke width | 1.5-2px for icons at 24px |
| Min detail | Nothing smaller than 2px at display size |
| Colors | Prefer `currentColor` for icons (inherits CSS color) |
| Gradients | Use `linearGradient` or `radialGradient` with IDs |
| Accessibility | Always add `<title>` and `aria-label` |

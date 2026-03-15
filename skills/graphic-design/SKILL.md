---
name: graphic-design
description: Design systems, color palettes, typography, brand kits, and visual design fundamentals. Use when user asks about color schemes, font pairing, design tokens, brand guidelines, design systems, UI design principles, visual hierarchy, spacing systems, or needs to create a cohesive visual identity.
license: MIT
metadata:
  version: 1.0.0
  author: Sam
  category: design
  domain: design-systems
  updated: 2026-02-25
  tech-stack: CSS, Design Tokens, Figma
---

# Graphic Design Systems

Create professional design systems: color palettes, typography, spacing, brand kits, and design tokens.

---

## Keywords

graphic design, color palette, typography, font pairing, design system, brand kit, design tokens, visual hierarchy, spacing system, brand guidelines, color theory, layout grid, design principles, UI design, brand identity, style guide

---

## Core Workflows

### Workflow 1: Generate Color Palette

**Color Harmony Methods:**

```css
/* Monochromatic (one hue, varying lightness) */
:root {
  --primary-50: hsl(245, 82%, 97%);
  --primary-100: hsl(245, 82%, 93%);
  --primary-200: hsl(245, 82%, 85%);
  --primary-300: hsl(245, 82%, 73%);
  --primary-400: hsl(245, 82%, 63%);
  --primary-500: hsl(245, 82%, 53%);  /* Base color */
  --primary-600: hsl(245, 82%, 43%);
  --primary-700: hsl(245, 82%, 35%);
  --primary-800: hsl(245, 82%, 25%);
  --primary-900: hsl(245, 82%, 15%);
}

/* Complementary (opposite on color wheel) */
:root {
  --primary: hsl(245, 82%, 53%);    /* Indigo */
  --complement: hsl(65, 82%, 53%);  /* Yellow-green */
}

/* Analogous (adjacent on color wheel) */
:root {
  --color-1: hsl(225, 82%, 53%);  /* Blue */
  --color-2: hsl(245, 82%, 53%);  /* Indigo */
  --color-3: hsl(265, 82%, 53%);  /* Purple */
}

/* Triadic (evenly spaced, 120° apart) */
:root {
  --color-1: hsl(245, 82%, 53%);  /* Indigo */
  --color-2: hsl(5, 82%, 53%);    /* Red */
  --color-3: hsl(125, 82%, 53%);  /* Green */
}
```

**Curated Dark Mode Palette:**
```css
:root {
  /* Backgrounds */
  --bg-primary: #0f172a;
  --bg-secondary: #1e293b;
  --bg-tertiary: #334155;
  --bg-elevated: rgba(255, 255, 255, 0.05);
  
  /* Text */
  --text-primary: #f1f5f9;
  --text-secondary: #94a3b8;
  --text-muted: #475569;
  
  /* Accents */
  --accent-primary: #6366f1;
  --accent-secondary: #ec4899;
  --accent-success: #22c55e;
  --accent-warning: #f59e0b;
  --accent-error: #ef4444;
  
  /* Borders */
  --border-default: rgba(99, 102, 241, 0.15);
  --border-hover: rgba(99, 102, 241, 0.3);
}
```

### Workflow 2: Typography System

**Font Pairing Rules:**
1. Contrast: Pair serif heading with sans-serif body (or vice versa)
2. Keep max 2 font families
3. Use weight contrast within same family for minimal designs

**Recommended Pairings:**

| Heading | Body | Mood |
|---------|------|------|
| Playfair Display | Inter | Elegant, editorial |
| Space Grotesk | Inter | Modern, tech |
| Outfit | DM Sans | Clean, SaaS |
| Fraunces | Source Sans 3 | Premium, luxury |
| Sora | IBM Plex Sans | Professional |
| Cabinet Grotesk | Satoshi | Trendy, startup |

**Type Scale (1.250 ratio — Major Third):**
```css
:root {
  --text-xs: 0.64rem;    /* 10.24px */
  --text-sm: 0.8rem;     /* 12.8px */
  --text-base: 1rem;     /* 16px */
  --text-lg: 1.25rem;    /* 20px */
  --text-xl: 1.563rem;   /* 25px */
  --text-2xl: 1.953rem;  /* 31.25px */
  --text-3xl: 2.441rem;  /* 39.06px */
  --text-4xl: 3.052rem;  /* 48.83px */
  --text-5xl: 3.815rem;  /* 61.04px */
  
  --leading-tight: 1.2;
  --leading-normal: 1.5;
  --leading-relaxed: 1.75;
  
  --tracking-tight: -0.02em;
  --tracking-normal: 0;
  --tracking-wide: 0.05em;
}
```

### Workflow 3: Spacing System

```css
:root {
  /* 4px grid system */
  --space-0: 0;
  --space-1: 0.25rem;  /* 4px */
  --space-2: 0.5rem;   /* 8px */
  --space-3: 0.75rem;  /* 12px */
  --space-4: 1rem;     /* 16px */
  --space-5: 1.25rem;  /* 20px */
  --space-6: 1.5rem;   /* 24px */
  --space-8: 2rem;     /* 32px */
  --space-10: 2.5rem;  /* 40px */
  --space-12: 3rem;    /* 48px */
  --space-16: 4rem;    /* 64px */
  --space-20: 5rem;    /* 80px */
  --space-24: 6rem;    /* 96px */
  
  /* Border radius */
  --radius-sm: 6px;
  --radius-md: 12px;
  --radius-lg: 16px;
  --radius-xl: 24px;
  --radius-full: 9999px;
  
  /* Shadows */
  --shadow-sm: 0 1px 2px rgba(0, 0, 0, 0.05);
  --shadow-md: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
  --shadow-lg: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
  --shadow-xl: 0 20px 25px -5px rgba(0, 0, 0, 0.1);
  --shadow-glow: 0 0 30px rgba(99, 102, 241, 0.3);
}
```

### Workflow 4: Brand Kit Generator

**Output a complete brand kit as CSS + HTML reference:**
1. Logo usage guidelines (clear space, minimum size)
2. Primary & secondary color palettes with hex, RGB, HSL
3. Typography spec with Google Fonts imports
4. Button styles (primary, secondary, ghost, destructive)
5. Card/container styles
6. Icon style guidelines
7. Photography/illustration style notes

```css
/* Brand Kit — Complete Design Tokens */
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=Space+Grotesk:wght@500;600;700&display=swap');

:root {
  /* Brand Colors */
  --brand-primary: #6366f1;
  --brand-secondary: #ec4899;
  --brand-gradient: linear-gradient(135deg, var(--brand-primary), var(--brand-secondary));
  
  /* Typography */
  --font-heading: 'Space Grotesk', sans-serif;
  --font-body: 'Inter', sans-serif;
  
  /* Component Tokens */
  --button-radius: 12px;
  --card-radius: 20px;
  --input-radius: 10px;
  --card-bg: rgba(255, 255, 255, 0.05);
  --card-border: rgba(99, 102, 241, 0.15);
  
  /* Transitions */
  --transition-fast: 150ms ease;
  --transition-normal: 250ms ease;
  --transition-slow: 400ms ease;
}
```

---

## Design Principles

1. **Proximity**: Group related elements together
2. **Alignment**: Every element should have visual connection to something else
3. **Repetition**: Repeat visual elements for consistency
4. **Contrast**: Make differences obvious, not subtle
5. **Hierarchy**: Guide the eye (size → color → weight → position)
6. **White Space**: Don't fear emptiness, it adds elegance
7. **Consistency**: Same element = same style everywhere

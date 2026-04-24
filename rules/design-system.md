---
paths:
  - "components/**"
  - "styles/**"
  - "tailwind.config.ts"
  - "app/**/page.tsx"
---

# Visual Design System: Editorial Luxury

## Theme

This is NOT a dark-mode site. This is NOT a generic AI website.

- **Warm cream (#FAF8F4) is the default background.** Non-negotiable.
- Alternating sections use stone (#ECE8E1) for visual rhythm.
- Dark navy (#0C1220) sections ONLY for homepage hero and CTA sections.
- No purple. No blue-purple. No gradients. No dark theme.

## Color Palette

```
cream:          #FAF8F4   (main background)
stone:          #ECE8E1   (alternating sections, scrollbar track)
sand:           #DDD8D0   (borders, dividers, hr)
parchment:      #D9D4CC   (scrollbar thumb)

ink:            #111111   (headings, primary text)
ink-secondary:  #333330   (body text, default body color)
ink-muted:      #5C5850   (descriptions, secondary copy)
ink-faint:      #8A847D   (labels, captions, timestamps)

emerald:        #0D7C66   (accent: CTAs, links, highlights, badges)
emerald-hover:  #0A9A7E   (hover states)
emerald-deep:   #095E4E   (pressed states, inline code on light bg)
emerald-muted:  rgba(13, 124, 102, 0.08)  (badge/label backgrounds)

navy:           #0C1220   (dark section background)
navy-card:      #131B2E   (cards on dark bg)
navy-elevated:  #1A243A   (elevated surfaces on dark bg, code blocks)
navy-border:    #243048   (borders on dark bg)

positive:       #2D9D78   (success states)
negative:       #D44747   (error states)
warning:        #D4913E   (warning states)
```

## Color Rules

- Emerald ONLY for: CTAs, links, badges, section labels, metric highlights, hover borders
- NEVER use emerald as a background fill for large sections
- NEVER use gradients. Flat, solid colors only.
- Card on cream bg: `shadow-soft` + `ring-1 ring-ink/[0.04]`, not heavy shadows
- Card on dark bg: `ring-1 ring-white/[0.06]`

## Typography

Satoshi font via Fontshare CDN `@font-face` in `globals.css`. Weights: 300, 400, 500, 700, 900.

```
font-display: 'Satoshi', system-ui, sans-serif   (--font-satoshi)
font-body:    'Satoshi', system-ui, sans-serif
font-mono:    'JetBrains Mono', monospace         (--font-jetbrains)
```

**Scale (in tailwind.config.ts):**

| Token    | Size                            | Line Height | Tracking | Weight |
|----------|---------------------------------|-------------|----------|--------|
| display  | clamp(3.25rem, 6vw, 5rem)      | 1.02        | -0.04em  | 800    |
| h1       | clamp(2.25rem, 4.5vw, 3.25rem) | 1.08        | -0.03em  | 700    |
| h2       | clamp(1.75rem, 3vw, 2.25rem)   | 1.15        | -0.02em  | 700    |
| h3       | clamp(1.25rem, 2vw, 1.5rem)    | 1.35        | -0.005em | 600    |
| body-lg  | 1.125rem (18px)                | 1.8         | normal   | 400    |
| body     | 1.0625rem (17px)               | 1.8         | normal   | 400    |
| caption  | 0.8125rem (13px)               | 1.4         | 0.06em   | 500    |
| small    | 0.9375rem (15px)               | 1.6         | normal   | 400    |

**Typography rules:**
- Headlines: tight negative letter-spacing for premium feel
- Body line-height: 1.8 (generous for readability on cream)
- ALL CAPS only for section labels, badges, eyebrow text. Never for sentences.
- JetBrains Mono only for: code blocks, terminal mockups, inline code, system labels

## Border Radius

```
sm: 6px (badges) | md: 10px (buttons) | lg: 16px (cards)
xl: 24px | 2xl: 32px | pill: 9999px (CTAs, section labels)
btn: 10px | card: 16px | badge: 6px
```

## Shadows

```
soft:       0 2px 8px rgba(26,26,26,0.04), 0 1px 2px rgba(26,26,26,0.03)    (default card)
medium:     0 8px 24px rgba(26,26,26,0.06), 0 2px 6px rgba(26,26,26,0.04)   (hover card)
elevated:   0 16px 48px rgba(26,26,26,0.08), 0 4px 12px rgba(26,26,26,0.04) (browser/terminal frames)
inner-glow: inset 0 1px 1px rgba(255,255,255,0.6)                            (premium card inner)
emerald:    0 4px 16px rgba(13, 124, 102, 0.15)                              (emerald CTA hover)
```

## Animations (in tailwind.config.ts)

- `fade-up`: 0.8s, translateY(24px) to 0, blur(4px) to 0
- `fade-in`: 0.6s opacity
- `marquee`: 25s linear infinite translateX
- `pulse-soft`: 3s ease-in-out opacity
- `flow`: 3s translateX(-100%) to translateX(100%)
- `draw`: 2s strokeDashoffset for SVG
- `shimmer`: 2s background-position shift
- `float`: 6s translateY(0) to -8px

Keep interactive animations under 300ms. No parallax. No heavy scroll animations.

## Icons

- Lucide React (outline style, 1.5-2px stroke)
- NO emojis as icons anywhere

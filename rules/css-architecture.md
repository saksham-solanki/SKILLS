---
paths:
  - "styles/**"
  - "*.css"
  - "tailwind.config.ts"
---

# CSS Architecture

## Global Styles (`styles/globals.css`)

**Layer: base**
- Box-sizing reset, smooth scroll, antialiased rendering
- Body: Satoshi font, `#FAF8F4` background, `#333330` text, line-height 1.75
- Selection: emerald tint
- Custom scrollbar (stone track, parchment thumb)

**Layer: components**

| Class               | Purpose                                                                    |
|---------------------|----------------------------------------------------------------------------|
| `.section-padding`  | `py-16 sm:py-20 lg:py-24`                                                 |
| `.section-padding-sm`| `py-12 sm:py-16 lg:py-20`                                                |
| `.container-width`  | `max-w-container mx-auto px-5 sm:px-8` (1280px)                           |
| `.container-narrow` | `max-w-narrow mx-auto px-5 sm:px-8` (720px)                               |
| `.section-label`    | Pill eyebrow: emerald text, emerald-muted bg, rounded-pill, uppercase      |
| `.card-premium`     | Double-bezel outer: `bg-white/60 rounded-xl p-1 ring-1 ring-ink/[0.04]`   |
| `.card-premium-inner`| Double-bezel inner: `bg-white rounded-[calc(0.75rem-4px)] p-6 sm:p-8 shadow-inner-glow` |
| `.card-cream`       | Card on cream: white, shadow-soft, ring-1, hover: shadow-medium + emerald  |
| `.card-dark`        | Card on navy: navy-card, ring-1 ring-white/[0.06], hover: ring-emerald/30  |
| `.browser-frame`    | Browser window chrome wrapper                                              |
| `.terminal-frame`   | Terminal window chrome wrapper                                             |
| `.dark-section`     | `bg-navy text-white`                                                       |
| `.noise-overlay`    | Fixed noise texture at 2.5% opacity                                        |
| `.prose-light`      | MDX typography on cream backgrounds                                        |
| `.prose-dark`       | MDX typography on dark backgrounds                                         |